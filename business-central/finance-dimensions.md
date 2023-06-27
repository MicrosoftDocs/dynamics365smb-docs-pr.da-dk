---
title: Arbejde med dimensioner for sporing og analyse af data
description: 'Brug dimensioner til at kategorisere poster, f.eks. efter afdeling eller projekt, så du nemt kan spore og analysere data og lettere træffe gode beslutninger for din virksomhed.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/27/2023
ms.custom: bap-template
ms.search.keywords: 'analysis, history, track, business intelligence'
ms.search.form: '408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253'
---
# <a name="work-with-dimensions" />Arbejde med dimensioner

Dimensioner er værdier, der kategoriserer poster, så du kan spore og analysere dem i dokumenter som f.eks. salgsordrer. Dimensioner kan f.eks. angive det projekt eller den afdeling, en post kommer fra.  

Så i stedet for at oprette separate finanskonti for hver afdeling og hvert projekt kan du bruge dimensioner som grundlag for analyse og undgå at skulle oprette en kompliceret kontoplan. Få mere at vide om [Business Intelligence](bi.md).

Som et andet eksempel kan du oprette en dimension med navnet *Afdeling* og bruge den, når du bogfører salgsdokumenter. Derved kan du bruge business intelligence-værktøjer til at se, hvilke afdelinger der har solgt hvilke varer. Jo flere dimensioner, du bruger, jo mere detaljerede rapporter kan du basere forretningsmæssige beslutninger på. Nu kan en enkelt salgspost indeholde oplysninger fra flere dimensioner, f.eks.:  

* Den konto, som varesalget blev bogført på.  
* Hvor varen blev solgt.
* Hvem, der solgte den.
* Hvilken kunde har købt den.

## <a name="analyzing-by-dimensions" />Analyse efter dimensioner

Dimensioner spiller en vigtig rolle i business intelligence, f.eks. når du definerer analyser. Få mere at vide i [Analysere data efter dimensioner](bi-how-analyze-data-dimension.md).

> [!TIP]
> For hurtigt at analysere transaktionsdata efter dimensioner kan du bruge handlingen **Indstil dimensionsfilter** til at filtrere totaler efter dimensioner i kontoplanen og på alle sider for poster.

