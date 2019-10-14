---
title: Opsætning for serviceartikler og serviceartikelkomponenter | Microsoft Docs
description: Få mere at vide om de ting, du skal konfigurere, før du kan bruge serviceartikler, herunder standardværdier som f.eks. svartid, kontraktrabatprocent og serviceprisgruppe.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 41c2a4ea5a79f7fe66eaae93c7bffa2c7bbe3d2e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316112"
---
# <a name="set-up-service-items-and-service-item-components"></a><span data-ttu-id="d18ad-103">Konfigurere serviceartikler og serviceartikelkomponenter</span><span class="sxs-lookup"><span data-stu-id="d18ad-103">Set Up Service Items and Service Item Components</span></span>
<span data-ttu-id="d18ad-104">Hvis du vil arbejde med serviceartikler, skal du oprette følgende</span><span class="sxs-lookup"><span data-stu-id="d18ad-104">To work with service items, you must set up the following</span></span>

* <span data-ttu-id="d18ad-105">Serviceartikelgrupper.</span><span class="sxs-lookup"><span data-stu-id="d18ad-105">Service item groups.</span></span>
* <span data-ttu-id="d18ad-106">Valgfri</span><span class="sxs-lookup"><span data-stu-id="d18ad-106">Optional</span></span>

## <a name="to-set-up-service-item-groups"></a><span data-ttu-id="d18ad-107">Sådan defineres serviceartikelgrupper</span><span class="sxs-lookup"><span data-stu-id="d18ad-107">To set up service item groups</span></span>
<span data-ttu-id="d18ad-108">Du kan definere grupper af varer, der er beslægtede med hensyn til reparation og vedligeholdelse.</span><span class="sxs-lookup"><span data-stu-id="d18ad-108">You can set up groups of items that are related in terms of repair and maintenance.</span></span> <span data-ttu-id="d18ad-109">Du kan definere standardværdier for serviceartikler i en serviceartikelgruppe, som f.eks. svartid, kontraktrabatprocent og serviceprisgruppe.</span><span class="sxs-lookup"><span data-stu-id="d18ad-109">You can define default values for service items in a service item group, such as response time, contract discount percent, and service price group.</span></span> <span data-ttu-id="d18ad-110">Du kan vælge, at varer i en serviceartikelgruppe automatisk registreres som serviceartikler, når de bliver solgt.</span><span class="sxs-lookup"><span data-stu-id="d18ad-110">For items in a service item group, you can select whether you want them to be automatically registered as service items when they are sold.</span></span>  

<span data-ttu-id="d18ad-111">Du tildeler serviceartikelgrupper til varer på **Vare**-kortet og til serviceartikler på **Serviceartikel**-kortet.</span><span class="sxs-lookup"><span data-stu-id="d18ad-111">You assign service item groups to items on the **Item** card, and to service items on the **Service Item** card.</span></span>  

1. <span data-ttu-id="d18ad-112">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceartikelgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d18ad-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d18ad-113">Opret en ny serviceartikelgruppe.</span><span class="sxs-lookup"><span data-stu-id="d18ad-113">Create a new service item group.</span></span>  
3. <span data-ttu-id="d18ad-114">Udfyld felterne **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="d18ad-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="d18ad-115">Angiv den standardkontraktrabatprocent, som skal gælde for serviceartiklerne i gruppen, i feltet **Kontraktrabatpct. (standard)**.</span><span class="sxs-lookup"><span data-stu-id="d18ad-115">In the **Default Contract Discount %** field, enter the default contract discount percentage that you want the service items in the group to have.</span></span>  
5. <span data-ttu-id="d18ad-116">Angiv den standardserviceprisgruppekode, som serviceartiklerne i gruppen skal have, i feltet **Serviceprisgrp.kode (standard)**.</span><span class="sxs-lookup"><span data-stu-id="d18ad-116">In the **Default Serv. Price Group Code** field, enter the default service price group code that you want the service items in the group to have.</span></span>  
6. <span data-ttu-id="d18ad-117">Angiv den standardsvartid i timer, der skal gælde for serviceartiklerne i gruppen, i feltet **Standardsvartid (timer)**.</span><span class="sxs-lookup"><span data-stu-id="d18ad-117">In the **Default Response Time (Hours)** field, enter the default response time in hours that you want the service items in the group to have.</span></span>  
7. <span data-ttu-id="d18ad-118">Hvis varerne i gruppen skal registreres som serviceartikler, når de bliver solgt, skal du markere feltet **Opret serviceartikel**.</span><span class="sxs-lookup"><span data-stu-id="d18ad-118">If you want to register the items in the group as service items when they are sold, select the **Create Service Item** field.</span></span>  

## <a name="to-set-up-service-item-components"></a><span data-ttu-id="d18ad-119">Sådan defineres serviceartikelkomponenter</span><span class="sxs-lookup"><span data-stu-id="d18ad-119">To set up service item components</span></span>
<span data-ttu-id="d18ad-120">En serviceartikel kan bestå af flere komponenter, som kan udskiftes med reservedele, når varen repareres.</span><span class="sxs-lookup"><span data-stu-id="d18ad-120">A service item can consist of several components, which can be replaced with spare parts when the item is serviced.</span></span> <span data-ttu-id="d18ad-121">Komponenterne defineres på siden **Komponentoversigt – serviceart**.</span><span class="sxs-lookup"><span data-stu-id="d18ad-121">These components are set up on the **Service Item Component List** page.</span></span> <span data-ttu-id="d18ad-122">Hvis du desuden vil definere komponenter for serviceartikler, som er styklister, kan du kopiere styklistevarerne og oprette dem som serviceartikelkomponenter.</span><span class="sxs-lookup"><span data-stu-id="d18ad-122">Additionally, if you want to set up components for service items that are BOMs, you can copy the BOM items and create them as service item components.</span></span>

