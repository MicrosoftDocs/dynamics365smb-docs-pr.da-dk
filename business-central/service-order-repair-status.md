---
title: Konfigurere statusser for serviceordrer og reparationer | Microsoft Docs
description: Du skal definere ni reparationsstatusindstillinger, som identificerer status for reparation og vedligeholdelse af serviceartikler i serviceordrer.
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
ms.openlocfilehash: 64afbccba0573445902efdaf3c3919dacdb40e8c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250568"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Konfigurere statusser for serviceordrer og reparationer
Du skal definere reparationsstatusindstillinger, som identificerer status for reparation og vedligeholdelse af serviceartikler i serviceordrer. Du skal definere mindst ni indstillinger for reparationsstatus, som angiver de situationer eller handlinger, der udføres, når serviceartikler repareres.  

Du kan angive prioritetsniveauet for indstillinger for serviceordrestatus. De fire prioriteter er Meget høj, Høj, Lav, og Meget lav.  

Når du ændrer reparationsstatus for en serviceartikel i en serviceordre, opdateres serviceordrens status automatisk. Reparationsstatussen for hver enkelt serviceartikel er knyttet til serviceordrestatussen. Hvis serviceartiklerne er knyttet til to eller flere indstillinger for serviceordrestatus, vælges statussen med den højeste prioritet automatisk.  

## <a name="to-set-up-a-repair-status"></a>Definere reparationsstatus  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Reparationsstatus**, og vælg derefter det relaterede link.
2. Opret en ny reparationsstatus.  
3. Udfyld felterne **Kode** og **Beskrivelse**.  
4. I feltet **Serviceordrestatus** skal du vælge den ordrestatus, reparationsstatussen skal knyttes til. Feltet **Prioritet** viser prioriteten for den serviceordrestatus, du har valgt.  
5. Vælg en reparationsstatus. Du kan kun vælge en.  
6. Hvis du vil kunne bogføre serviceordrer, der indeholder serviceartikler med denne reparationsstatus, skal du vælge feltet **Bogføring tilladt**.  
7. Hvis du manuelt kan ændre indstillingen for serviceordrestatus til **Igangsat** i serviceordrer, der indeholder serviceartikler med denne reparationsstatus, skal du markere afkrydsningsfeltet **Igangsat-status tilladt**.  
8. Marker afkrydsningsfelterne **I arbejde-status tilladt**, **Færdig-status tilladt** og **Afvent-status tilladt** på samme måde.
  
## <a name="to-set-up-service-status-priorities"></a>Sådan defineres statusprioriteter  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceordrestatus**, og vælg derefter det relaterede link.  
2. Marker den serviceordrestatus, du vil definere en prioritet for.  
3. Vælg den prioritet, som serviceordrestatussen skal have, i feltet **Prioritet**. Gentag dette trin for hver status.  

## <a name="see-also"></a>Se også  
[Serviceordrestatus og reparationsstatus](service-service-order-status-and-repair-status.md)  
[Konfigurere Service](service-setup-service.md)  
