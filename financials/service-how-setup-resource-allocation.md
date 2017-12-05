---
title: Konfigurere ressourceallokering | Microsoft Docs
description: "Få at vide, hvordan systemet kan hjælpe med at sikre, at den person, du tildeler en serviceydelse, har de nødvendige kvalifikationer til at udføre ydelsen."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 08/22/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6c20c0b346186adad6e4b125dbd48bd0d3f56ab2
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-resource-allocation"></a><span data-ttu-id="f1737-103">Fremgangsmåde: Definere ressourceallokering</span><span class="sxs-lookup"><span data-stu-id="f1737-103">How to: Set Up Resource Allocation</span></span>
<span data-ttu-id="f1737-104">Det er vigtigt at finde en ressource, der er kvalificeret til at udføre arbejdet, for at sikre, at en serviceopgave udføres korrekt.</span><span class="sxs-lookup"><span data-stu-id="f1737-104">To ensure that a service task is performed well, it's important to find a resource who is qualified to do the work.</span></span> <span data-ttu-id="f1737-105">Du kan konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)], så det er nemt at allokere en person, der har de korrekte kvalifikationer til sagen.</span><span class="sxs-lookup"><span data-stu-id="f1737-105">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] so that it's easy to allocate someone who has the right skills for the job.</span></span> <span data-ttu-id="f1737-106">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kalder vi det _ressourceallokering_.</span><span class="sxs-lookup"><span data-stu-id="f1737-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], we call this _resource allocation_.</span></span> <span data-ttu-id="f1737-107">Du kan allokere ressourcer, alt efter deres færdigheder og tilgængelighed, eller om de er i samme servicezone som kunden.</span><span class="sxs-lookup"><span data-stu-id="f1737-107">You can allocate resources based on their skill, availability, or whether they are in the same service zone as the customer.</span></span> 

<span data-ttu-id="f1737-108">Når du vil bruge ressourceallokering, skal du angive:</span><span class="sxs-lookup"><span data-stu-id="f1737-108">To use resource allocation, you must set up:</span></span>  
  
* <span data-ttu-id="f1737-109">De kvalifikationer, der kræves til at reparere og vedligeholde serviceartikler.</span><span class="sxs-lookup"><span data-stu-id="f1737-109">The skills required to repair and maintain service items.</span></span> <span data-ttu-id="f1737-110">Du kan tildele dem til serviceartikler og ressourcer.</span><span class="sxs-lookup"><span data-stu-id="f1737-110">You assign these to service items and resources.</span></span>  
* <span data-ttu-id="f1737-111">Geografiske områder, kaldet zoner, som du har defineret for dit marked.</span><span class="sxs-lookup"><span data-stu-id="f1737-111">Geographic regions, called zones, that you define for your market.</span></span> <span data-ttu-id="f1737-112">For eksempel øst, vest, centralt osv.</span><span class="sxs-lookup"><span data-stu-id="f1737-112">For example, East, West, Central, and so on.</span></span> <span data-ttu-id="f1737-113">Du tildeler grupperne til debitorer og ressourcer.</span><span class="sxs-lookup"><span data-stu-id="f1737-113">You assign these to customers and resources.</span></span>  
* <span data-ttu-id="f1737-114">Om der skal vises ressourcekvalifikationer og zoner, og om der skal vises en advarsel, hvis en bruger vælger en ukvalificeret ressource eller en ressource, som ikke er i kundezonen.</span><span class="sxs-lookup"><span data-stu-id="f1737-114">Whether to display resource skills and zones, and whether to display a warning if someone chooses unqualified resource, or a resource that is not in the customer zone.</span></span>  

