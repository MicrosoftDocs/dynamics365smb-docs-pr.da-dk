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
ms.date: 06/01/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 75ed584feda066a6c412f861bd624646c4c31085
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="setting-up-sales"></a><span data-ttu-id="58988-103">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="58988-103">Setting Up Sales</span></span>
<span data-ttu-id="58988-104">Før du kan administrere salgsprocesser, skal du konfigurere de regler og værdier, der definerer virksomhedens salgspolitikker.</span><span class="sxs-lookup"><span data-stu-id="58988-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="58988-105">Du skal definere den generelle opsætning, f.eks. hvilke salgsdokumenter der kræves, og hvordan dokumenternes værdier bogføres.</span><span class="sxs-lookup"><span data-stu-id="58988-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="58988-106">Denne generelle opsætning udføres typisk én gang i forbindelse med den indledende implementering.</span><span class="sxs-lookup"><span data-stu-id="58988-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="58988-107">En særskilt sæt opgaver i forbindelse med registrering af nye debitorer er at registrere en særlig pris eller rabataftaler, du indgår med hver debitorer.</span><span class="sxs-lookup"><span data-stu-id="58988-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="58988-108">Den finansrelaterede salgsopsætning, som betalingsmetoder og valutaer, dækkes i afsnittet Konfigurere Finans.</span><span class="sxs-lookup"><span data-stu-id="58988-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="58988-109">Der er flere oplysninger i [Konfigurere Finans](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="58988-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="58988-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="58988-110">To</span></span> | <span data-ttu-id="58988-111">Se</span><span class="sxs-lookup"><span data-stu-id="58988-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="58988-112">Opret et debitorkort for hver debitor, du sælger til.</span><span class="sxs-lookup"><span data-stu-id="58988-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="58988-113">Fremgangsmåde: Registrere nye debitorer</span><span class="sxs-lookup"><span data-stu-id="58988-113">How to: Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="58988-114">Aktivere debitorer til at betale via PayPal, ved at vælge PayPal-logoet på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="58988-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="58988-115">Fremgangsmåde: Aktivere debitorbetaling via PayPal</span><span class="sxs-lookup"><span data-stu-id="58988-115">How to: Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="58988-116">Angive forskellige rabatter og specialpriser, som du yder kunderne, afhængigt af varen, antal og/eller dato.</span><span class="sxs-lookup"><span data-stu-id="58988-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="58988-117">Fremgangsmåde: Registrere salgspris, rabat og betalingsaftaler</span><span class="sxs-lookup"><span data-stu-id="58988-117">How to: Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="58988-118">Konfigurer sælgere, så du kan tildele dem til debitorkontakter eller måle sælgernes præstationer som grundlag for beregning af salgsprovision eller bonus.</span><span class="sxs-lookup"><span data-stu-id="58988-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="58988-119">Fremgangsmåde: Konfigurere sælgere</span><span class="sxs-lookup"><span data-stu-id="58988-119">How to: Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="58988-120">Angiv for individuelle debitorer eller for alle kunder, hvordan salgsdokumenterne sendes som standard, når du vælger **Bogfør og send** handlingen.</span><span class="sxs-lookup"><span data-stu-id="58988-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="58988-121">Fremgangsmåde: Konfigurere dokumentafsendelsesprofiler</span><span class="sxs-lookup"><span data-stu-id="58988-121">How to: Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="58988-122">Konfigurer din mail til at indeholde en oversigt over oplysningerne i det salgsdokument, der skal sendes.</span><span class="sxs-lookup"><span data-stu-id="58988-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="58988-123">[Fremgangsmåde: Sende dokumenter via mail](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="58988-123">[How to: Send Documents by Email](ui-how-send-documents-email.md).</span></span> |

## <a name="see-also"></a><span data-ttu-id="58988-124">Se også</span><span class="sxs-lookup"><span data-stu-id="58988-124">See Also</span></span>
[<span data-ttu-id="58988-125">Salg</span><span class="sxs-lookup"><span data-stu-id="58988-125">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="58988-126">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="58988-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

