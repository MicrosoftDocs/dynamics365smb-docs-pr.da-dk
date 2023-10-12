---
title: Designoplysninger - Håndtering af genbestillingsmetoder
description: 'Denne artikel giver et overblik over de genbestillingsmetoder, du kan bruge i forsyningsplanlægning.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/24/2023
ms.custom: bap-template
---
# Designoplysninger: Håndtering af genbestillingsmetoder

Hvis du vil medtage en vare i forsyningsplanlægningen, skal du angive en genbestillingsmetode for den på **varekort**-siden. Der findes følgende fire genbestillingsmetoder:  

* Fast genbestil.antal  
* Maks. antal  
* Sorteringsrækkefølge  
* Lot-for-Lot  

Politikmetoderne **Fast genbestil.antal** og **Maks. antal**, der er relateret til lagerplanlægning. Disse politikker findes sammen med den trinvise balance mellem levering og ordresporing.  

## Genbestillingspunktets rolle

Et genbestillingspunkt repræsenterer behov under leveringstid. Når den projekterede lagerbeholdning kommer under den lagerbeholdning, der er defineret af genbestillingspunktet, er det tid til at bestille mere. Lagerbeholdningen reduceres gradvist, indtil genopfyldningen ankommer. Den kan nå nul eller sikkerhedsniveauet. Planlægningssystemet vil derfor foreslå en forsyningsordre, der er planlagt fremad, når den forventede lagerbeholdning er under genbestillingspunktet.  

Lagerniveauer kan bevæges væsentligt i tids filsættet. Derfor overvåger planlægningssystemet konstant tilgængelig beholdning.

## Overvågning af det forventede lagerniveau og genbestillingspunktet

Lageret er en slags forsyning, men for lagerplanlægning skelner planlægningssystemet mellem to lagerniveauer:  

* Planlagt beholdning  
* Forventet disponibel beholdning  

### Planlagt beholdning  

I starten af planlægningsprocessen er planlagt beholdning bruttomængden af lager. Brutto antallet omfatter bogført og ikke-bogført udbud og efterspørgsel i fortiden. Denne mængde bliver til projekteret lageropgørelse, som bruttomængder fra fremtidig udbud og efterspørgselsvedligehold. Fremtidig levering og efterspørgsel introduceres langs tidslinjen, uanset om de reserveres eller allokeres på andre måder.  

Den planlagte beholdning bruges af systemet til at overvåge genbestillingspunktet og bestemme genbestillingsantallet, når du bruger genbestillingsmetoden **Maks. antal**.  

### Forventet disponibel beholdning  

Den forventede disponible beholdning er en del af det planlagte lager, der er tilgængeligt til at opfylde behov på et givet tidspunkt. Den forventede disponible beholdning der bruges af planlægningssystemet ved overvågning af niveauet for sikkerhedslageret. Sikkerhedslageret skal altid være tilgængeligt for uventet efterspørgsel.  

### Intervaller  

Det er afgørende at have streng kontrol med den forventede lagerbeholdning for at registrere, når genbestillingspunktet nås eller passeres, og for at beregne det korrekte ordreantal, når du bruger genbestillingsmetoden **Maks. antal**.  

