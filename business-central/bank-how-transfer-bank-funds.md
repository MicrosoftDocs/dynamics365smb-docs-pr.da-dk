---
title: Overføre bankbeløb
description: Du kan overføre beløb fra én bankkonto til en anden, herunder forskellige valutaer, ved at bogføre transaktionen i finanskladden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/29/2021
ms.author: edupont
ms.openlocfilehash: da9c8711751040cecb267a3b2209bad2534b618b
ms.sourcegitcommit: 08ca5798cf3f04fc3ea38fff40c1860196a70adf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2021
ms.locfileid: "5985383"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="86042-103">Overføre bankbeløb</span><span class="sxs-lookup"><span data-stu-id="86042-103">Transfer Bank Funds</span></span>

<span data-ttu-id="86042-104">Undertiden kan du have brug for at overføre et beløb fra én bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] til en anden.</span><span class="sxs-lookup"><span data-stu-id="86042-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="86042-105">Hvis du vil gøre dette, skal du bogføre på en transaktion på siden **Finanskladde**.</span><span class="sxs-lookup"><span data-stu-id="86042-105">To do this, you must post the transaction on the **General Journal** page.</span></span> <span data-ttu-id="86042-106">Opgaven afhænger af, om bankkontiene bruger samme valuta eller forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="86042-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="86042-107">Sådan bogføres overførsler mellem bankkonti med samme valutakode</span><span class="sxs-lookup"><span data-stu-id="86042-107">To post a transfer between bank accounts with the same currency code</span></span>

1. <span data-ttu-id="86042-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="86042-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="86042-109">Udfyld **Bogføringsdato** og **Bilagsnr.** på en kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="86042-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="86042-110">Klik på feltet **Kontotype**, og vælg **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="86042-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="86042-111">I feltet **Kontonr.** skal du vælge den bank, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="86042-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="86042-112">Angiv det beløb, der skal overføres, i feltet **Beløb**.</span><span class="sxs-lookup"><span data-stu-id="86042-112">In the **Amount** field, enter the amount to be transferred.</span></span>

    <span data-ttu-id="86042-113">Derefter skal du angive modkontoen.</span><span class="sxs-lookup"><span data-stu-id="86042-113">Next, you must specify the balancing account.</span></span> <span data-ttu-id="86042-114">Hvis du ikke kan se de relevante felter, skal du vælge handlingen **Vis flere kolonner** for at få vist alle tilgængelige felter.</span><span class="sxs-lookup"><span data-stu-id="86042-114">If you can't see the relevant fields, then choose the **Show More Columns** action to view all available fields.</span></span>
6. <span data-ttu-id="86042-115">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="86042-115">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="86042-116">I feltet **Modkontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="86042-116">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="86042-117">Bogfør journalen.</span><span class="sxs-lookup"><span data-stu-id="86042-117">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="86042-118">Sådan bogføres overførsler mellem bankkonti med forskellige valutakoder</span><span class="sxs-lookup"><span data-stu-id="86042-118">To post a transfer between bank accounts with different currency codes</span></span>

