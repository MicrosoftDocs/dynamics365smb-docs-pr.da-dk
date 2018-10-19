---
title: "Sådan bruges varefamilier i produktionen | Microsoft Docs"
description: "Den vigtigste opgave i forbindelse med tilpasning af en basiskalender for din virksomhed eller en samarbejdspartner, er at angive eventuelle ændringer i statussen for arbejdsdage eller fridage."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 4e89cee3fb8b3c079cebf0665a1e068ac1f46fae
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="work-with-production-families"></a><span data-ttu-id="b0c26-103">Arbejde med produktionsfamilier</span><span class="sxs-lookup"><span data-stu-id="b0c26-103">Work with Production Families</span></span>
<span data-ttu-id="b0c26-104">En produktfamilie er en gruppe individuelle varer, hvis slægtskab er baseret på lighedspunkter i fremstillingsprocesserne.</span><span class="sxs-lookup"><span data-stu-id="b0c26-104">A production family is a group of individual items whose relationship is based on the similarity of their manufacturing processes.</span></span> <span data-ttu-id="b0c26-105">Ved hjælp af produktionsfamilier kan visse varer forarbejdes to eller flere gange i samme proces, hvilket optimerer materialeforbruget.</span><span class="sxs-lookup"><span data-stu-id="b0c26-105">By forming production families, some items can be manufactured twice or more in one production, which will optimize material consumption.</span></span>

<span data-ttu-id="b0c26-106">I feltet **Antal** i vinduet **Familie** skal du angive det antal, der er produceret, når hele familien er produceret én gang.</span><span class="sxs-lookup"><span data-stu-id="b0c26-106">In the **Quantity** field in the **Family** window, you enter the quantity that will be produced when the whole family has been manufactured once.</span></span>

## <a name="example"></a><span data-ttu-id="b0c26-107">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b0c26-107">Example</span></span>
<span data-ttu-id="b0c26-108">Ved en udstansning kan fire stk. af samme vare produceres fra et emne og ti stk. af en anden vare samtidig.</span><span class="sxs-lookup"><span data-stu-id="b0c26-108">In punching processes, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span> <span data-ttu-id="b0c26-109">Stansemaskinen vil udstanse alle 14 stykker i en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="b0c26-109">The punching machine will punch all 14 pieces in one step.</span></span>

<span data-ttu-id="b0c26-110">Ved at oprette produktionsfamilier reduceres spildantallet, fordi det, der normalt ville være tilovers som spild ved produktion af store stykker, i stedet kan benyttes til at producere små stykker.</span><span class="sxs-lookup"><span data-stu-id="b0c26-110">Forming production families reduces the scrap quantity because what would normally be leftover scrap, when producing big pieces, will be used instead to produce small items.</span></span>

## <a name="to-set-up-a-production-family"></a><span data-ttu-id="b0c26-111">Sådan oprettes en produktionsfamilie</span><span class="sxs-lookup"><span data-stu-id="b0c26-111">To set up a production family</span></span>
1. <span data-ttu-id="b0c26-112">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Familier**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b0c26-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Families**, and then choose the related link.</span></span>
2. <span data-ttu-id="b0c26-113">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="b0c26-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-familily"></a><span data-ttu-id="b0c26-114">Sådan produceres på basis af en produktionsfamilie</span><span class="sxs-lookup"><span data-stu-id="b0c26-114">To produce based on a production familily</span></span>
1. <span data-ttu-id="b0c26-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fastlagte prod.ordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b0c26-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="b0c26-116">Opret et ny produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="b0c26-116">Create a new production order.</span></span> <span data-ttu-id="b0c26-117">Du kan finde flere oplysninger i [Oprette produktionsordrer](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="b0c26-117">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>
3. <span data-ttu-id="b0c26-118">Vælg **Familie** i feltet **Kildetype**.</span><span class="sxs-lookup"><span data-stu-id="b0c26-118">In the **Source Type** field, select **Family**.</span></span>  
4. <span data-ttu-id="b0c26-119">Vælg den relevante produktionsfamilie i feltet **Kildenr.**.</span><span class="sxs-lookup"><span data-stu-id="b0c26-119">In the **Source No.** field, select the relevant production family.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0c26-120">Se også</span><span class="sxs-lookup"><span data-stu-id="b0c26-120">See Also</span></span>
[<span data-ttu-id="b0c26-121">Oprette produktionsstyklister</span><span class="sxs-lookup"><span data-stu-id="b0c26-121">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="b0c26-122">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="b0c26-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="b0c26-123">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="b0c26-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="b0c26-124">[Planlægning](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="b0c26-124">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="b0c26-125">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="b0c26-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b0c26-126">Køb</span><span class="sxs-lookup"><span data-stu-id="b0c26-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="b0c26-127">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b0c26-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

