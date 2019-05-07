---
title: Konfigurere virksomhedskonfiguration | Microsoft dokumenter
description: Implementeringsprocessen, der begynder med Business Central-løsningen, kræver. Du kan samle alle disse oplysninger i konfigurationspakker.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e003f429122bd31ee35ef9b843682bfe8866407a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "926459"
---
# <a name="set-up-company-configuration"></a>Konfigurere virksomhedskonfiguration
Implementeringsprocessen, der begynder med Microsoft-partneren. Partneren er ansvarlig for at gennemtænke konfigurationsdetaljerne og oprettelse af en pakke, der let kan anvendes af en kunde. Før du opretter en ny virksomhed, skal du planlægge, hvordan den konfigureres. Du skal overveje grundlæggende konfigurationsdata og de datatyper, som din [!INCLUDE[d365fin](includes/d365fin_md.md)]-løsning kræver. Du kan samle alle disse oplysninger i konfigurationspakker.

RapidStart Services giver dig også de værktøjer, du skal bruge til at overflytte ældre data, f.eks. kunder og kreditorer.  

Vi anbefaler, at du opretter konfigurationspakker med de fleste af de konfigurationstabeller, som allerede udfyldt, så kunder behøver kun at ændre nogle få indstillinger, når pakken er installeret. Når du f.eks. opretter en ny virksomhed, udfyldes tabellerne **Nummerserie** og **Nummerserielinje**, med et sæt nummerserie og starttal. De tilsvarende **Nummerserie**-felter i opsætningstabellerne udfyldes også automatisk. Du behøver ikke at indtaste nummerserier og andre grundlæggende opsætningsdata. Du kan også manuelt ændre alle standarddata, der bruges med RapidStart Services ved at bruge konfigurationsregnearket.  

Konfigurationspakkerne bygger på en forudkonfigureret virksomhed. Når du har konfigureret en virksomhed, der opfylder dine behov, kan du oprette en konfigurationspakke, der indeholder relevante data fra denne virksomhed. Du kan derefter oprette en ny virksomhed, der skal konfigureres på samme måde.  

Som en hjælp til at importere masterdata, f.eks. debitor- og kreditoroplysninger, kan du bruge konfigurationsskabeloner. Konfigurationsskabeloner indeholder et sæt standardindstillinger, der automatisk tildeles de poster, der importeres til [!INCLUDE[d365fin](includes/d365fin_md.md)].

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

|**For at**|**Skal du se**|  
|------------|-------------|  
|Planlægge en virksomhedskonfiguration ved at udfylde konfigurationsarket.|[Administrere virksomhedskonfigurationen i et regneark](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Oprette en konfigurationspakke, tilpasse en pakke, tildele tabeller til en pakke, gennemse eller redigere eksisterende debitordata, oprette den nye virksomhed og derefter flytte testdata til produktionsmiljøet.|[Forberede en konfigurationspakke](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a>Se også  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)
