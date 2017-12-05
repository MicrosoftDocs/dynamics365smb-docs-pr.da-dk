---
title: Konsolidere data fra flere virksomheder | Microsoft Docs
description: "Få vist en oversigt over den finansielle tilstand på tværs af din virksomhed."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 07/14/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 9739f89c45dd63d03235fef4204b2adeb48ac4d3
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---

# <a name="how-to-work-with-the-consolidated-trial-balance-report"></a><span data-ttu-id="6f5ee-103">Fremgangsmåde: Arbejde med rapporten Konsolideret råbalance</span><span class="sxs-lookup"><span data-stu-id="6f5ee-103">How To: Work with the Consolidated Trial Balance Report</span></span>
<span data-ttu-id="6f5ee-104">Hvis du har mere end én virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan rapporten Konsolideret råbalance i Rollecenteret Regnskabsmedarbejder give dig et overblik over virksomheden samlede finansielle tilstand.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-104">If you have more than one company in [!INCLUDE[d365fin](includes/d365fin_md.md)], the Consolidated Trial Balance Report on the Accountant Role Center can give you an overview of the financial health of your overall business.</span></span>  

<span data-ttu-id="6f5ee-105">Rapporten kombinerer finansposter fra alle dine regnskaber i et nyt virksomhed, som du opretter til at indeholder de konsoliderede data.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-105">The report combines general ledger (G/L) entries from each of your companies in a new company that you create to contain the consolidated data.</span></span> <span data-ttu-id="6f5ee-106">Dette regnskab kaldes typisk det "konsoliderede regnskab".</span><span class="sxs-lookup"><span data-stu-id="6f5ee-106">This company is typically referred to as the "consolidated company."</span></span> <span data-ttu-id="6f5ee-107">Det konsoliderede regnskab er kun en beholder til de konsoliderede data og har ingen direkte forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-107">The consolidated company is just a container for the consolidated data, and does not have any live business data.</span></span> <span data-ttu-id="6f5ee-108">De regnskaber, du inkluderer i det konsoliderede regnskab, bliver **koncernvirksomheder** i rapporten.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-108">The companies that you include in the consolidated company become **Business Units** in the report.</span></span>

<span data-ttu-id="6f5ee-109">Du kan konsolidere:</span><span class="sxs-lookup"><span data-stu-id="6f5ee-109">You can consolidate:</span></span>  

* <span data-ttu-id="6f5ee-110">På tværs af regnskaber med forskellige kontoplaner.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-110">Across companies that have different charts of accounts.</span></span>  
* <span data-ttu-id="6f5ee-111">Regnskaber med forskellige regnskabsår og forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-111">Companies that use different fiscal years and different currencies.</span></span>  
* <span data-ttu-id="6f5ee-112">Enten det fulde beløb eller en procentdel af et regnskabs finansielle oplysninger</span><span class="sxs-lookup"><span data-stu-id="6f5ee-112">Either the full amount or a percentage of a company's financial information</span></span>
* <span data-ttu-id="6f5ee-113">Ved brug af forskellige valutakurser i de enkelte finanskonti</span><span class="sxs-lookup"><span data-stu-id="6f5ee-113">Using different currency exchange rates in individual G/L accounts</span></span>

<span data-ttu-id="6f5ee-114">Afhængigt af kompleksiteten af virksomhederne kan rapporten konfigureres på to måder:</span><span class="sxs-lookup"><span data-stu-id="6f5ee-114">Depending on the complexity of your businesses, there are two ways to set up the report:</span></span>

* <span data-ttu-id="6f5ee-115">Hvis du ikke har brug for avancerede indstillinger, f.eks. inklusion af et regnskab, som du kun er en del af, kan du bruge den assisterede opsætningsvejledning **Virksomhedskonsolidering** til hurtigt at oprette en konsolidering.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-115">If you don't need advanced settings, such as including a company that you only own part of, you can use the **Company Consolidation** assisted setup guide to quickly set up a consolidation.</span></span> <span data-ttu-id="6f5ee-116">Guiden hjælper dig gennem de grundlæggende trin.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-116">The guide helps you through the basic steps.</span></span>
* <span data-ttu-id="6f5ee-117">Hvis du har brug for mere avancerede indstillinger, kan du oprette det konsoliderede regnskab og koncernvirksomhederne selv.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-117">If you do need more advanced settings, you can set up the consolidated company and business units yourself.</span></span>

