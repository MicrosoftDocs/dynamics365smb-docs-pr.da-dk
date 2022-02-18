---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e75327e1c87af593d8e3f7e4f95e74349fb3a63c
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104066"
---
I følgende tabel beskrives nogle af nøglerapporterne i kreditorrapporter.

| Report | Objekt-id | Beskrivlse |
|--|--|--|
| **Aldersfordelte tilgodehavender** | 120 | Viser det udestående beløb med debitorer fordelt på tids intervaller for den overskredne tid. Rapporten viser også den del af debitor balancen, der ikke er forfaldne, og som kan vises med eller uden dokumentoplysninger for hver debitor. Denne rapport er den hovedrapport, der bruges til at afstemme debitorposter med finansmodulet. Hvis du ikke har tilladt at bogføre på de konti, der bruges i debitorbogføringsgruppens debitorkonto, er denne rapport en specifikation af de beløb, som du finder i finansregnskabet. |
| **Kontoudtog** | 1316 | Opretter et kundekontoudtog inden for et bestemt tidsinterval. Den sendes som regel til kunderne, så de kan få et overblik over de udestående beløb og også som rykker for at betale forfaldne beløb. Du kan vælge at få vist de forfaldne beløb i en separat sektion. Du kan medtage et aldersfordelingsinterval, der svarer til den, der bruges i rapporten over **Aldersfordelte tilgodehavender**. For det aldersfordelte bånd skal du typisk angive *30D*, hvilket betyder 30 dages mellemrum, f. eks. as30, 60, 90 og 90 + dage overskredet, fra slutdatoen eller *1m + cm*, som er den aktuelle måned i et separat interval og derefter månedlige intervaller for de foregående måneder. **Bemærk**: På debitorlisten har denne rapport også en særskilt aktion, **Planlagte kontoudtog**. Denne indstilling filtrerer ikke til den kunde, du har valgt. Det er den samme rapport, men bruges, når du vil sende en opgørelse til alle/flere debitorer. |
| **Debitor - saldo til dato** | 121 | Viser de åbne debitorposter indtil slutdatoen. Rapporten viser det samme indhold som kundens kontoudtog, men uden angivelse af, om posten er forfalden. **Bemærk**: Der anvendes et datofilter på de detaljerede debitorposter. Det betyder, at hvis du har betalinger, der er senere end slutdatoen, der er blevet udlignet med fakturaer inden for datointervallet, vises fakturaerne i rapporten, da de ikke er blevet lukket på samme måde som slutdatoen. |
| **Debitor - balance** | 129 | Viser bevægelserne på debitorerne for den periode, der er angivet i datofilteret, sammen med nettoændringen år-til-dato for det regnskabsår, der svarer til den valgte periode. Rapporten er grupperet efter debitorbogføringsgrupper og giver en anden oversigt over debitorposter end rapporten **Aldersfordelte tilgodehavender**. **Bemærk**: Hvis du ikke har oprettet en regnskabsperiode, vil systemet ikke vide, hvilket regnskabsår du skal bruge, og du skal enten få vist år-til-dato fra det seneste regnskabsår, der er defineret, eller blot vælge perioden, som kan være fra begyndelsen af et år.|
| **Debitor - Detaljeret råbalance** | 104 | Viser alle debitorposter inden for det angivne datofilter. Denne rapport bruges som regel til at kontrollere, at alle poster for en bestemt kunde er konto til, eller om der sker en anden intern kontrol af debitorposter. |
| **Debitor - betalingskvittering** | 211 | Opretter en betalingskvittering for hver debitorpost af typen **Betaling**. Hvis betalingen er udlignet med fakturaer, angives fakturaerne. ellers vil den blot angive, at betalingsbeløbet skal være ikke-udlignet. Denne rapport bruges til at sende til kunder, der vil have dokumentation for modtagelsen af betalingen.|
| **Afstem debitor- og kreditorkonti** | 33 |Viser finansposterne fra bogføring af debitor-og kreditorposter opdelt pr. finanskonto og bogføringsgrupper. Denne rapport bruges til afstemning af saldi på debitor-og kreditorkonti til Finans saldi. |
| **Debitor - aldersfordelt saldo**| 109 |Dette er en ældre version af en rapport med aldersfordelt tilgodehavender. Det anbefales, at du i stedet bruger rapporten **Aldersfordelte tilgodehavender**. |
| **Salgsstatistik** |112  |[!INCLUDE [reports-sales-statistics](reports-sales-statistics.md)]<br>Denne rapport kan også bruges i tilgodehavender, da det er nemmere at foretage en hurtig søgning efter bogførte betalinger, rabatter og salg for en bestemt debitor.|
|**Debitoroversigt**|101| Viser diverse stamoplysninger, der er knyttet til debitoren, f.eks. debitorbogføringsgruppe, rabatgruppe, rente- og betalingsoplysninger, sælger, debitors basisvaluta, kreditmaksimum i den lokale valuta (RV) og debitorens aktuelle saldo (i RV). Rapporten kan f.eks. bruges til at vedligeholde oplysningerne i tabellen Debitortabel.|
