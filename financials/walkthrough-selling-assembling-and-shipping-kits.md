---
title: Gennemgang - Salg, montering og levering af pakker | Microsoft Docs
description: "For at støtte en for JIT-lagerstrategi og muligheden for at tilpasse produkter til debitorkrav, kan montageordrer automatisk oprettes og tilknyttes, så snart salgsordrelinjen er oprettet. Kæden mellem salgsbehov og montagelevering giver salgsordrebehandlere mulighed for at tilpasse montageelementet automatisk og love leveringsdatoer i henhold til komponentens tilgængelighed. Desuden bogføres montageforbrug og afgang automatisk med leverancen af den tilknyttede salgsordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 015acdfbbc349477b9e86225f2c971f993215000
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="walkthrough-selling-assembling-and-shipping-kits"></a>Gennemgang: Salg, montering og levering af pakker
For at støtte en for JIT-lagerstrategi og muligheden for at tilpasse produkter til debitorkrav, kan montageordrer automatisk oprettes og tilknyttes, så snart salgsordrelinjen er oprettet. Kæden mellem salgsbehov og montagelevering giver salgsordrebehandlere mulighed for at tilpasse montageelementet automatisk og love leveringsdatoer i henhold til komponentens tilgængelighed. Desuden bogføres montageforbrug og afgang automatisk med leverancen af den tilknyttede salgsordre.  

Der findes specielle funktioner til at dække levering af montage til ordre-mængder, både i grundlæggende og avancerede lagerkonfigurationer. Når medarbejdere, der er ansvarlige for montering, afslutter monteringsdele eller montage til ordre-mængde, registrerer de det i feltet **Levér antal** på lagerleverancelinjen i avancerede konfigurationer og vælger **Bogfør lev.**. Resultatet er, at den tilsvarende montageafgang bogføres, herunder det relaterede komponentforbrug, og en salgsleverance for mængden bogføres for den tilknyttede salgsordre. Denne gennemgang viser processen for det avancerede lager.  

I grundlæggende lagerkonfigurationer bogfører den ansvarlige lagermedarbejder et lagerpluk for salgsordrelinjerne, når en montage til ordre-mængde er klar til at blive leveret. Derefter oprettes en flytning (lager) for komponenterne, og montageoutputtet og salgsordreleverancen bogføres. Du kan finde flere oplysninger i afsnittet "Håndtere montage til ordre-varer i Pluk (lager)" i Pluk (lager).  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
Denne gennemgang viser følgende opgaver:  

### <a name="setting-up-assembly-items"></a>Konfigurere montageelementer  
Montageelementer er kendetegnet ved deres genbestillingssystem og montagestyklisten. Varens montagepolitik kan enten være montage til ordre (ATO) eller montage til lager (ATS). Dette afsnit dækker følgende opgaver:  

-   Angive det relevante genbestillingssystem og den relevante montagepolitik på et nyt montagevarekort.  
-   Oprette en montagestykliste, der viser montagekomponenter og den ressource, der indgår i montageelementet.  

### <a name="selling-customized-assembly-items"></a>Sælge tilpassede montageelementer  
[!INCLUDE[d365fin](includes/d365fin_md.md)]  giver fleksibilitet til både at indtaste et lagerantal og en montage til ordre-mængde på én salgsordrelinje. Dette afsnit dækker følgende opgaver:  

-   Oprette en ren ATO-salgsordrelinje, hvor den fulde mængde ikke er tilgængelig, og som skal samles før afsendelse.  
-   Tilpasse ATO elementer.  
-   Genberegne salgsprisen på et tilpasset montageelement.  
-   Oprette en blandet salgsordrelinje, hvor dele af salgsmængden leveres fra lager, og den resterende del skal samles før afsendelse.  
-   Forstå ATO-tilgængelighedsadvarsler.  

### <a name="planning-for-assembly-items"></a>Planlægge for montageelementer  
Montageefterspørgsel og forsyning håndteres af planlægningssystemet, præcis som for køb, overførsel og produktion. Dette afsnit dækker følgende opgaver:  

-   Køre en totalplan for varer med salgsbehov for monteret levering.  
-   Oprette en montageordre for at opfylde et salgslinjeantal for den efterspurgte afsendelsesdato.  

