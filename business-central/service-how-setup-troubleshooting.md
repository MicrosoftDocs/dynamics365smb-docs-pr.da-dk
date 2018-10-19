---
title: Konfigurere fejlfindingsprocesser | Microsoft Docs
description: "Få at vide, hvordan du konfigurerer processer, som hjælper servicerepræsentanter med at identificere og løse problemer med serviceartikler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 24a4fa9811547acfd3372d3eaf7de7b9f1882c7d
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---

# <a name="setting-up-troubleshooting-for-service-items"></a>Opsætning af fejlfinding for serviceartikler
Du kan angive fejlfindingsretningslinjer, som hjælper teknikere med at løse problemer, når de yder service. Retningslinjerne kan f.eks. være en række trin, der skal udføres i forbindelse med en reparation, eller en række spørgsmål, der skal stilles om varerne. Når du har konfigureret retningslinjerne for fejlfinding, kan du tildele dem til serviceartikelgrupper, serviceartikler og varer. Der er et nedarvningshierarki for retningslinjer. Hvis du tildeler dem til en serviceartikelgruppe, arver de varer, der indgår i gruppen, retningslinjerne, medmindre du angiver retningslinjer for varerne. Desuden arver serviceartikler retningslinjer fra varer.  

## <a name="to-set-up-troubleshooting-guidelines"></a>Definere retningslinjer for fejlfinding
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fejlfinding**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a>Sådan tildeles retningslinjer for fejlfinding til varer, serviceartikler eller serviceartikelgrupper.
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, **Serviceartikler** eller **Serviceartikelgrupper**, og vælg derefter det relaterede link.  
2. Vælg den relevante enhed, og vælg derefter handlingen **Fejlfinding**.  

## <a name="see-also"></a>Se også
[Service](service-service.md)
