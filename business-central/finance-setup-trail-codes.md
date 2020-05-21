---
title: Definere koder for revisionsspor | Microsoft Docs
description: Få mere at vide om de opgaver, der bruges til at oprette kilde- og årsagskoder, som du kan bruge til at spore revisionsspor.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 05/12/2020
ms.author: edupont
ms.openlocfilehash: eac9b5268cda8671a7189a429dedd9eb3cbfbc53
ms.sourcegitcommit: b9264b4ed650feca18776892ec23f2aa7ec43e20
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2020
ms.locfileid: "3372683"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><span data-ttu-id="f32ac-103">Oprette kilde- og årsagskoder til revisionsspor</span><span class="sxs-lookup"><span data-stu-id="f32ac-103">Setting Up Source Codes and Reason Codes for Audit Trails</span></span>

<span data-ttu-id="f32ac-104">Alle bogførte poster får automatisk tildelt en kildekode, så transaktioner kan spores til deres oprindelse.</span><span class="sxs-lookup"><span data-stu-id="f32ac-104">All posted entries are automatically assigned a source code so that transactions can be traced to their origin.</span></span> <span data-ttu-id="f32ac-105">Hvis du vil knytte en supplerende kildekode til poster, kan du benytte årsagskoder.</span><span class="sxs-lookup"><span data-stu-id="f32ac-105">If you want to give entries a supplementary source code, you can use reason codes.</span></span> <span data-ttu-id="f32ac-106">Årsagskoder kan bruges til at angive, hvorfor en post er oprettet.</span><span class="sxs-lookup"><span data-stu-id="f32ac-106">Reason codes are used to indicate why an entry was created.</span></span> <span data-ttu-id="f32ac-107">Når du har angivet årsagskoder, kan du tildele dem til hele anlægskladdetyper og kladder, og derefter kan du tildele dem til individuelle kladdelinjer og dokumenter.</span><span class="sxs-lookup"><span data-stu-id="f32ac-107">When you set up reason codes, you can assign them to entire journal templates and journal batches, and you can assign them to individual journal lines and documents.</span></span>  

<span data-ttu-id="f32ac-108">Brug koder, der er lette at huske, og som er beskrivende, til både kilde- og årsagskoder.</span><span class="sxs-lookup"><span data-stu-id="f32ac-108">For both source codes and reason codes, use codes that are easy to remember and descriptive.</span></span> <span data-ttu-id="f32ac-109">Koden skal være entydig, og du kan oprette et ubegrænset antal koder.</span><span class="sxs-lookup"><span data-stu-id="f32ac-109">The code must be unique, and you can set up as many codes as you like.</span></span>

## <a name="define-source-codes"></a><span data-ttu-id="f32ac-110">Definere kildekoder</span><span class="sxs-lookup"><span data-stu-id="f32ac-110">Define source codes</span></span>

<span data-ttu-id="f32ac-111">Det kan være nyttigt at se, hvordan en bestemt post blev oprettet, f.eks. om posten blev oprettet ved bogføring af en finanskladde eller af en købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="f32ac-111">Sometimes, you want see how a particular entry arose, such as whether it came from posting a general journal or a purchase invoice.</span></span> <span data-ttu-id="f32ac-112">En kildekode angiver, hvor en post er oprettet.</span><span class="sxs-lookup"><span data-stu-id="f32ac-112">A source code indicates where an entry was created.</span></span> <span data-ttu-id="f32ac-113">Der oprettes poster, når kladder og fakturaer bogføres, og når visse kørsler udføres.</span><span class="sxs-lookup"><span data-stu-id="f32ac-113">Entries are created when journals and invoices are posted and when certain batch jobs are executed.</span></span> <span data-ttu-id="f32ac-114">Hver bogføringstype har en bestemt kildekode, der tilknyttes, når der oprettes individuelle poster.</span><span class="sxs-lookup"><span data-stu-id="f32ac-114">Each posting type has a specific source code that is assigned when individual entries are created.</span></span>  

<span data-ttu-id="f32ac-115">Når kladder, ordrer, fakturaer eller kreditnotaer bogføres, og når forskellige kørsler udføres, oprettes der poster i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="f32ac-115">Posting journals, orders, invoices, or credit memos, and running various batch jobs, creates entries in the financial statements.</span></span> <span data-ttu-id="f32ac-116">Siden **Kildekodedefinition** indeholder adskillige oversigtspaneler med en for hvert modul.</span><span class="sxs-lookup"><span data-stu-id="f32ac-116">The **Source Code Setup** page contains several FastTabs, one for each application area.</span></span> <span data-ttu-id="f32ac-117">Hvert oversigtspanel indeholder kildekoder, der kan anvendes til det pågældende område.</span><span class="sxs-lookup"><span data-stu-id="f32ac-117">Each FastTab contains the source codes that are applicable for that application area.</span></span>