### <a name="assembling-items"></a>Montageelementer  
Montageordrer fungerer på samme måde som produktionsordrer, bortset fra at forbruget og afgangen registreres og bogføres direkte fra ordren. Når varerne skal samles til lager, har montagearbejderen fuld adgang til alle sidehoved- og linjefelter. Når varerne skal samles til en ordre, hvor mængden og datoen er bekræftet for debitoren, kan visse felter på montageordren ikke redigeres. I så fald udføres montagebogføringen fra lagerleverance for den tilknyttede salgsordre. Dette afsnit dækker følgende opgaver.  

-   Registrere og bogføre montageforbrug og afgang til lager.  
-   Adgang til en lagerleverancelinje fra en ATO-montageordre for at registrere montagearbejde.  
-   Adgang til en ATO-montageordre fra en lagerleverancelinje for automatisk at gennemse de indtastede data.  

### <a name="shipping-assembly-items-from-stock-and-assembled-to-order"></a>Levere montageelementer fra lager og monteret til ordre  
Der findes specialfunktioner til styring af leveringen af montage efter ordre-mængder. Dette afsnit dækker følgende opgaver:  

-   Oprette et lagerpluk for lagermontageelementer og montagekomponenter, der skal samles før afsendelse.  
-   Registrere lagerpluk for montagekomponenter og derefter for montageelementer.  
-   Adgang til en montageordre fra en lagerleverance for at gennemgå plukkede eller forbrugte komponenter.  
-   Levere montage til ordre-mængder.  
-   Levere lagermontageelementer.  

## <a name="roles"></a>Roller  
Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:  

-   Salgsordrebehandler  
-   Planlægger  
-   Montagearbejder  
-   Vælger  
-   Leveranceansvarlig  

## <a name="prerequisites"></a>Forudsætninger  
Før du kan udføre opgaverne i denne gennemgang, skal du gøre følgende:  

-   Installer [!INCLUDE[d365fin](includes/d365fin_md.md)]  
-   Opret dig selv som en lagermedarbejder på lokationen HVID ved at følge disse trin:  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
2.  Vælg feltet **Bruger-id**, og vælg din egen brugerkonto i vinduet **Brugere**.  
3.  Angiv HVID i feltet **Lokationskode**.  
4.  Markér feltet **Standard**.  

Forbered placeringen HVID til montagebehandling ved at følge disse trin:  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg derefter det relaterede link.  
2.  Åbn lokationskortet for lokationen HVID.  
3.  I oversigtspanelet **Placering** skal du angive **W-10-0001** i feltet **Placeringskode til til-montage**.  

    Ved at angive denne ikke-plukkede placeringskode, vil alle montageordrelinjer være klar til at modtage deres komponenter på placeringen.  

4.  I feltet **Placeringskode til fra-montage** skal du angive **W-01-0001**.  

    Ved at angive denne plukplaceringskode afsendes der færdige montageelementer til placeringen.  

Fjern standardleveringstiden for interne processer ved at følge disse trin:  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Produktionsopsætning** og vælg derefter det relaterede link.  
2.  I vinduet **Produktionsopsætning** i oversigtspanelet **Planlægning** skal du fjerne værdien i feltet **Standardsikkerhedstid**.  

Opret lager for montagekomponenter ved at følge afsnittet "Forberede eksempeldata" i denne gennemgang.  

## <a name="story"></a>Historie  
Den 23. januar modtager Susanne, der er salgsordrebehandler en ordre fra Enhedsbutikken på tre enheder af pakke B, som er et ATO-element. Alle tre enheder er tilpasset og skal indeholde det stærke grafikkort og en ekstra RAM-blok. Diskdrevene er opgraderet til DVD, fordi cd-drev ikke er tilgængelige. Susanne ved, at enhederne kan samles med det samme, så hun bevarer den foreslåede afsendelsesdato, der er den 23. januar.  

På samme tid tilbyder debitoren femten enheder af pakke A med en særlig anmodning om, at fem enheder tilpasses, så de indeholder det stærke grafikkort. Selvom pakke A typisk er en montage til lager-vare, kombinerer ordrebehandleren salgslinjemængder for at sælge ti enheder fra lageret og samle fem tilpassede enheder til ordren. Ti enheder af pakke A er tilgængelige og skal først leveres til lageret ved en montageordre i henhold til varens montagepolitik. Susanne får at vide af montageafdelingen, at pakke A-enheder ikke kan færdiggøres i den aktuelle uge. Hun angiver afsendelsesdatoen for den anden salgsordrelinje for blandet ATO og lagermængden til den 27. januar og oplyser debitoren om, at 15 enheder af pakke A afsendes fire dage senere end de tre enheder af pakke B. For at signalere til afsendelseafdelingen, at denne salgsordre kræver montagebehandling, opretter Susanne lagerleverancedokumentet fra salgsordren.  