Som tidligere nævnt beregnes den forventede lagerbeholdning i starten af planlægningsperioden. Det er et bruttoniveau, der ikke medtager reservationer og lignende fordelinger. Systemet overvåger de aggregerede ændringer over en tidsperiode, et interval, for at overvåge dette lagerniveau under planlægningssekvensen. Denne periode kaldes et *tidsinterval*. Hvis du vil vide mere om tidsintervaller, skal du gå til [Intervallets rolle](#the-role-of-the-time-bucket). Planlægningssystemet sikrer, at tidsintervallet er mindst én dag. En dag er den mindste tidsenhed for behovs-eller forsyningshændelser.  

### Bestemmelse af det forventede lagerniveau  

Følgende sekvens beskriver, hvordan det planlagte system bestemmer det planlagte lagerniveau:  

* Når en forsyningshændelse, f.eks. en indkøbsordre, er blevet fuldstændig planlagt, øges den projekterede lagerbeholdning på forfaldsdatoen.  
* Når en behovshændelse har opfyldt behovet, formindskes den projekterede lagerbeholdning ikke straks. Der bogføres i stedet en påmindelse om reducering, som er en intern post, der indeholder dato og mængdebidrag til den planlagte lagerbeholdning.  
* Når der planlægges og føjes en senere forsynings hændelse til tidslinjen, undersøger systemet de bogførte reduktions rykkere én efter én til den planlagte dato for levering. Under denne proces kan niveauet for genbestillingspunktet for den interne forøgelse blive nået eller passeret.  
* Hvis der er indført en ny forsyningsordre, kontrollerer systemet, om den er indtastet før den aktuelle forsyning. Hvis det er, bliver den nye forsyning den aktuelle forsyning, og den udlignende procedure genstarter.  

Følgende billede viser dette princip.  

![Bestemmelse af det forventede lagerniveau.](media/nav_app_supply_planning_2_projected_inventory.png "Bestemmelse af det forventede lagerniveau")  

1. Forsyning **Sa** af 4 (faste) lukker behov **Da** af -3.  
2. CloseDemand: Opret en påmindelse om reducering af -3 (ikke vist).  
3. Udbud **Sa** er lukket med et overskud på 1 (der findes ingen yderligere behov).  

     Dette øger det forventede lagerniveau til +4, mens den forventede **disponible** beholdning bliver -1.  

4. Den næste forsyning **Sb** af 2 (en anden ordre) er allerede placeret på tidslinjen.  
5. Systemet kontrollerer, om der er påmindelse om reducering før **Sb** (det er der ikke, så ingen handling).  
6. Systemet lukker forsyning **Sb** (der findes ingen yderligere behov) – enten A: ved at reducere den til 0 (annullere) eller B: ved at lade den være.  

     Dette øger den projekterede lagerbeholdning (A: +0 => +4 eller B: +2 = +6).  

7. Planlægningssystemet foretager en endelig check. Er der nogen reduceringsrykker? Ja, der er en på datoen for **Da**.  
8. Systemet føjer reduktionsrykkeren af -3-rykker til det planlagte lagerniveau enten A: +4 -3 = 1 eller B: +6 -3 = +3.  
9. I tilfælde af A opretter systemet en fremad planlagt ordre fra datoen **Da**. Genbestillingspunktet er ikke nået i B, og der oprettes ingen ny ordre.

## Intervallets rolle

Formålet med intervallet er at indsamle behovshændelser inden for en tidsperiode for at oprette en fælles forsyningsordre.  

For genbestillingspolitikker, der bruger et genbestillingspunkt, kan du angive et interval. Tidsintervallet hjælper med at sikre, at behov inden for samme tidsperiode akkumuleres. Derefter kontrolleres effekten på den planlagte lagerbeholdning, og om genbestillingspunktet er bestået.

Hvis genbestillingspunktet er overskredet, er en ny forsyningsordre planlagt fremad fra udgangen af den periode, der er defineret i intervallet. Intervaller starter på den planlagte startdato.  

Begrebet interval afspejler den manuelle proces til hyppig kontrol af lagerniveauet i stedet for hver transaktion. Du skal definere frekvensen (intervallet). Brugeren samler f.eks. alle varebehov fra en kreditor for at foretage en ugentlig bestilling.  

![Eksempel på et interval i planlægningen.](media/nav_app_supply_planning_2_reorder_cycle.png "Eksempel på et interval i planlægningen")  

Intervaller bruges normalt til at undgå en overlapningseffekt. For eksempel en afstemt række af behov og forsyning, hvor et tidligt behov annulleres, eller et ny oprettes. Resultatet ville være, at hver forsyningsordre (undtagen den sidste) skal omplanlægges.

## Beregning af overløbsniveau

Når du bruger metoderne **Maks. antal** og **Fast genbestil.antal**, fokuserer planlægningssystemet kun på den planlagte lagerbeholdning i det angivne tidsinterval. Det kan foreslå ekstra forsyning, når negativ efterspørgsel eller positiv forsyning ændres uden for det pågældende interval. I forbindelse med ekstra levering beregnes det antal, du skal reducere leveringen med. Dette antal kaldes "overløbsniveauet". Overløbet kommunikeres som en planlægningslinje med en handling i form af **Ret antal (reducering)** eller **Annuller** og følgende advarselsmeddelelse:  

* Bemærk: Den forventede lagerbeholdning [xx] er højere end overløbsniveauet [xx] på forfaldsdatoen [xx].*  

![Overløbsniveau for lagerbeholdning.](media/supplyplanning_2_overflow1_new.png "Overløbsniveau for lagerbeholdning")  

### Beregning af overløbsniveau  

Overløbsniveauet beregnes på forskellige måder afhængig af genbestillingspolitikken.  

#### Maks. antal

Overløbsniveau = Maks. lagerbeholdning  

> [!NOTE]  
> Hvis du bruger et min. ordreantal, tilføjes det på følgende måde:
>
> Overløbsniveau = maks. lagerbeholdning + ordrestørrelse.  

#### Fast genbestil.antal  

overløbsniveau = ordrekvantum + genbestillingspunkt  

> [!NOTE]  
> Hvis min. ordrestørrelse er højere end genbestillingspunkt, erstattes det af følgende:
>
> overløbsniveau = ordrekvantum + genbestillingspunkt  

#### Oprundingsfaktor  

Hvis en ordre findes flere gange, vil den justere overløbsniveauet for både maks. og fast genbestillingsantal som genbestillingsmetoder.  

### Oprettelse af planlægningslinjen med overløbsadvarsel  

Der oprettes en planlægningslinje, når forsyningen medfører, at den projekterede lagerbeholdning bliver større end overløbsniveauet ved slutningen af et interval. For at advare om potentiel overflødig levering indeholder planlægningslinjen en advarselsmeddelelse, feltet **Accepter aktionsmeddelelse** er ikke markeret, og aktionsmeddelelsen er enten **Annuller** eller **Ret antal**  

#### Beregning af antallet af planlægningslinjer  

Det antal, der kan reserveres, beregnes sådan:

planlægning af linjeantallet = aktuel forsyningsmængde – (projekteret lagerbeholdning – overløbsniveau)  

> [!NOTE]  
> Som med alle advarselslinjer vil alle maksimale/minimale ordremængder eller oprundingsfaktorer blive ignoreret.  

#### Definition af aktionsmeddelelsestypen  

* Hvis antallet på planlægningslinjen er højere end 0, er aktionsmeddelelsen **Ret antal**  
* Hvis antallet på planlægningslinjen er lig med eller mindre end 0, er aktionsmeddelelsen **Annuller**  

#### Oprettelse af advarselsmeddelelsen  

I forbindelse med overløb vises der på siden **Ikke-sporede planlægningselementer** en advarsel med følgende oplysninger:  

* Det planlagte lagerniveau, der udløste advarslen  
* Det beregnede overløbsniveau  
* Forfaldsdatoen for forsyningshændelsen  

Eksempel: "Den planlagte beholdning 120 er større end overløbsniveauet 60 på 01-28-23"  

### Scenarieeksempel  

I dette scenario ændrer en kunde en salgsordre fra 70 til 40 stykker mellem to kørsler af planlægning. Overløbsfunktionen reducerer det køb, der blev foreslået for det oprindelige salgsantal.  

#### Vareopsætning  

|Genbestillingsmetode|Maks. antal|  
|-----------------------|------------------|  
|Maks. ordrestørrelse|100|  
|Genbestillingspunkt|50|  
|Lagerbeholdning|80|  

#### Situationen før salgsreducering  

|Begivenhed|Ret antal|Planlagt beholdning|  
|-----------|-----------------|-------------------------|  
|Dag et|Ingen|80|  
|Salg|-70|10|  
|Slutning på interval|Ingen|10|  
|Foreslå ny købsordre|+90|100|  

#### Situationen efter salgsreducering  

|Ændring|Ret antal|Planlagt beholdning|  
|------------|-----------------|-------------------------|  
|Dag et|Ingen|80|  
|Salg|-40|40|  
|Køb|+90|130|  
|Slutning på interval|Ingen|130|  
|Foreslå at reducere køb<br><br> ordre fra 90 til 60|-30|100|  

#### Resulterende planlægningslinjer  

Der oprettes en planlægningslinje (advarsel) for at reducere køb med 30 fra 90 til 60 for at bevare den projekterede lagerbeholdning på 100 i henhold til overløbsniveauet.  

![Planlæg i overensstemmelse med overløbsniveau.](media/nav_app_supply_planning_2_overflow2.png "Planlæg i overensstemmelse med overløbsniveau")  

> [!NOTE]  
> Uden overløbsfunktionen vises der ingen advarsel, hvis den projekterede lagerbeholdning ligger over maks., hvilket kunne forårsage ekstra forsyning af 30.

## Håndtering af forventet negativt lager

Genbestillingspunktet udtrykker det forventede behov under leveringstiden for varen. Den forventede lagerbeholdning skal være stor nok til at dække behovet, indtil den nye ordre er modtaget. I mellemtiden bør sikkerhedslageret tage højde for udsving i behov op til et målrettet serviceniveau.  

Planlægningssystemet betragter den som en nødsituation, hvis et fremtidigt behov ikke kan håndteres fra den planlagte lagerbeholdning. Eller udtrykkes på anden måde, og det planlagte lager er negativt. Systemet foreslår, at du opretter en ny forsyningsordre for at dække unmet del af behovet. Den nye forsynings ordres størrelse tager ikke hensyn til det maksimale lager eller genbestillingsantal eller følgende ordrefaktorer:

* Maks. ordrestørrelse
* Min. ordrestørrelse
* Oprundingsfaktor 

I stedet afspejler den nøjagtig mangel.  

Planlægningslinjen for denne forsyningsordre viser et **Nødsituation**-advarselsikon, og yderligere oplysninger kan findes ved opslag.  

I følgende illustration repræsenterer forsynings-id en akutordre for at justere for negativt lager.  

![Forslag til nødplanlægning for at undgå negativt lager.](media/nav_app_supply_planning_2_negative_inventory.png "Forslag til nødplanlægning for at undgå negativt lager")  

1. Forsyning **A**, oprindeligt planlagte lagerbeholdning, er under genbestillingspunkt.  
2. En ny ordre, der er planlagt fremad, oprettes (**C**).  

     (antal = maks. lagerbeholdning – forventet lagerbeholdning)  
3. Forsyning **A** er lukket af behov **B**, som ikke fuldt ud dækkes.  

     (Behov **B** kunne forsøge at planlægge forsyning C, men det vil ikke ske i overensstemmelse med intervalkonceptet).  
4. Ny forsyning (**D**) er oprettet for at dække det resterende antal efter behov **B**.  
5. Behov **B** er lukket (oprettelse af en påmindelse til den forventede lagerbeholdning).  
6. Den nye forsyning **D** er lukket.  
7. Planlagt beholdning kontrolleret. Genbestillingspunktet er ikke blevet overskredet.  
8. Forsyning **C** er lukket (der findes ingen yderligere behov).  
9. Sidste kontrol. Der findes ingen udestående påmindelser om lagerniveau.  

I følgende afsnit beskrives karakteristika for de fire understøttede genbestillingsmetoder.

## Genbestillingsmetoder

Genbestillingsmetoder definerer, hvor meget der skal bestilles, når varen skal genbestilles. Der findes fire forskellige genbestillingsmetoder.  

### Fastlagt ordrekvantum

Fastlagt ordrekvantum bruges typisk til lager planlægning for varer med følgende egenskaber:

* Lav lageromkostning
* Lav risiko for forældelse
* Lavt antal af elementer

Denne metode bruges normalt i forbindelse med et genbestillingspunkt, hvilket afspejler det forventede behov under leveringstiden.  

#### Beregnet pr. interval  

Hvis du når til eller krydse ved genbestillingspunktet i et tidsinterval (genbestillingscyklus), foreslås der to handlinger:

* Opret en ny forsyningsordre for ordrekvantum
* Planlægge en fremadrettet rækkefølge fra første dato efter slutningen af et interval  

Det tidsbegrænsede genbestillingspunkt reducerer antallet af forsyningsforslag. Den afspejler en proces, hvor der manuelt kontrolleres for det aktuelle antal placeringer på lagerstedet.  

#### Opretter kun nødvendige forsyninger  

Før der foreslås en ny forsyningsordre for at opfylde et genbestillingspunkt, kontrollerer planlægningssystemet, om der er følgende levering:

* Om levering allerede er bestilt
* Om du forventer at modtage levering inden for varens gennemløbstid

Systemet foreslår ikke en ny forsyningsordre, hvis forsyningen bringer den projekterede lagerbeholdning til genbestillingspunktet inden for leveringstiden.  

Forsyningsordrer, der er oprettet specielt med henblik på at opfylde genbestillingspunktet, er udelukket fra almindelig forsyningsafstemning og vil ikke på nogen måde blive ændret bagefter. Hvis du vil uddele en vare, der har genbestillingspunkt, skal du gennemgå de udestående forsyningsordrer manuelt eller ændre genbestillingsmetoden til **Lot-for-lot**. Systemet reducerer eller annullerer ekstra levering.  

#### Kombineres med ordremodifikatorer  

Ordremodifikatorerne Min. ordrestørrelse, Maks. ordrestørrelse og Oprundingsfaktor bør ikke spille en stor rolle, når metoden for fast genbestillingsantal bruges. Planlægningssystemet tager imidlertid dem i betragtning:

* Reducer antallet til det angivne maksimale ordreantal (og Opret to eller flere leverancer for at nå det samlede ordreantal)
* Forøg ordren til det angivne minimum ordreantal
* Rund ordreantallet op for at overholde en angivet flere ordre flere  

#### Kombinerer med kalendere  

Før du foreslår en ny forsyningsordre for at opfylde et genbestillingspunkt, kontrollerer planlægningssystemet, om ordren er planlagt til en fridag. Den bruger de kalendere, du angiver i feltet **Basiskalenderkode** på siderne **Firmaoplysninger** og **lokationskort**.  

Hvis den planlagte dato er en ikkearbejdsdag, flytter planlægningssystemet ordren frem til den nærmeste arbejdsdag. Flyttes datoen kan det resultere i en ordre, der opfylder et genbestillingspunkt, men ikke opfylder visse specifikke behov. Planlægningssystemet opretter en ekstra levering for sådanne behov.  

#### Bør ikke bruges med forecast  

Det er ikke nødvendigt at medtage en prognose i planlægningen af en vare ved hjælp af et genbestillingspunktet, fordi det forventede behov allerede er angivet i genbestillingspunktet. Hvis det er relevant at basere planen på et forecast, kan du bruge politikken **Lot-for-Lot**.  

#### Må ikke anvendes med reservationer  

Hvis du har reserveret en mængde, for eksempel et antal på lageret, til nogle fremtidige behov, bliver grundlaget for planlægningen forstyrret. Selvom det planlagte beholdningsniveau er acceptabelt i relation til genbestillingspunktet, er mængderne muligvis ikke tilgængelige. Systemet kan forsøge at kompensere ved at oprette undtagelses ordrer. Det anbefales dog, at feltet **Reserver** er angivet til **Aldrig** for varer, der er planlagt vha. genbestillingspunkt.

### Maksimumantal

Det maksimale antal er en måde at vedligeholde lageret ved hjælp af et genbestillingspunkt.  

Alt om den faste genbestillingsantalmetode gælder også for denne metode. Den eneste forskel er omfanget af den foreslåede forsyning. Når metoden med maksimalt antal bruges, defineres genbestillingsantallet dynamisk baseret på det planlagte lagerniveau. Derfor adskiller den sig som regel fra ordre til ordre.  

#### Beregn pr. interval

Når du når til eller kryds genbestillingspunktet, bestemmer systemet genbestillings antallet i slutningen af et tidsinterval. Systemet måler afstanden fra den nuværende forventede lagerbeholdning og den angivne maksimale lagerbeholdning for at bestemme den ordremængden. Systemet kontrollerer derefter:

* Om levering allerede er bestilt
* Om du forventer at modtage levering inden for varens gennemløbstid

Hvis det er tilfældet, reduceres antallet i den nye forsyningsordre med de antal, der allerede er bestilt.  

Hvis du ikke angiver et maksimalt lagerantal, sørger planlægningssystemet for, at den planlagte beholdning når ordreantallet.

#### Kombineres med ordremodifikatorer

Afhængigt af opsætningen kan det være bedst at kombinere politikken for maks. antal ved ordre ændring: 

* Sikre et mindste ordreantal
* Afrund antallet til et heltal af måleenheder for køb
* Antallet inddeles, hvis det overskrider det maksimale ordreantal  

### Kombinerer med kalendere

Før du foreslår en ny forsyningsordre for at opfylde et genbestillingspunkt, kontrollerer planlægningssystemet, om ordren er planlagt til en fridag. Den bruger de kalendere, du angiver i feltet **Basiskalenderkode** på siderne **Firmaoplysninger** og **lokationskort**.  

Hvis den planlagte dato er en ikkearbejdsdag, flytter planlægningssystemet ordren frem til den nærmeste arbejdsdag. Flyttes datoen kan det resultere i en ordre, der opfylder et genbestillingspunkt, men ikke opfylder visse specifikke behov. Planlægningssystemet opretter en ekstra levering for sådanne behov.

### Sorteringsrækkefølge

I et fremstil-til-ordre-miljø bliver en vare købt eller produceret til at dække et bestemt behov. Fastlagt ordrekvantum bruges typisk til lager planlægning for varer med følgende egenskaber

* Behovet er ikke hyppigere
* Leveringstiden er ikke betydelig
* Krævede attributter varierer  

[!INCLUDE [prod_short](includes/prod_short.md)] opretter et ordre-til-ordre-link, der fungerer som en indledende forbindelse mellem forsyningen, en forsyningsordre eller lager og det behov, som den eller det skal opfylde. Du kan anvende ordre-til-ordre-linket under planlægningen på følgende måder:  

* Når du bruger Fremstil-til-ordre til at oprette produktionsordrer med flere niveauer eller produktionsordrer af projekttype (fremstilling af nødvendige komponenter på den samme produktionsordre)  
* Når du bruger salgsordreplanlægning til at oprette en produktionsordre fra en salgsordre  

> [!TIP]
> Hvis vareattributter ikke varierer, kan det være bedst at bruge en Lot-for-Lot-genbestillingsmetode. Som resultat bruger systemet ikke-planlagt lagerbeholdning og akkumulerer kun salgsordrer med samme afsendelsesdato eller inden for et defineret interval.  

#### Ordre-til-ordre-links og overskredne datoer

I modsætning til de fleste forsyning-behov-sæt, planlægges tilknyttede ordrer med forfaldsdatoer, før planlægningsstartdatoen er fuldt planlagt af systemet. Årsagen til denne undtagelse er, at bestemte behov-forsyningssæt skal synkroniseres. Du kan finde flere oplysninger om den fastlåste zone, der gælder for de fleste behovsforsyningstyper i [Håndtering af ordrer før planlægningsstartdatoen](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).

### Lot-for-Lot

Lot-for-Lot-politikken er den mest fleksible, da systemet kun reagerer på faktisk behov. Det handler om forventede behov fra prognose- og tomme ordrer og udligner derefter ordreantallet på basis af behovet. Lot-for-lot-politik er beregnet til elementer, hvor lageret kan accepteres, men bør undgås.  

På nogle måder svarer politikken Lot-for-lot til ordrepolitikken. Den kan acceptere antal på lager, og den har bundtet behov og levering i de intervaller, du definerer.

Du kan angive tidsintervallet i feltet **Tidsinterval** på siden **Varekort**. Den minimale størrelse på et interval er én dag, da det er den mindste tidsenhed, der gælder for behovs-og leverings hændelser i [!INCLUDE [prod_short](includes/prod_short.md)].  

Intervallet angiver også grænser for, hvornår en eksisterende forsyningsordre bør omplanlægges for at opfylde et bestemt behov. Forsyningen i intervallet flyttes ind eller ud for at opfylde behovet. Tidligere levering vil medføre ekstra lagerbeholdning, og du skal annullere den. Opret en ny forsyningsordre til levering senere.  

Med denne politik kan du angive et sikkerhedslager for at kompensere for ændringer i forsyningen eller til at opfylde et pludseligt behov. Lot-for-Lot-politikken kan også omfatte en bufferperiode og en buffermængde for at reducere ordreplanlægning.  

Sammen med feltet **Ændringsperiode** bidrager feltet **Akkumuleringsperiode for lot** til at definere virksomhedens genbestillingscyklus. Fra datoen for det første behov akkumuleres alle behov i den næste akkumuleringsperiode for lot i én forsyningsordre, der er placeret på datoen for det første behov. Behov, som er uden for akkumuleringsperiode for lot er ikke omfattet af forsyningsordren.

Da forsyningsordre antallet er baseret på det faktiske behov, kan det være en god idé at bruge ordre faktorerne:

* Afrunde ordreantallet, så det svarer til en ordre af flere (eller købsenhed)
* Forøg ordren til det angivne minimum ordreantal
* Reducer antallet til det angivne maksimale ordreantal (og opret to eller flere leverancer for at nå det samlede ordreantal)

## Se også  

[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)  
[Designoplysninger: Tabellen Planlægningsopgave](design-details-planning-assignment-table.md)  
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designoplysninger: Afstemning af behov og efterspørgsel](design-details-balancing-demand-and-supply.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]