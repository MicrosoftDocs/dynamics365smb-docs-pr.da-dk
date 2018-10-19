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
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a10c05116e97cdf000bd46258a9d67f4c9910c90
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---

# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="1c013-103">Udvidelsen C5-dataoverførsel</span><span class="sxs-lookup"><span data-stu-id="1c013-103">The C5 Data Migration Extension</span></span>
<span data-ttu-id="1c013-104">Denne udvidelse gør det let at overføre debitorer, kreditorer, varer og finanskonti fra Microsoft Dynamics C5 2012 til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1c013-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1c013-105">Du kan også overføre gamle poster for finanskonti.</span><span class="sxs-lookup"><span data-stu-id="1c013-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="1c013-106">Virksomheden i [!INCLUDE[d365fin](includes/d365fin_md.md)] må ikke indeholde data.</span><span class="sxs-lookup"><span data-stu-id="1c013-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="1c013-107">Når du starter en overførsel, må du desuden ikke oprette debitorer, kreditorer, varer eller konti, før overflytningen er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="1c013-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="1c013-108">Hvilke data overføres?</span><span class="sxs-lookup"><span data-stu-id="1c013-108">What Data is Migrated?</span></span>
<span data-ttu-id="1c013-109">Følgende data overføres for hver enhed:</span><span class="sxs-lookup"><span data-stu-id="1c013-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="1c013-110">**Kunder (Debitorer)**</span><span class="sxs-lookup"><span data-stu-id="1c013-110">**Customers**</span></span>
* <span data-ttu-id="1c013-111">Kontakter</span><span class="sxs-lookup"><span data-stu-id="1c013-111">Contacts</span></span>  
* <span data-ttu-id="1c013-112">Sted</span><span class="sxs-lookup"><span data-stu-id="1c013-112">Location</span></span>
* <span data-ttu-id="1c013-113">Land/område</span><span class="sxs-lookup"><span data-stu-id="1c013-113">Country</span></span>
* <span data-ttu-id="1c013-114">Kundedimensioner (afdeling, arbejdscenter og formål)</span><span class="sxs-lookup"><span data-stu-id="1c013-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="1c013-115">Leveringsform</span><span class="sxs-lookup"><span data-stu-id="1c013-115">Shipment method</span></span>
* <span data-ttu-id="1c013-116">Sælger</span><span class="sxs-lookup"><span data-stu-id="1c013-116">Sales Person</span></span>
* <span data-ttu-id="1c013-117">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="1c013-117">Payment terms</span></span>
* <span data-ttu-id="1c013-118">Betalingsform</span><span class="sxs-lookup"><span data-stu-id="1c013-118">Payment method</span></span>
* <span data-ttu-id="1c013-119">Debitorprisgruppe</span><span class="sxs-lookup"><span data-stu-id="1c013-119">Customer price group</span></span>
* <span data-ttu-id="1c013-120">Debitorfakturarabat</span><span class="sxs-lookup"><span data-stu-id="1c013-120">Customer invoice discount</span></span>

