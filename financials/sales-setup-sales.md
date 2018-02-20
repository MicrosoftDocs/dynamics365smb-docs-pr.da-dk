---
title: Oversigt over opgaver til konfiguration af salgsprocesser | Microsoft Docs
description: "Beskriver opgaver til oprettelse af regler og værdier, som du kan bruge til at definere virksomhedens salgspolitikker og -processer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 10/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6407b49cf9b5e844b4e0920ccf1fc299d96ae34f
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-sales"></a><span data-ttu-id="bee70-103">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="bee70-103">Setting Up Sales</span></span>
<span data-ttu-id="bee70-104">Før du kan administrere salgsprocesser, skal du konfigurere de regler og værdier, der definerer virksomhedens salgspolitikker.</span><span class="sxs-lookup"><span data-stu-id="bee70-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="bee70-105">Du skal definere den generelle opsætning, f.eks. hvilke salgsdokumenter der kræves, og hvordan dokumenternes værdier bogføres.</span><span class="sxs-lookup"><span data-stu-id="bee70-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="bee70-106">Denne generelle opsætning udføres typisk én gang i forbindelse med den indledende implementering.</span><span class="sxs-lookup"><span data-stu-id="bee70-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="bee70-107">En særskilt sæt opgaver i forbindelse med registrering af nye debitorer er at registrere en særlig pris eller rabataftaler, du indgår med hver debitorer.</span><span class="sxs-lookup"><span data-stu-id="bee70-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="bee70-108">Den finansrelaterede salgsopsætning, som betalingsmetoder og valutaer, dækkes i afsnittet Konfigurere Finans.</span><span class="sxs-lookup"><span data-stu-id="bee70-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="bee70-109">Der er flere oplysninger i [Konfigurere Finans](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="bee70-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="bee70-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="bee70-110">To</span></span> | <span data-ttu-id="bee70-111">Se</span><span class="sxs-lookup"><span data-stu-id="bee70-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="bee70-112">Opret et debitorkort for hver debitor, du sælger til.</span><span class="sxs-lookup"><span data-stu-id="bee70-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="bee70-113">Registrere nye debitorer</span><span class="sxs-lookup"><span data-stu-id="bee70-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="bee70-114">Aktivere debitorer til at betale via PayPal, ved at vælge PayPal-logoet på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="bee70-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="bee70-115">Aktivere debitorbetaling via PayPal</span><span class="sxs-lookup"><span data-stu-id="bee70-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="bee70-116">Angive forskellige rabatter og specialpriser, som du yder kunderne, afhængigt af varen, antal og/eller dato.</span><span class="sxs-lookup"><span data-stu-id="bee70-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="bee70-117">Registrere salgspris, rabat og betalingsaftaler</span><span class="sxs-lookup"><span data-stu-id="bee70-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="bee70-118">Konfigurer sælgere, så du kan tildele dem til debitorkontakter eller måle sælgernes præstationer som grundlag for beregning af salgsprovision eller bonus.</span><span class="sxs-lookup"><span data-stu-id="bee70-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="bee70-119">Konfigurere sælgere</span><span class="sxs-lookup"><span data-stu-id="bee70-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="bee70-120">Angiv for individuelle debitorer eller for alle kunder, hvordan salgsdokumenterne sendes som standard, når du vælger **Bogfør og send** handlingen.</span><span class="sxs-lookup"><span data-stu-id="bee70-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="bee70-121">Konfigurere dokumentafsendelsesprofiler</span><span class="sxs-lookup"><span data-stu-id="bee70-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="bee70-122">Konfigurer din mail til at indeholde en oversigt over oplysningerne i det salgsdokument, der skal sendes.</span><span class="sxs-lookup"><span data-stu-id="bee70-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="bee70-123">[Sende dokumenter som mail](ui-how-send-documents-email.md)</span><span class="sxs-lookup"><span data-stu-id="bee70-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="bee70-124">Bruge en EU-webtjeneste til at kontrollere en kundes SE/CVR-nummer.</span><span class="sxs-lookup"><span data-stu-id="bee70-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="bee70-125">Kontrollere SE/CVR-numre</span><span class="sxs-lookup"><span data-stu-id="bee70-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="bee70-126">Angive oplysninger om de forskellige transportleverandører, virksomheden bruger, herunder et link til deres pakkesporingsservice.</span><span class="sxs-lookup"><span data-stu-id="bee70-126">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="bee70-127">Oprette speditører</span><span class="sxs-lookup"><span data-stu-id="bee70-127">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a><span data-ttu-id="bee70-128">Se også</span><span class="sxs-lookup"><span data-stu-id="bee70-128">See Also</span></span>
[<span data-ttu-id="bee70-129">Salg</span><span class="sxs-lookup"><span data-stu-id="bee70-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="bee70-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bee70-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