## <a name="to-do-a-simple-consolidation-setup"></a><span data-ttu-id="6f5ee-118">Sådan udfører du en simpel konsolideringsopsætning</span><span class="sxs-lookup"><span data-stu-id="6f5ee-118">To do a simple consolidation setup</span></span>
<span data-ttu-id="6f5ee-119">Hvis din konsolidering er enkel, f.eks. fordi du er eneejer af de koncernvirksomheder, der skal konsolideres, hjælper den assisterede opsætningsvejledning **Virksomhedskonsolidering** dig gennem følgende trin:</span><span class="sxs-lookup"><span data-stu-id="6f5ee-119">If your consolidation is straightforward, for example because you wholly-own the business units to consolidate, the **Company Consolidation** assisted setup guide will help you through the following steps:</span></span>

* <span data-ttu-id="6f5ee-120">Vælg, om du vil oprette et nyt konsolideret regnskab, eller om du vil konsolidere data i et regnskab, som du allerede har oprettet til konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-120">Choose whether to create a new consolidated company, or whether to consolidate the data in a company that you have already created for the consolidation.</span></span> <span data-ttu-id="6f5ee-121">Regnskabet må ikke indeholde transaktioner.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-121">The company should not contain transactions.</span></span>
* <span data-ttu-id="6f5ee-122">Få vist resultaterne.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-122">Preview the results.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6f5ee-123"> kontrollerer, at masterdata og transaktioner kan overføres til det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-123"> verifies that the master data and transactions can be successfully transferred to the consolidated company.</span></span>

<span data-ttu-id="6f5ee-124">Hvis du vil bruge den assisterede opsætningsvejledning, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="6f5ee-124">To use the assisted setup guide, follow these steps:</span></span>

1. <span data-ttu-id="6f5ee-125">I Rollecenteret **Bogholder** skal du vælge handlingen **Assisteret opsætning**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-125">On the **Accountant** Role Center, choose the **Assisted Setup** action.</span></span>
2. <span data-ttu-id="6f5ee-126">Vælg **Konfigurer konsolideringsrapportering**, og udfør derefter de enkelte trin i den assisterede opsætningsvejledning.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-126">Choose **Set up consolidation reporting**, and then complete each step in the assisted setup guide.</span></span>

## <a name="to-do-an-advanced-consolidation-setup"></a><span data-ttu-id="6f5ee-127">Sådan konfigurerer du en avanceret konsolidering</span><span class="sxs-lookup"><span data-stu-id="6f5ee-127">To do an advanced consolidation setup</span></span>
<span data-ttu-id="6f5ee-128">Hvis du har brug for mere avancerede indstillinger til din konsolidering, kan du oprette konsolideringen manuelt.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-128">If you need more advanced settings for your consolidation, you can set up consolidation manually.</span></span> <span data-ttu-id="6f5ee-129">Hvis du f.eks. har virksomheder, som du kun ejer delvist, eller virksomheder, som du ikke vil have med i konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-129">For example, if you have companies that you own only partially, or you have companies that you don’t want to include in the consolidation.</span></span> <span data-ttu-id="6f5ee-130">Du kan oprette det konsoliderede regnskab på samme måde, som du opretter andre regnskaber.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-130">You set up the consolidated company in the say way that you set up other companies.</span></span> <span data-ttu-id="6f5ee-131">Du kan finde flere oplysninger under [Blive klar til at handle](ui-get-ready-business.md).</span><span class="sxs-lookup"><span data-stu-id="6f5ee-131">For more information, see [Getting Ready for Doing Business](ui-get-ready-business.md).</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6f5ee-132"> giver dig mulighed for at oprette en liste over regnskaber, der skal konsolideres, kontrollere regnskabsdataene, før du konsoliderer dem, importere filer og oprette konsolideringsrapporter.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-132"> lets you set up a list of companies to consolidate, verify the accounting data before you consolidate it, import files, and generate consolidation reports.</span></span>  

