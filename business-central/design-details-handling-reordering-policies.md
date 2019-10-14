---
title: Designoplysninger – Håndtering af genbestillingsmetoder | Microsoft Docs
description: Oversigt over opgaver til at definere en genbestillingsmetode i forsyningsplanlægning.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 53d9d0ff2d9d1f42bb7f9c05ed49aa4df20f2a92
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307152"
---
# <a name="design-details-handling-reordering-policies"></a>Designoplysninger: Håndtering af genbestillingsmetoder
En genbestillingsmetode skal defineres for, at en vare kan være en del af forsyningsplanlægning. Der findes følgende fire genbestillingsmetoder:  

* Fast genbestil.antal  
* Maks. antal  
* Ordre  
* Lot-for-Lot  

Fast genbestil.antal- og Maks. antal-metoder, der er relateret til lagerplanlægning. Selvom lagerplanlægning er teknisk enklere end udligningsproceduren, skal disse politikker fungere sammen med den trinvise afstemning af forsyning og ordresporing. For at styre integrationen mellem de to og for at give indsigt i den involverede planlægningslogik styrer strenge principper, hvordan genbestillingsmetoder håndteres.  

## <a name="the-role-of-the-reorder-point"></a>Genbestillingspunktets rolle
Udover den generelle afstemning af udbud og efterspørgsel, skal planlægningssystemet også overvåge lagerniveauer for de pågældende varer for at respektere de definerede genbestillingsmetoder.  

Et genbestillingspunkt repræsenterer behov under leveringstid. Når den projekterede lagerbeholdning kommer under den lagerbeholdning, der er defineret af genbestillingspunktet, er det tid til at bestille mere. I mellemtiden forventes lagerføring at reduceres gradvist og eventuelt nå nul (eller sikkerhedslagerniveau), indtil genopfyldningen ankommer.  

Planlægningssystemet vil derfor foreslå en forsyningsordre, der er planlagt fremad, når den forventede lagerbeholdning er under genbestillingspunktet.  

Genbestillingspunktet afspejler et bestemt lagerniveau. Lagerniveauer kan dog flytte betydeligt under intervallet, og planlægningssystemet skal derfor hele tiden overvåge den forventede disponible beholdning.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Overvågning af det forventede lagerniveau og genbestillingspunktet
Lageret er en slags forsyning, men for lagerplanlægning skelner planlægningssystemet mellem to lagerniveauer:  

* Planlagt beholdning  
* Forventet disponibel beholdning  

### <a name="projected-inventory"></a>Planlagt beholdning  
Oprindeligt er planlagt lagerbeholdning mængden af bruttolager, herunder forsyning og behov i fortiden, selvom det ikke er bogført, når du starter planlægningsprocessen. I fremtiden bliver det et bevægeligt planlagt lagerniveau, der vedligeholdes af bruttomængder fra fremtidig forsyning og behov, fordi det føres langs tidslinjen (uanset om det er reserveret eller på andre måder tildelt).  

Den planlagte beholdning bruges af systemet til at overvåge genbestillingspunktet og bestemme genbestillingsantallet, når du bruger genbestillingsmetoden Maks. antal.  

### <a name="projected-available-inventory"></a>Forventet disponibel beholdning  
Den forventede disponible beholdning er en del af det planlagte lager, der er tilgængeligt til at opfylde behov på et givet tidspunkt. Den forventede disponible beholdning der bruges af planlægningssystemet ved overvågning af niveauet for sikkerhedslageret.  

Den forventede disponible beholdning bruges i planlægningssystemet til at overvåge niveauet for sikkerhedslageret, da sikkerhedslageret altid skal være tilgængeligt til at afhjælpe uventede behov.  

### <a name="time-buckets"></a>Intervaller  
Det er afgørende at have streng kontrol med den forventede lagerbeholdning for at registrere, når genbestillingspunktet nås eller passeres, og for at beregne det korrekte ordreantal, når du bruger genbestillingsmetoden Maks. antal.  

