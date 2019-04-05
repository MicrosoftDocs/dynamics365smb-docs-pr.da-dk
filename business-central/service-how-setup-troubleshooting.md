---
title: Konfigurere fejlfindingsprocesser | Microsoft Docs
description: Få at vide, hvordan du konfigurerer processer, som hjælper servicerepræsentanter med at identificere og løse problemer med serviceartikler.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 24a4fa9811547acfd3372d3eaf7de7b9f1882c7d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792641"
---
# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="765cc-103">Opsætning af fejlfinding for serviceartikler</span><span class="sxs-lookup"><span data-stu-id="765cc-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="765cc-104">Du kan angive fejlfindingsretningslinjer, som hjælper teknikere med at løse problemer, når de yder service.</span><span class="sxs-lookup"><span data-stu-id="765cc-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="765cc-105">Retningslinjerne kan f.eks. være en række trin, der skal udføres i forbindelse med en reparation, eller en række spørgsmål, der skal stilles om varerne.</span><span class="sxs-lookup"><span data-stu-id="765cc-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="765cc-106">Når du har konfigureret retningslinjerne for fejlfinding, kan du tildele dem til serviceartikelgrupper, serviceartikler og varer.</span><span class="sxs-lookup"><span data-stu-id="765cc-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="765cc-107">Der er et nedarvningshierarki for retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="765cc-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="765cc-108">Hvis du tildeler dem til en serviceartikelgruppe, arver de varer, der indgår i gruppen, retningslinjerne, medmindre du angiver retningslinjer for varerne.</span><span class="sxs-lookup"><span data-stu-id="765cc-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="765cc-109">Desuden arver serviceartikler retningslinjer fra varer.</span><span class="sxs-lookup"><span data-stu-id="765cc-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="765cc-110">Definere retningslinjer for fejlfinding</span><span class="sxs-lookup"><span data-stu-id="765cc-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="765cc-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fejlfinding**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="765cc-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="765cc-112">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="765cc-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="765cc-113">Sådan tildeles retningslinjer for fejlfinding til varer, serviceartikler eller serviceartikelgrupper.</span><span class="sxs-lookup"><span data-stu-id="765cc-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="765cc-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, **Serviceartikler** eller **Serviceartikelgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="765cc-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="765cc-115">Vælg den relevante enhed, og vælg derefter handlingen **Fejlfinding**.</span><span class="sxs-lookup"><span data-stu-id="765cc-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="765cc-116">Se også</span><span class="sxs-lookup"><span data-stu-id="765cc-116">See Also</span></span>
[<span data-ttu-id="765cc-117">Service Management</span><span class="sxs-lookup"><span data-stu-id="765cc-117">Service Management</span></span>](service-service.md)