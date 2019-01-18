---
title: Arbejde med dimensioner | Microsoft Docs
description: "Du kan bruge dimensioner til at kategorisere poster, f.eks. efter afdeling eller projekt, så du nemt kan spore og analysere data."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: ac8d1f84c3daacbee931d559e6f67f4351df73c5
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="working-with-dimensions"></a>Arbejde med dimensioner
For at gøre det lettere at analysere dokumenter som f.eks. salgsordrer kan du bruge dimensioner. Dimensioner er attributter og værdier, der kategoriserer poster, så du kan spore og analysere dem. Dimensioner kan f.eks. angive det projekt eller den afdeling, en post kommer fra.  

I stedet for f.eks. at oprette en særskilt finanskonto til hver afdeling og hvert projekt kan du bruge dimensioner. Det giver en god analysemulighed uden at skulle oprette en kompliceret kontoplan. Du kan finde flere oplysninger i [Business Intelligence](bi.md).

Som et andet eksempel kan du oprette en dimension med navnet *Afdeling* og bruge den, når du bogfører salgsdokumenter. Derved kan du bruge business intelligence-værktøjer til at se, hvilke afdelinger der har solgt hvilke varer.
Jo flere dimensioner, du bruger, jo mere detaljerede rapporter kan du basere forretningsmæssige beslutninger på. F.eks. kan en enkelt salgspost indeholde flere dimensionsoplysninger, f.eks.:  

* Den konto, som varesalget blev bogført på  
* Hvor varen blev solgt
* Hvem, der solgte den
* Hvilken type kunde der købte den  

## <a name="analyzing-by-dimensions"></a>Analyse efter dimensioner
Funktionen Dimensioner spiller en vigtig rolle i business intelligence, f.eks. når du definerer analyser. Du kan finde flere oplysninger under [Analysere data efter dimensioner](bi-how-analyze-data-dimension.md).

> [!TIP]
> For hurtigt at analysere transaktionsdata efter dimensioner kan du filtrere totaler i kontoplanen og poster på alle sider af typen **Poster** efter dimensioner. Kig efter handlingen **Angiv dimensionsfilter**.

## <a name="dimension-sets"></a>Dimensionsgrupper
En dimensionsgruppe er en entydig kombination af dimensionsværdier. Det er gemt som dimensionsgruppeposter i databasen. Hver dimensionsgruppepost repræsenterer en enkelt dimensionsværdi. Dimensionsgruppen er identificeret med en fælles dimensionsgruppe-id, der tildeles til hver dimensionsgruppepost, der hører til dimensionsgruppen.  

Når du opretter en kladdelinje, et nyt bilagshoved eller en ny bilagslinje, kan du angive en kombination af dimensionsværdier. I stedet for at eksplicit at gemme hver dimensionsværdi i databasen, tildeles kladdelinjen, bilagshovedet eller bilagslinjen en dimensionsgruppe-id, der angiver dimensionsgruppen.  

## <a name="setting-up-dimensions"></a>Oprette dimensioner
Du kan definere dimensioner og dimensionsværdier for at kategorisere kladder og dokumenter, f.eks. salgsordrer og indkøbsordrer. Du kan oprette dimensioner på siden **Dimensioner**, hvor du opretter én linje for hver dimension, f.eks. *Projekt*, *Afdeling*, *Område* og *Sælger*.

Du kan også angive værdier for dimensioner. Værdier kan f.eks. være afdelinger i virksomheden. Dimensionsværdierne kan oprettes i en hierarkisk struktur - ligesom kontoplanen - så data kan opdeles i forskellige granularitetsniveauer, og dimensionsdelmængder kan lægges sammen. Du kan angive det antal dimensioner og dimensionsværdier, som du har brug for, og de kan bruges af alle i virksomheden.

Du kan også oprette nogle globale dimensioner og genvejsdimensioner:  

