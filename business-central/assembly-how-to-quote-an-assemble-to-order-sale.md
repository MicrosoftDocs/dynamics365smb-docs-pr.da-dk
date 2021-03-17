---
title: Sådan oprettes tilbud på montage til ordre-salg | Microsoft Docs
description: Du kan bruge montagestyring til at tilpasse et montageelement på anmodning af en debitor under salgsprocessen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 807c924e64764e7ac1932321603a415101e3bbf3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386645"
---
# <a name="quote-an-assemble-to-order-sale"></a><span data-ttu-id="cd72d-103">Oprette tilbud på montage til ordre-salg</span><span class="sxs-lookup"><span data-stu-id="cd72d-103">Quote an Assemble-to-Order Sale</span></span>
<span data-ttu-id="cd72d-104">Du kan bruge montagestyring til at tilpasse et montageelement på anmodning af en debitor under salgsprocessen.</span><span class="sxs-lookup"><span data-stu-id="cd72d-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="cd72d-105">Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="cd72d-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

<span data-ttu-id="cd72d-106">Du kan også oprette et salgstilbud for en tilpasset montageelement, som når du sælger en anden type emne, før det konverteres til en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="cd72d-106">As when you sell any other type of item, you can also create a sales quote for a customized assembly item before converting it to a sales order.</span></span> <span data-ttu-id="cd72d-107">Denne proces omfatter flere ekstra trin, når du sammenligner med oprettelse af et normalt salgstilbud, og det bruger en variation af tilknyttet montageordre, som er et montagetilbud.</span><span class="sxs-lookup"><span data-stu-id="cd72d-107">This process involves several extra steps when you compare it to creating a regular sales quote, and it uses a variation of a linked assembly order, which is an assembly quote.</span></span>

> [!NOTE]  
>  <span data-ttu-id="cd72d-108">Ligesom alle typer tilbud bruges mængderne med montagetilbud ikke i forbindelse med tilgængelighed, planlægning eller reservationer.</span><span class="sxs-lookup"><span data-stu-id="cd72d-108">Like all types of quotes, the quantities on assembly quotes are not used in availability, planning, or reservations.</span></span>  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a><span data-ttu-id="cd72d-109">Sådan oprettes et salgstilbud til et montage efter ordre-element</span><span class="sxs-lookup"><span data-stu-id="cd72d-109">To create a sales quote for an assemble-to-order item</span></span>  
1.  <span data-ttu-id="cd72d-110">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgstilbud**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="cd72d-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Quote**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cd72d-111">Opret en ny salgstilbudslinje med en linje til et montageelement.</span><span class="sxs-lookup"><span data-stu-id="cd72d-111">Create a sales quote line with one line for an assembly item.</span></span> <span data-ttu-id="cd72d-112">Der er flere oplysninger i [Give salgstilbud](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="cd72d-112">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span>  
3.  <span data-ttu-id="cd72d-113">I feltet **Antal til montage efter ordre** skal du angive den samlede mængde.</span><span class="sxs-lookup"><span data-stu-id="cd72d-113">In the **Qty. to Assemble to Order** field, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="cd72d-114">Du bør ikke give tilbud på en delmængde.</span><span class="sxs-lookup"><span data-stu-id="cd72d-114">You should not quote a partial quantity.</span></span> <span data-ttu-id="cd72d-115">Derfor skal du angive det samme antal, som du har angivet i feltet **Antal** på salgstilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="cd72d-115">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the sales quote line.</span></span>  

4.  <span data-ttu-id="cd72d-116">På oversigtspanelet **Linjer** skal du vælge **Linje**, vælg **Montage efter ordre**, og vælg derefter **Montage efter ordre-linjer**.</span><span class="sxs-lookup"><span data-stu-id="cd72d-116">On the **Lines** FastTab, choose **Line**, choose **Assemble to Order**, and then choose **Assemble-to-Order Lines**.</span></span> <span data-ttu-id="cd72d-117">Du kan også vælge feltet **Antal til montage efter ordre** på linjen.</span><span class="sxs-lookup"><span data-stu-id="cd72d-117">Alternatively, choose the **Qty. to Assemble to Order** field on the line.</span></span>  
5.  <span data-ttu-id="cd72d-118">På siden **Montage efter ordre-linjer** kan du gennemse eller ændre linjerne til montageordre efter det tilbud, som kunden anmoder om.</span><span class="sxs-lookup"><span data-stu-id="cd72d-118">On the **Assemble-to-Order Lines** page, review or modify the assembly order lines according to the quote that the customer is requesting.</span></span> <span data-ttu-id="cd72d-119">Hvis du vil se flere oplysninger, kan du vælge handlingen **Vis dokument** for at åbne den samlede rammetilbudsordre.</span><span class="sxs-lookup"><span data-stu-id="cd72d-119">If you want to view more information, choose the **Show Document** action to open the complete blanket quote order.</span></span> <span data-ttu-id="cd72d-120">Du kan ikke ændre indholdet af de fleste felter, og du kan ikke bogføre.</span><span class="sxs-lookup"><span data-stu-id="cd72d-120">You cannot change the contents of most fields, and you cannot post.</span></span>  
6.  <span data-ttu-id="cd72d-121">Når du har reguleret montageordrelinjerne i overensstemmelse med tilbuddet, skal du lukke siden **Montage efter ordre-linjer** for at vende tilbage til siden **Salgstilbud**.</span><span class="sxs-lookup"><span data-stu-id="cd72d-121">When you have adjusted the assembly order lines according to the quote, close the **Assemble-to-Order Lines** page to return to the **Sales Quote** page.</span></span>  
7.  <span data-ttu-id="cd72d-122">Hvis debitor accepterer tilbuddet, kan du oprette en salgsordre for det tilbudte montageelement.</span><span class="sxs-lookup"><span data-stu-id="cd72d-122">If the customer accepts the quote, then create a sales order for the quoted assembly item.</span></span> <span data-ttu-id="cd72d-123">Der er flere oplysninger i [Give salgstilbud](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="cd72d-123">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span> <span data-ttu-id="cd72d-124">Det sammenkædede montagetilbud og eventuelle tilpasninger er knyttet til den pågældende nye salgsordre for at forberede til montage af varen eller de varer, der skal sælges.</span><span class="sxs-lookup"><span data-stu-id="cd72d-124">The linked assembly quote and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cd72d-125">Se også</span><span class="sxs-lookup"><span data-stu-id="cd72d-125">See Also</span></span>  
[<span data-ttu-id="cd72d-126">Montagestyring</span><span class="sxs-lookup"><span data-stu-id="cd72d-126">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="cd72d-127">Arbejde med styklister</span><span class="sxs-lookup"><span data-stu-id="cd72d-127">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="cd72d-128">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="cd72d-128">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="cd72d-129">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="cd72d-129">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="cd72d-130">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cd72d-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]