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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: df7ce179f14fdaea9a65645d6ccf5d69076212db
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194111"
---
# <a name="the-microsoft-pay-extension"></a><span data-ttu-id="86dea-103">Udvidelsen Microsoft Pay</span><span class="sxs-lookup"><span data-stu-id="86dea-103">The Microsoft Pay Extension</span></span>

> [!IMPORTANT]
> <span data-ttu-id="86dea-104">Med ikrafttræden den 8. februar 2020 vil ændringer i Microsoft Pay-tjenesten påvirke Microsoft Pay-udvidelsen i Microsoft [!INCLUDE[d365fin](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="86dea-104">Effective February 8 2020, changes in the Microsoft Pay service will affect the Microsoft Pay extension in Microsoft [!INCLUDE[d365fin](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="86dea-105">På grund af de ændringer vil **Betal nu**-betalingslinks, som  Microsoft Pay-udvidelsen genererer for fakturaer i [!INCLUDE[d365fin](includes/d365fin_md.md)], ikke åbne Microsoft Pay efter den 8. februar.</span><span class="sxs-lookup"><span data-stu-id="86dea-105">Due to the changes, after February 8, the **Pay now** payment links that the Microsoft Pay extension generates for invoices in [!INCLUDE[d365fin](includes/d365fin_md.md)] will not open Microsoft Pay.</span></span> <span data-ttu-id="86dea-106">Kunder, der bruger udvidelsen, skal ændre deres konfiguration af betalingstjenester for at begynde at bruge PayPal-udvidelsen i stedet.</span><span class="sxs-lookup"><span data-stu-id="86dea-106">Customers who are using the extension should change their Payment Services setup to start using the PayPal extension instead.</span></span><br /></br>
>
> <span data-ttu-id="86dea-107">Fra den 8. januar viser vi en meddelelse i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="86dea-107">From January 8, we will display a notification in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="86dea-108">Meddelelsen vil indeholde et link til de indstillinger, du skal ændre, og til flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="86dea-108">The notification will contain a link to the settings that you need to change and to more information.</span></span> <span data-ttu-id="86dea-109">Efter den 8. februar vil Microsoft Pay-udvidelsen ikke længere være tilgængelig i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="86dea-109">After February 8, the Microsoft Pay extension will no longer be available in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span><br /></br>
>
> <span data-ttu-id="86dea-110">Ændringerne påvirker følgende versioner af Business Central:</span><span class="sxs-lookup"><span data-stu-id="86dea-110">The changes impact the following versions of Business Central:</span></span>
> - <span data-ttu-id="86dea-111">Microsoft Dynamics 365 Business Central, oktober 2018</span><span class="sxs-lookup"><span data-stu-id="86dea-111">Microsoft Dynamics 365 Business Central October 2018</span></span>
> - <span data-ttu-id="86dea-112">Microsoft Dynamics 365 Business Central, april 2019</span><span class="sxs-lookup"><span data-stu-id="86dea-112">Microsoft Dynamics 365 Business Central April 2019</span></span>
> - <span data-ttu-id="86dea-113">Microsoft Dynamics 365 Business Central, frigivelsesbølge 2 i 2019</span><span class="sxs-lookup"><span data-stu-id="86dea-113">Microsoft Dynamics 365 Business Central 2019 Release Wave 2</span></span>

<span data-ttu-id="86dea-114">Kunder kræver hele tiden bedre kundeservice, både med hensyn til produkternes kvalitet, men også med hensyn til leverings- og betalingstjenester.</span><span class="sxs-lookup"><span data-stu-id="86dea-114">Customers continuously require higher customer service, both in terms of the quality of product but also in terms of delivery and payment services.</span></span> <span data-ttu-id="86dea-115">Tjenesten Microsoft Pay hjælper dig med at øge din kundeservice.</span><span class="sxs-lookup"><span data-stu-id="86dea-115">The Microsoft Pay service helps you increase your customer service.</span></span>

<span data-ttu-id="86dea-116">Microsoft Pay-udvidelsen føjer et Microsoft Pay-link til dine salgsdokumenter, så kunderne nemt kan betale ved hjælp af Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="86dea-116">The Microsoft Pay extension adds a Microsoft Pay link to your sales documents so customers can easily pay using Microsoft Pay.</span></span> <span data-ttu-id="86dea-117">Derefter kan du sende dokumenterne via e-mail for at yde højere kundeservice og reducere den tid, det tager for kundernes betalinger at gå ind på din bankkonto.</span><span class="sxs-lookup"><span data-stu-id="86dea-117">Then you can send the documents by email to provide higher customer service and shorten the time it takes for customers’ payments to arrive on your bank account.</span></span>

<span data-ttu-id="86dea-118">Microsoft Pay-udvidelsen giver følgende fordele:</span><span class="sxs-lookup"><span data-stu-id="86dea-118">The Microsoft Pay extension provides the following benefits:</span></span>
- <span data-ttu-id="86dea-119">Debitorbetalinger vises hurtigere på bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="86dea-119">Customer payments appear faster on your bank account.</span></span>
- <span data-ttu-id="86dea-120">Kunder har flere måder at betale fakturaer på.</span><span class="sxs-lookup"><span data-stu-id="86dea-120">Customers have more ways to pay invoices.</span></span>
- <span data-ttu-id="86dea-121">Microsoft Pay tilbyder en pålidelig betalingstjeneste, som debitorer foretrækker frem for at angive kreditkortoplysninger på ukendte websteder.</span><span class="sxs-lookup"><span data-stu-id="86dea-121">Microsoft Pay offers a trustworthy payment service, which customers prefer to entering credit card information on unknown web sites.</span></span>
- <span data-ttu-id="86dea-122">Microsoft Pay tilbyder flere måder til håndtering af betalinger, herunder kreditkortbehandling via f.eks. PayPal og Stripe.</span><span class="sxs-lookup"><span data-stu-id="86dea-122">Microsoft Pay offers multiple ways of handling payments, including credit card processing, such as PayPal and Stripe.</span></span>
- <span data-ttu-id="86dea-123">Linket til Microsoft Pay kan integreres automatisk på alle fakturadokumenter eller af brugeren.</span><span class="sxs-lookup"><span data-stu-id="86dea-123">The Microsoft Pay link can be embedded automatically on every invoice document or by the user.</span></span>
- <span data-ttu-id="86dea-124">Da denne funktion er udviklet som en udvidelse, kan du altid aktivere den, når og hvis dine forretningsprocesser kræver det.</span><span class="sxs-lookup"><span data-stu-id="86dea-124">Because this functionality is built as an extension, it gives you full control to enable it when and if your business processes require it.</span></span>

<span data-ttu-id="86dea-125">Aktivering af betalingstjenesteudvidelser er gratis i [!INCLUDE[d365fin](includes/d365fin_md.md)], men du skal kontakte betalingstjenesten for at få en konto.</span><span class="sxs-lookup"><span data-stu-id="86dea-125">Enabling payment service extensions is free in [!INCLUDE[d365fin](includes/d365fin_md.md)], however, you will need to contact the payment service to get an account.</span></span> <span data-ttu-id="86dea-126">Du kan finde flere oplysninger i [Aktivere debitorbetalinger via betalingstjenester](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="86dea-126">For more information, see [Enable Customer Payment Through Payment Services](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="86dea-127">Se også</span><span class="sxs-lookup"><span data-stu-id="86dea-127">See Also</span></span>
<span data-ttu-id="86dea-128">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="86dea-128">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="86dea-129">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="86dea-129">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="86dea-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="86dea-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