## <a name="to-set-up-skills"></a><span data-ttu-id="f1737-115">Sådan oprettes kvalifikationer</span><span class="sxs-lookup"><span data-stu-id="f1737-115">To set up skills</span></span>
1. <span data-ttu-id="f1737-116">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kvalifikationer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f1737-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Skills**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f1737-117">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f1737-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><span data-ttu-id="f1737-118">Sådan tildeles kvalifikationer til serviceartikler og ressourcer</span><span class="sxs-lookup"><span data-stu-id="f1737-118">To assign skills to service items and resources</span></span>
1. <span data-ttu-id="f1737-119">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceartikler** eller **Ressourcer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f1737-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f1737-120">Åbn kortet for serviceartiklen eller ressourcen, og vælg derefter en af følgende:</span><span class="sxs-lookup"><span data-stu-id="f1737-120">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="f1737-121">Vælg **Ressourcekvalifikationer** for serviceartikler.</span><span class="sxs-lookup"><span data-stu-id="f1737-121">For service items, choose **Resource Skills**.</span></span>  
    * <span data-ttu-id="f1737-122">Vælg **Kvalifikationer** for ressourcer.</span><span class="sxs-lookup"><span data-stu-id="f1737-122">For resources, choose **Skills**.</span></span>  

## <a name="to-set-up-zones"></a><span data-ttu-id="f1737-123">Sådan defineres zoner</span><span class="sxs-lookup"><span data-stu-id="f1737-123">To set up zones</span></span>
1. <span data-ttu-id="f1737-124">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Zoner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f1737-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Zones**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f1737-125">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f1737-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><span data-ttu-id="f1737-126">Sådan tildeles zoner til kunder og ressourcer</span><span class="sxs-lookup"><span data-stu-id="f1737-126">To assign zones to customers and resources</span></span> 
1. <span data-ttu-id="f1737-127">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kunder** eller **Ressourcer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f1737-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f1737-128">Åbn kortet for serviceartiklen eller ressourcen, og vælg derefter en af følgende:</span><span class="sxs-lookup"><span data-stu-id="f1737-128">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="f1737-129">For kunder skal du vælge en zone i feltet **Servicezonekode**.</span><span class="sxs-lookup"><span data-stu-id="f1737-129">For customers, choose a zone in the **Service Zone Code** field.</span></span>  
    * <span data-ttu-id="f1737-130">For ressourcer skal du vælge handlingen **Servicezoner**.</span><span class="sxs-lookup"><span data-stu-id="f1737-130">For resources, choose the **Service Zones** action.</span></span>  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><span data-ttu-id="f1737-131">Sådan angiver du, hvad der skal vises, når en ressource vælges</span><span class="sxs-lookup"><span data-stu-id="f1737-131">To specify what to show when a resource is chosen</span></span>
1. <span data-ttu-id="f1737-132">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceopsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f1737-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="f1737-133">I feltet **Indstilling for ressourcekval.** skal du vælge en af de indstillinger, der er beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f1737-133">In the **Resource Skills Option** field, choose one of the options described in the following table.</span></span>  
  
    |<span data-ttu-id="f1737-134">**Indstilling**</span><span class="sxs-lookup"><span data-stu-id="f1737-134">**Option**</span></span>|<span data-ttu-id="f1737-135">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="f1737-135">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="f1737-136">Vis kode</span><span class="sxs-lookup"><span data-stu-id="f1737-136">Code Shown</span></span> | <span data-ttu-id="f1737-137">Viser kun koden.</span><span class="sxs-lookup"><span data-stu-id="f1737-137">Displays the code only.</span></span>|  
    |<span data-ttu-id="f1737-138">Vis advarsel</span><span class="sxs-lookup"><span data-stu-id="f1737-138">Warning Displayed</span></span> | <span data-ttu-id="f1737-139">Viser oplysninger og en advarsel, hvis du vælger en ressource, som ikke er kvalificeret.</span><span class="sxs-lookup"><span data-stu-id="f1737-139">Shows the information and displays a warning if you choose a resource that is not qualified.</span></span>|  
    |<span data-ttu-id="f1737-140">Bruges ikke</span><span class="sxs-lookup"><span data-stu-id="f1737-140">Not Used</span></span> | <span data-ttu-id="f1737-141">Viser ikke disse oplysninger.</span><span class="sxs-lookup"><span data-stu-id="f1737-141">Does not show this information.</span></span>|  

## <a name="to-update-resource-capacity"></a><span data-ttu-id="f1737-142">Sådan opdateres ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="f1737-142">To update resource capacity</span></span>  
<span data-ttu-id="f1737-143">Du skal muligvis ændre ressourcernes kapacitet.</span><span class="sxs-lookup"><span data-stu-id="f1737-143">You may need to change the capacity of resources.</span></span>  
  
