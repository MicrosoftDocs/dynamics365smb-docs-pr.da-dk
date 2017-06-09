---
title: Oprette dimensioner | Microsoft Docs
description: "Du kan definere de dimensioner og dimensionsværdier, du vil bruge til at kategorisere kladder og dokumenter, f.eks. salgsordrer og indkøbsordrer."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/28/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0da77c5be3b49f715384752ad61fc072aea8525c
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-dimensions"></a>Oprette dimensioner
Du kan definere dimensioner og dimensionsværdier for at kategorisere kladder og dokumenter, f.eks. salgsordrer og indkøbsordrer. Du kan oprette dimensioner i vinduet **Dimensioner**, hvor du opretter én linje for hver dimension, f.eks. *Projekt*, *Afdeling*, *Område* og *Sælger*.

Du kan også angive værdier for dimensioner. Værdier kan f.eks. være afdelinger i virksomheden. Dimensionsværdierne kan oprettes i en hierarkisk struktur - ligesom kontoplanen - så data kan opdeles i forskellige granularitetsniveauer, og dimensionsdelmængder kan lægges sammen. Du kan angive det antal dimensioner og dimensionsværdier, som du har brug for, og de kan bruges af alle i virksomheden.

Du kan også oprette nogle globale dimensioner og genvejsdimensioner:  

* **Globale dimensioner** bruges som filtre, f.eks. i rapporter og kørsler. Du kan kun bruge to globale dimensioner, så vælg dimensioner, du bruger ofte.
* **Genvejsdimensioner** er tilgængelige som felter på kladde- og dokumentlinjer. Du kan oprette op til seks af disse.  

**Bemærk**: Denne funktion kræver, at oplevelsen er indstillet til **Pakke**. Du kan finde flere oplysninger i [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Oprette standarddimensioner for kunder, leverandører og andre konti
Du kan tildele en standarddimension for en specifik konto. Dimensionen kopieres til kladden eller dokumentet, når du angiver kontonummeret på en linje, men du kan slette og ændre koden på linjen, hvis det er relevant. Du kan også oprette en dimension, der kræves til bogføring af en post med en bestemt type konto.  

## <a name="translate-the-names-of-dimensions"></a>Oversætte navnene på dimensioner
Når du opretter en dimension, og især en genvejsdimension, opretter du faktisk en brugerdefineret felt- eller kolonneoverskrift. Hvis din virksomhed er international, kan du angive oversættelser af navnet på dimensionen. Dokumenter, som indeholder dimensionen, bruger det oversatte navn, hvis det er relevant.   

## <a name="example"></a>Eksempel
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
**Bemærk!** Hvis du vil oprette et hierarki, skal koderne være i alfabetisk orden. Dette omfatter koderne for de dimensionsværdier, der er angivet i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

For **AFDELING** tilføjer du følgende dimensionsværdier:

| Kode | Name | Dimensionsværditype |
| --- | --- | --- |
| ADMIN |Opsætning |Standard |
| PROD |Produktion |Standard |
| SALG |Salg |Standard |

Med denne opsætning tilføjer du derefter to dimensioner som de to globale dimensioner i vinduet **Opsætning af Finans**. Det betyder, at du kan bruge OMRÅDE og AFDELING som filtre til finansposter samt i rapporter og kontoskemaer. Begge globale dimensioner kan også bruges som genvejsdimensioner på postlinjer og i bilagshoveder.  

Med denne opsætning kan du begynde at føje dimensioner til dokumenter og kladder. Du kan finde flere oplysninger under [Dimensioner](finance-dimensions.md).  

## <a name="see-also"></a>Se også
[Dimensioner](finance-dimensions.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