> [!NOTE]
> Analysevisninger bruger ofte data fra dimensioner. Hvis du opdager, at der er anvendt en ukorrekt dimension på bogførte finansposter, kan du rette dimensionsværdierne og opdatere dine analysevisninger. På den måde kan du lettere sikre, at dine finansrapporter og analyser bliver nøjagtige. Få mere at vide i [Fejlfinding og korrigering af dimensioner](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="dimension-sets" />Dimensionsgrupper

En dimensionsgruppe er en entydig kombination af dimensionsværdier. De er gemt som dimensionsgruppeposter i databasen. Hver dimensionsgruppepost repræsenterer en enkelt dimensionsværdi. Derudover identificeres hver dimensionsgruppe og dimensionsgruppepost i den af et fælles dimensionsgruppe-id.  

Når du opretter en kladdelinje, et nyt bilagshoved eller en ny bilagslinje, kan du angive en kombination af dimensionsværdier. I stedet for at eksplicit at gemme hver dimensionsværdi i databasen, tildeles kladdelinjen, bilagshovedet eller bilagslinjen en dimensionsgruppe-id, der angiver dimensionsgruppen.  

## <a name="setting-up-dimensions" />Oprette dimensioner

Du kan definere dimensioner og dimensionsværdier for at kategorisere kladder og dokumenter, f.eks. salgsordrer og indkøbsordrer. Du kan oprette dimensioner på siden **Dimensioner**, hvor du opretter én linje for hver dimension, f.eks. *Projekt*, *Afdeling*, *Område* og *Sælger*.

Du kan også angive værdier for dimensioner. Antag, at værdier repræsenterer virksomhedens afdelinger. Dimensionsværdier kan oprettes i en hierarkisk struktur, der ligner kontoplanen. Det betyder, at data kan opdeles i forskellige niveauer, og undersæt af dimensionsværdier kan sammentælles. Du kan angive det antal dimensioner og dimensionsværdier, som du har brug for, og de kan bruges af alle i virksomheden.

Når dimensioner og værdier er oprettet, kan du definere globale dimensioner og genvejsdimensioner på siden **Opsætning af Finans**. Disse dimensioner er derefter altid tilgængelige, så du kan vælge dem som felter på kladde- og dokumentlinjer og i finansposter uden først at åbne **Dimensioner**-siden. Få flere oplysninger i [Sådan konfigureres globale dimensioner og genvejsdimensioner](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Globale dimensioner** bruges som filtre, f.eks. i rapporter, kørsler og XMLporte. Du kan kun bruge to globale dimensioner, så vælg dimensioner, du bruger ofte.
* **Genvejsdimensioner** er tilgængelige som felter på kladde- og dokumentlinjer og ældre poster. Du kan oprette op til otte af disse.  

> [!NOTE]
> Når du har brugt en ny dimension i en post, f. eks. en linje eller en ny post, kan du ikke slette dimensionen, selvom du ikke bogfører posten. Det skyldes, at [!INCLUDE[prod_short](includes/prod_short.md)] med det samme opretter en dimensionsopsætning til linjen eller posten. Der er flere oplysninger i [Dimensionsgrupper](finance-dimensions.md#dimension-sets).

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts" />Sådan konfigureres standarddimensioner for kunder, leverandører og andre konti

Du kan tildele en standarddimension for en specifik konto. Dimensionen kopieres til kladden eller dokumentet, når du angiver kontonummeret på en linje, men du kan slette og ændre koden på linjen, hvis det er relevant. Du kan også kræve en dimension til bogføring af en post i en bestemt type konto. > 

> [!NOTE]
> Prioritering af standarddimensioner åbner for scenarier i salg og køb, som du gerne vil betale særligt kendskab til. Når du bruger standarddimensionsprioriteter på salgs-og købsdokumenter, skal [!INCLUDE [prod_short](includes/prod_short.md)] altid tage højde for dimensionerne i hovedet, som stammer fra debitoren eller kreditoren. Dette gælder for dimensioner, som du angiver manuelt eller som standard, og som specielt er relevant, når du bruger standarddimensioner på lokationer og varer, men ikke på debitorer eller kreditorer.
>
> **Eksempel**
>
> Du har et scenarie med følgende dimensionsindstillinger:
>
> * En debitor uden standarddimensioner
> * En vare med ADM som dimensionsværdi for AFDELING-dimensionen
> * En lokation med PROD som dimensionsværdi for AFDELING-dimensionen
> * Prioritering af standarddimensioner angives som debitor > vare > lokation
>
> Når du opretter et nyt dokument i dette scenario, bruges dimensionerne som følger:
>
> * Hvis du opretter et nyt dokument og tilføjer en lokation, vil standardværdien for nye linjer være PRODUKTIONSORDRE. Når du tilføjer linjer med varer, bevarer [!INCLUDE [prod_short](includes/prod_short.md)] PRODUKTION-ordren, fordi den kommer fra dokumentets hoved.
>
> * Hvis du opretter et nyt dokument og tilføjer varer, der har dimensionen ADM, og derefter angiver en placering i dokumentets hoved, spørger [!INCLUDE [prod_short](includes/prod_short.md)], om du vil overskrive de eksisterende linjer, da der er en konflikt.
>
> Det anbefales, at du tester standardopsætningen af dimensioner, dimensions prioriteter og den rækkefølge, du angiver data i dokumenter i.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Dimensioner**, og vælg derefter det relaterede link.  
2. På siden **Dimensioner** skal du vælge den relevante dimension og derefter vælge handlingen **Kontotype - standarddim**.  
3. Udfyld en linje for hver ny standarddimension, du vil oprette. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Hvis en dimension skal gøres obligatorisk, men du ikke vil tildele en standardværdi til dimensionen, skal du undlade at udfylde feltet **Dimensionsværdikode** og derefter markere **Tvungen kode** i feltet **Værdibogføring**.  

> [!WARNING]  
> Hvis en konto skal bruges i kørslerne **Juster valutakurser** eller **Bogfør lagerregulering**, skal du ikke vælge **Kode skal angives** eller **Samme kode**. Kørslerne kan ikke anvende dimensionskoder.  

> [!NOTE]  
> Hvis en konto skal have tilknyttet en anden dimension end standarddimensionen til kontotypen, skal du oprette en ny standarddimension til denne konto. Standarddimensionen for den enkelte konto erstatter standarddimensionen for kontotypen.  

### <a name="to-set-up-default-dimension-priorities" />Sådan oprettes prioritering af standarddimensioner

Forskellige kontotyper, f.eks. en debitorkonto eller en varekonto, kan have forskellige standarddimensioner. Et resultat heraf er, at en post kan have mere end én standarddimension som forslag. For at undgå sådanne konflikter, kan du knytte prioriteringsregler til forskellige kilder.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Prioritering af standarddim.**, og vælg derefter det relaterede link.  
2. På siden **Prioritering af standarddim.** i feltet **Kildekode** skal du indtaste kildekoden for den posteringstabel, som standarddimensionsprioriteterne skal gælde for.  
3. Udfyld en linje for hver standarddimensionsprioritet, du ønsker for det valgte kildespor.
4. Gentag denne fremgangsmåde for hvert kildespor, du vil oprette standarddimensionsprioriteter til.  

> [!IMPORTANT]  
> Hvis du har oprettet to tabeller med samme prioritering for samme kildespor, vælger [!INCLUDE[prod_short](includes/prod_short.md)] altid tabellen med det laveste tabel-id.  

### <a name="to-set-up-dimension-combinations" />Sådan oprettes kombinationer af dimensioner

For at undgå bogføringsposter med modstridende eller irrelevante dimensioner kan du blokere eller begrænse bestemte kombinationer af to dimensioner. En blokeret dimensionskombination betyder, at du ikke kan bogføre begge dimensioner i samme post, uanset hvad dimensionsværdierne er. En begrænset dimensionskombination tillader derimod bogføring af begge dimensioner i samme post, men kun med visse kombinationer af dimensionsværdier.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **dimensionskombinationer**, og vælg derefter det relaterede link.  
2. På siden **Dimensionskombinationer** skal du vælge det ønskede felt med dimensionskombinationen blandt følgende indstillinger.  

    |Felt|Beskrivelse|
    |----------------------------------|---------------------------------------|  
    |**Ingen begrænsninger**|Denne dimensionskombination har ingen begrænsninger. Alle dimensionsværdier er tilladt.|  
    |**Begrænset**|Denne dimensionskombination har begrænsninger, der afhænger af, hvilke dimensionsværdier du angiver. Du skal angive begrænsningerne på siden **Dimensionsværdikombination**.|  
    |**Spærret**|Denne dimensionskombination er ikke tilladt.|  

3. Hvis du valgte indstillingen **Begrænset**, skal du definere, hvilke dimensionsværdikombinationer, der er blokeret. For at gøre dette skal du vælge feltet for at definere dimensionsværdikombinationen.  
4. Vælg herefter en dimensionsværdikombination som er blokeret og skriv **Blokeret** i feltet. Et tomt feltet betyder, at dimensionsværdikombinationen er tilladt. Gentag hvis flere kombinationer er blokerede.  

> [!NOTE]  
> De samme dimensioner vises i både rækker og kolonner, så derfor vises alle dimensionskombinationer to gange. [!INCLUDE[prod_short](includes/prod_short.md)] viser automatisk indstillingen i begge felter. Du kan ikke vælge noget i felterne fra øverste venstre hjørne og nedefter, fordi disse felter har samme dimension i både rækker og kolonner.  
>
> Den valgte indstilling kan ikke vises, før du forlader feltet.  
>
> Hvis du vil have vist navnet på dimensionen i stedet for koden, skal du markere feltet **Vis kolonnenavn**.

### <a name="to-set-up-global-and-shortcut-dimensions" />Sådan oprettes globale dimensioner og genvejsdimensioner

Globale dimensioner og genvejsdimensioner kan bruges som filter overalt i [!INCLUDE[prod_short](includes/prod_short.md)], herunder i rapporter, kørsler, ældre poster og analysevisninger. Globale dimensioner og genvejsdimensioner kan indsættes direkte, uden at siden **Dimensioner** først skal åbnes. På kladde- og dokumentlinjer kan du vælge globale dimensioner og genvejsdimensioner i et felt på linjen. Du kan også oprette to globale dimensioner og otte genvejsdimensioner. Vælg de dimensioner, du oftest benytter.

> [!IMPORTANT]
> Hvis du ændrer en global dimension eller en genvejsdimension, kræver det, at alle poster bogført med dimensionen er opdateret. Du kan ændre en global dimension med funktionen **Rediger globale dimensioner**, men det kan være tidskrævende og kan påvirke ydeevnen, og tabellerne er muligvis låst under opdateringen. Sørg for at vælge de globale dimensioner og genvejsdimensioner omhyggeligt, så du ikke behøver at ændre dem senere. Hvis du vil ændre en genvejsdimension, skal du bruge handlingen **Rediger dimensioner**.
>
> Du kan finde flere oplysninger i [Sådan ændres globale dimensioner](finance-dimensions.md#to-change-global-dimensions).

> [!NOTE]
> Når du tilføjer eller ændrer en global dimension eller genvejsdimension, logges du automatisk ud og ind igen, så den nye værdi er forberedt til brug.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af Finans**, og vælg derefter det relaterede link.
2. Udfyld felterne i oversigtspanelet **Dimensioner**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions" />Sådan ændres globale dimensioner

Når du ændrer en global dimension eller en genvejsdimension, opdateres alle poster, som er bogført med denne dimension. Da denne proces kan være tidskrævende og kan påvirke ydeevnen, kan processen tilpasses databasens størrelse ved hjælp af to forskellige tilstande.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af Finans**, og vælg derefter det relaterede link.
2. Vælg handlingen **Rediger globale dimensioner**.
3. Øverst på siden skal du vælge en af følgende to indstillinger for kørsel af batchjobbet.

    |Indstilling|Beskrivelse|
    |-|-|
    |**Fortløbende**|(Standard) Hele dimensionsændringen udføres med én transaktion, der tilbagefører alle poster til de dimensioner, som de havde før ændringen.<br /><br />Denne indstilling anbefales, hvis virksomheden har forholdsvis få bogførte poster, så det vil tage den korteste tid at fuldføre batchjobbet. Processen låser flere tabeller og blokerer andre brugere, indtil den er færdig. Bemærk, at processen muligvis slet ikke fuldføres i denne tilstand for store databaser. Hvis det er tilfældet, skal du bruge indstillingen **Parallel**.|
    |**Parallel**|Dimensions ændringen foregår i flere baggrundssessioner, og operationen deles op i flere transaktioner. Hvis du vil bruge denne indstilling, skal du slå **Parallel behandling** til/fra . <br /><br />Denne indstilling anbefales til store databaser eller virksomheder med mange bogførte poster, fordi det vil tage den korteste tid at fuldføre. Bemærk, at denne opdateringsproces ikke starter i denne tilstand, hvis der er mere end én aktiv databasesession.|  

4. Indtast de nye dimensioner i felterne **Global dimension 1-kode** og/eller **Global dimension 2-kode**. De aktuelle dimensioner vises som grå bag felterne.
5. Benyt en af følgende fremgangsmåder afhængigt af tilstanden:
    * Vælg handlingen **Start** i tilstanden **Sekventiel**.
    * Vælg handlingen **Klargør** i tilstanden **Parallel**.

    Fanen **Logposter** er udfyldt med oplysninger om de dimensioner, der vil blive ændret.
6. Log ud af [!INCLUDE[prod_short](includes/prod_short.md)], og log på igen.
7. Vælg handlingen **Start** for at begynde parallel behandling af dimensionsændringer.

### <a name="example-of-dimension-setup" />Eksempel på dimensionsopsætning

Lad os antage, at dit firma vil kunne spore transaktioner baseret på virksomhedens struktur og geografiske placeringer. Til det formål kan du oprette to dimensioner på siden **Dimensioner**:

* **OMRÅDE**  
* **AFDELING**  

| Kode | Name | Kodetekst | Filtertekst |
| --- | --- | --- | --- |
| OMRÅDE |Område |Områdekode |Områdefilter |
| AFDELING |Afdeling |Afdelingskode |Afdelingsfilter |

For **OMRÅDE** tilføjer du følgende dimensionsværdier:

| Kode | Navn | Dimensionsværditype |
| --- | --- | --- |
| 10 |Nord- og Sydamerika |Fra-sum |
| 20 |Nordamerika |Standard |
| 30 |Stillehavsområdet |Standard |
| 40 |Sydamerika |Standard |
| 50 |Nord- og Sydamerika, total |Til-sum |
| 60 |Europa |Fra-sum |
| 70 |EU |Standard |
| 80 |Uden for EU |Standard |
| 90 |Europa, total |Til-sum |

For de to vigtigste geografiske områder, Nord- og Sydamerika og Europa, tilføjer du underkategorier for områder ved at indrykke dimensionsværdierne. Så kan du rapportere salg eller udgifter i områder og få vist totaler for større geografiske områder. Du kan også vælge at bruge lande, områder, regioner eller byer som dimensionsværdier, afhængigt af din virksomhed.

> [!NOTE]  
> Hvis du vil oprette et hierarki, skal koderne være i alfabetisk orden. Dette omfatter koderne for de dimensionsværdier, der er angivet i [!INCLUDE[prod_short](includes/prod_short.md)].  

For **AFDELING** tilføjer du følgende dimensionsværdier:

| Kode | Navn | Dimensionsværditype |
| --- | --- | --- |
| ADMIN |Opsætning |Standard |
| PROD |Produktion |Standard |
| SALG |Salg |Standard |

Med denne opsætning kan du tilføje dine to dimensioner som de to globale dimensioner på siden **Opsætning af Finans**. Det betyder, at du kan bruge OMRÅDE og AFDELING som filtre til finansposter samt i rapporter. Begge globale dimensioner kan også bruges som genvejsdimensioner på postlinjer og i bilagshoveder.

## <a name="getting-an-overview-of-dimensions-used-multiple-times" />Få et overblik over dimensioner, der bruges flere gange

Siden **Standarddimensioner - flere** angiver, hvordan en gruppe af konti bruger dimensioner og dimensionsværdier. Du kan angive dette ved at markere flere konti og derefter angive standarddimensioner og dimensionsværdier for dem. Derefter foreslår programmet disse dimensioner og dimensionsværdier, når en af disse konti bruges, f.eks. på en kladdelinje. Det gør det nemmere for brugeren at bogføre poster, eftersom felterne med dimensioner udfyldes automatisk. Bemærk også, at det er muligt manuelt at ændre de dimensionsværdier, der bliver foreslået, eksempelvis på kladdelinjer.

Siden **Standarddimensioner-flere** indeholder følgende felter:

|Felt|Beskrivelse|
|-----|-----------|  
|**Dimensionskode**|Viser alle de dimensioner, der er defineret som standarddimensioner for en eller flere af de markerede konti. Hvis du vælger feltet, får du vist en oversigt over alle tilgængelige dimensioner. Hvis du markerer en dimension, bliver den valgte dimension defineret som standarddimension for alle de markerede konti.|
|**Dimensionsværdikode**|Viser enten en enkelt dimensionsværdi eller ordet (Konflikt). Hvis feltet indeholder en dimensionsværdi, har alle markerede konti den samme standarddimensionsværdi for en dimension. Hvis der står (Konflikt) i feltet, så er det ikke alle de markerede konti, der har den samme standarddimensionsværdi for en dimension. Hvis du vælger feltet **Dimensionskode**, får du vist en oversigt over alle de tilgængelige dimensionsværdier for en dimension. Hvis du markerer en dimensionsværdi, bliver den defineret som standarddimensionsværdi for alle de markerede konti.|
|**Værdibogføring**|Viser enten en enkelt værdibogføringsregel eller ordet (Konflikt). Hvis der vises en værdibogføringsregel i feltet, så har alle markerede konti den samme værdibogføringsregel for en dimensionsværdi. Hvis der står (Konflikt) i feltet, så er det ikke alle de markerede konti, der har den samme værdibogføringsregel for en dimensionsværdi. Hvis du vælger feltet **Værdibogføring**, får du vist en liste med værdibogføringsregler for en dimension. Hvis du markerer en værdibogføringsregel, bliver den anvendt på alle de markerede konti.|

## <a name="use-dimensions" />Bruge dimensioner

I et dokument, f.eks en salgsordre, kan du tilføje dimensionsoplysninger for en individuel dokumentlinje og for selve dokumentet. Så på siden **Salgsordre** kan du f.eks. angive dimensionsværdier for de første to genvejsdimensioner på de enkelte salgslinjer, og du kan tilføje flere dimensionsoplysninger, hvis du vælger knappen **Dimensioner**.  

Hvis du i stedet arbejder i en kladde, kan du tilføje dimensionsoplysninger til en post på samme måde, hvis du har oprettet genvejsdimensioner som felter direkte på kladdelinjer.  

Du kan også angive standarddimensioner for konti eller kontotyper, så dimensioner og dimensionsværdier udfyldes automatisk.

### <a name="to-view-global-dimensions-in-ledger-entry-pages" />Sådan får du vist globale dimensioner på sider med poster

Globale dimensioner er altid virksomhedsdefineret og navngivet efter virksomheden. Du kan se de globale dimensioner for dit regnskab ved at åbne siden **Regnskabsopsætning**.

Du kan se, om der er globale dimensioner for poster, når du åbner en side med poster. De to globale dimensioner adskiller sig fra resten af dimensionerne, fordi du kan bruge dem som filtre overalt i [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Angiv **Kontoplan**, og vælg derefter det relaterede link.  
2. På siden **IC-kontoplan** skal du vælge handlingen **Poster**.  
3. Angiv et eller flere filtre, så du kun får vist de relevante poster på siden.  
4. Hvis du vil have vist alle dimensioner for en post, skal du vælge den og derefter vælge handlingen **Dimensioner**.  

> [!NOTE]  
> Siden **Postdimensioner** viser dimensioner for én post ad gangen. Når du ruller gennem finansposter, ændres indholdet på siden **Postdimensioner** løbende.

## <a name="see-related-microsoft-training" />Se relateret [Microsoft-træning](/training/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also" />Se også

[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Analysere data efter dimensioner](bi-how-analyze-data-dimension.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
