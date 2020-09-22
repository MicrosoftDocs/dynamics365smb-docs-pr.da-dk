---
title: Sådan spærres varer mod salg eller køb
description: Du kan forhindre, at en vare bliver brugt, f.eks. på salgs- eller købsdokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: fb80cecd119cf061b3102d94f586da4c103bd21c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784809"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="46440-103">Spærre varer mod salg eller køb</span><span class="sxs-lookup"><span data-stu-id="46440-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="46440-104">Du kan spærre for, at en vare angives på linjer i salgs- eller købsdokumenter og for, at den bogføres i nogen posteringer.</span><span class="sxs-lookup"><span data-stu-id="46440-104">You can block an item from being entered on lines in sales or purchase documents, and you can block it from being posted in any transaction.</span></span> <span data-ttu-id="46440-105">Dette er f.eks. nyttigt, hvis en vare har en kendt defekt.</span><span class="sxs-lookup"><span data-stu-id="46440-105">For example, this is useful when an item has a known defect.</span></span> <span data-ttu-id="46440-106">Hvis en person vælger en spærret vare på et salgs- eller købsdokument, vil en meddelelse give dem om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="46440-106">If someone chooses a blocked item on a sales or purchase document a message will inform them that the item is blocked.</span></span>

<span data-ttu-id="46440-107">Tabellen nedenfor beskriver, hvad der sker, når varer spærres.</span><span class="sxs-lookup"><span data-stu-id="46440-107">The following table describes what occurs when items are blocked.</span></span>  

|<span data-ttu-id="46440-108">Indstilling</span><span class="sxs-lookup"><span data-stu-id="46440-108">Option</span></span>|<span data-ttu-id="46440-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="46440-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="46440-110">**Spærret salg**</span><span class="sxs-lookup"><span data-stu-id="46440-110">**Sales Blocked**</span></span>|<span data-ttu-id="46440-111">Du kan ikke angive varen i et salgsdokument eller i en salgsvarekladde.</span><span class="sxs-lookup"><span data-stu-id="46440-111">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="46440-112">**Spærret køb**</span><span class="sxs-lookup"><span data-stu-id="46440-112">**Purchasing Blocked**</span></span>|<span data-ttu-id="46440-113">Du kan ikke angive varen i et købsdokument, i en købsvarekladde eller i købsplanlægningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="46440-113">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="46440-114">**Spærret**</span><span class="sxs-lookup"><span data-stu-id="46440-114">**Blocked**</span></span>|<span data-ttu-id="46440-115">Du kan ikke bruge varen til nogen varetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="46440-115">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="46440-116">Blokerede varer kan returneres.</span><span class="sxs-lookup"><span data-stu-id="46440-116">Blocked items can be returned.</span></span> <span data-ttu-id="46440-117">Det betyder, at ingen af indstillingerne ovenfor gælder, når varen bruges på returvareordrer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="46440-117">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="46440-118">Når du bruger funktionen **Kopier fra dokument** til at oprette nye dokumenter, der er baserede på eksisterende dokumenter, vises der en meddelelse, hvis varerne på kildedokumentlinjerne er spærret.</span><span class="sxs-lookup"><span data-stu-id="46440-118">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="46440-119">De spærrede dokumentlinjer medtages ikke i det nye dokument, og der vises en meddelelse indeholdende en oversigt over alle de dokumentlinjer, der er spærrede i kildedokumentet.</span><span class="sxs-lookup"><span data-stu-id="46440-119">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="46440-120">Sådan spærrer du for, at en vare kan angives på salgslinjer</span><span class="sxs-lookup"><span data-stu-id="46440-120">To block an item from being entered on sales lines</span></span>  
1.  <span data-ttu-id="46440-121">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="46440-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="46440-122">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret salg**.</span><span class="sxs-lookup"><span data-stu-id="46440-122">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="46440-123">Sådan spærrer du for, at en vare kan angives på købslinjer</span><span class="sxs-lookup"><span data-stu-id="46440-123">To block an item from being entered on purchase lines</span></span>  
1.  <span data-ttu-id="46440-124">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="46440-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="46440-125">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret køb**.</span><span class="sxs-lookup"><span data-stu-id="46440-125">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="46440-126">Sådan spærrer du for, at en vare kan bogføres</span><span class="sxs-lookup"><span data-stu-id="46440-126">To block an item from being posted</span></span>
1. <span data-ttu-id="46440-127">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="46440-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="46440-128">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret**.</span><span class="sxs-lookup"><span data-stu-id="46440-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="46440-129">Se også</span><span class="sxs-lookup"><span data-stu-id="46440-129">See Also</span></span>  
[<span data-ttu-id="46440-130">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="46440-130">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="46440-131">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="46440-131">Inventory</span></span>](inventory-manage-inventory.md)  
