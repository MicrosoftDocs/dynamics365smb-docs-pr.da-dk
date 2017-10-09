---
title: "Sådan oprettes tilbud på montage til ordre-salg | Microsoft Docs"
description: "Du kan bruge montagestyring til at tilpasse en montageelement på anmodning af en debitor under salgsprocessen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7602b067e4b3fc99815a581c851138d7cc3ff41e
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-quote-an-assemble-to-order-sale"></a><span data-ttu-id="eb4a1-103">Sådan oprettes tilbud på montage efter ordre-salg</span><span class="sxs-lookup"><span data-stu-id="eb4a1-103">How to: Quote an Assemble-to-Order Sale</span></span>
<span data-ttu-id="eb4a1-104">Du kan bruge montagestyring til at tilpasse et montageelement på anmodning af en debitor under salgsprocessen.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="eb4a1-105">Du kan finde flere oplysninger i [Sådan sælger du en vare, der er monteret efter ordre](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="eb4a1-105">For more information, see [How to: Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

<span data-ttu-id="eb4a1-106">Du kan også oprette et salgstilbud for en tilpasset montageelement, som når du sælger en anden type emne, før det konverteres til en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-106">As when you sell any other type of item, you can also create a sales quote for a customized assembly item before converting it to a sales order.</span></span> <span data-ttu-id="eb4a1-107">Denne proces omfatter flere ekstra trin, når du sammenligner med oprettelse af et normalt salgstilbud, og det bruger en variation af tilknyttet montageordre, som er et montagetilbud.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-107">This process involves several extra steps when you compare it to creating a regular sales quote, and it uses a variation of a linked assembly order, which is an assembly quote.</span></span>

> [!NOTE]  
>  <span data-ttu-id="eb4a1-108">Ligesom alle typer tilbud bruges mængderne med montagetilbud ikke i forbindelse med tilgængelighed, planlægning eller reservationer.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-108">Like all types of quotes, the quantities on assembly quotes are not used in availability, planning, or reservations.</span></span>  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a><span data-ttu-id="eb4a1-109">Sådan oprettes et salgstilbud til et montage efter ordre-element</span><span class="sxs-lookup"><span data-stu-id="eb4a1-109">To create a sales quote for an assemble-to-order item</span></span>  
1.  <span data-ttu-id="eb4a1-110">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgstilbud**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Quote**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="eb4a1-111">Opret en ny salgstilbudslinje med en linje til et montageelement.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-111">Create a sales quote line with one line for an assembly item.</span></span> <span data-ttu-id="eb4a1-112">Du kan finde flere oplysninger under [Fremgangsmåde: Fremsætte tilbud](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="eb4a1-112">For more information, see [How to: Make Offers](sales-how-make-offers.md).</span></span>  
3.  <span data-ttu-id="eb4a1-113">I feltet **Antal til montage efter ordre** skal du angive den samlede mængde.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-113">In the **Qty. to Assemble to Order** field, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="eb4a1-114">Du bør ikke give tilbud på en delmængde.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-114">You should not quote a partial quantity.</span></span> <span data-ttu-id="eb4a1-115">Derfor skal du angive det samme antal, som du har angivet i feltet **Antal** på salgstilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-115">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the sales quote line.</span></span>  

4.  <span data-ttu-id="eb4a1-116">På oversigtspanelet **Linjer** skal du vælge **Linje**, vælg **Montage efter ordre**, og vælg derefter **Montage efter ordre-linjer**.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-116">On the **Lines** FastTab, choose **Line**, choose **Assemble to Order**, and then choose **Assemble-to-Order Lines**.</span></span> <span data-ttu-id="eb4a1-117">Du kan også vælge feltet **Antal til montage efter ordre** på linjen.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-117">Alternatively, choose the **Qty. to Assemble to Order** field on the line.</span></span>  
5.  <span data-ttu-id="eb4a1-118">I vinduet **Montage efter ordre-linjer** kan du gennemse eller ændre linjerne til montageordre efter det tilbud, som kunden anmoder om.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-118">In the **Assemble-to-Order Lines** window, review or modify the assembly order lines according to the quote that the customer is requesting.</span></span> <span data-ttu-id="eb4a1-119">Hvis du vil se flere oplysninger, kan du vælge handlingen **Vis dokument** for at åbne den samlede rammetilbudsordre.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-119">If you want to view more information, choose the **Show Document** action to open the complete blanket quote order.</span></span> <span data-ttu-id="eb4a1-120">Du kan ikke ændre indholdet af de fleste felter, og du kan ikke bogføre.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-120">You cannot change the contents of most fields, and you cannot post.</span></span>  
6.  <span data-ttu-id="eb4a1-121">Når du har reguleret montageordrelinjerne i overensstemmelse med tilbuddet, skal du lukke vinduet **Montage efter ordre-linjer** for at vende tilbage til vinduet **Salgstilbud**.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-121">When you have adjusted the assembly order lines according to the quote, close the **Assemble-to-Order Lines** window to return to the **Sales Quote** window.</span></span>  
7.  <span data-ttu-id="eb4a1-122">Hvis debitor accepterer tilbuddet, kan du oprette en salgsordre for det tilbudte montageelement.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-122">If the customer accepts the quote, then create a sales order for the quoted assembly item.</span></span> <span data-ttu-id="eb4a1-123">Du kan finde flere oplysninger under [Fremgangsmåde: Fremsætte tilbud](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="eb4a1-123">For more information, see [How to: Make Offers](sales-how-make-offers.md).</span></span> <span data-ttu-id="eb4a1-124">Det sammenkædede montagetilbud og eventuelle tilpasninger er knyttet til den pågældende nye salgsordre for at forberede til montage af varen eller de varer, der skal sælges.</span><span class="sxs-lookup"><span data-stu-id="eb4a1-124">The linked assembly quote and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eb4a1-125">Se også</span><span class="sxs-lookup"><span data-stu-id="eb4a1-125">See Also</span></span>  
[<span data-ttu-id="eb4a1-126">Montagestyring</span><span class="sxs-lookup"><span data-stu-id="eb4a1-126">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="eb4a1-127">Fremgangsmåde: Arbejde med styklister</span><span class="sxs-lookup"><span data-stu-id="eb4a1-127">How to: Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="eb4a1-128">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="eb4a1-128">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="eb4a1-129">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="eb4a1-129">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="eb4a1-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eb4a1-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

