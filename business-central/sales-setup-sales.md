---
title: Oversigt over opgaver til konfiguration af salgsprocesser | Microsoft Docs
description: Beskriver opgaver til oprettelse af regler og værdier, som du kan bruge til at definere virksomhedens salgspolitikker og -processer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2a7964b255f78fa599ab58f66cb9425befaa038d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393320"
---
# <a name="setting-up-sales"></a><span data-ttu-id="51548-103">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="51548-103">Setting Up Sales</span></span>
<span data-ttu-id="51548-104">Før du kan administrere salgsprocesser, skal du konfigurere de regler og værdier, der definerer virksomhedens salgspolitikker.</span><span class="sxs-lookup"><span data-stu-id="51548-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="51548-105">Du skal definere den generelle opsætning, f.eks. hvilke salgsdokumenter der kræves, og hvordan dokumenternes værdier bogføres.</span><span class="sxs-lookup"><span data-stu-id="51548-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="51548-106">Denne generelle opsætning udføres typisk én gang i forbindelse med den indledende implementering.</span><span class="sxs-lookup"><span data-stu-id="51548-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="51548-107">En særskilt sæt opgaver i forbindelse med registrering af nye debitorer er at registrere en særlig pris eller rabataftaler, du indgår med hver debitorer.</span><span class="sxs-lookup"><span data-stu-id="51548-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="51548-108">Den finansrelaterede salgsopsætning, som betalingsmetoder og valutaer, dækkes i afsnittet Konfigurere Finans.</span><span class="sxs-lookup"><span data-stu-id="51548-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="51548-109">Der er flere oplysninger i [Konfigurere Finans](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="51548-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="51548-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="51548-110">To</span></span> | <span data-ttu-id="51548-111">Se</span><span class="sxs-lookup"><span data-stu-id="51548-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="51548-112">Opret et debitorkort for hver debitor, du sælger til.</span><span class="sxs-lookup"><span data-stu-id="51548-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="51548-113">Registrere nye debitorer</span><span class="sxs-lookup"><span data-stu-id="51548-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="51548-114">Aktivere debitorer til at betale via PayPal, ved at vælge PayPal-logoet på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="51548-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="51548-115">Aktivere debitorbetaling via PayPal</span><span class="sxs-lookup"><span data-stu-id="51548-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="51548-116">Angive forskellige rabatter og specialpriser, som du yder kunderne, afhængigt af varen, antal og/eller dato.</span><span class="sxs-lookup"><span data-stu-id="51548-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="51548-117">Registrere salgspris, rabat og betalingsaftaler</span><span class="sxs-lookup"><span data-stu-id="51548-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="51548-118">Konfigurer sælgere, så du kan tildele dem til debitorkontakter eller måle sælgernes præstationer som grundlag for beregning af salgsprovision eller bonus.</span><span class="sxs-lookup"><span data-stu-id="51548-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="51548-119">Konfigurere sælgere</span><span class="sxs-lookup"><span data-stu-id="51548-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="51548-120">Angiv for individuelle debitorer eller for alle kunder, hvordan salgsdokumenterne sendes som standard, når du vælger **Bogfør og send** handlingen.</span><span class="sxs-lookup"><span data-stu-id="51548-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="51548-121">Konfigurere dokumentafsendelsesprofiler</span><span class="sxs-lookup"><span data-stu-id="51548-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="51548-122">Konfigurer din mail til at indeholde en oversigt over oplysningerne i det salgsdokument, der skal sendes.</span><span class="sxs-lookup"><span data-stu-id="51548-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="51548-123">[Sende dokumenter som mail](ui-how-send-documents-email.md)</span><span class="sxs-lookup"><span data-stu-id="51548-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="51548-124">Bruge en EU-webtjeneste til at kontrollere en kundes SE/CVR-nummer.</span><span class="sxs-lookup"><span data-stu-id="51548-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="51548-125">Kontrollere SE/CVR-numre</span><span class="sxs-lookup"><span data-stu-id="51548-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="51548-126">Definere de forskellige incoterms, du tilbyder kunderne, eller som dine leverandører tilbyder dig.</span><span class="sxs-lookup"><span data-stu-id="51548-126">Define the different incoterms that you offer to customers or that your vendors offer you.</span></span>|[<span data-ttu-id="51548-127">Oprette leveringsformer</span><span class="sxs-lookup"><span data-stu-id="51548-127">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)|
|<span data-ttu-id="51548-128">Angive oplysninger om de forskellige transportleverandører, virksomheden bruger, herunder et link til deres pakkesporingsservice.</span><span class="sxs-lookup"><span data-stu-id="51548-128">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="51548-129">Oprette speditører</span><span class="sxs-lookup"><span data-stu-id="51548-129">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|
|<span data-ttu-id="51548-130">Angiv standardrapporter, der skal bruges til forskellige dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="51548-130">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="51548-131">Rapportvalg i Business Central</span><span class="sxs-lookup"><span data-stu-id="51548-131">Report Selection in Business Central</span></span>](across-report-selections.md)|

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="51548-132">Se relateret oplæring på [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="51548-132">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="51548-133">Se også</span><span class="sxs-lookup"><span data-stu-id="51548-133">See Also</span></span>
[<span data-ttu-id="51548-134">Salg</span><span class="sxs-lookup"><span data-stu-id="51548-134">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="51548-135">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="51548-135">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]