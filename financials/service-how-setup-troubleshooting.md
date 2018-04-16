---
title: Konfigurere fejlfindingsprocesser | Microsoft Docs
description: "Få at vide, hvordan du konfigurerer processer, som hjælper servicerepræsentanter med at identificere og løse problemer med serviceartikler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5876bf5d959d106eefb9b0f765e42e74dd13ab07
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---

# <a name="setting-up-troubleshooting-for-service-items"></a>Opsætning af fejlfinding for serviceartikler
Du kan angive fejlfindingsretningslinjer, som hjælper teknikere med at løse problemer, når de yder service. Retningslinjerne kan f.eks. være en række trin, der skal udføres i forbindelse med en reparation, eller en række spørgsmål, der skal stilles om varerne. Når du har konfigureret retningslinjerne for fejlfinding, kan du tildele dem til serviceartikelgrupper, serviceartikler og varer. Der er et nedarvningshierarki for retningslinjer. Hvis du tildeler dem til en serviceartikelgruppe, arver de varer, der indgår i gruppen, retningslinjerne, medmindre du angiver retningslinjer for varerne. Desuden arver serviceartikler retningslinjer fra varer.  

## <a name="to-set-up-troubleshooting-guidelines"></a>Definere retningslinjer for fejlfinding
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Fejlfinding**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a>Sådan tildeles retningslinjer for fejlfinding til varer, serviceartikler eller serviceartikelgrupper.
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer** eller **Serviceartikler** eller **Serviceartikelgrupper**, og vælg derefter det relaterede link.  
2. Vælg den relevante enhed, og vælg derefter handlingen **Fejlfinding**.  

## <a name="see-also"></a>Se også
[Service](service-service.md)
