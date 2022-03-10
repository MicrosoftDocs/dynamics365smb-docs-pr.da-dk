---
title: Tip - RapidStart Services | Microsoft Docs
description: Når du konfigurerer virksomheder ved hjælp af RapidStart Services, er der nogle tip og tricks, som du kan bruge til at hjælpe dig med, at implementeringen går problemfrit.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9b08f4ed71afb580438a5fc8d67cbdfc6c0f5ac6
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8129021"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Tip: RapidStart Services

Når du konfigurerer virksomheder ved hjælp af RapidStart Services, er der nogle tip og tricks, som du kan bruge til at hjælpe dig med, at implementeringen går problemfrit.  

## <a name="take-advantage-of-configuration-templates"></a>Udnytte fordelen ved konfigurationsskabeloner

Konfigurationsskabeloner kan hjælpe dig med at strømline implementeringsprocessen. Ved hjælp af dem kan du inkludere lignende kunder i segmenter og derefter udarbejde en protokol til implementering, der behandler alle kunder i et segment på samme måde. På denne måde kan du anvende et niveau af forudkonfiguration til hvert segment og fortsætte med en hurtig implementering.  

## <a name="configuration-questionnaires"></a>Konfigurationsspørgeskemaer

Du skal overveje at definere standardsvar for at angive de bedste fremgangsmåder, som en støtte til processen med at udfylde et konfigurationsspørgeskema.  

## <a name="batch-creation-of-journal-lines"></a>Batchoprettelse af kladdelinjer

Vi anbefaler, at du bruger de leverede værktøjer til dataoverflytning til at overflytte journalposter. Hvis du bruger et batchjob til at oprette kladdelinjer, har dette et begrænset omfang og opretter kun præ-standardfelter i en kladde. Resten af kladden skal derefter udfyldes manuelt.  

## <a name="migrating-transactions"></a>Overflytning af transaktioner

Vi anbefaler, at du overflytter startsaldoer i følgende rækkefølge. <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. Overflytte startsaldoer for regnskab uden brug af underregnskaber i finans. Brug af specifikke primosaldo modregningskonti, én opsat for hvert underregnskab. Konfigurer modregningskontiene til at aktivere direkte bogføring.  
2. Overflyt åbne debitorposter.  <!--work on these-->
3. Overflyt åbne vareposter.  
4. Overflyt åbne anlægsposter.  

## <a name="make-each-package-manageable"></a>Gøre hver pakke håndterbar

Når du bruger konfigurationspakker til at overføre data, skal du opdele dataene i separate pakker, så de er nemmere at overføre. Hvis du f.eks. vil overføre 20 års finansposter, kan det tage mange timer og dage, før importen er udført. I stedet skal du opdele dataene, så de enkelte pakker bliver nemmere at håndtere. I øjeblikket er der ingen faste regler for, hvad der gør en pakke håndterbar, men hvis du har problemer med at importere eller eksportere en pakke, skal du gøre den mindre og se, om det hjælper.  

## <a name="see-also"></a>Se også

[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]