Som tidligere nævnt beregnes den forventede lagerbeholdning i starten af planlægningsperioden. Det er et bruttoniveau, der ikke medtager reservationer og lignende fordelinger. Systemet overvåger de aggregerede ændringer over en tidsperiode, et interval, for at overvåge dette lagerniveau under planlægningssekvensen. Systemet sikrer, at tidsintervallet er mindst én dag, da det er den mest nøjagtige tidsenhed for en behovs- eller forsyningshændelse.  

### <a name="determining-the-projected-inventory-level"></a>Bestemmelse af det forventede lagerniveau  
Følgende sekvens beskriver, hvordan det planlagte lagerniveau bestemmes:  

* Når en forsyningshændelse, f.eks. en indkøbsordre, er blevet fuldstændig planlagt, øges den projekterede lagerbeholdning på forfaldsdatoen.  
* Når en behovshændelse har opfyldt behovet, formindskes den projekterede lagerbeholdning ikke straks. Der bogføres i stedet en påmindelse om reducering, som er en intern post, der indeholder dato og mængdebidrag til den planlagte lagerbeholdning.  
* Når en efterfølgende forsyningshændelse planlægges og placeres på tidslinjen, undersøges de bogførte reduktionsrykkerne én efter én indtil den planlagte dato for levering, mens den projekterede lagerbeholdning opdateres. Under denne proces kan niveauet for genbestillingspunktet for den interne forøgelse blive nået eller passeret.  
* Hvis der er indført en ny forsyningsordre, kontrollerer systemet, om den er indtastet før den aktuelle forsyning. Hvis det er, bliver den nye forsyning den aktuelle forsyning, og den udlignende procedure starter forfra.  

Nedenstående viser en grafisk illustration af dette princip:  

![Bestemme det planlagte lagerniveau](media/nav_app_supply_planning_2_projected_inventory.png "Bestemme det planlagte lagerniveau")  

1. Forsyning **Sa** af 4 (faste) lukker behov **Da** af -3.  
2. CloseDemand: Opret en påmindelse om reducering af -3 (ikke vist).  
3. Forsyning **Sa** er lukket med et overskud på 1 (der findes ingen yderligere behov).  

     Dette øger det forventede lagerniveau til +4, mens den forventede **disponible** beholdning bliver -1.  

4. Den næste forsyning **Sb** af 2 (en anden ordre) er allerede placeret på tidslinjen.  
5. Systemet kontrollerer, om der er påmindelse om reducering før **Sb** (det er der ikke, så ingen handling).  
6. Systemet lukker forsyning **Sb** (der findes ingen yderligere behov) – enten A: ved at reducere den til 0 (annullere) eller B: ved at lade den være.  

     Dette øger den projekterede lagerbeholdning (A: +0 => +4 eller B: +2 = +6).  

7. Systemet foretager endelig kontrol: Er der nogen påmindelse om reducering? Ja, der er en på datoen for **Da**.  
8. Systemet føjer reduktionsrykkeren af -3-rykker til det planlagte lagerniveau enten A: +4 -3 = 1 eller B: +6 -3 = +3.  
9. I tilfælde af A opretter systemet en fremad planlagt ordre fra datoen **Da**.  

     Genbestillingspunktet er ikke nået i B, og der oprettes ingen ny ordre.

## <a name="the-role-of-the-time-bucket"></a>Intervallets rolle
Formålet med intervallet er at indsamle behovshændelser inden for tidssiden for at oprette en fælles forsyningsordre.  

For genbestillingspolitikker, der bruger et genbestillingspunkt, kan du angive et interval. Dette sikrer, at behov inden for den samme tidsperiode er akkumuleret, før du tjekker indvirkningen på den forventede lagerbeholdning, og om genbestillingspunktet er blevet overskredet. Hvis genbestillingspunktet er overskredet, er en ny forsyningsordre planlagt fremad fra udgangen af den periode, der er defineret i intervallet. Intervaller starter på den planlagte startdato.  

Begrebet interval afspejler den manuelle proces til hyppig kontrol af lagerniveauet i stedet for hver transaktion. Brugeren skal definere frekvensen (intervallet). Brugeren samler f.eks. alle varebehov fra en kreditor for at foretage en ugentlig bestilling.  

![Eksempel på interval ved planlægning](media/nav_app_supply_planning_2_reorder_cycle.png "Eksempel på interval ved planlægning")  

