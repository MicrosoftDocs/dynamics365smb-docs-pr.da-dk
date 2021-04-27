---
title: Import af mange varebilleder fra en zip-fil | Microsoft Docs
description: Du kan importere flere varebilleder på en gang. Navngiv blot dine billedfiler svarende til dine varenumre, komprimer dem til en zip-fil, og benyt siden Importer varebilleder for at styre, hvilke varebilleder, der skal importeres.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4d4221ca3af412cc2548634cc6920f58171233ce
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785919"
---
# <a name="import-multiple-item-pictures"></a><span data-ttu-id="a7e2f-104">Importer flere varebilleder</span><span class="sxs-lookup"><span data-stu-id="a7e2f-104">Import Multiple Item Pictures</span></span>
<span data-ttu-id="a7e2f-105">Du kan importere flere varebilleder på en gang.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-105">You can import multiple item pictures in one go.</span></span> <span data-ttu-id="a7e2f-106">Navngiv blot dine billedfiler svarende til dine varenumre, komprimer dem til en zip-fil, og benyt siden **Importer varebilleder** for at styre, hvilke varebilleder, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-106">Simply name your picture files with names corresponding to your item numbers, compress them to a ZIP file, and then use the **Import Item Pictures** page to manage which item pictures to import.</span></span>

<span data-ttu-id="a7e2f-107">Alle standardfilformater er understøttet.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-107">All common file formats are supported.</span></span>

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><span data-ttu-id="a7e2f-108">Navngivning af billedfiler efter varenavne og klargøring af zip-filen</span><span class="sxs-lookup"><span data-stu-id="a7e2f-108">To name picture files by the item names and prepare the ZIP file</span></span>
1. <span data-ttu-id="a7e2f-109">Navngiv hver fil i henhold til den pågældende vares nummer på lokationen, hvor du dine varebilleder er gemt.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-109">At the location where your item pictures are stored, name each files according to the number of the related item.</span></span> <span data-ttu-id="a7e2f-110">Eksempler:</span><span class="sxs-lookup"><span data-stu-id="a7e2f-110">For example:</span></span>

    |<span data-ttu-id="a7e2f-111">Varenr.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-111">Item No.</span></span>|<span data-ttu-id="a7e2f-112">Filnavn</span><span class="sxs-lookup"><span data-stu-id="a7e2f-112">File Name</span></span>|
    |-|-|
    |<span data-ttu-id="a7e2f-113">1000</span><span class="sxs-lookup"><span data-stu-id="a7e2f-113">1000</span></span>|<span data-ttu-id="a7e2f-114">1000.bmp</span><span class="sxs-lookup"><span data-stu-id="a7e2f-114">1000.bmp</span></span>|
    |<span data-ttu-id="a7e2f-115">1001</span><span class="sxs-lookup"><span data-stu-id="a7e2f-115">1001</span></span>|<span data-ttu-id="a7e2f-116">1001.bmp</span><span class="sxs-lookup"><span data-stu-id="a7e2f-116">1001.bmp</span></span>|
    |<span data-ttu-id="a7e2f-117">1002</span><span class="sxs-lookup"><span data-stu-id="a7e2f-117">1002</span></span>|<span data-ttu-id="a7e2f-118">1002.bmp</span><span class="sxs-lookup"><span data-stu-id="a7e2f-118">1002.bmp</span></span>|

2. <span data-ttu-id="a7e2f-119">Saml alle filerne i en zip-fil.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-119">Collect all the files in a ZIP file.</span></span> <span data-ttu-id="a7e2f-120">F.eks.: I Windows Explorer vælger du filerne, og derefter vælger du **Send til**, **Komprimeret (zipped) mappe**.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-120">For example, in Windows Explorer, select the files, and then choose **Send to**, **Compressed (zipped) folder**.</span></span>     

## <a name="to-import-item-pictures"></a><span data-ttu-id="a7e2f-121">Importer varebilleder</span><span class="sxs-lookup"><span data-stu-id="a7e2f-121">To import item pictures</span></span>
1. <span data-ttu-id="a7e2f-122">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lageropsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="a7e2f-123">Vælg handlingen **Importer billeder**.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-123">Choose the **Import Item Pictures** action.</span></span>
3. <span data-ttu-id="a7e2f-124">Find feltet **Vælg en zip-fil**, vælg den relevante zip-mappe, og vælg dernæst knappen **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-124">In the **Select a ZIP file** field, select the relevant ZIP folder, and then choose the **Open** button.</span></span>

    <span data-ttu-id="a7e2f-125">Der oprettes en linje for hver vare og billede på siden **Importer varebilleder**.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-125">A line for each item and picture is created on the **Import Item Pictures** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a7e2f-126">For varekort, der allerede har et billede, vælges afkrydsningsfeltet **Billede findes allerede**.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-126">For item cards that already have a picture, the **Picture Already Exists** check box is selected.</span></span> <span data-ttu-id="a7e2f-127">Hvis du ikke ønsker, at eksisterende billeder erstattes, fravælges afkrydsningsfeltet **Erstat billeder**.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-127">If you do not want any existing pictures to be replaced, deselect the **Replace Pictures** check box.</span></span> <span data-ttu-id="a7e2f-128">Hvis du ikke ønsker, at individuelle eksisterende billeder erstattes, skal du slette de pågældende linjer.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-128">If you do not want individual existing pictures to be replaced, delete the lines in question.</span></span>

3. <span data-ttu-id="a7e2f-129">Vælg handlingen **Importer billeder**.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-129">Choose the **Import Pictures** action.</span></span>

<span data-ttu-id="a7e2f-130">Feltet **Importstatus** opdateres for at vise, om billedimporten blev annulleret eller gennemført.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-130">The **Import Status** field is updated to show if the picture import was skipped or completed.</span></span>       

## <a name="see-also"></a><span data-ttu-id="a7e2f-131">Se også</span><span class="sxs-lookup"><span data-stu-id="a7e2f-131">See Also</span></span>
[<span data-ttu-id="a7e2f-132">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="a7e2f-132">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="a7e2f-133">Oprette nummerserie</span><span class="sxs-lookup"><span data-stu-id="a7e2f-133">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="a7e2f-134">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="a7e2f-134">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a7e2f-135">Køb</span><span class="sxs-lookup"><span data-stu-id="a7e2f-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="a7e2f-136">Salg</span><span class="sxs-lookup"><span data-stu-id="a7e2f-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="a7e2f-137">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a7e2f-137">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]