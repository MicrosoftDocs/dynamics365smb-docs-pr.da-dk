---
title: Bruge fordelingsnøgler i finanskladder | Microsoft Docs
description: Få at vide, hvordan du kan bruge fordelingsnøgler i kladder.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: aa2e553b28825338dadd758f48c5ff43a0494cf4
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "913821"
---
# <a name="use-allocation-keys-in-general-journals"></a><span data-ttu-id="68248-103">Bruge fordelingsnøgler i finanskladder</span><span class="sxs-lookup"><span data-stu-id="68248-103">Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="68248-104">Du kan allokere en post i en finanskladde til flere forskellige konti, når du bogfører kladden.</span><span class="sxs-lookup"><span data-stu-id="68248-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="68248-105">Allokeringen kan foretages efter antal, procent eller beløb.</span><span class="sxs-lookup"><span data-stu-id="68248-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="68248-106">Sådan konfigureres fordelingsnøgler</span><span class="sxs-lookup"><span data-stu-id="68248-106">To set up allocation keys</span></span>
1. <span data-ttu-id="68248-107">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finansgentagelseskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="68248-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="68248-108">Vælg feltet **Kladdenavn** for at åbne siden **Finanskladdenavne**.</span><span class="sxs-lookup"><span data-stu-id="68248-108">Choose the **Batch Name** field to open the **General Journal Batches** page.</span></span>
3. <span data-ttu-id="68248-109">Du kan ændre fordelinger for et eksisterende navn på listen eller oprette et nyt navn med fordelinger.</span><span class="sxs-lookup"><span data-stu-id="68248-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="68248-110">Du kan oprette en ny kladde ved at vælge handlingen **Ny** og gå til næste trin.</span><span class="sxs-lookup"><span data-stu-id="68248-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="68248-111">Vælg kladden og gå til trin 7, hvis du vil ændre fordelingerne af en eksisterende kladde.</span><span class="sxs-lookup"><span data-stu-id="68248-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="68248-112">Angiv navnet på en ny kladde i feltet **Navn**, f.eks. Rengøring.</span><span class="sxs-lookup"><span data-stu-id="68248-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="68248-113">Angiv en beskrivelse i feltet **Beskrivelse**, f.eks. Kladde til rengøringsudgifter.</span><span class="sxs-lookup"><span data-stu-id="68248-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="68248-114">Når du er færdig, skal du lukke siden.</span><span class="sxs-lookup"><span data-stu-id="68248-114">When you are done, close the page.</span></span> <span data-ttu-id="68248-115">Der åbnes en ny tom gentagelseskladde.</span><span class="sxs-lookup"><span data-stu-id="68248-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="68248-116">Udfyld felterne på linjen.</span><span class="sxs-lookup"><span data-stu-id="68248-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="68248-117">Vælg handlingen **Fordelinger**.</span><span class="sxs-lookup"><span data-stu-id="68248-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="68248-118">Tilføj en linje for hver fordeling.</span><span class="sxs-lookup"><span data-stu-id="68248-118">Add a line for each allocation.</span></span> <span data-ttu-id="68248-119">Du skal udfylde et af følgende felter: **Allokeringspct.**, **Andel i antal** eller **Beløb**.</span><span class="sxs-lookup"><span data-stu-id="68248-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="68248-120">Du skal udfylde feltet **Kontonr.** og desuden felterne for globale dimensioner, hvis du allokerer transaktionen mellem globale dimensioner.</span><span class="sxs-lookup"><span data-stu-id="68248-120">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="68248-121">Hvis du angiver en procent på en linje, beregnes beløbet i feltet **Beløb** automatisk.</span><span class="sxs-lookup"><span data-stu-id="68248-121">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="68248-122">Disse beløb har det modsatte tegn af tegnet fra det totale beløb i feltet **Beløb** i gentagelseskladden.</span><span class="sxs-lookup"><span data-stu-id="68248-122">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="68248-123">Når du har angivet linjerne med fordelinger, skal du vælge **OK** for at gå tilbage til siden **Finansgentagelseskladde**.</span><span class="sxs-lookup"><span data-stu-id="68248-123">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** page.</span></span> <span data-ttu-id="68248-124">Feltet **Fordelt beløb (RV)** udfyldes og svarer til feltet **Beløb**.</span><span class="sxs-lookup"><span data-stu-id="68248-124">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="68248-125">Bogfør journalen.</span><span class="sxs-lookup"><span data-stu-id="68248-125">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="68248-126">Sådan ændres en fordelingsnøgle, der allerede er oprettet</span><span class="sxs-lookup"><span data-stu-id="68248-126">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="68248-127">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finansgentagelseskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="68248-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="68248-128">Vælg kladden med allokeringen på siden **Finansgentagelseskladde**.</span><span class="sxs-lookup"><span data-stu-id="68248-128">On the **Recurring General Journal** page, select the journal with the allocation.</span></span>
3. <span data-ttu-id="68248-129">Vælg linjen med fordelingen og vælg derefter handlingen **Fordelinger**.</span><span class="sxs-lookup"><span data-stu-id="68248-129">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="68248-130">Rediger de relevante felter, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="68248-130">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="68248-131">Se også</span><span class="sxs-lookup"><span data-stu-id="68248-131">See Also</span></span>
[<span data-ttu-id="68248-132">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="68248-132">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="68248-133">Bogføring af dokumenter og kladder</span><span class="sxs-lookup"><span data-stu-id="68248-133">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="68248-134">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="68248-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
