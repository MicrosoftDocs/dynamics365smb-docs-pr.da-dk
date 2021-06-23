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
ms.openlocfilehash: a29cea15cba15da1bc68816e07f76de59f43958b
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216124"
---
# <a name="finding-related-entries-for-posted-documents"></a><span data-ttu-id="45161-103">Finde relaterede poster for bogførte bilag</span><span class="sxs-lookup"><span data-stu-id="45161-103">Finding Related Entries for Posted Documents</span></span> 

<span data-ttu-id="45161-104">I denne artikel kan du læse, hvordan du finder dokumenter og poster, der er relateret til hinanden, på basis af fælles oplysninger, f.eks.:</span><span class="sxs-lookup"><span data-stu-id="45161-104">In this article, you learn how to find documents and entries that are related to each other based on a common information, like:</span></span>

- <span data-ttu-id="45161-105">Bilagsnummer eller bogføringsdato</span><span class="sxs-lookup"><span data-stu-id="45161-105">Document number or posting date</span></span>
- <span data-ttu-id="45161-106">Forretningskontakttype, nummer eller eksternt bilagsnummer</span><span class="sxs-lookup"><span data-stu-id="45161-106">Business contact type, number, or external document number</span></span>
- <span data-ttu-id="45161-107">Vareserienummer eller lotnummer</span><span class="sxs-lookup"><span data-stu-id="45161-107">Item serial number or lot number</span></span>

<span data-ttu-id="45161-108">Funktionen er især nyttig til at finde finansposter, der er oprettet som resultat af bestemte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="45161-108">This feature is useful for finding the ledger entries that resulted from certain transactions.</span></span> <span data-ttu-id="45161-109">Når du søger efter dokumentnummer, kan du udskrive oversigten fra rapporten Bilagsposter.</span><span class="sxs-lookup"><span data-stu-id="45161-109">When you search by document number, you can print the summary from the Document Entries report.</span></span>

## <a name="get-started"></a><span data-ttu-id="45161-110">Kom i gang</span><span class="sxs-lookup"><span data-stu-id="45161-110">Get started</span></span>

<span data-ttu-id="45161-111">Du kan få adgang til funktionen Find poster på de fleste sider, hvor der vises bogførte dokumenter eller bogførte bilag, for både lister og kort.</span><span class="sxs-lookup"><span data-stu-id="45161-111">The find entries feature is readily available on most pages that display posted documents or posted documents entries - for both lists and cards.</span></span> <span data-ttu-id="45161-112">Det første trin er at åbne en af disse sider.</span><span class="sxs-lookup"><span data-stu-id="45161-112">So the first step is open one of these pages.</span></span> <span data-ttu-id="45161-113">Derefter skal du enten vælge handlingen **Find poster** eller trykke på alt+G-tasterne.</span><span class="sxs-lookup"><span data-stu-id="45161-113">Then, either choose the **Find Entries** action or press the Alt+G keys.</span></span>

<span data-ttu-id="45161-114">Siden **Find poster** indeholder alle relaterede dokumenter og poster, der er baseret på bilagsnr. og bogføringsdato.</span><span class="sxs-lookup"><span data-stu-id="45161-114">The **Find Entries** page  includes all related documents and entries based on the document no. and posting date.</span></span> <span data-ttu-id="45161-115">Siden er inddelt i tre sektioner:</span><span class="sxs-lookup"><span data-stu-id="45161-115">The page is divided into three sections:</span></span>

- <span data-ttu-id="45161-116">Den øverste del viser de felter og handlinger, du kan bruge til at filtrere din søgning.</span><span class="sxs-lookup"><span data-stu-id="45161-116">The top section displays fields and actions that you use for filtering your search.</span></span>
- <span data-ttu-id="45161-117">Den midterste del viser relaterede dokumenter, der er baseret på søgningen.</span><span class="sxs-lookup"><span data-stu-id="45161-117">The middle section displays related documents based on the search.</span></span>
- <span data-ttu-id="45161-118">Den nederste del indeholder oplysninger om kildedokumentet, som blev fundet ved søgning.</span><span class="sxs-lookup"><span data-stu-id="45161-118">The bottom section displays information about the source document that was found by searching.</span></span>


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a><span data-ttu-id="45161-119">Søg efter poster</span><span class="sxs-lookup"><span data-stu-id="45161-119">Search for entries</span></span>

<span data-ttu-id="45161-120">Du kan søge efter poster på grundlag af oplysninger om enten dokument-, forretningskontaktperson- eller var referencen.</span><span class="sxs-lookup"><span data-stu-id="45161-120">You can search for entries based on information about either the document, business contact, or item reference.</span></span> <span data-ttu-id="45161-121">Hvis du vil ændre søgningen, skal du vælge **Handlinger**, **Find efter** og derefter en af følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="45161-121">To change the search, select **Actions**, **Find By**, then one of the following actions:</span></span>

