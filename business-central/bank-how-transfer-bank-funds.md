---
title: Overføre bankbeløb | Microsoft Docs
description: Du kan overføre beløb fra én bankkonto til en anden, herunder forskellige valutaer, ved at bogføre transaktionen i finanskladden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 69e5f439ee8a02ae553d8b148480b655596e2951
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244166"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="915e8-103">Overføre bankbeløb</span><span class="sxs-lookup"><span data-stu-id="915e8-103">Transfer Bank Funds</span></span>
<span data-ttu-id="915e8-104">Undertiden kan du have brug for at overføre et beløb fra én bankkonto til en anden.</span><span class="sxs-lookup"><span data-stu-id="915e8-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="915e8-105">Hvis du vil gøre dette, skal du bogføre på en transaktion i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="915e8-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="915e8-106">Opgaven afhænger af, om bankkontiene bruger samme valuta eller forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="915e8-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="915e8-107">Sådan bogføres overførsler mellem bankkonti med samme valutakode</span><span class="sxs-lookup"><span data-stu-id="915e8-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="915e8-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kassekladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="915e8-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="915e8-109">Udfyld **Bogføringsdato** og **Bilagsnr.** på en kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="915e8-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="915e8-110">Klik på feltet **Kontotype**, og vælg **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="915e8-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="915e8-111">I feltet **Kontonr.** skal du vælge den bank, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="915e8-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="915e8-112">Angiv det beløb, der skal overføres, i feltet **Beløb**.</span><span class="sxs-lookup"><span data-stu-id="915e8-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="915e8-113">Vælg handlingen **Vis flere kolonner** for at få vist alle tilgængelige felter.</span><span class="sxs-lookup"><span data-stu-id="915e8-113">Choose the **Show More Columns** action to view all available fields.</span></span>
7. <span data-ttu-id="915e8-114">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="915e8-114">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
8. <span data-ttu-id="915e8-115">I feltet **Modkontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="915e8-115">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
9. <span data-ttu-id="915e8-116">Bogfør journalen.</span><span class="sxs-lookup"><span data-stu-id="915e8-116">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="915e8-117">Sådan bogføres overførsler mellem bankkonti med forskellige valutakoder</span><span class="sxs-lookup"><span data-stu-id="915e8-117">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="915e8-118">Hvis du vil overføre beløb mellem bankkonti, der bruger forskellige valutaer, skal du bogføre to finanskladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="915e8-118">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="915e8-119">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kassekladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="915e8-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="915e8-120">Opret to kladdelinjer, og udfyld felterne **Bogføringsdato** og **Bilagsnr.**</span><span class="sxs-lookup"><span data-stu-id="915e8-120">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="915e8-121">På den første kladdelinje skal du vælge **Bankkonto** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="915e8-121">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="915e8-122">I feltet **Kontonr.** skal du vælge den bankkonto, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="915e8-122">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="915e8-123">I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="915e8-123">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="915e8-124">Angiv kreditbeløb med et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="915e8-124">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="915e8-125">Angiv debetbeløb uden et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="915e8-125">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="915e8-126">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="915e8-126">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="915e8-127">I feltet **Modkontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="915e8-127">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="915e8-128">På den anden kladdelinje skal du vælge **Bankkonto** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="915e8-128">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="915e8-129">I feltet **Kontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="915e8-129">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="915e8-130">I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="915e8-130">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="915e8-131">Angiv kreditbeløb med et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="915e8-131">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="915e8-132">Angiv debetbeløb uden et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="915e8-132">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="915e8-133">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="915e8-133">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="915e8-134">I feltet **Modkontonr.** skal du vælge den bankkonto, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="915e8-134">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="915e8-135">Hvis den anvendte valutakurs i kladden er en anden en kursen på siden **Valutakurser**, skal du oprette en tredje linje til kurstab og -gevinster.</span><span class="sxs-lookup"><span data-stu-id="915e8-135">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="915e8-136">Indtast **Finanskonto** i feltet **Kontotype**.</span><span class="sxs-lookup"><span data-stu-id="915e8-136">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="915e8-137">Angiv finanskontonummeret for kurstab og -gevinster i feltet **Kontonummer**.</span><span class="sxs-lookup"><span data-stu-id="915e8-137">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="915e8-138">Angiv kurstab eller -tab i feltet **Beløb** henholdsvis med og uden et minustegn foran kredit og debet.</span><span class="sxs-lookup"><span data-stu-id="915e8-138">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="915e8-139">Bogfør journalen.</span><span class="sxs-lookup"><span data-stu-id="915e8-139">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="915e8-140">Se også</span><span class="sxs-lookup"><span data-stu-id="915e8-140">See Also</span></span>
[<span data-ttu-id="915e8-141">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="915e8-141">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="915e8-142">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="915e8-142">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="915e8-143">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="915e8-143">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="915e8-144">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="915e8-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
