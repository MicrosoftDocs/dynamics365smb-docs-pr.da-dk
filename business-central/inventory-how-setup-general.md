---
title: Definere den generelle lageropsætning
description: Beskriver, hvordan du definerer den generelle Lageropsætning, så du kan administrere lagerstedet og lagerbeholdningen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e3ecf8d206e50244c19a820bdb67d2992cbefe36
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746362"
---
# <a name="set-up-general-inventory-information"></a><span data-ttu-id="f6745-103">Konfigurere generelle lageroplysninger</span><span class="sxs-lookup"><span data-stu-id="f6745-103">Set Up General Inventory Information</span></span>

<span data-ttu-id="f6745-104">Du kan angive dine generelle lageropsætning på siden **Lageropsætning**.</span><span class="sxs-lookup"><span data-stu-id="f6745-104">You specify your general inventory setup on the **Inventory Setup** page.</span></span>

## <a name="to-set-up-general-inventory-information"></a><span data-ttu-id="f6745-105">Sådan konfigurerer du generelle lageroplysninger</span><span class="sxs-lookup"><span data-stu-id="f6745-105">To set up general inventory information</span></span>

1. <span data-ttu-id="f6745-106">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lageropsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f6745-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f6745-107">På siden **Lageropsætning** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f6745-107">On the **Inventory Setup** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="f6745-108">Hvis du vil have detaljerede oplysninger om omkostningsfelterne **Aut. lagerværdibogføring**, **Bogf. af forventet kostpris** og **Standardmetode for kostprisberegning**, skal du se [Afstemme lageromkostninger med finansregnskabet](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md) og [Designoplysninger: Bogføring af forventet kostpris](design-details-expected-cost-posting.md).</span><span class="sxs-lookup"><span data-stu-id="f6745-108">For detailed information about the costing fields, **Automatic Cost Posting**, **Expected Cost Posting to G/L**, and **Default Costing Method**, see [Reconcile Inventory Costs with the General Ledger](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Design Details: Inventory Costing](design-details-inventory-costing.md), and [Design Details: Expected Cost Posting](design-details-expected-cost-posting.md).</span></span> <span data-ttu-id="f6745-109">Du kan finde flere oplysninger om kostpris i almindelighed under [Administrere lageromkostninger](finance-manage-inventory-costs.md).</span><span class="sxs-lookup"><span data-stu-id="f6745-109">For more information about costing in general, see [Managing Inventory Costs](finance-manage-inventory-costs.md).</span></span>  

<span data-ttu-id="f6745-110">Hvis du automatisk vil inkludere lagerekspeditionstiden i beregningen af leveringstiden på købslinjen, kan du angive det som standardindstilling på siden **Opsætning af Lager** og for din lokation.</span><span class="sxs-lookup"><span data-stu-id="f6745-110">If you want to include warehouse handling time in the order promising calculation on the purchase line, you can set it up as a default for the inventory, on the **Inventory Setup** page, and for your location.</span></span> <span data-ttu-id="f6745-111">Du kan finde flere oplysninger i [Beregne ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="f6745-111">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="f6745-112">Funktionen til **Automatisk regulering af kostpris** er som standard aktiveret for at sikre, at lagerværdierne altid er korrekte i finansbogholderiet, som samtidig holder salgs- og overskudsstatistikken ajour.</span><span class="sxs-lookup"><span data-stu-id="f6745-112">The **Automatic Cost Adjustment** toggle is turned on by default to ensure that inventory values are always correct in the general ledger, which in turn keeps your sales and profit statistics up to date.</span></span> <span data-ttu-id="f6745-113">Kostprisændringer fra indgående poster, f.eks. for køb eller produktionsoutput, er tilknyttet de relaterede udgående poster, f.eks. salg eller overførsler.</span><span class="sxs-lookup"><span data-stu-id="f6745-113">Cost changes from inbound entries, such as those for purchases or production output, are assigned to the related outbound entries, such as sales or transfers.</span></span> <span data-ttu-id="f6745-114">Dette er nyttigt for nye [!INCLUDE[prod_short](includes/prod_short.md)] kunder og mindre virksomheder med relativt lave lagertransaktionsniveauer.</span><span class="sxs-lookup"><span data-stu-id="f6745-114">This is helpful for new [!INCLUDE[prod_short](includes/prod_short.md)] customers and small businesses with relatively low inventory transaction levels.</span></span> <span data-ttu-id="f6745-115">Men i takt med at virksomhedens vækst vokser, og lagerniveauet stiger, kan det gøre systemets ydeevne langsommere.</span><span class="sxs-lookup"><span data-stu-id="f6745-115">However, as a business grows and inventory levels increase, this can slow down system performance.</span></span> <span data-ttu-id="f6745-116">Hvis du vil minimere reduceret ydeevne under bogføringen, skal du vælge en tidsindstilling for at definere, hvor langt tilbage i forhold til arbejdsdatoen en indgående transaktion må forekomme for at udløse reguleringen af relaterede udgående værdiposter.</span><span class="sxs-lookup"><span data-stu-id="f6745-116">To minimize reduced performance during posting, select a time option to define how far back in time from the work date an inbound transaction can occur to potentially trigger adjustment of related outbound value entries.</span></span> <span data-ttu-id="f6745-117">Alternativt kan du ændre omkostningerne manuelt med kørslen Reguler kostværdi - vareposter.</span><span class="sxs-lookup"><span data-stu-id="f6745-117">Alternatively, you can manually adjust costs at regular intervals with the Adjust Cost - Item Entries batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6745-118">Se også</span><span class="sxs-lookup"><span data-stu-id="f6745-118">See Also</span></span>
[<span data-ttu-id="f6745-119">Konfigurere lager</span><span class="sxs-lookup"><span data-stu-id="f6745-119">Set Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="f6745-120">[Designoplysninger: Kostmetoder](design-details-costing-methods.md)  </span><span class="sxs-lookup"><span data-stu-id="f6745-120">[Design Details: Costing Methods](design-details-costing-methods.md)  </span></span>  
[<span data-ttu-id="f6745-121">Administrere lager</span><span class="sxs-lookup"><span data-stu-id="f6745-121">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f6745-122">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f6745-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="f6745-123">Ændre, hvilke funktioner der vises</span><span class="sxs-lookup"><span data-stu-id="f6745-123">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="f6745-124">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="f6745-124">General Business Functionality</span></span>](ui-across-business-areas.md)