1. <span data-ttu-id="6f5ee-133">Log på det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-133">Sign in to the consolidated company.</span></span>
2. <span data-ttu-id="6f5ee-134">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncernvirksomheder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-134">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Business Units**, and then choose the related link.</span></span>  
3. <span data-ttu-id="6f5ee-135">Vælg **Ny**, og udfyld de påkrævede felter.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-135">Choose **New**, and then fill in the required fields.</span></span>  

<span data-ttu-id="6f5ee-136">Hvis koncernvirksomheden bruger en fremmed valuta, skal du angive kursen, der skal anvendes i konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-136">If your business unit uses a foreign currency, you must specify the exchange rate to use in the consolidation.</span></span> <span data-ttu-id="6f5ee-137">Du skal også angive konsolideringsoplysninger om koncernvirksomhedens finanskonti.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-137">You must also enter consolidation information about the business unit's general ledger accounts.</span></span> <span data-ttu-id="6f5ee-138">Disse processer beskrives i de følgende afsnit.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-138">These processes are described in the following sections.</span></span>

### <a name="to-prepare-general-ledger-accounts-for-consolidation"></a><span data-ttu-id="6f5ee-139">Sådan klargøres finanskonti til konsolidering</span><span class="sxs-lookup"><span data-stu-id="6f5ee-139">To prepare general ledger accounts for consolidation</span></span>
<span data-ttu-id="6f5ee-140">Hvis kontoplanen i koncernvirksomheden er anderledes end det konsoliderede regnskab, skal du forberede finanskonti til konsolidering.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-140">If the chart of accounts in the business unit differs from the consolidated company, you must prepare general ledger accounts for consolidation.</span></span> <span data-ttu-id="6f5ee-141">Du kan angive de konti, hvor debet og kredit skal posteres, og metoden, der skal bruges til at oversætte valutaer i det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-141">You can specify the accounts to post debits and credits to, and the method to use to translate currencies in the consolidated company.</span></span> <span data-ttu-id="6f5ee-142">Det er f.eks. nyttigt, hvis du ofte udfører rapporten.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-142">For example, this is useful if you frequently run the report.</span></span>

1. <span data-ttu-id="6f5ee-143">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-143">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6f5ee-144">Åbn kortet for kontoen, og udfyld derefter felterne på oversigtspanelet **Konsolidering**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-144">Open the card for the account, and then fill in the fields on the **Consolidation** FastTab.</span></span>

### <a name="to-specify-exchange-rates-for-consolidations"></a><span data-ttu-id="6f5ee-145">Sådan angives kurser for konsolideringer</span><span class="sxs-lookup"><span data-stu-id="6f5ee-145">To specify exchange rates for consolidations</span></span>
<span data-ttu-id="6f5ee-146">Hvis en koncernvirksomhed bruger en anden valuta end det konsoliderede regnskab, skal du angive valutakursmetoder for hver konto, før du konsoliderer.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-146">If a business unit uses a different currency than the consolidated company, you must specify exchange rate methods for each account before you consolidate.</span></span> <span data-ttu-id="6f5ee-147">For hver konto bestemmer indholdet af feltet **Konsol. oversættelsesmetode** valutakursen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-147">For each account, the content of the **Consol. Translation Method** field determines the exchange rate.</span></span> <span data-ttu-id="6f5ee-148">På hvert koncernvirksomhedskort angiver du i feltet **Valutakurstabel**, om konsolideringen skal bruge valutakurser fra koncernvirksomhedens regnskab eller det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-148">On each business unit card, in the **Currency Exchange Rate Table** field, you specify whether consolidation will use exchange rates from the business unit or the consolidated company.</span></span> <span data-ttu-id="6f5ee-149">Hvis du bruger valutakurser fra det konsoliderede regnskab, kan du ændre kurserne for en koncernvirksomhed.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-149">If you use exchange rates from the consolidated company, you can change the exchange rates for a business unit.</span></span> <span data-ttu-id="6f5ee-150">For koncernvirksomheder gælder: Hvis der i feltet **Valutakurstabel** på koncernvirksomhedskortet står **Lokal**, kan du ændre valutakursen fra koncernvirksomhedskortet.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-150">For business units, if the **Currency Exchange Rate Table** field on the business unit card contains **Local**, you can change the exchange rate from the business unit card.</span></span> <span data-ttu-id="6f5ee-151">Valutakurserne kopieres fra tabellen **Valutakurs**, men du kan ændre dem inden kosolideringen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-151">The exchange rates are copied from the **Currency Exchange Rate** table, but you can change them before consolidating.</span></span>

