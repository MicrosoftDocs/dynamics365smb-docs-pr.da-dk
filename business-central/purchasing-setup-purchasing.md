---
title: Oversigt over opgaver til opsætning af køb | Microsoft Docs
description: Beskriver de opgaver, der definerer virksomhedens indkøbspolitikker, og som du bruger til at oprette dine indkøbsprocesser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 81bbb013cba1039bfe6bb76e8489d5b8ed7c9831
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772500"
---
# <a name="setting-up-purchasing"></a><span data-ttu-id="69a1c-103">Opsætning af indkøb</span><span class="sxs-lookup"><span data-stu-id="69a1c-103">Setting Up Purchasing</span></span>
<span data-ttu-id="69a1c-104">Før du kan administrere købsprocesser, skal du konfigurere de regler og værdier, der definerer virksomhedens købspolitikker.</span><span class="sxs-lookup"><span data-stu-id="69a1c-104">Before you can manage purchase processes, you must configure the rules and values that define the company's purchase policies.</span></span>

<span data-ttu-id="69a1c-105">Du skal angive den generelle opsætning, f.eks. hvilke indkøbsdokumenter der kræves, og hvordan deres værdi bogføres.</span><span class="sxs-lookup"><span data-stu-id="69a1c-105">You must define the general setup, such as which purchase documents are required and how their values are posted.</span></span> <span data-ttu-id="69a1c-106">Denne generelle opsætning udføres typisk én gang i forbindelse med den indledende implementering.</span><span class="sxs-lookup"><span data-stu-id="69a1c-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="69a1c-107">En særskilt sæt opgaver i forbindelse med registrering af nye kreditorer er at registrere en særlig pris eller rabataftaler, du indgår med hver kreditorer.</span><span class="sxs-lookup"><span data-stu-id="69a1c-107">A separate series of tasks related to registering new vendors is to record any special price or discount agreements that you have with each vendor.</span></span>

<span data-ttu-id="69a1c-108">Den finansrelaterede købsopsætning, som betalingsmetoder og valutaer, dækkes i afsnittet Konfigurere Finans.</span><span class="sxs-lookup"><span data-stu-id="69a1c-108">Finance-related purchase setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="69a1c-109">Der er flere oplysninger i [Konfigurere Finans](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="69a1c-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="69a1c-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="69a1c-110">To</span></span> | <span data-ttu-id="69a1c-111">Se</span><span class="sxs-lookup"><span data-stu-id="69a1c-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="69a1c-112">Opret et kreditorkort for hver kreditor, du køber fra</span><span class="sxs-lookup"><span data-stu-id="69a1c-112">Create a vendor card for each vendor that you purchase from</span></span>|[<span data-ttu-id="69a1c-113">Registrere nye kreditorer</span><span class="sxs-lookup"><span data-stu-id="69a1c-113">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md) |
| <span data-ttu-id="69a1c-114">Angiv de forskellige rabatter og specialpriser, som kreditorer yder dig, afhængigt af vare, antal og/eller dato.</span><span class="sxs-lookup"><span data-stu-id="69a1c-114">Enter the different discounts and special prices that vendors grant you depending on item, quantities, and/or date</span></span> |[<span data-ttu-id="69a1c-115">Registrer købspris, rabat og betalingsaftaler</span><span class="sxs-lookup"><span data-stu-id="69a1c-115">Record Purchase Price, Discount, and Payment Agreements</span></span>](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| <span data-ttu-id="69a1c-116">Tildele kreditorer prioritet</span><span class="sxs-lookup"><span data-stu-id="69a1c-116">Prioritize vendors</span></span> |[<span data-ttu-id="69a1c-117">Tildele kreditorer prioritet</span><span class="sxs-lookup"><span data-stu-id="69a1c-117">Prioritize Vendors</span></span>](purchasing-how-prioritize-vendors.md) |
| <span data-ttu-id="69a1c-118">Oprette indkøbere</span><span class="sxs-lookup"><span data-stu-id="69a1c-118">Set up purchasers</span></span> |[<span data-ttu-id="69a1c-119">Oprette indkøbere</span><span class="sxs-lookup"><span data-stu-id="69a1c-119">Set Up Purchasers</span></span>](purchasing-how-setup-purchasers.md) |
|<span data-ttu-id="69a1c-120">Angiv standardrapporter, der skal bruges til forskellige dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="69a1c-120">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="69a1c-121">Rapportvalg i Business Central</span><span class="sxs-lookup"><span data-stu-id="69a1c-121">Report Selection in Business Central</span></span>](across-report-selections.md)|

> [!TIP]
> <span data-ttu-id="69a1c-122">Nogle sider kan indeholde felter, der ikke er beskrevet i de artikler, der er angivet her, fordi de gælder for lokal funktionalitet eller tilpasninger, afhængigt af din geografiske placering.</span><span class="sxs-lookup"><span data-stu-id="69a1c-122">Depending on your geographical location, some pages can contain fields that are not described in the articles that are listed here because they apply to local functionality or customizations.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="69a1c-123">Se relateret oplæring på [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="69a1c-123">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="69a1c-124">Se også</span><span class="sxs-lookup"><span data-stu-id="69a1c-124">See Also</span></span>

[<span data-ttu-id="69a1c-125">Køb</span><span class="sxs-lookup"><span data-stu-id="69a1c-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="69a1c-126">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="69a1c-126">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]