Intervallet bruges normalt til at undgå en overlapningseffekt. For eksempel en afstemt række af behov og forsyning, hvor et tidligt behov annulleres, eller et ny oprettes. Resultatet ville være, at hver forsyningsordre (undtagen den sidste) skal omplanlægges.

## <a name="staying-under-the-overflow-level"></a>Forblive under overløbsniveauet
Når du bruger metoderne Maks. antal og Fast genbestil.antal, fokuserer planlægningssystemet kun på den planlagte lagerbeholdning i det angivne tidsinterval. Det betyder, at planlægningssystemet kan foreslå overflødig forsyning, når der forekommer negative behovs- eller positive forsyningsændringer uden for det angivne tidsinterval. Hvis der derfor foreslås en overflødig forsyning, beregner planlægningssystemet, hvilket antal forsyningen skal reduceres til (eller slettes) for at undgå overflødig forsyning. Dette antal kaldes "overløbsniveauet". Overløbet kommunikeres som en planlægningslinje med en handling i form af **Ret antal (reducering)** eller **Annuller** og følgende advarselsmeddelelse:  

*Bemærk: Den forventede lagerbeholdning [xx] er højere end overløbsniveauet [xx] på forfaldsdatoen [xx].*  

![Lageroverløbsniveau](media/supplyplanning_2_overflow1_new.png "Lageroverløbsniveau")  

###  <a name="calculating-the-overflow-level"></a>Beregning af overløbsniveau  
Overløbsniveauet beregnes på forskellige måder afhængig af planlægningsopsætningen.  

#### <a name="maximum-qty-reordering-policy"></a>Maksimalt antal som genbestillingsmetode  
Overløbsniveau = Maks. lagerbeholdning  

> [!NOTE]  
>  Hvis der findes en min. ordrestørrelse bliver den tilføjet som følger: overløbsniveau = maks. lagerbeholdning + min. ordrestørrelse.  

#### <a name="fixed-reorder-qty-reordering-policy"></a>Fast genbestil.antal-genbestillingsmetode  
Overløbsniveau = Ordrekvantum + Genbestillingspunkt  

> [!NOTE]  
>  Hvis den mindste ordrestørrelse er højere end genbestillingspunktet, vil det erstatte på følgende måde: Overløbsniveau = genbestil.antal + min. ordrestørrelse  

#### <a name="order-multiple"></a>Oprundingsfaktor  
Hvis en ordre findes flere gange, vil den justere overløbsniveauet for både maks. og fast genbestillingsantal som genbestillingsmetoder.  

###  <a name="creating-the-planning-line-with-overflow-warning"></a>Oprettelse af planlægningslinjen med overløbsadvarsel  
Når en eksisterende forsyning medfører, at den projekterede lagerbeholdning bliver større end overløbsniveauet ved slutningen af et interval, oprettes der en planlægningslinje. For at advare om potentiel overflødig levering indeholder planlægningslinjen en advarselsmeddelelse, feltet **Accepter aktionsmeddelelse** er ikke markeret, og aktionsmeddelelsen er enten Annuller eller Ret antal.  

#### <a name="calculating-the-planning-line-quantity"></a>Beregning af antallet af planlægningslinjer.  
Planlægning af linjeantallet = aktuel forsyningsmængde – (projekteret lagerbeholdning – overløbsniveau)  

> [!NOTE]  
>  Som med alle advarselslinjer vil alle maksimale/minimale ordremængder eller oprundingsfaktorer blive ignoreret.  

#### <a name="defining-the-action-message-type"></a>Definition af aktionsmeddelelsestypen  

-   Hvis antallet på planlægningslinjen er højere end 0, er aktionsmeddelelsen Ret antal  
-   Hvis antallet på planlægningslinjen er lig med eller mindre end 0, er aktionsmeddelelsen Annuller  

#### <a name="composing-the-warning-message"></a>Oprettelse af advarselsmeddelelsen  
I forbindelse med overløb vises der på siden **Ikke-sporede planlægningselementer** en advarsel med følgende oplysninger:  

-   Det planlagte lagerniveau, der udløste advarslen  
-   Det beregnede overløbsniveau  
-   Forfaldsdatoen for forsyningshændelsen.  

