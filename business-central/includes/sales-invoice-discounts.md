---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470283"
---
Når alle varer er indsat på salgslinjerne, kan du beregne fakturarabatten for det samlede dokument ved at vælge Handlinger og derefter vælge **Beregn fakturarabat**.

Rabatten er beregnet baseret på samtlige linjer i salgsdokumentet for de varer, hvor der står **Ja** i feltet **Beregn fakturarabat** på salgsordrelinjen. Dette er standardindstillingen for varer. Linjer med varegebyrer er f. eks. ikke medtaget i beregningen af fakturarabatten. Hvis du vil anvende en rabat på disse linjer, skal du angive feltet **Linjerabat i %** på de relevante linjer.  

> [!TIP]
> Hvis feltet **Beregn fakturarabat** er markeret i vinduet **Salgsopsætning**, beregnes fakturarabatten automatisk, når du gør ét af følgende på salgsdokumentet:
>
> * Vis statistik
> * Vis a kontrolrapport
> * Udskriv
> * Post

Fakturarabatbetingelserne for en debitor defineres på siden **Deb./fakturarabat** for debitoren. Desuden anvendes valutakoden på salgsdokumentet til at fastsætte fakturarabatbetingelserne i den tilsvarende valuta.

Hvis der ikke er defineret fakturarabatter i udenlandske valutaer, bliver fakturarabatbetingelserne for den relevante valuta, der er defineret i tabellen **Deb./fakt.rabat** med beløbene i den lokale valuta, og kursen pr. bogføringsdatoen på salgsdokumentet bruges automatisk til at beregne fakturarabatten i udenlandsk valuta.
