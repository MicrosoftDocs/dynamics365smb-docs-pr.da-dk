---
title: 'Sælge, montere og levere pakker'
description: 'For at støtte en for JIT-lagerstrategi kan montageordrer automatisk oprettes og tilknyttes, så snart salgsordrelinjen er oprettet.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-selling-assembling-and-shipping-kits" />Gennemgang: Salg, montering og levering af pakker

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

For at støtte en for JIT-lagerstrategi og muligheden for at tilpasse produkter til debitorkrav, kan montageordrer automatisk oprettes og tilknyttes, så snart salgsordrelinjen er oprettet. Kæden mellem salgsbehov og montagelevering giver salgsordrebehandlere mulighed for at tilpasse montageelementet automatisk og love leveringsdatoer i henhold til komponentens tilgængelighed. Desuden bogføres montageforbrug og afgang automatisk med leverancen af den tilknyttede salgsordre.  

Der findes specielle funktioner til at dække levering af montage til ordre-mængder, både i grundlæggende og avancerede lagerkonfigurationer. Når medarbejdere, der er ansvarlige for montering, afslutter monteringsdele eller montage til ordre-mængde, registrerer de det i feltet **Levér antal** på lagerleverancelinjen i avancerede konfigurationer og vælger **Bogfør lev.**. Resultatet er, at den tilsvarende montageafgang bogføres, herunder det relaterede komponentforbrug, og en salgsleverance for mængden bogføres for den tilknyttede salgsordre. Denne gennemgang viser processen for det avancerede lager.  

I grundlæggende lagerkonfigurationer bogfører den ansvarlige lagermedarbejder et lagerpluk for salgsordrelinjerne, når en montage til ordre-mængde er klar til at blive leveret. Derefter oprettes en flytning (lager) for komponenterne, og montageoutputtet og salgsordreleverancen bogføres. Du kan finde flere oplysninger i [Håndtere montageordrevarer i Pluk (lager)](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).  

## <a name="about-this-walkthrough" />Om denne gennemgang

Denne gennemgang viser følgende opgaver:  

### <a name="setting-up-assembly-items" />Konfigurere montageelementer

Montageelementer er kendetegnet ved deres genbestillingssystem og montagestyklisten. Varens montagepolitik kan enten være montage til ordre (ATO) eller montage til lager (ATS). Dette afsnit dækker følgende opgaver:  

-   Angive det relevante genbestillingssystem og den relevante montagepolitik på et nyt montagevarekort.  
-   Oprette en montagestykliste, der viser montagekomponenter og den ressource, der indgår i montageelementet.  

### <a name="selling-customized-assembly-items" />Sælge tilpassede montageelementer

[!INCLUDE[prod_short](includes/prod_short.md)] giver fleksibilitet til både at indtaste et lagerantal og en montage til ordre-mængde på én salgsordrelinje. Dette afsnit dækker følgende opgaver:  

-   Oprette en ren ATO-salgsordrelinje, hvor den fulde mængde ikke er tilgængelig, og som skal samles før afsendelse.  
-   Tilpasse ATO elementer.  
-   Genberegne salgsprisen på et tilpasset montageelement.  
-   Oprette en blandet salgsordrelinje, hvor dele af salgsmængden leveres fra lager, og den resterende del skal samles før afsendelse.  
-   Forstå ATO-tilgængelighedsadvarsler.  

### <a name="planning-for-assembly-items" />Planlægge for montageelementer

Montageefterspørgsel og forsyning håndteres af planlægningssystemet, præcis som for køb, overførsel og produktion. Dette afsnit dækker følgende opgaver:  

-   Køre en totalplan for varer med salgsbehov for monteret levering.  
-   Oprette en montageordre for at opfylde et salgslinjeantal for den efterspurgte afsendelsesdato.  

### <a name="assembling-items" />Montageelementer

Montageordrer fungerer på samme måde som produktionsordrer, bortset fra at forbruget og afgangen registreres og bogføres direkte fra ordren. Når varerne skal samles til lager, har montagearbejderen fuld adgang til alle sidehoved- og linjefelter. Når varerne skal samles til en ordre, hvor mængden og datoen er bekræftet for debitoren, kan visse felter på montageordren ikke redigeres. I så fald udføres montagebogføringen fra lagerleverance for den tilknyttede salgsordre. Dette afsnit dækker følgende opgaver.  