<span data-ttu-id="f32ac-118">Når du bogfører eller udfører en kørsel, knyttes den korrekte kildekode automatisk til posten.</span><span class="sxs-lookup"><span data-stu-id="f32ac-118">When you post or run a batch job, the correct source code is automatically attached to the entry.</span></span> <span data-ttu-id="f32ac-119">Det vil sige, at når du f.eks. bogfører fra kassekladden, får posten koden *KASSEKLD*.</span><span class="sxs-lookup"><span data-stu-id="f32ac-119">For example, when you post from the general journal, the entry is coded as *GENJNL*.</span></span> <span data-ttu-id="f32ac-120">Herefter kan du filtrere siden **Finansposter** for at se, hvilke poster der er bogført fra finanskladden eller fra salgsdokumenter, f. eks.</span><span class="sxs-lookup"><span data-stu-id="f32ac-120">You can then filter the **General Ledger Entries** page to show which entries were posted from the general journal or from sales documents, for example</span></span>

### <a name="to-define-source-codes"></a><span data-ttu-id="f32ac-121">Sådan defineres kildekoder</span><span class="sxs-lookup"><span data-stu-id="f32ac-121">To define source codes</span></span>

1. <span data-ttu-id="f32ac-122">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kildekodedefinition**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f32ac-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Code Setup**, and then choose the related link.</span></span>  

2. <span data-ttu-id="f32ac-123">Angiv den relevante kildekode for hver bogføringstype og kørsel i vinduet **Kildekodedefinition**.</span><span class="sxs-lookup"><span data-stu-id="f32ac-123">In the **Source Code Setup** window, for each each posting type and batch job, specify the relevant source code.</span></span>  

<span data-ttu-id="f32ac-124">Du kan ændre indholdet i et felt senere. Herefter vil ændringerne påvirke fremtidige bogføringer.</span><span class="sxs-lookup"><span data-stu-id="f32ac-124">You can change the contents of a field later, and that change will then impact future postings.</span></span>

## <a name="change-source-codes"></a><span data-ttu-id="f32ac-125">Ændre kildekoder</span><span class="sxs-lookup"><span data-stu-id="f32ac-125">Change source codes</span></span>

<span data-ttu-id="f32ac-126">Det kan være en fordel at ændre en kildekode.</span><span class="sxs-lookup"><span data-stu-id="f32ac-126">You may want to change a source code.</span></span> <span data-ttu-id="f32ac-127">Lad os sige, at du vil ændre kildekoden *KASSEKLD* til *GNJ*.</span><span class="sxs-lookup"><span data-stu-id="f32ac-127">For example, you want to change the source code *GENJNL* to *GNJ*.</span></span>

### <a name="to-change-source-codes"></a><span data-ttu-id="f32ac-128">Sådan ændres kildekoder</span><span class="sxs-lookup"><span data-stu-id="f32ac-128">To change source codes</span></span>

1. <span data-ttu-id="f32ac-129">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kildekoder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f32ac-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="f32ac-130">Vælg den kode, der skal ændres, på den pågældende linje i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="f32ac-130">On the line with the code to be changed, select the code in the **Code** field.</span></span>

3. <span data-ttu-id="f32ac-131">Indtast den nye kode, og tryk derefter på knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f32ac-131">Enter the new code, and then choose the **Yes** button.</span></span> <span data-ttu-id="f32ac-132">Du kan også ændre indholdet i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f32ac-132">You can also change the contents of the **Description** field.</span></span>

<span data-ttu-id="f32ac-133">Alle nye poster, der er bogført fra finanskladden, skal have en ny kildekode.</span><span class="sxs-lookup"><span data-stu-id="f32ac-133">All new entries that are posted from the general journal will have the new source code.</span></span>

## <a name="define-reason-codes"></a><span data-ttu-id="f32ac-134">Definere årsagskoder</span><span class="sxs-lookup"><span data-stu-id="f32ac-134">Define reason codes</span></span>

<span data-ttu-id="f32ac-135">Årsagskoder supplerer kildekoder og bruges til at angive, hvorfor en post er oprettet.</span><span class="sxs-lookup"><span data-stu-id="f32ac-135">Reason codes supplement the source codes and are used to indicate why an entry was created.</span></span> <span data-ttu-id="f32ac-136">Du kan tildele årsagskoder i individuelle poster, og du kan tildele permanente koder i bestemte anlægskladder og kladder.</span><span class="sxs-lookup"><span data-stu-id="f32ac-136">You can assign reason codes on individual entries, and you can assign permanent codes to specific journal templates and journal batches.</span></span> <span data-ttu-id="f32ac-137">Når en årsagskode er knyttet til en kladdelinje eller til købs- og salgshoveder, bliver alle posterne markeret med årsagskoder, når de bogføres.</span><span class="sxs-lookup"><span data-stu-id="f32ac-137">When a reason code is linked to a journal line or a sales or purchase header, all entries are marked with the reason code when they are posted.</span></span>  

### <a name="to-set-up-reason-codes"></a><span data-ttu-id="f32ac-138">Sådan oprettes årsagskoder</span><span class="sxs-lookup"><span data-stu-id="f32ac-138">To set up reason codes</span></span>

