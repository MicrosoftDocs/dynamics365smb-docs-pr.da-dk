---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ed62e60d3b5b1af2158d8adc6c411884ea4c12aa
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133572"
---
Når alle varer er indsat som linjer, kan du beregne fakturarabatten for hele salgsdokumentet ved at vælge handlingen **Beregn fakturarabat**.

Rabatten er beregnet baseret på samtlige linjer i salgsdokumentet for de varer, hvor der står **Ja** i feltet **Beregn fakturarabat** på salgsordrelinjen. Dette er standardindstillingen for varer. Linjer med varegebyrer er f.eks. ikke medtaget i beregningen af fakturarabatten. Hvis du vil anvende en rabat på disse linjer, skal du angive feltet **Linjerabat i %** på de relevante linjer.  

> [!TIP]
> Hvis feltet **Beregn fakturarabat** er markeret i vinduet **Salgsopsætning**, beregnes fakturarabatten automatisk, når du gør ét af følgende på salgsdokumentet:
>
> * Vis statistik
> * Vis a kontrolrapport
> * Udskriv
> * Post

Fakturarabatbetingelserne for en debitor defineres på siden **Deb./fakturarabat** for debitoren. Desuden anvendes valutakoden på salgsdokumentet til at fastsætte fakturarabatbetingelserne i den tilsvarende valuta.

Hvis der ikke er defineret fakturarabatter i udenlandske valutaer, bliver fakturarabatbetingelserne for den relevante valuta, der er defineret i tabellen **Deb./fakt.rabat** med beløbene i den lokale valuta, og kursen pr. bogføringsdatoen på salgsdokumentet bruges automatisk til at beregne fakturarabatten i udenlandsk valuta.
