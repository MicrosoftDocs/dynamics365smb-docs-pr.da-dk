---
title: Konfigurere fejlfindingsprocesser | Microsoft Docs
description: Få at vide, hvordan du konfigurerer processer, som hjælper servicerepræsentanter med at identificere og løse problemer med serviceartikler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 214c83c4614a92a8cc94c7dc88efe527686ef397
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773676"
---
# <a name="setting-up-troubleshooting-for-service-items"></a>Opsætning af fejlfinding for serviceartikler
Du kan angive fejlfindingsretningslinjer, som hjælper teknikere med at løse problemer, når de yder service. Retningslinjerne kan f.eks. være en række trin, der skal udføres i forbindelse med en reparation, eller en række spørgsmål, der skal stilles om varerne. Når du har konfigureret retningslinjerne for fejlfinding, kan du tildele dem til serviceartikelgrupper, serviceartikler og varer. Der er et nedarvningshierarki for retningslinjer. Hvis du tildeler dem til en serviceartikelgruppe, arver de varer, der indgår i gruppen, retningslinjerne, medmindre du angiver retningslinjer for varerne. Desuden arver serviceartikler retningslinjer fra varer.  

## <a name="to-set-up-troubleshooting-guidelines"></a>Definere retningslinjer for fejlfinding
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fejlfinding**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a>Sådan tildeles retningslinjer for fejlfinding til varer, serviceartikler eller serviceartikelgrupper.
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer** eller **Serviceartikler** eller **Serviceartikelgrupper**, og vælg derefter det relaterede link.  
2. Vælg den relevante enhed, og vælg derefter handlingen **Fejlfinding**.  

## <a name="see-also"></a>Se også
[Service Management](service-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]