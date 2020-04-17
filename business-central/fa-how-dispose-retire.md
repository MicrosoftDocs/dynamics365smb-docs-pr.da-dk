---
title: Afhænde eller lade anlæg udgå | Microsoft Docs
description: Når du kasserer, sælger eller lader et anlægsaktiv udgå, skal du bogføre en salgsværdi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 97c21286b640571f374e97a02b7953ce839645c6
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184432"
---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="37406-103">Afhænde eller lade anlægsaktiver udgå</span><span class="sxs-lookup"><span data-stu-id="37406-103">Dispose of or Retire Fixed Assets</span></span>
<span data-ttu-id="37406-104">Når du sælger eller på anden måde afhænder et anlægsaktiv, skal salgsværdien bogføres for at beregne og registrere tab eller vinding.</span><span class="sxs-lookup"><span data-stu-id="37406-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="37406-105">En salgspost skal være den sidste post, der bogføres for et anlæg.</span><span class="sxs-lookup"><span data-stu-id="37406-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="37406-106">I forbindelse med delvist solgte anlægsaktiver, kan du bogføre mere end én salgspost.</span><span class="sxs-lookup"><span data-stu-id="37406-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="37406-107">Det samlede antal bogførte salgsbeløb skal være et kreditbeløb.</span><span class="sxs-lookup"><span data-stu-id="37406-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="37406-108">Hvis du bruger et anlæg som delvis betaling for et andet, skal du registrere både salget af det gamle anlæg og købet (anskaffelsen) af det nye.</span><span class="sxs-lookup"><span data-stu-id="37406-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="37406-109">Du kan finde flere oplysninger i [Anskaffe anlægsaktiver](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="37406-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="37406-110">Sådan bogføres et salg fra anlægskassekladden</span><span class="sxs-lookup"><span data-stu-id="37406-110">To post a disposal from the fixed asset G/L journal</span></span>
1. <span data-ttu-id="37406-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægskasseklader**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="37406-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Asset G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="37406-112">Opret en første kladdelinje, og udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="37406-112">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="37406-113">I feltet **Anlægsbogføringstype** skal du vælge **Salg**.</span><span class="sxs-lookup"><span data-stu-id="37406-113">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="37406-114">Vælg handlingen **Indsæt anlægsmodkonto**.</span><span class="sxs-lookup"><span data-stu-id="37406-114">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="37406-115">Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af salg.</span><span class="sxs-lookup"><span data-stu-id="37406-115">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="37406-116">Trin 4 fungerer kun, hvis du har angivet følgende: På siden **Anlægsbogføringsgruppekort** for bogføringsgruppen for anlægsaktivet indeholder feltet **Salgskonto** finansdebetkontoen, og feltet **Salgsmodkonto** indeholder den finanskonto, hvor du vil bogføre modposter til opskrivning.</span><span class="sxs-lookup"><span data-stu-id="37406-116">Step 4 only works if you have set up the following: On the **FA Posting Group Card** page for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="37406-117">Du kan finde flere oplysninger i [Sådan oprettes anlægsbogføringsgrupper](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="37406-117">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
5. <span data-ttu-id="37406-118">Vælg handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="37406-118">Choose the **Post** action.</span></span>  

<span data-ttu-id="37406-119">Hvis du sælger eller afhænder en del af et anlæg, skal du opdele anlægget, inden du kan registrere salgstransaktionen.</span><span class="sxs-lookup"><span data-stu-id="37406-119">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="37406-120">Du kan finde flere oplysninger i [Overføre, opdele eller kombinere anlægsaktiver](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="37406-120">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="37406-121">Sådan får du vist salgsposter</span><span class="sxs-lookup"><span data-stu-id="37406-121">To view disposal ledger entries</span></span>
<span data-ttu-id="37406-122">Når du sælger eller på anden måde afhænder et anlægsaktiv, skal salgsværdien bogføres i finansregnskabet, når du kan se resultatet.</span><span class="sxs-lookup"><span data-stu-id="37406-122">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="37406-123">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlæg**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="37406-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="37406-124">Vælg det anlægsaktiv, du vil have vist poster for, og vælg derefter handlingen **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="37406-124">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="37406-125">Vælg den afskrivningsprofil, du vil have vist poster for, og vælg derefter handlingen **Poster**.</span><span class="sxs-lookup"><span data-stu-id="37406-125">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="37406-126">Vælg en linje med **Salg** i feltet **Anlægsbogføringskategori**, og vælg derefter handlingen **Naviger**.</span><span class="sxs-lookup"><span data-stu-id="37406-126">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Navigate** action.</span></span>  
5. <span data-ttu-id="37406-127">På siden **Naviger** skal du vælge finanspostlinjen og derefter vælge handlingen **Vis**.</span><span class="sxs-lookup"><span data-stu-id="37406-127">On the **Navigate** page, select the general ledger entry line, and then choose the **Show** action.</span></span>  

<span data-ttu-id="37406-128">Siden **Finansposter** åbnes, og du kan se de poster, som bogføringen af salget har resulteret i.</span><span class="sxs-lookup"><span data-stu-id="37406-128">The **General Ledger Entries** page opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="37406-129">Se også</span><span class="sxs-lookup"><span data-stu-id="37406-129">See Also</span></span>
[<span data-ttu-id="37406-130">Anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="37406-130">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="37406-131">Opsætning af Anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="37406-131">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="37406-132">Finans</span><span class="sxs-lookup"><span data-stu-id="37406-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="37406-133">Introduktion</span><span class="sxs-lookup"><span data-stu-id="37406-133">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="37406-134">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="37406-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
