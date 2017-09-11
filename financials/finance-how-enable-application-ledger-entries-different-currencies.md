---
title: Udligne poster i forskellige valutaer | Microsoft Docs
description: "Du kan udligne finansposter i flere valutaer, f.eks. hvis du sælger i én valuta og modtager betaling i en anden."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 035f4c0e98e3b7ba308319c2017568de832e26c5
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="03e04-103">Fremgangsmåde: Muliggøre udligning af finansposter i forskellige valutaer</span><span class="sxs-lookup"><span data-stu-id="03e04-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="03e04-104">Hvis du køber varer fra en leverandør i én valuta, men foretager betaling i en anden valuta, kan du udligne betalingen med købet.</span><span class="sxs-lookup"><span data-stu-id="03e04-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="03e04-105">Ligeledes, hvis du sælger til en debitor i en valuta og modtager betaling i en anden, kan du knytte betalingen til salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="03e04-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="03e04-106">Følgende procedure beskriver, hvordan du kan angive dette for kreditorposter i vinduet **Købsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="03e04-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="03e04-107">Der er tilsvarende opsætning for debitorposter i vinduet **Salgsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="03e04-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="03e04-108">Denne funktion kræver, at oplevelsen er indstillet til **Pakke**.</span><span class="sxs-lookup"><span data-stu-id="03e04-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="03e04-109">Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="03e04-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="03e04-110">Sådan aktiveres udligning af kreditorposter i forskellige valutaer</span><span class="sxs-lookup"><span data-stu-id="03e04-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="03e04-111">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsopsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="03e04-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="03e04-112">Vælg en af følgende indstillinger i feltet **Valutaudligning**.</span><span class="sxs-lookup"><span data-stu-id="03e04-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="03e04-113">Indstilling</span><span class="sxs-lookup"><span data-stu-id="03e04-113">Option</span></span> | <span data-ttu-id="03e04-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="03e04-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="03e04-115">Ingen</span><span class="sxs-lookup"><span data-stu-id="03e04-115">None</span></span> |<span data-ttu-id="03e04-116">Udligning mellem valutaer er ikke tilladt.</span><span class="sxs-lookup"><span data-stu-id="03e04-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="03e04-117">ØMU</span><span class="sxs-lookup"><span data-stu-id="03e04-117">EMU</span></span> |<span data-ttu-id="03e04-118">Udligning mellem ØMU-valutaer er tilladt.</span><span class="sxs-lookup"><span data-stu-id="03e04-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="03e04-119">Alle</span><span class="sxs-lookup"><span data-stu-id="03e04-119">All</span></span> |<span data-ttu-id="03e04-120">Udligning mellem alle valutaer er tilladt.</span><span class="sxs-lookup"><span data-stu-id="03e04-120">Application between all currencies is allowed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="03e04-121">Se også</span><span class="sxs-lookup"><span data-stu-id="03e04-121">See Also</span></span>
[<span data-ttu-id="03e04-122">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="03e04-122">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="03e04-123">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="03e04-123">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="03e04-124">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="03e04-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

