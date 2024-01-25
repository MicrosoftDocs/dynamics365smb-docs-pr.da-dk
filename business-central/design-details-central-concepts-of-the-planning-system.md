---
title: Designoplysninger for centrale begreber i planlægningssystemet
description: 'Planlægning foreslår mulige handlinger, som brugeren kan udføre på baggrund af behovs-/leverings situationen og varens planlægningsparametre.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
---
# Designoplysninger: Centrale begreber i planlægningssystemet

Planlægningsfunktionerne er indeholdt i en kørsel, der først vælger de relevante varer og den relevante periode, der skal planlægges. Derefter kalder kørslen en kodeenhed, der beregner en forsyningsplan, i overensstemmelse med hver vares laveste-niveau-kode (styklisteposition). Kodeenheden balancerer sæt af leveringsbehov og foreslår handlinger, som brugeren skal udføre. De foreslåede handlinger vises som linjer i planlægningskladden eller indkøbskladden.  

![Indhold på siden Planlægningskladdeside.](media/design_details_central_concepts_of_the_planning_system_planning_worksheets.png "Indhold på siden Planlægningskladdeside")  

Planlæggeren i en virksomhed, f.eks. en indkøber eller produktionsplanlægger, formodes at være brugeren af planlægningssystemet. Planlægningssystemet hjælper brugeren ved at udføre omfattende, men temmeligt enkle beregninger af en plan. Brugeren kan derefter koncentrere sig om at løse mere komplekse problemer, f.eks. når ting er anderledes. end de plejer.  

Planlægningssystemet styres af forventet og faktiskt kundebehov, f.eks. prognoser og salgsordrer. Planlægningsberegninger foreslår handlinger, du kan udføre i forbindelse med levering af leverandører, montage eller produktion eller overførsler fra andre lagre. Eksempel på foreslået handling kunne være at oprette nye forsyningsordrer, som f.eks. købs- eller produktionsordrer. Hvis der allerede findes forsyningsordrer, kan den foreslåede aktivitet f.eks. være at øge eller fremskynde ordrerne for på den måde at imødekomme det ændrede behov.  

Et andet formål med planlægningssystemet er at sikre, at lagerbeholdningen ikke vokser unødvendigt. Hvis behovet falder, kan planlægningssystemet foreslå, at brugeren udskyder eksisterende forsyningsordrer, angiver mindre antal til dem eller helt annullerer dem.  

En kodeenhed indeholder planlægningslogikken og følgende funktioner:

* MRP og MPS
* Beregn nettoplan
* Beregn totalplan

Beregningen af forsyningsplan omfatter dog forskellige undersystemer.  

Planlægningssystemet har ingen dedikeret logik for kapacitetsudjævning eller finplanlægning. De forskellige typer planlægningsarbejde udføres separat. Manglende direkte integration mellem de to områder betyder også, at væsentlige ændringer af kapacitet eller tidsplan kræver, at planlægning gentages.  

## Planlægningsparametre

Planlægningsparametre, som brugeren angiver for en vare eller en gruppe af varer, styrer hvilke handlinger planlægningssystemet foreslår i forskellige situationer. Planlægningsparametrene defineres på hvert enkelt varekort, for at styre hvornår, hvor meget og hvordan du genbestiller.  

Planlægningsparametre kan også være defineret for en kombination af vare, variant og lokation ved at oprette en lagervare for hver kombination, der er nødvendig, og derefter angive individuelle parametre. Du kan finde flere oplysninger i [Designoplysninger - Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) og [Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md).  

## Planlægningsstartdato

Planlægningssystemet hjælper dig med at undgå tidligere åbne ordrer og foreslåede handlinger, der ikke er mulige. Ved planlægning behandles alle datoer før startdato som en fastfrosset zone. Følgende regel gælder for den frosne zone:  

* Alle forsyninger og behov før startdatoen for planlægningsperioden vil blive betragtet som en del af lagerbeholdningen eller leveret. Med andre ord antages det, at planen for fortiden er udført i overensstemmelse med den givne plan. Flere oplysninger i [Håndtering af ordrer før planlægningsstartdatoen](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).  

