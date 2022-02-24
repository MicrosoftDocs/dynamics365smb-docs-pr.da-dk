---
title: Designoplysninger – Afstemning af efterspørgsel og udbud | Microsoft Docs
description: Det er nødvendigt at forstå de prioriterede mål i planlægningssystemet for at forstå, hvordan systemet fungerer, og de vigtigste af disse er at sikre, at enhver efterspørgsel opfyldes at et tilstrækkeligt udbud, og at ethvert udbud tjener et formål.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: a1e55d983abae5f85807039da6dd4d846c3e40b3
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185704"
---
# <a name="design-details-balancing-demand-and-supply"></a>Designoplysninger: Afstemning mellem behov og forsyning
Det er nødvendigt at forstå de prioriterede mål i planlægningssystemet for at forstå, hvordan systemet fungerer, og de vigtigste er for at sikre, at:  

- Alle behov vil blive opfyldt ved tilstrækkelig forsyning.  
- Enhver forsyning tjener et formål.  

 Disse mål opnås generelt ved at afstemme forsyninger med behov.  

## <a name="demand-and-supply"></a>Behov og forsyning
 Behov er fællesbetegnelsen for enhver form for bruttobehov, som f.eks. en salgsordre og et komponentbehov fra en produktionsordre. Programmet giver desuden mulighed for mere tekniske typer behov som negativ lagerbeholdning og købsreturvarer.  

  Forsyning er fællesbetegnelsen for enhver form for positiv eller indgående mængde, f.eks. lagerbeholdning, køb, montage, produktion eller indgående overførsler. Desuden kan en salgsreturvare også repræsentere forsyning.  

  Planlægningssystemet organiserer de mange kilder for behov og forsyning på to tidslinjer, der kaldes lagerprofiler, for at få dem sorteret. En profil indeholder efterspørgsler, og den anden indeholder de tilsvarende forsyningshændelser. Hver hændelse repræsenterer én ordrenetværksenhed, f.eks. en salgsordrelinje, en varepost eller en produktionsordrelinje.  

  Når lagerprofiler er indlæst, afstemmes de forskellige behov-forsyningssæt for at fremstille en forsyningsplan, der opfylder de angivne mål.  

  Planlægningsparametre og lagerbeholdninger er andre typer af behov og forsyning, som underkastes integreret justering for at genbestille lagervarer. Du kan finde flere oplysninger i [Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Kort om begrebet Justering
  Behov afhænger af en virksomheds kunder. Forsyning er, hvad virksomheden kan oprette og fjerne for at skabe balance. Planlægningssystemet starter med det uafhængige behov og sporer derefter baglæns til forsyningen.  

   Lagerprofiler bruges til at indeholde oplysninger om behov og forsyninger, mængder og timing. Disse profiler udgør reelt to sider af afstemningsskalaen.  

   Formålet med planlægningsmekanismen er at opveje behovet og forsyningen af en vare for at sikre, at forsyning svarer til behov på en gennemførlig måde, som defineret af planlægningsparametre og -regler.  

   ![Oversigt over overensstemmelse mellem udbud og efterspørgsel](media/nav_app_supply_planning_2_balancing.png "Oversigt over overensstemmelse mellem udbud og efterspørgsel")

## <a name="dealing-with-orders-before-the-planning-starting-date"></a>Håndtering af ordrer før planlægningsstartdatoen
For at undgå, at en forsyningsplan viser umulige og derfor ubrugelige forslag, anser planlægningssystemet perioden indtil den planlagte startdato for en frossen zone, hvor intet er planlagt. Følgende regel gælder for den frosne zone:  

Alle forsyninger og behov før startdatoen for planlægningsperioden vil blive betragtet som en del af lagerbeholdningen eller leveret.  

Derfor vil planlægningssystemet ikke, med nogle få undtagelser, foreslå ændringer til forsyningsordrer i den frosne zone, og der oprettes eller vedligeholdes ingen ordresporingslinks for den pågældende periode.  

Undtagelser til denne regel er som følger:  

   * Hvis den forventede disponible beholdning, herunder summen af forsyning og behov i den frosne zone, er under nul.  
   * Hvis der kræves serienumre/lotnumre på den eller de tilbagedaterede ordrer.  
   * Hvis forsyning-behov-sæt er sammenkædet af en ordre-til-ordre-politik.  

Hvis den første disponible lagerbeholdning er under nul, foreslås der en nødforsyningsordre dagen før planlægningsperioden til at dække den manglende mængde. Derfor vil den forventede og disponible lagerbeholdning altid være mindst nul, når planlægningen for den fremtidige periode begynder. Planlægningslinjen for denne forsyningsordre viser et Nødsituation-advarselsikon, og yderligere oplysninger kan findes ved opslag.  

### <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Serienumre/lotnumre og ordre-til-ordre-links er fritaget fra den frosne zone  
   Hvis serienumre/lotnumre er nødvendige eller findes i en ordre-til-ordre-link, vil planlægningssystemet se bort fra den frosne zone og indarbejde disse mængder, der er dateret tilbage fra startdatoen, og potentielt foreslå korrigerende handlinger, hvis behov og forsyning ikke er synkroniseret. Forretningsårsagen til dette princip er, at sådanne specifikke behov-forsyningssæt skal stemme overens for at sikre, at dette specifikke behov er opfyldt.

## <a name="loading-the-inventory-profiles"></a>Indlæsning af lagerprofiler
Planlægningssystemet organiserer de mange kilder for behov og forsyning på to tidslinjer, der kaldes lagerprofiler, for at få dem sorteret.  

Normale typer af behov og forsyning med forfaldsdatoer på eller efter den planlagte startdato indlæses i hver lagerprofil. Når de er indlæst, sorteres de forskellige behovs- og forsyningstyper i henhold til overordnede prioriteter, f.eks. forfaldsdato, laveste-niveau-koder, lokation og variant. Desuden anvendes ordreprioriteter på de forskellige typer for at sikre, at de vigtigste behov opfyldes først. Du kan finde flere oplysninger i [Prioritering af ordrer](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

Som tidligere nævnt kan behov også være negativt. Det betyder, at det bør behandles som forsyning. I modsætning til de normale typer forsyning anses negative behov dog som fast forsyning. Planlægningssystemet kan tage det i betragtning, men ikke vil foreslå ændringer.  

Generelt tager planlægningssystemet højde for alle forsyningsordrer efter den planlagte startdato i forbindelse med ændringer for at opfylde behovet. Så snart et antal er bogført fra en forsyningsordre, kan det dog ikke længere ændres af planlægningssystemet. Derfor kan følgende forskellige ordrer ikke planlægges om:  

- Frigivne produktionsordrer, hvor der er bogført forbrug eller afgang.  
- Montageordrer, hvor der er bogført forbrug eller afgang.  
- Overflytningsordrer, hvor leverancen er blevet bogført.  
- Indkøbsordrer, hvor modtagelsen er blevet bogført.  

Bortset fra indlæsning af behovs- og forsyningstyper, indlæses visse typer med opmærksomhed på særlige regler og afhængigheder, der er beskrevet i det følgende.  

### <a name="item-dimensions-are-separated"></a>Varedimensioner er adskilt  
Forsyningsplanen skal beregnes pr. kombination af varedimensioner, f.eks. variant og lokation. Der er ingen grund til at beregne nogen teoretisk kombination. Kun de kombinationer, der bærer behov og/eller forsyning, skal beregnes.  

Planlægningssystemet kontrollerer dette ved at køre gennem lagerprofilen. Når der findes en ny kombination, opretter programmet en automatisk kontrolpost, der indeholder den faktiske kombinationsoplysninger. Programmet indsætter lagervaren som kontrolpost eller ydre løkke. Derfor angives de korrekte planlægningsparametre i overensstemmelse med en kombination af variant og placering, og programmet kan gå videre til den indre løkke.  

> [!NOTE]  
>  Programmet kræver ikke, at brugeren angiver en lagervarepost ved angivelse af behov og/eller forsyning for en bestemt kombination af variant og lokation. Hvis der ikke findes en lagervare for en given kombination, opretter programmet derfor sin egen midlertidige lagervare baseret på varekortdata. Hvis Tvungen lokationskode er angivet til Ja på siden Lageropsætning, skal der oprettes en Lagervare, eller komponenter på lokation skal angives til Ja. Du kan finde flere oplysninger i [Designoplysninger: Behov på lokationen TOM](design-details-demand-at-blank-location.md).  

### <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Serienumre/lotnumre indlæses efter specifikationsniveau  
Attributter i form af serie-/lotnumre indlæses i lagerprofilerne sammen med det behov og den forsyning, de er tildelt.  

Behov- og forsyningsattributter arrangeres efter ordreprioritet og efter deres specifikationsniveau. Da afstemte serienumre/lotnumre afspejler specifikationsniveauet, vil de mere specifikke behov, som f.eks. et lotnummer, der er valgt specifikt til en salgslinje, søge efter en overensstemmelse, før mindre specifikke behov, f.eks. et salg fra et valgt lotnummer.  

> [!NOTE]  
>  Der er ingen dedikerede prioriteringsregler for serie-/lotnummereret behov og forsyning udover niveauet af specifikation, der er defineret af deres kombinationer af serie- og lotnumre og varesporingsopsætningen for de involverede varer.  

Under justering anser planlægningssystemet forsyning, der har serienumre/lotnumre, for ufleksible og forsøger ikke at forøge eller omplanlægge sådanne forsyningsordre (medmindre de bruges i en ordre-til-ordre-relation). Se Ordre-til-ordre-links er aldrig brudt). Dette sikrer, at forsyningen ikke modtager flere, eventuelt modstridende aktionsmeddelelser, når en forsyning har forskellige attributter, f.eks. en samling af forskellige serienumre.  

En anden grund til, at serie-/lotnummereret forsyning er ufleksibel er, at serie-/lotnumre generelt tildeles så sent i processen, at det ville være forvirrende, hvis der foreslås ændringer.  

Afstemning af serienumre/lotnumre overholder ikke den *frosne zone*. Hvis behov og forsyning ikke er synkroniseret, kan planlægningssystemet foreslå ændringer eller foreslå nye ordrer, uanset den planlagte startdato.  

### <a name="order-to-order-links-are-never-broken"></a>Ordre-til-ordre-links er aldrig brudt  
Ved planlægning af en ordre-til-ordre-vare må den tilknyttede forsyning ikke bruges til andre behov end det, den oprindeligt var tiltænkt. Sammenkædede behov bør ikke være dækket af andre tilfældige forsyninger, selv om den aktuelt er tilgængelig i tid og antal. En montageordre, der er knyttet til en salgsordre i et montage-til-ordre-scenarie, kan f.eks. ikke bruges til at dække andre behov.  

Ordre-til-ordre efterspørgsel og udbud skal afstemmes nøjagtigt. Planlægningssystemet sikrer forsyningen under alle omstændigheder uden hensyntagen til ordrestørrelsesparametre, modifikatorer og antal på lager (bortset fra antal, der er relateret til linkede ordrer). Af samme grund foreslår systemet at reducere overskydende forsyninger, hvis det tilknyttede behov reduceres.  

Denne udligning påvirker også timingen. Den begrænsede horisont, der er givet af intervallet, tages ikke i betragtning. Forsyning flyttes, hvis timingen af behovet er blevet ændret. Aktionsgrænsen for tid vil dog blive overholdt og vil forhindre, at ordre-til-ordre-forsyninger planlægges, bortset fra de interne forsyninger af en produktionsordre med flere niveauer (projektordre).  

> [!NOTE]  
>  Serienumre/lotnumre kan også angives på ordre-til-ordre efter behov. I så fald betragtes forsyning ikke som fleksibel som standard, hvilket normalt er tilfældet for serienumre/lotnumre. I så fald vil systemet øge/reducere efter ændringer i behovet. Hvis ét behov desuden har forskellige serie-/lotnumre, som f.eks. mere end ét lotnummer, vil der blive foreslået en forsyningsordre pr. lot.  

> [!NOTE]  
>  Forecasts bør ikke føre til at oprettelse af forsyningsordrer, der er bundet af et ordre-til-ordre-link. Hvis forecast bruges, skal det kun bruges som en generator af afhængigt behov i et produktionsmiljø.  

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Komponentbehov er indlæst i overensstemmelse med ændringer af produktionsordrer  
Ved håndtering af produktionsordrer skal planlægningssystemet overvåge de nødvendige komponenter, før de indlæses i behovsprofilen. Komponentlinjer, der skyldes en ændret produktionsordre, erstatter dem fra den oprindelige ordre. Dette sikrer, at planlægningssystemet definerer, at planlægningslinjer for komponentbehov aldrig kopieres.  

###  <a name="safety-stock-may-be-consumed"></a><a name="BKMK_SafetyStockMayBeConsumed"></a> Sikkerhedslager kan forbruges  
Sikkerhedslageret er primært en behovstype og indlæses derfor i lagerprofilen på planlægningens startdato.  

Sikkerhedslager er et lagerantal, der er lagt til side for at kompensere for usikkerheden i behov under leveringstiden for genopfyldning. Det kan dog forbruges, hvis det er nødvendigt at tage fra det for at opfylde et behov. I dette tilfælde, vil planlægningssystemet sikre, at sikkerhedslageret hurtigt fyldes igen ved at foreslå en forsyningsordre den dag, hvor sikkerhedslageret opbruges. Denne planlægningslinje vil vise ikonet Undtagelsesadvarsel, som forklarer planlæggeren, at sikkerhedslageret er blevet helt eller delvist opbrugt ved brug af en undtagelsesordre for det manglende antal.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>Forecastbehov reduceres af salgsordrer  
Behovsprognosen udtrykker det forventede fremtidige behov. Mens faktisk behov angives, normalt som salgsordrer for producerede varer, bruger den prognosen.  

Selve forecastet er ikke reelt reduceret af salgsordrer; det forbliver det samme. Dog reduceres forecastantal i beregningen af planlægning (med salgsordremængder) før det eventuelle resterende antal i behovet for lagerprofilen. Når planlægningssystemet undersøger faktiske salgstal i en periode, medtages både åbne salgsordrer og vareposter fra leverede salg, medmindre de stammer fra en rammeordre.  

En bruger skal angive en gyldig prognoseperiode. Datoen på det planlagte antal angiver starten af perioden, og datoen på det næste forecast angiver slutningen af perioden.  

Forecast for perioder før planlægningsperioden bruges ikke, uanset om det er forbrugt eller ej. Det første budgetterede tal af interesse er enten datoen eller den nærmeste dato før planlægningens startdato.  

Forecast kan være for uafhængige behov som salgsordrer eller afhængige behov som produktionsordrekomponenter (modul-forecast). En vare kan have begge typer forecast. Under planlægningen sker forbruget separat, først for uafhængige behov og derefter for afhængige behov.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Rammeordrebehov reduceres af salgsordrer  
Forecastfunktionaliteten suppleres af rammesalgsordren som en måde til at angive fremtidige behov fra en bestemt kunde. Som med (uspecificerede) prognoser bør faktiske salg forbruge det forventede behov, og det resterende antal bør indgå i behovslagerprofilen. Igen, forbruget reducerer ikke rammeordren.  

Planlægningsberegningen finder åbne salgsordrer, der er knyttet til den bestemte rammeordrelinje, men den tager ikke hensyn til en gyldig periode. Der tages heller ikke højde for bogførte ordrer, da bogføringsproceduren allerede har reduceret udestående rammeordreantal.

## <a name="prioritizing-orders"></a>Prioritering af ordrer
Inden for en given SKU repræsenterer den anmodede eller tilgængelige dato den højeste prioritet. Behovene i dag skal behandles før behovene for næste uge. Men ud over denne overordnede prioritet foreslår planlægningssystemet også, hvilken type behov der skal være opfyldt, inden andre behov opfyldes. Det foreslås ligeledes, hvilken forsyningskilde der skal anvendes, før du anvender andre forsyningskilder. Dette udføres i overensstemmelse med ordreprioriteter.  

Indlæst behov og forsyning, der bidrager til en profil for den planlagte lagerbeholdning i henhold til følgende prioriteter:  

### <a name="priorities-on-the-demand-side"></a>Prioriteter på efterspørgselssiden  
1. Allerede leveret: varepost  
2. Købsreturvareordre  
3. Salgsordre  
4. Serviceordre  
5. Produktionskomponentbehov  
6. Montageordrelinje  
7. Udgående overflytningsordre  
8. Rammeordre (der ikke allerede er brugt af relaterede salgsordrer)  
9. Forecast (der ikke allerede er anvendt af andre salgsordrer)  

> [!NOTE]  
>  Købsreturvarer er normalt ikke involveret i forsyningsplanlægning. De skal altid være reserveret fra det lot, der skal returneres. Hvis den ikke er reserveret, spiller købsreturvarer en rolle i udbuddet og er højt prioriteret for at undgå, at planlægningssystemet foreslår en forsyningsordre, der blot skal tjene et købsreturnering.  

### <a name="priorities-on-the-supply-side"></a>Prioriteter på forsyningssiden  
1. Allerede på lager: Varepost (planlægningsfleksibilitet = ingen)  
2. Salgsreturvareordre (planlægningsfleksibilitet = ingen)  
3. Indgående overflytningsordre  
4. Produktionsordre  
5. Montageordre  
6. Købsordre  

### <a name="priority-related-to-the-state-of-demand-and-supply"></a>Prioritet, der er relateret til tilstand af efterspørgsel og udbud  
Bortset fra de prioriteter, der er angivet af typen af behov og forsyning, definerer den nuværende ordrestatus i udførelsesprocessen også en prioritet. Lageraktiviteter har f.eks. indflydelse, og status for salg, køb, overførsel, montage og produktionsordrer tages i betragtning:  

1. Delvist håndteres (planlægningsfleksibilitet = ingen)  
2. Allerede under behandling i lageret (planlægningsfleksibilitet = ingen)  
3. Frigivet – alle ordretyper (planlægningsfleksibilitet = ubegrænset)  
4. Fastlagt og planlagt produktionsordre (planlægningsfleksibilitet = ubegrænset)  
5. Planlagt/åben – alle ordretyper (planlægningsfleksibilitet = ubegrænset)

## <a name="balancing-supply-with-demand"></a>Afstemning af behov og forsyning
Kernen i planlægningssystemet omfatter udlignende efterspørgsel og udbud ved at foreslå brugerhandlinger for at revidere forsyningsordrer, når der er ubalance. Dette sker pr. kombination af variant og lokation.  

Forestil dig, at hver lagerprofil indeholder en streng af behovshændelser (sorteret efter dato og prioritet) og en tilsvarende streng af forsyningshændelser. Hver hændelse refererer tilbage til dens kildetype og identifikation. Reglerne for afstemning af varen er ligetil. Fire forekomster af tilsvarende behov og forsyning kan ske på et hvilket som helst tidspunkt i processen:  

1. Der findes ingen behov eller forsyning for varen = > planlægning er afsluttet (eller bør ikke starte).  
2. Behov findes, men der er ingen forsyning = > forsyning bør foreslås.  
3. Forsyning findes, men der er ingen efterspørgsel for det = > forsyning bør annulleres.  
4. Både behov og forsyning findes = > spørgsmål bør stilles og besvares, før systemet kan sikre, at efterspørgslen imødekommes og forsyningen er tilstrækkelig.  

    Hvis tidspunktet for forsyning ikke er egnet, kan den måske planlægges som følger:  

    1.  Hvis forsyningen er placeret tidligere end behovet, kan forsyningen måske planlægges om, så lageret er så lavt som muligt.  
    2.  Hvis levering er senere end behovet, kan levering måske planlægges igen. I modsat fald foreslås ny forsyning.  
    3.  Hvis forsyningen opfylder behovet på datoen, kan planlægningssystemet fortsætte med at undersøge, om forsyningsantallet kan dække behovet.  

    Når timingen er på plads, kan den passende leveringsmængde beregnes på følgende måde:  

    1.  Hvis forsyningsantallet er mindre end behovet, er det muligt, at forsyningsantallet kan øges (eller ikke, hvis begrænset af en maksimummængdepolitik).  
    2.  Hvis forsyningsantallet er større end behovet, er det muligt, at forsyningsantallet kan reduceres (eller ikke, hvis begrænset af en minimummængdepolitik).  

    På nuværende tidspunkt er en af disse to situationer aktuelle:  

    1.  Det aktuelle behov kan dækkes, i hvilket tilfælde det kan lukkes, og planlægning af næste behov kan starte.  
    2.  Forsyningen har nået sit maksimum og efterlader nogle i behovsantallet uafdækkede. I dette tilfælde kan planlægningssystemet lukke den aktuelle forsyning og gå videre til den næste.  

 Proceduren starter forfra med det næste behov og den aktuelle forsyning eller omvendt. Den aktuelle forsyning kan måske dække dette næste behov, eller det aktuelle behov er ikke endnu fuldt dækket.  

### <a name="rules-concerning-actions-for-supply-events"></a>Regler for handlinger for forsyningshændelser  
Når planlægningssystemet opretter en top-down-beregning, hvor forsyningen skal opfylde behovet, tages behovet for givet, det vil sige, det ligger uden for kontrol af planlægningssystemet. Men forsyningssiden kan administreres. Planlægningssystemet foreslår derfor oprettelse af nye forsyningsordrer, omlægning af eksisterende og/eller ændring af ordreantallet. Hvis en eksisterende forsyningsordre bliver overflødig, foreslår planlægningssystemet, at brugeren annullerer den.  

Hvis brugeren ønsker at udelukke en eksisterende forsyningsordre fra planlægningsforslagene, han brugeren angive, at den har ingen planlægningsfleksibilitet (planlægningsfleksibilitet = ingen). Derefter bliver overskydende forsyning fra den pågældende ordre brugt til at dække behov, men der foreslås ingen handling.  

Alle forsyninger har generelt en planlægningsfleksibilitet, som er begrænset af betingelserne for hver af de foreslåede handlinger.  

-   **Omplanlæg ud**: Datoen for en eksisterende forsyningsordre kan planlægges ud til at imødekomme behovets forfaldsdato, medmindre:  

    -   Det repræsenterer lager (altid på dag nul).  
    -   Den har en ordre-til-ordre, der er knyttet til et andet behov.  
    -   Det ligger uden for den omplanlægningsside, der er defineret i intervallet.  
    -   Der er en forsyning tættere på, der kan anvendes.  
    -   På den anden side kan brugeren beslutte at omplanlægge, fordi:  
    -   Forsyningsordren er allerede knyttet til et andet behov på en tidligere dato.  
    -   Den nødvendige ændring i planen er så minimal, at brugeren finder den ubetydelig.  

-   **Omplanlæg ind**: Datoen for en eksisterende forsyningsordre, der kan planlægges, undtagen under følgende betingelser:  

    -   Det er knyttet direkte til et andet behov.  
    -   Det ligger uden for den omplanlægningsside, der er defineret i intervallet.  

> [!NOTE]  
>  Ved planlægning af en vare ved hjælp af et genbestillingspunkt kan forsyningsordrer altid planlægges med, hvis der er behov for det. Det er almindeligt i forbindelse med forsyningsordrer, der er planlagt fremad, og som er udløst af et genbestillingspunkt.  

-   **Øg antal**: Antallet af en eksisterende forsyningsordre kan øges for at imødekomme behovet, medmindre forsyningsordren er knyttet direkte til et behov efter et ordre-til-ordre-link.  

> [!NOTE]  
>  Selvom det er muligt at øge forsyningsordren, kan det være begrænset på grund af et defineret maksimalt ordreantal.  

-   **Reducer antal**: En eksisterende forsyningsordre med et overskud sammenlignet med et eksisterende behov kan reduceres for at opfylde behovet.  

> [!NOTE]  
>  Selvom antallet kan blive reduceret, kan der stadig være overskud, sammenlignet med behovet, på grund af et defineret minimumsordreantal eller en oprundingsfaktor.  

-   **Annuller**: Som et særligt tilfælde af handlingen, der reducerer antallet, kan forsyningsordren blive annulleret, hvis den er reduceret til nul.  
-   **Ny**: Hvis der ikke allerede findes en forsyningsordre, eller en eksisterende ikke kan ændres for at opfylde det nødvendige antal på den efterspurgte forfaldsdato, foreslås der en ny forsyningsordre.  

### <a name="determining-the-supply-quantity"></a>Bestemmelse af forsyningsantallet  
Planlægningsparametre, der er defineret af brugeren, styrer det foreslåede antal af hver forsyningsordre.  

Når planlægningssystemet beregner antallet af en ny forsyningsordre eller ændring af antallet på en eksisterende, kan det foreslåede antal være forskelligt fra det, der faktisk kræves.  

Hvis en maksimal lager- eller fast ordremængde er valgt, kan det foreslåede antal øges for at opfylde det faste antal eller det maksimale lagerniveau. Hvis genbestillingsmetoden bruger et genbestillingspunkt, kan antallet forhøjes for i det mindste at opfylde genbestillingspunktet.  

 Det foreslåede antal kan ændres i denne rækkefølge:  

1. Ned til det højst tilladte ordreantal (hvis der er et).  
2. Op til det mindste ordreantal.  
3. Op til at opfylde den nærmeste oprundingsfaktor. (I tilfælde af forkerte indstillinger kan den højst tilladte ordrestørrelse overskrides).  

### <a name="order-tracking-links-during-planning"></a>Ordresporingsbindinger under planlægning  
Med hensyn til ordresporing under planlægning, er det vigtigt at nævne, at planlægningssystemet omarrangerer de dynamisk oprettede ordresporingsbindinger til vare-/variant-/lokationskombinationerne.  

Der er to grunde til dette:  

-   Planlægningssystemet skal være i stand til at begrunde sine forslag om at alle behov er dækket, og at ingen forsyningsordrer er overflødige.  
-   Dynamisk oprettede ordresporingsbindinger skal regelmæssigt afstemmes.  

I tidens løb bliver dynamiske ordresporingsbindinger uafstemte, fordi det samlede ordresporingsnetværk ikke omarrangeres, før en behovs- eller forsyningshændelse faktisk er lukket.  

Før udligning af forsyning med behov, sletter programmet alle eksisterende ordresporingsbindinger. Under den udlignende procedure, når en behovs- eller forsyningshændelse er lukket, etablerer det derefter nye ordresporingsbindinger mellem forsyning og behov.  

> [!NOTE]  
>  Selvom varen ikke er konfigureret til dynamisk ordresporing, opretter planlægningssystemet afstemte ordresporingsbindinger, som forklaret ovenfor.
## <a name="closing-demand-and-supply"></a>Lukning af behov og forsyning
Når de forsyningsudlignende procedurer er blevet udført, er der tre mulige slutsituationer:  

* Det påkrævede antal og den påkrævede dato for behovhændelserne er opfyldt, og planlægning af dem kan lukkes. Forsyningshændelsen er stadig åben og kan dække det næste behov, så udligningsproceduren kan starte forfra med den aktuelle forsyningshændelse og det næste behov.  
* Forsyningsordren kan ikke ændres, så den dækker alle behov. Behovshændelsen er stadig åben, med nogle udækkede antal, der kan dækkes ved næste forsyningshændelse. Derfor lukkes den aktuelle forsyning, så den udlignende handling kan starte forfra med det aktuelle behov og den næste forsyningshændelse.  
* Alle behov er blevet dækket: Der er ingen efterfølgende behov (eller der har ikke været nogen behov overhovedet). Hvis der er en eventuel overskydende forsyning, kan den reduceres (eller annulleres) og derefter lukkes. Det er muligt, at der findes yderligere forsyningshændelser i kæden, og de bør også annulleres.  

Endelig opretter planlægningssystemet et ordresporingslink mellem forsyning og behov.  

### <a name="creating-the-planning-line-suggested-action"></a>Oprettelse af planlægningslinjen (foreslået aktivitet)  
Hvis en handling – Ny, Ret antal, Omplanlæg, Omplanlæg og ret antal eller Annuller – foreslås for at revidere forsyningsordren, vil planlægningssystemet oprette en planlægningslinje i planlægningskladden. På grund af ordresporing oprettes planlægningslinjen ikke kun, når forsyningshændelsen er lukket, men også hvis behovhændelsen er lukket, selvom forsyningshændelsen stadig er åben og kan være underlagt yderligere ændringer, når næste behovshændelse behandles. Det betyder, at når planlægningslinjen er oprettet, kan den ændres igen.  

Planlægningslinjen kan vedligeholdes i tre niveauer for at minimere databaseadgang, når der håndteres produktionsordrer, mens det tilstræbes at udføre det mindst krævende vedligeholdelsesniveau:  

* Opret kun planlægningslinjen med den aktuelle forfaldsdato og antallet, men uden rute og komponenter.  
* Omfatter rute: Den planlagte rute er opstillet med beregning af start- og slutdatoer og -tidspunkter. Dette er påkrævet i forbindelse med adgang til databasen. For at bestemme slutdato og forfaldsdatoer kan det være nødvendigt at beregne dette, selvom forsyningshændelsen ikke er blevet lukket (i tilfælde af fremadrettet planlægning).  
* Omfatter styklisteudfoldelsen: Dette kan vente indtil lige før leveringshændelsen er lukket.  

Dette afslutter beskrivelserne af, hvordan behov og forsyning indlæses, prioriteres og afstemmes af planlægningssystemet. I integration med denne planlægningsaktivitet af forsyning skal systemet sikre, at det nødvendige lagerniveau for hver planlagt vare opretholdes i overensstemmelse med dens genbestillingsmetoder.

## <a name="see-also"></a>Se også  
 [Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)   
 [Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
 [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
