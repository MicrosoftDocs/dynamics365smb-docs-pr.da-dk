---
title: Sådan spærres varer mod salg eller køb
description: I Business Central kan en vare være markeret som spærret for salg, spærret for køb eller spærret i alle sammenhænge.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c453a10f30d2a45f6d4641bda8b24ee3659b1a32
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182296"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="1a45e-103">Spærre varer mod salg eller køb</span><span class="sxs-lookup"><span data-stu-id="1a45e-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="1a45e-104">Du kan spærre for, at en vare angives på salgs- eller købslinjer og for, at den bogføres i nogen posteringer.</span><span class="sxs-lookup"><span data-stu-id="1a45e-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="1a45e-105">Tabellen nedenfor viser, hvad der sker, når varer spærres.</span><span class="sxs-lookup"><span data-stu-id="1a45e-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="1a45e-106">Indstilling</span><span class="sxs-lookup"><span data-stu-id="1a45e-106">Option</span></span>|<span data-ttu-id="1a45e-107">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1a45e-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="1a45e-108">**Spærret salg**</span><span class="sxs-lookup"><span data-stu-id="1a45e-108">**Sales Blocked**</span></span>|<span data-ttu-id="1a45e-109">Du kan ikke angive varen i et salgsdokument eller i en salgsvarekladde.</span><span class="sxs-lookup"><span data-stu-id="1a45e-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="1a45e-110">**Spærret køb**</span><span class="sxs-lookup"><span data-stu-id="1a45e-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="1a45e-111">Du kan ikke angive varen i et købsdokument, i en købsvarekladde eller i købsplanlægningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="1a45e-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="1a45e-112">**Spærret**</span><span class="sxs-lookup"><span data-stu-id="1a45e-112">**Blocked**</span></span>|<span data-ttu-id="1a45e-113">Du kan ikke bruge varen til nogen varetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="1a45e-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="1a45e-114">Blokerede varer kan returneres.</span><span class="sxs-lookup"><span data-stu-id="1a45e-114">Blocked items can be returned.</span></span> <span data-ttu-id="1a45e-115">Det betyder, at ingen af indstillingerne ovenfor gælder, når varen bruges på returvareordrer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="1a45e-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="1a45e-116">Når du bruger funktionen **Kopier fra dokument** til at oprette nye dokumenter, der er baserede på eksisterende dokumenter, vises der en meddelelse, hvis varerne på kildedokumentlinjerne er spærret.</span><span class="sxs-lookup"><span data-stu-id="1a45e-116">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="1a45e-117">De spærrede dokumentlinjer medtages ikke i det nye dokument, og der vises en meddelelse indeholdende en oversigt over alle de dokumentlinjer, der er spærrede i kildedokumentet.</span><span class="sxs-lookup"><span data-stu-id="1a45e-117">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="1a45e-118">Sådan spærrer du for, at en vare kan angives på salgslinjer</span><span class="sxs-lookup"><span data-stu-id="1a45e-118">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="1a45e-119">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1a45e-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1a45e-120">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret salg**.</span><span class="sxs-lookup"><span data-stu-id="1a45e-120">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="1a45e-121">Hvis du forsøger at angive varen på et salgsdokument eller kladdelinje, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="1a45e-121">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="1a45e-122">Sådan spærrer du for, at en vare kan angives på købslinjer</span><span class="sxs-lookup"><span data-stu-id="1a45e-122">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="1a45e-123">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1a45e-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1a45e-124">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret køb**.</span><span class="sxs-lookup"><span data-stu-id="1a45e-124">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="1a45e-125">Hvis du forsøger at angive varen på et købsdokument eller kladdelinje, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="1a45e-125">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="1a45e-126">Sådan spærrer du for, at en vare kan bogføres</span><span class="sxs-lookup"><span data-stu-id="1a45e-126">To block an item from being posted</span></span>
1. <span data-ttu-id="1a45e-127">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1a45e-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="1a45e-128">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret**.</span><span class="sxs-lookup"><span data-stu-id="1a45e-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="1a45e-129">Hvis du forsøger at bogføre en transaktionstype for varen, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="1a45e-129">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a45e-130">Se også</span><span class="sxs-lookup"><span data-stu-id="1a45e-130">See Also</span></span>  
[<span data-ttu-id="1a45e-131">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="1a45e-131">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="1a45e-132">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="1a45e-132">Inventory</span></span>](inventory-manage-inventory.md)  
