---
title: "Bruge udvidelsen QuickBooks-overførsel | Microsoft Docs"
description: Beskriver, hvordan du bruger udvidelsen til at importere debitorer, kreditorer, varer og konti fra QuickBooks Desktop til Dynamics 365 for Financials.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: fdda803b7cc2f93ae4d7353be28282dc60d904d8
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-business-edition"></a><span data-ttu-id="44f8b-103">Udvidelsen QuickBooks-dataoverførsel til Dynamics 365 Business edition</span><span class="sxs-lookup"><span data-stu-id="44f8b-103">The QuickBooks Data Migration Extension for Dynamics 365 Business edition</span></span>
<span data-ttu-id="44f8b-104">Denne udvidelse gør det nemt at overflytte debitorer, kreditorer, varer og konti fra QuickBooks til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="44f8b-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="44f8b-105">Hvis din virksomhed bruger QuickBooks i dag, kan du eksportere de relevante oplysninger og derefter åbne en assisteret opsætningsvejledning for at overføre dataene til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="44f8b-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="44f8b-106">Du kan finde flere oplysninger under [Importere virksomhedsdata fra andre økonomisystemer](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="44f8b-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="44f8b-107">Udlæse data fra QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="44f8b-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="44f8b-108">Du skal have udlæst nogle eller alle eksisterende kunder, leverandører, lagervarer og konti til en IIF-fil (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="44f8b-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="44f8b-109">Udvidelsen Overførsel af QuickBooks-data indeholder en standardtilknytning af QuickBooks-data, så du kan bruge dine eksisterende data til at teste den nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-virksomhed.</span><span class="sxs-lookup"><span data-stu-id="44f8b-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="44f8b-110">Standardtilknytningen er tilstrækkelig i de fleste tilfælde, men du kan ændre tilknytningen i den assisterede opsætningsvejledning.</span><span class="sxs-lookup"><span data-stu-id="44f8b-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="44f8b-111">I QuickBooks indeholder menuen Filer et værktøj til eksport af lister.</span><span class="sxs-lookup"><span data-stu-id="44f8b-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="44f8b-112">I forbindelse med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du eksportere følgende lister:</span><span class="sxs-lookup"><span data-stu-id="44f8b-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="44f8b-113">Debitoroversigt</span><span class="sxs-lookup"><span data-stu-id="44f8b-113">Customer List</span></span>  
* <span data-ttu-id="44f8b-114">Kreditoroversigt</span><span class="sxs-lookup"><span data-stu-id="44f8b-114">Vendor List</span></span>  
* <span data-ttu-id="44f8b-115">Vareoversigt</span><span class="sxs-lookup"><span data-stu-id="44f8b-115">Item List</span></span>  
* <span data-ttu-id="44f8b-116">Kontooversigt</span><span class="sxs-lookup"><span data-stu-id="44f8b-116">Account List</span></span>  

<span data-ttu-id="44f8b-117">De eksporterede data gemmes som en IIF-fil, som du derefter kan overføre til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="44f8b-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="44f8b-118">Sådan finder du udvidelsen Overførsel af QuickBooks-data</span><span class="sxs-lookup"><span data-stu-id="44f8b-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="44f8b-119">Udvidelsen Overførsel af QuickBooks-data er installeret og klar til brug som en integreret del af den assisterende opsætningsvejledning til dataoverførsel.</span><span class="sxs-lookup"><span data-stu-id="44f8b-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="44f8b-120">Hvis du er klar til at komme i gang nu og har eksporteret dine data fra QuickBooks, skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Assisteret opsætning** og derefter vælge det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="44f8b-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="44f8b-121">Vælg **Overflyt forretningsdata**, og følg derefter trinnene i vejledningen.</span><span class="sxs-lookup"><span data-stu-id="44f8b-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="44f8b-122">Se også</span><span class="sxs-lookup"><span data-stu-id="44f8b-122">See Also</span></span>
[<span data-ttu-id="44f8b-123">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="44f8b-123">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="44f8b-124">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="44f8b-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

