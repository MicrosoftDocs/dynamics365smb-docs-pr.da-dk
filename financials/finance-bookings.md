---
title: Fakturere dine reservationer i Dynamics 365 | Microsoft Docs
description: "Få mere at vide, hvordan du kan udstede flere fakturaer ad gangen fra Microsoft Bookings i Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 06/14/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1f1a1645ba27a3b42d67c11f7472c283ca44dbd1
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a><span data-ttu-id="736e0-103">Massefakturering for Microsoft Bookings i [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="736e0-103">Bulk Invoicing for Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="736e0-104">Hvis dit firma bruger Bookings-appen i Office 365, kan du udstede flere fakturaer ad gangen for aftaler.</span><span class="sxs-lookup"><span data-stu-id="736e0-104">If your company uses the Bookings app in Office 365, you can do bulk invoicing for appointments.</span></span> <span data-ttu-id="736e0-105">Siden **Ikke-fakturerede Bookings** i [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en oversigt over virksomhedens udførte reservationer.</span><span class="sxs-lookup"><span data-stu-id="736e0-105">The **Uninvoiced Bookings** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a list of the company's completed bookings.</span></span> <span data-ttu-id="736e0-106">På denne side kan du hurtigt vælge de aftaler, som du vil fakturere, og oprette udkast til fakturaer for de ydede services.</span><span class="sxs-lookup"><span data-stu-id="736e0-106">In this page you can quickly select the appointments that you want to invoice and create draft invoices for the services provided.</span></span>  

## <a name="connect-to-bookings"></a><span data-ttu-id="736e0-107">Oprette forbindelse til Bookings</span><span class="sxs-lookup"><span data-stu-id="736e0-107">Connect to Bookings</span></span>
<span data-ttu-id="736e0-108">For at forbinde din [!INCLUDE[d365fin](includes/d365fin_md.md)] med Bookings skal du angive din Bookings-virksomhed, hvad der skal synkroniseres med Bookings, hvor ofte synkroniseringen skal foretages, og hvilke skabeloner der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="736e0-108">To connect your [!INCLUDE[d365fin](includes/d365fin_md.md)] with Bookings, you must specify your Bookings company, what to synchronize with Bookings, how often to synchronize, and which templates to use.</span></span> <span data-ttu-id="736e0-109">Du kan oprette oplysningerne på siden **Opsætning af Bookings-synkronisering**, som du kan starte fra siden **Opsætning af Exchange-synkronisering**, som du kan finde via [Søg](ui-search.md).</span><span class="sxs-lookup"><span data-stu-id="736e0-109">You set up this information in the **Booking Sync. Setup** page, which you can launch from the **Exchange Sync. Setup** page, which you can find through [Search](ui-search.md).</span></span>  

<span data-ttu-id="736e0-110">Hvis du vil synkronisere kunder mellem Bookings og [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du angive den standardskabelon, der skal bruges, for at tilføje nye debitorer i [!INCLUDE[d365fin](includes/d365fin_md.md)] baseret på debitorerne i din Bookings-virksomhed.</span><span class="sxs-lookup"><span data-stu-id="736e0-110">For example, if you want to synchronize customers between Bookings and [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the default template to use to add new customers in [!INCLUDE[d365fin](includes/d365fin_md.md)] based on the customers in your Bookings company.</span></span>  

## <a name="invoice-appointments"></a><span data-ttu-id="736e0-111">Fakturaaftaler</span><span class="sxs-lookup"><span data-stu-id="736e0-111">Invoice Appointments</span></span>
<span data-ttu-id="736e0-112">Når du skal sende fakturaer for de færdige reservationer, skal du gå til siden **Ikke-fakturerede Bookings**.</span><span class="sxs-lookup"><span data-stu-id="736e0-112">When it is time to send invoices for the completed bookings, you go to the **Uninvoiced Bookings** page.</span></span> <span data-ttu-id="736e0-113">Afhængigt af hvor ofte oplysningerne synkroniseres er listen lang eller kort.</span><span class="sxs-lookup"><span data-stu-id="736e0-113">Depending on how often the information is synchronized, the list is long or short.</span></span> <span data-ttu-id="736e0-114">Du kan oprette fakturaer for alle reservationer på listen eller én reservation ad gangen.</span><span class="sxs-lookup"><span data-stu-id="736e0-114">You can create invoices for all bookings in the list or one booking at a time.</span></span> <span data-ttu-id="736e0-115">Du kan vælge en eller flere poster på listen og fakturere dem som de eneste.</span><span class="sxs-lookup"><span data-stu-id="736e0-115">You can select one or more entries in the list and invoice those only.</span></span>  

<span data-ttu-id="736e0-116">Understøttelse af faktureringsaftaler fra Bookings er lettere end den fulde arbejdsproces, hvor du arbejder med tilbud, salgsordrer og salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="736e0-116">The support for invoicing appointments from Bookings is simpler than the fuller workflow of working with sales quotes, sales orders, and sales invoices.</span></span> <span data-ttu-id="736e0-117">Du kan finde flere oplysninger under [Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="736e0-117">For more information, see [How to: Invoice Sales](sales-how-invoice-sales.md).</span></span> <span data-ttu-id="736e0-118">Du kan vælge at sælge dine tjenesteydelser ved hjælp af [!INCLUDE[d365fin](includes/d365fin_md.md)] eller vælge at bruge Bookings, afhængigt af dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="736e0-118">You can choose to sell your services using [!INCLUDE[d365fin](includes/d365fin_md.md)] or choose to use Bookings, depending on your business needs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="736e0-119">Se også</span><span class="sxs-lookup"><span data-stu-id="736e0-119">See Also</span></span>
[<span data-ttu-id="736e0-120">Finans</span><span class="sxs-lookup"><span data-stu-id="736e0-120">Finance</span></span>](finance.md)  
[<span data-ttu-id="736e0-121">Fremgangsmåde: Fakturere salg</span><span class="sxs-lookup"><span data-stu-id="736e0-121">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="736e0-122">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="736e0-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="736e0-123">Microsoft Bookings</span><span class="sxs-lookup"><span data-stu-id="736e0-123">Microsoft Bookings</span></span>](https://products.office.com/en-us/business/scheduling-and-booking-app)  

