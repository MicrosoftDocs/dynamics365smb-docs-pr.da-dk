---
title: Konfigurere statusser for serviceordrer og reparationer | Microsoft Docs
description: Du skal definere ni reparationsstatusindstillinger, som identificerer status for reparation og vedligeholdelse af serviceartikler i serviceordrer.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 36925a08f7fdfffedf13902a5c6feaaa8b0929a4
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="16fe1-103">Fremgangsmåde: Konfigurere statusser for serviceordrer og reparationer</span><span class="sxs-lookup"><span data-stu-id="16fe1-103">How to: Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="16fe1-104">Du skal definere reparationsstatusindstillinger, som identificerer status for reparation og vedligeholdelse af serviceartikler i serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="16fe1-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="16fe1-105">Du skal definere mindst ni indstillinger for reparationsstatus, som angiver de situationer eller handlinger, der udføres, når serviceartikler repareres.</span><span class="sxs-lookup"><span data-stu-id="16fe1-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="16fe1-106">Du kan angive prioritetsniveauet for indstillinger for serviceordrestatus.</span><span class="sxs-lookup"><span data-stu-id="16fe1-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="16fe1-107">De fire prioriteter er Meget høj, Høj, Lav, og Meget lav.</span><span class="sxs-lookup"><span data-stu-id="16fe1-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  
  
<span data-ttu-id="16fe1-108">Når du ændrer reparationsstatus for en serviceartikel i en serviceordre, opdateres serviceordrens status automatisk.</span><span class="sxs-lookup"><span data-stu-id="16fe1-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="16fe1-109">Reparationsstatussen for hver enkelt serviceartikel er knyttet til serviceordrestatussen.</span><span class="sxs-lookup"><span data-stu-id="16fe1-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="16fe1-110">Hvis serviceartiklerne er knyttet til to eller flere indstillinger for serviceordrestatus, vælges statussen med den højeste prioritet automatisk.</span><span class="sxs-lookup"><span data-stu-id="16fe1-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="16fe1-111">Definere reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="16fe1-111">To set up a repair status</span></span>  
1. <span data-ttu-id="16fe1-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Reparationsstatus**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="16fe1-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Repair Status**, and then choose the related link.</span></span> <span data-ttu-id="16fe1-113">2.</span><span class="sxs-lookup"><span data-stu-id="16fe1-113">2.</span></span> <span data-ttu-id="16fe1-114">Opret en ny reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="16fe1-114">Create a new repair status.</span></span>  
3. <span data-ttu-id="16fe1-115">Udfyld felterne **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="16fe1-115">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="16fe1-116">I feltet **Serviceordrestatus** skal du vælge den ordrestatus, reparationsstatussen skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="16fe1-116">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="16fe1-117">Feltet **Prioritet** viser prioriteten for den serviceordrestatus, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="16fe1-117">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="16fe1-118">Vælg en reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="16fe1-118">Choose a repair status.</span></span> <span data-ttu-id="16fe1-119">Du kan kun vælge en.</span><span class="sxs-lookup"><span data-stu-id="16fe1-119">You can choose only one.</span></span>  
6. <span data-ttu-id="16fe1-120">Hvis du vil kunne bogføre serviceordrer, der indeholder serviceartikler med denne reparationsstatus, skal du vælge feltet **Bogføring tilladt**.</span><span class="sxs-lookup"><span data-stu-id="16fe1-120">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="16fe1-121">Hvis du manuelt kan ændre indstillingen for serviceordrestatus til **Igangsat** i serviceordrer, der indeholder serviceartikler med denne reparationsstatus, skal du markere afkrydsningsfeltet **Igangsat-status tilladt**.</span><span class="sxs-lookup"><span data-stu-id="16fe1-121">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="16fe1-122">Marker afkrydsningsfelterne **I arbejde-status tilladt**, **Færdig-status tilladt** og **Afvent-status tilladt** på samme måde.</span><span class="sxs-lookup"><span data-stu-id="16fe1-122">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="16fe1-123">Sådan defineres statusprioriteter</span><span class="sxs-lookup"><span data-stu-id="16fe1-123">To set up service status priorities</span></span>  
1. <span data-ttu-id="16fe1-124">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceordrestatus**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="16fe1-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="16fe1-125">Marker den serviceordrestatus, du vil definere en prioritet for.</span><span class="sxs-lookup"><span data-stu-id="16fe1-125">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="16fe1-126">Vælg den prioritet, som serviceordrestatussen skal have, i feltet **Prioritet**.</span><span class="sxs-lookup"><span data-stu-id="16fe1-126">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="16fe1-127">Gentag dette trin for hver status.</span><span class="sxs-lookup"><span data-stu-id="16fe1-127">Repeat this step for each status.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="16fe1-128">Se også</span><span class="sxs-lookup"><span data-stu-id="16fe1-128">See Also</span></span>  
[<span data-ttu-id="16fe1-129">Om serviceordrestatus og reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="16fe1-129">Understanding Service Order Status and Repair Status</span></span>]()  
[<span data-ttu-id="16fe1-130">Konfigurere Service</span><span class="sxs-lookup"><span data-stu-id="16fe1-130">Setting Up Service Management</span></span>](service-setup-service.md)  

