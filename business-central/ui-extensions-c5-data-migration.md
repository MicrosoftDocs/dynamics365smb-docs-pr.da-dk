---
title: "Bruge udvidelsen C5-dataoverførsel | Microsoft Docs"
description: "Du kan bruge denne udvidelse til at overføre debitorer, kreditorer, varer og omkostninger på finanskonti fra Microsoft Dynamics C5 2012 til Business Central."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/09/208
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: fa6779ee8fb2bbb453014e32cb7f3cf8dcfa18da
ms.openlocfilehash: 698bde6949c6053501881d07135586810fc81bdd
ms.contentlocale: da-dk
ms.lasthandoff: 04/11/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="f8cf8-103">Udvidelsen Overførsel af C5-data til Business Central</span><span class="sxs-lookup"><span data-stu-id="f8cf8-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="f8cf8-104">Denne udvidelse gør det let at overføre debitorer, kreditorer, varer og finanskonti fra Microsoft Dynamics C5 2012 til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f8cf8-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f8cf8-105">Du kan også overføre gamle poster for finanskonti.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="f8cf8-106">Virksomheden i [!INCLUDE[d365fin](includes/d365fin_md.md)] må ikke indeholde data.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="f8cf8-107">Når du starter en overførsel, må du desuden ikke oprette debitorer, kreditorer, varer eller konti, før overflytningen er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="f8cf8-108">Hvilke data overføres?</span><span class="sxs-lookup"><span data-stu-id="f8cf8-108">What Data is Migrated?</span></span>
<span data-ttu-id="f8cf8-109">Følgende data overføres for hver enhed:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="f8cf8-110">**Kunder (Debitorer)**</span><span class="sxs-lookup"><span data-stu-id="f8cf8-110">**Customers**</span></span>
* <span data-ttu-id="f8cf8-111">Sted</span><span class="sxs-lookup"><span data-stu-id="f8cf8-111">Location</span></span>
* <span data-ttu-id="f8cf8-112">Land</span><span class="sxs-lookup"><span data-stu-id="f8cf8-112">Country</span></span>
* <span data-ttu-id="f8cf8-113">Kundedimensioner (afdeling, arbejdscenter og formål)</span><span class="sxs-lookup"><span data-stu-id="f8cf8-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="f8cf8-114">Leveringsform</span><span class="sxs-lookup"><span data-stu-id="f8cf8-114">Shipment method</span></span>
* <span data-ttu-id="f8cf8-115">Sælger</span><span class="sxs-lookup"><span data-stu-id="f8cf8-115">Sales Person</span></span>
* <span data-ttu-id="f8cf8-116">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="f8cf8-116">Payment terms</span></span>
* <span data-ttu-id="f8cf8-117">Betalingsform</span><span class="sxs-lookup"><span data-stu-id="f8cf8-117">Payment method</span></span>
* <span data-ttu-id="f8cf8-118">Debitorprisgruppe</span><span class="sxs-lookup"><span data-stu-id="f8cf8-118">Customer price group</span></span>
* <span data-ttu-id="f8cf8-119">Debitorfakturarabat</span><span class="sxs-lookup"><span data-stu-id="f8cf8-119">Customer invoice discount</span></span>

<span data-ttu-id="f8cf8-120">Hvis du overfører konti, overføres følgende data også:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="f8cf8-121">Opsætning for debitorbogføring</span><span class="sxs-lookup"><span data-stu-id="f8cf8-121">Customer posting setup</span></span>
* <span data-ttu-id="f8cf8-122">Finanskladdenavn</span><span class="sxs-lookup"><span data-stu-id="f8cf8-122">General journal batch</span></span>
* <span data-ttu-id="f8cf8-123">Åbne transaktioner (debitorposter)</span><span class="sxs-lookup"><span data-stu-id="f8cf8-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="f8cf8-124">**Leverandører (Kreditorer)**</span><span class="sxs-lookup"><span data-stu-id="f8cf8-124">**Vendors**</span></span>
* <span data-ttu-id="f8cf8-125">Sted</span><span class="sxs-lookup"><span data-stu-id="f8cf8-125">Location</span></span>
* <span data-ttu-id="f8cf8-126">Land</span><span class="sxs-lookup"><span data-stu-id="f8cf8-126">Country</span></span>
* <span data-ttu-id="f8cf8-127">Kreditordimensioner (afdeling, arbejdscenter og formål)</span><span class="sxs-lookup"><span data-stu-id="f8cf8-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="f8cf8-128">Fakturarabat</span><span class="sxs-lookup"><span data-stu-id="f8cf8-128">Invoice discount</span></span>
* <span data-ttu-id="f8cf8-129">Leveringsform</span><span class="sxs-lookup"><span data-stu-id="f8cf8-129">Shipment method</span></span>
* <span data-ttu-id="f8cf8-130">Indkøber</span><span class="sxs-lookup"><span data-stu-id="f8cf8-130">Purchaser</span></span>
* <span data-ttu-id="f8cf8-131">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="f8cf8-131">Payment terms</span></span>
* <span data-ttu-id="f8cf8-132">Betalingsform</span><span class="sxs-lookup"><span data-stu-id="f8cf8-132">Payment method</span></span>
* <span data-ttu-id="f8cf8-133">Kreditorfakturarabat</span><span class="sxs-lookup"><span data-stu-id="f8cf8-133">Vendor invoice discount</span></span>

