---
title: Tip - RapidStart Services | Microsoft Docs
description: Når du konfigurerer virksomheder ved hjælp af RapidStart Services, er der nogle tip og tricks, som du kan bruge til at hjælpe dig med, at implementeringen går problemfrit.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: acdac865286577b30f9fe036cca8a50eb7e143a0
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878982"
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
Vi anbefaler, at du overflytter startsaldoer i følgende rækkefølge.  

1.  Overflytte startsaldoer for regnskab uden brug af underregnskaber i finans. Brug af specifikke primosaldo modregningskonti, én opsat for hvert underregnskab. Konfigurer modregningskontiene til at aktivere direkte bogføring.  
2.  Overflyt åbne debitorposter.  
3.  Overflyt åbne vareposter.  
4.  Overflyt åbne anlægsposter.  

## <a name="see-also"></a>Se også  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)