* **Globale dimensioner** bruges som filtre, f.eks. i rapporter og kørsler. Du kan kun bruge to globale dimensioner, så vælg dimensioner, du bruger ofte.
* **Genvejsdimensioner** er tilgængelige som felter på kladde- og dokumentlinjer. Du kan oprette op til seks af disse.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Oprette standarddimensioner for kunder, leverandører og andre konti
Du kan tildele en standarddimension for en specifik konto. Dimensionen kopieres til kladden eller dokumentet, når du angiver kontonummeret på en linje, men du kan slette og ændre koden på linjen, hvis det er relevant. Du kan også oprette en dimension, der kræves til bogføring af en post med en bestemt type konto.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Dimensioner**, og vælg derefter det relaterede link.  
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
>  Hvis du har oprettet to tabeller med samme prioritering for samme kildespor, vælger [!INCLUDE[d365fin](includes/d365fin_md.md)] altid tabellen med den laveste tabel-id.  

### <a name="to-set-up-dimension-combinations"></a>Sådan oprettes kombinationer af dimensioner  
For at undgå bogføringsposter med modstridende eller irrelevante dimensioner kan du blokere eller begrænse bestemte kombinationer af to dimensioner. Hvis en dimensionskombination er blokeret, kan du ikke bogføre dimensionerne i samme post, uanset hvad dimensionsværdierne er. En begrænset dimensionskombination tillader bogføring af begge dimensioner i samme post, men kun med visse kombinationer af dimensionsværdier.

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Dimensionskombinationer**, og vælg derefter det relaterede link.  
2.  På siden **Dimensionskombinationer** skal du vælge feltet med dimensionskombinationen og vælge en af følgende indstillinger.  

    |Felt|Beskrivelse|
    |----------------------------------|---------------------------------------|  
    |**Ingen begrænsninger**|Denne dimensionskombination har ingen begrænsninger. Alle dimensionsværdier er tilladt.|  
    |**Begrænset**|Denne dimensionskombination har begrænsninger, der afhænger af, hvilke dimensionsværdier du angiver. Du skal angive begrænsningerne på siden **Dimensionsværdikombination**.|  
    |**Spærret**|Denne dimensionskombination er ikke tilladt.|  

3.  Hvis du valgte indstillingen **Begrænset**, skal du definere, hvilke dimensionsværdikombinationer, der er blokeret. For at gøre dette skal du vælge feltet for at definere dimensionskombinationen.  
4.  Vælg herefter en dimensionsværdikombination som er blokeret og skriv **Blokeret** i feltet. Et tomt feltet betyder, at dimensionsværdikombinationen er tilladt. Gentag hvis flere kombinationer er blokerede.  

> [!NOTE]  
>  De samme dimensioner vises i både rækker og kolonner, og derfor vises alle dimensionskombinationer to gange. [!INCLUDE[d365fin](includes/d365fin_md.md)] viser automatisk indstillingen i begge felter. Du kan ikke vælge noget i felterne fra øverste venstre hjørne og nedefter, fordi disse felter har samme dimension i både rækker og kolonner.  
>   
>  Den valgte indstilling kan ikke vises, før du forlader feltet.  
>   
>  Hvis du vil have vist navnet på dimensionen i stedet for koden, skal du markere feltet **Vis kolonnenavn**.

### <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Få et overblik over dimensioner, der bruges flere gange
Siden **Standarddimensioner - flere** angiver, hvordan en gruppe af konti bruger dimensioner og dimensionsværdier. Det kan du gøre ved at markere flere konti og derefter angive standarddimensioner og dimensionsværdier for alle de konti, du har markeret i kontooversigten. Når du har angivet standarddimensioner for de markerede konti, foreslår programmet, at de samme dimensioner og dimensionsværdier benyttes, hver gang en af disse konti benyttes, f.eks. på en kladdelinje. Det gør det nemmere for brugeren at bogføre poster, eftersom felterne med dimensioner udfyldes automatisk. Det er dog muligt manuelt at ændre de dimensionsværdier, der bliver foreslået, eksempelvis på kladdelinjer.

