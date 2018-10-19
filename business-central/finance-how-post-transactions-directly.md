---
title: "Registrere udgifter eller indtægter direkte i Finans | Microsoft Docs"
description: "Du kan oprette relaterede transaktioner for aktiviteter, der ikke er repræsenteret af et dokument, f.eks. mindre udgifter eller indbetalinger, ved at bogføre kladdelinjer i vinduet Finanskladde."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6aedfbd1decc7d897c7beb4119f7eacdf5d9c23d
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="63df5-103">Bogføre transaktioner direkte i finansposterne</span><span class="sxs-lookup"><span data-stu-id="63df5-103">Post Transactions Directly to the General Ledger</span></span>

<span data-ttu-id="63df5-104">Du bruger finanskladder til at bogføre økonomiske transaktioner direkte på finanskonti og andre konti, f.eks. bank-, debitor-, kreditor- og medarbejderkonti.</span><span class="sxs-lookup"><span data-stu-id="63df5-104">You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span>  

<span data-ttu-id="63df5-105">En typisk anvendelse af finanskladden er at bogføre medarbejdernes brug af egne penge under forretningsaktiviteter for senere refusion.</span><span class="sxs-lookup"><span data-stu-id="63df5-105">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="63df5-106">Du kan finde flere oplysninger i [Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="63df5-106">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="63df5-107">Finanskladder bogfører finansposteringer direkte på finanskonti og andre konti, f.eks. bank-, debitor-, kreditor- og medarbejderkonti.</span><span class="sxs-lookup"><span data-stu-id="63df5-107">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="63df5-108">Når du bogfører via en finanskonto, oprettes der altid poster i finanskonti.</span><span class="sxs-lookup"><span data-stu-id="63df5-108">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="63df5-109">Det gælder også, når du bogfører f.eks. en kladdelinje på en debitorkonto, fordi der bogføres en post på en finanskonto for tilgodehavende via en bogføringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="63df5-109">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="63df5-110">Du kan tilpasse din version af en finanskladde ved at oprette et kladdenavn eller en skabelon.</span><span class="sxs-lookup"><span data-stu-id="63df5-110">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="63df5-111">Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="63df5-111">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="63df5-112">I modsætning til poster, der bogføres med dokumenter, som kræver en kreditnotaproces, kan du korrekt tilbageføre poster, der bogføres i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="63df5-112">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="63df5-113">Du kan finde flere oplysninger i [Tilbageføre poster](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="63df5-113">For more information, see [Reverse Postings](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="63df5-114">Sådan bogføres en transaktion direkte på en finanspostkonto</span><span class="sxs-lookup"><span data-stu-id="63df5-114">To post a transaction directly to a general ledger account</span></span>

1. <span data-ttu-id="63df5-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="63df5-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="63df5-116">Åbn det relevante finanskladdenavn.</span><span class="sxs-lookup"><span data-stu-id="63df5-116">Open the relevant general journal batch.</span></span> <span data-ttu-id="63df5-117">Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="63df5-117">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="63df5-118">Udfyld felterne efter behov på en ny kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="63df5-118">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!TIP]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="63df5-119">Gentag trin 3 for alle separate transaktioner, du vil bogføre.</span><span class="sxs-lookup"><span data-stu-id="63df5-119">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="63df5-120">Hvis du vil angive flere transaktionslinjer over én modkontolinje, f.eks. for én bankkonto, skal du markere afkrydsningsfeltet **Foreslå modkontobeløb** på linjen for kørslen i vinduet **Finanskladdenavne**.</span><span class="sxs-lookup"><span data-stu-id="63df5-120">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="63df5-121">Feltet **Beløb** på modkontolinjen er forudfyldt automatisk med den værdi, der skal bruges til at afstemme posteringerne.</span><span class="sxs-lookup"><span data-stu-id="63df5-121">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="63df5-122">Vælg handlingen **Bogfør** for at registrere transaktionerne på de angivne konti i Finans.</span><span class="sxs-lookup"><span data-stu-id="63df5-122">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="63df5-123">Se også</span><span class="sxs-lookup"><span data-stu-id="63df5-123">See Also</span></span>

[<span data-ttu-id="63df5-124">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="63df5-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="63df5-125">Registrere og refundere medarbejdernes udgifter</span><span class="sxs-lookup"><span data-stu-id="63df5-125">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="63df5-126">Tilbageføre poster</span><span class="sxs-lookup"><span data-stu-id="63df5-126">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="63df5-127">Finans</span><span class="sxs-lookup"><span data-stu-id="63df5-127">Finance</span></span>](finance.md)  
<span data-ttu-id="63df5-128">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="63df5-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