Eksempel: "Den planlagte beholdning 120 er større end overløbsniveauet 60 på 28-01-11"  

### <a name="scenario"></a>Scenarie  
I dette scenario ændrer en kunde en salgsordre fra 70 til 40 stykker mellem to kørsler af planlægning. Overløbsfunktionen begynder at reducere det køb, der blev foreslået for det oprindelige salgsantal.  

#### <a name="item-setup"></a>Vareopsætning  

|Genbestillingsmetode|Maks. antal|  
|-----------------------|------------------|  
|Maks. ordrestørrelse|100|  
|Genbestillingspunkt|50|  
|Lagerbeholdning|80|  

#### <a name="situation-before-sales-decrease"></a>Situationen før salgsreducering  

|Hændelse|Ret antal|Planlagt beholdning|  
|-----------|-----------------|-------------------------|  
|Dag et|Ingen|80|  
|Salg|-70|10|  
|Slutning på interval|Ingen|10|  
|Foreslå ny købsordre|+90|100|  

#### <a name="situation-after-sales-ddecrease"></a>Situationen efter salgsreducering  

|Ændring|Ret antal|Planlagt beholdning|  
|------------|-----------------|-------------------------|  
|Dag et|Ingen|80|  
|Salg|-40|40|  
|Køb|+90|130|  
|Slutning på interval|Ingen|130|  
|Foreslå at reducere køb<br /><br /> ordre fra 90 til 60|-30|100|  

#### <a name="resulting-planning-lines"></a>Resulterende planlægningslinjer  
 Der oprettes en planlægningslinje (advarsel) for at reducere køb med 30 fra 90 til 60 for at bevare den projekterede lagerbeholdning på 100 i henhold til overløbsniveauet.  

![Planlægge efter overløbsniveau](media/nav_app_supply_planning_2_overflow2.png "Planlægge efter overløbsniveau")  

> [!NOTE]  
>  Uden overløbsfunktionen vises der ingen advarsel, hvis den projekterede lagerbeholdning ligger over maks. Dette kan medføre en overflødig forsyning på 30.

## <a name="handling-projected-negative-inventory"></a>Håndtering af forventet negativt lager
Genbestillingspunktet udtrykker det forventede behov under leveringstiden for varen. Når genbestillingspunktet er overskredet, er det tid til at bestille mere. Men den forventede lagerbeholdning skal være stor nok til at dække behovet, indtil den nye ordre er modtaget. I mellemtiden bør sikkerhedslageret tage højde for udsving i behov op til et målrettet serviceniveau.  

 Derfor anser planlægningssystemet det for en nødsituation, hvis et fremtidigt behov ikke kan dækkes fra den forventede lagerbeholdning, eller udtrykt på en anden måde, hvis den forventede lagerbeholdning bliver negativ. Systemet håndterer en sådan undtagelse ved at foreslå en ny forsyningsordre for at imødekomme en del af det behov, som ikke kan opfyldes af lagerbeholdningen eller andre forsyninger. Ordrestørrelsen på den nye forsyningsordre vil ikke tage det maksimale lager eller genbestillingsantal i betragtning og vil heller ikke tage ordremodifikatorerne Maks. ordrestørrelse, Min. ordrestørrelse og Oprundingsfaktor i betragtning. I stedet afspejler den nøjagtig mangel.  

 Planlægningslinjen for denne type forsyningsordre viser et Nødsituation-advarselsikon, og yderligere oplysninger kan findes ved opslag for at informere brugeren om situationen.  

 I følgende illustration repræsenterer forsynings-id en akutordre for at justere for negativt lager.  

 ![Planlægningsforslag om at undgå negativt lager i nødsituation](media/nav_app_supply_planning_2_negative_inventory.png "Planlægningsforslag om at undgå negativt lager i nødsituation")  

1.  Forsyning **A**, oprindeligt planlagte lagerbeholdning, er under genbestillingspunkt.  
2.  En ny ordre, der er planlagt fremad, oprettes (**C**).  

     (Antal = Maks. lagerbeholdning – Forventet lagerbeholdning)  
