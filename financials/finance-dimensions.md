---
title: Arbejde med dimensioner | Microsoft Docs
description: "Du kan bruge dimensioner til at kategorisere poster, f.eks. efter afdeling eller projekt, så du nemt kan spore og analysere data."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/14/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 844668124df1897493737b28383a68a2a0a66d10
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

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

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Suite**. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="analyzing-by-dimensions"></a>Analyse efter dimensioner
Funktionen Dimensioner spiller en vigtig rolle i business intelligence, f.eks. når du definerer analyser. Du kan finde flere oplysninger under [Fremgangsmåde: Analyser data efter dimensioner](bi-how-analyze-data-dimension.md).

> [!TIP]
> For hurtigt at analysere transaktionsdata efter dimensioner kan du filtrere totaler i kontoplanen og poster i alle vinduer af typen **Poster** efter dimensioner. Kig efter handlingen **Angiv dimensionsfilter**.

## <a name="dimension-sets"></a>Dimensionsgrupper
En dimensionsgruppe er en entydig kombination af dimensionsværdier. Det er gemt som dimensionsgruppeposter i databasen. Hver dimensionsgruppepost repræsenterer en enkelt dimensionsværdi. Dimensionsgruppen er identificeret med en fælles dimensionsgruppe-id, der tildeles til hver dimensionsgruppepost, der hører til dimensionsgruppen.  

Når du opretter en kladdelinje, et nyt bilagshoved eller en ny bilagslinje, kan du angive en kombination af dimensionsværdier. I stedet for at eksplicit at gemme hver dimensionsværdi i databasen, tildeles kladdelinjen, bilagshovedet eller bilagslinjen en dimensionsgruppe-id, der angiver dimensionsgruppen.  

## <a name="setting-up-dimensions"></a>Oprette dimensioner
Du kan definere dimensioner og dimensionsværdier for at kategorisere kladder og dokumenter, f.eks. salgsordrer og indkøbsordrer. Du kan oprette dimensioner i vinduet **Dimensioner**, hvor du opretter én linje for hver dimension, f.eks. *Projekt*, *Afdeling*, *Område* og *Sælger*.

Du kan også angive værdier for dimensioner. Værdier kan f.eks. være afdelinger i virksomheden. Dimensionsværdierne kan oprettes i en hierarkisk struktur - ligesom kontoplanen - så data kan opdeles i forskellige granularitetsniveauer, og dimensionsdelmængder kan lægges sammen. Du kan angive det antal dimensioner og dimensionsværdier, som du har brug for, og de kan bruges af alle i virksomheden.

Du kan også oprette nogle globale dimensioner og genvejsdimensioner:  

* **Globale dimensioner** bruges som filtre, f.eks. i rapporter og kørsler. Du kan kun bruge to globale dimensioner, så vælg dimensioner, du bruger ofte.
* **Genvejsdimensioner** er tilgængelige som felter på kladde- og dokumentlinjer. Du kan oprette op til seks af disse.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Oprette standarddimensioner for kunder, leverandører og andre konti
Du kan tildele en standarddimension for en specifik konto. Dimensionen kopieres til kladden eller dokumentet, når du angiver kontonummeret på en linje, men du kan slette og ændre koden på linjen, hvis det er relevant. Du kan også oprette en dimension, der kræves til bogføring af en post med en bestemt type konto.  

### <a name="translating-the-names-of-dimensions"></a>Oversætte navnene på dimensioner
Når du opretter en dimension, og især en genvejsdimension, opretter du faktisk en brugerdefineret felt- eller kolonneoverskrift. Hvis din virksomhed er international, kan du angive oversættelser af navnet på dimensionen. Dokumenter, som indeholder dimensionen, bruger det oversatte navn, hvis det er relevant.   

### <a name="example-of-dimension-setup"></a>Eksempel på dimensionsopsætning
Lad os antage, at dit firma vil kunne spore transaktioner baseret på virksomhedens struktur og geografiske placeringer. Til det formål kan du oprette to dimensioner i vinduet **Dimensioner**:

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
| 2.0 |Nordamerika |Standard |
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

Med denne opsætning tilføjer du derefter to dimensioner som de to globale dimensioner i vinduet **Opsætning af Finans**. Det betyder, at du kan bruge OMRÅDE og AFDELING som filtre til finansposter samt i rapporter og kontoskemaer. Begge globale dimensioner kan også bruges som genvejsdimensioner på postlinjer og i bilagshoveder.  

## <a name="using-dimensions"></a>Bruge dimensioner
I et dokument, f.eks en salgsordre, kan du tilføje dimensionsoplysninger for en individuel dokumentlinje og for selve dokumentet. I vinduet **Salgsordre** kan du f.eks. angive dimensionsværdier for de første to genvejsdimensioner på de enkelte salgslinjer, og du kan tilføje flere dimensionsoplysninger, hvis du vælger knappen **Dimensioner**.  

Hvis du i stedet arbejder i en kladde, kan du tilføje dimensionsoplysninger til en post på samme måde, hvis du har oprettet genvejsdimensioner som felter direkte på kladdelinjer.  

Du kan angive standarddimensioner for konti eller kontotyper, så dimensioner og dimensionsværdier udfyldes automatisk.

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Fremgangsmåde: Analysere data efter dimensioner](bi-how-analyze-data-dimension.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

