---
title: Microsoft Pay Standard| Microsoft Docs
description: Indeholder oplysninger om Microsoft Pay-udvidelsen
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 748316c411c4b04947685c6053e9c53aa9102c35
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747564"
---
# <a name="the-microsoft-pay-extension"></a><span data-ttu-id="b6291-103">Udvidelsen Microsoft Pay</span><span class="sxs-lookup"><span data-stu-id="b6291-103">The Microsoft Pay Extension</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6291-104">Med ikrafttræden den 8. februar 2020 vil ændringer i Microsoft Pay-tjenesten påvirke Microsoft Pay-udvidelsen i Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span><span class="sxs-lookup"><span data-stu-id="b6291-104">Effective February 8 2020, changes in the Microsoft Pay service will affect the Microsoft Pay extension in Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span></span> <span data-ttu-id="b6291-105">På grund af de ændringer vil **Betal nu**-betalingslinks, som  Microsoft Pay-udvidelsen genererer for fakturaer i [!INCLUDE[prod_short](includes/prod_short.md)], ikke åbne Microsoft Pay efter den 8. februar.</span><span class="sxs-lookup"><span data-stu-id="b6291-105">Due to the changes, after February 8, the **Pay now** payment links that the Microsoft Pay extension generates for invoices in [!INCLUDE[prod_short](includes/prod_short.md)] will not open Microsoft Pay.</span></span> <span data-ttu-id="b6291-106">Kunder, der bruger udvidelsen, skal ændre deres konfiguration af betalingstjenester for at begynde at bruge PayPal-udvidelsen i stedet.</span><span class="sxs-lookup"><span data-stu-id="b6291-106">Customers who are using the extension should change their Payment Services setup to start using the PayPal extension instead.</span></span><br /></br>
>
> <span data-ttu-id="b6291-107">Fra den 8. januar viser vi en meddelelse i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b6291-107">From January 8, we will display a notification in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b6291-108">Meddelelsen vil indeholde et link til de indstillinger, du skal ændre, og til flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="b6291-108">The notification will contain a link to the settings that you need to change and to more information.</span></span> <span data-ttu-id="b6291-109">Efter den 8. februar vil Microsoft Pay-udvidelsen ikke længere være tilgængelig i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b6291-109">After February 8, the Microsoft Pay extension will no longer be available in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span><br /></br>
>
> <span data-ttu-id="b6291-110">Ændringerne påvirker følgende versioner af Business Central:</span><span class="sxs-lookup"><span data-stu-id="b6291-110">The changes impact the following versions of Business Central:</span></span>
> - <span data-ttu-id="b6291-111">Microsoft Dynamics 365 Business Central, oktober 2018</span><span class="sxs-lookup"><span data-stu-id="b6291-111">Microsoft Dynamics 365 Business Central October 2018</span></span>
> - <span data-ttu-id="b6291-112">Microsoft Dynamics 365 Business Central, april 2019</span><span class="sxs-lookup"><span data-stu-id="b6291-112">Microsoft Dynamics 365 Business Central April 2019</span></span>
> - <span data-ttu-id="b6291-113">Microsoft Dynamics 365 Business Central, frigivelsesbølge 2 i 2019</span><span class="sxs-lookup"><span data-stu-id="b6291-113">Microsoft Dynamics 365 Business Central 2019 Release Wave 2</span></span>

<span data-ttu-id="b6291-114">Kunder kræver hele tiden bedre kundeservice, både med hensyn til produkternes kvalitet, men også med hensyn til leverings- og betalingstjenester.</span><span class="sxs-lookup"><span data-stu-id="b6291-114">Customers continuously require higher customer service, both in terms of the quality of product but also in terms of delivery and payment services.</span></span> <span data-ttu-id="b6291-115">Tjenesten Microsoft Pay hjælper dig med at øge din kundeservice.</span><span class="sxs-lookup"><span data-stu-id="b6291-115">The Microsoft Pay service helps you increase your customer service.</span></span>

<span data-ttu-id="b6291-116">Microsoft Pay-udvidelsen føjer et Microsoft Pay-link til dine salgsdokumenter, så kunderne nemt kan betale ved hjælp af Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="b6291-116">The Microsoft Pay extension adds a Microsoft Pay link to your sales documents so customers can easily pay using Microsoft Pay.</span></span> <span data-ttu-id="b6291-117">Derefter kan du sende dokumenterne via e-mail for at yde højere kundeservice og reducere den tid, det tager for kundernes betalinger at gå ind på din bankkonto.</span><span class="sxs-lookup"><span data-stu-id="b6291-117">Then you can send the documents by email to provide higher customer service and shorten the time it takes for customers’ payments to arrive on your bank account.</span></span>

<span data-ttu-id="b6291-118">Microsoft Pay-udvidelsen giver følgende fordele:</span><span class="sxs-lookup"><span data-stu-id="b6291-118">The Microsoft Pay extension provides the following benefits:</span></span>
- <span data-ttu-id="b6291-119">Debitorbetalinger vises hurtigere på bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="b6291-119">Customer payments appear faster on your bank account.</span></span>
- <span data-ttu-id="b6291-120">Kunder har flere måder at betale fakturaer på.</span><span class="sxs-lookup"><span data-stu-id="b6291-120">Customers have more ways to pay invoices.</span></span>
- <span data-ttu-id="b6291-121">Microsoft Pay tilbyder en pålidelig betalingstjeneste, som debitorer foretrækker frem for at angive kreditkortoplysninger på ukendte websteder.</span><span class="sxs-lookup"><span data-stu-id="b6291-121">Microsoft Pay offers a trustworthy payment service, which customers prefer to entering credit card information on unknown web sites.</span></span>
- <span data-ttu-id="b6291-122">Microsoft Pay tilbyder flere måder til håndtering af betalinger, herunder kreditkortbehandling via f.eks. PayPal og Stripe.</span><span class="sxs-lookup"><span data-stu-id="b6291-122">Microsoft Pay offers multiple ways of handling payments, including credit card processing, such as PayPal and Stripe.</span></span>
- <span data-ttu-id="b6291-123">Linket til Microsoft Pay kan integreres automatisk på alle fakturadokumenter eller af brugeren.</span><span class="sxs-lookup"><span data-stu-id="b6291-123">The Microsoft Pay link can be embedded automatically on every invoice document or by the user.</span></span>
- <span data-ttu-id="b6291-124">Da denne funktion er udviklet som en udvidelse, kan du altid aktivere den, når og hvis dine forretningsprocesser kræver det.</span><span class="sxs-lookup"><span data-stu-id="b6291-124">Because this functionality is built as an extension, it gives you full control to enable it when and if your business processes require it.</span></span>

<span data-ttu-id="b6291-125">Aktivering af betalingstjenesteudvidelser er gratis i [!INCLUDE[prod_short](includes/prod_short.md)], men du skal kontakte betalingstjenesten for at få en konto.</span><span class="sxs-lookup"><span data-stu-id="b6291-125">Enabling payment service extensions is free in [!INCLUDE[prod_short](includes/prod_short.md)], however, you will need to contact the payment service to get an account.</span></span> <span data-ttu-id="b6291-126">Du kan finde flere oplysninger i [Aktivere debitorbetalinger via betalingstjenester](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="b6291-126">For more information, see [Enable Customer Payment Through Payment Services](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b6291-127">Se også</span><span class="sxs-lookup"><span data-stu-id="b6291-127">See Also</span></span>
<span data-ttu-id="b6291-128">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="b6291-128">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="b6291-129">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="b6291-129">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="b6291-130">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b6291-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