Erik, der er planlægger, kører planlægningskladden og genererer en montageordre for ti standardenheder af pakke A med en intern forfaldsdato den 27. januar.  

Sammy, der er ansvarlig for levering, får tre lagerleverancelinjer til salgsordren: Én linje for de tre rene ATO-enheder, én linje for de fem ATO-enheder på linjen for blandede salgsordrer og én linje for de ti ATS-enheder på linjen for blandet salgordre. Han opretter et lagerplukdokument for alle montagekomponenter, der er nødvendige for at samle de i alt otte ATO-enheder på lagerleverancedokumentet.  

John, der er plukkeren, henter komponenter til alle ATO-mængder på lagerleverancedokumentet og bringer dem til montageområdet. Han indtaster den mængde, der skal håndteres, og registrerer lagerplukket.  

Linda samler de tre ATO-enheder i pakke B. Komponenterne er allerede plukket, og hun registrerer ikke afgang og forbrugte mængder eller bogfører ordren, da begge disse handlinger udføres automatisk gennem de relaterede lagerleverancelinjer.  

Sammy registrerer den monterede mængde på lagerleverancelinjen og bogfører leverancen af de tre enheder af pakke B. Den første linje i salgsordren opdateres ved levering. Den tilknyttede montageordre forbliver åben, indtil salgsordren er fuldt faktureret. De to salgsleverancelinjer, én ATO og én ATS, til pakke A med forfaldsdatoen den 27. januar forbliver åbne.  

Den 27. januar behandler Linda to montageordrer for pakke A. Den første ordre er ATO-ordren på fem enheder, som hun behandler anderledes end ATO-ordren for pakke B, som hun behandlede den 23. januar. På denne ordre har hun selv adgangstilladelse til lagerleverancelinjen og kan registrere det udførte montagearbejde. De nødvendige komponenter er klar i montageafdelingen, da de blev plukket sammen med komponenterne til pakke B.  

Den anden montageordre er ATS-ordren på ti enheder, der blev oprettet af planlægningssystemet. På denne ATS-ordre foretager Linda alle involverede handlinger fra montageordren. Hun opretter et lagerplukdokument for alle montagekomponenter, der er nødvendige for at montere de ti enheder. Når pc'erne samles, bogfører Linda montageordren og signalerer dermed, at varerne er disponible på lageret og kan plukkes til forsendelse.  

Sammy opretter et lagerplukdokument for de mængder, der er tilbage, før lagerleverancen kan bogføres. Der oprettes et plukdokument for ti enheder af pakke A, der lige er afsluttet. Komponenter, der skal bruges til at samle de fem enheder af pakke A, blev plukket den 23. januar.  

John henter ti enheder af pakke A fra lageret til det angivne afsendelsesområde, registrerer mængden, der skal håndteres, og registrerer derefter plukket.  

Sammy pakker de ti ATS-enheder med de fem ATO-enheder, som Linda samlede tidligere på dagen. Han udfylder mængden, der skal leveres, på begge linjer og bogfører derefter den sidste leverance til Enhedsbutikken. Den relaterede montageordre på fem enheder af pakke A bogføres automatisk. Den anden linje i salgsordren opdateres ved levering. To tilknyttede montageordrer forbliver åbne, indtil salgsordren er faktureret og lukket.  

Når salgsordren senere bogføres som fuldt faktureret, fjernes salgsordren og den tilknyttede montageordre.  

