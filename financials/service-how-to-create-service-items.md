---
title: "Sådan oprettes serviceartikler | Microsoft Docs"
description: "Når du modtager en ikke-registreret vare til reparation, kan du registrere den som en serviceartikel."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: acd3305694186793ccc5c305573f62c16a718531
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-service-items"></a><span data-ttu-id="ae0bc-103">Sådan gør du: Oprette serviceartikler</span><span class="sxs-lookup"><span data-stu-id="ae0bc-103">How to: Create Service Items</span></span>
<span data-ttu-id="ae0bc-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)] refererer termen "serviceartikel" til udstyr eller varer, der kræver service.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the term "service item" refers to equipment or items that require service.</span></span> <span data-ttu-id="ae0bc-105">Når du opretter en serviceordre, kan du angive de varer, der har brug for service.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-105">When you create a service order, you specify the items that need service.</span></span> <span data-ttu-id="ae0bc-106">I ordren kan du knytte en serviceartikel til en vare på lageret eller en serviceartikelgruppe.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-106">In the order, you can link a service item to an item in inventory or a service item group.</span></span>    

<span data-ttu-id="ae0bc-107">Når du modtager en vare, der kræver service, kan du registrere den som en serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-107">When you receive an item that needs service, you can register it as a service item.</span></span> <span data-ttu-id="ae0bc-108">Dette kan gøres på flere måder.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-108">There are several ways to do so.</span></span> <span data-ttu-id="ae0bc-109">Du kan f.eks. oprette en serviceartikel på siden **Serviceartikler** eller som en del af en anden proces, f.eks. når du arbejder med en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-109">For example, you can create a service item on the **Service Items** page, or as part of another process, such as when working with a service order.</span></span>   

## <a name="to-create-a-service-item"></a><span data-ttu-id="ae0bc-110">Oprette en serviceartikel</span><span class="sxs-lookup"><span data-stu-id="ae0bc-110">To create a service item</span></span>  
1. <span data-ttu-id="ae0bc-111">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceartikler**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae0bc-112">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a><span data-ttu-id="ae0bc-113">Sådan oprettes serviceartikler fra serviceordrer</span><span class="sxs-lookup"><span data-stu-id="ae0bc-113">To create service items within a service order</span></span>  
<span data-ttu-id="ae0bc-114">Når du modtager artikler, som du vil registrere som serviceartikler, kan du oprette dem som serviceartikler i vinduerne **Serviceordre** eller **Servicetilbud**.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-114">When you receive items for service that you want to register as service items, you can create them as service items in the **Service Order** or **Service Quote** windows.</span></span>  

1. <span data-ttu-id="ae0bc-115">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ae0bc-116">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="ae0bc-117">Vælg handlingen **Opret serviceartikel**.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-117">Choose the **Create Service Item** action.</span></span>  

    <span data-ttu-id="ae0bc-118">Der tildeles et nummer til serviceartiklen, og der oprettes et serviceartikelkort.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-118">A number is assigned to the service item and a service item card is created.</span></span> <span data-ttu-id="ae0bc-119">Feltet **Serviceartikelnr.** udfyldes med nummeret på den nye serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-119">The **Service Item No.** field is filled in with the number of the new service item.</span></span>

## <a name="to-create-a-service-item-when-shipping-items"></a><span data-ttu-id="ae0bc-120">Oprette en serviceartikel ved levering af varer</span><span class="sxs-lookup"><span data-stu-id="ae0bc-120">To create a service item when shipping items</span></span>  
<span data-ttu-id="ae0bc-121">Når du leverer varer enten ved at bogføre serviceordrer eller servicefakturaer, registreres de leverede varer automatisk som serviceartikler, hvis følgende betingelser er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-121">When you ship items by posting either service orders or service invoices, the shipped items are automatically registered as service items if the following condition is met.</span></span> <span data-ttu-id="ae0bc-122">Varerne skal høre til en serviceartikelgruppe, hvor afkrydsningsfeltet **Opret serviceartikel** er markeret.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-122">The items must belong to a service item group with the **Create Service Item** check box selected.</span></span> <span data-ttu-id="ae0bc-123">Hvis varerne har serienumre registreret i vinduet Varesporingslinje, kopieres disse oplysninger automatisk til feltet **Serienr.** på serviceartikelkortet ved oprettelse af serviceartikler.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-123">If the items have serial numbers registered in the Item Tracking Lines window, this information is copied automatically to the **Serial No.** field on the service item card when creating service items.</span></span>  