<span data-ttu-id="6f5ee-152">I følgende tabel beskrives de valutakursmetoder, du kan bruge til konti.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-152">The following table describes the exchange rate methods you can use for accounts.</span></span>

|<span data-ttu-id="6f5ee-153">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="6f5ee-153">Exchange rate</span></span> | <span data-ttu-id="6f5ee-154">Typisk anvendelse</span><span class="sxs-lookup"><span data-stu-id="6f5ee-154">Typical use</span></span> |
|---|---|
|<span data-ttu-id="6f5ee-155">Gennemsnitskurs (manuel)</span><span class="sxs-lookup"><span data-stu-id="6f5ee-155">Average Rate (Manual)</span></span> | <span data-ttu-id="6f5ee-156">Du kan manuelt beregne den gennemsnitlige kurs for konsolideringsperioden.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-156">You manually calculate the average rate for the period to consolidate.</span></span> <span data-ttu-id="6f5ee-157">Beregn enten gennemsnittet som et aritmetisk gennemsnit eller som et kvalificeret estimat, og angiv resultatet for hver koncernvirksomhed.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-157">Calculate the average either as an arithmetic average or as a best estimate, and specify the result for each business unit.</span></span> <span data-ttu-id="6f5ee-158">Bruges til resultatopgørelseskonti.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-158">Used for income statement accounts.</span></span>|
|<span data-ttu-id="6f5ee-159">Ultimokurs</span><span class="sxs-lookup"><span data-stu-id="6f5ee-159">Closing Rate</span></span> | <span data-ttu-id="6f5ee-160">Bruges til konti på balancen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-160">Used for balance sheet accounts.</span></span>|
|<span data-ttu-id="6f5ee-161">Sidste ultimokurs</span><span class="sxs-lookup"><span data-stu-id="6f5ee-161">Last Closing Rate</span></span> | <span data-ttu-id="6f5ee-162">Den gældende kurs på valutamarkedet på den dato, hvor balancen eller resultatopgørelsen udarbejdes.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-162">The rate that was valid in the foreign exchange market on the date for which the balance sheet or income statement is being prepared.</span></span> <span data-ttu-id="6f5ee-163">Angiv denne kurs for hver koncernvirksomhed.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-163">You enter this rate for each business unit.</span></span> <span data-ttu-id="6f5ee-164">Bruges til konti på balancen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-164">Used for balance sheet accounts.</span></span>|
|<span data-ttu-id="6f5ee-165">Historisk kurs</span><span class="sxs-lookup"><span data-stu-id="6f5ee-165">Historical Rate</span></span> | <span data-ttu-id="6f5ee-166">Den valutakurs, der var gældende, da transaktionen fandt sted.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-166">The exchange rate that was valid when the transaction occurred.</span></span>|
|<span data-ttu-id="6f5ee-167">Sammensat kurs</span><span class="sxs-lookup"><span data-stu-id="6f5ee-167">Composite Rate</span></span> | <span data-ttu-id="6f5ee-168">Beløbene i den aktuelle periode oversættes til gennemsnitskursen og føjes til den tidligere registrerede balance i det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-168">The current period amounts are translated at the average rate and added to the previously recorded balance in the consolidated company.</span></span> <span data-ttu-id="6f5ee-169">Denne metode bruges typisk til resultatkonti, fordi disse omfatter beløb overført fra forskellige perioder og derfor er sammensat af beløb, der er oversat med forskellige valutakurser.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-169">This method is typically used for retained earnings accounts because they include amounts from different periods and are therefore a composite of amounts translated with different exchange rates.</span></span>|
|<span data-ttu-id="6f5ee-170">Aktiekurs</span><span class="sxs-lookup"><span data-stu-id="6f5ee-170">Equity Rate</span></span> | <span data-ttu-id="6f5ee-171">Dette svarer til **sammensat**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-171">This is similar to **Composite**.</span></span> <span data-ttu-id="6f5ee-172">Differencerne bogføres på separate finanskonti.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-172">Differences are posted to separate general ledger accounts.</span></span>|   

