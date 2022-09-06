---
title: Udvidelser af skymigrering
description: Brug skymigreringsudvidelserne til at flytte lokale data til Business Central online. Disse udvidelser flytter dataene til den lokale computer til skyen.
author: jenolson
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, import, implement
ms.search.form: 4021, 4026, 4031, 4090, 4091, 4092, 4093, 4094, 4095, 4096, 4097, 40027,
ms.reviewer: edupont
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: e04a5ba015914a39c87a9966c317a7b5f1e3d55a
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361934"
---
# <a name="cloud-migration-extensions-for-migrating-to-business-central-online"></a>Udvidelser af skymigrering for migrering til Business Central Online

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

[Udvidelser af skymigreringsbase](ui-extensions-intelligent-cloud.md)  
[Overførsel af data i det lokale miljø til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
