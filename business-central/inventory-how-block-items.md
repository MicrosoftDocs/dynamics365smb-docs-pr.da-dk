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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8c98e4b893783c795a49e05ab04dc70b03161c6a
ms.sourcegitcommit: bf5f89dfaf5ad9f8f9902941cf3dac3e9f3553e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/22/2019
ms.locfileid: "1594241"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="c015f-103">Spærre varer mod salg eller køb</span><span class="sxs-lookup"><span data-stu-id="c015f-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="c015f-104">Du kan spærre for, at en vare angives på salgs- eller købslinjer og for, at den bogføres i nogen posteringer.</span><span class="sxs-lookup"><span data-stu-id="c015f-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="c015f-105">Tabellen nedenfor viser, hvad der sker, når varer spærres.</span><span class="sxs-lookup"><span data-stu-id="c015f-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="c015f-106">Indstilling</span><span class="sxs-lookup"><span data-stu-id="c015f-106">Option</span></span>|<span data-ttu-id="c015f-107">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c015f-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="c015f-108">**Spærret salg**</span><span class="sxs-lookup"><span data-stu-id="c015f-108">**Sales Blocked**</span></span>|<span data-ttu-id="c015f-109">Du kan ikke angive varen i et salgsdokument eller i en salgsvarekladde.</span><span class="sxs-lookup"><span data-stu-id="c015f-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="c015f-110">**Spærret køb**</span><span class="sxs-lookup"><span data-stu-id="c015f-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="c015f-111">Du kan ikke angive varen i et købsdokument, i en købsvarekladde eller i købsplanlægningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="c015f-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="c015f-112">**Spærret**</span><span class="sxs-lookup"><span data-stu-id="c015f-112">**Blocked**</span></span>|<span data-ttu-id="c015f-113">Du kan ikke bruge varen til nogen varetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="c015f-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="c015f-114">Blokerede varer kan returneres.</span><span class="sxs-lookup"><span data-stu-id="c015f-114">Blocked items can be returned.</span></span> <span data-ttu-id="c015f-115">Det betyder, at ingen af indstillingerne ovenfor gælder, når varen bruges på returvareordrer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="c015f-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="c015f-116">Sådan spærrer du for, at en vare kan angives på salgslinjer</span><span class="sxs-lookup"><span data-stu-id="c015f-116">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="c015f-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c015f-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c015f-118">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret salg**.</span><span class="sxs-lookup"><span data-stu-id="c015f-118">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="c015f-119">Hvis du forsøger at angive varen på et salgsdokument eller kladdelinje, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="c015f-119">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="c015f-120">Sådan spærrer du for, at en vare kan angives på købslinjer</span><span class="sxs-lookup"><span data-stu-id="c015f-120">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="c015f-121">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c015f-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c015f-122">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret køb**.</span><span class="sxs-lookup"><span data-stu-id="c015f-122">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="c015f-123">Hvis du forsøger at angive varen på et købsdokument eller kladdelinje, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="c015f-123">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="c015f-124">Sådan spærrer du for, at en vare kan bogføres</span><span class="sxs-lookup"><span data-stu-id="c015f-124">To block an item from being posted</span></span>
1. <span data-ttu-id="c015f-125">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c015f-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="c015f-126">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret**.</span><span class="sxs-lookup"><span data-stu-id="c015f-126">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="c015f-127">Hvis du forsøger at bogføre en transaktionstype for varen, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="c015f-127">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="c015f-128">Se også</span><span class="sxs-lookup"><span data-stu-id="c015f-128">See Also</span></span>  
[<span data-ttu-id="c015f-129">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="c015f-129">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="c015f-130">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c015f-130">Inventory</span></span>](inventory-manage-inventory.md)  
