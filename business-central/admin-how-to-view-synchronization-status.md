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
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="c197e-103">Se status på en synkronisering</span><span class="sxs-lookup"><span data-stu-id="c197e-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="c197e-104">Du kan få vist status for de enkelte synkroniseringsjob, der er udført for [!INCLUDE[crm_md](includes/crm_md.md)]-integration.</span><span class="sxs-lookup"><span data-stu-id="c197e-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="c197e-105">Dette omfatter synkroniseringsjob, der er kørt fra opgavekøen, og manuelle synkroniseringsjob, der er udført på poster fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c197e-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c197e-106">Dette er nyttigt under fejlfinding af synkroniseringsproblemer, fordi det giver dig adgang til oplysninger om de specifikke fejl.</span><span class="sxs-lookup"><span data-stu-id="c197e-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-synchronization-issues-for-coupled-records"></a><span data-ttu-id="c197e-107">Sådan får du vist synkroniseringsproblemer for sammenkoblede poster</span><span class="sxs-lookup"><span data-stu-id="c197e-107">To view synchronization issues for coupled records</span></span>
1. <span data-ttu-id="c197e-108">Vælg ![elpære-ikonet, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), gå til **Fejl ved sammenkædet datasynkronisering**, og vælg derefter det tilhørende link.</span><span class="sxs-lookup"><span data-stu-id="c197e-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="c197e-109">På siden **Fejl ved sammenkædet datasynkronisering** vises problemer, der opstod, da du synkroniserede sammenkoblede poster.</span><span class="sxs-lookup"><span data-stu-id="c197e-109">The **Coupled Data Synchronization Errors** page shows issues that occurred when you synchronized coupled records.</span></span> <span data-ttu-id="c197e-110">Du kan filtrere og sortere poster og udføre handlinger som f.eks **Gendan** eller **Slet poster** for at løse et problem ad gangen.</span><span class="sxs-lookup"><span data-stu-id="c197e-110">You can filter and sort records and take actions such as **Restore** or **Delete Records** to resolve issues one by one.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="c197e-111">Sådan får du vist synkroniseringslog for en bestemt (manuelt synkroniseret) post</span><span class="sxs-lookup"><span data-stu-id="c197e-111">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="c197e-112">Åbn f.eks. en debitor, vare eller en anden post, der synkroniserer data mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales.</span><span class="sxs-lookup"><span data-stu-id="c197e-112">Open, for example, a customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales.</span></span>
2. <span data-ttu-id="c197e-113">Vælg handlingen **Synkroniseringslog** for at få vist synkroniseringsloggen for en valgt post.</span><span class="sxs-lookup"><span data-stu-id="c197e-113">Choose the **Synchronization Log** action to view the synchronization log for a selected record.</span></span> <span data-ttu-id="c197e-114">En bestemt kunde f.eks., som du har synkroniseret manuelt.</span><span class="sxs-lookup"><span data-stu-id="c197e-114">For example, a specific customer you synchronized manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="c197e-115">Se også</span><span class="sxs-lookup"><span data-stu-id="c197e-115">See Also</span></span>  
[<span data-ttu-id="c197e-116">Konfigurere Dynamics 365 for Sales-integration i Business Central</span><span class="sxs-lookup"><span data-stu-id="c197e-116">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="c197e-117">Brug af Dynamics 365 for Sales fra Business Central</span><span class="sxs-lookup"><span data-stu-id="c197e-117">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
