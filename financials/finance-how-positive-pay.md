---
title: Eksportere Positive Pay-filer | Microsoft Docs
description: "Du kan sikre dig, at din bank kun afregner validerede checks og beløb, ved at eksportere en Positive Pay-fil, der indeholder kreditor- og betalingsoplysninger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: dfae1975a78c9380b5b6d4086569d63fe3793832
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-export-a-positive-pay-file"></a><span data-ttu-id="f522b-103">Fremgangsmåde: Eksportere en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="f522b-103">How to: Export a Positive Pay file</span></span>
<span data-ttu-id="f522b-104">Du kan sikre dig, at din bank kun afregner validerede checks og beløb, ved at eksportere en Positive Pay-fil, der indeholder relevante betalingsoplysninger, checknummer og betalingsbeløb, som du sender til banken som reference, når du behandler betalinger.</span><span class="sxs-lookup"><span data-stu-id="f522b-104">To make sure that your bank only clears validated checks and amounts, you can export a Positive Pay file that contains vendor information, check number, and payment amount, which you send to the bank for reference when you process payments.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f522b-105"> er konfigureret til at understøtte Positive Pay-filer for Bank of America og City Bank.</span><span class="sxs-lookup"><span data-stu-id="f522b-105"> is preconfigured to support Positive Pay files for Bank of America and City Bank.</span></span>

## <a name="to-set-up-a-bank-account-for-positive-pay"></a><span data-ttu-id="f522b-106">Sådan konfigureres en bankkonto til Positive Pay</span><span class="sxs-lookup"><span data-stu-id="f522b-106">To set up a bank account for Positive Pay</span></span>
1. <span data-ttu-id="f522b-107">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f522b-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="f522b-108">Åbn kortet for den bank, som du vil bruge Positive Pay til.</span><span class="sxs-lookup"><span data-stu-id="f522b-108">Open the card for the bank that you want to use Positive Pay for.</span></span>
3. <span data-ttu-id="f522b-109">I feltet **Eksportkode for Positive Pay** skal du angive POSPAYBANK.</span><span class="sxs-lookup"><span data-stu-id="f522b-109">In the **Positive Pay Export Code** field, enter POSPAYBANK.</span></span>
4. <span data-ttu-id="f522b-110">Luk vinduet.</span><span class="sxs-lookup"><span data-stu-id="f522b-110">Close the window.</span></span>

## <a name="to-export-a-positive-pay-file"></a><span data-ttu-id="f522b-111">Sådan eksporteres en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="f522b-111">To export a Positive Pay file</span></span>
1. <span data-ttu-id="f522b-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f522b-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="f522b-113">Vælg den bankkonto, du vil eksportere en Positive Pay-fil for.</span><span class="sxs-lookup"><span data-stu-id="f522b-113">Select the bank account that you want to export a Positive Pay file for.</span></span>
3. <span data-ttu-id="f522b-114">Vælg handlingen **Eksport af Positive Pay-betalingsposter**.</span><span class="sxs-lookup"><span data-stu-id="f522b-114">Choose **Positive Pay Export** action.</span></span>

    <span data-ttu-id="f522b-115">Vinduet **Eksport af Positive Pay-betalingsposter** åbnes og viser betalinger, der er foretaget for bankkontoen, siden den sidste overførselsdato, som vist i felterne **Sidst uploadet den** og **Sidst uploadet kl.**.</span><span class="sxs-lookup"><span data-stu-id="f522b-115">The **Positive Pay Export** window opens displaying payments that have been made for the bank account since the last upload date, as shown in the **Last Upload Date** and **Last Upload Time** fields.</span></span>