3.  Forsyning **A** er lukket af behov **B**, som ikke fuldt ud dækkes.  

     (Behov **B** kunne forsøge at planlægge forsyning C, men det vil ikke ske i overensstemmelse med intervalkonceptet).  
4.  Ny forsyning (**D**) er oprettet for at dække det resterende antal efter behov **B**.  
5.  Behov **B** er lukket (oprettelse af en påmindelse til den forventede lagerbeholdning).  
6.  Den nye forsyning **D** er lukket.  
7.  Planlagt lagerbeholdning kontrolleres, og genbestillingspunkt er ikke krydset.  
8.  Forsyning **C** er lukket (der findes ingen yderligere behov).  
9. Sidste kontrol: Der findes ingen udestående påmindelser om lagerniveau.  

> [!NOTE]  
>  Trin 4 afspejler, hvordan systemet reagerer i versioner tidligere end Microsoft Dynamics NAV 2009 SP1.  

Dette afslutter beskrivelsen af de centrale principper vedrørende lagerplanlægning baseret på genbestillingsmetoder. I følgende afsnit beskrives karakteristika for de fire understøttede genbestillingsmetoder.

## <a name="reordering-policies"></a>Genbestillingsmetoder
Genbestillingsmetoder definerer hvor meget der skal bestilles, når varen skal genbestilles. Der findes fire forskellige genbestillingsmetoder.  

### <a name="fixed-reorder-qty"></a>Fast genbestil.antal
Fast genbestil.antal er relateret til lageret, planlægning af typiske C-varer (lav lageromkostning, lav risiko for forældelse og/eller mange varer). Denne metode bruges normalt i forbindelse med et genbestillingspunkt, hvilket afspejler det forventede behov under leveringstiden for varen.  

#### <a name="calculated-per-time-bucket"></a>Beregnet pr. interval  
Hvis planlægningssystemet har registreret, at genbestillingspunktet er nået eller overskredet i et bestemt interval (genbestillingscyklus) – over eller ved genbestillingspunktet i begyndelsen af perioden og under eller ved genbestillingspunktet sidst i perioden – vil den foreslå at oprette en ny forsyningsordre af det angivne genbestillingsantal og planlægge det fremad fra den første dag efter slutningen af intervallet.  

Det tidsbegrænsede genbestillingspunkt reducerer antallet af forsyningsforslag. Dette afspejler den manuelle proces, der består i ofte at gå gennem lageret for at kontrollere det faktiske indhold på de forskellige placeringer.  

#### <a name="creates-only-necessary-supply"></a>Opretter kun nødvendige forsyninger  
Før der foreslås, at en ny forsyningsordre opfylder et genbestillingspunkt, kontrollerer planlægningssystemet, om forsyning allerede er bestilt til modtagelse inden for varens leveringstid. Hvis en eksisterende forsyningsordre kan løse problemet ved at bringe den projekterede lagerbeholdning til eller over genbestillingspunktet inden for leveringstiden, vil systemet ikke foreslå en ny forsyningsordre.  

Forsyningsordrer, der er oprettet specielt med henblik på at opfylde genbestillingspunktet, er udelukket fra almindelig forsyningsafstemning og vil ikke på nogen måde blive ændret bagefter. Hvis en vare, der bruger genbestillingspunktet skal udfases (ikke genbestilt), er det derfor hensigtsmæssigt at gennemgå udestående forsyningsordrer manuelt eller ændre genbestillingsmetoden til lot-for-lot, hvorved systemet vil reducere eller annullere overflødige forsyninger.  

#### <a name="combines-with-order-modifiers"></a>Kombineres med ordremodifikatorer  
Ordremodifikatorerne Min. ordrestørrelse, Maks. ordrestørrelse og Oprundingsfaktor bør ikke spille en stor rolle, når metoden for fast genbestillingsantal bruges. Dog tager planlægningssystemet stadig højde for disse modifikatorer og vil reducere antallet til det angivne maksimale ordreantal (og oprette to eller flere forsyninger for at nå det samlede ordreantal), øge ordren til den angivne minimummængde eller runde ordreantallet op for at opfylde en bestemt oprundingsfaktor.  

