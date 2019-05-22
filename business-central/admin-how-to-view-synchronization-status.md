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
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="8d211-103">Se status på en synkronisering</span><span class="sxs-lookup"><span data-stu-id="8d211-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="8d211-104">Du kan få vist status for de enkelte synkroniseringsjob, der er udført for [!INCLUDE[crm_md](includes/crm_md.md)]-integration.</span><span class="sxs-lookup"><span data-stu-id="8d211-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="8d211-105">Dette omfatter synkroniseringsjob, der er kørt fra opgavekøen, og manuelle synkroniseringsjob, der er udført på poster fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8d211-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8d211-106">Dette er nyttigt under fejlfinding af synkroniseringsproblemer, fordi det giver dig adgang til oplysninger om de specifikke fejl.</span><span class="sxs-lookup"><span data-stu-id="8d211-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-all-synchronization-issues"></a><span data-ttu-id="8d211-107">Sådan får du vist alle synkroniseringsproblemer</span><span class="sxs-lookup"><span data-stu-id="8d211-107">To view all synchronization issues</span></span>
1. <span data-ttu-id="8d211-108">Vælg ![elpære-ikonet, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), gå til **Fejl ved sammenkædet datasynkronisering**, og vælg derefter det tilhørende link.</span><span class="sxs-lookup"><span data-stu-id="8d211-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="8d211-109">På siden **Fejl ved sammenkædet datasynkronisering** kan du se alle de problemer, der er opstået under synkronisering af data mellem [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], filtrere og sortere poster på siden efter tabel, fejlmeddelelse og foretage handlinger som **Prøv igen** eller **Fjern sammenkædning** for at løse problemer ét for ét eller samlet.</span><span class="sxs-lookup"><span data-stu-id="8d211-109">On the **Coupled Data Synchronization Errors** page you can view of all issues that occurred in synchronization of data between [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)], filter and sort records in the page by table, error message and take actions such as **Retry** or **Remove Coupling** to resolve issues one by one or in bulk.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="8d211-110">Sådan får du vist synkroniseringslog for en bestemt (manuelt synkroniseret) post</span><span class="sxs-lookup"><span data-stu-id="8d211-110">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="8d211-111">Åbn f.eks. debitor, vare eller en anden post, der synkroniserer data mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og salg</span><span class="sxs-lookup"><span data-stu-id="8d211-111">Open, for example, customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales</span></span>
2. <span data-ttu-id="8d211-112">Vælg handlingen **Synkroniseringslog** for at se synkroniseringsloggen for den valgte post, f.eks. en bestemt kunde, som du har synkroniseret manuelt</span><span class="sxs-lookup"><span data-stu-id="8d211-112">Choose **Synchronization Log** action to view the synchronization log for selected record, for example, specific customer you synchronized manually</span></span>

## <a name="see-also"></a><span data-ttu-id="8d211-113">Se også</span><span class="sxs-lookup"><span data-stu-id="8d211-113">See Also</span></span>  
[<span data-ttu-id="8d211-114">Konfigurere Dynamics 365 for Sales-integration i Business Central</span><span class="sxs-lookup"><span data-stu-id="8d211-114">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="8d211-115">Brug af Dynamics 365 for Sales fra Business Central</span><span class="sxs-lookup"><span data-stu-id="8d211-115">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
