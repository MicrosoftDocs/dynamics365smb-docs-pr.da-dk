---
title: Arbejde med dimensioner for nem sporing og analyse af data
description: Du kan bruge dimensioner til at kategorisere poster, f.eks. efter afdeling eller projekt, så du nemt kan spore og analysere data og lettere træffe gode beslutninger for din virksomhed.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track, business intelligence
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: aa97686299648b81e68aef1a3701e0c32d73138a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774076"
---
# <a name="working-with-dimensions"></a>Arbejde med dimensioner
Dimensioner er værdier, der kategoriserer poster, så du kan spore og analysere dem i dokumenter som f.eks. salgsordrer. Dimensioner kan f.eks. angive det projekt eller den afdeling, en post kommer fra.  

I stedet for at oprette separate finanskonti for hver afdeling og hvert projekt kan du bruge dimensioner som grundlag for analyse og undgå at skulle oprette en kompliceret kontoplan. Du kan finde flere oplysninger i [Business Intelligence](bi.md).

Som et andet eksempel kan du oprette en dimension med navnet *Afdeling* og bruge den, når du bogfører salgsdokumenter. Derved kan du bruge business intelligence-værktøjer til at se, hvilke afdelinger der har solgt hvilke varer. Jo flere dimensioner, du bruger, jo mere detaljerede rapporter kan du basere forretningsmæssige beslutninger på. F.eks. kan en enkelt salgspost indeholde oplysninger fra flere dimensioner, f.eks.:  

* Den konto, som varesalget blev bogført på  
* Hvor varen blev solgt
* Hvem, der solgte den
* Hvilken type kunde der købte den  

## <a name="analyzing-by-dimensions"></a>Analyse efter dimensioner
Dimensioner spiller en vigtig rolle i business intelligence, f.eks. når du definerer analyser. Du kan finde flere oplysninger i [Analysere data efter dimensioner](bi-how-analyze-data-dimension.md).

> [!TIP]
> For hurtigt at analysere transaktionsdata efter dimensioner kan du filtrere handlingen **Indstil dimensionsfilter** efter dimensioner i kontoplanen og på alle sider for poster.

## <a name="dimension-sets"></a>Dimensionsgrupper
<!--we describe what they are, but not their value.-->
En dimensionsgruppe er en entydig kombination af dimensionsværdier. Det er gemt som dimensionsgruppeposter i databasen. Hver dimensionsgruppepost repræsenterer en enkelt dimensionsværdi. Dimensionsgruppen er identificeret med en fælles dimensionsgruppe-id, der tildeles til hver dimensionsgruppepost, der hører til dimensionsgruppen.  

Når du opretter en kladdelinje, et nyt bilagshoved eller en ny bilagslinje, kan du angive en kombination af dimensionsværdier. I stedet for at eksplicit at gemme hver dimensionsværdi i databasen, tildeles kladdelinjen, bilagshovedet eller bilagslinjen en dimensionsgruppe-id, der angiver dimensionsgruppen.  

## <a name="setting-up-dimensions"></a>Oprette dimensioner
Du kan definere dimensioner og dimensionsværdier for at kategorisere kladder og dokumenter, f.eks. salgsordrer og indkøbsordrer. Du kan oprette dimensioner på siden **Dimensioner**, hvor du opretter én linje for hver dimension, f.eks. *Projekt*, *Afdeling*, *Område* og *Sælger*.

Du kan også angive værdier for dimensioner. Værdier kan f.eks. være afdelinger i virksomheden. Dimensionsværdierne kan oprettes i en hierarkisk struktur - ligesom kontoplanen - så data kan opdeles i forskellige granularitetsniveauer, og dimensionsdelmængder kan lægges sammen. Du kan angive det antal dimensioner og dimensionsværdier, som du har brug for, og de kan bruges af alle i virksomheden.