4. <span data-ttu-id="f522b-116">I feltet **Skæringsdato for upload** skal du angiver en dato, før hvilken betalinger ikke inkluderes i den eksporterede fil.</span><span class="sxs-lookup"><span data-stu-id="f522b-116">In the **Cutoff Upload Date** field, specify a date before which payments are not included in the exported file.</span></span>
5. <span data-ttu-id="f522b-117">Vælg handlingen **Eksportér**.</span><span class="sxs-lookup"><span data-stu-id="f522b-117">Choose the **Export** action.</span></span>
6. <span data-ttu-id="f522b-118">I vinduet **Udlæs fil** skal du klikke på knappen **Gem** og derefter gemme filen på et relevant sted.</span><span class="sxs-lookup"><span data-stu-id="f522b-118">In the **Export File** window, choose the **Save** button, and then save the file to a convenient location.</span></span>
7. <span data-ttu-id="f522b-119">Overfør filen til din netbank.</span><span class="sxs-lookup"><span data-stu-id="f522b-119">Upload the file to your electronic bank site.</span></span>
8. <span data-ttu-id="f522b-120">Notér det bekræftelsesnummer, der vises, når filoverførslen er fuldført, og kopiér det.</span><span class="sxs-lookup"><span data-stu-id="f522b-120">Write down or copy the confirmation number that is displayed when the file upload is successful.</span></span>

<span data-ttu-id="f522b-121">Sådan får du vist eksporterede Positive Pay-poster</span><span class="sxs-lookup"><span data-stu-id="f522b-121">To view exported Positive Pay records</span></span>

1. <span data-ttu-id="f522b-122">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f522b-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="f522b-123">Vælg den bankkonto, du vil have vist Positive Pay-eksportposter for.</span><span class="sxs-lookup"><span data-stu-id="f522b-123">Select the bank account that you want to view Positive Pay export records for.</span></span>
3. <span data-ttu-id="f522b-124">Vælg handlingen **Positive Pay-betalingsposter**.</span><span class="sxs-lookup"><span data-stu-id="f522b-124">Choose the **Positive Pay Entries** action.</span></span>

    <span data-ttu-id="f522b-125">I vinduet **Positive Pay-betalingsposter** kan du se alle de eksporterede Positive Pay-poster for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="f522b-125">In the **Positive Pay Entries** window, you can see all the Positive Pay export records for the bank account.</span></span>
4. <span data-ttu-id="f522b-126">I feltet **Bekræftelsesnr.** skal du for hver eksportpost angive bekræftelsesnummeret, der vises, når filen er overført til banken.</span><span class="sxs-lookup"><span data-stu-id="f522b-126">In the **Confirmation Number** field, enter, for each export record, the confirmation number that you receive when the file upload to the bank is successful.</span></span>
5. <span data-ttu-id="f522b-127">For at få vist de relaterede betalingslinjer skal du vælge handlingen **Oplysninger om Positive Pay-betalingspost**.</span><span class="sxs-lookup"><span data-stu-id="f522b-127">To view the related payment lines, choose the **Positive Pay Entry Details** action.</span></span>

<span data-ttu-id="f522b-128">Sådan reeksporteres Positive Pay-filer</span><span class="sxs-lookup"><span data-stu-id="f522b-128">To reexport Positive Pay files</span></span>

1. <span data-ttu-id="f522b-129">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f522b-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="f522b-130">Vælg den bankkonto, du vil reeksportere Positive Pay-filer for.</span><span class="sxs-lookup"><span data-stu-id="f522b-130">Select the bank account that you want to reexport Positive Pay files for.</span></span>
3. <span data-ttu-id="f522b-131">Vælg handlingen **Positive Pay-betalingsposter**.</span><span class="sxs-lookup"><span data-stu-id="f522b-131">Choose the **Positive Pay Entries** action.</span></span>
4. <span data-ttu-id="f522b-132">Vælg den linje for den Positive Pay-eksportfil, som du vil reeksportere.</span><span class="sxs-lookup"><span data-stu-id="f522b-132">Select the line for the Positive Pay export file that you want to reexport.</span></span>
5. <span data-ttu-id="f522b-133">I vinduet **Positive Pay-betalingsposter** skal du vælge handlingen **Reeksportér Positive Pay-betaling til fil**.</span><span class="sxs-lookup"><span data-stu-id="f522b-133">In the **Positive Pay Entries** window, choose the **Reexport Positive Pay to File** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="f522b-134">Se også</span><span class="sxs-lookup"><span data-stu-id="f522b-134">See Also</span></span>
[<span data-ttu-id="f522b-135">Finans</span><span class="sxs-lookup"><span data-stu-id="f522b-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="f522b-136">Konfigurere Finans</span><span class="sxs-lookup"><span data-stu-id="f522b-136">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="f522b-137">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="f522b-137">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="f522b-138">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f522b-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

