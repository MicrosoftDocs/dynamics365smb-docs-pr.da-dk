---
title: Registrere udgifter eller indtægter direkte i Finans | Microsoft Docs
description: Du kan oprette relaterede transaktioner for aktiviteter, der ikke er repræsenteret af et dokument, f.eks. mindre udgifter eller indbetalinger, ved at bogføre kladdelinjer på siden Finanskladde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 84b6c80131662675df1117bcb771aaa0ee9553c1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914310"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="45e69-103">Bogføre transaktioner direkte i finansposterne</span><span class="sxs-lookup"><span data-stu-id="45e69-103">Post Transactions Directly to the General Ledger</span></span>

<span data-ttu-id="45e69-104">Du bruger finanskladder til at bogføre økonomiske transaktioner direkte på finanskonti og andre konti, f.eks. bank-, debitor-, kreditor- og medarbejderkonti.</span><span class="sxs-lookup"><span data-stu-id="45e69-104">You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span>  

<span data-ttu-id="45e69-105">En typisk anvendelse af finanskladden er at bogføre medarbejdernes brug af egne penge under forretningsaktiviteter for senere refusion.</span><span class="sxs-lookup"><span data-stu-id="45e69-105">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="45e69-106">Du kan finde flere oplysninger i [Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="45e69-106">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="45e69-107">Finanskladder bogfører finansposteringer direkte på finanskonti og andre konti, f.eks. bank-, debitor-, kreditor- og medarbejderkonti.</span><span class="sxs-lookup"><span data-stu-id="45e69-107">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="45e69-108">Når du bogfører via en finanskonto, oprettes der altid poster i finanskonti.</span><span class="sxs-lookup"><span data-stu-id="45e69-108">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="45e69-109">Det gælder også, når du bogfører f.eks. en kladdelinje på en debitorkonto, fordi der bogføres en post på en finanskonto for tilgodehavende via en bogføringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="45e69-109">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="45e69-110">Du kan tilpasse din version af en finanskladde ved at oprette et kladdenavn eller en skabelon.</span><span class="sxs-lookup"><span data-stu-id="45e69-110">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="45e69-111">Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="45e69-111">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="45e69-112">I modsætning til poster, der bogføres med dokumenter, som kræver en kreditnotaproces, kan du korrekt tilbageføre poster, der bogføres i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="45e69-112">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="45e69-113">Du kan finde flere oplysninger i [Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="45e69-113">For more information, see [Reverse Journal Postings and Undo Receipts/Shipments](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="45e69-114">Sådan bogføres en transaktion direkte på en finanspostkonto</span><span class="sxs-lookup"><span data-stu-id="45e69-114">To post a transaction directly to a general ledger account</span></span>

1. <span data-ttu-id="45e69-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="45e69-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="45e69-116">Åbn det relevante finanskladdenavn.</span><span class="sxs-lookup"><span data-stu-id="45e69-116">Open the relevant general journal batch.</span></span> <span data-ttu-id="45e69-117">Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="45e69-117">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="45e69-118">Udfyld felterne efter behov på en ny kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="45e69-118">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="45e69-119">Gentag trin 3 for alle separate transaktioner, du vil bogføre.</span><span class="sxs-lookup"><span data-stu-id="45e69-119">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="45e69-120">Hvis du vil angive flere transaktionslinjer over én modkontolinje, f.eks. for én bankkonto, skal du markere afkrydsningsfeltet **Foreslå modkontobeløb** på linjen for kørslen på siden **Finanskladdenavne**.</span><span class="sxs-lookup"><span data-stu-id="45e69-120">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="45e69-121">Feltet **Beløb** på modkontolinjen er forudfyldt automatisk med den værdi, der skal bruges til at afstemme posteringerne.</span><span class="sxs-lookup"><span data-stu-id="45e69-121">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="45e69-122">Vælg handlingen **Bogfør** for at registrere transaktionerne på de angivne konti i Finans.</span><span class="sxs-lookup"><span data-stu-id="45e69-122">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="45e69-123">Se også</span><span class="sxs-lookup"><span data-stu-id="45e69-123">See Also</span></span>

[<span data-ttu-id="45e69-124">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="45e69-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="45e69-125">Registrere og refundere medarbejdernes udgifter</span><span class="sxs-lookup"><span data-stu-id="45e69-125">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="45e69-126">Tilbageføre kladdeposteringer og annullere modtagelser/leverancer</span><span class="sxs-lookup"><span data-stu-id="45e69-126">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="45e69-127">Finans</span><span class="sxs-lookup"><span data-stu-id="45e69-127">Finance</span></span>](finance.md)  
<span data-ttu-id="45e69-128">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="45e69-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