-   Registrere og bogføre montageforbrug og afgang til lager.  
-   Adgang til en lagerleverancelinje fra en ATO-montageordre for at registrere montagearbejde.  
-   Adgang til en ATO-montageordre fra en lagerleverancelinje for automatisk at gennemse de indtastede data.  

### <a name="shipping-assembly-items-from-stock-and-assembled-to-order" />Levere montageelementer fra lager og monteret til ordre

Der findes specialfunktioner til styring af leveringen af montage efter ordre-mængder. Dette afsnit dækker følgende opgaver:  

-   Oprette et lagerpluk for lagermontageelementer og montagekomponenter, der skal samles før afsendelse.  
-   Registrere lagerpluk for montagekomponenter og derefter for montageelementer.  
-   Adgang til en montageordre fra en lagerleverance for at gennemgå plukkede eller forbrugte komponenter.  
-   Levere montage til ordre-mængder.  
-   Levere lagermontageelementer.  

## <a name="roles" />Roller

Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:  

-   Salgsordrebehandler  
-   Planlægger  
-   Montagearbejder  
-   Vælger  
-   Leveranceansvarlig  

## <a name="prerequisites" />Forudsætninger

Før du kan udføre opgaverne i denne gennemgang, skal du gøre følgende:  

-   Installer [!INCLUDE[prod_short](includes/prod_short.md)]  
-   Opret dig selv som en lagermedarbejder på lokationen HVID ved at følge disse trin:  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
2.  Vælg feltet **Bruger-id**, og vælg din egen brugerkonto på siden **Brugere**.  
3.  Angiv HVID i feltet **Lokationskode**.  
4.  Markér feltet **Standard**.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Forbered placeringen HVID til montagebehandling ved at følge disse trin:  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.  
2.  Åbn lokationskortet for lokationen HVID.  
3.  I oversigtspanelet **Placering** skal du angive **W-10-0001** i feltet **Placeringskode til til-montage**.  

    Ved at angive denne ikke-plukkede placeringskode, vil alle montageordrelinjer være klar til at modtage deres komponenter på placeringen.  

4.  I feltet **Placeringskode til fra-montage** skal du angive **W-01-0001**.  

    Ved at angive denne plukplaceringskode afsendes der færdige montageelementer til placeringen.  

Fjern standardleveringstiden for interne processer ved at følge disse trin:  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Produktionsopsætning**, og vælg derefter det relaterede link.  
2.  På siden **Produktionsopsætning** i oversigtspanelet **Planlægning** skal du fjerne værdien i feltet **Standardsikkerhedstid**.  