## <a name="setting-up-the-sample-data"></a>Oprette eksempeldata  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagerkladder**, og vælg derefter det relaterede link.  
2.  Vælg feltet **Kladdenavn**, og vælg derefter standardkladden.  
3.  Opret positive lagerreguleringer på lokationen HVID på arbejdsdatoen, 23. januar, ved at indtaste følgende oplysninger.  

    |**Varenr.**|**Zonekode**|**Placeringskode**|**Antal**|  
    |-----------------------------------|---------------------------------------|--------------------------------------|------------------------------------|  
    |80001|PLUK|V-01-0001|2.0|  
    |80005|PLUK|V-01-0001|2.0|  
    |80011|PLUK|V-01-0001|20|  
    |80014|PLUK|V-01-0001|20|  
    |80203|PLUK|V-01-0001|20|  
    |80209|PLUK|V-01-0001|20|  

4.  Under fanen **Startside** skal du i gruppen **Registrering** vælge **Registrer** og derefter vælge knappen **Ja**.  

    Synkroniser derefter de nye lagerposter med lageret.  

5.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varekladder**, og vælg derefter det relaterede link. Vinduet **Varekladde** åbnes.  
6.  Under fanen **Handlinger** i gruppen **Funktioner** vælges **Beregn lagerregulering**.  
7.  I vinduet **Beregn lagerregulering** skal du vælge knappen **OK**.  
8.  I vinduet **Varekladde** under fanen **Handlinger** i gruppen **Funktioner** skal du vælge **Bogfør** og derefter vælge knappen **Ja**.  

### <a name="creating-the-assembly-items"></a>Oprette montageelementer  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Under fanen **Startside** i gruppen **Administrer** skal du vælge **Ny**.  
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

4.  Vælg knappen **Montage** i gruppen **Montage/Produktion** under fanen **Naviger**, og vælg derefter **Montagestykliste**.  
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

7.  Vælg knappen **Montage** i gruppen **Montage/Produktion** under fanen **Naviger**, og vælg derefter **Montagestykliste**.  
8.  Definer en montagestykliste for pakke B med følgende oplysninger.  

    |**Type**|**Nummer**|**Antal pr.**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Vare|80005|1|  
    |Vare|80014|1|  
    |Vare|80210|1|  
    |Ressource|Lise|1|  

### <a name="selling-the-assembly-items"></a>Sælge montageelementerne  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.  
2.  Under fanen **Startside** i gruppen **Administrer** skal du vælge **Ny**.  
3.  Opret to salgsordrelinjer for debitor 62000, Enhedsbutikken, på datoen for arbejde med følgende oplysninger.  

    |**Type**|**Beskrivelse**|**Antal**|Antal til montage til ordre|Afsendelsesdato|  
    |--------------|---------------------|------------------|-------------------------------|-------------------|  
    |Vare|Pakke B – Pro-pc|3|3|23. januar|  
    |Vare|Pakke A – grundlæggende pc-pakke|15|5|27. januar|  

    > [!NOTE]  
    >  Der findes følgende tilgængelighedsproblem for salgsordrelinjen for pakke B:  
    >   
    >  -   Montagekomponenten 80210 er ikke tilgængelig. Det betyder, at tre angivne enheder af pakke B ikke kan samles, hvilket angives med **0** i feltet **Mulighed for montage** i vinduet **Montagedisponering**.  
    >   
    >  Der findes følgende tilgængelighedsproblem for salgsordrelinjen for pakke A:  
    >   
    >  -   Ti enheder af pakke A er ikke tilgængelige. Dette angiver over for planlægningssystemet, at mængden skal samles til lager.  

    Herefter kan du tilpasse salgsordren.  

4.  Vælg salgsordrelinjen på tre enheder af pakke B.  
5.  På oversigtspanelet **Linjer** skal du vælge **Linje**, vælg **Montage efter ordre**, og vælg derefter **Montage efter ordre-linjer**.  
6.  I vinduet **Montage efter ordre-linjer** skal du på montageordrelinjen for vare 80014 angive **2** i feltet **Antal pr.**.  
7.  På montageordrelinjen for vare 80210 skal du vælge feltet **Nummer** og derefter vælge vare 80209 i stedet.  
8.  Opret en ny montageordrelinje med følgende oplysninger.  

    |Enhedstype|Nej.|Antal pr.|  
    |----------|---------|------------------|  
    |Vare|80203|1|  

9. Luk vinduet **Montage efter ordre-linjer**.  

    Derefter skal du opdatere salgsprisen for pakke B i henhold til den tilpasning, som du netop har udført. Læg mærke til den aktuelle værdi i feltet **Enhedpris ekskl. moms**.  