<span data-ttu-id="6f5ee-173">Gør følgende for at angive valutakurser for koncernvirksomheder:</span><span class="sxs-lookup"><span data-stu-id="6f5ee-173">To specify exchange rates for business units, follow these steps:</span></span>

1. <span data-ttu-id="6f5ee-174">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncernvirksomheder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-174">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Business Units**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6f5ee-175">Vælg koncernvirksomheden på siden **Koncernvirksomhedsoversigt**, og vælg derefter handlingen **Gennemsnitskurs (manuel)**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-175">On the **Business Unit List** page, choose the business unit, and then choose the **Average Rate (Manual)** action.</span></span>   
3. <span data-ttu-id="6f5ee-176">På siden **Ret valutakurs** er indholdet af feltet **Associeret valutakurs** blevet kopieret fra tabellen **Valutakurs**, men du kan ændre oplysningerne efter behov.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-176">On the **Change Exchange Rate** page, the contents of the **Relational Exch. Rate** field have been copied from the **Currency Exchange Rate** table, but you can modify them.</span></span> <span data-ttu-id="6f5ee-177">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-177">Close the page.</span></span>  
4. <span data-ttu-id="6f5ee-178">Vælg handlingen **Ultimokurs**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-178">Choose the **Closing Rate** action.</span></span>  
5. <span data-ttu-id="6f5ee-179">I feltet **Associeret valutakursbeløb** skal du angive valutakursen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-179">In the **Relational Exch. Rate Amount** field, enter the exchange rate.</span></span>

<!-- ### To include or exclude dimensions

COMMENTING THIS OUT BECAUSE i CANNOT REPRODUCE THE SETTINGS. tHERE IS NO CONSOLIDATION CODE FIELD ON DIMENSIONS OR DIMENSIOIN VALUES.

You can consolidate dimension information and general ledger accounts, as follows:

* To exclude dimension information in the consolidation, leave the **Consolidation Code** field blank, and do not choose dimensions in the **Copy Dimensions** fields in any consolidation functions or reports described later in this topic.
* To include dimension information in the consolidation, leave the **Consolidation Code** field blank. However, the consolidation will only work if the dimension values in the business unit are the same as the consolidated company.
* To consolidate the dimension value code in the business unit with a different dimension value code in the consolidated company, fill in the **Consolidation Code**. -->

### <a name="to-exclude-a-company-from-consolidation"></a><span data-ttu-id="6f5ee-180">Sådan udelukkes en virksomhed fra konsolideringen</span><span class="sxs-lookup"><span data-stu-id="6f5ee-180">To exclude a company from consolidation</span></span>
<span data-ttu-id="6f5ee-181">Hvis du ikke vil medtage en koncernvirksomhed i konsolideringen, kan du udelukke den.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-181">If you do not want to include a business unit in the consolidation, you can exclude it.</span></span> <span data-ttu-id="6f5ee-182">Gå til koncernvirksomhedskortet for at gøre dette, og fjern markeringen af afkrydsningsfeltet **Konsolideres**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-182">To do that, go to the business unit card, and clear the **Consolidate** check box.</span></span>

### <a name="to-include-a-partially-owned-company-in-consolidation"></a><span data-ttu-id="6f5ee-183">Sådan inkluderes en delvis ejet virksomhed i konsolideringen</span><span class="sxs-lookup"><span data-stu-id="6f5ee-183">To include a partially-owned company in consolidation</span></span>
<span data-ttu-id="6f5ee-184">Hvis du kun ejer en del af en virksomhed, kan du medtage en procentdel af hver transaktion, der svarer til den procentdel af virksomheden, du ejer.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-184">If you own only part of a company, you can include a percentage of each transaction that corresponds to the percentage of the company you own.</span></span> <span data-ttu-id="6f5ee-185">Hvis du f.eks. ejer 70 % af virksomheden, inkluderer konsolideringen $70 af en faktura på $100.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-185">For example, if you own 70% of the company, consolidation will include $70 of an invoice for $100.</span></span> <span data-ttu-id="6f5ee-186">Du angiver den procentdel af virksomheden, du ejer, ved at gå til koncernvirksomhedskortet og angive procentdelen i feltet **Konsolideringspct.**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-186">To specify the percentage of the company you own, go to the business unit card, and enter the percentage in the **Consolidation %** field.</span></span>  