## Dynamisk ordresporing (udligning)

Dynamisk ordresporing med samtidig oprettelse af aktionsmeddelelser i planlægningskladden er ikke en del af forsyningsplanlægningssystemet. Denne funktion sammenkæder, behovet og det antal, der kan dække det, i realtid, hver gang et nyt behov eller en ny forsyning oprettes eller ændres.  

Hvis brugeren f.eks. indtaster eller ændrer en salgsordre, vil det dynamiske ordresporingssystem søge efter en relevant forsyning, der kan dække behovet. Forsyningen kan være fra lagerbeholdning eller fra en forventet forsyningsordre (f.eks. en købsordre eller en produktionsordre). Når der bliver fundet en forsyningskilde, knyttes [!INCLUDE [prod_short](includes/prod_short.md)] behovet til tilbuddet. Du får adgang til hyperlinket på Vis sider fra dokumentlinjerne. Når der ikke bliver fundet tilstrækkelige forsyninger, opretter det dynamiske ordresporingssystem aktionsmeddelelser i planlægningskladden med forslag til forsyningsplanlægning.  

Dynamisk ordresporing hjælper dig med at vurdere, om der skal accepteres leveringsordreforslag. Fra forsyningssiden vises det behov, der oprettede leveringen. Fra forsyningssiden vises den forsyning, der oprettede leveringen.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking.png" alt-text="Eksempel på dynamisk ordresporing.":::

Flere oplysninger i [Designoplysninger: Reservation, ordresporing og aktionsmeddelelser](design-details-reservation-order-tracking-and-action-messaging.md).  

I virksomheder med en lav varestrøm og mindre avancerede produktstrukturer kan det være tilstrækkeligt at bruge dynamisk ordresporing som det vigtigste middel til forsyningsplanlægning. I travle miljøer bør planlægningssystemet dog bruges til altid at sikre en korrekt afstemt forsyningsplan.  

### Dynamisk ordresporing kontra planlægningssystemet

Ved første øjekast kan det være svært at skelne mellem planlægningssystemet og dynamisk ordresporing. Begge funktioner viser afgang i planlægningskladden ved at foreslå handlinger, som planlæggeren skal udføre. Dog afviger den måde, dette output er produceret.  

Planlægningssystemet vedrører hele udbud og efterspørgselsmønsteret for en vare. Den betragter alle niveauer i styklistehierarkiet langs tidslinjen. Dynamisk ordresporing løser kun situationen i den ordre, der aktiverede den. Når udbud og efterspørgsel bestemmes, opretter planlægningssystemet links i en brugeraktiveret batchtilstand. Dynamisk ordresporing opretter automatisk kæderne, når du angiver udbud og efterspørgsel. Når du f. eks. opretter en salgs- eller købsordre.  

Dynamisk ordresporing etablerer forbindelser mellem behov og forsyning, når der indtastes data, på grundlag af først til mølle-princippet. Dette kan føre til nogen uorden i prioriteter. En salgsordre, der er angivet først med forfaldsdato næste måned, kan f. eks. være knyttet til leveringen på lageret. Den næste salgsordre forfalder i morgen, men der kan opstå en aktionsmeddelelse til at oprette en ny købsordre for at dække den. Følgende billede viser dette scenarie.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking_graph.png" alt-text="Eksempel på ordresporing i forsyningsplanlægning 1.":::

Planlægningssystemet kan håndtere behov og levering af varer i en prioriteret ordre. Ordren prioriteres i overensstemmelse med forfaldsdatoer og ordretyper. Dvs. efter forbrugs-først-mølle-princippet. Den sletter alle ordresporingslinks, der er oprettet dynamisk, og genopretter dem i overensstemmelse med prioritet af forfaldsdato. Når planlægningssystemet er kørt, har det løst alle ubalancer mellem behov og forsyning, som vist nedenfor, for de samme data.

