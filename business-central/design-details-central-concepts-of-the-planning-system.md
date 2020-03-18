---
title: Designoplysninger – Centrale begreber i planlægningssystemet | Microsoft Docs
description: Planlægningsfunktionerne er indeholdt i en kørsel, der først vælger de relevante varer og den periode, der skal planlægges for, og derefter foreslår mulige handlinger, brugeren kan udføre, på basis af udbud og efterspørgselssituation og varens planlægningsparametre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b809743aa25aee409b9a71ca98da77ea64b58fb1
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076510"
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Designoplysninger: Centrale begreber i planlægningssystemet
Planlægningsfunktionerne er indeholdt i en kørsel, der først vælger de relevante varer og den relevante periode, der skal planlægges. Ifølge hver vares laveste-niveau-kode (styklisteposition) kalder kørslen en kodeenhed, der beregner en forsyningsplan ved at afstemme forsyning-behov-sæt og foreslå mulige handlinger, som brugeren kan foretage. De foreslåede handlinger vises som linjer i planlægningskladden eller indkøbskladden.  

![Indhold på siden Planlægningskladde](media/NAV_APP_supply_planning_1_planning_worksheet.png "Indhold på siden Planlægningskladde")  

Planlæggeren i en virksomhed, f.eks. en indkøber eller produktionsplanlægger, formodes at være brugeren af planlægningssystemet. Planlægningssystemet hjælper brugeren ved at udføre omfattende, men temmeligt enkle beregninger af en plan. Brugeren kan derefter koncentrere sig om at løse mere komplekse problemer, f.eks. når ting er anderledes. end de plejer.  

Planlægningssystemet styres af forventet og faktiskt kundebehov, f.eks. prognoser og salgsordrer. Når planlægningsberegningen køres, foreslås brugeren, at der tages bestemte forholdsregler, f.eks. forsyning fra leverandører, montage- eller produktionsafdelinger eller overflytninger fra andre lagersteder. Disse foreslåede handlinger kunne være at oprette nye forsyningsordrer, som f.eks. købs- eller produktionsordrer. Hvis der allerede findes forsyningsordrer, kan den foreslåede aktivitet f.eks. være at øge eller fremskynde ordrerne for på den måde at imødekomme det ændrede behov.  

Et andet formål med planlægningssystemet er at sikre, at lagerbeholdningen ikke vokser unødvendigt. Hvis behovet falder, kan planlægningssystemet foreslå, at brugeren udskyder eksisterende forsyningsordrer, angiver mindre antal til dem eller helt annullerer dem.  

MRP og hovedplan: Beregn nettoplan og Beregn totalplan er alle funktioner i én kodeenhed, der indeholder logikken i planlægningssystemet. Beregningen af forsyningsplan omfatter dog forskellige undersystemer.  

Bemærk, at planlægningssystemet har ingen dedikeret logik for kapacitetsudjævning eller finplanlægning. Den slags planlægningsarbejde udføres derfor som en separat disciplin. Manglende direkte integration mellem de to områder betyder også, at væsentlige ændringer af kapacitet eller tidsplan kræver, at planlægning gentages.  

## <a name="planning-parameters"></a>Planlægningsparametre  
Planlægningsparametre, som brugeren angiver for en vare eller en gruppe af varer, styrer hvilke handlinger planlægningssystemet foreslår i forskellige situationer. Planlægningsparametrene defineres på hvert enkelt varekort, for at styre hvornår, hvor meget og hvordan du genbestiller.  

Planlægningsparametre kan også være defineret for en kombination af vare, variant og lokation ved at oprette en lagervare for hver kombination, der er nødvendig, og derefter angive individuelle parametre.  

