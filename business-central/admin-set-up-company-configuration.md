---
title: Konfigurere virksomhedskonfiguration | Microsoft dokumenter
description: Implementeringsprocessen, der begynder med Business Central-løsningen, kræver. Du kan samle alle disse oplysninger i konfigurationspakker.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e9b54a28c960ccdaa41c16cce237266e8cb43a88
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4745938"
---
# <a name="set-up-company-configuration"></a>Konfigurere virksomhedskonfiguration
Implementeringsprocessen, der begynder med Microsoft-partneren. Partneren er ansvarlig for at gennemtænke konfigurationsdetaljerne og oprettelse af en pakke, der let kan anvendes af en kunde. Før du opretter en ny virksomhed, skal du planlægge, hvordan den konfigureres. Du skal overveje grundlæggende konfigurationsdata og de datatyper, som din [!INCLUDE[prod_short](includes/prod_short.md)]-løsning kræver. Du kan samle alle disse oplysninger i konfigurationspakker.

RapidStart Services giver dig også de værktøjer, du skal bruge til at overflytte ældre data, f.eks. debitorer og kreditorer.  

Vi anbefaler, at du opretter konfigurationspakker med de fleste af de konfigurationstabeller, som allerede udfyldt, så kunder behøver kun at ændre nogle få indstillinger, når pakken er installeret. Når du f.eks. opretter en ny virksomhed, udfyldes tabellerne **Nummerserie** og **Nummerserielinje**, med et sæt nummerserie og starttal. De tilsvarende **Nummerserie**-felter i opsætningstabellerne udfyldes også automatisk. Du behøver ikke at indtaste nummerserier og andre grundlæggende opsætningsdata. Du kan også manuelt ændre alle standarddata, der bruges til RapidStart Services, ved at bruge konfigurationsregnearket.  

Konfigurationspakkerne bygger på en forudkonfigureret virksomhed. Når du har konfigureret en virksomhed, der opfylder dine behov, kan du oprette en konfigurationspakke, der indeholder relevante data fra denne virksomhed. Du kan derefter oprette en ny virksomhed, der skal konfigureres på samme måde.  

Som en hjælp til at importere masterdata, f.eks. debitor- og kreditoroplysninger, kan du bruge konfigurationsskabeloner. Konfigurationsskabeloner indeholder et sæt standardindstillinger, der automatisk tildeles de poster, der importeres til [!INCLUDE[prod_short](includes/prod_short.md)].

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

|**For at**|**Skal du se**|  
|------------|-------------|  
|Planlægge en virksomhedskonfiguration ved at udfylde konfigurationsarket.|[Administrere virksomhedskonfigurationen i et regneark](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Oprette en konfigurationspakke, tilpasse en pakke, tildele tabeller til en pakke, gennemse eller redigere eksisterende debitordata, oprette den nye virksomhed og derefter flytte testdata til produktionsmiljøet.|[Forberede en konfigurationspakke](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a>Se også  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]