1. <span data-ttu-id="f1737-144">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourcekapacitet**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f1737-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Capacity**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f1737-145">Vælg ressourcen, og vælg derefter handlingen **Angiv kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="f1737-145">Choose the resource, and then choose the **Set Capacity** action.</span></span>  
3. <span data-ttu-id="f1737-146">Foretag ændringerne, og vælg derefter **Opdater kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="f1737-146">Make the changes, and then choose **Update Capacity**.</span></span>  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><span data-ttu-id="f1737-147">Sådan opdateres kvalifikationer for artikler, serviceartikler eller serviceartikelgrupper</span><span class="sxs-lookup"><span data-stu-id="f1737-147">To update skills for items, service items, or service item groups</span></span>
<span data-ttu-id="f1737-148">Hvis du vil ændre kvalifikationskoder, der er tildelt til varer, for eksempel fra **PC** til **PCS**, kan du gøre det for en vare, en serviceartikel eller for alle varer i en serviceartikelgruppe.</span><span class="sxs-lookup"><span data-stu-id="f1737-148">If you want to change the skill codes assigned to items, for example from **PC** to **PCS**, you can do so either for an item, service item, or for all items in a service item group.</span></span>  
  
1. <span data-ttu-id="f1737-149">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer** eller **Serviceartikel** eller **Serviceartikelgruppe**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f1737-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items** or **Service Item**, or **Service Item Group**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f1737-150">Vælg den enhed, der skal opdateres, og vælg derefter handlingen **Ressourcekvalifikationer**.</span><span class="sxs-lookup"><span data-stu-id="f1737-150">Choose the entity to update, and then choose the **Resource Skills** action.</span></span>  
3. <span data-ttu-id="f1737-151">Vælg den relevante kvalifikationskode i feltet **Kvalifikationskode** på linjen med den kode, der skal ændres.</span><span class="sxs-lookup"><span data-stu-id="f1737-151">On the line with the code to be changed, in the **Skill Code** field, choose the relevant skill code.</span></span>  
4.  <span data-ttu-id="f1737-152">Hvis artiklen er knyttet til serviceartikler, åbnes en dialogboks med følgende to indstillinger:</span><span class="sxs-lookup"><span data-stu-id="f1737-152">If the item has associated service items, a dialog box opens with the following two options:</span></span>  
  
    * <span data-ttu-id="f1737-153">Skift kvalifikationskoderne til den valgte værdi: Vælg denne indstilling, hvis du vil erstatte den gamle kvalifikationskode med den nye kode for alle relaterede serviceartikler.</span><span class="sxs-lookup"><span data-stu-id="f1737-153">Change the skill codes to the selected value: Select this option if you want to replace the old skill code with the new one on all the related service items.</span></span>  
    * <span data-ttu-id="f1737-154">Slet kvalifikationskoderne, eller opdater deres relation: Vælg denne indstilling, hvis du kun vil ændre kvalifikationskode for denne vare.</span><span class="sxs-lookup"><span data-stu-id="f1737-154">Delete the skill codes or update their relation: Select this option if you want to change the skill code on this item only.</span></span> <span data-ttu-id="f1737-155">Kvalifikationskoden for de relaterede serviceartikler bliver tildelt igen, dvs. feltet **Tildelt fra** opdateres.</span><span class="sxs-lookup"><span data-stu-id="f1737-155">The skill code on the related service items will be reassigned, that is, the **Assigned From** field will be updated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1737-156">Se også</span><span class="sxs-lookup"><span data-stu-id="f1737-156">See Also</span></span>
[<span data-ttu-id="f1737-157">Sådan gør du: Allokere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f1737-157">How to: Allocate Resources</span></span>](service-how-to-allocate-resources.md)  
[<span data-ttu-id="f1737-158">Sådan gør du: Definere arbejdstimer og serviceåbningstider</span><span class="sxs-lookup"><span data-stu-id="f1737-158">How to: Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)  
[<span data-ttu-id="f1737-159">Fremgangsmåde: Definere fejlrapportering</span><span class="sxs-lookup"><span data-stu-id="f1737-159">How to: Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md)  
[<span data-ttu-id="f1737-160">Fremgangsmåde: Definere koder for standardservices</span><span class="sxs-lookup"><span data-stu-id="f1737-160">How to: Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)  
 