Du kan finde flere oplysninger i [Designoplysninger - Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) og [Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Planlægningsstartdato  
For at undgå en forsyningsplan, der indeholder åbne ordrer i fortiden, og som foreslår eventuelt umulige handlinger, behandler planlægningssystemet alle datoer før planlægningsstartdatoen som en frossen zone, hvor der gælder følgende særlige regel:  

Alle forsyninger og behov før startdatoen for planlægningsperioden vil blive betragtet som en del af lagerbeholdningen eller leveret.  

Med andre ord antages det, at planen for fortiden er udført i overensstemmelse med den givne plan.  

Du kan finde flere oplysninger i [Håndtering af ordrer før planlægningsstartdatoen](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).  

## <a name="dynamic-order-tracking-pegging"></a>Dynamisk ordresporing (udligning)  
Dynamisk ordresporing med samtidig oprettelse af aktionsmeddelelser i planlægningskladden er ikke en del af forsyningsplanlægningssystemet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Denne funktion sammenkæder, behovet og det antal, der kan dække det, i realtid, hver gang et nyt behov eller en ny forsyning oprettes eller ændres.  

Hvis brugeren f.eks. indtaster eller ændrer en salgsordre, vil det dynamiske ordresporingssystem søge efter en relevant forsyning, der kan dække behovet. Dette kan være fra lagerbeholdning eller fra en forventet forsyningsordre (f.eks. en købsordre eller en produktionsordre). Når der findes en forsyningskilde opretter systemet opretter en kæde mellem behov og forsyning og viser den på skrivebeskyttede sider, der åbnes fra de involverede dokumentlinjer. Når der ikke bliver fundet tilstrækkelige forsyninger, opretter det dynamiske ordresporingssystem aktionsmeddelelser i planlægningskladden med forslag til forsyningsplanlægning, der afspejler den dynamiske balance. Derfor tilbyder det dynamiske ordresporingssystem et meget grundlæggende planlægningssystem, der kan være til hjælp både for planlæggeren og andre roller i den interne forsyningskæde.  

Dynamisk ordresporing kan derfor betragtes som et værktøj, der hjælper brugeren med at vurdere, om forsyningsordreforslag skal accepteres. Fra forsyningssiden kan en bruger se, hvilke behov der har oprettet forsyningen, og fra behovssiden, hvilken forsyning der skal dække behovet.  

![Eksempel på dynamisk ordresporing](media/NAV_APP_supply_planning_1_dynamic_order_tracking.png "Eksempel på dynamisk ordresporing")  

Du kan finde flere oplysninger i [Designoplysninger: Reservation, ordresporing og aktionsmeddelelser](design-details-reservation-order-tracking-and-action-messaging.md).  

I virksomheder med en lav varestrøm og mindre avancerede produktstrukturer kan det være tilstrækkeligt at bruge dynamisk ordresporing som det vigtigste middel til forsyningsplanlægning. I travle miljøer bør planlægningssystemet dog bruges til altid at sikre en korrekt afstemt forsyningsplan.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Dynamisk ordresporing kontra planlægningssystemet  
Ved første øjekast kan det være svært at skelne mellem planlægningssystemet og dynamisk ordresporing. Begge funktioner viser afgang i planlægningskladden ved at foreslå handlinger, som planlæggeren skal udføre. Dog afviger den måde, dette output er produceret.  

Planlægningssystemet håndterer hele forsynings-behov-mønstret for en vare gennem alle niveauer i styklistehierarkiet langs tidslinjen, hvorimod dynamisk ordresporing kun tager sig af situationen i den ordre, der aktiverede den. Ved balancering af behov og forsyning, opretter planlægningssystemet kæder i en brugeraktiveret batchtilstand, mens dynamisk ordresporing opretter links automatisk og løbende, når brugeren indtaster et behov eller en forsyning i programmet, f.eks. en salgsordre eller indkøbsordre.  

Dynamisk ordresporing etablerer forbindelser mellem behov og forsyning, når der indtastes data, på grundlag af først til mølle-princippet. Dette kan føre til nogen uorden i prioriteter. En salgsordre, der først er angivet med en forfaldsdato næste måned, kan f.eks. være knyttet til forsyningen på lageret, mens de næste salgsordrer, der forfalder i morgen, kan forårsage, at en aktionsmeddelelse opretter en ny købsordre for at dække det, som vist nedenfor.  

![Eksempel på ordresporing i forsyningsplanlægning 1](media/NAV_APP_supply_planning_1_dynamic_order_tracking_graph.png "Eksempel på ordresporing i forsyningsplanlægning 1")  

Derimod vedrører planlægningssystemet alle behov og forsyninger for en bestemt vare i prioriteret rækkefølge i forhold til forfaldsdatoer og ordretyper, det vil sige ud fra først til mølle. Den sletter alle ordresporingslinks, der er oprettet dynamisk, og genopretter dem i overensstemmelse med prioritet af forfaldsdato. Når planlægningssystemet er kørt, har det løst alle ubalancer mellem behov og forsyning, som vist nedenfor, for de samme data.  

![Eksempel på ordresporing i forsyningsplanlægning 2](media/NAV_APP_supply_planning_1_planning_graph.png "Eksempel på ordresporing i forsyningsplanlægning 2")  

Efter planlægningskørslen forbliver ingen aktionsmeddelelser i tabellen Aktionsmeddelelsespost, fordi de er blevet erstattet af de foreslåede handlinger i planlægningskladden  

Du kan finde flere oplysninger under Ordresporingsbindinger under planlægning i [Afstemning af forsyning med behov](design-details-balancing-demand-and-supply.md#balancing-supply-with-demand).  

## <a name="sequence-and-priority-in-planning"></a>Rækkefølge og prioritet i planlægningen  
Når du opretter en plan, er rækkefølgen af beregningerne vigtig for at få arbejdet gjort inden for en rimelig tidsramme. Desuden spiller prioriteringen af krav og ressourcer en vigtig rolle for at opnå de bedste resultater.  

Planlægningssystemet i [!INCLUDE[d365fin](includes/d365fin_md.md)] er behovstyret. Varer med højt niveau bør planlægges før varer med lavt niveau, fordi planen for varer med højt niveau kan generere yderligere behov for varerne på lavere niveau. Det betyder for eksempel, at detaillokationer bør planlægges før distributionscentre planlægges, fordi planen for en retaillokation kan omfatte yderligere behov fra distributionscentret. På en nærmere afvejning betyder dette også, at en salgsordre ikke skal udløse en ny forsyningsordre, hvis en allerede frigiven forsyningsordre kan dække salgsordren. Desuden må en forsyning med et bestemt lotnummer ikke allokeres for at dække et generisk behov, hvis et andet behov kræver denne specifikke lot.  

### <a name="item-priority--low-level-code"></a>Vareprioritet/laveste-niveau-kode  
I et produktionsmiljø medfører behovet for en færdig salgbar vare afledte behov for komponenter, der udgør den færdige vare. Styklistestrukturen styrer komponentstrukturen og kan omfatte flere niveauer af halvfabrikata. Planlægning af en vare på ét niveau vil medføre afledte behov for komponenter på næste niveau osv. I sidste ende vil dette resultere i afledte behov for købte varer. Derfor planlægger planlægningssystemet efter varer i rækkefølge efter deres placering i det samlede styklistehierarki, med start ved færdige, salgbare varer på det højeste niveau, og fortsætter ned i produktstrukturen til varerne på lavere niveau (i henhold til laveste-niveau-koden).  

![Planlægning af styklister](media/NAV_APP_supply_planning_1_BOM_planning.png "Planlægning af styklister")  

Tallene viser, i hvilken rækkefølge systemet giver forslag til forsyningsordrer på øverste niveau og under antagelse af, at brugeren accepterer disse forslag, og for alle varer på lavere niveauer.  

Du kan finde flere oplysninger om overvejelser i forbindelse med produktion i [Indlæsning af lagerprofiler](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

### <a name="locations--transfer-level-priority"></a>Lokationer / prioritet af overførselsniveau  
Virksomheder, der gør forretning på mere end én lokation, kan være nødt til at planlægge individuelt for hver lokation. En vares sikkerhedslagerniveau og dens genbestillingsmetode kan f.eks. variere fra én lokation til en anden. I så fald skal planlægningsparametrene angives pr. vare og pr. lokation.  

Dette understøttes ved hjælp af lagervarer, hvor individuelle planlægningsparametre kan angives på lagervareniveau. En lagervare kan betragtes som en vare på en bestemt placering. Hvis brugeren ikke har angivet en lagervare for den pågældende lokation, bruges de standardparametre, der er angivet på varekortet. Programmet beregner kun en plan for aktive lokationer, som er der, hvor der er eksisterende behov eller forsyning for den pågældende vare.  

Et element kan håndteres på enhver lokation i princippet, men programmets tilgang til begrebet lokation er meget streng. En salgsordre på ét sted kan f.eks. ikke opfyldes af et antal på lager på en anden lokation. Antal på lager skal først overflyttes til den lokation, der er angivet på salgsordren.  

![Planlægning af lagervarer pr. lokation](media/NAV_APP_supply_planning_1_SKU_planning.png "Planlægning af lagervarer pr. lokation")  

Du kan finde flere oplysninger i [Designoplysninger: Overførsler i planlægning](design-details-transfers-in-planning.md).  

### <a name="order-priority"></a>Prioritering for ordrer  
Inden for en given SKU repræsenterer den anmodede eller tilgængelige dato den højeste prioritet. Behovene i dag skal behandles før behovene for de kommende dage. Men bortset fra denne slags prioritet sorteres de forskellige behov og forsyningstyper efter forretningsmæssig vigtighed for at beslutte, hvilke behov der skal opfyldes, før andre opfyldes. På forsyningssiden fortæller ordreprioriteten, hvilken forsyningskilde der skal anvendes, før der anvendes andre forsyningskilder.  

Du kan finde flere oplysninger i [Prioritering af ordrer](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

## <a name="demand-forecasts-and-blanket-orders"></a>Behovsprognoser og rammeordrer  
Forecasts og rammesalgsordrer repræsenterer begge forventet behov. Den rammeordre, som dækker en debitors tiltænkte køb over en bestemt tidsperiode, skal mindske usikkerheden af det samlede forecast. Rammeordren er en debitorspecifik prognose i tillæg til den uspecificerede prognose, som vist nedenfor.  

![Planlægning ved hjælp af prognoser](media/NAV_APP_supply_planning_1_forecast_and_blanket.png "Planlægning ved hjælp af prognoser")  

Du kan finde flere oplysninger i afsnittet "Forecastbehov reduceres af salgsordrer" i [Indlæsning af lagerprofiler](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

## <a name="planning-assignment"></a>Planlægningsopgave  
Der skal foretages planlægning for alle varer, men der er ingen grund til at beregne en plan for en vare, medmindre der er sket en ændring i mønstret for behov eller forsyning, siden sidst en plan blev beregnet.  

Hvis brugeren har angivet en ny salgsordre eller ændret en eksisterende, er der grund til at genberegne planen. Andre årsager omfatter en ændring i budgettet eller den ønskede mængde sikkerhedslager. Ændring af en stykliste ved at tilføje eller fjerne en komponent ville sandsynligvis angive en ændring, men kun for komponentvaren.  

Planlægningssystemet overvåger sådanne hændelser og tildeler de relevante varer til planlægning.  

For flere lokationer finder tildelingen sted på niveauet for vare pr. lokationskombination. Hvis en salgsordre f.eks. er blevet oprettet på kun én lokation, bliver varen tildelt på den pågældende lokation til planlægning.  

Årsagen til at vælge varer til planlægning er et spørgsmål om systemets ydeevne. Hvis der ikke er opstået nogen ændring af en vares behov-forsyningsmønster, foreslår planlægningssystemet ikke nogen handlinger, der skal udføres. Uden planlægningsopgave ville systemet skulle udføre beregningerne for alle varer for at finde ud af, hvad der skal planlægges, og det ville forbruge systemressourcer.  

Den komplette liste over grunde til at tildele en vare i planlægning kan du finde i [Designoplysninger: Tabellen Planlægningsopgave](design-details-planning-assignment-table.md).  

Planlægningsindstillingerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] er:  

-   Beregn totalplan – beregner alle valgte varer, uanset om det er nødvendigt eller ej.  
-   Beregn nettoplan – beregner kun de valgte varer, hvor der er foretaget ændringer i behov- og forsyningsmønstre, og som derfor er blevet tildelt planlægning.  

Nogle brugere mener, at nettoplanlægning skal udføres i farten, f.eks. når salgsordrer angives. Men det kan være forvirrende, fordi dynamisk ordresporing og aktionsmeddelelser også beregnes løbende. [!INCLUDE[d365fin](includes/d365fin_md.md)] tilbyder desuden disponibel til levering-kontrol i realtid og viser pop op-advarsler, når du angiver salgsordrer, hvis behovet ikke kan opfyldes gennem den aktuelle forsyningsplan.  

Udover disse overvejelser planlægger planlægningssystemet kun for de varer, som brugeren har udarbejdet med passende planlægningsparametre. I modsat fald antages det, at brugeren kommer til at planlægge varer halvautomatisk eller manuelt ved hjælp af funktionen Ordreplanlægning.  

Du kan finde flere oplysninger om de automatiske planlægningsprocedurer i [Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Varedimensioner  
Behov og forsyning kan have variantkoder og lokationskoder, der skal overholdes, når planlægningssystemet afstemmer behov og forsyning.  

Systemet behandler variant- og lokationskoder som varedimensioner på en salgsordrelinje, lagerpost osv. Derfor beregnes der en plan for hver kombination af variant og lokation, som om kombinationen var et separat varenummer.  

I stedet for beregning af en teoretisk kombination af variant og lokation beregnes kun de kombinationer, der faktisk findes i databasen.  

Du kan finde flere oplysninger om, hvordan planlægningssystemet håndterer lokationskoder efter behov, i [Designoplysninger: Behov på lokationen TOM](design-details-balancing-demand-and-supply.md).  

## <a name="item-attributes"></a>Vareattributter  
Bortset fra generelle varedimensioner som f.eks. varenummer, variantkode, lokationskode og ordretype, kan hver behov- og forsyningshændelse have yderligere specifikationer i form af serienumre/lotnumre. Planlægningssystemet planlægger disse attributter på bestemte måder, afhængigt af deres specifikationsniveau.  

Et ordre-til-ordre-link mellem behov og forsyning er en anden type attribut, der har indflydelse på planlægningssystemet.  

### <a name="specific-attributes"></a>Specifikke attributter  
Visse attributter i forbindelse med behov er specifikke og skal gengives nøjagtigt med en tilsvarende forsyning. Der findes følgende to specifikke attributter:  

-   Påkrævede serienumre/lotnumre, der kræver et bestemt program (afkrydsningsfeltet **Serienr.specifik sporing** eller **Lotspecifik sporing** er markeret af siden **Varesporingskodekort** for den varesporingskode, der bruges af varen).  
-   Links til forsyningsordrer, der er oprettet manuelt eller automatisk for et bestemt behov (ordre-til-ordre-links).  

Planlægningssystemet anvender følgende regler for disse attributter:  

-   Behov med specifikke attributter kan kun opfyldes ved forsyning med tilsvarende attributter.  
-   Forsyning med særlige attributter kan også opfylde behovet, der ikke anmoder specifikt om disse attributter.  

Hvis et behov for bestemte attributter ikke kan opfyldes af lagerbeholdningen eller de forventede forsyninger, foreslår planlægningssystemet derfor en ny forsyningsordre til at dække disse behov uden hensyntagen til planlægningsparametre.  

### <a name="non-specific-attributes"></a>Ikke-specifikke attributter  
Serie- eller lotnumrevarer uden specifik opsætning af varesporing kan have serienumre/lotnumre, der ikke skal anvendes til præcist samme serienummer/lotnummer, men kan anvendes på ethvert serienummer/lotnummer. Dette giver planlægningssystemet mere frihed til at afstemme f.eks. et behov med serienummer med en forsyning med serienummer, typisk på lageret.  

Behov-forsyning med serie-/lotnumre, specifikke eller ikke-specifikke, betragtes som høj prioritet og er derfor fritaget fra den frosne zone, hvilket betyder, at de er en del af planlægningen, selvom de forfalder før planlægningens startdato.  

Du kan finde flere oplysninger i afsnittet "Serienumre/lotnumre indlæses efter specifikationsniveau" i [Indlæsning af lagerprofiler](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

Hvis du ønsker yderligere oplysninger om, hvordan planlægningssystemet afstemmer attributter, kan du se [Serienumre/lotnumre og ordre-til-ordre-links er fritaget fra den frosne zone](design-details-balancing-demand-and-supply.md#seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone).  

## <a name="order-to-order-links"></a>Ordre-til-ordre-links  
Ordre-til-ordre-indkøb betyder, at en vare er købt, monteret eller produceret udelukkende til at dække et bestemt behov. Normalt relateres det til A-varer og motivationen for at vælge denne metode kan være, at behovet er sjældent, leveringstiden er ubetydelig, eller de påkrævede attributter varierer.  

Et andet særligt tilfælde, der bruger ordre-til-ordre-links er, når en montageordre linkes til en salgsordre i et montage til ordre-scenario.  

Ordre-til-ordre-links anvendes mellem efterspørgsel og udbud på fire måder:  

-   Når den planlagte vare bruger genbestillingsmetoden Ordre.  
-   Når produktionsmetoden Fremstil-til-ordre bruges til at oprette produktionsordrer med flere niveauer eller produktionsordrer af projekttype (fremstilling af nødvendige komponenter på den samme produktionsordre).  
-   Ved oprettelse af produktionsordrer for salgsordrer med funktionen Salgsordreplanlægning.  
-   Ved montering af en vare til en salgsordre. (Montagepolitik er indstillet til Montage til ordre.  

I disse tilfælde foreslår planlægningssystemet kun at bestille den ønskede mængde. Når den er oprettet, vil indkøbs-, produktions- eller montageordren matche det tilsvarende behov. Hvis en salgsordre f.eks. ændres i tid eller antal, foreslår planlægningssystemet, at den tilsvarende forsyningsordre ændres i overensstemmelse hermed.  

Når der findes ordre-til-ordre-links, medtager planlægningssystemet ikke tilknyttet forsyning eller lagerbeholdning i udligningsproceduren. Det er op til brugeren at vurdere, om sammenkædede forsyning skal bruges til at dække andre eller nye behov, og i så fald slette forsyningsordren eller reservere den sammenkædede forsyning manuelt.  

Reservationer og ordresporingskæder brydes, hvis en situation bliver umulig som f.eks at flytte behovet til en dato før forsyningen. Ordre-til-ordre-link tilpasses dog ændringer i de respektive udbud eller efterspørgsler, og dermed afbrydes forbindelsen aldrig.  

## <a name="reservations"></a>Reservationer  
Planlægningssystemet medtager ikke nogen reserverede mængder i beregningen. Hvis en salgsordre f.eks. er blevet helt eller delvist reserveret mod antallet på lager, kan det reserverede antal på lager ikke bruges til at dække andre behov. Planlægningssystemet medtager ikke dette behov-forsyningssæt i beregningen.  

Dog omfatter planlægningssystemet stadig reserverede mængder i den planlagte lagerprofil, fordi alle mængder, der skal tages i betragtning, når det bestemmes, både når genbestillingspunktet er passeret, og hvor mange der skal genbestilles for at nå og ikke overskride det maksimale lagerniveau. Unødvendige reservationer vil derfor føre til øget risiko for, at lagerniveauer bliver lave, fordi logikken i planlægningen ikke registrerer de reserverede antal.  

Følgende illustration viser, hvordan reservationer kan hæmme den mest velegnede plan.  

![Planlægning ved hjælp af reservationer](media/NAV_APP_supply_planning_1_reservations.png "Planlægning ved hjælp af reservationer")  

Du kan finde flere oplysninger i [Designoplysninger: Reservation, ordresporing og aktionsmeddelelser](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Advarsler  
Den første kolonne i planlægningsarket for advarselsfelterne. I en planlægningslinje, der er oprettet til en usædvanlig situation, vises der et advarselsikon i dette felt, som brugeren kan klikke på for at få yderligere oplysninger.  

Forsyning på planlægningslinjer med advarsler vil normalt ikke blive ændret i henhold til planlægningsparametre. Planlægningssystemet foreslår i stedet for kun en forsyning til at dække det nøjagtige behovsantal. Systemet kan dog konfigureres til at overholde bestemte planlægningsparametre for planlægningslinjer med visse advarsler. Du kan finde flere oplysninger i beskrivelsen af disse indstillinger for henholdsvis kørslen **Beregn plan - planlægningskld.** og kørslen **Beregn plan - indkøbskladde** .  

Advarselsoplysningerne vises af siden **Ikke-sporede planlægningselementer**, som også bruges til at vise ordresporingsbindinger for ikke-ordrerelaterede netværksenheder. Der findes følgende advarselstyper:  

-   Nødsituation  
-   Undtagelse  
-   Bemærk  

![Advarsler i planlægningskladden](media/NAV_APP_supply_planning_1_warnings.png "Advarsler i planlægningskladden")  

### <a name="emergency"></a>Nødsituation  
Denne advarsel vises i to tilfælde:  

-   Når lageret er negativt på den planlagte startdato.  
-   Når der er antedaterede forsyning- eller behovshændelser.  

Hvis varens lager er negativt på den planlagte startdato, foreslås der en nødforsyning for den negative mængde, som skal ankomme på den planlagte startdato. Advarslen angiver startdatoen og mængden for nødordren. Du kan finde flere oplysninger i [Håndtering af forventet negativt lager](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Evt. dokumentlinjer med forfaldsdatoer før den planlagte startdato konsolideres i én nødforsyningsordre, så varen kan ankomme på den planlagte startdato.  

### <a name="exception"></a>Undtagelse  
Advarslen om undtagelsen vises, hvis det forventede disponible lager kommer under sikkerhedslageret. Planlægningssystemet foreslår en forsyningsordre, der skal opfylde behovet på forfaldsdatoen. Advarslen angiver varens sikkerhedslager og den dato, hvor det overtrædes.  

Overskridelse af niveauet for sikkerhedslageret anses for at være en undtagelse, fordi det ikke bør forekomme, hvis genbestillingspunktet er angivet korrekt. Du kan finde flere oplysninger i [Genbestillingspunktets rolle](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Generelt sikrer exceptionelle ordreforslag, at den planlagte disponible beholdning aldrig er lavere end niveauet for sikkerhedslageret. Dette betyder, at det foreslåede antal lige akkurat er nok til at dække sikkerhedslageret uden at tage hensyn til planlægningsparametrene. Men i nogle eksempler tages der hensyn til ordremodifikatorer.  

> [!NOTE]  
>  Planlægningssystemet har måske tilsigtet forbrugt sikkerhedslageret og vil derefter genopfylde det med det samme. Du kan finde flere oplysninger under [Sikkerhedslager kan forbruges](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

### <a name="attention"></a>Bemærk!  
Denne advarsel vises i tre tilfælde:  

-   Når den planlagte startdato ligger før arbejdsdatoen.  
-   Når planlægningslinjen foreslår ændring af en en frigivet købs- eller produktionsordre.  
-   Den planlagte beholdning overskrider overløbsniveauet på forfaldsdatoen. Du kan finde flere oplysninger i [Forblive under overløbsniveauet](design-details-handling-reordering-policies.md#staying-under-the-overflow-level).  

> [!NOTE]  
>  På planlægningslinjer med advarsler er feltet **Accepter aktionsmeddelelse** ikke markeret, fordi planlæggeren forventes at undersøge disse linjer nærmere, før planen udføres.  

## <a name="error-logs"></a>Fejllogfiler  
Brugeren kan vælge feltet **Stop, og vis første fejl** på beregningsplanens anmodningsside for at stoppe planlægningskørslen, når der opstår fejl. Samtidig vises der en meddelelse med oplysninger om fejlen. Hvis der er fejl, vises kun de fejlfri planlægningslinjer i planlægningskladden, som blev oprettet, inden fejlen opstod.  

Hvis feltet ikke er markeret, fortsætter kørslen Beregn Plan, indtil den er færdig. Fejl afbryder ikke kørslen. Hvis der er en eller flere fejl, vises der en meddelelse, når kørslen er afsluttet, med angivelse af, hvor mange varer der er omfattet af fejl. Siden **Log over planlægningsfejl** åbnes med flere oplysninger om fejlen og indeholder links til det eller de berørte dokumenter eller opsætningskort.  

![Fejlmeddelelser i planlægningskladden](media/NAV_APP_supply_planning_1_error_log.png "Fejlmeddelelser i planlægningskladden")  

## <a name="planning-flexibility"></a>Planlægningsfleksibilitet  
Det er ikke altid praktisk at planlægge en eksisterende forsyningsordre, når produktionen er startet, eller ekstra personer er ansat på en bestemt dag til at udføre jobbet. Med henblik på at angive om en eksisterende ordre kan ændres af planlægningssystemet, har alle forsyningsordrelinjer et planlægningsfleksibilitetsfelt med to indstillinger: Ubegrænset eller Ingen. Hvis feltet er angivet til Ingen, vil planlægningssystemet ikke forsøge at ændre forsyningsordrelinjen.  

Feltet kan manuelt indstilles af brugeren, men i nogle tilfælde angives det automatisk af systemet. Den omstændighed, at planlægningsfleksibiliteten kan angives manuelt af brugeren, er vigtig, fordi den gør det nemt at tilpasse brugen af funktionen til forskellige arbejdsgange og forretningssituationer.  

Du kan finde flere oplysninger om, hvordan dette felt bruges, i [Designoplysninger: Overførsler i planlægning](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Ordreplanlægning  
Basisforsyningens planlægningsværktøj, der er repræsenteret af siden **Ordreplanlægning**, er designet til manuel beslutningstagning. Den tager ikke højde for nogen planlægningsparametre og er derfor ikke beskrevet yderligere i dette dokument. Hvis du vil have flere oplysninger om funktionen Ordreplanlægning, kan du gå til Hjælp i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  Det anbefales ikke at bruge Ordreplanlægning, hvis firmaet anvender allerede planlægning eller indkøbskladder. Forsyningsordrer, der er oprettet via siden **Ordreplanlægning**, kan ændres eller slettes under de automatiske planlægningskørsler. Dette skyldes, at den automatiske planlægningskørsel bruger planlægningsparametre, og disse parametre kan muligvis ikke tages i betragtning af den bruger, der oprettede den manuelle plan af siden Ordreplanlægning.  

##  <a name="finite-loading"></a>Belastningsbegrænsning  
[!INCLUDE[d365fin](includes/d365fin_md.md)] er et standard ERP-system, ikke et ekspeditions- eller shop floor control-system. Det planlægger en mulig udnyttelse af ressourcer ved at tilbyde en grov plan, men det opretter og vedligeholder ikke automatisk detaljerede planer, der er baseret på prioriteter eller optimeringsregler.  

Den tilsigtede brug af funktionen kapacitetsbegrænsede ressourcer er 1): for at undgå overbelastning af bestemte ressourcer og 2): at sikre, at ingen kapacitet er ikke-allokeret, hvis det kunne sætte skub i en produktionsordre. Funktionen indeholder ingen faciliteter eller muligheder for at prioritere eller optimere operationer, som man kunne forvente at finde i et afsendelsessystem. Det kan dog fastsætte grove kapacitetsoplysninger, der er nyttige til at identificere flaskehalse og undgå overbelastning af ressourcer.  

Ved planlægning med kapacitetsbegrænsede ressourcer sikrer systemet, at der ikke indlæses nogen ressource over dens definerede kapacitet (kritisk belastning). Dette gøres ved at tildele hver operation til det nærmeste tilgængelige tidsrum. Hvis tidsrummet ikke er stort nok til at fuldføre hele handlingen, bliver handlingen opdelt i to eller flere dele, der er placeret i de nærmeste ledige tidsrum.  

> [!NOTE]  
>  I tilfælde af opdeling af operationen er opstillingstiden kun tildelt én gang, da det antages, at nogen manuel regulering er udført for at optimere planen.  

Aktionsgrænse for tid kan føjes til ressourcer for at minimere opdeling af funktionen. Dette gør det muligt for systemet at planlægge belastning på den sidst mulige dag ved at overskride den kritiske belastningsprocent en smule, hvis dette kan reducere antallet af operationer, der er opdelt.  

Dette afslutter beskrivelsen af de centrale begreber vedrørende forsyningsplanlægning i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I de følgende afsnit undersøges disse begreber nærmere, og de placeres i forbindelse med kerneplanlægningsprocedurer, justering af efterspørgsel og udbud samt brugen af genbestillingsmetoder.  

## <a name="see-also"></a>Se også  
[Designoplysninger: Overførsler i planlægning](design-details-transfers-in-planning.md)   
[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
[Designoplysninger: Tabellen Planlægningsopgave](design-details-planning-assignment-table.md)   
[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)