### <a name="to-test-the-data-before-you-consolidate"></a><span data-ttu-id="6f5ee-187">Sådan kontrolleres dataene, før du konsoliderer</span><span class="sxs-lookup"><span data-stu-id="6f5ee-187">To test the data before you consolidate</span></span>
<span data-ttu-id="6f5ee-188">Du kan teste dataene, inden du overfører dem til det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-188">You can test your data before you transfer it to the consolidated company.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6f5ee-189"> kontrollerer, om der er forskelle mellem oplysningerne i koncernvirksomhederne og den konsoliderede virksomhed.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-189"> looks for differences in the information in the business units and the consolidated company.</span></span> <span data-ttu-id="6f5ee-190">F.eks., om kontonumre eller dimensionskoder er anderledes.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-190">For example, whether account numbers or dimension codes are different.</span></span> <span data-ttu-id="6f5ee-191">Du skal rette fejlene, før du kan køre rapporten.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-191">You must correct errors before you can run the report.</span></span> <span data-ttu-id="6f5ee-192">Du kan teste databasen, eller hvis du importerer data fra en XML-fil, kan du teste filen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-192">You can test the database or, if you are importing data from an XML file, you can test the file.</span></span>   

1. <span data-ttu-id="6f5ee-193">Åbn det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-193">Open the consolidated company.</span></span>  
2. <span data-ttu-id="6f5ee-194">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncernvirksomheder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-194">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Business Units**, and then choose the related link.</span></span>  
3. <span data-ttu-id="6f5ee-195">Gør ét af følgende:</span><span class="sxs-lookup"><span data-stu-id="6f5ee-195">Do one of the following:</span></span>  

    * <span data-ttu-id="6f5ee-196">For at teste en fil, skal du vælge handlingen **Kontroller fil**, angive navnet på filen, der skal kontrollere, og derefter vælge **Udskriv**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-196">To test a file, choose the **Test File** action, enter the name of the file to test, and then choose **Print**.</span></span>  
    * <span data-ttu-id="6f5ee-197">Du kan teste databasen ved at vælge **Test database**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-197">To test the database, choose **Test Database**.</span></span>  

## <a name="to-run-the-consolidation"></a><span data-ttu-id="6f5ee-198">Så køres konsolideringen</span><span class="sxs-lookup"><span data-stu-id="6f5ee-198">To run the consolidation</span></span>
<span data-ttu-id="6f5ee-199">Når du har testet dataene, kan du overføre dem til det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-199">After you have tested the data, you can transfer it to the consolidated company.</span></span>  

1. <span data-ttu-id="6f5ee-200">Log på det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-200">Sign in to the consolidated company.</span></span>  
2. <span data-ttu-id="6f5ee-201">I **Rollecenteret Bogholder** skal du vælge handlingen **Kør konsolidering**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-201">On the **Accountant Role Center**, choose the **Run Consolidation** action.</span></span>  
3. <span data-ttu-id="6f5ee-202">Udfyld de påkrævede felter.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-202">Fill in the required fields.</span></span>  
4. <span data-ttu-id="6f5ee-203">I feltet **Hvor** skal du vælge **Virksomhedsnavn** og derefter vælge det konsoliderede regnskab i feltet **er**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-203">In the **Where** field, choose **Company Name**, and then choose the consolidated company in the **is** field.</span></span>  

## <a name="to-export-data-from-dynamics-nav-and-import-it-in-included365finincludesd365finmdmd"></a><span data-ttu-id="6f5ee-204">Sådan eksporteres data fra Dynamics NAV og importeres i [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="6f5ee-204">To export data from Dynamics NAV and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="6f5ee-205">Hvis data for en koncernvirksomhed er placeret i en anden database, skal du eksportere dataene til en fil, før de kan medtages i konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-205">If data for a business unit is in another database, you must export the data to a file before you can include it in the consolidation.</span></span> <span data-ttu-id="6f5ee-206">Regnskaberne skal udlæses separat.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-206">Each company must be exported separately.</span></span> <span data-ttu-id="6f5ee-207">Til det formål bruges kørslen **Udlæs konsolideringsposter**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-207">For this purpose, use the **Export Consolidation** batch job.</span></span>  

