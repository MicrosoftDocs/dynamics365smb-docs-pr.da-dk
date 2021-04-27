---
title: Angive et prioritetsniveau for en kreditor | Microsoft Docs
description: Du kan tildele numre til kreditorer eller leverandører for at prioritere dem og lette betalingsforslag i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1604113b255a585532677ccb47d7e68d1cc64059
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772775"
---
# <a name="prioritize-vendors"></a><span data-ttu-id="f6052-103">Tildele kreditorer prioritet</span><span class="sxs-lookup"><span data-stu-id="f6052-103">Prioritize Vendors</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="f6052-104">kan foreslå forskellige betalinger til kreditorer. Det kan f.eks. være betalinger, som snart forfalder, eller som omfatter rabat.</span><span class="sxs-lookup"><span data-stu-id="f6052-104">can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="f6052-105">Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="f6052-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="f6052-106">Du skal først at prioritere dine kreditorer ved at tildele numre til dem.</span><span class="sxs-lookup"><span data-stu-id="f6052-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a><span data-ttu-id="f6052-107">Sådan tildeler du kreditorer prioritet</span><span class="sxs-lookup"><span data-stu-id="f6052-107">To prioritize vendors</span></span>
1. <span data-ttu-id="f6052-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leverandører (Kreditorer)**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f6052-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="f6052-109">Vælg den relevante kreditor, og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="f6052-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="f6052-110">Angiv et nummer i feltet **Prioritet**.</span><span class="sxs-lookup"><span data-stu-id="f6052-110">In the **Priority** field, enter a number.</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="f6052-111">betragter det laveste nummer, bortset fra 0, som den højeste prioritet.</span><span class="sxs-lookup"><span data-stu-id="f6052-111">considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="f6052-112">Bruger du f.eks. 1, 2 og 3, har 1 den højeste prioritet.</span><span class="sxs-lookup"><span data-stu-id="f6052-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="f6052-113">Hvis der er en kreditor, du ikke vil tildele prioritet, skal du lade feltet **Prioritet** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="f6052-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="f6052-114">Hvis du bruger betalingsforslag figurerer den pågældende kreditor i så fald efter alle andre kreditorer, som har et prioritetstal.</span><span class="sxs-lookup"><span data-stu-id="f6052-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="f6052-115">Der er ingen begrænsninger på, hvor mange prioritetsniveauer du kan angive.</span><span class="sxs-lookup"><span data-stu-id="f6052-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6052-116">Se også</span><span class="sxs-lookup"><span data-stu-id="f6052-116">See Also</span></span>
[<span data-ttu-id="f6052-117">Opsætning af indkøb</span><span class="sxs-lookup"><span data-stu-id="f6052-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="f6052-118">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="f6052-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="f6052-119">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f6052-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]