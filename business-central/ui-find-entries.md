---
title: Finde poster | Microsoft Docs
description: I denne artikel beskrives det, hvordan du kan se de relaterede dokumenter og poster
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 5f8ddd7176e69c9d1eb3b8d8ff98c93695d50993
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771157"
---
# <a name="finding-related-entries-for-posted-documents"></a><span data-ttu-id="a8d9f-103">Finde relaterede poster for bogførte bilag</span><span class="sxs-lookup"><span data-stu-id="a8d9f-103">Finding Related Entries for Posted Documents</span></span> 

<span data-ttu-id="a8d9f-104">I denne artikel kan du læse, hvordan du finder dokumenter og poster, der er relateret til hinanden, på basis af fælles oplysninger, f.eks.:</span><span class="sxs-lookup"><span data-stu-id="a8d9f-104">In this article, you learn how to find documents and entries that are related to each other based on a common information, like:</span></span>

- <span data-ttu-id="a8d9f-105">Bilagsnummer eller bogføringsdato</span><span class="sxs-lookup"><span data-stu-id="a8d9f-105">Document number or posting date</span></span>
- <span data-ttu-id="a8d9f-106">Forretningskontakttype, nummer eller eksternt bilagsnummer</span><span class="sxs-lookup"><span data-stu-id="a8d9f-106">Business contact type, number, or external document number</span></span>
- <span data-ttu-id="a8d9f-107">Vareserienummer eller lotnummer</span><span class="sxs-lookup"><span data-stu-id="a8d9f-107">Item serial number or lot number</span></span>

<span data-ttu-id="a8d9f-108">Funktionen er især nyttig til at finde finansposter, der er oprettet som resultat af bestemte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-108">This feature is useful for finding the ledger entries that resulted from certain transactions.</span></span> <span data-ttu-id="a8d9f-109">Når du søger efter dokumentnummer, kan du udskrive oversigten fra rapporten Bilagsposter.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-109">When you search by document number, you can print the summary from the Document Entries report.</span></span>

## <a name="get-started"></a><span data-ttu-id="a8d9f-110">Kom i gang</span><span class="sxs-lookup"><span data-stu-id="a8d9f-110">Get started</span></span>

<span data-ttu-id="a8d9f-111">Du kan få adgang til funktionen Find poster på de fleste sider, hvor der vises bogførte dokumenter eller bogførte bilag, for både lister og kort.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-111">The find entries feature is readily available on most pages that display posted documents or posted documents entries - for both lists and cards.</span></span> <span data-ttu-id="a8d9f-112">Det første trin er at åbne en af disse sider.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-112">So the first step is open one of these pages.</span></span> <span data-ttu-id="a8d9f-113">Derefter skal du enten vælge handlingen **Find poster** eller trykke på alt+G-tasterne.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-113">Then, either choose the **Find Entries** action or press the Alt+G keys.</span></span>

<span data-ttu-id="a8d9f-114">Siden **Find poster** indeholder alle relaterede dokumenter og poster, der er baseret på bilagsnr. og bogføringsdato.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-114">The **Find Entries** page  includes all related documents and entries based on the document no. and posting date.</span></span> <span data-ttu-id="a8d9f-115">Siden er inddelt i tre sektioner:</span><span class="sxs-lookup"><span data-stu-id="a8d9f-115">The page is divided into three sections:</span></span>

- <span data-ttu-id="a8d9f-116">Den øverste del viser de felter og handlinger, du kan bruge til at filtrere din søgning.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-116">The top section displays fields and actions that you use for filtering your search.</span></span>
- <span data-ttu-id="a8d9f-117">Den midterste del viser relaterede dokumenter, der er baseret på søgningen.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-117">The middle section displays related documents based on the search.</span></span>
- <span data-ttu-id="a8d9f-118">Den nederste del indeholder oplysninger om kildedokumentet, som blev fundet ved søgning.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-118">The bottom section displays information about the source document that was found by searching.</span></span>


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a><span data-ttu-id="a8d9f-119">Søg efter poster</span><span class="sxs-lookup"><span data-stu-id="a8d9f-119">Search for entries</span></span>

<span data-ttu-id="a8d9f-120">Du kan søge efter poster på grundlag af oplysninger om enten dokument-, forretningskontaktperson- eller var referencen.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-120">You can search for entries based on information about either the document, business contact, or item reference.</span></span> <span data-ttu-id="a8d9f-121">Hvis du vil ændre søgningen, skal du vælge **Handlinger**, **Find efter** og derefter en af følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="a8d9f-121">To change the search, select **Actions**, **Find By**, then one of the following actions:</span></span>