#### <a name="combines-with-calendars"></a>Kombinerer med kalendere  
Før der bliver foreslået en ny forsyningsordre for at opfylde et genbestillingspunkt, kontrollerer planlægningssystemet, om ordren er planlagt til en ikkearbejdsdag i overensstemmelse med de kalendere, der er defineret i feltet **Basiskalenderkode** på siderne **Virksomhedsoplysninger** og **Lokationskort**.  

Hvis den planlagte dato er en ikkearbejdsdag, flytter planlægningssystemet ordren frem til den nærmeste arbejdsdag. Det kan resultere i en ordre, der opfylder et genbestillingspunkt, men ikke opfylder visse specifikke behov. Planlægningssystemet opretter en ekstra levering for sådanne behov.  

#### <a name="should-not-be-used-with-forecast"></a>Bør ikke bruges med forecast  
Det er ikke nødvendigt at medtage en prognose i planlægningen af en vare ved hjælp af et genbestillingspunktet, fordi det forventede behov allerede er angivet i genbestillingspunktet. Hvis det er relevant at basere planen på et forecast, kan du bruge politikken lot-for-lot.  

#### <a name="must-not-be-used-with-reservations"></a>Må ikke anvendes med reservationer  
Hvis brugeren har reserveret en mængde, for eksempel et antal på lageret, til nogle fremtidige behov, bliver grundlaget for planlægningen forstyrret. Selvom det planlagte beholdningsniveau er acceptabelt i relation til genbestillingspunktet, er mængderne muligvis ikke tilgængelige. Systemet kan forsøge at kompensere for dette ved at oprette undtagelsesordrer. Det anbefales dog, at feltet Reserver angives til Aldrig på varer, der er planlagt ved hjælp af et genbestillingspunkt.

### <a name="maximum-qty"></a>Maks. antal
Det maksimale antal er en måde at vedligeholde lageret ved hjælp af et genbestillingspunkt.  

Alt om den faste genbestillingsantalmetode gælder også for denne metode. Den eneste forskel er omfanget af den foreslåede forsyning. Når metoden med maksimalt antal bruges, defineres genbestillingsantallet dynamisk baseret på det planlagte lagerniveau og varierer derfor normalt fra ordre til ordre.  

#### <a name="calculated-per-time-bucket"></a>Beregnet pr. interval  
Genbestillingsantallet bestemmes på det tidspunkt (slutningen af et interval), hvor planlægningssystemet registrerer, at genbestillingspunktet er passeret. På dette tidspunkt måler systemet afstanden fra den nuværende forventede lagerbeholdning op til den angivne maksimale lagerbeholdning. Dette består af det antal, der skal genbestilles. Derefter kontrollerer systemet, om leveringen allerede er bestilt andre steder med henblik på at blive modtaget inden for leveringstiden, og i så fald reduceres mængden af den nye forsyningsordre med allerede bestilte antal.  

Systemet sikrer, at den projekterede lagerbeholdning mindst når genbestillingsniveauet – i tilfælde af at brugeren har glemt at angive et maksimalt lagerantal.  

#### <a name="combines-with-order-modifiers"></a>Kombineres med ordremodifikatorer  
Afhængigt af opsætningen, kan det være bedst at kombinere metoden Maks. antal med ordremodifikatorer for at sikre et mindste ordreantal eller afrunde til et heltal af købsmåleenheder eller opdele det i flere lotter, som er defineret af det højst tilladte antal.  

### <a name="combines-with-calendars"></a>Kombinerer med kalendere  
Før der bliver foreslået en ny forsyningsordre for at opfylde et genbestillingspunkt, kontrollerer planlægningssystemet, om ordren er planlagt til en ikkearbejdsdag i overensstemmelse med de kalendere, der er defineret i feltet **Basiskalenderkode** på siderne **Virksomhedsoplysninger** og **Lokationskort**.  

Hvis den planlagte dato er en ikkearbejdsdag, flytter planlægningssystemet ordren frem til den nærmeste arbejdsdag. Det kan resultere i en ordre, der opfylder et genbestillingspunkt, men ikke opfylder visse specifikke behov. Planlægningssystemet opretter en ekstra levering for sådanne behov.