<span data-ttu-id="86042-119">Hvis du vil overføre beløb mellem bankkonti, der bruger forskellige valutaer, skal du bogføre to finanskladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="86042-119">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="86042-120">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **FFinanskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="86042-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="86042-121">Opret to kladdelinjer, og udfyld felterne **Bogføringsdato** og **Bilagsnr.**</span><span class="sxs-lookup"><span data-stu-id="86042-121">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="86042-122">På den første kladdelinje skal du vælge **Bankkonto** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="86042-122">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="86042-123">I feltet **Kontonr.** skal du vælge den bankkonto, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="86042-123">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="86042-124">I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen med eller uden et minustegn.</span><span class="sxs-lookup"><span data-stu-id="86042-124">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="86042-125">Et beløb uden fortegn er debet, og et beløb med et minustegn er kredit.</span><span class="sxs-lookup"><span data-stu-id="86042-125">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>

    > [!NOTE]
    > <span data-ttu-id="86042-126">Nogle virksomheder foretrækker at overføre konti på separate kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="86042-126">Some companies prefer to transfer between accounts on separate journal lines.</span></span> <span data-ttu-id="86042-127">Andre virksomheder foretrækker at bogføre alt på én kladdelinje vha. en modkonto.</span><span class="sxs-lookup"><span data-stu-id="86042-127">Other companies prefer to post everything on one journal line by using a balancing account.</span></span> <span data-ttu-id="86042-128">Kontakt din lokale ekspert, hvis du ikke er sikker på, hvad du skal gøre.</span><span class="sxs-lookup"><span data-stu-id="86042-128">Check with your local expert if you're not sure what to do.</span></span>
    >
    > <span data-ttu-id="86042-129">Hvis virksomheden foretrækker at bruge en modkonto, skal du angive feltet **Modkontotype** til **Bankkonto** og derefter sætte feltet **Modkonto** til den bankkonto, som du vil overføre fondene til.</span><span class="sxs-lookup"><span data-stu-id="86042-129">If your company prefers to use a balancing account, then set the **Bal. Account Type** field to **Bank Account**, and set the **Bal. Account No.** field to the bank account to which you want to transfer the funds.</span></span> <span data-ttu-id="86042-130">Gå derefter til trin 9 eller 10.</span><span class="sxs-lookup"><span data-stu-id="86042-130">Then proceed to step 9 or 10.</span></span>
    >
    > <span data-ttu-id="86042-131">Hvis din virksomhed foretrækker at bruge en separat kladdelinje, skal du gå videre til næste trin.</span><span class="sxs-lookup"><span data-stu-id="86042-131">If your company prefers to use a separate journal line, then move on to the next step.</span></span>
6. <span data-ttu-id="86042-132">På den anden kladdelinje skal du vælge **Bankkonto** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="86042-132">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="86042-133">I feltet **Kontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="86042-133">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="86042-134">I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen med eller uden et minustegn.</span><span class="sxs-lookup"><span data-stu-id="86042-134">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="86042-135">Et beløb uden fortegn er debet, og et beløb med et minustegn er kredit.</span><span class="sxs-lookup"><span data-stu-id="86042-135">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
9. <span data-ttu-id="86042-136">Hvis den anvendte valutakurs i kladden er en anden en kursen på siden **Valutakurser**, skal du oprette en ny linje til kurstab og -gevinster.</span><span class="sxs-lookup"><span data-stu-id="86042-136">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a new journal line for the exchange rate gain or loss.</span></span>  

    1. <span data-ttu-id="86042-137">Indtast **Finanskonto** i feltet **Kontotype**.</span><span class="sxs-lookup"><span data-stu-id="86042-137">Enter **G/L Account** in the **Account Type** field.</span></span>  

    2. <span data-ttu-id="86042-138">Angiv finanskontonummeret for kurstab og -gevinster i feltet **Kontonummer**.</span><span class="sxs-lookup"><span data-stu-id="86042-138">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span>  

    3. <span data-ttu-id="86042-139">Angiv kurstab eller-gevinst i feltet **Beløb** med eller uden et minustegn.</span><span class="sxs-lookup"><span data-stu-id="86042-139">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="86042-140">Et beløb uden fortegn er debet, og et beløb med et minustegn er kredit.</span><span class="sxs-lookup"><span data-stu-id="86042-140">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
10. <span data-ttu-id="86042-141">Bogfør journalen.</span><span class="sxs-lookup"><span data-stu-id="86042-141">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="86042-142">Se også</span><span class="sxs-lookup"><span data-stu-id="86042-142">See Also</span></span>

[<span data-ttu-id="86042-143">Bankkontoafstemning</span><span class="sxs-lookup"><span data-stu-id="86042-143">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="86042-144">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="86042-144">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="86042-145">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="86042-145">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="86042-146">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="86042-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]