1. <span data-ttu-id="f32ac-139">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Årsagskoder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f32ac-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **Reason Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="f32ac-140">I vinduet **Årsagskoder** skal du indtaste den første kode i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="f32ac-140">In the **Reason Codes** window, enter the first code in the **Code** field.</span></span> <span data-ttu-id="f32ac-141">Angiv en beskrivende tekst i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f32ac-141">In the **Description** field, enter an explanatory text.</span></span>

<span data-ttu-id="f32ac-142">Gentag denne fremgangsmåde for hver enkelt af de koder, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="f32ac-142">Repeat the procedure for each code you want to use.</span></span> <span data-ttu-id="f32ac-143">Du kan oprette et ubegrænset antal koder.</span><span class="sxs-lookup"><span data-stu-id="f32ac-143">You can set up any number of codes.</span></span>

<span data-ttu-id="f32ac-144">Følgende fremgangsmåde beskriver, hvordan du føjer en årsagskode til en kladdetype, men lignende trin gælder for tilføjelse af en årsagskode til en kladdelinje eller et kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="f32ac-144">The following procedure describes how to add a reason code to a journal template, but similar steps apply to adding a reason code to a journal line or journal batch.</span></span>  

### <a name="to-assign-reason-codes-to-journal-templates"></a><span data-ttu-id="f32ac-145">Sådan knytter du årsagskoder til kladdetyper</span><span class="sxs-lookup"><span data-stu-id="f32ac-145">To assign reason codes to journal templates</span></span>

1. <span data-ttu-id="f32ac-146">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladdetyper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f32ac-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **General Journal Templates**, and then choose the related link.</span></span>

2. <span data-ttu-id="f32ac-147">Angiv den relevante kode i feltet **Årsagskode** på linjen med den valgte kladdetype.</span><span class="sxs-lookup"><span data-stu-id="f32ac-147">On the line with the selected journal template, in the **Reason Code** field, specify the relevant code.</span></span>

3. <span data-ttu-id="f32ac-148">Luk kladdetypen.</span><span class="sxs-lookup"><span data-stu-id="f32ac-148">Close the journal template.</span></span>

<span data-ttu-id="f32ac-149">Den valgte årsagskode kopieres til nye kladdenavne, der er oprettet under denne kladdetype.</span><span class="sxs-lookup"><span data-stu-id="f32ac-149">The selected reason code will be copied to new journal batches created under this journal template.</span></span> <span data-ttu-id="f32ac-150">Du kan knytte årsagskoder til kladdetyper i andre områder på samme måde.</span><span class="sxs-lookup"><span data-stu-id="f32ac-150">You assign reason codes to journal templates in the other application areas in the same way.</span></span>

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><span data-ttu-id="f32ac-151">Sådan bruges årsagskoder i salgs- og købsdokumenter</span><span class="sxs-lookup"><span data-stu-id="f32ac-151">To use reason codes on sales and purchase documents</span></span>

1. <span data-ttu-id="f32ac-152">Åbn det relevante salgs- eller købsdokument.</span><span class="sxs-lookup"><span data-stu-id="f32ac-152">Open the relevant sales or purchase document.</span></span>

2. <span data-ttu-id="f32ac-153">Angiv koden i feltet **Årsagskode** i salgs- eller købshovedet.</span><span class="sxs-lookup"><span data-stu-id="f32ac-153">On the sales or purchase header, enter the code in the **Reason Code** field.</span></span>

<span data-ttu-id="f32ac-154">Når fakturaen er bogført, kopieres årsagskoden til hver finans-, debitor- og kreditorpost.</span><span class="sxs-lookup"><span data-stu-id="f32ac-154">When the invoice is posted, the reason code is copied to each general ledger, customer, and vendor entry.</span></span> <span data-ttu-id="f32ac-155">Du kan ikke knytte forskellige årsagskoder til individuelle købs- og salgslinjer, fordi alle linjer er bogført som en post.</span><span class="sxs-lookup"><span data-stu-id="f32ac-155">You cannot assign different reason codes to the individual purchase and sales lines because all lines are posted as one entry.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="f32ac-156">Se relateret oplæring på [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="f32ac-156">See Related Training at [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="f32ac-157">Se også</span><span class="sxs-lookup"><span data-stu-id="f32ac-157">See Also</span></span>

[<span data-ttu-id="f32ac-158">Finans</span><span class="sxs-lookup"><span data-stu-id="f32ac-158">Finance</span></span>](finance.md)  
[<span data-ttu-id="f32ac-159">Bankkontoafstemning</span><span class="sxs-lookup"><span data-stu-id="f32ac-159">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="f32ac-160">Arbejde med dimensioner</span><span class="sxs-lookup"><span data-stu-id="f32ac-160">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="f32ac-161">Importer virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="f32ac-161">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="f32ac-162">Analysere pengestrømme i din virksomhed</span><span class="sxs-lookup"><span data-stu-id="f32ac-162">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="f32ac-163">[Arbejde med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f32ac-163">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
