---
title: Rapporter og analyser for kreditor
description: Se, hvilke rapporter og analyser der er tilgængelige i standardversionen af Business Central, så du kan holde styr på kreditorer.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 347
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: edb3b32f88198d8e21aa2bfddafc1b7f319be9de
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953380"
---
# <a name="accounts-payable-reports-and-analytics-in-business-central"></a>Kreditorrapporter og analyser i Business Central

Som en hjælp til styring af kreditorer i [!INCLUDE [prod_short](includes/prod_short.md)], standardrapporter og analyser er indbygget. Den flyttes udover traditionelle rapporterings begrænsninger for at gøre det nemmere at designe forskellige typer rapporter.  

## <a name="reports"></a>Rapporter

I følgende tabel beskrives nogle af nøglerapporterne i kreditorrapporter.

| Report | Objekt-id | Beskrivlse |
|--|--|--|
| **Aldersfordelt gæld** | 322|Viser forfaldne beløb for kreditorer i forfaldne tidsintervaller. De forfaldne beløb kan vises efter forfaldsdato, bogføringsdato eller bilagsdato efter behov. Du kan vælge at få vist beløbene i lokal valuta (RV) og udskrive detaljer om de forfaldne dokumenter. Tidsintervallet kan have overskrifter med datoer eller med antallet af forfaldne datoer i forhold til den angivne aldersfordelt efter type.<br>Denne rapport er den hovedrapport, der bruges til at afstemme kreditorposter med finansmodulet. Hvis du ikke har tilladt at bogføre på de konti, der bruges i kreditor bogføringsgruppens kreditorkonto, er denne rapport en specifikation af de beløb, som du finder i finansregnskabet.|
| **Kreditor - saldo til dato** | 321 | Viser kreditorsaldoen på det angivne datointervals slutdato. Du kan vælge at få vist kreditorsaldoen i den lokale valuta (RV). Marker feltet **Medtag ikke-udlignede poster** for at få vist de poster, der er blevet lukket med slutdatoen, men som er blevet fjernet (åbnet) senere. Marker afkrydsningsfeltet **Vis poster med nul saldo** for at få vist kreditorer med en saldo på nul til dato filterets slutdato. Datofilteret gælder for de detaljerede kreditorposter for poster i rapporten. Hvis du har betalinger, der er senere end slutdatoen, der er blevet udlignet med fakturaer inden for datointervallet, vises fakturaerne i rapporten, da de ikke er blevet lukket på samme måde som slutdatoen. |
| **Kreditor - balance** | 329 | Viser bevægelserne på kreditorerne for den periode, der er angivet i datofilteret, sammen med nettoændringen år-til-dato for det regnskabsår, der svarer til den valgte periode. Rapporten er grupperet efter kreditorbogføringsgrupper og giver en anden oversigt over kreditorposter end rapporten **Aldersfordelt gæld**. **Bemærk**: Hvis du ikke har oprettet en regnskabsperiode, vil systemet ikke vide, hvilket regnskabsår du skal bruge, og du skal enten få vist år-til-dato fra det seneste regnskabsår, der er defineret, eller blot vælge perioden, som kan være fra begyndelsen af et år.|
| **Kreditor - Detaljeret råbalance** | 304 | Viser alle kreditorposter inden for det angivne datofilter. Rapporten viser kreditorens primosaldi i forhold til datofilteret. |
| **Købsstatistik** |312 |[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]<br>Denne rapport kan også bruges i modulet Kreditor, da det er nemmere at foretage en hurtig søgning efter bogførte betalinger, rabatter og andre transaktioner for en bestemt kreditor.|
|**Kreditor - forfaldsoversigt**|305| Ældre rapport for aldersfordelt gæld. Det anbefales, at du i stedet bruger rapporten **aldersfordelt gæld**. Du kan vælge en periodelængde og en dato, der skal bruges som angivet *forsinket pr. dato*.|
|**Afventende kreditorposter**|319|Viser kreditorposter, hvor feltet **Afvent** er tomt.|
|**Forudbetalingskladde for kreditor**|317|Viser udbetalingskladden med oplysninger om kontantrabat og tolerance. Rapporten kan bruges til at kontrollere betalinger, før der oprettes betalingsfiler, og hvordan kladden bogføres. **Bemærk**: rapporten viser kontantrabatten forkert, når der er brugt flere kreditnotaer i et program. I dette tilfælde vises kontantrabatten for de ekstra kreditnotaer som et annulleret beløb.|
|**kreditoroversigt**|301|Viser diverse stamoplysninger om kreditorer, f.eks. kreditorbogføringsgruppe, rabat- og betalingsoplysninger, prioritetsniveau, kreditors standardvaluta samt kreditorens aktuelle saldo (i RV). Rapporten kan f.eks. bruges til at vedligeholde oplysningerne i tabellen Kreditor.|

## <a name="see-also"></a>Se også

[Analysere regnskaber i Microsoft Excel](finance-analyze-excel.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Administrere anlægsaktiver](fa-manage.md)  
[Lokal funktionalitetsoversigt](about-localization.md)  
[Revisoroplevelser i [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
