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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7fdbc30e20e7d5a8feeb17a97ccdee3688fa7607
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380402"
---
# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="44398-103">Opsætning af fejlfinding for serviceartikler</span><span class="sxs-lookup"><span data-stu-id="44398-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="44398-104">Du kan angive fejlfindingsretningslinjer, som hjælper teknikere med at løse problemer, når de yder service.</span><span class="sxs-lookup"><span data-stu-id="44398-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="44398-105">Retningslinjerne kan f.eks. være en række trin, der skal udføres i forbindelse med en reparation, eller en række spørgsmål, der skal stilles om varerne.</span><span class="sxs-lookup"><span data-stu-id="44398-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="44398-106">Når du har konfigureret retningslinjerne for fejlfinding, kan du tildele dem til serviceartikelgrupper, serviceartikler og varer.</span><span class="sxs-lookup"><span data-stu-id="44398-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="44398-107">Der er et nedarvningshierarki for retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="44398-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="44398-108">Hvis du tildeler dem til en serviceartikelgruppe, arver de varer, der indgår i gruppen, retningslinjerne, medmindre du angiver retningslinjer for varerne.</span><span class="sxs-lookup"><span data-stu-id="44398-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="44398-109">Desuden arver serviceartikler retningslinjer fra varer.</span><span class="sxs-lookup"><span data-stu-id="44398-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="44398-110">Definere retningslinjer for fejlfinding</span><span class="sxs-lookup"><span data-stu-id="44398-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="44398-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fejlfinding**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="44398-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="44398-112">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="44398-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="44398-113">Sådan tildeles retningslinjer for fejlfinding til varer, serviceartikler eller serviceartikelgrupper.</span><span class="sxs-lookup"><span data-stu-id="44398-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="44398-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer** eller **Serviceartikler** eller **Serviceartikelgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="44398-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="44398-115">Vælg den relevante enhed, og vælg derefter handlingen **Fejlfinding**.</span><span class="sxs-lookup"><span data-stu-id="44398-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="44398-116">Se også</span><span class="sxs-lookup"><span data-stu-id="44398-116">See Also</span></span>
[<span data-ttu-id="44398-117">Service Management</span><span class="sxs-lookup"><span data-stu-id="44398-117">Service Management</span></span>](service-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]