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
ms.date: 12/04/2019
ms.author: sgroespe
ms.openlocfilehash: 0218cf1b4982b9e8c5b5c2817590bc5ebd8f1941
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896057"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="25718-103">Spærre varer mod salg eller køb</span><span class="sxs-lookup"><span data-stu-id="25718-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="25718-104">Du kan spærre for, at en vare angives på salgs- eller købslinjer og for, at den bogføres i nogen posteringer.</span><span class="sxs-lookup"><span data-stu-id="25718-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="25718-105">Tabellen nedenfor viser, hvad der sker, når varer spærres.</span><span class="sxs-lookup"><span data-stu-id="25718-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="25718-106">Indstilling</span><span class="sxs-lookup"><span data-stu-id="25718-106">Option</span></span>|<span data-ttu-id="25718-107">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="25718-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="25718-108">**Spærret salg**</span><span class="sxs-lookup"><span data-stu-id="25718-108">**Sales Blocked**</span></span>|<span data-ttu-id="25718-109">Du kan ikke angive varen i et salgsdokument eller i en salgsvarekladde.</span><span class="sxs-lookup"><span data-stu-id="25718-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="25718-110">**Spærret køb**</span><span class="sxs-lookup"><span data-stu-id="25718-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="25718-111">Du kan ikke angive varen i et købsdokument, i en købsvarekladde eller i købsplanlægningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="25718-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="25718-112">**Spærret**</span><span class="sxs-lookup"><span data-stu-id="25718-112">**Blocked**</span></span>|<span data-ttu-id="25718-113">Du kan ikke bruge varen til nogen varetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="25718-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="25718-114">Blokerede varer kan returneres.</span><span class="sxs-lookup"><span data-stu-id="25718-114">Blocked items can be returned.</span></span> <span data-ttu-id="25718-115">Det betyder, at ingen af indstillingerne ovenfor gælder, når varen bruges på returvareordrer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="25718-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="25718-116">Når du bruger funktionen **Kopier dokument** til at oprette nye dokumenter, der er baserede på eksisterende dokumenter, vises der en meddelelse, hvis varerne på kildedokumentlinjerne er spærret.</span><span class="sxs-lookup"><span data-stu-id="25718-116">When you use the **Copy Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="25718-117">De spærrede dokumentlinjer medtages ikke i det nye dokument, og der vises en meddelelse indeholdende en oversigt over alle de dokumentlinjer, der er spærrede i kildedokumentet.</span><span class="sxs-lookup"><span data-stu-id="25718-117">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="25718-118">Sådan spærrer du for, at en vare kan angives på salgslinjer</span><span class="sxs-lookup"><span data-stu-id="25718-118">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="25718-119">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="25718-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="25718-120">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret salg**.</span><span class="sxs-lookup"><span data-stu-id="25718-120">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="25718-121">Hvis du forsøger at angive varen på et salgsdokument eller kladdelinje, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="25718-121">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="25718-122">Sådan spærrer du for, at en vare kan angives på købslinjer</span><span class="sxs-lookup"><span data-stu-id="25718-122">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="25718-123">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="25718-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="25718-124">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret køb**.</span><span class="sxs-lookup"><span data-stu-id="25718-124">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="25718-125">Hvis du forsøger at angive varen på et købsdokument eller kladdelinje, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="25718-125">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="25718-126">Sådan spærrer du for, at en vare kan bogføres</span><span class="sxs-lookup"><span data-stu-id="25718-126">To block an item from being posted</span></span>
1. <span data-ttu-id="25718-127">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="25718-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="25718-128">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret**.</span><span class="sxs-lookup"><span data-stu-id="25718-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="25718-129">Hvis du forsøger at bogføre en transaktionstype for varen, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="25718-129">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="25718-130">Se også</span><span class="sxs-lookup"><span data-stu-id="25718-130">See Also</span></span>  
[<span data-ttu-id="25718-131">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="25718-131">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="25718-132">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="25718-132">Inventory</span></span>](inventory-manage-inventory.md)  
