---
title: "Fortryde en kladdepostering ved at bogføre en tilbageføringspost | Microsoft Docs"
description: "Hvis du har oprettet en forkert bogføring i finanskladden, kan du bruge funktionen Tilbagefør transaktion til at fortryde bogføringen med et korrekt revisionsspor."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-reverse-journal-posting"></a><span data-ttu-id="cc9a1-103">Sådan tilbageføres en kladdepost</span><span class="sxs-lookup"><span data-stu-id="cc9a1-103">How to: Reverse Journal Posting</span></span>
<span data-ttu-id="cc9a1-104">Hvis du vil tilbageføre en fejlpostering i en kladde, skal du vælge posten og oprette en modpost (poster, der er identiske med den originale post, men med modsat fortegn i beløbsfeltet) med det samme bilagsnummer og den samme bogføringsdato som den oprindelige post.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="cc9a1-105">Når du har tilbageført en post, skal du oprette den korrekte post.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="cc9a1-106">Du kan kun tilbageføre poster, der er bogført fra en finanskladdelinje.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="cc9a1-107">En post kan kun tilbageføres én gang.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="cc9a1-108">Du kan finde flere oplysninger om bogføring fra en finanskladde i [Fremgangsmåde: Bogfør transaktioner direkte i finansposter](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="cc9a1-108">For more information about posting from a general journal, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="cc9a1-109">Du kan tilbageføre poster fra alle **Poster**-vinduer:</span><span class="sxs-lookup"><span data-stu-id="cc9a1-109">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="cc9a1-110">Følgende procedure er baseret på vinduet **Finansposter**.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-110">The following procedure is based on the **General Ledger Entries** window.</span></span>

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="cc9a1-111">Sådan tilbageføres kladdepost på en finanspost</span><span class="sxs-lookup"><span data-stu-id="cc9a1-111">To reverse the journal posting of a general ledger entry</span></span>
1. <span data-ttu-id="cc9a1-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finansposter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="cc9a1-113">Marker den post, du vil tilbageføre, og vælg derefter handlingen **Tilbagefør transaktion**.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-113">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="cc9a1-114">Bemærk, at den skal stamme fra en kladdepost.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-114">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="cc9a1-115">I vinduet **Tilbagefør transaktionsposter** skal du vælge den relevante post og derefter vælge handlingen **Tilbagefør**.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-115">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="cc9a1-116">Vælg knappen **Ja** i bekræftelsesmeddelelsen.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-116">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc9a1-117">Se også</span><span class="sxs-lookup"><span data-stu-id="cc9a1-117">See Also</span></span>
[<span data-ttu-id="cc9a1-118">Fremgangsmåde: Bogføre transaktioner direkte i finansposterne</span><span class="sxs-lookup"><span data-stu-id="cc9a1-118">How to: Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="cc9a1-119">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="cc9a1-119">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="cc9a1-120">Finans</span><span class="sxs-lookup"><span data-stu-id="cc9a1-120">Finance</span></span>](finance.md)  
<span data-ttu-id="cc9a1-121">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cc9a1-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