<span data-ttu-id="6f5ee-208">Når du kører batchjobbet, behandles alle poster i finanskonti.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-208">After you run the batch job, all entries in general ledger accounts are processed.</span></span> <span data-ttu-id="6f5ee-209">Indhold i felterne **Beløb** sammentælles og udlæses for hver kombination af valgte dimensioner og dato.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-209">For every combination of selected dimensions and date, the contents of the entries' **Amount** fields are totaled and exported.</span></span> <span data-ttu-id="6f5ee-210">Den næste kombination af valgte dimensioner og dato med samme kontonummer behandles, og derefter behandles kombinationerne i næste kontonummer osv.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-210">The next combination of selected dimensions and date with the same account number is processed, then the combinations in the next account number are processed, and so on.</span></span>  

<span data-ttu-id="6f5ee-211">De udlæste poster indeholder følgende felter: **Kontonr.**, **Bogføringsdato** og **Beløb**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-211">The exported entries contain the following fields: **Account No.**, **Posting Date**, and **Amount**.</span></span> <span data-ttu-id="6f5ee-212">Hvis dimensionsoplysningerne også blev eksporteret, medtages dimensionskoderne og dimensionsværdierne også.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-212">If dimensions information was also exported, dimension codes and dimension values are also included.</span></span>  

1. <span data-ttu-id="6f5ee-213">For hver eksporteret linje, hvis summen af **Beløb**-felterne er et debetbeløb, eksporteres det kontonummer , der er oprettet i koncernvirksomhedens felt **Kons.debetkonto** til linjen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-213">For each exported line, if the total of the **Amount** fields is a debit, the account number that is set up in the business unit's **Consol. Debit Acc.** field is exported to the line.</span></span> <span data-ttu-id="6f5ee-214">Hvis summen er et kreditbeløb, eksporteres det tilsvarende tal i feltet **Kons.kreditkonto** til linjen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-214">If the total is a credit, the corresponding number in the **Consol. Credit Acc.** field is exported to the line.</span></span>  
2. <span data-ttu-id="6f5ee-215">Den dato, der bruges til de udlæste linjer er enten periodens slutdato, eller også er det den nøjagtige dato for beregningen, hvis overførslen finder sted pr. dag.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-215">The date used for each exported line is either the period's ending date or, if the transfer occurs each day, the exact date of the calculation.</span></span>  
3. <span data-ttu-id="6f5ee-216">Den dimensionsværdi, der blev udlæst for posten, vil blive det konsoliderede regnskabs dimensionsværdi, som er oprettet i feltet **Konsolideringskode** for dimensionsværdien.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-216">The dimension value exported for the entry will be the consolidated company dimension value that is set up in the **Consolidation Code** field for that dimension value.</span></span> <span data-ttu-id="6f5ee-217">Hvis der ikke er blevet oprettet en dimensionsværdi for det konsoliderede regnskab i feltet **Konsolideringskode** for dimensionsværdien, vil selve dimensionsværdien blive udlæst til linjen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-217">If no consolidated company dimension value has been entered in the **Consolidated Code** field for that dimension value, the dimension value itself will be exported to the line.</span></span>   
4. <span data-ttu-id="6f5ee-218">XML-filerne indeholder også valutakurserne i konsolideringsperioden.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-218">The XML files also contain the currency exchange rates in the consolidation period.</span></span> <span data-ttu-id="6f5ee-219">Disse kurser er inkluderet i en separat sektion øverst i filen.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-219">These rates are included in a separate section at the beginning of the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f5ee-220">Se også</span><span class="sxs-lookup"><span data-stu-id="6f5ee-220">See Also</span></span>
<span data-ttu-id="6f5ee-221">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6f5ee-221">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="6f5ee-222">Eksportere forretningsdata til Excel</span><span class="sxs-lookup"><span data-stu-id="6f5ee-222">Exporting Your Business Data to Excel</span></span>](about-export-data.md)
