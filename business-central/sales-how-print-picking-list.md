---
title: Sådan udskriver du en lagerplukliste fra en salgsordre
description: Du kan udskrive en lagerplukliste direkte i salgsordrer, salg, fakturaer og andre udgående salgsdokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 47ae132d862d2c05bef4ea0d0af26688bdd16588
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758213"
---
# <a name="print-the-picking-list"></a><span data-ttu-id="d4aed-103">Udskrive pluklisten</span><span class="sxs-lookup"><span data-stu-id="d4aed-103">Print the Picking List</span></span>
<span data-ttu-id="d4aed-104">Du kan udskrive en lagerplukliste direkte i salgsordrer, en salgsfakturaer og andre udgående salgsdokumenter, der bruges til at starte leverance af varer.</span><span class="sxs-lookup"><span data-stu-id="d4aed-104">You can print an inventory picking list directly from a sales order, a sales invoice, or any other document that initiates shipment of items.</span></span>

<span data-ttu-id="d4aed-105">Denne rapport bruges typisk i virksomheder uden dedikeret funktionalitet til lagerstyring, så en lagermedarbejder kan nøjes med at se eller udskrive pluklisten fra det relaterede salgsdokument.</span><span class="sxs-lookup"><span data-stu-id="d4aed-105">This report is typically used in companies without dedicated functionality for warehouse management, so that an inventory worker can simply view or print the picking list from the related sales document.</span></span> <span data-ttu-id="d4aed-106">I virksomheder med større eller mere komplicerede processer planlægges og udføres plukningen i dedikerede lagerdokumenter.</span><span class="sxs-lookup"><span data-stu-id="d4aed-106">In companies with higher volume or more complex processes, picking is planned and performed in dedicated warehouse documents.</span></span> <span data-ttu-id="d4aed-107">Du kan finde flere oplysninger i [Plukkevarer](warehouse-pick-items.md).</span><span class="sxs-lookup"><span data-stu-id="d4aed-107">For more information, see [Pick Items](warehouse-pick-items.md).</span></span>

## <a name="to-print-a-picking-list-from-a-sales-order"></a><span data-ttu-id="d4aed-108">Sådan udskriver du en plukliste fra en salgsordre</span><span class="sxs-lookup"><span data-stu-id="d4aed-108">To print a picking list from a sales order</span></span>  
<span data-ttu-id="d4aed-109">Følgende procedure er baseret på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="d4aed-109">The following procedure is based on a sales order.</span></span> <span data-ttu-id="d4aed-110">Fremgangsmåden er den samme for alle salgsdokumenter, der kan bruges til at starte leverance af varer.</span><span class="sxs-lookup"><span data-stu-id="d4aed-110">The steps are similar for all sales documents that can be used to initiate shipment of items.</span></span>

1. <span data-ttu-id="d4aed-111">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d4aed-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d4aed-112">Åbn den salgsordre, som du vil plukke varer til.</span><span class="sxs-lookup"><span data-stu-id="d4aed-112">Open the sales order that you want to pick items for.</span></span>  
3. <span data-ttu-id="d4aed-113">Vælg handlingen **Rapport**, og vælg derefter handlingen **Plukliste efter ordre**.</span><span class="sxs-lookup"><span data-stu-id="d4aed-113">Choose the **Report** action, and then choose the **Picking List by Order** action.</span></span>  
4. <span data-ttu-id="d4aed-114">Klik på **Udskriv** for at udskrive pluklisten, eller klik på **Vis udskrift** for at se den på skærmen.</span><span class="sxs-lookup"><span data-stu-id="d4aed-114">Choose the **Print** button to print the picking list or choose the **Preview** button to view it on the screen.</span></span>

<span data-ttu-id="d4aed-115">Du kan også gemme pluklisten som et dokument, hvis du f. eks. vil sende den til en anden person eller tilføje den som en vedhæftet fil i salgsordren.</span><span class="sxs-lookup"><span data-stu-id="d4aed-115">You can also save the picking list as a document, for example, to send to someone or to add as an attachment to the sales order.</span></span> <span data-ttu-id="d4aed-116">Du kan få flere oplysninger i [Administrere vedhæftede filer, links og noter på kort og dokumenter](ui-how-add-link-to-record.md).</span><span class="sxs-lookup"><span data-stu-id="d4aed-116">For more information, see [Manage Attachments, Links, and Notes on Cards and Documents](ui-how-add-link-to-record.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d4aed-117">Hvis du har brugt funktionen **Udfold stykliste** på salgsordren, vises kun de komponenter, der hører til det relaterede montageelement, i rapporten.</span><span class="sxs-lookup"><span data-stu-id="d4aed-117">If you used the **Explode BOM** function on the sales order, then only the components of the related assembly item are shown in the report.</span></span> <span data-ttu-id="d4aed-118">Du kan finde flere oplysninger under [Arbejde med styklister](inventory-how-work-BOMs.md).</span><span class="sxs-lookup"><span data-stu-id="d4aed-118">For more information, see [Work with Bills of Material](inventory-how-work-BOMs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d4aed-119">Se også</span><span class="sxs-lookup"><span data-stu-id="d4aed-119">See Also</span></span>  
[<span data-ttu-id="d4aed-120">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="d4aed-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="d4aed-121">Plukke varer</span><span class="sxs-lookup"><span data-stu-id="d4aed-121">Pick Items</span></span>](warehouse-pick-items.md)  
<span data-ttu-id="d4aed-122">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d4aed-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>   
