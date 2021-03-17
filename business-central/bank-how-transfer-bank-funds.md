---
title: Overføre bankbeløb | Microsoft Docs
description: Du kan overføre beløb fra én bankkonto til en anden, herunder forskellige valutaer, ved at bogføre transaktionen i finanskladden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1a0ab7c2a96c278740c07ff243ad785be1d72dd4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388095"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="ec2c7-103">Overføre bankbeløb</span><span class="sxs-lookup"><span data-stu-id="ec2c7-103">Transfer Bank Funds</span></span>
<span data-ttu-id="ec2c7-104">Undertiden kan du have brug for at overføre et beløb fra én bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] til en anden.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="ec2c7-105">Hvis du vil gøre dette, skal du bogføre på en transaktion på siden **Finanskladde**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-105">To do this, you must post the a transaction on the **General Journal** page.</span></span> <span data-ttu-id="ec2c7-106">Opgaven afhænger af, om bankkontiene bruger samme valuta eller forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="ec2c7-107">Sådan bogføres overførsler mellem bankkonti med samme valutakode</span><span class="sxs-lookup"><span data-stu-id="ec2c7-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="ec2c7-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="ec2c7-109">Udfyld **Bogføringsdato** og **Bilagsnr.** på en kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="ec2c7-110">Klik på feltet **Kontotype**, og vælg **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="ec2c7-111">I feltet **Kontonr.** skal du vælge den bank, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="ec2c7-112">Angiv det beløb, der skal overføres, i feltet **Beløb**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="ec2c7-113">Vælg handlingen **Vis flere kolonner** for at få vist alle tilgængelige felter.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-113">Choose the **Show More Columns** action to view all available fields.</span></span>
7. <span data-ttu-id="ec2c7-114">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-114">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
8. <span data-ttu-id="ec2c7-115">I feltet **Modkontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-115">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
9. <span data-ttu-id="ec2c7-116">Bogfør journalen.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-116">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="ec2c7-117">Sådan bogføres overførsler mellem bankkonti med forskellige valutakoder</span><span class="sxs-lookup"><span data-stu-id="ec2c7-117">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="ec2c7-118">Hvis du vil overføre beløb mellem bankkonti, der bruger forskellige valutaer, skal du bogføre to finanskladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-118">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="ec2c7-119">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **FFinanskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="ec2c7-120">Opret to kladdelinjer, og udfyld felterne **Bogføringsdato** og **Bilagsnr.**</span><span class="sxs-lookup"><span data-stu-id="ec2c7-120">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="ec2c7-121">På den første kladdelinje skal du vælge **Bankkonto** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-121">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="ec2c7-122">I feltet **Kontonr.** skal du vælge den bankkonto, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-122">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="ec2c7-123">I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-123">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="ec2c7-124">Angiv kreditbeløb med et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-124">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="ec2c7-125">Angiv debetbeløb uden et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-125">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="ec2c7-126">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-126">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="ec2c7-127">I feltet **Modkontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-127">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="ec2c7-128">På den anden kladdelinje skal du vælge **Bankkonto** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-128">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="ec2c7-129">I feltet **Kontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-129">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="ec2c7-130">I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-130">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="ec2c7-131">Angiv kreditbeløb med et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-131">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="ec2c7-132">Angiv debetbeløb uden et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-132">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="ec2c7-133">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-133">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="ec2c7-134">I feltet **Modkontonr.** skal du vælge den bankkonto, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-134">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="ec2c7-135">Hvis den anvendte valutakurs i kladden er en anden en kursen på siden **Valutakurser**, skal du oprette en tredje linje til kurstab og -gevinster.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-135">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="ec2c7-136">Indtast **Finanskonto** i feltet **Kontotype**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-136">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="ec2c7-137">Angiv finanskontonummeret for kurstab og -gevinster i feltet **Kontonummer**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-137">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="ec2c7-138">Angiv kurstab eller -tab i feltet **Beløb** henholdsvis med og uden et minustegn foran kredit og debet.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-138">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="ec2c7-139">Bogfør journalen.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-139">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec2c7-140">Se også</span><span class="sxs-lookup"><span data-stu-id="ec2c7-140">See Also</span></span>
[<span data-ttu-id="ec2c7-141">Bankkontoafstemning</span><span class="sxs-lookup"><span data-stu-id="ec2c7-141">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="ec2c7-142">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="ec2c7-142">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="ec2c7-143">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="ec2c7-143">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="ec2c7-144">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ec2c7-144">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]