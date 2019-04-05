---
title: Sådan spærres varer mod salg eller køb
description: I Business Central kan en vare være markeret som spærret for salg, spærret for køb eller spærret i alle sammenhænge.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 0d5ad688cfa6fb58e8383692362105beeee386f8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792196"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="d4b99-103">Spærre varer mod salg eller køb</span><span class="sxs-lookup"><span data-stu-id="d4b99-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="d4b99-104">Du kan spærre for, at en vare angives på salgs- eller købslinjer og for, at den bogføres i nogen posteringer.</span><span class="sxs-lookup"><span data-stu-id="d4b99-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="d4b99-105">Tabellen nedenfor viser, hvad der sker, når varer spærres.</span><span class="sxs-lookup"><span data-stu-id="d4b99-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="d4b99-106">Indstilling</span><span class="sxs-lookup"><span data-stu-id="d4b99-106">Option</span></span>|<span data-ttu-id="d4b99-107">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d4b99-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="d4b99-108">**Spærret salg**</span><span class="sxs-lookup"><span data-stu-id="d4b99-108">**Sales Blocked**</span></span>|<span data-ttu-id="d4b99-109">Du kan ikke angive varen i et salgsdokument eller i en salgsvarekladde.</span><span class="sxs-lookup"><span data-stu-id="d4b99-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="d4b99-110">**Spærret køb**</span><span class="sxs-lookup"><span data-stu-id="d4b99-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="d4b99-111">Du kan ikke angive varen i et købsdokument, i en købsvarekladde eller i købsplanlægningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="d4b99-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="d4b99-112">**Spærret**</span><span class="sxs-lookup"><span data-stu-id="d4b99-112">**Blocked**</span></span>|<span data-ttu-id="d4b99-113">Du kan ikke bruge varen til nogen varetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="d4b99-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="d4b99-114">Du kan finde flere oplysninger om spærring af en vare i alle sammenhænge på varekortet.</span><span class="sxs-lookup"><span data-stu-id="d4b99-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="d4b99-115">Sådan spærrer du for, at en vare kan angives på salgslinjer</span><span class="sxs-lookup"><span data-stu-id="d4b99-115">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="d4b99-116">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d4b99-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d4b99-117">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret salg**.</span><span class="sxs-lookup"><span data-stu-id="d4b99-117">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="d4b99-118">Hvis du forsøger at angive varen på et salgsdokument eller kladdelinje, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="d4b99-118">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="d4b99-119">Sådan spærrer du for, at en vare kan angives på købslinjer</span><span class="sxs-lookup"><span data-stu-id="d4b99-119">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="d4b99-120">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d4b99-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d4b99-121">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret køb**.</span><span class="sxs-lookup"><span data-stu-id="d4b99-121">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="d4b99-122">Hvis du forsøger at angive varen på et købsdokument eller kladdelinje, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="d4b99-122">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="d4b99-123">Sådan spærrer du for, at en vare kan bogføres</span><span class="sxs-lookup"><span data-stu-id="d4b99-123">To block an item from being posted</span></span>
1. <span data-ttu-id="d4b99-124">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d4b99-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="d4b99-125">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret**.</span><span class="sxs-lookup"><span data-stu-id="d4b99-125">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="d4b99-126">Hvis du forsøger at bogføre en transaktionstype for varen, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="d4b99-126">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4b99-127">Se også</span><span class="sxs-lookup"><span data-stu-id="d4b99-127">See Also</span></span>  
[<span data-ttu-id="d4b99-128">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="d4b99-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="d4b99-129">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="d4b99-129">Inventory</span></span>](inventory-manage-inventory.md)  
