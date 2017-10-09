---
title: "Overføre bankbeløb | Microsoft Docs"
description: "Du kan overføre beløb fra én bankkonto til en anden, herunder forskellige valutaer, ved at bogføre transaktionen i finanskladden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 20661cce60bc9007adb9767388bf5af6f9c3acb9
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-bank-funds"></a><span data-ttu-id="39527-103">Fremgangsmåde: Overføre bankbeløb</span><span class="sxs-lookup"><span data-stu-id="39527-103">How to: Transfer Bank Funds</span></span>
<span data-ttu-id="39527-104">Undertiden kan du have brug for at overføre et beløb fra én bankkonto til en anden.</span><span class="sxs-lookup"><span data-stu-id="39527-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="39527-105">Hvis du vil gøre dette, skal du bogføre på en transaktion i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="39527-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="39527-106">Opgaven afhænger af, om bankkontiene bruger samme valuta eller forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="39527-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="39527-107">Sådan bogføres overførsler mellem bankkonti med samme valutakode</span><span class="sxs-lookup"><span data-stu-id="39527-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="39527-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="39527-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="39527-109">Udfyld **Bogføringsdato** og **Bilagsnr.** på en kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="39527-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="39527-110">Klik på feltet **Kontotype**, og vælg **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="39527-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="39527-111">I feltet **Kontonr.** skal du vælge den bank, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="39527-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="39527-112">Angiv det beløb, der skal overføres, i feltet **Beløb**.</span><span class="sxs-lookup"><span data-stu-id="39527-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="39527-113">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="39527-113">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="39527-114">I feltet **Modkontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="39527-114">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="39527-115">Bogfør journalen.</span><span class="sxs-lookup"><span data-stu-id="39527-115">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="39527-116">Sådan bogføres overførsler mellem bankkonti med forskellige valutakoder</span><span class="sxs-lookup"><span data-stu-id="39527-116">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="39527-117">Hvis du vil overføre beløb mellem bankkonti, der bruger forskellige valutaer, skal du bogføre to finanskladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="39527-117">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="39527-118">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="39527-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="39527-119">Opret to kladdelinjer, og udfyld felterne **Bogføringsdato** og **Bilagsnr.**</span><span class="sxs-lookup"><span data-stu-id="39527-119">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="39527-120">På den første kladdelinje skal du vælge **Bankkonto** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="39527-120">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="39527-121">I feltet **Kontonr.** skal du vælge den bankkonto, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="39527-121">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="39527-122">I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="39527-122">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="39527-123">Angiv kreditbeløb med et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="39527-123">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="39527-124">Angiv debetbeløb uden et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="39527-124">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="39527-125">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="39527-125">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="39527-126">I feltet **Modkontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="39527-126">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="39527-127">På den anden kladdelinje skal du vælge **Bankkonto** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="39527-127">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="39527-128">I feltet **Kontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="39527-128">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="39527-129">I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="39527-129">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="39527-130">Angiv kreditbeløb med et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="39527-130">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="39527-131">Angiv debetbeløb uden et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="39527-131">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="39527-132">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="39527-132">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="39527-133">I feltet **Modkontonr.** skal du vælge den bankkonto, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="39527-133">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="39527-134">Hvis den anvendte valutakurs i kladden er en anden en kursen i vinduet **Valutakurser**, skal du oprette en tredje linje til kurstab og -gevinster.</span><span class="sxs-lookup"><span data-stu-id="39527-134">If the exchange rates used in the journal are different than the exchange rates in the **Currency Exchange Rates** window, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="39527-135">Indtast **Finanskonto** i feltet **Kontotype**.</span><span class="sxs-lookup"><span data-stu-id="39527-135">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="39527-136">Angiv finanskontonummeret for kurstab og -gevinster i feltet **Kontonummer**.</span><span class="sxs-lookup"><span data-stu-id="39527-136">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="39527-137">Angiv kurstab eller -tab i feltet **Beløb** henholdsvis med og uden et minustegn foran kredit og debet.</span><span class="sxs-lookup"><span data-stu-id="39527-137">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="39527-138">Bogfør journalen.</span><span class="sxs-lookup"><span data-stu-id="39527-138">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="39527-139">Se også</span><span class="sxs-lookup"><span data-stu-id="39527-139">See Also</span></span>
[<span data-ttu-id="39527-140">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="39527-140">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="39527-141">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="39527-141">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="39527-142">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="39527-142">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="39527-143">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="39527-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

