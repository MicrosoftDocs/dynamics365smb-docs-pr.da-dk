---
title: Konfigurere statusser for serviceordrer og reparationer | Microsoft Docs
description: Du skal definere ni reparationsstatusindstillinger, som identificerer status for reparation og vedligeholdelse af serviceartikler i serviceordrer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: 4c28fcfbc2cbc7493ba183812383225754fd3dfa
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389645"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="231aa-103">Konfigurere statusser for serviceordrer og reparationer</span><span class="sxs-lookup"><span data-stu-id="231aa-103">Set Up Statuses for Service Orders and Repairs</span></span>

<span data-ttu-id="231aa-104">Du skal definere reparationsstatusindstillinger, som identificerer status for reparation og vedligeholdelse af serviceartikler i serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="231aa-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="231aa-105">Du skal definere mindst ni indstillinger for reparationsstatus, som angiver de situationer eller handlinger, der udføres, når serviceartikler repareres.</span><span class="sxs-lookup"><span data-stu-id="231aa-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="231aa-106">Du kan angive prioritetsniveauet for indstillinger for serviceordrestatus.</span><span class="sxs-lookup"><span data-stu-id="231aa-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="231aa-107">De fire prioriteter er **Høj**, **Mellemhøj**, **Mellemlav** og **Lav**.</span><span class="sxs-lookup"><span data-stu-id="231aa-107">The four priorities are **High**, **Medium High**, **Medium Low**, and **Low**.</span></span>  

<span data-ttu-id="231aa-108">Når du ændrer reparationsstatus for en serviceartikel i en serviceordre, opdateres serviceordrens status automatisk.</span><span class="sxs-lookup"><span data-stu-id="231aa-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="231aa-109">Reparationsstatussen for hver enkelt serviceartikel er knyttet til serviceordrestatussen.</span><span class="sxs-lookup"><span data-stu-id="231aa-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="231aa-110">Hvis serviceartiklerne er knyttet til to eller flere indstillinger for serviceordrestatus, vælges statussen med den højeste prioritet automatisk.</span><span class="sxs-lookup"><span data-stu-id="231aa-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

<span data-ttu-id="231aa-111">Før du kan oprette en reparationsstatus, skal du oprette servicestatusprioriteter.</span><span class="sxs-lookup"><span data-stu-id="231aa-111">Before you can set up a repair status, you must set up service status priorities.</span></span>

## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="231aa-112">Sådan defineres statusprioriteter</span><span class="sxs-lookup"><span data-stu-id="231aa-112">To set up service status priorities</span></span>

1. <span data-ttu-id="231aa-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceordrestatus**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="231aa-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="231aa-114">Marker den serviceordrestatus, du vil definere en prioritet for.</span><span class="sxs-lookup"><span data-stu-id="231aa-114">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="231aa-115">Vælg den prioritet, som serviceordrestatussen skal have, i feltet **Prioritet**.</span><span class="sxs-lookup"><span data-stu-id="231aa-115">In the **Priority** field, choose the priority you want for this service order status.</span></span>  

<span data-ttu-id="231aa-116">Gentag trin 2 og 3, indtil du har defineret prioriteten for hver af de fire statusindstillinger: **Afventer**, **Igang**, **Afsluttet** og **Afventer**.</span><span class="sxs-lookup"><span data-stu-id="231aa-116">Repeat steps 2 and 3 until you have set the priority for each of the four status options: **Pending**, **In Process**, **Finished**, and **On Hold**.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="231aa-117">Definere reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="231aa-117">To set up a repair status</span></span>

1. <span data-ttu-id="231aa-118">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Reparationsstatus**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="231aa-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Repair Status**, and then choose the related link.</span></span>
2. <span data-ttu-id="231aa-119">Opret en ny reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="231aa-119">Create a new repair status.</span></span>  
3. <span data-ttu-id="231aa-120">Udfyld felterne **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="231aa-120">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="231aa-121">I feltet **Serviceordrestatus** skal du vælge den ordrestatus, reparationsstatussen skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="231aa-121">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="231aa-122">Feltet **Prioritet** viser prioriteten for den serviceordrestatus, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="231aa-122">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="231aa-123">Vælg en reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="231aa-123">Choose a repair status.</span></span> <span data-ttu-id="231aa-124">Du kan kun vælge en.</span><span class="sxs-lookup"><span data-stu-id="231aa-124">You can choose only one.</span></span> <span data-ttu-id="231aa-125">En reparationsstatus kan ikke sammenkædes med mere end én indstilling for reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="231aa-125">A repair status cannot be linked more than one repair status option.</span></span>  
6. <span data-ttu-id="231aa-126">Hvis du vil kunne bogføre serviceordrer, der indeholder serviceartikler med denne reparationsstatus, skal du vælge feltet **Bogføring tilladt**.</span><span class="sxs-lookup"><span data-stu-id="231aa-126">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="231aa-127">Hvis du manuelt kan ændre indstillingen for serviceordrestatus til **Igangsat** i serviceordrer, der indeholder serviceartikler med denne reparationsstatus, skal du markere afkrydsningsfeltet **Igangsat-status tilladt**.</span><span class="sxs-lookup"><span data-stu-id="231aa-127">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="231aa-128">Marker afkrydsningsfelterne **I arbejde-status tilladt**, **Færdig-status tilladt** og **Afvent-status tilladt** på samme måde.</span><span class="sxs-lookup"><span data-stu-id="231aa-128">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>

<span data-ttu-id="231aa-129">Gentag disse trin for hver af indstillingerne for reparationsstatus, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="231aa-129">Repeat these steps for each of the repair status options you want to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="231aa-130">Se også</span><span class="sxs-lookup"><span data-stu-id="231aa-130">See Also</span></span>

[<span data-ttu-id="231aa-131">Serviceordrestatus og reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="231aa-131">Service Order Status and Repair Status</span></span>](service-service-order-status-and-repair-status.md)  
[<span data-ttu-id="231aa-132">Konfigurere Service</span><span class="sxs-lookup"><span data-stu-id="231aa-132">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]