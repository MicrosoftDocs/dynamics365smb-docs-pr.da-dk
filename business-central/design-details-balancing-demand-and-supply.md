---
title: Designoplysninger - Afstemning mellem udbud og efterspørgsel
description: 'Denne artikel beskriver, hvordan du prioriterede mål efter balanceret levering med behov.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/15/2022
ms.custom: bap-template
---
# <a name="design-details-balancing-supply-and-demand"></a><a name="design-details-balancing-supply-and-demand"></a>Designoplysninger: Afstemning mellem udbud og efterspørgsel

Hvis du vil have en forståelse af, hvordan planlægningssystemet fungerer, er det vigtigt at forstå, om det er prioriterede mål:  

* Alle behov vil blive opfyldt ved tilstrækkelig forsyning.  
* Enhver forsyning tjener et formål.  

Disse mål opnås generelt ved at afstemme forsyninger med behov.  

## <a name="supply-and-demand"></a><a name="supply-and-demand"></a>Udbud og efterspørgsel

Betegnelsen *udbud* henviser til enhver form for positiv eller indgående mængde, f. eks.:

* Lager
* Køb
* Montage
* Produktion
* Indgående overflytning
* Salgsreturneringer  

Betegnelsen *Efterspørgsel* henviser til en hvilken som helst form for bruttobehov, f. eks.:

* Opret en salgsordre for en vare
* Komponent til produktionsordre

[!INCLUDE [prod_short](includes/prod_short.md)] giver desuden mulighed for mere tekniske typer behov som negativ lagerbeholdning og købsreturvarer.

Planlægningssystemet organiserer de mange kilder for udbud og efterspørgsel på to tidslinjer, der kaldes lagerprofiler, for at få dem sorteret. En profil indeholder efterspørgsler, og den anden indeholder de tilsvarende forsyningshændelser. Hver forsyningshændelse repræsenterer én enhed i en ordre, f. eks.:

* En salgsordrelinje
* En varepost
* En produktionslinje

Når lagerprofiler er indlæst, afstemmes behov-forsyningssæt for at fremstille en forsyningsplan, der opfylder de angivne mål.

