---
title: Business Central intelligente skyudvidelser til skymigrering | Microsoft Docs
description: Brug skymigreringsudvidelserne til at flytte lokale data til Business Central online. Disse udvidelser flytter data, der findes i den lokale sky, til skyen, så du kan bruge Business Central online med dine eksisterende data.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f2d8d556ca4628a66c10f323f47137cd35732a68
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757288"
---
# <a name="intelligent-cloud-extensions-for-cloud-migration"></a>Intelligente skyudvidelser til skymigrering

Afhængigt af løsningen i det lokale miljø, skal du bruge forskellige filtypenavne til at oprette forbindelse til dine data med [!INCLUDE[prod_short](includes/prod_short.md)] online for at kunne overflytte løsningen til skyen.  

Hvis du bruger et af de understøttede lokale produkter, kan du konfigurere dit skymiljø baseret på en produktspecifik udvidelse. Når dit skymiljø er konfigureret, kan du flytte data fra din lokale løsning til [!INCLUDE[prod_short](includes/prod_short.md)]. Dette gør det muligt for dig at få fuldt udbytte af, hvad skyen kan tilbyde din virksomhed f.eks. udvidet indsigt i din virksomhed, kunstig intelligens, adgang til flere enheder og adgang overalt og til enhver tid.  

Du kan finde flere oplysninger i [Overførsel af lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsindholdet for [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="business-central-on-premises"></a>Business Central til det lokale miljø

Hvis du bruger en lokal installation af [!INCLUDE[prod_short](includes/prod_short.md)], skal du hente **Intelligent sky basis**-udvidelsen og **Intelligent sky i Business Central**-udvidelsen og derefter køre den assisterede opsætningsvejledning **Konfiguration af skymigrering**.  

## <a name="dynamics-gp"></a>Dynamics GP

Hvis du bruger Dynamics GP, skal du hente **Intelligent sky basisudvidelsen** og  **Dynamics GP Intelligent sky**-udvidelsen og derefter køre den assisterede opsætningsvejledning **Konfiguration af skymigrering**.  

> [!IMPORTANT]
> Overførsel fra Dynamics GP ved hjælp af vejledningen **Konfigurer skymigrering** som assisteret opsætning understøttes i øjeblikket kun på følgende markeder: USA, Canada, Storbritannien.

## <a name="dynamics-sl"></a>Dynamics SL

Hvis du bruger Dynamics SL, skal du hente udvidelsen **Intelligent cloudbase**, udvidelsen **Intelligent sky i Microsoft Dynamics SL** og udvidelsen **SmartLists for Microsoft Dynamics SL-historik** og derefter køre den assisterede opsætningsvejledning **Konfiguration af cloudmigrering**.  

## <a name="see-also"></a>Se også

[Intelligent indsigt](about-intelligent-cloud.md)  
[Intelligent sky basisudvidelsen](ui-extensions-intelligent-cloud.md)  