### <a name="order"></a>Sorteringsrækkefølge
I et Fremstil-til-ordre-miljø bliver en vare købt eller produceret udelukkende til at dække et bestemt behov. Normalt relateres det til A-varer, og motivationen for at vælge denne ordregenbestillingsmetode kan være, at behovet er sjældent, leveringstiden er ubetydelig, eller de påkrævede attributter varierer.  

Programmet opretter et ordre-til-ordre-link, der fungerer som en indledende forbindelse mellem forsyningen, en forsyningsordre eller lager og det behov, som den eller det skal opfylde.  

Bortset fra brug af prdrepolitikken, kan ordre-til-ordre-linket anvendes under planlægningen på følgende måder:  

* Når produktionsmetoden Fremstil-til-ordre bruges til at oprette produktionsordrer med flere niveauer eller produktionsordrer af projekttype (fremstilling af nødvendige komponenter på den samme produktionsordre).  
* Når funktionen Salgsordreplanlægning bruges til at oprette en produktionsordre fra en salgsordre.  

Selvom en produktionsvirksomhed anser sig selv som værende et Fremstil-til-ordre-miljø, kan det være bedst at bruge en genbestillingsmetode med lot-for-lot, hvis varerne er ren standard uden variation i attributter. Som resultat vil systemet bruge ikke-planlagt lagerbeholdning og akkumulerer kun salgsordrer med samme afsendelsesdato eller inden for et defineret interval.  

#### <a name="order-to-order-links-and-past-due-dates"></a>Ordre-til-ordre-links og overskredne datoer  
I modsætning til de fleste forsyning-behov-sæt, planlægges tilknyttede ordrer med forfaldsdatoer, før planlægningsstartdatoen er fuldt planlagt af systemet. Forretningsårsagen til denne undtagelse er, at bestemte behov-forsyningssæt skal synkroniseres til kørsel. Du kan finde flere oplysninger om den fastlåste zone, der gælder for de fleste behovsforsyningstyper i [Designoplysninger: Håndtering af ordrer før planlægningsstartdatoen](design-details-dealing-with-orders-before-the-planning-starting-date.md).

### <a name="lot-for-lot"></a>Lot-for-Lot
Lot-for-lot-politik er den mest fleksible, fordi systemet kun reagerer på det faktiske behov, plus det fungerer på forventet behov fra prognose og rammeordrer og udligner derefter ordreantallet på baggrund af behovet. Lot-for-lot-politik tager sigte på A - og B-varer, hvor lageret kan accepteres, men bør undgås.  

På nogle måder ser lot-for-lot politik ud som ordrepolitikken, men der er en generisk tilgang til varer: Den kan acceptere antal på lager, og den kombinerer behov og tilsvarende forsyning i intervaller, der er defineret af brugeren.  

Intervallet er defineret i feltet **Interval**. Systemet fungerer med et mindste interval på én dag, da det er den mindste tidsenhed på behovs- og forsyningshændelser i systemet (selvom tidsenheden på produktionsordrer og komponentbehov i praksis kan være sekunder).  

Intervallet angiver også grænser for, hvornår en eksisterende forsyningsordre bør omplanlægges for at opfylde et bestemt behov. Hvis forsyningen ligger i intervallet, bliver den flyttet ind eller ud for at opfylde behovet. Hvis den ligger tidligere, vil det medføre unødvendig ophobning af lageret og skal annulleres. Hvis den ligger senere, oprettes en ny forsyningsordre i stedet.  

Med denne politik er det også muligt at definere et sikkerhedslager for at kompensere for mulige udsving i udbud eller for at imødekomme pludselige behov.  

Da forsyningsordreantallet er baseret på det faktiske behov, kan det være smart at bruge ordremodifikatorer: Rund ordreantallet op, så det passer med en specifik oprundingsfaktor (eller købsenhedskoden), forøg ordren til et fastsat minimumsordreantal, eller reducer antallet til det angivne maksimale antal (og opret derefter to eller flere forsyninger for at nå det nødvendige samlede antal).

## <a name="see-also"></a>Se også  
[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
[Designoplysninger: Tabellen Planlægningsopgave](design-details-planning-assignment-table.md)   
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