Når dimensioner og værdier konfigureres, kan du definere globale dimensioner og genvejsdimensioner på siden **Regnskabsopsætning**, der altid vil kunne vælges som felter på kladde- og dokumentlinjer, og ældre poster, uden at siden **Dimensioner** skal åbnes først. Du kan finde flere oplysninger i [Sådan konfigureres globale dimensioner og genvejsdimensioner](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Globale dimensioner** bruges som filtre, f.eks. i rapporter, kørsler og XMLporte. Du kan kun bruge to globale dimensioner, så vælg dimensioner, du bruger ofte.
* **Genvejsdimensioner** er tilgængelige som felter på kladde- og dokumentlinjer og ældre poster. Du kan oprette op til otte af disse.  

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Sådan konfigureres standarddimensioner for kunder, leverandører og andre konti
Du kan tildele en standarddimension for en specifik konto. Dimensionen kopieres til kladden eller dokumentet, når du angiver kontonummeret på en linje, men du kan slette og ændre koden på linjen, hvis det er relevant. Du kan også oprette en dimension, der kræves til bogføring af en post med en bestemt type konto.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Dimensioner**, og vælg derefter det tilknyttede link.  
2.  På siden **Dimensioner** skal du vælge den relevante dimension og derefter vælge handlingen **Kontotype-standarddim**.  
4.  Udfyld felterne for hver ny linje, du vil oprette. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Hvis en dimension skal gøres obligatorisk, men du ikke vil tildele en standardværdi til dimensionen, skal du undlade at udfylde feltet **Dimensionsværdikode** og derefter markere **Tvungen kode** i feltet **Værdibogføring**.  

> [!WARNING]  
>  Hvis en konto skal bruges i kørslerne **Juster valutakurser** eller **Bogfør lagerregulering**, skal du ikke vælge **Tvungen kode** eller **Samme kode**. Kørslerne kan ikke anvende dimensionskoder.  

> [!NOTE]  
>  Hvis en konto har tilknyttet en anden dimension end standarddimensionen, der allerede er oprettet til kontotypen, skal du oprette en standarddimension til denne konto. Standarddimensionen for den enkelte konto erstatter standarddimensionen for kontotypen.  

### <a name="to-set-up-default-dimension-priorities"></a>Sådan oprettes prioritering af standarddimensioner  
Forskellige kontotyper, f.eks. en debitorkonto eller en varekonto, kan have forskellige standarddimensioner angivet. Et resultat heraf er, at en post kan have mere end én standarddimension som forslag til en dimension. For at undgå sådanne konflikter, kan du knytte prioriteringsregler til forskellige kilder.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Prioritering af standarddim.**, og vælg derefter det relaterede link.  
2.  På siden **Prioritering af standarddim.** i feltet **Kildekode** skal du indtaste kildekoden for den posteringstabel, som standarddimensionsprioriteterne skal gælde for.  
3.  Udfyld en linje for hver standarddimensionsprioritet som du ønsker for det valgte kildespor.
4.  Gentag denne fremgangsmåde for hvert kildespor, du vil standarddimensionsprioriteter til.  

> [!IMPORTANT]  
>  Hvis du har oprettet to tabeller med samme prioritering for samme kildespor, vælger [!INCLUDE[prod_short](includes/prod_short.md)] altid tabellen med den laveste tabel-id.  

### <a name="to-set-up-dimension-combinations"></a>Sådan oprettes kombinationer af dimensioner  
For at undgå bogføringsposter med modstridende eller irrelevante dimensioner kan du blokere eller begrænse bestemte kombinationer af to dimensioner. Hvis en dimensionskombination er blokeret, kan du ikke bogføre dimensionerne i samme post, uanset hvad dimensionsværdierne er. En begrænset dimensionskombination tillader bogføring af begge dimensioner i samme post, men kun med visse kombinationer af dimensionsværdier.

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Dimensionskombinationer**, og vælg derefter det tilknyttede link.  
2.  På siden **Dimensionskombinationer** skal du vælge feltet med dimensionskombinationen og vælge en af følgende indstillinger.  

    |Felt|Beskrivelse|
    |----------------------------------|---------------------------------------|  
    |**Ingen begrænsninger**|Denne dimensionskombination har ingen begrænsninger. Alle dimensionsværdier er tilladt.|  
    |**Begrænset**|Denne dimensionskombination har begrænsninger, der afhænger af, hvilke dimensionsværdier du angiver. Du skal angive begrænsningerne på siden **Dimensionsværdikombination**.|  
    |**Spærret**|Denne dimensionskombination er ikke tilladt.|  

3.  Hvis du valgte indstillingen **Begrænset**, skal du definere, hvilke dimensionsværdikombinationer, der er blokeret. For at gøre dette skal du vælge feltet for at definere dimensionskombinationen.  
4.  Vælg herefter en dimensionsværdikombination som er blokeret og skriv **Blokeret** i feltet. Et tomt feltet betyder, at dimensionsværdikombinationen er tilladt. Gentag hvis flere kombinationer er blokerede.  

> [!NOTE]  
>  De samme dimensioner vises i både rækker og kolonner, og derfor vises alle dimensionskombinationer to gange. [!INCLUDE[prod_short](includes/prod_short.md)] viser automatisk indstillingen i begge felter. Du kan ikke vælge noget i felterne fra øverste venstre hjørne og nedefter, fordi disse felter har samme dimension i både rækker og kolonner.  
>   
>  Den valgte indstilling kan ikke vises, før du forlader feltet.  
>   
>  Hvis du vil have vist navnet på dimensionen i stedet for koden, skal du markere feltet **Vis kolonnenavn**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Sådan oprettes globale dimensioner og genvejsdimensioner
Globale dimensioner og genvejsdimensioner kan bruges som filter overalt i [!INCLUDE[prod_short](includes/prod_short.md)], herunder i rapporter, kørsler, ældre poster og analysevisninger. Globale dimensioner og genvejsdimensioner er altid tilgængelige, så de kan indsættes direkte, uden at siden **Dimensioner** først skal åbnes. På kladde- og dokumentlinjer kan du vælge globale dimensioner og genvejsdimensioner i et felt på linjen. Du kan også oprette to globale dimensioner og otte genvejsdimensioner. Vælg de dimensioner, du oftest benytter.

> [!Important]  
> Hvis du ændrer en global dimension eller en genvejsdimension, kræver det, at alle poster bogført med dimensionen er opdateret. Du kan ændre en global dimension med funktionen **Rediger globale dimensioner**, men det kan være tidskrævende og kan påvirke ydeevnen, og tabellerne er muligvis låst under opdateringen. Derfor skal du vælge de globale dimensioner og genvejsdimensioner omhyggeligt, så du ikke behøver at ændre dem senere. Hvis du vil ændre en genvejsdimension, skal du bruge handlingen **Rediger dimensioner**. <br /><br />
> Du kan finde flere oplysninger i [Sådan ændres globale dimensioner](finance-dimensions.md#to-change-global-dimensions).

> [!Note]
> Når du tilføjer eller ændrer en global dimension eller genvejsdimension, logges du automatisk ud og ind igen, så den nye værdi er forberedt til brug.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af Finans**, og vælg derefter det relaterede link.
2. Udfyld felterne i oversigtspanelet **Dimensioner**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Sådan ændres globale dimensioner
Når du ændrer en global dimension eller en genvejsdimension, opdateres alle poster, som er bogført i den pågældende dimension. Da denne proces kan være tidskrævende og kan påvirke ydeevnen, kan processen tilpasses databasens størrelse ved hjælp af to forskellige tilstande.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af Finans**, og vælg derefter det relaterede link.
2. Vælg handlingen **Rediger globale dimensioner**.
3. Øverst på siden skal du vælge en af følgende indstillinger for at definere, i hvilken tilstand batchjobbet skal køres.

    |Indstilling|Description|
    |-|-|
    |**Fortløbende**|(Standard) Hele dimensionsændringen udføres med én transaktion, der tilbagefører alle poster til de dimensioner, som de havde før ændringen.<br /><br />Denne indstilling anbefales, hvis virksomheden har forholdsvis få bogførte poster, hvor det vil tage den korteste tid at færdiggøre. Processen låser flere tabeller og blokerer andre brugere, indtil den er færdig. Bemærk: Processen kan muligvis slet ikke fuldføres i denne tilstand i store databaser. Hvis det er tilfældet, skal du bruge indstillingen **Parallel**.|
    |**Parallel**|Dimensions ændringen foregår i flere baggrundssessioner, og operationen deles op i flere transaktioner. Hvis du vil bruge denne indstilling, skal du slå **Parallel behandling** til/fra . <br /><br />Denne indstilling anbefales til store databaser eller virksomheder med mange bogførte poster, hvor det vil tage den korteste tid at færdiggøre. Bemærk: Denne opdateringsproces starter ikke med denne tilstand, hvis der er mere end én aktiv databasesession.|  

4. Indtast de nye dimensioner i felterne **Global dimension 1-kode** og/eller **Global dimension 2-kode**. De aktuelle dimensioner vises som grå bag felterne.
5. Benyt en af følgende fremgangsmåder afhængigt af tilstanden:
    * Vælg handlingen **Start** i tilstanden **Sekventiel**.
    * Vælg handlingen **Klargør** i tilstanden **Parallel**.

    Fanen **Logposter** er udfyldt med oplysninger om de dimensioner, der vil blive ændret.
7. Log ud af [!INCLUDE[prod_short](includes/prod_short.md)], og log på igen.
8. Vælg handlingen **Start** for at begynde parallel behandling af dimensionsændringer. <!--is this also dependent on the mode?-->

### <a name="example-of-dimension-setup"></a>Eksempel på dimensionsopsætning
Lad os antage, at dit firma vil kunne spore transaktioner baseret på virksomhedens struktur og geografiske placeringer. Til det formål kan du oprette to dimensioner på siden **Dimensioner**:

* **OMRÅDE**  
* **AFDELING**  

| Kode | Name | Kodetekst | Filtertekst |
| --- | --- | --- | --- |
| OMRÅDE |Område |Områdekode |Områdefilter |
| AFDELING |Afdeling |Afdelingskode |Afdelingsfilter |

For **OMRÅDE** tilføjer du følgende dimensionsværdier:

| Kode | Name | Dimensionsværditype |
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

For de to vigtigste geografiske områder, Nord- og Sydamerika og Europa, tilføjer du underkategorier for områder ved at indrykke dimensionsværdierne. Derved kan du rapportere salg eller udgifter i områder, og få vist totaler for større geografiske områder. Du kan også vælge at bruge lande eller områder som dimensionsværdier, eller områder eller byer, afhængigt af din virksomhed.

> [!NOTE]  
>   Hvis du vil oprette et hierarki, skal koderne være i alfabetisk orden. Dette omfatter koderne for de dimensionsværdier, der er angivet i [!INCLUDE[prod_short](includes/prod_short.md)].  

For **AFDELING** tilføjer du følgende dimensionsværdier:

| Kode | Name | Dimensionsværditype |
| --- | --- | --- |
| ADMIN |Opsætning |Standard |
| PROD |Produktion |Standard |
| SALG |Salg |Standard |

Med denne opsætning kan du tilføje dine to dimensioner som de to globale dimensioner på siden **Opsætning af Finans**. Det betyder, at du kan bruge OMRÅDE og AFDELING som filtre til finansposter samt i rapporter og kontoskemaer. Begge globale dimensioner kan også bruges som genvejsdimensioner på postlinjer og i bilagshoveder.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Få et overblik over dimensioner, der bruges flere gange
Siden **Standarddimensioner - flere** angiver, hvordan en gruppe af konti bruger dimensioner og dimensionsværdier. Det kan du gøre ved at markere flere konti og derefter angive standarddimensioner og dimensionsværdier for alle de konti, du har markeret i kontooversigten. Når du har angivet standarddimensioner for de markerede konti, foreslår programmet, at de samme dimensioner og dimensionsværdier benyttes, hver gang en af disse konti benyttes, f.eks. på en kladdelinje. Det gør det nemmere for brugeren at bogføre poster, eftersom felterne med dimensioner udfyldes automatisk. Det er dog muligt manuelt at ændre de dimensionsværdier, der bliver foreslået, eksempelvis på kladdelinjer.

Siden **Standarddimensioner-flere** indeholder følgende felter:

|Felt|Beskrivelse|
|-----|-----------|  
|**Dimensionskode**|Viser alle de dimensioner, der har været defineret som standarddimensioner for en eller flere af de markerede konti. Hvis du klikker på feltet, får du vist en oversigt over alle tilgængelige dimensioner. Hvis du markerer en dimension og klikker på OK, bliver den valgte dimension defineret som standarddimension for alle de markerede konti.|
|**Dimensionsværdikode**|Viser enten en enkelt dimensionsværdi eller ordet (Konflikt). Hvis feltet indeholder en dimensionsværdi, har alle markerede konti den samme standarddimensionsværdi for en dimension. Hvis der står (Konflikt) i feltet, så er det ikke alle de markerede konti, der har den samme standarddimensionsværdi for en dimension. Hvis du klikker på feltet, får du vist en oversigt over alle de dimensionsværdier, der kan benyttes i forbindelse med en dimension. Hvis du markerer en dimensionsværdi og klikker på OK, bliver den markerede dimensionsværdi defineret som standarddimensionsværdi for alle de markerede konti.|
|**Værdibogføring**|Viser enten en enkelt værdibogføringsregel eller ordet (Konflikt). Hvis der vises en værdibogføringsregel i feltet, så har alle markerede konti den samme værdibogføringsregel for en dimensionsværdi. Hvis der står (Konflikt) i feltet, så er det ikke alle de markerede konti, der har den samme værdibogføringsregel for en dimensionsværdi. Hvis du klikker på feltet Værdibogføring, får du vist en liste med værdibogføringsregler. Hvis du markerer en værdibogføringsregel, bliver den anvendt på alle de markerede konti.|

## <a name="using-dimensions"></a>Bruge dimensioner
I et dokument, f.eks en salgsordre, kan du tilføje dimensionsoplysninger for en individuel dokumentlinje og for selve dokumentet. På siden **Salgsordre** kan du f.eks. angive dimensionsværdier for de første to genvejsdimensioner på de enkelte salgslinjer, og du kan tilføje flere dimensionsoplysninger, hvis du vælger knappen **Dimensioner**.  

Hvis du i stedet arbejder i en kladde, kan du tilføje dimensionsoplysninger til en post på samme måde, hvis du har oprettet genvejsdimensioner som felter direkte på kladdelinjer.  

Du kan angive standarddimensioner for konti eller kontotyper, så dimensioner og dimensionsværdier udfyldes automatisk.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Sådan får du vist globale dimensioner på sider med poster  
Globale dimensioner er altid virksomheds\-defineret og navngivet efter virksomheden. Du kan se de globale dimensioner for dit regnskab ved at åbne siden **Regnskabsopsætning**.  

Du kan se, om der er globale dimensioner for poster, når du åbner en side med poster. De to globale dimensioner adskiller sig fra resten af dimensionerne, fordi du kan bruge dem som filtre overalt i [!INCLUDE[prod_short](includes/prod_short.md)].  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoplan**, og vælg derefter det relaterede link.  
2.  På siden **IC-kontoplan** skal du vælge handlingen **Poster**.  
3.  Angiv et eller flere filtre, så du kun får vist de relevante poster på siden.  
4.  Hvis du vil have vist alle dimensioner for en post, skal du vælge den og derefter vælge handlingen **Dimensioner**.  

> [!NOTE]  
>  Siden **Postdimensioner** viser dimensioner for en post ad gangen. Når du ruller gennem finansposter, ændres indholdet på siden **Postdimensioner** løbende.

## <a name="troubleshooting-dimensions-errors"></a>Fejlfinding af dimensioner
Når du bogfører dokumenter eller kladdelinjer, der indeholder dimensioner, kan der opstå flere fejl, der typisk vedrører forkert dimensionsopsætning eller -tildeling.

> [!NOTE]
> På følgende liste over mulige fejlmeddelelser er *%X*-koder pladsholdere for de datavariabler, som findes i den aktuelle meddelelse i brugergrænsefladen afhængig af konteksten. *%1 %2 er f.eks. spærret.* Kan vises i brugergrænsefladen som "Dimensionskode AREA er spærret.".  

|Udsted|Fejlmeddelelse|Mulig løsning|
|-----|-------------|-----------------|
|Spærret dimension|%1 %2 er spærret.|– Find ikke-bogførte bilag, der indeholder dimensionsgruppen med den dimension, der er spærret, og fjern spærringen.<br />– Fjern dimensionsgruppelinjen for den dimension, der er spærret.|
|Slettet dimension|%1 %2 blev ikke fundet.|– Gendan den manglende dimension.<br />– Find ikke-bogførte bilag, der indeholder dimensionsgruppen med den manglende dimension, og tilføj den.<br />– Fjern dimensionsgruppelinjen for den manglende dimension.|
|Spærret dimensionsværdi|%1 %2 - %3 er spærret.|– Find ikke-bogførte bilag, der indeholder dimensionsgruppen med den dimensionsværdi, der er spærret, og fjern spærringen.<br />– Fjern dimensionsgruppelinjen for den dimensionsværdi, der er spærret.|
|Slettet dimensionsværdi|    %1 for %2 mangler.|– Gendan den manglende dimensionsværdi.<br />– Find ikke-bogførte bilag, der indeholder dimensionsgruppen med den manglende dimensionsværdi, og tilføj den.<br />– Fjern dimensionsgruppelinjen for den manglende dimensionsværdi.|
|Forbudt dimensionsværdi|Dimensionsværditypen for %1 %2 - %3 må ikke være %4.|– Ret feltet **Dimensionsværditype** på siden **Dimensionsværdier** til **Standard** eller **Fra-sum**.<br />– Fjern dimensionsgruppelinjen for den dimensionsværdi, der er spærret.|
|Spærret dimensionskombination|Dimensionerne %1 og %2 kan ikke bruges samtidig.|– Find ikke-bogførte bilag, der indeholder dimensionsgruppen med den dimensionskombination, der er spærret, og fjern spærringen.<br />– Ret en af de modstridende linjer i rettighedssæt for dimensionskombinationen.|
|Spærret dimensionsværdikombination|Dimensionskombinationerne %1 - %2 og %3 - %4 kan ikke bruges samtidig.|– Find ikke-bogførte bilag, der indeholder dimensionsgruppen med den dimensionsværdikombination, der er spærret, og fjern spærringen.<br />– Ret en af de modstridende linjer i rettighedssæt for dimensionsværdikombinationen.|
|Tom dimensionsværdikode for standarddimensionen hvor feltet **Værdibogføring** indeholder **Tvungen kode**|– Angiv %1 for %2 %3.<br />– Vælg %1 til %2 %3 for %4 %5.|– Ret feltet **Værdibogføring** på siden **Standarddimension**.<br />– Angiv en ikke-tom dimensionsværdi for den modstridende dimension i dimensionsgruppen.|
|Forkert dimensionsværdikode for standarddimensionen hvor feltet **Værdibogføring** indeholder **Samme kode**|– Vælg %1 %2 til %3 %4.<br />– Vælg %1 %2 til %3 %4 for %5 %6|– Ret feltet **Værdibogføring** på siden **Standarddimension**.<br />– Angiv den krævede dimensionsværdi for den modstridende dimension i dimensionsgruppen.|
|Ikke-tom dimensionsværdikode for tom standarddimension hvor feltet **Værdibogføring** indeholder **Samme kode**|– %1 %2 skal være tom.<br />– %1 %2 skal være tom for %3 %4.|– Ret feltet **Værdibogføring** på siden **Standarddimension**.<br />– Angiv en tom dimensionsværdikode for den modstridende dimension i dimensionsgruppen.|
|Uventet dimensionsværdi for standarddimensionen hvor feltet **Værdibogføring** indeholder **Ingen kode**|– %1 %2 må ikke angives.<br />– %1 %2 må ikke angives for %3 %4|– Ret feltet **Værdibogføring** på siden **Standarddimension**.<br />– Fjern den uoverensstemmende linje fra dimensionsgruppen.|
|En dimensionsrettelse fuldføres ikke korrekt.||-Vælg **Nulstil** for at føre rettelsen tilbage til en kladdetilstand. Derved nulstilles ændringerne, og du kan udføre rettelsen igen.|

## <a name="changing-dimension-assignments-after-posting"></a>Ændring af dimensionstildelinger efter bogføring
Hvis du opdager, at der er anvendt en ukorrekt dimension på bogførte finansposter, kan du rette dimensionsværdierne og opdatere dine analysevisninger. På den måde kan du lettere sikre, at dine finansrapporter og analyser bliver nøjagtige.

### <a name="setting-up-dimension-corrections"></a>Opsætning af dimensionsrettelser
Du skal overveje to ting, når du opsætter dimensionsrettelser:

* Er der dimensioner, som du ikke vil give brugere tilladelse til at ændre? På siden **Indstillinger for dimensionsrettelser** skal du angive de dimensioner, som du vil spærre for ændringer.
* Hvem vil du tillade at ændre dimensioner? Hvis du vil tillade, at brugere foretager ændringer, skal du tildele brugerne tilladelsen **D365 DIM CORRECTION**. Med tilladelserne lader du brugerne oprette dimensionsrettelser, køre dem og fortryde dem, hvis det er nødvendigt. De kan også angive spærrede dimensioner. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md). 

### <a name="correcting-a-dimension"></a>Rettelse af en dimension
Du kan manuelt vælge en eller flere finansposter, eller du kan bruge filtre til at vælge sæt af poster. Hvis det er nødvendigt, kan du også tilføje eller slette dimensioner. 

1. Hvis du vil starte en dimensionsrettelse, skal du bruge én af følgende sider:

* Vælg en journal og derefter handlingen **Ret dimensioner** på siden **Finansjournal**. Dermed startes en rettelse af posterne i den valgte journal.
* Vælg handlingen **Dimensionsrettelse** på siden **Finansposter**. 

2. Angiv oplysninger om ændringen i feltet **Beskrivelse**. Andre brugere kan bruge disse oplysninger senere til at forstå, hvad der er udført.
3. Vælg de relevante poster I oversigtspanelet **Valgte finansposter**.

> [!IMPORTANT]
> Når du ændrer en valg, nulstilles værdierne i oversigtspanelet **Ændringer i dimensionsrettelser**. Du skal derfor altid vælge posterne, før du angiver ændringer af dimensionsværdierne.

   Den følgende tabel beskriver indstillingerne.

   |Indstilling  |Description  |
   |---------|---------|
   |Tilføje relaterede poster     |Tilføj finansposter, der er i den samme finansjournal.|   
   |Tilføje efter filter     |Brug filterkriterier, når du tilføjer finansposter.|
   |Manuelt valg     |Vælg specifikke finansposter.         |
   |Tilføje efter dimensioner     |Filtrer finansposter efter dimensioner.         |
   |Fjerne poster     |Fjern markering af finansposter.         |
   |Administrere valgkriterier     |Hold styr på valgprocessen, og fortryd valg, hvis det er nødvendigt.         |

4. Vælg den dimension, du vil ændre i feltet **Dimensionskode** i oversigtspanelet **Ændringer i dimensionsrettelser**, og vælg den nye værdi i feltet **Ny dimensionsværdikode**.
5. Hvis du vil validere rettelsen, skal du vælge **Valider dimensionsændringer**. Du kan finde flere oplysninger i [Validering af dimensionsrettelser](finance-dimensions.md#validating-dimension-corrections).
6. Vælg **Kør**.

### <a name="validating-dimension-corrections"></a>Validering af dimensionsrettelser
Før du foretager en rettelse, er det en god ide at validere den først. Validering kontrollerer, om der er begrænsninger for værdibogføring på finanskonti, begrænsninger for dimensioner, og om dimensionsværdierne er spærrede. Under valideringen angives status for rettelsen til **Validering i gang**. Når du validerer en rettelse, vises resultatet i feltet **Valideringsstatus**. Hvis der er fundet fejl, kan du bruge handlingen **Vis fejl** for at undersøge dem nærmere. Når du har rettet en fejl, skal du bruge handlingen **Genåbn** for at udføre rettelsen eller en ny validering.

Du kan enten udføre en rettelse med det samme eller planlægge, at den skal udføres senere. Hvis du udfører rettelser i et stort datasæt, anbefales det, at du planlægger at udføre dem uden for normal arbejdstid. Du kan finde flere oplysninger i [Dimensionsrettelser i store datasæt](finance-dimensions.md#dimension-corrections-on-large-data-sets).

### <a name="undoing-a-correction"></a>Annullering af en rettelse
Når du har rettet en dimension, kan du bruge handlingen **Fortryd** til at nulstille den tidligere værdi, hvis du ikke bryder dig om, hvad du ser. Du kan dog kun annullere den seneste rettelse. Før du annullerer en rettelse, kan du validere de ændringer, som annulleringen foretager. Dette er f.eks. nyttigt, hvis dimensionsbegrænsningerne er blevet ændret efter udførelsen af rettelsen.

Hvis handlingen Fortryd ikke er tilgængelig, f.eks. fordi du har udført mange rettelser, kan du bruge handlingen **Kopier til kladde** for at starte en ny rettelse i de samme poster.

### <a name="dimension-corrections-on-large-data-sets"></a>Dimensionsrettelser i store datasæt
Vær forsigtig, når du retter store sæt poster, f.eks. et sæt, der indeholder mere end 10.000 poster. Hvis du kan, anbefales det, at du bruger filtrene til at udføre rettelserne på mindre sæt af data. Det er også en god ide at udføre rettelser uden for normal åbningstid. 

### <a name="using-analysis-views-with-dimension-corrections"></a>Brug af analysevisninger med dimensionsrettelser
Hvis **Opdatering af bogføring** er aktiveret for en analysevisning, kan [!INCLUDE[prod_short](includes/prod_short.md)] vise, hvornår dokumenter og kladder er bogført. Du kan også opdatere visninger med resultater af dimensionsrettelser, når denne indstilling er aktiveret. Hvis du vil gøre det, skal du slå til/fra-knappen for **Opdater analysevisninger** til. Hvis du opdaterer analysevisninger, kan det påvirke ydeevnen, især for store datasæt. Derfor anbefales det, at du kun opdaterer analysevisninger for små datasæt.  

### <a name="viewing-historical-dimension-corrections"></a>Visning af historiske dimensionsrettelser
Hvis en finanspost er blevet rettet, kan du undersøge ændringen ved at bruge handlingen **Oversigt over dimensionsrettelser**.

### <a name="handling-incomplete-corrections"></a>Håndtering af ufuldstændige rettelser
Hvis en rettelse ikke fuldføres, vises der en advarsel på rettelseskortet. Hvis det sker, kan du bruge handlingen **Nulstil** til at annullere rettelsen til en kladdestatus og annullere ændringerne. Derefter kan du udføre rettelsen igen.

> [!NOTE]
> Nulstilling af en ufuldstændig rettelse påvirker ikke opdateringer af analysevisninger, fordi de sker i slutningen af rettelsesprocessen.

### <a name="using-cost-accounting-with-corrected-gl-entries"></a>Brug af omkostningsregnskab med rettede finansposter
Når du har rettet dimensionerne vil dine data til omkostningsregnskabet ikke være synkroniserede. Omkostningsregnskabet bruger dimensioner til at samle beløb for omkostningssteder og omkostningsemner og udføre omkostningsfordelinger. Ændring af dimensioner for finansposter vil det sandsynligvis betyde, at du skal køre dine omkostningsregnskabsmodeller igen. Uanset om du bare har brug for at slette nogle få omkostningsregistre og udføre fordelinger igen, eller du vil slette alle dine modeller, afhænger af de data, der er blevet opdateret, og hvordan funktionerne til omkostningsregnskabet er konfigureret. Identifikation af, hvor dimensionsrettelser vil påvirke omkostningsregnskabet, og hvor opdateringer er nødvendige, er en manuel proces. I øjeblikket kan [!INCLUDE[prod_short](includes/prod_short.md)] ikke udføre denne proces automatisk.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Analysere data efter dimensioner](bi-how-analyze-data-dimension.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]