---
title: Aktivere debitorbetalinger via betalingstjenester | Microsoft Docs
description: "Gør det lettere for kunderne at betale deres fakturaer ved at aktivere betalingstjenester."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c8f3faa68280a1c6157ab62ca2a19ce964bdbfd4
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="76fa5-103">Aktivere debitorbetalinger via betalingstjenester</span><span class="sxs-lookup"><span data-stu-id="76fa5-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="76fa5-104">Som et alternativ til opkrævning af betalinger via bankoverførsel eller kreditkort kan dine kunder betale dig via deres konto hos betalingstjenester som Microsoft Pay, PayPal eller WorldPay.</span><span class="sxs-lookup"><span data-stu-id="76fa5-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="76fa5-105">Når du har aktiveret en betalingstjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)], vises der et link til tjenesten på de salgsdokumenter, som du sender med mail til dine kunder.</span><span class="sxs-lookup"><span data-stu-id="76fa5-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="76fa5-106">Kunder kan bruge linket til at gå til betalingstjenesten og betale fakturaen direkte fra salgsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="76fa5-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="76fa5-107">Hvis du ikke vil indsætte linket, f.eks. hvis en debitor betaler kontant, kan du fjerne betalingstjenesten fra fakturaen inden bogføringen.</span><span class="sxs-lookup"><span data-stu-id="76fa5-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="76fa5-108">Microsoft Pay-, PayPal Payments Standard- og WorldPay Payments Standard-udvidelserne installeres i [!INCLUDE[d365fin](includes/d365fin_md.md)] og er klar til aktivering.</span><span class="sxs-lookup"><span data-stu-id="76fa5-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a><span data-ttu-id="76fa5-109">Sådan aktiverer du en betalingstjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="76fa5-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="76fa5-110">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingstjenester**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="76fa5-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="76fa5-111">I vinduet **Betalingstjenester** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="76fa5-111">In the **Payment Services** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="76fa5-112">Vælg betalingstjenesten, og luk derefter vinduet.</span><span class="sxs-lookup"><span data-stu-id="76fa5-112">Select the payment service, and then close the window.</span></span>  
4. <span data-ttu-id="76fa5-113">I vinduet **Betalingstjenester** skal du vælge handlingen **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="76fa5-113">In the **Payment Services** window, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="76fa5-114">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="76fa5-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="76fa5-115">Luk vinduet.</span><span class="sxs-lookup"><span data-stu-id="76fa5-115">Close the window.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="76fa5-116">Sådan vælger du en betalingstjeneste på en salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="76fa5-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="76fa5-117">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="76fa5-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="76fa5-118">Åbn den faktura, du vil betale med betalingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="76fa5-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="76fa5-119">Vælg betalingstjenesten i feltet **Betalingstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="76fa5-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="76fa5-120">Feltet **Betalingstjeneste** er kun tilgængeligt, hvis du har aktiveret betalingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="76fa5-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="76fa5-121">Se også</span><span class="sxs-lookup"><span data-stu-id="76fa5-121">See Also</span></span>  
[<span data-ttu-id="76fa5-122">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="76fa5-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="76fa5-123">Salg</span><span class="sxs-lookup"><span data-stu-id="76fa5-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="76fa5-124">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="76fa5-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="76fa5-125">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="76fa5-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