|<span data-ttu-id="a8d9f-122">Handling</span><span class="sxs-lookup"><span data-stu-id="a8d9f-122">Action</span></span>|<span data-ttu-id="a8d9f-123">Description</span><span class="sxs-lookup"><span data-stu-id="a8d9f-123">Description</span></span>|
|------|-----------|
|<span data-ttu-id="a8d9f-124">Søg efter dokument</span><span class="sxs-lookup"><span data-stu-id="a8d9f-124">Find by Document</span></span>|<span data-ttu-id="a8d9f-125">Få vist poster baseret på et bestemt bilagsnummer eller bogføringsdato.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-125">View entries based on a specific document number or posting date.</span></span>|
|<span data-ttu-id="a8d9f-126">Forretningskontakt</span><span class="sxs-lookup"><span data-stu-id="a8d9f-126">Business Contact</span></span> |<span data-ttu-id="a8d9f-127">Få vist poster, der er baseret på en bestemt kontakttype, kontaktnummer, ANR/eller eksternt bilagsnummer.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-127">View entries based on a specific contact type, contact number, anr/or external document number.</span></span> <span data-ttu-id="a8d9f-128">Du kan indtaste de dokumentoplysninger, der er tildelt af en kreditor eller en debitor.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-128">You can enter document information that was assigned by a vendor or a customer.</span></span> <span data-ttu-id="a8d9f-129">Brug de tilgængelige felter til at lede efter kreditorbilag vha. de samme tal som kreditor har givet dokumenterne.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-129">Use the available fields to search for vendor documents by using the numbers that the vendor has assigned the documents.</span></span>|
|<span data-ttu-id="a8d9f-130">Varereference</span><span class="sxs-lookup"><span data-stu-id="a8d9f-130">Item reference</span></span>|<span data-ttu-id="a8d9f-131">Få vist det hele baseret på et serienummer eller lotnummer.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-131">View entires based on a serial number or lot number.</span></span> <span data-ttu-id="a8d9f-132">Du kan angive lotnummer eller serienummer eller filtrere på de serie- eller lotnumre, du vil søge efter.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-132">You can enter the lot number or serial number, or filter on the lot number or serial number that you want to search for.</span></span> <span data-ttu-id="a8d9f-133">Handlingen er nyttig, hvis du vil se, hvor et bestemt varesporingsnummer blev brugt, hvilken leverandør det kom fra, eller hvilken kunde varen med det varenummer blev solgt til.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-133">This action is useful to see where a specific item tracking number was used, what vendor it came from, or what customer it was sold to.</span></span>|

<span data-ttu-id="a8d9f-134">Når du har foretaget en markering, skal du indtaste de relevante søgeoplysninger i felterne øverst.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-134">After you make a selection, enter the relevant search information in the fields at the top.</span></span> <span data-ttu-id="a8d9f-135">Brug værktøjstip i felterne som hjælp.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-135">Use the tooltips on the fields to help.</span></span> <span data-ttu-id="a8d9f-136">Når du er færdig, skal du vælge **Find** for at starte søgningen.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-136">When you're finished, choose **Find** to start the search.</span></span> <span data-ttu-id="a8d9f-137">Hvis du ændrer nogen af filtrene, skal du vælge **Find** igen.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-137">If you change any of the filters, you have to choose **Find** again.</span></span>

> [!TIP]
> <span data-ttu-id="a8d9f-138">Du kan finde et par eksempler på brug af **Find poster** under [Sporing af varesporede elementer](inventory-how-to-trace-item-tracked-items.md) og [Gennemgang: Sporing af serie-/lotnumre](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="a8d9f-138">For a couple examples about using **Find Entries**, see [Trace Item-Tracked Items](inventory-how-to-trace-item-tracked-items.md) and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="a8d9f-139">Se relateret oplæring på [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="a8d9f-139">See Related Training at [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="a8d9f-140">Se også</span><span class="sxs-lookup"><span data-stu-id="a8d9f-140">See Also</span></span>

[<span data-ttu-id="a8d9f-141">Arbejde med Business Central</span><span class="sxs-lookup"><span data-stu-id="a8d9f-141">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="a8d9f-142">Føje en sidehandling til rollecenteret</span><span class="sxs-lookup"><span data-stu-id="a8d9f-142">Add a Page Action to Your Role Center</span></span>](ui-bookmarks.md)  
[<span data-ttu-id="a8d9f-143">Spore vare via varesporing</span><span class="sxs-lookup"><span data-stu-id="a8d9f-143">Trace Item-Tracked Items</span></span>](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]