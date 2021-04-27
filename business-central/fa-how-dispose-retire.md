---
title: Afhænde eller lade anlæg udgå | Microsoft Docs
description: Når du kasserer, sælger eller lader et anlægsaktiv udgå, skal du bogføre en salgsværdi.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 041f228a0ea2e34fb9986ebb45e98c1300f02f8d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774026"
---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="96783-103">Afhænde eller lade anlægsaktiver udgå</span><span class="sxs-lookup"><span data-stu-id="96783-103">Dispose of or Retire Fixed Assets</span></span>

<span data-ttu-id="96783-104">Når du sælger eller på anden måde afhænder et anlægsaktiv, skal salgsværdien bogføres for at beregne og registrere tab eller vinding.</span><span class="sxs-lookup"><span data-stu-id="96783-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="96783-105">En salgspost skal være den sidste post, der bogføres for et anlæg.</span><span class="sxs-lookup"><span data-stu-id="96783-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="96783-106">I forbindelse med delvist solgte anlægsaktiver, kan du bogføre mere end én salgspost.</span><span class="sxs-lookup"><span data-stu-id="96783-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="96783-107">Det samlede antal bogførte salgsbeløb skal være et kreditbeløb.</span><span class="sxs-lookup"><span data-stu-id="96783-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="96783-108">Hvis du bruger et anlæg som delvis betaling for et andet, skal du registrere både salget af det gamle anlæg og købet (anskaffelsen) af det nye.</span><span class="sxs-lookup"><span data-stu-id="96783-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="96783-109">Du kan finde flere oplysninger i [Anskaffe anlægsaktiver](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="96783-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

<span data-ttu-id="96783-110">I følgende trin antages det, at du allerede har oprettet de relevante bogføringsgrupper på siden **Anlægsbogføringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="96783-110">The following steps assume that you have already set up the relevant posting groups in the **FA Posting Groups** page.</span></span> <span data-ttu-id="96783-111">Du kan finde flere oplysninger i [Sådan oprettes anlægsbogføringsgrupper](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="96783-111">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="96783-112">Sådan bogføres et salg fra anlægskassekladden</span><span class="sxs-lookup"><span data-stu-id="96783-112">To post a disposal from the fixed asset G/L journal</span></span>

1. <span data-ttu-id="96783-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægskasseklader**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="96783-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Asset G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="96783-114">Opret en første kladdelinje, og udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="96783-114">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="96783-115">I feltet **Anlægsbogføringstype** skal du vælge **Salg**.</span><span class="sxs-lookup"><span data-stu-id="96783-115">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="96783-116">Vælg handlingen **Indsæt anlægsmodkonto**.</span><span class="sxs-lookup"><span data-stu-id="96783-116">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="96783-117">Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af salg.</span><span class="sxs-lookup"><span data-stu-id="96783-117">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="96783-118">Trin 4 fungerer kun, hvis du har angivet følgende: På siden **Anlægsbogføringsgruppekort** for bogføringsgruppen for anlægsaktivet indeholder feltet **Salgskonto** finansdebetkontoen, og feltet **Salgsmodkonto** indeholder den finanskonto, hvor du vil bogføre modposter til opskrivning.</span><span class="sxs-lookup"><span data-stu-id="96783-118">Step 4 only works if you have set up the following: On the **FA Posting Group Card** page for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="96783-119">Du kan finde flere oplysninger i [Sådan oprettes anlægsbogføringsgrupper](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="96783-119">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
5. <span data-ttu-id="96783-120">Vælg handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="96783-120">Choose the **Post** action.</span></span>  

<span data-ttu-id="96783-121">Hvis du sælger eller afhænder en del af et anlæg, skal du opdele anlægget, inden du kan registrere salgstransaktionen.</span><span class="sxs-lookup"><span data-stu-id="96783-121">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="96783-122">Du kan finde flere oplysninger i [Overføre, opdele eller kombinere anlægsaktiver](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="96783-122">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="96783-123">Sådan får du vist salgsposter</span><span class="sxs-lookup"><span data-stu-id="96783-123">To view disposal ledger entries</span></span>
<span data-ttu-id="96783-124">Når du sælger eller på anden måde afhænder et anlægsaktiv, skal salgsværdien bogføres i finansregnskabet, når du kan se resultatet.</span><span class="sxs-lookup"><span data-stu-id="96783-124">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="96783-125">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlæg**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="96783-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="96783-126">Vælg det anlægsaktiv, du vil have vist poster for, og vælg derefter handlingen **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="96783-126">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="96783-127">Vælg den afskrivningsprofil, du vil have vist poster for, og vælg derefter handlingen **Poster**.</span><span class="sxs-lookup"><span data-stu-id="96783-127">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="96783-128">Vælg en linje med **Salg** i feltet **Anlægsbogføringskategori**, og vælg derefter handlingen **Find poster**.</span><span class="sxs-lookup"><span data-stu-id="96783-128">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Find Entries** action.</span></span>  
5. <span data-ttu-id="96783-129">På siden **Find poster** skal du vælge finanspostlinjen og derefter vælge handlingen **Vis relaterede poster**.</span><span class="sxs-lookup"><span data-stu-id="96783-129">On the **Find Entries** page, select the general ledger entry line, and then choose the **Show Related Entries** action.</span></span>  

<span data-ttu-id="96783-130">Siden **Finansposter** åbnes, og du kan se de poster, som bogføringen af salget har resulteret i.</span><span class="sxs-lookup"><span data-stu-id="96783-130">The **General Ledger Entries** page opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="96783-131">Se også</span><span class="sxs-lookup"><span data-stu-id="96783-131">See Also</span></span>

[<span data-ttu-id="96783-132">Anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="96783-132">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="96783-133">Opsætning af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="96783-133">Setting Up Fixed Assets</span></span>](fa-setup.md)  
<span data-ttu-id="96783-134">[Sådan oprettes anlægsbogføringsgrupper](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="96783-134">[To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
[<span data-ttu-id="96783-135">Finans</span><span class="sxs-lookup"><span data-stu-id="96783-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="96783-136">Blive køreklar</span><span class="sxs-lookup"><span data-stu-id="96783-136">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="96783-137">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="96783-137">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="96783-138">Find poster</span><span class="sxs-lookup"><span data-stu-id="96783-138">Find Entries</span></span>](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]