---
title: Betalingsudligning med Envestnet Yodlee Bank Feeds-udvidelsen
description: Beskriver udvidelsen Envestnet Yodlee Bank Feeds, der sammenkæder med bankkonti, så du hurtigt kan afstemme betalinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d8a04218e44c4a40d96f5e84677434c51f6ef5f3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757388"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="94fcb-103">Udvidelsen Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="94fcb-103">The Envestnet Yodlee Bank Feeds Extension</span></span>

<span data-ttu-id="94fcb-104">Med tjenesten Envestnet Yodlee Bank Feeds kan du knytte systembankkontoen til din onlinebankkonto for hurtigt at afstemme indbetalinger til bankkonti.</span><span class="sxs-lookup"><span data-stu-id="94fcb-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="94fcb-105">Det betyder, at det seneste bankkontoudtog automatisk eller manuelt indlæses i udligningskladden, hvilket sikrer, at du altid behandler de seneste betalinger med minimal risiko for fejl.</span><span class="sxs-lookup"><span data-stu-id="94fcb-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="94fcb-106">Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="94fcb-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="94fcb-107">Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i onlineversionen af Business Central.</span><span class="sxs-lookup"><span data-stu-id="94fcb-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="94fcb-108">Hvis du vil bruge denne funktionalitet lokalt, skal du have en cobrand-konto hos Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="94fcb-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="94fcb-109">Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="94fcb-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="94fcb-110">Kun banker, der er hjemmehørende i disse lande/områder, understøttes, selvom bankerne fra andre lande/områder kan blive vist i Envestnet Yodlee Bank Feeds-vinduet til bankvalg i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="94fcb-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94fcb-111">På grund af det nye betalingstjenestedirektiv i Europa (PSD2) kan du efter den 14. september 2019 ikke længere automatisk importere bankkontoudtog fra banker i Storbritannien til [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="94fcb-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="94fcb-112">Vi overvejer evt. at tilbyde denne funktion igen i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="94fcb-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="94fcb-113">Envestnet Yodlee Bank Feeds-tjenesten giver følgende fordele:</span><span class="sxs-lookup"><span data-stu-id="94fcb-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="94fcb-114">Fjerner behovet for manuel indtastning.</span><span class="sxs-lookup"><span data-stu-id="94fcb-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="94fcb-115">Forbedrer effektivitet og nøjagtighed, når du udfører en udligning af en betaling.</span><span class="sxs-lookup"><span data-stu-id="94fcb-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="94fcb-116">Understøtter et stort antal banker.</span><span class="sxs-lookup"><span data-stu-id="94fcb-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="94fcb-117">Tillader opdaterede oplysninger om banktransaktioner fra [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="94fcb-117">Allows up-to-date information about bank transactions from within [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
* <span data-ttu-id="94fcb-118">Understøtter manuelle samt automatiske bankfeeds.</span><span class="sxs-lookup"><span data-stu-id="94fcb-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="94fcb-119">Gør det muligt at outsource betalingsudligning til en bogholder ved at give adgang til bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="94fcb-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

## <a name="available-bank-feeds"></a><span data-ttu-id="94fcb-120">Tilgængelige bankfeeds</span><span class="sxs-lookup"><span data-stu-id="94fcb-120">Available Bank Feeds</span></span>
<span data-ttu-id="94fcb-121">Du kan kontrollere, om en bank understøttes ved at konfigurere og oprette forbindelse til tjenesten Envestnet Yodlee Bank Feeds.</span><span class="sxs-lookup"><span data-stu-id="94fcb-121">You can check whether a bank is supported by setting up and connecting to the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="94fcb-122">Banken vises på listen, hvis den understøttes af Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="94fcb-122">The bank will appear on the list if it is supported by Envestnet Yodlee.</span></span>

<span data-ttu-id="94fcb-123">Du kan finde flere oplysninger i [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="94fcb-123">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="94fcb-124">Se også</span><span class="sxs-lookup"><span data-stu-id="94fcb-124">See Also</span></span>
<span data-ttu-id="94fcb-125">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="94fcb-125">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="94fcb-126">Udligne betalinger automatisk og afstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="94fcb-126">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="94fcb-127">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="94fcb-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