:::image type="content" source="media/nav_app_supply_planning_1_planning_graph.png" alt-text="Eksempel på ordresporing i forsyningsplanlægning 2.":::  

Når du har kørt planlægningen, indeholder tabellen Aktionsmeddelelsespost ikke nogen aktionsmeddelelser. Disse meddelelser erstattes af de handlinger, der er foreslået i planlægningskladden. Flere oplysninger i [Ordresporingsbindinger under planlægning](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).  

## Rækkefølge og prioritet i planlægningen

Når du opretter en plan, er rækkefølgen af beregningerne vigtig for at få arbejdet gjort inden for en rimelig tidsramme. Desuden spiller prioriteringen af krav og ressourcer en vigtig rolle for at opnå de bedste resultater.  

Planlægningssystemet er behovstyret. Varer med højt niveau bør planlægges før varer med lavt niveau, fordi de kan generere yderligere behov for varerne på lavere niveau. Det betyder for eksempel, at detaillokationer bør planlægges før distributionscentre planlægges, fordi planen for en retaillokation kan omfatte yderligere behov fra distributionscentret. På en nærmere afvejning betyder dette også, at en salgsordre kan dække en salgsordre kan systemet ikke oprette en ny forsyningsordre. Desuden må en forsyning med et bestemt lotnummer ikke allokeres for at dække et generisk behov, hvis et andet behov kræver denne specifikke lot.  

### Vareprioritet/laveste-niveau-kode

I et produktionsmiljø medfører behovet for en færdig salgbar vare afledte behov for komponenter, der udgør den færdige vare. Styklistestrukturen styrer komponentstrukturen og kan omfatte flere niveauer af halvfabrikata. Planlægning af en vare på ét niveau vil medføre afledte behov for komponenter på næste niveau. Dette hierarki kan eventuelt resultere i afledte behov for købte varer. Planlægningssystemet planlægger varer i den bestilte rækkefølge i det samlede skyklistehierarki. Systemet starter med færdige salgbare elementer på det øverste niveau og fortsætter produktstrukturen til de lavere niveauer (i overensstemmelse med laveste-niveau-koden).  

Billedet nedenfor viser den rækkefølge, som [!INCLUDE [prod_short](includes/prod_short.md)] foreslå forsyningsordrer på øverste niveau. Det antages, at forslagene er accepteret og viser også varer på lavere niveauer.

:::image type="content" source="media/nav_app_supply_planning_1_bom_planning.png" alt-text="Planlægning af styklister.":::

