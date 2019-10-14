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
ms.openlocfilehash: d79ef7c076ec3a529aeb0c679b8b61658ef65af5
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315344"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="20e63-103">Udvidelsen Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="20e63-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="20e63-104">Med tjenesten Envestnet Yodlee Bank Feeds kan du knytte systembankkontoen til din onlinebankkonto for hurtigt at afstemme indbetalinger til bankkonti.</span><span class="sxs-lookup"><span data-stu-id="20e63-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="20e63-105">Det betyder, at det seneste bankkontoudtog automatisk eller manuelt indlæses i udligningskladden, hvilket sikrer, at du altid behandler de seneste betalinger med minimal risiko for fejl.</span><span class="sxs-lookup"><span data-stu-id="20e63-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="20e63-106">Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="20e63-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="20e63-107">Denne funktionalitet understøttes kun i onlineversionen af Business Central.</span><span class="sxs-lookup"><span data-stu-id="20e63-107">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="20e63-108">Hvis du vil bruge denne funktionalitet lokalt, skal du have en cobrand-konto hos Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="20e63-108">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />

> [!IMPORTANT]
> <span data-ttu-id="20e63-109">På grund af det nye betalingstjenestedirektiv i Europa (PSD2) kan du efter den 14. september 2019 ikke længere automatisk importere bankkontoudtog fra banker i Storbritannien til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="20e63-109">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="20e63-110">Vi overvejer evt. at tilbyde denne funktion igen i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="20e63-110">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="20e63-111">Envestnet Yodlee Bank Feeds-tjenesten giver følgende fordele:</span><span class="sxs-lookup"><span data-stu-id="20e63-111">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="20e63-112">Fjerner behovet for manuel indtastning.</span><span class="sxs-lookup"><span data-stu-id="20e63-112">Removes the need for manual entry.</span></span>
* <span data-ttu-id="20e63-113">Forbedrer effektivitet og nøjagtighed, når du udfører en udligning af en betaling.</span><span class="sxs-lookup"><span data-stu-id="20e63-113">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="20e63-114">Understøtter et stort antal banker.</span><span class="sxs-lookup"><span data-stu-id="20e63-114">Supports a large number of banks.</span></span>
* <span data-ttu-id="20e63-115">Tillader opdaterede oplysninger om banktransaktioner fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="20e63-115">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="20e63-116">Understøtter manuelle samt automatiske bankfeeds.</span><span class="sxs-lookup"><span data-stu-id="20e63-116">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="20e63-117">Gør det muligt at outsource betalingsudligning til en bogholder ved at give adgang til bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="20e63-117">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="20e63-118">Du kan finde flere oplysninger i [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="20e63-118">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="20e63-119">Se også</span><span class="sxs-lookup"><span data-stu-id="20e63-119">See Also</span></span>
<span data-ttu-id="20e63-120">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="20e63-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="20e63-121">Udligne betalinger automatisk og afstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="20e63-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="20e63-122">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="20e63-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
