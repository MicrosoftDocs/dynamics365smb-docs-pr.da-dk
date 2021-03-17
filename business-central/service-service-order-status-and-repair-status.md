---
title: Serviceordrestatus og reparationsstatus
description: Der er en særlig relation mellem feltet Status på siden Serviceordre og den serviceartikelreparationsstatus, der er repræsenteret af feltet Reparationsstatuskode på siden Serviceordre i Service. Serviceordrens status afspejler reparationsstatus for alle serviceartikler i serviceordren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: b9095cbfd1b8a55f525f0a3c4dcfad6cf56fc449
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386820"
---
# <a name="service-order-status-and-repair-status"></a><span data-ttu-id="65f10-104">Serviceordrestatus og reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="65f10-104">Service Order Status and Repair Status</span></span>

<span data-ttu-id="65f10-105">Der er en særlig relation mellem feltet **Status** på siden **Serviceordre** og den serviceartikelreparationsstatus, der er repræsenteret af feltet **Reparationsstatuskode** på siden **Serviceordre** i Service.</span><span class="sxs-lookup"><span data-stu-id="65f10-105">The **Status** field on the **Service Order** page and the service item repair status, which is represented by the **Repair Status Code** field on the **Service Order** page have a certain relationship in Service Management.</span></span> <span data-ttu-id="65f10-106">Serviceordrens status afspejler reparationsstatus for alle serviceartikler i serviceordren.</span><span class="sxs-lookup"><span data-stu-id="65f10-106">The service order status reflects the repair status of all the service items in the service order.</span></span>  

> [!NOTE]  
> <span data-ttu-id="65f10-107">Disse to statusfelter er ikke relateret til feltet **Frigivelsesstatus** på serviceordrehovedet, der styrer lagerets håndtering af serviceartikler.</span><span class="sxs-lookup"><span data-stu-id="65f10-107">These two status field are not related to the **Release Status** field on the service order header, which determines how the warehouse handles service items.</span></span>  

<span data-ttu-id="65f10-108">Når du ændrer reparationsstatus for en serviceartikel i en serviceordre, opdateres ordrens status automatisk.</span><span class="sxs-lookup"><span data-stu-id="65f10-108">Each time the repair status of a service item is changed in a service order, the status of the order is updated.</span></span> <span data-ttu-id="65f10-109">Hvis du vil have vist en status, som afspejler den generelle reparationsstatus for de enkelte serviceartikler, skal du angive følgende:</span><span class="sxs-lookup"><span data-stu-id="65f10-109">To display the status that reflects the overall repair status of the individual service items, you must specify the following:</span></span>  

* <span data-ttu-id="65f10-110">Den serviceordrestatus, som hver enkelt reparationsstatus er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="65f10-110">The service order status that each repair status is linked to.</span></span>  
* <span data-ttu-id="65f10-111">Prioritetsniveauet for hver enkelt serviceordrestatus.</span><span class="sxs-lookup"><span data-stu-id="65f10-111">The level of priority of each service order status option.</span></span>  

<span data-ttu-id="65f10-112">Når du konverterer et servicetilbud til en serviceordre, ændres reparationsstatussen automatisk for hver enkelt serviceartikel i ordren til **Ingen tidl. serv.** og serviceordrestatus til **Igangsat**.</span><span class="sxs-lookup"><span data-stu-id="65f10-112">When you convert a service quote to a service order, the repair status of each service item is changed in the order to **Initial** and the service order status is changed to **Pending**.</span></span>  

