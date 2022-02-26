---
title: Konfigurere virksomhedskonfiguration
description: Som partner skal du konfigurere Business Central korrekt for din debitor med standardkonfigurationer eller kundespecifikke konfigurationer, som du bundter i konfigurationspakker.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5baef81f22e260fa6f582b536dcf356d3ae25d25
ms.sourcegitcommit: ecbabd2d0fdf2566cea4a05a25b09ff6ca6256c6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/22/2021
ms.locfileid: "6649708"
---
# <a name="set-up-company-configuration"></a>Konfigurere virksomhedskonfiguration
Implementeringsprocessen, der begynder med Microsoft-partneren. Som partner er du ansvarlig for at gennemtænke konfigurationsdetaljerne og oprette en pakke, som en debitor let kan anvende. Før du opretter en ny virksomhed i [!INCLUDE [prod_short](includes/prod_short.md)] online eller i det lokale miljø, skal du planlægge, hvordan den skal konfigureres. Du skal overveje grundlæggende konfigurationsdata og de datatyper, som din [!INCLUDE[prod_short](includes/prod_short.md)]-løsning kræver. Du kan samle alle disse oplysninger i konfigurationspakker.

RapidStart Services tilbyder også de værktøjer, du skal bruge til at overflytte ældre data, f.eks. debitorer og kreditorer.  

Vi anbefaler, at du opretter konfigurationspakker med de fleste af de konfigurationstabeller, som allerede udfyldt, så kunder behøver kun at ændre nogle få indstillinger, når pakken er installeret. Når du f.eks. opretter en ny virksomhed, udfyldes tabellerne **Nummerserie** og **Nummerserielinje**, med et sæt nummerserie og starttal. De tilsvarende **Nummerserie**-felter i opsætningstabellerne udfyldes også automatisk. Du behøver ikke at indtaste nummerserier og andre grundlæggende opsætningsdata. Du kan også manuelt ændre alle standarddata, der bruges til RapidStart Services, ved at bruge konfigurationsregnearket.  

Konfigurationspakkerne bygger på en forudkonfigureret virksomhed. Når du har konfigureret en virksomhed, der opfylder dine behov, kan du oprette en konfigurationspakke, der indeholder relevante data fra denne virksomhed. Du kan derefter oprette en ny virksomhed, der skal konfigureres på samme måde.  

Som en hjælp til at importere masterdata, f.eks. debitor- og kreditoroplysninger, kan du bruge konfigurationsskabeloner. Konfigurationsskabeloner indeholder et sæt standardindstillinger, der automatisk tildeles de poster, der importeres til [!INCLUDE[prod_short](includes/prod_short.md)].

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

|**For at**|**Skal du se**|  
|------------|-------------|  
|Planlægge en virksomhedskonfiguration ved at udfylde konfigurationsarket.|[Administrere virksomhedskonfigurationen i et regneark](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Oprette en konfigurationspakke, tilpasse en pakke, tildele tabeller til en pakke, gennemse eller redigere eksisterende debitordata, oprette den nye virksomhed og derefter flytte testdata til produktionsmiljøet.|[Forberede en konfigurationspakke](admin-how-to-prepare-a-configuration-package.md)|

Du kan også oprette konfigurationspakker med standardkonfigurationer, som du kan bruge igen og igen. Du kan finde flere oplysninger i [Oprette standardkonfigurationspakker for virksomheder](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) i indholdet til udviklere og administration.  

## <a name="see-also"></a>Se også

[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]