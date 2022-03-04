---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c2f5f4c264150802920169139c90c0456f9a27c4
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/23/2022
ms.locfileid: "8334846"
---
I følgende tabel beskrives nogle af nøglerapporterne i kreditorrapporter.

| Report | Beskrivlse | Id | 
|--|--|--|
| [Aldersfordelt gæld](https://businesscentral.dynamics.com?report=322) |Viser forfaldne beløb for kreditorer i forfaldne tidsintervaller. De forfaldne beløb kan vises efter forfaldsdato, bogføringsdato eller bilagsdato efter behov. Du kan vælge at få vist beløbene i lokal valuta (RV) og udskrive detaljer om de forfaldne dokumenter. Tidsintervallet kan have overskrifter med datoer eller med antallet af forfaldne datoer i forhold til den angivne aldersfordelt efter type.<br>Denne rapport er den hovedrapport, der bruges til at afstemme kreditorposter med finansmodulet. Hvis du ikke har tilladt at bogføre på de konti, der bruges i kreditor bogføringsgruppens kreditorkonto, er denne rapport en specifikation af de beløb, som du finder i finansregnskabet.| 322|
| [Kreditor - saldo til dato](https://businesscentral.dynamics.com?report=321) | Viser kreditorsaldoen på det angivne datointervals slutdato. Du kan vælge at få vist kreditorsaldoen i den lokale valuta (RV). Marker feltet **Medtag ikke-udlignede poster** for at få vist de poster, der er blevet lukket med slutdatoen, men som er blevet fjernet (åbnet) senere. Marker afkrydsningsfeltet **Vis poster med nul saldo** for at få vist kreditorer med en saldo på nul til dato filterets slutdato. Datofilteret gælder for de detaljerede kreditorposter for poster i rapporten. Hvis du har betalinger, der er senere end slutdatoen, der er blevet udlignet med fakturaer inden for datointervallet, vises fakturaerne i rapporten, da de ikke er blevet lukket på samme måde som slutdatoen. | 321 |
| [Kreditor - balance](https://businesscentral.dynamics.com?report=329) | Viser bevægelserne på kreditorerne for den periode, der er angivet i datofilteret, sammen med nettoændringen år-til-dato for det regnskabsår, der svarer til den valgte periode. Rapporten er grupperet efter kreditorbogføringsgrupper og giver en anden oversigt over kreditorposter end rapporten **Aldersfordelt gæld**. **Bemærk**: Hvis du ikke har oprettet en regnskabsperiode, vil systemet ikke vide, hvilket regnskabsår du skal bruge, og du skal enten få vist år-til-dato fra det seneste regnskabsår, der er defineret, eller blot vælge perioden, som kan være fra begyndelsen af et år.|329 | 
| [Kreditor - Detaljeret råbalance](https://businesscentral.dynamics.com?report=304) | Viser alle kreditorposter inden for det angivne datofilter. Rapporten viser kreditorens primosaldi i forhold til datofilteret. | 304 | 
| [Købsstatistik](https://businesscentral.dynamics.com?report=312) |[!INCLUDE [reports-purchase-statistics](reports-purchase-statistics.md)]<br>Denne rapport kan også bruges i modulet Kreditor, da det er nemmere at foretage en hurtig søgning efter bogførte betalinger, rabatter og andre transaktioner for en bestemt kreditor.| 312 |
| [Kreditor - forfaldsoversigt](https://businesscentral.dynamics.com?report=305)| Ældre rapport for aldersfordelt gæld. Det anbefales, at du i stedet bruger rapporten **aldersfordelt gæld**. Du kan vælge en periodelængde og en dato, der skal bruges som angivet *forsinket pr. dato*.|305| 
| [Afventende kreditorposter](https://businesscentral.dynamics.com?report=319)| Viser kreditorposter, hvor feltet **Afvent** er tomt.| 319 |
| [Forudbetalingskladde for kreditor](https://businesscentral.dynamics.com?report=317)|Viser udbetalingskladden med oplysninger om kontantrabat og tolerance. Rapporten kan bruges til at kontrollere betalinger, før der oprettes betalingsfiler, og hvordan kladden bogføres. **Bemærk**: rapporten viser kontantrabatten forkert, når der er brugt flere kreditnotaer i et program. I dette tilfælde vises kontantrabatten for de ekstra kreditnotaer som et annulleret beløb.| 317 |
| [Kreditoroversigt](https://businesscentral.dynamics.com?report=301)|Viser diverse stamoplysninger om kreditorer, f.eks. kreditorbogføringsgruppe, rabat- og betalingsoplysninger, prioritetsniveau, kreditors standardvaluta samt kreditorens aktuelle saldo (i RV). Rapporten kan f.eks. bruges til at vedligeholde oplysningerne i tabellen Kreditor.|301|