<span data-ttu-id="f8cf8-134">Hvis du overfører konti, overføres følgende data også:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="f8cf8-135">Opsætning af kreditorbogføring</span><span class="sxs-lookup"><span data-stu-id="f8cf8-135">Vendor posting setup</span></span>
* <span data-ttu-id="f8cf8-136">Finanskladdenavn</span><span class="sxs-lookup"><span data-stu-id="f8cf8-136">General journal batch</span></span>
* <span data-ttu-id="f8cf8-137">Åbne transaktioner (kreditorposter)</span><span class="sxs-lookup"><span data-stu-id="f8cf8-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="f8cf8-138">**Varer**</span><span class="sxs-lookup"><span data-stu-id="f8cf8-138">**Items**</span></span>
* <span data-ttu-id="f8cf8-139">Sted</span><span class="sxs-lookup"><span data-stu-id="f8cf8-139">Location</span></span>
* <span data-ttu-id="f8cf8-140">Land</span><span class="sxs-lookup"><span data-stu-id="f8cf8-140">Country</span></span>
* <span data-ttu-id="f8cf8-141">Varedimensioner (afdeling, arbejdscenter og formål)</span><span class="sxs-lookup"><span data-stu-id="f8cf8-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="f8cf8-142">Salgslinjerabatter</span><span class="sxs-lookup"><span data-stu-id="f8cf8-142">Sales line discounts</span></span>
* <span data-ttu-id="f8cf8-143">Debitorrabatgrupper</span><span class="sxs-lookup"><span data-stu-id="f8cf8-143">Customer discount groups</span></span>
* <span data-ttu-id="f8cf8-144">Varerabatgrupper</span><span class="sxs-lookup"><span data-stu-id="f8cf8-144">Item discount groups</span></span>
* <span data-ttu-id="f8cf8-145">Salgspris</span><span class="sxs-lookup"><span data-stu-id="f8cf8-145">Sales price</span></span>
* <span data-ttu-id="f8cf8-146">Tarifnummer</span><span class="sxs-lookup"><span data-stu-id="f8cf8-146">Tariff number</span></span>
* <span data-ttu-id="f8cf8-147">Enheder</span><span class="sxs-lookup"><span data-stu-id="f8cf8-147">Units of measure</span></span>
* <span data-ttu-id="f8cf8-148">Varesporingskode</span><span class="sxs-lookup"><span data-stu-id="f8cf8-148">Item tracking code</span></span>
* <span data-ttu-id="f8cf8-149">Debitorprisgruppe</span><span class="sxs-lookup"><span data-stu-id="f8cf8-149">Customer price group</span></span>

