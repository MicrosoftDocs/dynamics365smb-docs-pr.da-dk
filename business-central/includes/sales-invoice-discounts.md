---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035777"
---
Når alle varer er indsat på salgsordrelinjerne, kan du beregne fakturarabatten for det samlede salgsdokument ved at vælge Handlinger og derefter vælge **Beregn fakturarabat**.

Hvis feltet **Beregn fakturarabat** er markeret i vinduet **Salgsopsætning**, beregnes fakturarabatten automatisk, når du gør ét af følgende på salgsdokumentet:

* Vis statistik
* Vis a kontrolrapport
* Udskriv
* Post

Rabatten er fordelt på samtlige linjer i salgsdokumentet for de varer, hvor der står **Ja** i feltet **Beregn fakturarabat** på salgsordrelinjen. Dette er standardindstillingen for varer.

Fakturarabatbetingelserne defineres på siden **Deb./fakturarabat**, hvor fakturarabatten beregnes. Desuden anvendes valutakoden på salgsdokumentet til at fastsætte fakturarabatbetingelserne i den tilsvarende valuta.

Hvis der ikke er defineret fakturarabatter i udenlandske valutaer, bliver fakturarabatbetingelserne for den relevante valuta, der er defineret i tabellen **Deb./fakt.rabat** med beløbene i den lokale valuta, og kursen pr. bogføringsdatoen på salgsdokumentet bruges automatisk til at beregne fakturarabatten i udenlandsk valuta.
