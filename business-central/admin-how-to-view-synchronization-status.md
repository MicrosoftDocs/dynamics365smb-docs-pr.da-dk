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
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245681"
---
# <a name="view-the-status-of-a-synchronization"></a>Se status på en synkronisering
Du kan få vist status for de enkelte synkroniseringsjob, der er udført for [!INCLUDE[crm_md](includes/crm_md.md)]-integration. Dette omfatter synkroniseringsjob, der er kørt fra opgavekøen, og manuelle synkroniseringsjob, der er udført på poster fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette er nyttigt under fejlfinding af synkroniseringsproblemer, fordi det giver dig adgang til oplysninger om de specifikke fejl.

### <a name="to-view-all-synchronization-issues"></a>Sådan får du vist alle synkroniseringsproblemer
1. Vælg ![elpære-ikonet, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), gå til **Fejl ved sammenkædet datasynkronisering**, og vælg derefter det tilhørende link.
2. På siden **Fejl ved sammenkædet datasynkronisering** kan du se alle de problemer, der er opstået under synkronisering af data mellem [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], filtrere og sortere poster på siden efter tabel, fejlmeddelelse og foretage handlinger som **Prøv igen** eller **Fjern sammenkædning** for at løse problemer ét for ét eller samlet.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Sådan får du vist synkroniseringslog for en bestemt (manuelt synkroniseret) post
1. Åbn f.eks. debitor, vare eller en anden post, der synkroniserer data mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og salg
2. Vælg handlingen **Synkroniseringslog** for at se synkroniseringsloggen for den valgte post, f.eks. en bestemt kunde, som du har synkroniseret manuelt

## <a name="see-also"></a>Se også  
[Konfigurere Dynamics 365 for Sales-integration i Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Brug af Dynamics 365 for Sales fra Business Central](marketing-integrate-dynamicscrm.md)