Lagerniveauer og planlægningsparametre er andre former for udbud og efterspørgsel. Disse typer underkastes integreret justering til genopfyldningsvarer. Flere oplysninger [Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a><a name="the-concept-of-balancing-in-brief"></a>Kort om begrebet Justering

Efterspørgslen kommer fra dine kunder. Forsyning er, hvad virksomheden kan oprette og fjerne for at skabe balance. Planlægningssystemet starter med behovet og sporer derefter baglæns til forsyningen.  

Lagerprofiler indeholder oplysninger om udbud og efterspørgsel, mængder og timing. Disse profiler udgør to sider af afstemningsskalaen.  

Formålet med planlægningsmekanismen er at opveje udbud og efterspørgsel for en vare for at sikre, at forsyning svarer til behov på en gennemførlig måde, som defineret af planlægningsparametre og -regler.  

:::image type="content" source="media/nav_app_supply_planning_2_balancing.png" alt-text="Oversigt over overensstemmelse mellem udbud og efterspørgsel.":::

## <a name="process-orders-before-the-planning-start-date"></a><a name="process-orders-before-the-planning-start-date"></a>Håndtering af ordrer før planlægningsstartdatoen

For at undgå at en forsyningsplan viser urimelige forslag, planlægger planlægningssystemet ikke noget i perioden før planlægningens startdato. Følgende regel gælder for den periode:

* Alle forsyninger og behov før startdatoen for planlægningsperioden vil blive betragtet som en del af lagerbeholdningen eller leveret.  

Derfor vil planlægningssystemet ikke, med nogle få undtagelser, foreslå ændringer til forsyningsordrer i perioden, og der oprettes eller vedligeholdes ingen ordresporingslinks for den pågældende periode. Følgende er undtagelser til denne regel:  

* Det lager, der forventes at være tilgængelig, herunder summen af udbud og efterspørgsel i den periode, er under nul.  
* Tilbagedaterede ordrer kræver serienumre eller lotnumre.  
* Hvis forsyning-behov-sæt er sammenkædet af en ordre-til-ordre-politik. 

Hvis den første disponible lagerbeholdning er under nul, foreslås der en nødforsyningsordre dagen før planlægningsperioden til at dække den manglende mængde. Derfor vil den forventede og disponible lagerbeholdning altid være mindst nul, når planlægningen for den fremtidige periode begynder. Planlægningslinjen for denne forsyningsordre viser et Nødsituation-advarselsikon, og yderligere oplysninger kan findes ved opslag.

### <a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period"></a><a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period"></a>Serienumre og lotnumre og ordre-til-ordre-links er fritaget fra den tidligere periode

Hvis der kræves serie-eller lotnumre for at oprette en ordre-til-ordre-kæde, tilsidesætter planlægningssystemet reglen for den forrige periode. Den vil omfatte tilbagedaterede mængder fra startdatoen og kan foreslå korrigerende handlinger, hvis udbud og efterspørgsel ikke synkroniseres. Disse udbud og efterspørgsel-sæt skal stemme overens for at sikre, at et bestemt behov er opfyldt.

## <a name="load-inventory-profiles"></a><a name="load-inventory-profiles"></a>Indlæsning af lagerprofiler

Planlægningssystemet organiserer de mange kilder for udbud og efterspørgsel på to tidslinjer, der kaldes lagerprofiler, for at få dem sorteret.  

Udbud og efterspørgsel med forfaldsdatoer på eller efter den planlagte startdato indlæses i hver lagerprofil. Når udbud- og efterspørgselstyperne indlæses, sorteres de i henhold til de generelle prioriteter, f. eks.:

* Forfaldsdato
* laveste-niveaukoder
* Lokation
* Variant

Ordreprioriteter anvendes på de forskellige typer for at sikre, at de vigtigste behov opfyldes først. Få mere at vide om [Prioritering af ordrer](design-details-balancing-demand-and-supply.md#prioritize-orders).  

Behov kan også være negativ. Behandle negativt behov som levering. I modsætning til almindelig levering betragtes negative behov imidlertid som fast levering. Planlægningssystemet kan tage det i betragtning, men ikke vil foreslå ændringer.  

Generelt tager planlægningssystemet højde for alle forsyningsordrer efter den planlagte startdato i forbindelse med ændringer for at opfylde behovet. Så snart et antal er bogført fra en forsyningsordre, kan ikke længere ændres af planlægningssystemet. Følgende ordrer kan ikke planlægges:  

* Frigivne produktionsordrer, hvor der er bogført forbrug eller afgang.  
* Montageordrer, hvor der er bogført forbrug eller afgang.  
* Overflytningsordrer, hvor leverancen er blevet bogført.  
* Indkøbsordrer, hvor modtagelsen er blevet bogført.  

Bortset fra indlæsning af udbud og efterspørgsel-typer, indlæses visse typer med opmærksomhed på særlige regler og afhængigheder. I følgende afsnit i artiklen beskrives reglerne og afhængighederne.  

### <a name="item-dimensions-are-separated"></a><a name="item-dimensions-are-separated"></a>Varedimensioner er adskilt

Forsyningsplanen skal beregnes pr. kombination af varedimensioner, f.eks. variant og lokation. Kun de kombinationer, der bærer behov og/eller forsyning, skal beregnes.  

Planlægningssystemet søger efter kombinationer i lagerprofilen. Når der findes en ny kombination, opretter programmet en automatisk kontrolpost, der indeholder oplysninger om kombinationen. Planlægningssystemet indsætter SKU som kontrolpost eller ydre løkke. Derfor angives de korrekte planlægningsparametre i overensstemmelse med en kombination af variant og placering, og programmet kan gå videre til den indre løkke. 

> [!NOTE]  
> Du skal ikke angive en SKU-post, når du angiver en behov og/eller forsyning for en bestemt kombination af variant og lokation. Hvis der ikke findes en SKU for en given kombination, opretter [!INCLUDE [prod_short](includes/prod_short.md)] derfor sin egen midlertidige SKU baseret på varekortdata. Hvis **Tvungen lokationskode** er angivet til Ja på siden **Lageropsætning**, skal der oprettes en Lagervare, eller **komponenter på lokation** skal angives til Ja. Flere oplysninger i [Planlægge med eller uden lokationer](production-planning-with-without-locations.md).  

### <a name="serial-and-lot-numbers-are-loaded-by-specification-level"></a><a name="serial-and-lot-numbers-are-loaded-by-specification-level"></a>Serienumre/lotnumre indlæses efter specifikationsniveau

Serie-/lotnumre indlæses i lagerprofilerne sammen med det behov og udbud og efterspørgsel, de er tildelt.  

Udbud og efterspørgselsattributter arrangeres efter ordreprioritet og efter deres specifikationsniveau. Da serie-og lotnummer svarer til specifikations niveauet, vil et mere specifikt behov stemme overens før et mindre specifikt behov. Et specifikt behov kan f. eks. være et lotnummer, der er angivet for en salgslinje. Et mindre specifikt behov kan være et salg fra et hvilket som helst lotnummer.

> [!NOTE]  
> De eneste dedikerede prioriteringsregler for serie-/lotnummereret behov og forsyning udover niveauet af specifikation, der er defineret af deres kombinationer af serie- og lotnumre og varesporingsopsætningen for de involverede varer.  

Under udligning vurderer planlægningssystemet forsyning, der har serie-og lotnumre, som ufleksibelt. Systemet vil ikke stige eller omplanlægge forsyningsordrer. Den eneste undtagelse er, hvis de bruges i en ordre-til-ordre-relation. Se [Ordre-til-ordre-links er aldrig brudt](#order-to-order-links-are-never-broken). Denne undtagelse beskytter forsyningen fra modtagelse af flere, eventuelt modstridende aktionsmeddelelser, når en forsyning har forskellige attributter. Du kan f. eks. variere attributter, når levering har en samling forskellige serienumre.  

En anden årsag til, at serie- og lotnumre er infleksible, er, fordi serie- og lotnumre ofte tildeles sent i processen. Det kan være forvirrende, hvis der foreslås ændringer på dette punkt.  

Serie- og lotnummer betyder, at reglen ikke planlægges før startdatoen for planlægningen. Hvis udbud og efterspørgsel ikke er synkroniseret, kan planlægningssystemet foreslå ændringer eller foreslå nye ordrer, uanset den planlagte startdato.  

### <a name="order-to-order-links-are-never-broken"></a><a name="order-to-order-links-are-never-broken"></a>Ordre-til-ordre-links er aldrig brudt

Ved planlægning af en ordre-til-ordre-vare må den tilknyttede forsyning ikke bruges til det, den oprindeligt var tiltænkt. Sammenkædede behov bør ikke være dækket af andre tilfældige forsyninger, selv om den leveringen er tilgængelig i tid og antal. En montageordre, der er knyttet til en salgsordre i et montage-til-ordre-scenarie, kan f.eks. ikke bruges til at dække andre behov.  

Ordre-til-ordre efterspørgsel og udbud skal afstemmes nøjagtigt. Planlægningssystemet sikrer forsyningen uden hensyntagen til ordrestørrelsesparametre, modifikatorer og antal på lager (bortset fra antal, der er relateret til linkede ordrer). Af samme grund foreslår systemet at reducere overskydende forsyninger, hvis det tilknyttede behov reduceres.  

Denne udligning påvirker også timingen. Den begrænsede horisont, der er givet af intervallet, tages ikke i betragtning. Forsyning flyttes, hvis timingen af behovet er blevet ændret. Aktionsgrænsen for tid vil dog blive overholdt og vil forhindre, at ordre-til-ordre-forsyninger planlægges, bortset fra de interne forsyninger af en produktionsordre med flere niveauer (projektordre).  

> [!NOTE]  
> Serienumre/lotnumre kan også angives på ordre-til-ordre efter behov. I så fald betragtes forsyning ikke som fleksibel som standard, hvilket normalt er tilfældet for serienumre/lotnumre. I så fald vil systemet øge/reducere efter ændringer i behovet. Hvis ét behov desuden har forskellige serie-/lotnumre, som f.eks. mere end ét lotnummer, vil der blive foreslået en forsyningsordre pr. lot.  

> [!NOTE]  
> Forecasts bør ikke føre til at oprettelse af forsyningsordrer, der er bundet af et ordre-til-ordre-link. Hvis forecast bruges, skal det kun bruges som en generator af afhængigt behov i et produktionsmiljø.

### <a name="component-need-is-loaded-according-to-production-order-changes"></a><a name="component-need-is-loaded-according-to-production-order-changes"></a>Komponentbehov er indlæst i overensstemmelse med ændringer af produktionsordrer

Ved håndtering af produktionsordrer skal planlægningssystemet overvåge de nødvendige komponenter, før de indlæses i behovsprofilen. Komponentlinjer, der skyldes en ændret produktionsordre, erstatter dem fra den oprindelige ordre. Ændringen sikrer, at planlægningssystemet ikke duplikerer planlægningslinjer for komponentbehov.  

### <a name="consume-safety-stock"></a><a name="consume-safety-stock"></a>Forbrug sikkerhedslager

Mængden i sikkerhedslageret er en behovstype og indlæses derfor i lagerprofilen på planlægningens startdato.  

Sikkerhedslager er et lagerantal, der er lagt til side for at kompensere for usikkerheden i behov under leveringstiden for genopfyldning. Du kan dog bruge den til at opfylde et behov. I så fald vil planlægningssystemet sikre, at sikkerhedslageret hurtigt kan udskiftes. Systemet foreslår en forsyningsordre for at genopfylde sikkerhedslageret på den dato, det forbruges. Planlægningslinjen vil vise ikonet Undtagelsesadvarsel, som forklarer planlæggeren, at sikkerhedslageret er blevet helt eller delvist opbrugt ved brug af en undtagelsesordre for det manglende antal.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a><a name="forecast-demand-is-reduced-by-sales-orders"></a>Forecast-behov reduceres af salgsordrer

Behovsprognosen udtrykker det forventede fremtidige behov. Mens faktisk behov angives, normalt som salgsordrer for producerede varer, bruger den prognosen.

Selve forecast reduceres ikke af salgsordrer. Dog reduceres forecastantal i beregningen af planlægning (med salgsordremængder) før det eventuelle resterende antal i behovet for lagerprofilen. I forbindelse med salg i en periode indeholder planlægningen både åbne salgsordrer og vareposter fra leverede salg. Undtagelsen til denne regel er, når de stammer fra en rammeordre.  

Du skal angive en gyldig prognoseperiode. Datoen på det planlagte antal angiver starten af perioden, og datoen på det næste forecast angiver slutningen af perioden.  

Forecast for perioder før planlægningsperioden bruges ikke, uanset om det er forbrugt eller ej. Det første budgetterede tal af interesse er enten datoen for planlægningens startdato eller den nærmeste dato.  

Budgettet kan være til forskellige behovstyper:

* Uafhængigt behov, f. eks. salgsordrer
* Afhængigt behov, f. eks. komponenter til produktionsordrer.

En vare kan have begge typer forecast. Under planlægningen sker forbruget separat, først for uafhængige behov og derefter for afhængige behov.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a><a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Rammeordrebehov reduceres af salgsordrer

Forecastfunktionaliteten suppleres af rammesalgsordrer som en måde til at angive fremtidige behov fra en bestemt kunde. Som med (uspecificerede) prognoser bør faktiske salg forbruge det forventede behov, og det resterende antal bør indgå i behovslagerprofilen. Forbruget reducerer ikke rammeordren.

Planlægningsberegningen omfatter åbne salgsordrer, der er knyttet til den bestemte rammeordrelinje, men den tager ikke hensyn til en gyldig periode. Der tages heller ikke højde for bogførte ordrer, da bogføringsproceduren allerede har reduceret udestående rammeordreantal.

## <a name="prioritize-orders"></a><a name="prioritize-orders"></a>Prioritering af ordrer

Den ønskede eller tilgængelige dato for et bestemt varenummer repræsenterer den højeste prioritet. Behov for dags dato skal behandles inden næste uges behov. Men ud over den overordnede prioritering fremstiller planlægningssystemet følgende forslag i overensstemmelse med ordreprioriteter:

* Hvilken type behov du skal opfylde først.
* Hvilken forsyningskilde skal anvendes, før du anvender andre forsyningskilder.  

Indlæst udbud og efterspørgsel, der bidrager til en profil for den planlagte lagerbeholdning i henhold til følgende prioriteter.  

### <a name="priorities-on-the-demand-side"></a><a name="priorities-on-the-demand-side"></a>Prioriteter på efterspørgselssiden

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
> Købsreturvarer er normalt ikke involveret i forsyningsplanlægning. De skal altid være reserveret fra det lot, der skal returneres. Hvis den ikke er reserveret, spiller købsreturvarer en rolle i udbuddet og er højt prioriteret for at undgå, at planlægningssystemet foreslår en forsyningsordre, der blot skal tjene et købsreturnering.  

### <a name="priorities-on-the-supply-side"></a><a name="priorities-on-the-supply-side"></a>Prioriteter på forsyningssiden

1. Allerede på lager: Varepost (planlægningsfleksibilitet = ingen)  
2. Salgsreturvareordre (planlægningsfleksibilitet = ingen)  
3. Indgående overflytningsordre  
4. Produktionsordre  
5. Montageordre  
6. Købsordre  

### <a name="priority-related-to-the-state-of-supply-and-demand"></a><a name="priority-related-to-the-state-of-supply-and-demand"></a>Prioritet, der er relateret til tilstand af efterspørgsel og udbud

Ud over de prioriteter, der er angivet for levering og behov, er der andre ting, der påvirker planlægningsfleksibiliteten. F.eks. lageraktiviteter og status for følgende ordrer:

* Salg
* Køb
* Overførsel
* Montage
* Produktion

Status for disse ordrer har følgende effekter: 

1. Delvist håndteres (planlægningsfleksibilitet = ingen)  
2. Allerede under behandling i lageret (planlægningsfleksibilitet = ingen)  
3. Frigivet – alle ordretyper (planlægningsfleksibilitet = ubegrænset)  
4. Fastlagt og planlagt produktionsordre (planlægningsfleksibilitet = ubegrænset)  
5. Planlagt/åben – alle ordretyper (planlægningsfleksibilitet = ubegrænset)

## <a name="balancing-supply-with-demand"></a><a name="balancing-supply-with-demand"></a>Afstemning af udbud og efterspørgsel

Planlægningssystemet balancerer udbud og efterspørgsel ved at foreslå aktioner for at revidere forsyningsordrer, der ikke er afstemt. Saldoen forekommer for hver kombination af variant og lokation.  

Forestil dig, at hver lagerprofil indeholder to strenge:

* En streng af demand-hændelser sorteret efter dato og prioritet
* En tilsvarende streng af forsyningshændelser

Hver hændelse refererer til dens kildetype og identifikation. Reglerne for afstemning af varen er ligetil. Match af udbud og efterspørgsel kan ske på et hvilket som helst tidspunkt i processen:  

1. Der findes ingen behov eller forsyning for varen = > planlægning er afsluttet (eller bør ikke starte).  
2. Behov findes, men der er ingen forsyning = > forsyning bør foreslås.  
3. Forsyning findes, men der er ingen efterspørgsel for det = > forsyning bør annulleres.  
4. Både udbud og efterspørgsel eksisterer => spørgsmål bør stilles og besvares, før [!INCLUDE [prod_short](includes/prod_short.md)] kan sikre, at efterspørgslen imødekommes og forsyningen er tilstrækkelig.

    Hvis tidspunktet for forsyning ikke er egnet, kan den måske planlægges som følger:  

    1. Hvis forsyningen er placeret tidligere end behovet, kan forsyningen måske planlægges om, så lageret er så lavt som muligt.  
    2. Hvis levering er senere end behovet, kan levering måske planlægges fremad. I modsat fald foreslås ny forsyning.  
    3. Hvis forsyningen opfylder behovet på datoen, kan planlægningssystemet fortsætte med at undersøge, om forsyningsantallet kan dække behovet.  

    Når timingen er på plads, kan den passende leveringsmængde beregnes på følgende måde:  

    1. Hvis forsyningsantallet er mindre end behovet, er det muligt, at forsyningsantallet kan øges (eller ikke, hvis begrænset af en maksimummængdepolitik).  
    2. Hvis forsyningsantallet er større end behovet, er det muligt, at forsyningsantallet kan reduceres (eller ikke, hvis begrænset af en minimumsmængdepolitik).  

    På nuværende tidspunkt er en af disse to situationer aktuelle:  

    1. Det aktuelle behov kan dækkes, i hvilket tilfælde det kan lukkes, og planlægning af næste behov kan starte.  
    2. Forsyningen har nået sit maksimum og efterlader nogle i behovsantallet uafdækkede. I dette tilfælde kan planlægningssystemet lukke den aktuelle forsyning og gå videre til den næste.  

 Proceduren starter forfra med det næste behov og den aktuelle forsyning eller omvendt. Den aktuelle forsyning kan måske dække dette næste behov, eller det aktuelle behov er ikke endnu fuldt dækket.  

### <a name="rules-for-actions-for-supply-events"></a><a name="rules-for-actions-for-supply-events"></a>Regler for handlinger for forsyningshændelser

Med henblik på de top-down beregninger, hvor levering skal opfylde behovet, tages behovet som angivet. Den er uden for styringen af planlægningssystemet. Planlægningssystemet kan imidlertid administrere forsynings siden og vil fremstille følgende forslag:

* Oprette nye forsyningsordrer
* Omplanlægge eksisterende ordrer eller ændre deres antal
* Annullere forsyningsordrer, der ikke længere skal bruges  

Hvis brugeren ønsker at udelukke en eksisterende forsyningsordre fra planlægningsforslagene, han brugeren angive, at den har ingen planlægningsfleksibilitet (planlægningsfleksibilitet = ingen). Derefter bliver overskydende forsyning fra den pågældende ordre brugt til at dække behov, men der foreslås ingen handling. 

Alle forsyninger har generelt en planlægningsfleksibilitet, som er begrænset af betingelserne for hver af de foreslåede handlinger.  

* **Omplanlæg ud**: Datoen for en eksisterende forsyningsordre kan planlægges ud til at imødekomme behovets forfaldsdato, medmindre:

  * Det repræsenterer lager (altid på dag nul).  
  * Den har en ordre-til-ordre, der er knyttet til et andet behov.  
  * Den er uden for vinduet til planlægning inden for tidsintervallet.
  * Der er en forsyning tættere på, der kan anvendes.  
  * På den anden side kan brugeren beslutte at omplanlægge, fordi:
  * Forsyningsordren er allerede knyttet til et andet behov på en tidligere dato.  
  * Den nødvendige ændring i planen er så minimal, at brugeren finder den ubetydelig.  

* **Omplanlæg ind**: Datoen for en eksisterende forsyningsordre, der kan planlægges, undtagen under følgende betingelser:

  * Det er knyttet direkte til et andet behov.  
  * Den er uden for vinduet til planlægning, der er defineret af tidsintervallet.

> [!NOTE]  
> Ved planlægning af en vare ved hjælp af et genbestillingspunkt kan forsyningsordrer altid planlægges. Det sker ofte i forbindelse med forsyningsordrer, der er planlagt fremad, og som er udløst af et genbestillingspunkt.

* **Øg antal**: Antallet af en eksisterende forsyningsordre kan øges for at imødekomme behovet, medmindre forsyningsordren er knyttet direkte til et behov efter et ordre-til-ordre-link.  

> [!NOTE]  
> Selvom det er muligt at øge forsyningsordren, kan det være begrænset på grund af et defineret maksimalt ordreantal.  

* **Reducer antal**: En eksisterende forsyningsordre med et overskud sammenlignet med et eksisterende behov kan reduceres for at opfylde behovet.  

> [!NOTE]  
> Selvom antallet kan blive reduceret, kan der stadig være overskud, sammenlignet med behovet, på grund af et defineret minimumsordreantal eller en oprundingsfaktor. 

* **Annuller**: Som et særligt tilfælde af handlingen, der reducerer antallet, kan forsyningsordren blive annulleret, hvis den er reduceret til nul. 
* **Ny**: Hvis der ikke allerede findes en forsyningsordre, eller en eksisterende ikke kan ændres for at opfylde det nødvendige antal på den efterspurgte forfaldsdato, foreslås der en ny forsyningsordre.  

### <a name="determine-the-supply-quantity"></a><a name="determine-the-supply-quantity"></a>Bestemmelse af forsyningsantallet

Definer planlægningsparametre, der styrer det foreslåede antal af hver forsyningsordre.  

Når planlægningssystemet beregner antallet af en ny forsyningsordre eller ændring af antallet på en eksisterende, kan det foreslåede antal være forskelligt fra det, der faktisk kræves.  

Hvis en maksimal lager- eller fast ordremængde er valgt, kan det foreslåede antal øges for at opfylde det faste antal eller det maksimale lagerniveau. Hvis genbestillingsmetoden bruger et genbestillingspunkt, kan antallet forhøjes for i det mindste at opfylde genbestillingspunktet. 

Det foreslåede antal kan ændres i denne rækkefølge:  

1. Ned til det højst tilladte ordreantal.  
2. Op til det mindste ordreantal.  
3. Op til at opfylde den nærmeste oprundingsfaktor.

### <a name="order-tracking-links-during-planning"></a><a name="order-tracking-links-during-planning"></a>Ordresporingsbindinger under planlægning

Med hensyn til ordresporing under planlægning, er det vigtigt at nævne, at planlægningssystemet omarrangerer de dynamisk oprettede ordresporingsbindinger til vare-/variant-/lokationskombinationerne. Systemet omarrangerer sporingslinks af følgende årsager:

* At kontrollere forslagene til dækning af alle behov, og sørg for, at alle forsyningsordrer er nødvendige.  
* Ordresporingsbindingerne skal balancere regelmæssigt.  

Ordresporingsbindinger bliver efter tiden afstemt. I tidens løb bliver dynamiske ordresporingsbindinger uafstemte, fordi det samlede ordresporingsnetværk ikke omarrangeres, før en behovs- eller forsyningshændelse faktisk er lukket.

Før udligning af forsyning med behov, sletter planlægningssystemet alle ordresporingsbindinger. Under den udlignende procedure, når en behovs- eller forsyningshændelse er lukket, etablerer det derefter nye ordresporingsbindinger mellem udbud og efterspørgsel.  

> [!NOTE]  
> Selvom varen ikke er konfigureret til dynamisk ordresporing, opretter planlægningssystemet afstemte ordresporingsbindinger, som forklaret ovenfor.

## <a name="close-balanced-supply-and-demand"></a><a name="close-balanced-supply-and-demand"></a>Luk afstemte udbud og efterspørgsel

Den balancerende leverance har tre mulige udfald:

* Det påkrævede antal og den påkrævede dato for behovhændelserne er opfyldt, og planlægning af dem kan lukkes. Forsyningshændelsen forbliver åben og kan muligvis dække det næste behov. Derfor lukkes den aktuelle forsyning, så den udlignende handling kan starte forfra med det aktuelle forsyningsbehov og den næste efterspørgsel.  
* Forsyningsordren kan ikke ændres, så den dækker alle behov. Behovshændelsen er stadig åben, med nogle udækkede antal, der kan dækkes ved næste forsyningshændelse. Derfor lukkes den aktuelle forsyning, så den udlignende handling kan starte forfra med det aktuelle behov og den næste forsyningshændelse.  
* Alle behov er blevet dækket, og der er ingen efterfølgende behov (eller der har ikke været nogen behov overhovedet). Overskydende forsyning kan reduceres (eller annulleres) og derefter lukkes. Også andre forsyningshændelser skal annulleres.  

Endelig opretter planlægningssystemet et ordresporingslink mellem forsyning og behov.  

### <a name="create-the-planning-line-suggested-action"></a><a name="create-the-planning-line-suggested-action"></a>Oprettelse af planlægningslinjen (foreslået aktivitet)

Hvis en handling **Ny**, **Ret antal**, **Omplanlæg**, **Omplanlæg og Ret antal** eller **Annuller** foreslås for at revidere forsyningsordren, vil planlægningssystemet oprette en planlægningslinje i planlægningskladden. I forbindelse med ordresporing oprettes planlægningslinjen ikke kun, når forsyningshændelsen lukkes, men også hvis behovshændelsen lukkes. Dette gælder også, selvom forsyningshændelsen stadig er åben og kan ændres, når den næste behovshændelse behandles. Planlægningslinjen kan ændres, når den er oprettet.

For at reducere belastningen af databasen, når der håndteres produktionsordrer, kan planlægningslinjen vedligeholdes på tre niveauer:

* Opret kun planlægningslinjen med den aktuelle forfaldsdato og antallet, men uden rute og komponenter.  
* Omfatter rute: Den planlagte rute omfatter beregning af start- og slutdatoer og -tidspunkter. Omfatter routing er påkrævet i forbindelse med adgang til databasen. For at bestemme slutdato og forfaldsdatoer kan det være nødvendigt at beregne routing, selvom forsyningshændelsen ikke er blevet lukket. Hvis du f. eks. foretager forlæns planlægning.  
* Omfatter styklisteudfoldelsen: Dette kan vente indtil lige før leveringshændelsen er lukket.

## <a name="see-also"></a><a name="see-also"></a>Se også

[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