|<span data-ttu-id="45161-122">Handling</span><span class="sxs-lookup"><span data-stu-id="45161-122">Action</span></span>|<span data-ttu-id="45161-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="45161-123">Description</span></span>|
|------|-----------|
|<span data-ttu-id="45161-124">Søg efter dokument</span><span class="sxs-lookup"><span data-stu-id="45161-124">Find by Document</span></span>|<span data-ttu-id="45161-125">Få vist poster baseret på et bestemt bilagsnummer eller bogføringsdato.</span><span class="sxs-lookup"><span data-stu-id="45161-125">View entries based on a specific document number or posting date.</span></span>|
|<span data-ttu-id="45161-126">Forretningskontakt</span><span class="sxs-lookup"><span data-stu-id="45161-126">Business Contact</span></span> |<span data-ttu-id="45161-127">Få vist poster, der er baseret på en bestemt kontakttype, kontaktnummer, ANR/eller eksternt bilagsnummer.</span><span class="sxs-lookup"><span data-stu-id="45161-127">View entries based on a specific contact type, contact number, anr/or external document number.</span></span> <span data-ttu-id="45161-128">Du kan indtaste de dokumentoplysninger, der er tildelt af en kreditor eller en debitor.</span><span class="sxs-lookup"><span data-stu-id="45161-128">You can enter document information that was assigned by a vendor or a customer.</span></span> <span data-ttu-id="45161-129">Brug de tilgængelige felter til at lede efter kreditorbilag vha. de samme tal som kreditor har givet dokumenterne.</span><span class="sxs-lookup"><span data-stu-id="45161-129">Use the available fields to search for vendor documents by using the numbers that the vendor has assigned the documents.</span></span>|
|<span data-ttu-id="45161-130">Varereference</span><span class="sxs-lookup"><span data-stu-id="45161-130">Item reference</span></span>|<span data-ttu-id="45161-131">Få vist det hele baseret på et serienummer eller lotnummer.</span><span class="sxs-lookup"><span data-stu-id="45161-131">View entires based on a serial number or lot number.</span></span> <span data-ttu-id="45161-132">Du kan angive lotnummer eller serienummer eller filtrere på de serie- eller lotnumre, du vil søge efter.</span><span class="sxs-lookup"><span data-stu-id="45161-132">You can enter the lot number or serial number, or filter on the lot number or serial number that you want to search for.</span></span> <span data-ttu-id="45161-133">Handlingen er nyttig, hvis du vil se, hvor et bestemt varesporingsnummer blev brugt, hvilken leverandør det kom fra, eller hvilken kunde varen med det varenummer blev solgt til.</span><span class="sxs-lookup"><span data-stu-id="45161-133">This action is useful to see where a specific item tracking number was used, what vendor it came from, or what customer it was sold to.</span></span>|

<span data-ttu-id="45161-134">Når du har foretaget en markering, skal du indtaste de relevante søgeoplysninger i felterne øverst.</span><span class="sxs-lookup"><span data-stu-id="45161-134">After you make a selection, enter the relevant search information in the fields at the top.</span></span> <span data-ttu-id="45161-135">Brug værktøjstip i felterne som hjælp.</span><span class="sxs-lookup"><span data-stu-id="45161-135">Use the tooltips on the fields to help.</span></span> <span data-ttu-id="45161-136">Når du er færdig, skal du vælge **Find** for at starte søgningen.</span><span class="sxs-lookup"><span data-stu-id="45161-136">When you're finished, choose **Find** to start the search.</span></span> <span data-ttu-id="45161-137">Hvis du ændrer nogen af filtrene, skal du vælge **Find** igen.</span><span class="sxs-lookup"><span data-stu-id="45161-137">If you change any of the filters, you have to choose **Find** again.</span></span>

> [!TIP]
> <span data-ttu-id="45161-138">Du kan se et par eksempler på brug af **Søg poster** under [Sporing af varesporede elementer](inventory-how-to-trace-item-tracked-items.md)</span><span class="sxs-lookup"><span data-stu-id="45161-138">For a couple examples about using **Find Entries**, see [Trace Item-Tracked Items](inventory-how-to-trace-item-tracked-items.md)</span></span> <!--and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md). -->

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="45161-139">Se relateret oplæring på [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="45161-139">See Related Training at [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="45161-140">Se også</span><span class="sxs-lookup"><span data-stu-id="45161-140">See Also</span></span>

[<span data-ttu-id="45161-141">Arbejde med Business Central</span><span class="sxs-lookup"><span data-stu-id="45161-141">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="45161-142">Føje en sidehandling til rollecenteret</span><span class="sxs-lookup"><span data-stu-id="45161-142">Add a Page Action to Your Role Center</span></span>](ui-bookmarks.md)  
[<span data-ttu-id="45161-143">Spore vare via varesporing</span><span class="sxs-lookup"><span data-stu-id="45161-143">Trace Item-Tracked Items</span></span>](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
