---
title: Aktivere debitorbetalinger via betalingstjenester | Microsoft Docs
description: Gør det lettere for kunderne at betale deres fakturaer ved at aktivere betalingstjenester.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5fa58c177629fdf386bca0ebfce2b668a55cbc8f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393345"
---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="9cd81-103">Aktivere debitorbetalinger via betalingstjenester</span><span class="sxs-lookup"><span data-stu-id="9cd81-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="9cd81-104">Som et alternativ til opkrævning af betalinger via bankoverførsel eller kreditkort kan dine kunder betale dig via deres konto hos betalingstjenester som Microsoft Pay, PayPal eller WorldPay.</span><span class="sxs-lookup"><span data-stu-id="9cd81-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="9cd81-105">Når du har aktiveret en betalingstjeneste i [!INCLUDE[prod_short](includes/prod_short.md)], vises der et link til tjenesten på de salgsdokumenter, som du sender med mail til dine kunder.</span><span class="sxs-lookup"><span data-stu-id="9cd81-105">After you enable a payment service in [!INCLUDE[prod_short](includes/prod_short.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="9cd81-106">Kunder kan bruge linket til at gå til betalingstjenesten og betale fakturaen direkte fra salgsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="9cd81-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="9cd81-107">Hvis du ikke vil indsætte linket, f.eks. hvis en debitor betaler kontant, kan du fjerne betalingstjenesten fra fakturaen inden bogføringen.</span><span class="sxs-lookup"><span data-stu-id="9cd81-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="9cd81-108">Microsoft Pay-, PayPal Payments Standard- og WorldPay Payments Standard-udvidelserne installeres i [!INCLUDE[prod_short](includes/prod_short.md)] og er klar til aktivering.</span><span class="sxs-lookup"><span data-stu-id="9cd81-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[prod_short](includes/prod_short.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-prod_short"></a><span data-ttu-id="9cd81-109">Sådan aktiverer du en betalingstjeneste i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="9cd81-109">To enable a payment service in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>
1. <span data-ttu-id="9cd81-110">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Betalingstjenester**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="9cd81-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9cd81-111">På siden **Betalingstjenester** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9cd81-111">On the **Payment Services** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="9cd81-112">Vælg betalingstjenesten, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="9cd81-112">Select the payment service, and then close the page.</span></span>  
4. <span data-ttu-id="9cd81-113">På siden **Betalingstjenester** skal du vælge handlingen **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="9cd81-113">On the **Payment Services** page, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="9cd81-114">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="9cd81-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="9cd81-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9cd81-115">Close the page.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="9cd81-116">Sådan vælger du en betalingstjeneste på en salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="9cd81-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="9cd81-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="9cd81-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9cd81-118">Åbn den faktura, du vil betale med betalingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="9cd81-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="9cd81-119">Vælg betalingstjenesten i feltet **Betalingstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="9cd81-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="9cd81-120">Feltet **Betalingstjeneste** er kun tilgængeligt, hvis du har aktiveret betalingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="9cd81-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9cd81-121">Se også</span><span class="sxs-lookup"><span data-stu-id="9cd81-121">See Also</span></span>  
[<span data-ttu-id="9cd81-122">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="9cd81-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="9cd81-123">Salg</span><span class="sxs-lookup"><span data-stu-id="9cd81-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="9cd81-124">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="9cd81-124">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="9cd81-125">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9cd81-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]