Siden **Standarddimensioner-flere** indeholder følgende felter:
|Felt|Beskrivelse|
|----------------------------------|---------------------------------------|  
|**Dimensionskode**|Viser alle de dimensioner, der har været defineret som standarddimensioner for en eller flere af de markerede konti. Hvis du klikker på feltet, får du vist en oversigt over alle tilgængelige dimensioner. Hvis du markerer en dimension og klikker på OK, bliver den valgte dimension defineret som standarddimension for alle de markerede konti.|
|**Dimensionsværdikode**|Viser enten en enkelt dimensionsværdi eller ordet (Konflikt). Hvis feltet indeholder en dimensionsværdi, har alle markerede konti den samme standarddimensionsværdi for en dimension. Hvis der står (Konflikt) i feltet, så er det ikke alle de markerede konti, der har den samme standarddimensionsværdi for en dimension. Hvis du klikker på feltet, får du vist en oversigt over alle de dimensionsværdier, der kan benyttes i forbindelse med en dimension. Hvis du markerer en dimensionsværdi og klikker på OK, bliver den markerede dimensionsværdi defineret som standarddimensionsværdi for alle de markerede konti.|
|**Værdibogføring**|Viser enten en enkelt værdibogføringsregel eller ordet (Konflikt). Hvis der vises en værdibogføringsregel i feltet, så har alle markerede konti den samme værdibogføringsregel for en dimensionsværdi. Hvis der står (Konflikt) i feltet, så er det ikke alle de markerede konti, der har den samme værdibogføringsregel for en dimensionsværdi. Hvis du klikker på feltet Værdibogføring, får du vist en liste med værdibogføringsregler. Hvis du markerer en værdibogføringsregel, bliver den anvendt på alle de markerede konti.|

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
>   Hvis du vil oprette et hierarki, skal koderne være i alfabetisk orden. Dette omfatter koderne for de dimensionsværdier, der er angivet i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

For **AFDELING** tilføjer du følgende dimensionsværdier:

| Kode | Name | Dimensionsværditype |
| --- | --- | --- |
| ADMIN |Opsætning |Standard |
| PROD |Produktion |Standard |
| SALG |Salg |Standard |

Med denne opsætning tilføjer du derefter to dimensioner som de to globale dimensioner på siden **Opsætning af Finans**. Det betyder, at du kan bruge OMRÅDE og AFDELING som filtre til finansposter samt i rapporter og kontoskemaer. Begge globale dimensioner kan også bruges som genvejsdimensioner på postlinjer og i bilagshoveder.  

## <a name="using-dimensions"></a>Bruge dimensioner
I et dokument, f.eks en salgsordre, kan du tilføje dimensionsoplysninger for en individuel dokumentlinje og for selve dokumentet. På siden **Salgsordre** kan du f.eks. angive dimensionsværdier for de første to genvejsdimensioner på de enkelte salgslinjer, og du kan tilføje flere dimensionsoplysninger, hvis du vælger knappen **Dimensioner**.  

Hvis du i stedet arbejder i en kladde, kan du tilføje dimensionsoplysninger til en post på samme måde, hvis du har oprettet genvejsdimensioner som felter direkte på kladdelinjer.  

Du kan angive standarddimensioner for konti eller kontotyper, så dimensioner og dimensionsværdier udfyldes automatisk.

## <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Sådan får du vist globale dimensioner på sider med poster  
Globale dimensioner er altid defineret og navngivet i det overordnede regnskab. Du kan se de globale dimensioner for dit regnskab ved at åbne siden **Regnskabsopsætning**.  

Du kan se, om der er globale dimensioner for poster, når du åbner en side med poster. De to globale dimensioner adskiller sig fra resten af dimensionerne, fordi du kan bruge dem som filtre overalt i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoplan**, og vælg derefter det relaterede link.  
2.  På siden **IC-kontoplan** skal du vælge handlingen **Poster**.  
3.  Angiv et eller flere filtre, så du kun får vist de relevante poster på siden.  
4.  Hvis du vil have vist alle dimensioner for en post, skal du vælge den og derefter vælge handlingen **Dimensioner**.  

> [!NOTE]  
>  Siden **Postdimensioner** viser dimensioner for en post ad gangen. Når du ruller gennem finansposter, ændres indholdet på siden **Postdimensioner** løbende.  

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Analysere data efter dimensioner](bi-how-analyze-data-dimension.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