<span data-ttu-id="ae0bc-124">Nedenstående fremgangsmåde viser, hvordan du kan oprette serviceartikler, når du leverer varer i serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-124">The following procedure shows how to create service items when you ship items on service orders.</span></span>  

1. <span data-ttu-id="ae0bc-125">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ae0bc-126">Åbn den relevante serviceordre.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-126">Open the relevant service order.</span></span>  
3. <span data-ttu-id="ae0bc-127">Vælg handlingen **Bogfør** eller **Bogfør og udskriv**.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-127">Choose the **Post** or **Post and Print** action.</span></span>  
4. <span data-ttu-id="ae0bc-128">Vælg handlingen **Lever** eller **Lever og fakturer**.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-128">Choose the **Ship** or **Ship and Invoice** action.</span></span>  
5. <span data-ttu-id="ae0bc-129">Der oprettes automatisk serviceartikler for varerne i ordren, forudsat at disse hører til en serviceartikelgruppe, som du har defineret for at oprette serviceartikler.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-129">The service items are automatically created for the items on the order, provided these belong to a service item group that you have set up to create service items.</span></span> <span data-ttu-id="ae0bc-130">Hvis der er registreret specifikke serienumre i vinduet **Varesporingslinjer**, tildeles de til disse serviceartikler.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-130">If you registered specific serial numbers in the **Item Tracking Lines** window, they will be assigned to these service items.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ae0bc-131">Hvis en vare er en stykliste, og du har udfoldet styklisten, bliver styklistevarerne behandlet på samme måde som almindelige varer.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-131">If an item is a BOM and you have exploded the BOM, the exploded BOM items are processed in the same way as regular items.</span></span> <span data-ttu-id="ae0bc-132">Der oprettes serviceartikler baseret på samme betingelser for serviceartikelgruppe og eventuelt betingelser for serienummer.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-132">Service items are created based on the service items group condition and, optionally, the serial numbers condition.</span></span> <span data-ttu-id="ae0bc-133">Hvis der oprettes en serviceartikel for en udfoldet styklistevare, som består af andre styklistekomponenter, oprettes disse varer desuden som serviceartikelkomponenter for den udfoldede styklisteartikel.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-133">Additionally, if a service item is created for an exploded BOM item that is made up of other BOM components, these items are created as service item components for the exploded BOM service item.</span></span>  
>   
>  <span data-ttu-id="ae0bc-134">Hvis varen er en stykliste, og du ikke har udfoldet styklisten, oprettes der en serviceartikel til den på de samme betingelser for serviceartikelgruppen og eventuelt betingelsen for serienumre.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-134">If an item is a BOM and you have not exploded the BOM, a service item is created for it based on the service item group condition and, optionally, the serial numbers condition.</span></span>  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a><span data-ttu-id="ae0bc-135">Sådan indsættes startgebyrer for serviceartikler</span><span class="sxs-lookup"><span data-stu-id="ae0bc-135">To insert a starting fee for a service item</span></span>
1. <span data-ttu-id="ae0bc-136">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceopgaver**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Tasks**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae0bc-137">Vælg handlingen **Varekladde**.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-137">Choose the **Item Worksheet** action.</span></span>
3. <span data-ttu-id="ae0bc-138">Vælg servicelinjen, og vælg derefter **Handlinger**, vælg **Funktioner**, og vælg derefter handlingen **Indsæt startgebyr**.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-138">Choose the service line, and then choose **Actions**, choose **Functions**, and then choose **Insert Starting Fee** action.</span></span>  

    <span data-ttu-id="ae0bc-139">Der indsættes en servicelinje af typen **Omkostning** med startgebyr.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-139">A service line of type **Cost** is inserted with the starting fee.</span></span> <span data-ttu-id="ae0bc-140">Startgebyret gælder den valgte serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="ae0bc-140">The starting fee applies to the selected service item.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae0bc-141">Se også</span><span class="sxs-lookup"><span data-stu-id="ae0bc-141">See Also</span></span>  
[<span data-ttu-id="ae0bc-142">Fremgangsmåde: Konfigurere serviceartikler og serviceartikelkomponenter</span><span class="sxs-lookup"><span data-stu-id="ae0bc-142">How to: Set Up Service Items and Service Item Components</span></span>](service-how-setup-service-items.md)  
[<span data-ttu-id="ae0bc-143">Konfigurere Service</span><span class="sxs-lookup"><span data-stu-id="ae0bc-143">Setting Up Service Management</span></span>](service-setup-service.md)  
[<span data-ttu-id="ae0bc-144">Service Management</span><span class="sxs-lookup"><span data-stu-id="ae0bc-144">Service Management</span></span>](service-service.md)  