10. På oversigtspanelet **Linjer** skal du vælge **Linje**, vælge **Montage til ordre** og derefter vælge **Akkumuleret pris**.  
11. Vælg knappen **Ja**. Læg mærke til den øgede værdi i feltet **Enhedpris ekskl. moms**.  
12. Vælg salgsordrelinjen på 15 enheder af pakke A.  
13. På oversigtspanelet **Linjer** skal du vælge **Linje**, vælg **Montage efter ordre**, og vælg derefter **Montage efter ordre-linjer**.  
14. Opret i vinduet **Montage efter ordre-linjer** en ny montageordrelinje med følgende oplysninger.  

    |Type|Nummer|Antal pr.|  
    |----------|---------|------------------|  
    |Vare|80203|1|  

     Dernæst skal du ændre afsendelsesdatoen af den anden salgsordrelinje ifølge montageplanen.  

15. På salgsordrelinjen for 15 enheder af pakke A skal du angive **27-01-2014** i feltet **Afsendelsesdato**.  
16. Under fanen **Handlinger** i gruppen **Frigiv** skal du vælge **Frigiv**.  
17. Vælg **Opret lagerleverance** i gruppen **Lagersted** under fanen **Handlinger**.  
18. Luk salgsordren.  

### <a name="planning-for-the-unavailable-ats-items"></a>Planlægge for utilgængelige ATS-elementer  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Planlægningskladde**, og vælg derefter det relaterede link.  
2.  Under fanen **Handlinger** i gruppen **Funktioner** skal du vælge **Beregn totalplan**.  
3.  I vinduet **Beregn plan** skal du angive følgende filtre.  

    |Startdato|Slutdato|Nummer|  
    |-------------------|-----------------|---------|  
    |01-23-2014|01-27-2014|Pakke A – grundlæggende pc-pakke|  

4.  Vælg knappen **OK**.  

    En ny planlægningslinjen oprettes for den nødvendige montageordre på ti enheder, forfaldsdato den 27. januar. Der kræves ingen ændres, så du kan nu oprette ordren.  

5.  Vælg **Udfør aktionsmeddelelse** i gruppen **Proces** under fanen **Handlinger**.  
6.  I vinduet **Udfør aktionsmeddelelse** skal du vælge feltet **Montageordre** og derefter vælge **Opret montageordrer**.  
7.  Vælg knappen **OK**.  

### <a name="assembling-and-shipping-the-first-ato-quantity"></a>Montere og levere den første ATO-mængde  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagerleverance**, og vælg derefter det relaterede link.  

    > [!NOTE]  
    >  I dette afsnit er den person, der er ansvarlig for leveringen, ansvarlig for registrering af det fuldførte ATO-montagearbejde på lagerleverancelinjen. Denne arbejdsproces, der kan opstå i miljøer, hvor montagearbejdet udføres af den person, der er ansvarlig for levering, eller af montagearbejdstagere i afsendelsesområdet.  
    >   
    >  I dette afsnit foretages handlinger på montageordren indirekte fra lagerleverancelinjen. Yderligere oplysninger om, hvordan du behandler en montageordre direkte, finder du i afsnittet "Samle varer til lager" i denne gennemgang.  

2.  Åbn seneste lagerleverance, der er oprettet til lokationen HVID.  

    Bemærk de tre lagerleverancelinjer: én linje for ATO-mængden i pakke B, som forfalder den 23. januar. En linje for ATO-mængden i pakke A med forfaldsdato den 27. januar. En linje for lagerantallet i pakke A med forfaldsdato den 27. januar.  

    Feltet **Montage efter ordre** angiver montagemetoden.

    Opret dernæst et plukdokument for alle ATO-montagekomponenter, der er nødvendige på lagerleverancen.  

3.  Under fanen **Handlinger** skal du i gruppen **Funktioner** vælge **Opret pluk** og derefter vælge knappen **OK**.  

    Dernæst skal du udføre vælgerens opgave.  

4.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Pluk**, og vælg derefter det relaterede link.  
5.  Åbn det lagerplukdokument, du oprettede i trin 3 i dette afsnit.  

    Bemærk værdien i feltet **Kildedokument**, og at alle pluklinjerne er til montagekomponenter.  

    Dernæst skal du registrere plukket uden at ændre standardoplysningerne.  