Du kan finde flere oplysninger om overvejelser i forbindelse med produktion i [Indlæsning af lagerprofiler](design-details-balancing-demand-and-supply.md#load-inventory-profiles).  

#### Optimere ydeevnen for beregninger med lavt niveau

Beregninger af laveste-niveau-kode kan påvirke systemets ydeevne. Du kan mindske virkningen ved at deaktivere **Beregningen af dynamisk laveste-niveau-kode** på siden **Produktionsopsætning**. Når du gør det, foreslår [!INCLUDE[prod_short](includes/prod_short.md)], at du opretter en tilbagevendende opgavekøpost, der opdaterer laveste-niveau-koder dagligt. Du kan sikre dig, at jobbet køres uden for arbejdstiden ved at angive et starttidspunkt for feltet **Tidligste startdato/klokkeslæt**.

Du kan også aktivere logik, som øger hastigheden på laveste-niveau-kode, ved at vælge **Optimer beregning af laveste niveau-kode** på siden **Produktionsopsætning**.

> [!IMPORTANT]
> Hvis du vælger at optimere ydeevnen, bruges [!INCLUDE[prod_short](includes/prod_short.md)] der nye beregningsmetoder til beregning af laveste-niveau-koder. Hvis du har et filtypenavn, der er afhængigt af de hændelser, der bruges i de gamle beregninger, fungerer udvidelsen måske ikke.

### Lokationer / prioritet af overførselsniveau

Virksomheder, der gør forretning på mere end én lokation, kan være nødt til at planlægge individuelt for hver lokation. En vares sikkerhedslagerniveau og dens genbestillingsmetode kan f.eks. variere fra én lokation til en anden. Du skal angive planlægningsparametrene pr. vare og lokation.  

Du kan bruge lagervarer til at angive individuelle planlægningsparametre. En lagervare kan betragtes som en vare på en bestemt placering. Hvis du ikke har angivet en lagervare for denne lokation, bruger [!INCLUDE [prod_short](includes/prod_short.md)] de parametre, der er angivet på varekortet. [!INCLUDE [prod_short](includes/prod_short.md)] beregner kun en plan for aktive lokationer, som er der, hvor der er eksisterende behov eller forsyning for den pågældende vare.  

Et element kan håndteres på enhver lokation i princippet, men [!INCLUDE [prod_short](includes/prod_short.md)] har tilgang til begrebet lokation er meget streng. En salgsordre på ét sted kan f.eks. ikke opfyldes af et antal på lager på en anden lokation. Antal på lager skal først overflyttes til den lokation, der er angivet på salgsordren.

:::image type="content" source="media/nav_app_supply_planning_1_sku_planning.png" alt-text="Planlægning af lagervarer pr. lokation.":::

Flere oplysninger i [Designoplysninger: Overførsler i planlægning](design-details-transfers-in-planning.md).  

### Prioritering for ordrer

Inden for en given SKU repræsenterer den anmodede eller tilgængelige dato den højeste prioritet. Behovene i dag skal behandles før behovene for de kommende dage. Men bortset fra denne slags prioritet sorteres de forskellige behov og forsyningstyper efter forretningsmæssig vigtighed for at beslutte, hvilke behov der skal opfyldes først. På forsyningssiden angiver ordrens prioritet den forsyningskilde, der skal udlignes først. Få mere at vide om [Prioritering af ordrer](design-details-balancing-demand-and-supply.md#prioritize-orders).  

## Behovsprognoser og rammeordrer

Forecasts og rammesalgsordrer repræsenterer begge forventet behov. Den rammeordre, som dækker en kundes tiltænkte køb over en bestemt tidsperiode, skal mindske usikkerheden af den samlede prognose. Rammeordren er en debitorspecifik prognose i tillæg til den uspecificerede prognose, som vist i følgende billede.  

:::image type="content" source="media/nav_app_supply_planning_1_forecast_and_blanket.png" alt-text="Planlægning ved hjælp af prognoser.":::

Flere oplysninger i [Forecastbehov reduceres af salgsordrer](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## Planlægningsopgave

Alle varer skal planlægges igen, når behovet for behov eller leveringstiden er ændret siden den seneste beregning af planen. Hvis du f.eks. angiver en ny salgsordre eller ændrer en eksisterende, er der grund til at genberegne planen. Andre årsager til genberegning omfatter en ændring i budgettet eller den ønskede mængde sikkerhedslager. Ændring af en stykliste ved at tilføje eller fjerne en komponent ville sandsynligvis angive en ændring, men kun for komponentvaren.  

Planlægningssystemet overvåger sådanne hændelser og tildeler de relevante varer til planlægning.  

For flere lokationer finder tildelingen sted på niveauet for vare pr. lokationskombination. Hvis en salgsordre f.eks. er blevet oprettet på kun én lokation, bliver [!INCLUDE [prod_short](includes/prod_short.md)] tildelt på den pågældende lokation til planlægning.  

Årsagen til at vælge varer til planlægning er et spørgsmål om systemets ydeevne. Hvis der ikke er opstået nogen ændring af en vares behovforsyningsmønster, foreslår planlægningssystemet ikke nogen handlinger, der skal udføres. Uden planlægningsopgave ville systemet skulle udføre beregningerne for alle varer for at finde ud af, hvad der skal planlægges. Den komplette liste over grunde til at tildele en vare i planlægning kan du finde i [Designoplysninger: Tabellen Planlægningsopgave](design-details-planning-assignment-table.md).  

Følgende beskriver de tilgængelige indstillinger:  

* **Beregn totalplan** beregner alle valgte varer, uanset om det er nødvendigt eller ej.  
* **Beregn nettoplan** beregner kun de valgte varer, hvor der er foretaget ændringer i behov- og forsyningsmønstre, og som derfor er blevet tildelt planlægning.  

Nogle brugere mener, at nettoplanlægning skal udføres i farten, f.eks. når salgsordrer angives. Men det kan være forvirrende, fordi dynamisk ordresporing og aktionsmeddelelser også beregnes løbende. [!INCLUDE[prod_short](includes/prod_short.md)] giver mulighed for klar kontrol i realtid. Det giver pop op-advarsler, når du angiver salgsordrer, og den aktuelle forsyningsplan ikke kan opfylde behovet.  

Udover disse overvejelser planlægger planlægningssystemet kun for de varer, som brugeren har udarbejdet med passende planlægningsparametre. I modsat fald antages det, at brugeren kommer til at planlægge varer halvautomatisk eller manuelt ved hjælp af funktionen Ordreplanlægning. Du kan finde flere oplysninger om de automatiske planlægningsprocedurer i [Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md).  

## Varedimensioner

Behov og forsyning kan have variantkoder og lokationskoder, der skal overholdes, når planlægningssystemet afstemmer behov og forsyning.  

[!INCLUDE [prod_short](includes/prod_short.md)] behandler variant- og lokationskoder som varedimensioner på en salgsordrelinje, lagerpost osv. Derfor beregnes der en plan for hver kombination af variant og lokation, som om kombinationen var et separat varenummer.  

I stedet for beregning af en teoretisk kombination af variant og lokation beregner [!INCLUDE [prod_short](includes/prod_short.md)] kun de kombinationer, der faktisk findes i databasen. Du kan finde flere oplysninger om, hvordan planlægningssystemet håndterer lokationskoder efter behov, i [Designoplysninger: Behov på tom lokation](design-details-balancing-demand-and-supply.md).  

## Vareattributter

Varer har ofte generelle attributter, f. eks. varenummer, variantkode, lokationskode og ordretype. Hver efterspørgsels- og leveringshændelse kan imidlertid have andre specifikationer, f. eks. serienumre eller lotnumre. Planlægningssystemet planlægger disse attributter på bestemte måder, afhængigt af deres specifikationsniveau.  

Et ordre-til-ordre-link mellem behov og forsyning er en anden type attribut, der har indflydelse på planlægningssystemet. Flere oplysninger i [Ordre-til-ordre-links](#order-to-order-links).

### Specifikke attributter

Nogle behovsattributter er specifikke, og en levering skal nøjagtigt svare til dem.

* Påkrævede serienumre/lotnumre, der kræver et bestemt program (Disse attributter kræves, hvis du markerer afkrydsningsfeltet **Serienr.specifik sporing** eller **Lotspecifik sporing** på siden **Varesporingskodekort** for den varesporingskode, der bruges af varen.)  
* Links til forsyningsordrer, der er oprettet manuelt eller automatisk for et bestemt behov (ordre-til-ordre-links).  

Planlægningssystemet anvender følgende regler for disse attributter:  

* Behov med specifikke attributter kan kun opfyldes ved forsyning med tilsvarende attributter.  
* Forsyning med særlige attributter kan også opfylde behovet, der ikke anmoder specifikt om disse attributter.  

Hvis lagerbeholdningen eller de forventede forsyninger, foreslår planlægningssystemet derfor en ny forsyningsordre uden hensyntagen til planlægningsparametre.  

### Ikke-specifikke attributter

Varer med serie- eller lotnumre uden en bestemt vare sporings opsætning kan have ikke-specifikke serie- eller lotnumre. Disse typer numre kan anvendes på serienumre eller lotnumre. Dette giver planlægningssystemet mere frihed til at afstemme f.eks. et behov med serienummer med en forsyning med serienummer, typisk på lageret.  

Behov-forsyning med serie- eller lotnumre, specifikke eller ikke-specifikke er vigtige og er undtaget fra den frosne zone. De vil være en del af planlægningen, selvom de forfalder før planlægningens startdato. Hvis du ønsker yderligere oplysninger, kan du se afsnittet [Serienumre/lotnumre indlæses efter specifikationsniveau](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).

Hvis du ønsker yderligere oplysninger om, hvordan planlægningssystemet afstemmer attributter, kan du se [Serienumre/lotnumre og ordre-til-ordre-links er fritaget fra den tidligere periode](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period).  

## Ordre-til-ordre-links

Ordre-til-ordre betyder, at du køber, samler eller fremstiller en vare til et bestemt behov. Der er flere grunde til at vælge denne politik:

* Behovet er ikke hyppigere.
* Leveringstiden er ikke betydelig.
* De krævede attributter varierer.  

Et andet tilfælde, der bruger ordre-til-ordre-links er, når en montageordre linkes til en salgsordre i et montage til ordre-scenario.  

Ordre-til-ordre-links anvendes mellem efterspørgsel og udbud på fire måder:  

* Når den planlagte vare bruger genbestillingsmetoden **Ordre**  
* Når produktionsmetoden Fremstil-til-ordre bruges til at oprette produktionsordrer med flere niveauer eller produktionsordrer af projekttype (fremstilling af nødvendige komponenter på den samme produktionsordre)  
* Ved oprettelse af produktionsordrer for salgsordrer med funktionen Salgsordreplanlægning  
* Når du samler en vare til en salgsordre (**montagepolitik** er indstillet til **montage efter ordre**)  

I disse tilfælde foreslår planlægningssystemet kun at bestille den ønskede mængde. Når den er oprettet, vil indkøbs-, produktions- eller montageordren matche det tilsvarende behov. Hvis en salgsordre f.eks. ændres i tid eller antal, foreslår planlægningssystemet, at den tilsvarende forsyningsordre ændres i overensstemmelse hermed.  

Når der findes ordre-til-ordre-links, medtager planlægningssystemet ikke tilknyttet forsyning eller lagerbeholdning i udligningsproceduren. Planlæggerne kan bestemme, om du vil bruge den tilknyttede levering eller et nyt behov. I sidstnævnte tilfælde kan de slette forsyningsordren eller reservere den tilknyttede levering manuelt.  

Reservationer og ordresporingslinks brydes, hvis en sådan situation bliver umulig. F.eks. når du flytter behovet til en dato, der ligger før levering. Ordre-til-ordre-links kan tilpasses ændringer i behov eller forsyning og aldrig bryde.  

## Reservationer

Planlægningssystemet medtager ikke nogen reserverede mængder i beregninger. Hvis et antal for en salgsordre f. eks. er helt eller delvist reserveret, kan du ikke bruge antallet til dækning af andet behov.

Planlægningssystemet medtager ikke nogen reserverede mængder i planlagt beholdningsprofil. Den skal overveje alle mængder for at bestemme, hvornår genbestillingspunktet er overskredet, og hvor mange der skal genbestilles for at nå det maksimale lagerniveau. Unødvendige reservationer kan føre til øget risiko for, at lagerniveauer bliver lave, fordi logikken i planlægningen ikke registrerer de reserverede antal.  

Følgende billede viser, hvordan reservationer kan hæmme planlægning.  

:::image type="content" source="media/nav_app_supply_planning_1_reservations.png" alt-text="Planlægning ved hjælp af reservationer.":::

Flere oplysninger i [Designoplysninger: Reservation, ordresporing og aktionsmeddelelser](design-details-reservation-order-tracking-and-action-messaging.md).  

## Advarsler

Den første kolonne i planlægningsarket for advarselsfelterne. Der vises et advarselsikon, når du opretter en planlægningslinje til en usædvanlig situation.  

Efterspørgsel på planlægningslinjer med advarsler modificeres normalt ikke i henhold til planlægningsparametre. Planlægningssystemet foreslår i stedet for kun en forsyning til at dække det nøjagtige behov. Systemet kan dog konfigureres til at overholde planlægningsparametre for planlægningslinjer med visse advarsler. Advarselsoplysningerne vises af siden **Ikke-sporede planlægningselementer**, som også bruges til at vise ordresporingsbindinger for ikke-ordrerelaterede netværksenheder. Der findes tre typer advarsler:  

* Nødsituation  
* Undtagelse  
* Bemærk  

:::image type="content" source="media/nav_app_supply_planning_1_warnings.png" alt-text="Advarsler i planlægningskladden.":::

### Nødsituation

Denne advarsel vises i to situationer:  

* Når lageret er negativt på den planlagte startdato  
* Når der er antedaterede forsyning- eller behovshændelser  

Hvis varens lager er negativt på den planlagte startdato, foreslås der en nødforsyning for den negative mængde, som skal ankomme på den planlagte startdato. Advarslen angiver startdatoen og mængden for nødordren. Flere oplysninger i [Håndtering af forventet negativt lager](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Dokumentlinjer med forfaldsdatoer før den planlagte startdato konsolideres i én nødforsyningsordre. Ordren er planlagt til at ankomme på den planlagte startdato.  

### Undtagelse

Advarslen om undtagelsen vises, hvis det forventede disponible lager kommer under sikkerhedslageret. Planlægningssystemet foreslår en forsyningsordre, der skal opfylde behovet på forfaldsdatoen. Advarslen angiver varemængden på sikkerhedslageret og den dato, hvor den overtrædes.  

Overskridelse af niveauet for sikkerhedslageret er en undtagelse. Det sker ikke, hvis genbestillingspunktet er angivet korrekt. Du kan finde flere oplysninger i [Genbestillingspunktets rolle](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Undtagelsesordreforslag hjælper med at sikre, at den planlagte disponible beholdning aldrig er lavere end niveauet for sikkerhedslageret. Det foreslåede antal dækker lige akkurat sikkerhedslageret uden at tage hensyn til planlægningsparametrene. Men i nogle eksempler tages der hensyn til ordremodifikatorer.  

> [!NOTE]  
> Planlægningssystemet har måske tilsigtet forbrugt sikkerhedslageret og vil derefter genopfylde det med det samme. Få mere at vide om [Forbrug af sikkerhedslager](design-details-balancing-demand-and-supply.md#consume-safety-stock).

### Bemærk

Denne advarsel vises i tre tilfælde:  

* Når den planlagte startdato ligger før arbejdsdatoen.  
* Når planlægningslinjen foreslår ændring af en en frigivet købs- eller produktionsordre.  
* Den planlagte beholdning overskrider overløbsniveauet på forfaldsdatoen. Flere oplysninger i [Forbliv under overløbsniveauet](design-details-handling-reordering-policies.md#stay-below-the-overflow-level).  

> [!NOTE]  
> På planlægningslinjer med advarsler er feltet **Accepter aktionsmeddelelse** ikke markeret, fordi planlæggeren forventes at undersøge disse linjer nærmere, før planen udføres.  

## Fejllogfiler

Brugeren kan vælge feltet **Stop, og vis første fejl** på **beregningsplanens** anmodningsside for at stoppe planlægningskørslen, når der opstår fejl. Der vises en meddelelse med oplysninger om fejlen. Hvis der er fejl, vises kun de fejlfri planlægningslinjer i planlægningskladden, som blev oprettet, inden fejlen opstod.  

Hvis feltet ikke er markeret, fortsætter kørslen **Beregn Plan**, indtil den er færdig. Fejl afbryder ikke batchjobbet. Hvis der er fejl, angiver en meddelelse, hvor mange elementer der blev berørt. Siden **Log over planlægningsfejl** åbnes med flere oplysninger om fejlen og indeholder links til det eller de berørte dokumenter eller opsætningskort.  

:::image type="content" source="media/nav_app_supply_planning_1_error_log.png" alt-text="Fejlmeddelelser i planlægningskladden.":::

## Planlægningsfleksibilitet

Det er ikke altid praktisk at planlægge en eksisterende forsyningsordre. Når produktionen f. eks. er startet, eller du ansætter ekstra personer på en bestemt dag for at udføre opgaven. Med henblik på at angive om en eksisterende ordre kan ændres af planlægningssystemet, har alle forsyningsordrelinjer et **planlægningsfleksibilitetsfelt** med to indstillinger: **Ubegrænset** eller **Ingen**. Hvis feltet er angivet til **Ingen**, vil planlægningssystemet ikke forsøge at ændre forsyningsordrelinjen.  

Feltet kan manuelt indstilles af brugeren, men i nogle tilfælde angives det automatisk af [!INCLUDE [prod_short](includes/prod_short.md)]. Den omstændighed, at planlægningsfleksibiliteten kan angives manuelt af brugeren, er vigtig, fordi den gør det nemt at tilpasse brugen af funktionen til forskellige arbejdsgange og forretningssituationer. Du kan finde flere oplysninger om, hvordan dette felt bruges, i [Designoplysninger: Overførsler i planlægning](design-details-transfers-in-planning.md).  

## Ordreplanlægning

Basisforsyningens planlægningsværktøj, der er repræsenteret af siden **Ordreplanlægning**, er designet til manuel beslutningstagning. Den tager ikke højde for nogen planlægningsparametre og er derfor ikke beskrevet yderligere i denne artikel. Du kan finde flere oplysninger i [Planlægning af ny behovsordre efter ordre](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
> Det anbefales ikke at bruge ordreplanlægning, hvis firmaet anvender allerede planlægning eller indkøbskladder. Forsyningsordrer, der er oprettet via siden **Ordreplanlægning**, kan ændres eller slettes under de automatiske planlægningskørsler. Disse ændringer sker, fordi den automatiske planlægningskørsel bruger planlægningsparametre, og disse parametre kan muligvis ikke tages i betragtning af den bruger, der oprettede den manuelle plan af siden Ordreplanlægning.  

## Begrænset belastning

[!INCLUDE[prod_short](includes/prod_short.md)] giver en grov planlægning for planlægning af en rimelig brug af ressourcer. Den opretter og vedligeholder ikke automatisk detaljerede planer på baggrund af prioriteter eller optimeringsregler.  

Den forventede brug af ressourcefunktionen for kapacitetsbegrænsning er følgende:

* Sådan undgås overbelastning af ressourcer
* Sådan sikres det, at kapaciteten ikke er blevet ikke tilbage allokeret, hvis den kan reducere tiden for en produktionsordre

Ved planlægning med kapacitetsbegrænsede ressourcer sikrer [!INCLUDE [prod_short](includes/prod_short.md)], at der ikke indlæses nogen ressource over dens definerede kapacitet (kritisk belastning). Det tildeler hver operation til det nærmeste tilgængelige tidsrum. Hvis tidsrummet ikke er stort nok til at fuldføre hele handlingen, bliver handlingen opdelt i to eller flere dele, der er placeret i de nærmeste ledige tidsrum.  

> [!NOTE]  
> I tilfælde af opdeling af operationen er opstillingstiden kun tildelt én gang, da det antages, at nogen manuel regulering er udført for at optimere planen.  

Du kan tilføje aktionsgrænse for tid kan føjes til ressourcer for at minimere opdeling af funktionen. Denne tid lader [!INCLUDE [prod_short](includes/prod_short.md)] planlægge belastningen den sidste mulige dag ved at overskride den kritiske belastningsprocent en smule.  

## Se også

[Designoplysninger: Overførsler i planlægning](design-details-transfers-in-planning.md)  
[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)  
[Designoplysninger: Tabellen Planlægningsopgave](design-details-planning-assignment-table.md)  
[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)  
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