1. <span data-ttu-id="d18ad-123">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicevarer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d18ad-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="d18ad-124">Åbn den serviceartikel, som du vil definere komponenter for.</span><span class="sxs-lookup"><span data-stu-id="d18ad-124">Open the service item for which you want to set up components.</span></span>  
3. <span data-ttu-id="d18ad-125">Vælg handlingen **Komponenter**.</span><span class="sxs-lookup"><span data-stu-id="d18ad-125">Choose the **Components** action.</span></span> <span data-ttu-id="d18ad-126">Siden **Komponentoversigt - serviceart.** åbnes.</span><span class="sxs-lookup"><span data-stu-id="d18ad-126">The **Service Item Component List** page opens.</span></span>  
4. <span data-ttu-id="d18ad-127">Tilføj en ny komponent.</span><span class="sxs-lookup"><span data-stu-id="d18ad-127">Add a new component.</span></span>  
5. <span data-ttu-id="d18ad-128">I feltet **Type** skal du vælge **Serviceartikel**, hvis komponenten selv er en registreret serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="d18ad-128">In the **Type** field, choose **Service Item** if the component itself is a registered service item.</span></span> <span data-ttu-id="d18ad-129">Ellers skal du vælge **Vare**.</span><span class="sxs-lookup"><span data-stu-id="d18ad-129">Otherwise, select **Item**.</span></span>  
6. <span data-ttu-id="d18ad-130">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="d18ad-130">In the **No.**</span></span> <span data-ttu-id="d18ad-131">skal du vælge den artikel eller serviceartikel, som er en komponent i serviceartiklen.</span><span class="sxs-lookup"><span data-stu-id="d18ad-131">field, choose the item or service item that is a component of the service item.</span></span>  

## <a name="to-set-up-service-item-components-from-a-bom"></a><span data-ttu-id="d18ad-132">Sådan defineres serviceartikelkomponenter fra styklister</span><span class="sxs-lookup"><span data-stu-id="d18ad-132">To set up service item components from a BOM</span></span>
1.  <span data-ttu-id="d18ad-133">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicevarer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d18ad-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d18ad-134">Åbn den serviceartikel, som du vil definere komponenter for ud fra en stykliste.</span><span class="sxs-lookup"><span data-stu-id="d18ad-134">Open the service item for which you want to set up components from a BOM.</span></span>  
3. <span data-ttu-id="d18ad-135">Vælg handlingen **Komponenter**.</span><span class="sxs-lookup"><span data-stu-id="d18ad-135">Choose the **Components** action.</span></span> <span data-ttu-id="d18ad-136">Siden **Komponentoversigt - serviceart.** åbnes.</span><span class="sxs-lookup"><span data-stu-id="d18ad-136">The **Service Item Component List** page opens.</span></span>  
4. <span data-ttu-id="d18ad-137">Vælg handlingen **Kopier fra stykliste**.</span><span class="sxs-lookup"><span data-stu-id="d18ad-137">Choose the **Copy from BOM** action.</span></span>  

    <span data-ttu-id="d18ad-138">Hvis varen, som serviceartiklen er knyttet til, er en stykliste, oprettes der automatisk komponenter for alle varerne i styklisten.</span><span class="sxs-lookup"><span data-stu-id="d18ad-138">If the item that the service item is linked to is a BOM, the components for all the items in the BOM are created automatically.</span></span>  

## <a name="to-set-up-a-service-shelf"></a><span data-ttu-id="d18ad-139">Sådan defineres serviceplaceringer</span><span class="sxs-lookup"><span data-stu-id="d18ad-139">To set up a service shelf</span></span>
<span data-ttu-id="d18ad-140">Du kan oprette serviceplaceringer, der identificerer, hvor du gemmer dine serviceartikler.</span><span class="sxs-lookup"><span data-stu-id="d18ad-140">You can set up service shelves that identify where you store your service items.</span></span> <span data-ttu-id="d18ad-141">Du tildeler serviceplaceringer til serviceartikler på siden **Serviceordre** og siden **Serviceartikelkladde**.</span><span class="sxs-lookup"><span data-stu-id="d18ad-141">You assign service shelves to service items on the **Service Order** and **Service Item Worksheet** pages.</span></span>  

1. <span data-ttu-id="d18ad-142">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceplacering**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d18ad-142">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Shelves**, and then choose the related link.</span></span>
2. <span data-ttu-id="d18ad-143">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="d18ad-143">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="d18ad-144">Se også</span><span class="sxs-lookup"><span data-stu-id="d18ad-144">See Also</span></span>
<span data-ttu-id="d18ad-145">[Definere koder for standardservices](service-how-setup-service-coding.md) </span><span class="sxs-lookup"><span data-stu-id="d18ad-145">[Set Up Codes for Standard Services](service-how-setup-service-coding.md) </span></span>  
[<span data-ttu-id="d18ad-146">Konfigurere fejlfinding</span><span class="sxs-lookup"><span data-stu-id="d18ad-146">Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md)