> [!NOTE]
> <span data-ttu-id="65f10-113">Før du kan oprette serviceordrer, skal du oprette reparationsstatus og servicestatusprioriteter.</span><span class="sxs-lookup"><span data-stu-id="65f10-113">Before you can create service orders, you must set up repair statuses and service status priorities.</span></span> <span data-ttu-id="65f10-114">Du kan finde flere oplysninger i [Konfigurere statusser for serviceordrer og reparationer](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="65f10-114">For more information, see [Set Up Statuses for Service Orders and Repairs](service-order-repair-status.md).</span></span>

## <a name="specifying-service-order-status-for-repair-status"></a><span data-ttu-id="65f10-115">Angive serviceordrestatus for reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="65f10-115">Specifying Service Order Status for Repair Status</span></span>

<span data-ttu-id="65f10-116">Hver reparationsstatus er knyttet til en bestemt serviceordrestatus.</span><span class="sxs-lookup"><span data-stu-id="65f10-116">Each repair status is linked to a particular service order status.</span></span> <span data-ttu-id="65f10-117">Indstillingerne for serviceordrestatus er som følger:</span><span class="sxs-lookup"><span data-stu-id="65f10-117">The options for the service order status are as follows:</span></span>

* <span data-ttu-id="65f10-118">**Igangsat**</span><span class="sxs-lookup"><span data-stu-id="65f10-118">**Pending**</span></span>
* <span data-ttu-id="65f10-119">**Igangsat**</span><span class="sxs-lookup"><span data-stu-id="65f10-119">**In Process**</span></span>
* <span data-ttu-id="65f10-120">**Afvent**</span><span class="sxs-lookup"><span data-stu-id="65f10-120">**On Hold**</span></span>
* <span data-ttu-id="65f10-121">**Færdig**</span><span class="sxs-lookup"><span data-stu-id="65f10-121">**Finished**</span></span>

<span data-ttu-id="65f10-122">Der findes følgende reparationsstatusindstillinger</span><span class="sxs-lookup"><span data-stu-id="65f10-122">The repair status options are as follows:</span></span>

* <span data-ttu-id="65f10-123">**Oprettet**</span><span class="sxs-lookup"><span data-stu-id="65f10-123">**Initial**</span></span>
* <span data-ttu-id="65f10-124">**Igangsat**</span><span class="sxs-lookup"><span data-stu-id="65f10-124">**In Process**</span></span>
* <span data-ttu-id="65f10-125">**Henvist**</span><span class="sxs-lookup"><span data-stu-id="65f10-125">**Referred**</span></span>
* <span data-ttu-id="65f10-126">**Delvist repareret**</span><span class="sxs-lookup"><span data-stu-id="65f10-126">**Partly Serviced**</span></span>
* <span data-ttu-id="65f10-127">**Tilbud færdigt**</span><span class="sxs-lookup"><span data-stu-id="65f10-127">**Quote Finished**</span></span>
* <span data-ttu-id="65f10-128">**Venter på kunde**</span><span class="sxs-lookup"><span data-stu-id="65f10-128">**Waiting for Customer**</span></span>
* <span data-ttu-id="65f10-129">**Reservedel bestilt**</span><span class="sxs-lookup"><span data-stu-id="65f10-129">**Spare Part Ordered**</span></span>
* <span data-ttu-id="65f10-130">**Reservedel modtaget**</span><span class="sxs-lookup"><span data-stu-id="65f10-130">**Spare Part Received**</span></span>
* <span data-ttu-id="65f10-131">**Færdig**</span><span class="sxs-lookup"><span data-stu-id="65f10-131">**Finished**</span></span>  

### <a name="pending"></a><span data-ttu-id="65f10-132">Igangsat</span><span class="sxs-lookup"><span data-stu-id="65f10-132">Pending</span></span>

<span data-ttu-id="65f10-133">Med serviceordrestatus **Igangsat** angives, at reparationen kan starte eller fortsætte når som helst.</span><span class="sxs-lookup"><span data-stu-id="65f10-133">The service order status **Pending** indicates that the service can start or continue at any time.</span></span> <span data-ttu-id="65f10-134">Indstillingerne for reparationsstatus, **Ingen tidl. serv.**, **Henvist**, **Delvist repareret** og **Reservedel modtaget**, kan derfor tilknyttes denne serviceordrestatus.</span><span class="sxs-lookup"><span data-stu-id="65f10-134">Therefore, the repair status options of **Initial**, **Referred**, **Partly Serviced**, and **Spare Part Received** can be linked to this service order status.</span></span>  

### <a name="in-process"></a><span data-ttu-id="65f10-135">I arbejde</span><span class="sxs-lookup"><span data-stu-id="65f10-135">In Process</span></span>

<span data-ttu-id="65f10-136">Serviceordrestatussen **I arbejde** angiver, at reparationen er i gang.</span><span class="sxs-lookup"><span data-stu-id="65f10-136">The service order status **In Process** indicates that the service is in process.</span></span> <span data-ttu-id="65f10-137">Indstillingerne for reparationsstatus, **I arbejde** og **Reservedel modtaget**, kan derfor begge tilknyttes denne serviceordrestatus.</span><span class="sxs-lookup"><span data-stu-id="65f10-137">Therefore, the repair status options **In Process** and **Spare Part Ordered** can both be linked to this service order status.</span></span> <span data-ttu-id="65f10-138">Hvis du tilknytter statussen **Reservedel bestilt** til statussen **I arbejde**, skal du også tilknytte statussen **Reservedel modtaget** til denne serviceordrestatus.</span><span class="sxs-lookup"><span data-stu-id="65f10-138">If you link the **Spare Part Ordered** status to an **In Process** service order status, you must also link the **Spare Part Received** status to this service order status.</span></span>  

### <a name="on-hold"></a><span data-ttu-id="65f10-139">Afvent</span><span class="sxs-lookup"><span data-stu-id="65f10-139">On Hold</span></span>

<span data-ttu-id="65f10-140">Serviceordrestatussen **Afvent** angiver, at reparationen er midlertidigt i venteposition, fordi du venter på svar fra en kunde eller på en reservedel, før du kan påbegynde reparationen.</span><span class="sxs-lookup"><span data-stu-id="65f10-140">The service order status **On Hold** indicates that the service is temporarily on hold because you are waiting for a customer response or spare parts before the service can start.</span></span> <span data-ttu-id="65f10-141">Indstillingerne for reparationsstatus, **Tilbud færdigt**, **Reservedel bestilt** og **Venter på kunde**, kan derfor tilknyttes denne serviceordrestatus.</span><span class="sxs-lookup"><span data-stu-id="65f10-141">Therefore, the repair status options of **Quote Finished**, **Spare Part Ordered**, and **Waiting for Customer** can be linked to this service order status.</span></span>  

### <a name="finished"></a><span data-ttu-id="65f10-142">Udført</span><span class="sxs-lookup"><span data-stu-id="65f10-142">Finished</span></span>

<span data-ttu-id="65f10-143">Serviceordrestatussen **Udført** angiver, at reparationen er gjort færdig.</span><span class="sxs-lookup"><span data-stu-id="65f10-143">The service order status **Finished** indicates that the service has been completed.</span></span> <span data-ttu-id="65f10-144">Derfor er reparationsstatussen **Udført** knyttet til denne status.</span><span class="sxs-lookup"><span data-stu-id="65f10-144">Therefore, the **Finished** repair status is linked to this status.</span></span>  

## <a name="assigning-priority-to-service-order-status"></a><span data-ttu-id="65f10-145">Tildele prioritet til serviceordrestatus</span><span class="sxs-lookup"><span data-stu-id="65f10-145">Assigning Priority to Service Order Status</span></span>

<span data-ttu-id="65f10-146">Når en reparationsstatus for en serviceartikel ændres, identificerer programmet automatisk den serviceordrestatus, der er tilknyttet de forskellige indstillinger for reparationsstatus for alle serviceartiklerne i ordren.</span><span class="sxs-lookup"><span data-stu-id="65f10-146">When a repair status of a service item is changed, the service order status options linked to the different repair status options of all the service items in the order are identified.</span></span> <span data-ttu-id="65f10-147">Hvis serviceartiklerne er knyttet til to eller flere indstillinger for serviceordrestatus, skal du vælge statussen med den højeste prioritet automatisk.</span><span class="sxs-lookup"><span data-stu-id="65f10-147">If the service items are linked to two or more service order status options, the service order status option with the highest priority is selected.</span></span>  

<span data-ttu-id="65f10-148">Du skal afgøre, hvilken serviceordrestatus der indeholder de vigtigste oplysninger om serviceordrens status, og tildele denne status den højeste prioritet, osv.</span><span class="sxs-lookup"><span data-stu-id="65f10-148">You must decide which service order status contains the most important information about the status of the service order and assign that status the highest priority, and so on.</span></span>  

<span data-ttu-id="65f10-149">Når du derefter opretter en ny serviceordre, og du føjer serviceartikler til den, opdateres feltet **Prioritet** på serviceordrehovedet på basis af prioriteterne for serviceartiklerne.</span><span class="sxs-lookup"><span data-stu-id="65f10-149">Then, when you create a new service order and you add service items to it, the **Priority** field on the service order header is updated based on the priorities on the service items.</span></span>  

### <a name="example"></a><span data-ttu-id="65f10-150">Eksempel</span><span class="sxs-lookup"><span data-stu-id="65f10-150">Example</span></span>

<span data-ttu-id="65f10-151">Eksempel på en typisk tildeling af prioritetsniveau:</span><span class="sxs-lookup"><span data-stu-id="65f10-151">A typical priority level assignment could be as follows:</span></span>  

* <span data-ttu-id="65f10-152">I arbejde – Meget høj</span><span class="sxs-lookup"><span data-stu-id="65f10-152">In Process - High</span></span>  
* <span data-ttu-id="65f10-153">Igangsat - Høj</span><span class="sxs-lookup"><span data-stu-id="65f10-153">Pending - Medium high</span></span>  
* <span data-ttu-id="65f10-154">Afvent - Lav</span><span class="sxs-lookup"><span data-stu-id="65f10-154">On Hold - Medium low</span></span>  
* <span data-ttu-id="65f10-155">Udført - Meget lav</span><span class="sxs-lookup"><span data-stu-id="65f10-155">Finished - Low</span></span>  

<span data-ttu-id="65f10-156">Hvis én serviceartikel f.eks. har reparationsstatus **Ingen tidl. serv.** tilknyttet serviceordrestatussen **Igangsat**, en anden har **I arbejde** tilknyttet serviceordrestatussen **I arbejde**, og en tredje har **Reservedel bestilt** tilknyttet serviceordrestatus **Afvent**, vil den resulterende serviceordrestatus så blive **I arbejde**, fordi det har den højeste prioritet.</span><span class="sxs-lookup"><span data-stu-id="65f10-156">For example, if one service item has the repair status **Initial**, linked to the service order status **Pending**, another has the repair status **In Process**, linked to the service order status **In Process**, and a third has the repair status **Spare Part Ordered**, linked to the service order status **On Hold**, the resulting service order status will be **In Process** because this has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="65f10-157">Se også</span><span class="sxs-lookup"><span data-stu-id="65f10-157">See Also</span></span>

[<span data-ttu-id="65f10-158">Konfigurere statusser for serviceordrer og reparationer</span><span class="sxs-lookup"><span data-stu-id="65f10-158">Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)  
[<span data-ttu-id="65f10-159">Konfigurere Service</span><span class="sxs-lookup"><span data-stu-id="65f10-159">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]