<!-- Create inventory for assembly components by following [Prepare Sample Data](walkthrough-selling-assembling-and-shipping-kits.md#prepare-sample-data).   -->

## <a name="story" />Historie

Den 23. januar modtager Susanne, der er salgsordrebehandler en ordre fra Enhedsbutikken på tre enheder af pakke B, som er et ATO-element. Alle tre enheder er tilpasset og skal indeholde det stærke grafikkort og en ekstra RAM-blok. Diskdrevene er opgraderet til DVD, fordi cd-drev ikke er tilgængelige. Susan ved, at enhederne kan samles med det samme, så hun bevarer den foreslåede afsendelsesdato, der er den 23. januar.  

På samme tid tilbyder debitoren femten enheder af pakke A med en særlig anmodning om, at fem enheder tilpasses, så de indeholder det stærke grafikkort. Selvom pakke A typisk er en montage til lager-vare, kombinerer ordrebehandleren salgslinjemængder for at sælge ti enheder fra lageret og samle fem tilpassede enheder til ordren. Ti enheder af pakke A er tilgængelige og skal først leveres til lageret ved en montageordre i henhold til varens montagepolitik. Susanne får at vide af montageafdelingen, at pakke A-enheder ikke kan færdiggøres i den aktuelle uge. Susan angiver afsendelsesdatoen for den anden salgsordrelinje for blandet ATO og lagermængden til den 27. januar og oplyser debitoren om, at 15 enheder af pakke A afsendes fire dage senere end de tre enheder af pakke B. For at signalere til afsendelseafdelingen, at denne salgsordre kræver montagebehandling, opretter Susanne lagerleverancedokumentet fra salgsordren.  

Erik, der er planlægger, kører planlægningskladden og genererer en montageordre for ti standardenheder af pakke A med en intern forfaldsdato den 27. januar.  

Sammy, der er ansvarlig for levering, får tre lagerleverancelinjer til salgsordren: Én linje for de tre rene ATO-enheder, én linje for de fem ATO-enheder på linjen for blandede salgsordrer og én linje for de ti ATS-enheder på linjen for blandet salgordre. Sammy opretter et lagerplukdokument for alle montagekomponenter, der er nødvendige for at samle de i alt otte ATO-enheder på lagerleverancedokumentet.  

John, der er plukkeren, henter komponenter til alle ATO-mængder på lagerleverancedokumentet og bringer dem til montageområdet. John indtaster den mængde, der skal håndteres, og registrerer lagerplukket.  

Linda samler de tre ATO-enheder i pakke B. Komponenterne er allerede plukket, og hun registrerer ikke afgang og forbrugte mængder eller bogfører ordren, da begge disse handlinger udføres automatisk gennem de relaterede lagerleverancelinjer.  

Sammy registrerer den monterede mængde på lagerleverancelinjen og bogfører leverancen af de tre enheder af pakke B. Den første linje i salgsordren opdateres ved levering. Den tilknyttede montageordre forbliver åben, indtil salgsordren er fuldt faktureret. De to salgsleverancelinjer, én ATO og én ATS, til pakke A med forfaldsdatoen den 27. januar forbliver åbne.  

Den 27. januar behandler Linda to montageordrer for pakke A. Den første ordre er ATO-ordren på fem enheder, som hun behandler anderledes end ATO-ordren for pakke B, som hun behandlede den 23. januar. På denne ordre har Linda selv adgangstilladelse til lagerleverancelinjen og kan registrere det udførte montagearbejde. De nødvendige komponenter er klar i montageafdelingen, da de blev plukket sammen med komponenterne til pakke B.  

Den anden montageordre er ATS-ordren på ti enheder, der blev oprettet af planlægningssystemet. På denne ATS-ordre foretager Linda alle involverede handlinger fra montageordren. Linda opretter et lagerplukdokument for alle montagekomponenter, der er nødvendige for at montere de ti enheder. Når pc'erne samles, bogfører Linda montageordren og signalerer dermed, at varerne er disponible på lageret og kan plukkes til forsendelse.  

Sammy opretter et lagerplukdokument for de mængder, der er tilbage, før lagerleverancen kan bogføres. Der oprettes et plukdokument for ti enheder af pakke A, der lige er afsluttet. Komponenter, der skal bruges til at samle de fem enheder af pakke A, blev plukket den 23. januar.  

John henter ti enheder af pakke A fra lageret til det angivne afsendelsesområde, registrerer mængden, der skal håndteres, og registrerer derefter plukket.  

Sammy pakker de ti ATS-enheder med de fem ATO-enheder, som Linda samlede tidligere på dagen. Sammy udfylder mængden, der skal leveres, på begge linjer og bogfører derefter den sidste leverance til Enhedsbutikken. Den relaterede montageordre på fem enheder af pakke A bogføres automatisk. Den anden linje i salgsordren opdateres ved levering. To tilknyttede montageordrer forbliver åbne, indtil salgsordren er faktureret og lukket.  

Når salgsordren senere bogføres som fuldt faktureret, fjernes salgsordren og den tilknyttede montageordre.  

## <a name="prepare-sample-data" />Klargøre eksempeldata

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerkladder**, og vælg derefter det relaterede link.  
2.  Vælg feltet **Kladdenavn**, og vælg derefter standardkladden.  
3.  Opret positive lagerreguleringer på lokationen HVID på arbejdsdatoen, 23. januar, ved at indtaste følgende oplysninger.  

    |**Varenr.**|**Zonekode**|**Placeringskode**|**Antal**|  
    |-----------------------------------|---------------------------------------|--------------------------------------|------------------------------------|  
    |80001|PLUK|V-01-0001|20|  
    |80005|PLUK|V-01-0001|20|  
    |80011|PLUK|V-01-0001|20|  
    |80014|PLUK|V-01-0001|20|  
    |80203|PLUK|V-01-0001|20|  
    |80209|PLUK|V-01-0001|20|  

4.  Vælg handlingen **Registrer**, og vælg derefter knappen **Ja**.  

    Synkroniser derefter de nye lagerposter med lageret.  

5.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varekladder**, og vælg derefter det relaterede link. Siden **Varekladde** åbnes.  
6.  Vælg handlingen **Beregn regulering (logistik)**.  
7.  På siden **Beregn lagerregulering** skal du vælge knappen **OK**.  
8.  På siden **Varekladde** skal du vælge handlingen **Bogfør** og derefter vælge knappen **Ja**.  

### <a name="creating-the-assembly-items" />Oprette montageelementer

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Opret det første montageelement baseret på følgende oplysninger.  

    |Felt|Værdi|  
    |---------------------------------|-----------|  
    |**Beskrivelse**|Pakke A – grundlæggende pc-pakke|  
    |**Basisenhed**|STK|  
    |**Varekategorikode**|Diverse|  
    |**Genbestillingssystem**|Montage|  
    |**Montagepolitik**|Montage-til-lager|  
    |**Genbestillingsmetode**|Lot-for-Lot|  

    > [!NOTE]  
    >  Pakke A, leveres typisk af montage til lager og har derfor en genbestilllingsmetode for at gøre det til en del af den generelle forsyningsplanlægning.  

4.  Vælg handlingen **Montage**, og vælg derefter **Montagestykliste**.  
5.  Definer en montagestykliste for pakke A med følgende oplysninger.  

    |**Type**|**Nummer**|**Antal pr.**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Vare|80001|1|  
    |Vare|80011|1|  
    |Vare|80209|1|  
    |Ressource|Lise|1|  

6.  Opret det andet montageelement baseret på følgende oplysninger.  

    |Felt|Værdi|  
    |---------------------------------|-----------|  
    |**Beskrivelse**|Pakke B – Pro-pc|  
    |**Basisenhed**|STK|  
    |**Varekategorikode**|Diverse|  
    |**Genbestillingssystem**|Montage|  
    |**Montagepolitik**|Montage efter ordre|  

    > [!NOTE]  
    >  Pakke B leveres normalt af montage til ordre og har derfor ikke en genbestilllingsmetode, fordi det ikke bør være en del af den generelle forsyningsplanlægning.  

7.  Vælg handlingen **Montage**, og vælg derefter **Montagestykliste**.  
8.  Definer en montagestykliste for pakke B med følgende oplysninger.  

    |**Type**|**Nummer**|**Antal pr.**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Vare|80005|1|  
    |Vare|80014|1|  
    |Vare|80210|1|  
    |Ressource|Lise|1|  

### <a name="selling-the-assembly-items" />Sælge montageelementerne

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Opret to salgsordrelinjer for debitor 62000, Enhedsbutikken, på datoen for arbejde med følgende oplysninger.  

    |**Type**|**Beskrivelse**|**Antal**|Antal til montage til ordre|Afsendelsesdato|  
    |--------------|---------------------|------------------|-------------------------------|-------------------|  
    |Vare|Pakke B – Pro-pc|3|3|23. januar|  
    |Vare|Pakke A – grundlæggende pc-pakke|15|5|27. januar|  

    > [!NOTE]  
    >  Der findes følgende tilgængelighedsproblem for salgsordrelinjen for pakke B:  
    >   
    >  -   Montagekomponenten 80210 er ikke tilgængelig. Det betyder, at tre angivne enheder af pakke B ikke kan samles, hvilket angives med **0** i feltet **Mulighed for montage** siden **Montagedisponering**.  
    >   
    >  Der findes følgende tilgængelighedsproblem for salgsordrelinjen for pakke A:  
    >   
    >  -   Ti enheder af pakke A er ikke tilgængelige. Dette angiver over for planlægningssystemet, at mængden skal samles til lager.  

    Herefter kan du tilpasse salgsordren.  

4.  Vælg salgsordrelinjen på tre enheder af pakke B.  
5.  På oversigtspanelet **Linjer** skal du vælge **Linje**, vælg **Montage efter ordre**, og vælg derefter **Montage efter ordre-linjer**.  
6.  På siden **Montage efter ordre-linjer** skal du på montageordrelinjen for vare 80014 angive **2** i feltet **Antal pr.**.  
7.  På montageordrelinjen for vare 80210 skal du vælge feltet **Nummer** og derefter vælge vare 80209 i stedet.  
8.  Opret en ny montageordrelinje med følgende oplysninger.  

    |Enhedstype|Nummer|Antal pr.|  
    |----------|---------|------------------|  
    |Vare|80203|1|  

9. Luk siden **Montage efter ordre-linjer**.  

    Derefter skal du opdatere salgsprisen for pakke B i henhold til den tilpasning, som du netop har udført. Læg mærke til den aktuelle værdi i feltet **Enhedpris ekskl. moms**.  

10. På oversigtspanelet **Linjer** skal du vælge **Linje**, vælge **Montage til ordre** og derefter vælge **Akkumuleret pris**.  
11. Vælg knappen **Ja**. Læg mærke til den øgede værdi i feltet **Enhedpris ekskl. moms**.  
12. Vælg salgsordrelinjen på 15 enheder af pakke A.  
13. På oversigtspanelet **Linjer** skal du vælge **Linje**, vælg **Montage efter ordre**, og vælg derefter **Montage efter ordre-linjer**.  
14. Opret på siden **Montage efter ordre-linjer** en ny montageordrelinje med følgende oplysninger.  

    |Type|Nummer|Antal pr.|  
    |----------|---------|------------------|  
    |Vare|80203|1|  

     Dernæst skal du ændre afsendelsesdatoen af den anden salgsordrelinje ifølge montageplanen.  

15. På salgsordrelinjen for 15 enheder af pakke A skal du angive **27-01-2014** i feltet **Afsendelsesdato**.  
16. Vælg handlingen **Frigivelse**.  
17. Vælg handlingen **Opret lagerleverance**.  
18. Luk salgsordren.  

### <a name="planning-for-the-unavailable-ats-items" />Planlægge for utilgængelige ATS-elementer

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Planlægningskladde**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Beregn totalplan**.  
3.  På siden **Beregn plan** skal du angive følgende filtre.  

    |Startdato|Afslutningsdato|Nej.|  
    |-------------------|-----------------|---------|  
    |01-23-2014|01-27-2014|Pakke A – grundlæggende pc-pakke|  

4.  Vælg knappen **OK**.  

    En ny planlægningslinjen oprettes for den nødvendige montageordre på ti enheder, forfaldsdato den 27. januar. Der kræves ingen ændres, så du kan nu oprette ordren.  

5.  Vælg handlingen **Udfør aktionsmeddelelse**.  
6.  På siden **Udfør aktionsmeddelelse** skal du vælge feltet **Montageordre** og derefter vælge **Opret montageordrer**.  
7.  Vælg knappen **OK**.  

### <a name="assembling-and-shipping-the-first-ato-quantity" />Montere og levere den første ATO-mængde

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerleverancestatus**, og vælg derefter det relaterede link.  

    > [!NOTE]  
    >  I dette afsnit er den person, der er ansvarlig for leveringen, ansvarlig for registrering af det fuldførte ATO-montagearbejde på lagerleverancelinjen. Denne arbejdsproces, der kan opstå i miljøer, hvor montagearbejdet udføres af den person, der er ansvarlig for levering, eller af montagearbejdstagere i afsendelsesområdet.  
    >   
    >  I dette afsnit foretages handlinger på montageordren indirekte fra lagerleverancelinjen. Yderligere oplysninger om, hvordan du behandler en montageordre direkte, finder du i afsnittet "Samle varer til lager" i denne gennemgang.  

2.  Åbn seneste lagerleverance, der er oprettet til lokationen HVID.  

    Bemærk de tre lagerleverancelinjer: én linje for ATO-mængden i pakke B, som forfalder den 23. januar. En linje for ATO-mængden i pakke A med forfaldsdato den 27. januar. En linje for lagerantallet i pakke A med forfaldsdato den 27. januar.  

    Feltet **Montage efter ordre** angiver montagemetoden.

    Opret dernæst et plukdokument for alle ATO-montagekomponenter, der er nødvendige på lagerleverancen.  

3.  Vælg handlingen **Opret pluk**, og vælg derefter knappen **OK**.  

    Dernæst skal du udføre vælgerens opgave.  

4.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk**, og vælg derefter det relaterede link.  
5.  Åbn det lagerplukdokument, du oprettede i trin 3 i dette afsnit.  

    Bemærk værdien i feltet **Kildedokument**, og at alle pluklinjerne er til montagekomponenter.  

    Dernæst skal du registrere plukket uden at ændre standardoplysningerne.  

6.  Vælg handlingen **Autofyld håndteringsantal**.  
7.  Vælg handlingen **Registrer pluk**.  

    Vend tilbage for at foretage leveringsopgaver.  

8.  Åbn siden **Lagerleverance** igen.  

    Bemærk, at feltet **Plukket antal** stadig er tomt på alle linjer. Dette skyldes, at du stadig ikke har plukket de varer, der skal afsendes, men kun de komponenter, der skal bruges til montage af ATO-mængderne.  

    Fortsæt med at gennemgå den relaterede montageordre.  

9. Vælg leverancelinjen på tre enheder af pakke B.  
10. På oversigtspanelet **Linjer** skal du vælge **Linje** og derefter vælge **Montage til ordre**. Siden **Montageordre** åbnes.  

    Bemærk, at flere felter på montageordren ikke er tilgængelige, da ordren er knyttet til en salgsordre.  

    Bemærk, at på montageordrelinjer er feltet **Plukket antal** udfyldt. Dette skyldes det pluk, som du registrerede i trin 7 i dette afsnit.  

11. I feltet **Antal til montage** kan du forsøge at angive en værdi, der er lavere end **3**.  

    Læs fejlmeddelelsen, der forklarer, hvorfor dette felt kun kan blive udfyldt via feltet **Lever antal** på den relaterede leverance.  

    Feltet **Antal til montage** kan redigeres og har til formål at understøtte de situationer, hvor du vil foretage en delvis levering af en lagermængde i stedet for at samle flere enheder til ordren. Du kan finde flere oplysninger i afsnittet "Kombinationsscenarier" i [Om Montage til ordre og Montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

12. Luk siden **Montageordre** for at vende tilbage til siden **Lagerleverance**.  
13. På leverancelinjen for tre enheder af pakke B skal du i feltet **Lever antal** indtaste **3**.  
14. Vælg handlingen **Bogfør lev.**, og vælg derefter knappen **Lever**.  

    Sammen med denne lagerleverancebogføring, bogføres det fulde forbrug og afgangsmængder for den relaterede montageordre, og feltet **Restantal** er tomt. Salgsordrelinjen for pakke B opdateres for at vise, at de tre enheder er leveret.  

    Lageraktiviteter for at opfylde den første salgsordrelinje den 23. januar er fuldført. Opfyld dernæst de salgsordrelinjer, der skal leveres den 27. januar  

### <a name="assembling-and-recording-the-second-ato-quantity" />Montere og registrere den anden ATO-mængde

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Montageordrer**, og vælg derefter det relaterede link.  

    Bemærk, at ATO-ordren for leverede enheder af pakke B stadig er på listen, selvom **Restantal** er tom. Dette skyldes, at den tilknyttede salgsordre stadig ikke er fuldt faktureret.  

    > [!NOTE]  
    >  I dette afsnit er montagearbejdstageren ansvarlig for registrering af det fuldførte ATO-montagearbejde på lagerleverancelinjen. Denne arbejdsproces kan opstå i miljøer, hvor montagearbejdet udføres i en separat montageafdeling, og montagearbejdstagere har tilladelse til at ændre lagerleverancelinje.  

2.  Åbn ATO-montageordren på fem enheder af pakke A.  

    Bemærk, at felterne **Antal til montage** og **Antal til forbrug** er tomme, da intet arbejde er registreret endnu.  

    Bemærk, at på montageordrelinjer er feltet **Plukket antal** udfyldt. Dette skyldes det pluk, der blev registreret den 23. januar.  

    Registrer derefter, at montageordren er fuldført.  

3.  Vælg handlingen **Ordremont.lagerleverancelinje**.  
4.  På siden **Ordremont.lagerleverancelinje** i feltet **Lever antal** skal du angive **5** og derefter lukke siden.  

    På siden **Montageordre** skal du bemærke, at felterne **Antal til montage** og **Antal til forbrug** nu udfyldes med de mængder til afgang og forbrug, der skal bogføres i forbindelse med forsendelsen.  

5.  Luk siden **Montageordre**.  

### <a name="assembling-the-ats-quantity" />Montere ATS-antallet

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Montageordrer**, og vælg derefter det relaterede link.  
2.  Åbn montageordren på ti enheder af pakke A.  

    Bemærk, at feltet **Antal til montage** udfyldes med forventet antal.  

    Dernæst skal du oprette et plukdokument for at hente de nødvendige komponenter.  

3.  Vælg handlingen **Frigiv**.  
4.  Vælg handlingen **Opret pluk (logistik)**, og vælg derefter knappen **OK**.  

    Dernæst skal du udføre vælgerens opgave.  

5.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk**, og vælg derefter det relaterede link.  
6.  Åbn det lagerplukdokument, du oprettede i trin 4 i dette afsnit.  

     Fortsæt med at registrere plukket uden at ændre standardoplysningerne.  

7.  Vælg handlingen **Autofyld håndteringsantal**.  
8.  Vælg handlingen **Registrer pluk**.  

    Gå tilbage til montageordren for at udføre den sidste montageopgave.  

9. Under **Montageordre** skal du vælge handlingen **Bogfør** og derefter vælge knappen **Ja**.  

    Bemærk, at montageordren fjernes fra listen over åbne ordrer.  

### <a name="shipping-the-remaining-items-partly-from-stock-and-partly-assembled-to-the-order" />Levere de resterende elementer delvist fra lager og delvist monteret til ordren

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerleverancestatus**, og vælg derefter det relaterede link.  
2.  Åbn seneste lagerleverance, der er oprettet til lokationen HVID.  

    Bemærk på linjen for ti enheder af pakke A, at feltet **Lever antal** og **Plukket antal** er tomt.  

    Derefter skal du vælge de resterende elementer.  

3.  Vælg handlingen **Opret pluk**, og vælg derefter knappen **OK**.  

    Dernæst skal du udføre vælgerens sidste opgave for denne lagerleverance.  

4.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk**, og vælg derefter det relaterede link.  
5.  Åbn det lagerplukdokument, du oprettede i trin 3 i dette afsnit.  

    Bemærk, at dette plukdokument er for montageelement, ikke for montagekomponenter.  

    Registrer derefter plukket uden at ændre standardoplysningerne.  

6.  Vælg handlingen **Autofyld håndteringsantal**.  
7.  Vælg handlingen **Registrer pluk**, og vælg derefter knappen **Ja**.  

    Gå tilbage til lagerleverancen for at udføre den sidste montageopgave.  

8.  Åbn siden **Lagerleverance** igen.  

    På siden **Lagerleverance** på linjen for ti enheder af pakke A, skal du bemærke, at felterne **Lever antal** og **Plukket antal** nu indeholder **10**.  

9. Vælg handlingen **Bogfør lev.**, og vælg derefter **Lever**.  

    Lagerleverancedokumentet fjernes, hvilket angiver, at de involverede lageraktiviteter er fuldført. Dernæst skal du bekræfte, at salgsordren er blevet behandlet.  

10. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link  
11. Åbn salgsordren for Enhedsbutikken.  

    Bemærk, at feltet **Leveret (antal)** indeholder den fulde mængde på begge linjer.  

    Når Enhedsbutikken betaler for deres modtagelse af 18 pc'er fra CRONUS, fjernes salgsordren og dens tilknyttede montageordrer.  

## <a name="see-related-microsoft-training" />Se relateret [Microsoft-træning](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also" />Se også

 [Om montage til ordre og montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md)   
 [Montere elementer](assembly-how-to-assemble-items.md)   
 [Plukke varer til lagerleverance](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md)   
 [Montere elementer](assembly-how-to-assemble-items.md)   
 [Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md)   
 [Designoplysninger: Internt lagerflow](design-details-internal-warehouse-flows.md)   
 [Designoplysninger: Udgående lagerflow](design-details-outbound-warehouse-flow.md)   
<!--  [Walkthrough: Planning Supplies Automatically](walkthrough-planning-supplies-automatically.md) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