<span data-ttu-id="f8cf8-150">Hvis du overfører konti, overføres følgende data også:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="f8cf8-151">Opsætning af lagerbogføring</span><span class="sxs-lookup"><span data-stu-id="f8cf8-151">Inventory posting setup</span></span>
* <span data-ttu-id="f8cf8-152">Bogføringsopsætning</span><span class="sxs-lookup"><span data-stu-id="f8cf8-152">General posting setup</span></span>
* <span data-ttu-id="f8cf8-153">Varekladdenavn</span><span class="sxs-lookup"><span data-stu-id="f8cf8-153">Item journal batch</span></span>
* <span data-ttu-id="f8cf8-154">Åbne transaktioner (vareposter)</span><span class="sxs-lookup"><span data-stu-id="f8cf8-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="f8cf8-155">Hvis der er åbne transaktioner, der bruger udenlandske valutaer, overføres valutakursen også for disse valutaer.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="f8cf8-156">Andre valutakurser overflyttes ikke.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-156">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="f8cf8-157">**Kontoplan**</span><span class="sxs-lookup"><span data-stu-id="f8cf8-157">**Chart of Accounts**</span></span>  
* <span data-ttu-id="f8cf8-158">Standarddimensioner: afdeling, omkostningssted og formål</span><span class="sxs-lookup"><span data-stu-id="f8cf8-158">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="f8cf8-159">Historiske finanstransaktioner</span><span class="sxs-lookup"><span data-stu-id="f8cf8-159">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="f8cf8-160">Historisk finanstransaktioner behandles lidt anderledes.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-160">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="f8cf8-161">Når du overfører data, angiver du en **Nuværende periode**-parameter.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-161">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="f8cf8-162">Denne parameter angiver, hvordan du skal behandle finanstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-162">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="f8cf8-163">Transaktioner efter denne dato overføres enkeltvis.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-163">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="f8cf8-164">Transaktioner inden denne dato lægges sammen pr. konto og overføres som et enkelt beløb.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-164">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="f8cf8-165">Lad os antage, at der er transaktioner i 2015, 2016, 2017, 2018, og du angiver den 1. januar 2017 i feltet Nuværende periode.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-165">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="f8cf8-166">For hver konto samles beløb for alle transaktioner på eller før den 31. december 2106 på en enkelt finanskladdelinje for hver finanskonto.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-166">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="f8cf8-167">Alle transaktioner efter denne dato overføres enkeltvis.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-167">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="f8cf8-168">Sådan overføres data</span><span class="sxs-lookup"><span data-stu-id="f8cf8-168">To migrate data</span></span>
<span data-ttu-id="f8cf8-169">Der er nogle få trin til at eksportere data fra C5 og indlæse dem i [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-169">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="f8cf8-170">I C5 skal du bruge funktionen **Eksportér databasen** til at eksportere dataene.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-170">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="f8cf8-171">Send derefter eksportmappen til en komprimeret (zippet) mappe.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-171">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="f8cf8-172">I [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Dataoverførsel** og derefter vælg **Dataoverførsel**.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-172">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="f8cf8-173">Udfør trinnene i guiden til assisteret opsætning.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-173">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="f8cf8-174">Sørg for at vælge **Indlæs fra Microsoft Dynamcis C5 2012** som datakilde.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-174">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="f8cf8-175">Virksomheder tilføje ofte felter for at tilpasse C5 til deres specifikke branche.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-175">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f8cf8-176"> overflytter ikke data fra brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-176"> does not migrate data from custom fields.</span></span> <span data-ttu-id="f8cf8-177">Overførslen mislykkes også, hvis du har mere end 10 brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-177">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="f8cf8-178">Få vist status for overførslen</span><span class="sxs-lookup"><span data-stu-id="f8cf8-178">Viewing the Status of the Migration</span></span>
<span data-ttu-id="f8cf8-179">Brug siden **Dataoverførselsoversigt** til at overvåge status for overførslen.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-179">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="f8cf8-180">Siden viser oplysninger, f.eks. antallet af enheder overførslen skal medtage, status for overførslen, og antallet af elementer, der er blevet overført, og om de var vellykket.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-180">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="f8cf8-181">Den viser også antallet af fejl, giver dig mulighed for at finde ud af, hvad der gik galt, og gør det, hvis det er muligt, nemt at gå til enheden for at løse problemerne.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-181">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="f8cf8-182">Du kan finde flere oplysninger i næste afsnit i dette emne.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-182">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="f8cf8-183">Mens du venter på resultaterne af overførslen, skal du opdatere siden for at få vist resultaterne.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-183">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="f8cf8-184">Sådan undgås dobbeltbogføring</span><span class="sxs-lookup"><span data-stu-id="f8cf8-184">How to Avoid Double-Posting</span></span>
<span data-ttu-id="f8cf8-185">For at undgå dobbeltbogføring i finansregnskabet bruges følgende modkonti til åbne posteringer:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-185">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  
  
* <span data-ttu-id="f8cf8-186">For kreditorer bruger vi kreditorkontoen fra kreditorbogføringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-186">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="f8cf8-187">For debitorer bruger vi debitorkontoen fra debitorbogføringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-187">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="f8cf8-188">For varer opretter vi en bogføringsopsætning, hvor reguleringskontoen er den konto, der er angivet som lagerkontoen i varebogføringsopsætningen.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-188">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="f8cf8-189">Rette fejl</span><span class="sxs-lookup"><span data-stu-id="f8cf8-189">Correcting Errors</span></span>
<span data-ttu-id="f8cf8-190">Hvis noget går galt, og der opstår en fejl, viser feltet **Status** teksten **Udført med fejl**, og feltet **Antal fejl** viser hvor mange.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-190">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="f8cf8-191">For at få vist en liste over fejlene, kan du åbne siden **Dataoverførselsfejl** side ved at vælge:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-191">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="f8cf8-192">Nummeret i feltet **Antal fejl** for enheden.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-192">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="f8cf8-193">Enheden og derefter handlingen **Vis fejl**.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-193">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="f8cf8-194">På siden **Dataoverførselsfejl** kan du for at rette en fejl vælge en fejlmeddelelse, og derefter vælge **Rediger post** for at åbne en side, der viser de overførte data for objektet.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-194">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="f8cf8-195">Når du retter en eller flere fejl, kan du vælge **Overfør** for kun at overføre de enheder, du rettede, uden at genstarte hele overførslen.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-195">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="f8cf8-196">Hvis du har rettet mere end én fejl, kan du bruge funktionen **Markér flere** til at markere flere linjer, der skal overføres.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-196">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="f8cf8-197">Hvis der omvendt er fejl, det ikke er vigtigt at løse, kan du vælge dem og derefter vælge **Spring valg over**.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-197">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="f8cf8-198">Hvis du har varer, der indgår i en stykliste, kan du være nødt til at overføre mere end én gang, hvis den oprindelige vare ikke er oprettet før de varianter, der refererer til den.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-198">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="f8cf8-199">Hvis en varevariant oprettes først, kan det medføre, at referencen til den oprindelige vare giver en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-199">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="f8cf8-200">Kontrol af data efter overførsel</span><span class="sxs-lookup"><span data-stu-id="f8cf8-200">Verifying Data After Migrating</span></span>
<span data-ttu-id="f8cf8-201">En måde til at kontrollere, at dine data overføres korrekt, er ved at se på følgende sider i C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f8cf8-201">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="f8cf8-202">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="f8cf8-202">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="f8cf8-203">Den kørsel, der skal bruges</span><span class="sxs-lookup"><span data-stu-id="f8cf8-203">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="f8cf8-204">Debitorposter</span><span class="sxs-lookup"><span data-stu-id="f8cf8-204">Customer Entries</span></span>| <span data-ttu-id="f8cf8-205">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="f8cf8-205">General Journals</span></span>| <span data-ttu-id="f8cf8-206">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="f8cf8-206">CUSTMIGR</span></span> |
|<span data-ttu-id="f8cf8-207">Kreditorposter</span><span class="sxs-lookup"><span data-stu-id="f8cf8-207">Vendor Entries</span></span>| <span data-ttu-id="f8cf8-208">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="f8cf8-208">General Journals</span></span>| <span data-ttu-id="f8cf8-209">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="f8cf8-209">VENDMIGR</span></span>|
|<span data-ttu-id="f8cf8-210">Vareposter</span><span class="sxs-lookup"><span data-stu-id="f8cf8-210">Item Entries</span></span>| <span data-ttu-id="f8cf8-211">Varekladder</span><span class="sxs-lookup"><span data-stu-id="f8cf8-211">Item Journals</span></span>| <span data-ttu-id="f8cf8-212">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="f8cf8-212">ITEMMIGR</span></span> |
|<span data-ttu-id="f8cf8-213">Finansposter</span><span class="sxs-lookup"><span data-stu-id="f8cf8-213">G/L Entries</span></span>| <span data-ttu-id="f8cf8-214">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="f8cf8-214">General Journals</span></span>| <span data-ttu-id="f8cf8-215">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="f8cf8-215">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="f8cf8-216">Stoppe dataoverførslen</span><span class="sxs-lookup"><span data-stu-id="f8cf8-216">Stopping Data Migration</span></span>
<span data-ttu-id="f8cf8-217">Du kan stoppe overførslen af data ved at vælge **Stop alle overførsler**.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-217">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="f8cf8-218">Hvis du gør det, stoppes alle ventende overførsler også.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-218">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8cf8-219">Se også</span><span class="sxs-lookup"><span data-stu-id="f8cf8-219">See Also</span></span>
<span data-ttu-id="f8cf8-220">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="f8cf8-220">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="f8cf8-221">Introduktion</span><span class="sxs-lookup"><span data-stu-id="f8cf8-221">Getting Started</span></span>](product-get-started.md) 