6.  Under fanen **Handlinger** i gruppen **Funktioner** skal du vælge **Autofyld håndteringsantal**.  
7.  Under fanen **Start** i gruppen **Registrering** skal du vælge **Registrer pluk**.  

    Vend tilbage for at foretage leveringsopgaver.  

8.  Åbn vinduet **Lagerleverance** igen.  

    Bemærk, at feltet **Plukket antal** stadig er tomt på alle linjer. Dette skyldes, at du stadig ikke har plukket de varer, der skal afsendes, men kun de komponenter, der skal bruges til montage af ATO-mængderne.  

    Fortsæt med at gennemgå den relaterede montageordre.  

9. Vælg leverancelinjen på tre enheder af pakke B.  
10. På oversigtspanelet **Linjer** skal du vælge **Linje** og derefter vælge **Montage til ordre**. Vinduet **Montageordre** åbnes.  

    Bemærk, at flere felter på montageordren ikke er tilgængelige, da ordren er knyttet til en salgsordre.  

    Bemærk, at på montageordrelinjer er feltet **Plukket antal** udfyldt. Dette skyldes det pluk, som du registrerede i trin 7 i dette afsnit.  

11. I feltet **Antal til montage** kan du forsøge at angive en værdi, der er lavere end **3**.  

    Læs fejlmeddelelsen, der forklarer, hvorfor dette felt kun kan blive udfyldt via feltet **Lever antal** på den relaterede leverance.  

    Feltet **Antal til montage** kan redigeres og har til formål at understøtte de situationer, hvor du vil foretage en delvis levering af en lagermængde i stedet for at samle flere enheder til ordren. Du kan finde flere oplysninger i afsnittet "Kombinationsscenarier" i [Om Montage til ordre og Montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

12. Luk vinduet **Montageordre** for at vende tilbage til vinduet **Lagerleverance**.  
13. På leverancelinjen for tre enheder af pakke B skal du i feltet **Lever antal** indtaste **3**.  
14. Vælg **Bogfør lev.** og derefter **Levér** i gruppen **Bogføring** under fanen **Handlinger**.  

    Sammen med denne lagerleverancebogføring, bogføres det fulde forbrug og afgangsmængder for den relaterede montageordre, og feltet **Restantal** er tomt. Salgsordrelinjen for pakke B opdateres for at vise, at de tre enheder er leveret.  

    Lageraktiviteter for at opfylde den første salgsordrelinje den 23. januar er fuldført. Opfyld dernæst de salgsordrelinjer, der skal leveres den 27. januar  

### <a name="assembling-and-recording-the-second-ato-quantity"></a>Montere og registrere den anden ATO-mængde  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Montageordrer**, og vælg derefter det relaterede link.  

    Bemærk, at ATO-ordren for leverede enheder af pakke B stadig er på listen, selvom **Restantal** er tom. Dette skyldes, at den tilknyttede salgsordre stadig ikke er fuldt faktureret.  

    > [!NOTE]  
    >  I dette afsnit er montagearbejdstageren ansvarlig for registrering af det fuldførte ATO-montagearbejde på lagerleverancelinjen. Denne arbejdsproces kan opstå i miljøer, hvor montagearbejdet udføres i en separat montageafdeling, og montagearbejdstagere har tilladelse til at ændre lagerleverancelinje.  

2.  Åbn ATO-montageordren på fem enheder af pakke A.  

    Bemærk, at felterne **Antal til montage** og **Antal til forbrug** er tomme, da intet arbejde er registreret endnu.  

    Bemærk, at på montageordrelinjer er feltet **Plukket antal** udfyldt. Dette skyldes det pluk, der blev registreret den 23. januar.  

    Registrer derefter, at montageordren er fuldført.  

3.  Under fanen **Naviger** i gruppen **Lagersted** skal du vælge **Ordremont.lagerleverancelinje**.  
4.  I vinduet **Ordremont.lagerleverancelinje** i feltet **Lever antal** skal du angive **5** og derefter lukke vinduet.  

    I vinduet **Montageordre** skal du bemærke, at felterne **Antal til montage** og **Antal til forbrug** nu udfyldes med de mængder til afgang og forbrug, der skal bogføres i forbindelse med forsendelsen.  

5.  Luk vinduet **Montageordre**.  

### <a name="assembling-the-ats-quantity"></a>Montere ATS-antallet  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Montageordrer**, og vælg derefter det relaterede link.  
2.  Åbn montageordren på ti enheder af pakke A.  

    Bemærk, at feltet **Antal til montage** udfyldes med forventet antal.  

    Dernæst skal du oprette et plukdokument for at hente de nødvendige komponenter.  

3.  Under fanen **Handlinger** i gruppen **Frigiv** skal du vælge **Frigiv**.  
4.  Under fanen **Handlinger** skal du i gruppen **Lagersted** vælge **Opret pluk (logistik)** og derefter vælge knappen **OK**.  

    Dernæst skal du udføre vælgerens opgave.  

5.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Pluk**, og vælg derefter det relaterede link.  
6.  Åbn det lagerplukdokument, du oprettede i trin 4 i dette afsnit.  

     Fortsæt med at registrere plukket uden at ændre standardoplysningerne.  

7.  Under fanen **Handlinger** i gruppen **Funktioner** skal du vælge **Autofyld håndteringsantal**.  
8.  Under fanen **Start** i gruppen **Registrering** skal du vælge **Registrer pluk**.  

    Gå tilbage til montageordren for at udføre den sidste montageopgave.  

9. I **Montageordre** skal du vælge **Bogfør** og derefter knappen **Ja** i gruppen **Bogføring** under fanen **Handlinger**.  

    Bemærk, at montageordren fjernes fra listen over åbne ordrer.  

### <a name="shipping-the-remaining-items-partly-from-stock-and-partly-assembled-to-the-order"></a>Levere de resterende elementer delvist fra lager og delvist monteret til ordren  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagerleverance**, og vælg derefter det relaterede link.  
2.  Åbn seneste lagerleverance, der er oprettet til lokationen HVID.  

    Bemærk på linjen for ti enheder af pakke A, at feltet **Lever antal** og **Plukket antal** er tomt.  

    Derefter skal du vælge de resterende elementer.  

3.  Under fanen **Handlinger** skal du i gruppen **Funktioner** vælge **Opret pluk** og derefter vælge knappen **OK**.  

    Dernæst skal du udføre vælgerens sidste opgave for denne lagerleverance.  

4.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Pluk**, og vælg derefter det relaterede link.  
5.  Åbn det lagerplukdokument, du oprettede i trin 3 i dette afsnit.  

    Bemærk, at dette plukdokument er for montageelement, ikke for montagekomponenter.  

    Registrer derefter plukket uden at ændre standardoplysningerne.  

6.  Under fanen **Handlinger** i gruppen **Funktioner** skal du vælge **Autofyld håndteringsantal**.  
7.  Under fanen **Startside** skal du i gruppen **Registrering** vælge **Registrer pluk** og derefter vælge knappen **Ja**.  

    Gå tilbage til lagerleverancen for at udføre den sidste montageopgave.  

8.  Åbn vinduet **Lagerleverance** igen.  

    I vinduet **Lagerleverance** på linjen for ti enheder af pakke A, skal du bemærke, at felterne **Lever antal** og **Plukket antal** nu indeholder **10**.  

9. Vælg **Bogfør lev.** og derefter **Levér** i gruppen **Bogføring** under fanen **Handlinger**.  

    Lagerleverancedokumentet fjernes, hvilket angiver, at de involverede lageraktiviteter er fuldført. Dernæst skal du bekræfte, at salgsordren er blevet behandlet.  

10. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link  
11. Åbn salgsordren for Enhedsbutikken.  

    Bemærk, at feltet **Leveret (antal)** indeholder den fulde mængde på begge linjer.  

    Når Enhedsbutikken betaler for deres modtagelse af 18 pc'er fra CRONUS, fjernes salgsordren og dens tilknyttede montageordrer.  

## <a name="see-also"></a>Se også  
 [Om montage til ordre og montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md)   
 [Montere elementer](assembly-how-to-assemble-items.md)   
 [Plukke varer til lagerleverance](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md)   
 [Montere elementer](assembly-how-to-assemble-items.md)   
 [Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md)   
 [Designoplysninger: Internt lagerflow](design-details-internal-warehouse-flows.md)   
 [Designoplysninger: Udgående lagerflow](design-details-outbound-warehouse-flow.md)   
 [Gennemgang: Automatisk planlægning af forsyninger](walkthrough-planning-supplies-automatically.md)

