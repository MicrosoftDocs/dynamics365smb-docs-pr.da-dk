---
title: Redigere bogførte salgs- og købsdokumenter | Microsoft Docs
description: Lære mere om de forskellige bogføringsfunktioner til bogføring af købsdokumenter, og hvordan du kan opdatere bogførte dokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 07/30/2019
ms.author: sgroespe
ms.openlocfilehash: 7fe0a8dd125411eb9b642410980a23c243fa7975
ms.sourcegitcommit: f46793abdb3efd8384c10eb7992e076383251f2c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/27/2019
ms.locfileid: "1921989"
---
# <a name="edit-posted-documents"></a><span data-ttu-id="10760-103">Redigere bogførte dokumenter</span><span class="sxs-lookup"><span data-stu-id="10760-103">Edit Posted Documents</span></span>
<span data-ttu-id="10760-104">Nogle gange er det nødvendigt at opdatere et bogført dokument, da oplysninger, der er relevante for dokumentet, er ændret.</span><span class="sxs-lookup"><span data-stu-id="10760-104">Sometimes you have to update a posted document because information that is relevant to the document has changed.</span></span> <span data-ttu-id="10760-105">I et bogført salgsdokument, kan det f. eks. være speditørens pakkesporingsnummer.</span><span class="sxs-lookup"><span data-stu-id="10760-105">On a posted sales document, this can be the shipping agent's package tracking number, for example.</span></span> <span data-ttu-id="10760-106">I et bogført købsdokument kan det være en betalingsreferencetekst.</span><span class="sxs-lookup"><span data-stu-id="10760-106">On a posted purchase document, this can be a payment reference text.</span></span>

<span data-ttu-id="10760-107">Du foretager ændringen i en redigerbar version af originaldokumentet, der er angivet med "**- Opdater**" i sidetitlen.</span><span class="sxs-lookup"><span data-stu-id="10760-107">You perform the change on an editable version of the original document, indicated by "**- Update**" in the page title.</span></span> <span data-ttu-id="10760-108">Siden indeholder et delsæt af felterne i det oprindelige dokument, hvoraf nogle er ikke-redigerbare felter, der kun vises til orientering.</span><span class="sxs-lookup"><span data-stu-id="10760-108">The page contains a subset of the fields on the original document, of which some are non-editable fields that are shown for information only.</span></span>

<span data-ttu-id="10760-109">Denne funktion er tilgængelig for følgende dokumenter i alle landeversioner:</span><span class="sxs-lookup"><span data-stu-id="10760-109">The functionality is available for the following documents in all country versions:</span></span>
- <span data-ttu-id="10760-110">Bogført salgsleverance</span><span class="sxs-lookup"><span data-stu-id="10760-110">Posted Sales Shipment</span></span>
- <span data-ttu-id="10760-111">Bogført købsfaktura</span><span class="sxs-lookup"><span data-stu-id="10760-111">Posted Purchase Invoice</span></span>
- <span data-ttu-id="10760-112">Bogført returvareleverance</span><span class="sxs-lookup"><span data-stu-id="10760-112">Posted Return Shipment</span></span>
- <span data-ttu-id="10760-113">Bogført returvaremodtagelse</span><span class="sxs-lookup"><span data-stu-id="10760-113">Posted Return Receipt</span></span>

<span data-ttu-id="10760-114">Følgende yderligere dokumenter kan redigeres i de valgte landeversioner:</span><span class="sxs-lookup"><span data-stu-id="10760-114">The following additional documents can be edited in selected country versions:</span></span>
- <span data-ttu-id="10760-115">ES: bogført salgsfaktura, bogført salgskreditnota, bogført købskreditnota</span><span class="sxs-lookup"><span data-stu-id="10760-115">ES: Posted Sales Invoice, Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="10760-116">APAC: bogført salgskreditnota, bogført købskreditnota</span><span class="sxs-lookup"><span data-stu-id="10760-116">APAC: Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="10760-117">RU: bogført salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="10760-117">RU: Posted Sales Credit Memo</span></span>
- <span data-ttu-id="10760-118">IT: Bogført overflytningsleverance, bogført serviceleverance</span><span class="sxs-lookup"><span data-stu-id="10760-118">IT: Posted Transfer Shipment, Posted Service Shipment</span></span>

## <a name="to-edit-a-posted-sales-shipment"></a><span data-ttu-id="10760-119">Sådan redigeres en bogført salgsleverance</span><span class="sxs-lookup"><span data-stu-id="10760-119">To edit a posted sales shipment</span></span>
<span data-ttu-id="10760-120">I det følgende forklares det, hvordan du kan redigere en bogført salgsleverance.</span><span class="sxs-lookup"><span data-stu-id="10760-120">The following explains how to edit a posted sales shipment.</span></span> <span data-ttu-id="10760-121">Fremgangsmåden er den samme for de andre understøttede dokumenter.</span><span class="sxs-lookup"><span data-stu-id="10760-121">The steps are similar for the other supported documents.</span></span>

1. <span data-ttu-id="10760-122">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte salgsleverancer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="10760-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Shipments**, and then choose the related link.</span></span>
2. <span data-ttu-id="10760-123">Vælg det dokument, som du vil redigere, og vælg derefter handlingen **Opdater dokument**.</span><span class="sxs-lookup"><span data-stu-id="10760-123">Select the document that you want to edit, and then choose the **Update Document** action.</span></span> <span data-ttu-id="10760-124">Du kan også åbne dokumentet og derefter vælge handlingen.</span><span class="sxs-lookup"><span data-stu-id="10760-124">Alternatively, open the document and then choose the action.</span></span>
3. <span data-ttu-id="10760-125">På siden **Bogført salgsleverance - Opdater** skal du f.eks. redigere feltet **Pakkesporingsnr.**</span><span class="sxs-lookup"><span data-stu-id="10760-125">On the **Posted Sales Shipment - Update** page, edit the **Package Tracking No.**</span></span> <span data-ttu-id="10760-126">.</span><span class="sxs-lookup"><span data-stu-id="10760-126">field, for example.</span></span>
4. <span data-ttu-id="10760-127">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="10760-127">Choose the **OK** button.</span></span>

<span data-ttu-id="10760-128">Den bogførte salgsleverance opdateres.</span><span class="sxs-lookup"><span data-stu-id="10760-128">The posted sales shipment is updated.</span></span>

## <a name="see-also"></a><span data-ttu-id="10760-129">Se også</span><span class="sxs-lookup"><span data-stu-id="10760-129">See Also</span></span>
[<span data-ttu-id="10760-130">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="10760-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
[<span data-ttu-id="10760-131">Køb</span><span class="sxs-lookup"><span data-stu-id="10760-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="10760-132">Bogføring af dokumenter og kladder</span><span class="sxs-lookup"><span data-stu-id="10760-132">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="10760-133">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="10760-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
