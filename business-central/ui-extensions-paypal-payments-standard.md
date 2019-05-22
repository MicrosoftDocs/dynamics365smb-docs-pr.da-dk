---
title: Bruge udvidelsen PayPal Payments Standard | Microsoft Docs
description: Beskriver, hvordan du bruger udvidelsen til at gøre det muligt for kunder at foretage betalinger med PayPal.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f715108b17d355084fee7983e106cd33dd476906
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249763"
---
# <a name="the-paypal-payments-standard-extension"></a><span data-ttu-id="9925e-103">Udvidelsen PayPal Payments Standard</span><span class="sxs-lookup"><span data-stu-id="9925e-103">The PayPal Payments Standard Extension</span></span>
<span data-ttu-id="9925e-104">Kunder kræver hele tiden bedre kundeservice, både med hensyn til produkternes kvalitet, men også med hensyn til leverings- og betalingsindstillinger.</span><span class="sxs-lookup"><span data-stu-id="9925e-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="9925e-105">Tjenesten PayPal Payments Standard hjælper dig med at øge din kundeservice.</span><span class="sxs-lookup"><span data-stu-id="9925e-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="9925e-106">Som et alternativ til opkrævning af betalinger via bankoverførsel eller kreditkort kan du tilbyde dine kunder at betale via deres PayPal-konto.</span><span class="sxs-lookup"><span data-stu-id="9925e-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="9925e-107">Når du sender en salgsfaktura eller en salgsordre med mail, er der et PayPal-link i brødteksten i mailen og i det vedhæftede PDF-dokument.</span><span class="sxs-lookup"><span data-stu-id="9925e-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="9925e-108">Når kunden vælger linket, vises servicesiden for deres PayPal-konto med betalingsoplysningerne for salget.</span><span class="sxs-lookup"><span data-stu-id="9925e-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="9925e-109">Kunden kan derefter betale fakturaen som andre PayPal-betalinger.</span><span class="sxs-lookup"><span data-stu-id="9925e-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="9925e-110">Tjenesten PayPal Payments Standard giver følgende fordele:</span><span class="sxs-lookup"><span data-stu-id="9925e-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="9925e-111">Debitorbetalinger kommer hurtigere ind på bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="9925e-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="9925e-112">Kunder har flere måder at betale fakturaer på.</span><span class="sxs-lookup"><span data-stu-id="9925e-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="9925e-113">PayPal tilbyder en pålidelig betalingstjeneste, som debitorer foretrækker frem for at angive kreditkortoplysninger på websteder.</span><span class="sxs-lookup"><span data-stu-id="9925e-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="9925e-114">PayPal tilbyder flere måder til håndtering af betalinger, herunder kreditkort, PayPal-konti og andre kilder.</span><span class="sxs-lookup"><span data-stu-id="9925e-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="9925e-115">PayPal-linket kan tilføjes automatisk til salgsdokumenter eller manuelt af brugeren.</span><span class="sxs-lookup"><span data-stu-id="9925e-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="9925e-116">Tjenesten PayPal Payments Standard er uden månedlige gebyrer eller opsætningsgebyrer.</span><span class="sxs-lookup"><span data-stu-id="9925e-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="9925e-117">Da PayPal Payments Standard er en udvidelse, kan du nemt aktivere den, når og hvis din virksomhed kræver det.</span><span class="sxs-lookup"><span data-stu-id="9925e-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="9925e-118">Du kan finde flere oplysninger i [Aktivere debitorbetaling via PayPal](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="9925e-118">For more information, see [Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9925e-119">Se også</span><span class="sxs-lookup"><span data-stu-id="9925e-119">See Also</span></span>
<span data-ttu-id="9925e-120">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="9925e-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="9925e-121">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="9925e-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="9925e-122">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9925e-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