<span data-ttu-id="1c013-121">Hvis du overfører konti, overføres følgende data også:</span><span class="sxs-lookup"><span data-stu-id="1c013-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="1c013-122">Opsætning for debitorbogføring</span><span class="sxs-lookup"><span data-stu-id="1c013-122">Customer posting setup</span></span>
* <span data-ttu-id="1c013-123">Finanskladdenavn</span><span class="sxs-lookup"><span data-stu-id="1c013-123">General journal batch</span></span>
* <span data-ttu-id="1c013-124">Åbne transaktioner (debitorposter)</span><span class="sxs-lookup"><span data-stu-id="1c013-124">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="1c013-125">**Leverandører (Kreditorer)**</span><span class="sxs-lookup"><span data-stu-id="1c013-125">**Vendors**</span></span>
* <span data-ttu-id="1c013-126">Kontakter</span><span class="sxs-lookup"><span data-stu-id="1c013-126">Contacts</span></span>
* <span data-ttu-id="1c013-127">Sted</span><span class="sxs-lookup"><span data-stu-id="1c013-127">Location</span></span>
* <span data-ttu-id="1c013-128">Land/område</span><span class="sxs-lookup"><span data-stu-id="1c013-128">Country</span></span>
* <span data-ttu-id="1c013-129">Kreditordimensioner (afdeling, arbejdscenter og formål)</span><span class="sxs-lookup"><span data-stu-id="1c013-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="1c013-130">Fakturarabat</span><span class="sxs-lookup"><span data-stu-id="1c013-130">Invoice discount</span></span>
* <span data-ttu-id="1c013-131">Leveringsform</span><span class="sxs-lookup"><span data-stu-id="1c013-131">Shipment method</span></span>
* <span data-ttu-id="1c013-132">Indkøber</span><span class="sxs-lookup"><span data-stu-id="1c013-132">Purchaser</span></span>
* <span data-ttu-id="1c013-133">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="1c013-133">Payment terms</span></span>
* <span data-ttu-id="1c013-134">Betalingsform</span><span class="sxs-lookup"><span data-stu-id="1c013-134">Payment method</span></span>
* <span data-ttu-id="1c013-135">Kreditorfakturarabat</span><span class="sxs-lookup"><span data-stu-id="1c013-135">Vendor invoice discount</span></span>

<span data-ttu-id="1c013-136">Hvis du overfører konti, overføres følgende data også:</span><span class="sxs-lookup"><span data-stu-id="1c013-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="1c013-137">Opsætning af kreditorbogføring</span><span class="sxs-lookup"><span data-stu-id="1c013-137">Vendor posting setup</span></span>
* <span data-ttu-id="1c013-138">Finanskladdenavn</span><span class="sxs-lookup"><span data-stu-id="1c013-138">General journal batch</span></span>
* <span data-ttu-id="1c013-139">Åbne transaktioner (kreditorposter)</span><span class="sxs-lookup"><span data-stu-id="1c013-139">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="1c013-140">**Varer**</span><span class="sxs-lookup"><span data-stu-id="1c013-140">**Items**</span></span>
* <span data-ttu-id="1c013-141">Sted</span><span class="sxs-lookup"><span data-stu-id="1c013-141">Location</span></span>
* <span data-ttu-id="1c013-142">Land</span><span class="sxs-lookup"><span data-stu-id="1c013-142">Country</span></span>
* <span data-ttu-id="1c013-143">Varedimensioner (afdeling, arbejdscenter og formål)</span><span class="sxs-lookup"><span data-stu-id="1c013-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="1c013-144">Salgslinjerabatter</span><span class="sxs-lookup"><span data-stu-id="1c013-144">Sales line discounts</span></span>
* <span data-ttu-id="1c013-145">Debitorrabatgrupper</span><span class="sxs-lookup"><span data-stu-id="1c013-145">Customer discount groups</span></span>
* <span data-ttu-id="1c013-146">Varerabatgrupper</span><span class="sxs-lookup"><span data-stu-id="1c013-146">Item discount groups</span></span>
* <span data-ttu-id="1c013-147">Salgspris</span><span class="sxs-lookup"><span data-stu-id="1c013-147">Sales price</span></span>
* <span data-ttu-id="1c013-148">Tarifnummer</span><span class="sxs-lookup"><span data-stu-id="1c013-148">Tariff number</span></span>
* <span data-ttu-id="1c013-149">Enheder</span><span class="sxs-lookup"><span data-stu-id="1c013-149">Units of measure</span></span>
* <span data-ttu-id="1c013-150">Varesporingskode</span><span class="sxs-lookup"><span data-stu-id="1c013-150">Item tracking code</span></span>
* <span data-ttu-id="1c013-151">Debitorprisgruppe</span><span class="sxs-lookup"><span data-stu-id="1c013-151">Customer price group</span></span>
* <span data-ttu-id="1c013-152">Montagestyklister</span><span class="sxs-lookup"><span data-stu-id="1c013-152">Assembly BOMs</span></span>

