---
title: Betalingsudligning med Envestnet Yodlee Bank Feeds-udvidelsen | Microsoft Docs
description: Beskriver udvidelsen Envestnet Yodlee Bank Feeds, der sammenkæder med bankkonti, så du hurtigt kan afstemme betalinger.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6089a51a0ef27175988ed0c00fdb353cd3c7e96c
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692940"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="75e5e-103">Udvidelsen Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="75e5e-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="75e5e-104">Med tjenesten Envestnet Yodlee Bank Feeds kan du knytte systembankkontoen til din onlinebankkonto for hurtigt at afstemme indbetalinger til bankkonti.</span><span class="sxs-lookup"><span data-stu-id="75e5e-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="75e5e-105">Det betyder, at det seneste bankkontoudtog automatisk eller manuelt indlæses i udligningskladden, hvilket sikrer, at du altid behandler de seneste betalinger med minimal risiko for fejl.</span><span class="sxs-lookup"><span data-stu-id="75e5e-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="75e5e-106">Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="75e5e-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="75e5e-107">Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i onlineversionen af Business Central.</span><span class="sxs-lookup"><span data-stu-id="75e5e-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="75e5e-108">Hvis du vil bruge denne funktionalitet lokalt, skal du have en cobrand-konto hos Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="75e5e-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="75e5e-109">Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="75e5e-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="75e5e-110">Kun banker, der er hjemmehørende i disse lande, understøttes, selvom bankerne fra andre lande kan blive vist i Envestnet Yodlee Bank Feeds-vinduet til bankvalg i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="75e5e-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75e5e-111">På grund af det nye betalingstjenestedirektiv i Europa (PSD2) kan du efter den 14. september 2019 ikke længere automatisk importere bankkontoudtog fra banker i Storbritannien til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="75e5e-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="75e5e-112">Vi overvejer evt. at tilbyde denne funktion igen i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="75e5e-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="75e5e-113">Envestnet Yodlee Bank Feeds-tjenesten giver følgende fordele:</span><span class="sxs-lookup"><span data-stu-id="75e5e-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="75e5e-114">Fjerner behovet for manuel indtastning.</span><span class="sxs-lookup"><span data-stu-id="75e5e-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="75e5e-115">Forbedrer effektivitet og nøjagtighed, når du udfører en udligning af en betaling.</span><span class="sxs-lookup"><span data-stu-id="75e5e-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="75e5e-116">Understøtter et stort antal banker.</span><span class="sxs-lookup"><span data-stu-id="75e5e-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="75e5e-117">Tillader opdaterede oplysninger om banktransaktioner fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="75e5e-117">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="75e5e-118">Understøtter manuelle samt automatiske bankfeeds.</span><span class="sxs-lookup"><span data-stu-id="75e5e-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="75e5e-119">Gør det muligt at outsource betalingsudligning til en bogholder ved at give adgang til bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="75e5e-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="75e5e-120">Du kan finde flere oplysninger i [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="75e5e-120">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="75e5e-121">Se også</span><span class="sxs-lookup"><span data-stu-id="75e5e-121">See Also</span></span>
<span data-ttu-id="75e5e-122">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="75e5e-122">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="75e5e-123">Udligne betalinger automatisk og afstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="75e5e-123">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="75e5e-124">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="75e5e-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
