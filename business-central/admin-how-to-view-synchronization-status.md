---
title: Se status på en synkronisering | Microsoft Docs
description: Få at vide, hvordan du får vist status for et bestemt synkroniseringsjob.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620880"
---
# <a name="view-the-status-of-a-synchronization"></a>Se status på en synkronisering
Du kan få vist status for de enkelte synkroniseringsjob, der er udført for [!INCLUDE[crm_md](includes/crm_md.md)]-integration. Dette omfatter synkroniseringsjob, der er kørt fra opgavekøen, og manuelle synkroniseringsjob, der er udført på poster fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette er nyttigt under fejlfinding af synkroniseringsproblemer, fordi det giver dig adgang til oplysninger om de specifikke fejl.

### <a name="to-view-synchronization-issues-for-coupled-records"></a>Sådan får du vist synkroniseringsproblemer for sammenkoblede poster
1. Vælg ![elpære-ikonet, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), gå til **Fejl ved sammenkædet datasynkronisering**, og vælg derefter det tilhørende link.
2. På siden **Fejl ved sammenkædet datasynkronisering** vises problemer, der opstod, da du synkroniserede sammenkoblede poster. Du kan filtrere og sortere poster og udføre handlinger som f.eks **Gendan** eller **Slet poster** for at løse et problem ad gangen.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Sådan får du vist synkroniseringslog for en bestemt (manuelt synkroniseret) post
1. Åbn f.eks. en debitor, vare eller en anden post, der synkroniserer data mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales.
2. Vælg handlingen **Synkroniseringslog** for at få vist synkroniseringsloggen for en valgt post. En bestemt kunde f.eks., som du har synkroniseret manuelt.

## <a name="see-also"></a>Se også  
[Konfigurere Dynamics 365 for Sales-integration i Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Brug af Dynamics 365 for Sales fra Business Central](marketing-integrate-dynamicscrm.md)