<span data-ttu-id="1c013-153">Hvis du overfører konti, overføres følgende data også:</span><span class="sxs-lookup"><span data-stu-id="1c013-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="1c013-154">Opsætning af lagerbogføring</span><span class="sxs-lookup"><span data-stu-id="1c013-154">Inventory posting setup</span></span>
* <span data-ttu-id="1c013-155">Bogføringsopsætning</span><span class="sxs-lookup"><span data-stu-id="1c013-155">General posting setup</span></span>
* <span data-ttu-id="1c013-156">Varekladdenavn</span><span class="sxs-lookup"><span data-stu-id="1c013-156">Item journal batch</span></span>
* <span data-ttu-id="1c013-157">Åbne transaktioner (vareposter)</span><span class="sxs-lookup"><span data-stu-id="1c013-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="1c013-158">Hvis der er åbne transaktioner, der bruger udenlandske valutaer, overføres valutakursen også for disse valutaer.</span><span class="sxs-lookup"><span data-stu-id="1c013-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="1c013-159">Andre valutakurser overflyttes ikke.</span><span class="sxs-lookup"><span data-stu-id="1c013-159">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="1c013-160">**Kontoplan**</span><span class="sxs-lookup"><span data-stu-id="1c013-160">**Chart of Accounts**</span></span>  
* <span data-ttu-id="1c013-161">Standarddimensioner: afdeling, omkostningssted og formål</span><span class="sxs-lookup"><span data-stu-id="1c013-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="1c013-162">Historiske finanstransaktioner</span><span class="sxs-lookup"><span data-stu-id="1c013-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="1c013-163">Historisk finanstransaktioner behandles lidt anderledes.</span><span class="sxs-lookup"><span data-stu-id="1c013-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="1c013-164">Når du overfører data, angiver du en **Nuværende periode**-parameter.</span><span class="sxs-lookup"><span data-stu-id="1c013-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="1c013-165">Denne parameter angiver, hvordan du skal behandle finanstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="1c013-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="1c013-166">Transaktioner efter denne dato overføres enkeltvis.</span><span class="sxs-lookup"><span data-stu-id="1c013-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="1c013-167">Transaktioner inden denne dato lægges sammen pr. konto og overføres som et enkelt beløb.</span><span class="sxs-lookup"><span data-stu-id="1c013-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="1c013-168">Lad os antage, at der er transaktioner i 2015, 2016, 2017, 2018, og du angiver den 1. januar 2017 i feltet Nuværende periode.</span><span class="sxs-lookup"><span data-stu-id="1c013-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="1c013-169">For hver konto samles beløb for alle transaktioner på eller før den 31. december 2106 på en enkelt finanskladdelinje for hver finanskonto.</span><span class="sxs-lookup"><span data-stu-id="1c013-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="1c013-170">Alle transaktioner efter denne dato overføres enkeltvis.</span><span class="sxs-lookup"><span data-stu-id="1c013-170">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="1c013-171">Sådan overføres data</span><span class="sxs-lookup"><span data-stu-id="1c013-171">To migrate data</span></span>
<span data-ttu-id="1c013-172">Der er nogle få trin til at eksportere data fra C5 og indlæse dem i [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="1c013-172">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="1c013-173">I C5 skal du bruge funktionen **Eksportér databasen** til at eksportere dataene.</span><span class="sxs-lookup"><span data-stu-id="1c013-173">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="1c013-174">Send derefter eksportmappen til en komprimeret (zippet) mappe.</span><span class="sxs-lookup"><span data-stu-id="1c013-174">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="1c013-175">I [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Dataoverførsel** og derefter vælge **Dataoverførsel**.</span><span class="sxs-lookup"><span data-stu-id="1c013-175">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="1c013-176">Udfør trinnene i guiden til assisteret opsætning.</span><span class="sxs-lookup"><span data-stu-id="1c013-176">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="1c013-177">Sørg for at vælge **Indlæs fra Microsoft Dynamcis C5 2012** som datakilde.</span><span class="sxs-lookup"><span data-stu-id="1c013-177">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="1c013-178">Virksomheder tilføje ofte felter for at tilpasse C5 til deres specifikke branche.</span><span class="sxs-lookup"><span data-stu-id="1c013-178">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="1c013-179">overflytter ikke data fra brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="1c013-179">does not migrate data from custom fields.</span></span> <span data-ttu-id="1c013-180">Overførslen mislykkes også, hvis du har mere end 10 brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="1c013-180">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="1c013-181">Få vist status for overførslen</span><span class="sxs-lookup"><span data-stu-id="1c013-181">Viewing the Status of the Migration</span></span>
<span data-ttu-id="1c013-182">Brug vinduet **Dataoverførselsoversigt** til at overvåge status for overførslen.</span><span class="sxs-lookup"><span data-stu-id="1c013-182">Use the **Data Migration Overview** window to monitor the success of the migration.</span></span> <span data-ttu-id="1c013-183">Siden viser oplysninger, f.eks. antallet af enheder overførslen skal medtage, status for overførslen, og antallet af elementer, der er blevet overført, og om de var vellykket.</span><span class="sxs-lookup"><span data-stu-id="1c013-183">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="1c013-184">Den viser også antallet af fejl, giver dig mulighed for at finde ud af, hvad der gik galt, og gør det, hvis det er muligt, nemt at gå til enheden for at løse problemerne.</span><span class="sxs-lookup"><span data-stu-id="1c013-184">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="1c013-185">Du kan finde flere oplysninger i næste afsnit i dette emne.</span><span class="sxs-lookup"><span data-stu-id="1c013-185">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="1c013-186">Mens du venter på resultaterne af overførslen, skal du opdatere siden for at få vist resultaterne.</span><span class="sxs-lookup"><span data-stu-id="1c013-186">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="1c013-187">Sådan undgås dobbeltbogføring</span><span class="sxs-lookup"><span data-stu-id="1c013-187">How to Avoid Double-Posting</span></span>
<span data-ttu-id="1c013-188">For at undgå dobbeltbogføring i finansregnskabet bruges følgende modkonti til åbne posteringer:</span><span class="sxs-lookup"><span data-stu-id="1c013-188">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="1c013-189">For kreditorer bruger vi kreditorkontoen fra kreditorbogføringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="1c013-189">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="1c013-190">For debitorer bruger vi debitorkontoen fra debitorbogføringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="1c013-190">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="1c013-191">For varer opretter vi en bogføringsopsætning, hvor reguleringskontoen er den konto, der er angivet som lagerkontoen i varebogføringsopsætningen.</span><span class="sxs-lookup"><span data-stu-id="1c013-191">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="1c013-192">Rette fejl</span><span class="sxs-lookup"><span data-stu-id="1c013-192">Correcting Errors</span></span>
<span data-ttu-id="1c013-193">Hvis noget går galt, og der opstår en fejl, viser feltet **Status** teksten **Udført med fejl**, og feltet **Antal fejl** viser hvor mange.</span><span class="sxs-lookup"><span data-stu-id="1c013-193">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="1c013-194">For at få vist en liste over fejlene skal du åbne vinduet **Dataoverførselsfejl** ved at vælge:</span><span class="sxs-lookup"><span data-stu-id="1c013-194">To view a list of the errors, you can open the **Data Migration Errors** window by choosing:</span></span>  

* <span data-ttu-id="1c013-195">Nummeret i feltet **Antal fejl** for enheden.</span><span class="sxs-lookup"><span data-stu-id="1c013-195">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="1c013-196">Enheden og derefter handlingen **Vis fejl**.</span><span class="sxs-lookup"><span data-stu-id="1c013-196">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="1c013-197">I vinduet **Dataoverførselsfejl** kan du for at rette en fejl vælge en fejlmeddelelse og derefter vælge **Rediger post** for at få vist de overførte data for objektet.</span><span class="sxs-lookup"><span data-stu-id="1c013-197">In the **Data Migration Errors** window, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="1c013-198">Hvis du har flere fejl, der skal løses, kan du vælge **Fejl flere fejl ad gangen** for at redigere objekter på en liste.</span><span class="sxs-lookup"><span data-stu-id="1c013-198">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="1c013-199">Du skal stadig åbne de individuelle poster, dog kun hvis fejlen blev forårsaget af en relateret post.</span><span class="sxs-lookup"><span data-stu-id="1c013-199">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="1c013-200">F.eks. overføres en leverandør ikke, hvis en e-mailadresse for en af leverandørens kontakter har et ugyldigt format.</span><span class="sxs-lookup"><span data-stu-id="1c013-200">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="1c013-201">Når du retter en eller flere fejl, kan du vælge **Overfør** for kun at overføre de enheder, du rettede, uden at genstarte hele overførslen.</span><span class="sxs-lookup"><span data-stu-id="1c013-201">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="1c013-202">Hvis du har rettet mere end én fejl, kan du bruge funktionen **Markér flere** til at markere flere linjer, der skal overføres.</span><span class="sxs-lookup"><span data-stu-id="1c013-202">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="1c013-203">Hvis der omvendt er fejl, det ikke er vigtigt at løse, kan du vælge dem og derefter vælge **Spring valg over**.</span><span class="sxs-lookup"><span data-stu-id="1c013-203">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="1c013-204">Hvis du har varer, der indgår i en stykliste, kan du være nødt til at overføre mere end én gang, hvis den oprindelige vare ikke er oprettet før de varianter, der refererer til den.</span><span class="sxs-lookup"><span data-stu-id="1c013-204">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="1c013-205">Hvis en varevariant oprettes først, kan det medføre, at referencen til den oprindelige vare giver en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="1c013-205">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="1c013-206">Kontrol af data efter overførsel</span><span class="sxs-lookup"><span data-stu-id="1c013-206">Verifying Data After Migrating</span></span>
<span data-ttu-id="1c013-207">En måde til at kontrollere, at dine data overføres korrekt, er ved at se på følgende sider i C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1c013-207">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="1c013-208">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="1c013-208">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="1c013-209">Den kørsel, der skal bruges</span><span class="sxs-lookup"><span data-stu-id="1c013-209">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="1c013-210">Debitorposter</span><span class="sxs-lookup"><span data-stu-id="1c013-210">Customer Entries</span></span>| <span data-ttu-id="1c013-211">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="1c013-211">General Journals</span></span>| <span data-ttu-id="1c013-212">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="1c013-212">CUSTMIGR</span></span> |
|<span data-ttu-id="1c013-213">Kreditorposter</span><span class="sxs-lookup"><span data-stu-id="1c013-213">Vendor Entries</span></span>| <span data-ttu-id="1c013-214">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="1c013-214">General Journals</span></span>| <span data-ttu-id="1c013-215">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="1c013-215">VENDMIGR</span></span>|
|<span data-ttu-id="1c013-216">Vareposter</span><span class="sxs-lookup"><span data-stu-id="1c013-216">Item Entries</span></span>| <span data-ttu-id="1c013-217">Varekladder</span><span class="sxs-lookup"><span data-stu-id="1c013-217">Item Journals</span></span>| <span data-ttu-id="1c013-218">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="1c013-218">ITEMMIGR</span></span> |
|<span data-ttu-id="1c013-219">Finansposter</span><span class="sxs-lookup"><span data-stu-id="1c013-219">G/L Entries</span></span>| <span data-ttu-id="1c013-220">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="1c013-220">General Journals</span></span>| <span data-ttu-id="1c013-221">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="1c013-221">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="1c013-222">Stoppe dataoverførslen</span><span class="sxs-lookup"><span data-stu-id="1c013-222">Stopping Data Migration</span></span>
<span data-ttu-id="1c013-223">Du kan stoppe overførslen af data ved at vælge **Stop alle overførsler**.</span><span class="sxs-lookup"><span data-stu-id="1c013-223">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="1c013-224">Hvis du gør det, stoppes alle ventende overførsler også.</span><span class="sxs-lookup"><span data-stu-id="1c013-224">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c013-225">Se også</span><span class="sxs-lookup"><span data-stu-id="1c013-225">See Also</span></span>
<span data-ttu-id="1c013-226">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="1c013-226">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="1c013-227">Introduktion</span><span class="sxs-lookup"><span data-stu-id="1c013-227">Getting Started</span></span>](product-get-started.md)

