---
title: Bogføringsdato på værdiposter
description: Få mere at vide, hvordan kørslen Juster kostpris - vareposter identificerer og tildeler en posteringsdato til de værdiposter, der er ved at blive oprettet.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: b08864a4cf7f7f198d692a6658ae437856860a51
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247555"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="7f6f3-103">Designoplysninger: Bogføringsdato på post med reguleringsværdi</span><span class="sxs-lookup"><span data-stu-id="7f6f3-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="7f6f3-104">Denne artikel indeholder en vejledning til brugere af funktionen Lagerkostmetode i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7f6f3-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7f6f3-105">Denne specifikke artikel giver en vejledning i, hvordan kørslen **Juster kostpris - vareposter** identificerer og tildeler en bogføringsdato til de værdiposter, der er ved at blive oprettet.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="7f6f3-106">Først gennemgås konceptet i processen, hvordan kørslen identificerer og tildeler en bogføringsdato til den værdipost, der er ved at blive oprettet.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="7f6f3-107">Derefter beskrives nogle scenarier, som vi i supportteamet støder på fra tid til anden, og endelig vises der en oversigt over de begreber, der er brugt fra version 3.0.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used from version 3.0.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="7f6f3-108">Konceptet</span><span class="sxs-lookup"><span data-stu-id="7f6f3-108">The Concept</span></span>  
<span data-ttu-id="7f6f3-109">Fra version 5.0 tildeler kørslen **Reguler kostværdi – vareposter** en bogføringsdato til den værdipost, der er ved at blive oprettet i følgende trin:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-109">From version 5.0, the **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="7f6f3-110">Først har bogføringsdatoen for posten, der skal oprettes, den samme dato som den post, den regulerer.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="7f6f3-111">Bogføringsdatoen valideres op mod lagerperioder og/eller Opsætning af Finans.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="7f6f3-112">Tildeling af bogføringsdato. Hvis den oprindelige bogføringsdato ikke er inden for det tilladte datointerval for posteringen, tildeler kørslen en tilladt bogføringsdato fra Opsætning af Finans eller lagerperiode.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="7f6f3-113">Hvis både lagerperioder og tilladte bogføringsdatoer i Opsætning af Finans er defineret, så er det den seneste dato af de to, der tildeles til posten med reguleringsværdien.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="7f6f3-114">Lad os gennemgå processen mere i praksis.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="7f6f3-115">Antag, at vi har en varepost for varesalg.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="7f6f3-116">Varen blev leveret på den 5. september 2013, og den blev faktureret dagen efter.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-116">The item was shipped on September 5th, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="7f6f3-117">![Tilstand for vareposter i scenariet](media/helene/TechArticleAdjustcost1.png "Tilstand for vareposter i scenariet")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-117">![State of item ledger entries in the scenario](media/helene/TechArticleAdjustcost1.png "State of item ledger entries in the scenario")</span></span>  

<span data-ttu-id="7f6f3-118">Nedenfor repræsenterer den første værdipost (379) forsendelsen og har den samme bogføringsdato som den overordnede varepost.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="7f6f3-119">Den anden værdipost (381) repræsenterer fakturaen.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="7f6f3-120">Den tredje værdipost (391) er en justering af faktureringsværdiposten (381)</span><span class="sxs-lookup"><span data-stu-id="7f6f3-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="7f6f3-121">![Tilstand for værdiposter i scenariet](media/helene/TechArticleAdjustcost2.png "Tilstand for værdiposter i scenariet")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-121">![State of value entries in the scenario](media/helene/TechArticleAdjustcost2.png "State of value entries in the scenario")</span></span>  

 <span data-ttu-id="7f6f3-122">Trin 1: Reguleringsværdiposten, der skal oprettes, er knyttet til samme bogføringsdato, som den post, den justerer, illustreret ovenfor af værdipost 391.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="7f6f3-123">Trin 2: Validering af oprindelig tildelt bogføringsdato.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="7f6f3-124">Kørslen **Juster kostpris - vareposter** bestemmer, om den første bogføringsdato for reguleringsværdiposten er inden for det tilladte bogføringsdatointerval, der er baseret på lagerperioder og/eller Opsætning af Finans.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="7f6f3-125">Lad os gennemgå ovennævnte salg ved at tilføje opsætningen af tilladte bogføringsdatointervaller.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="7f6f3-126">Lagerperioder:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-126">Inventory Periods:</span></span>  

<span data-ttu-id="7f6f3-127">![Lagerperioder i scenariet](media/helene/TechArticleAdjustcost3.png "Lagerperioder i scenariet")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-127">![Inventory periods in the scenario](media/helene/TechArticleAdjustcost3.png "Inventory periods in the scenario")</span></span>

 <span data-ttu-id="7f6f3-128">Den først tilladte bogføringsdato er den første dag i den første åbne periode.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="7f6f3-129">1. september 2013.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-129">September 1st, 2013.</span></span>  

 <span data-ttu-id="7f6f3-130">Opsætning af Finans:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-130">General Ledger Setup:</span></span>  

<span data-ttu-id="7f6f3-131">![Regnskabsopsætning i scenariet](media/helene/TechArticleAdjustcost4.png "Regnskabsopsætning i scenariet")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-131">![G/L Setup in the scenario](media/helene/TechArticleAdjustcost4.png "G/L Setup in the scenario")</span></span>

 <span data-ttu-id="7f6f3-132">Første tilladte bogføringsdato er den dato, der er angivet i feltet Tillad bogføring fra: 10. september 2013.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-132">First allowed posting date is the date stated in field Allow Posting From: September 10th, 2013.</span></span>  

 <span data-ttu-id="7f6f3-133">Hvis både lagerperioder og tilladte bogføringsdatoer i Opsætning af Finans er defineret, så er det den seneste dato af de to, der definerer det tilladte bogføringsdatointerval.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="7f6f3-134">Trin 3: Tildeling af en tilladt bogføringsdato.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="7f6f3-135">Den oprindeligt tildelt bogføringsdato er 6. september, som vist i trin 1.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-135">The initial assigned Posting Date was September 6th as illustrated in step 1.</span></span> <span data-ttu-id="7f6f3-136">Men i 2. trin identificerer kørslen Juster kostpris - vareposter, at den tidligst tilladte bogføringsdato er 10. september, og dermed tildeles 10. september til 10 reguleringsværdiposten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-136">However, in the 2nd step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10th and thereby assigns September 10th to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="7f6f3-137">![Tilstand for værdiposter i scenarie 2](media/helene/TechArticleAdjustcost5.png "Tilstand for værdiposter i scenarie 2")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-137">![State of value entries in the scenario 2](media/helene/TechArticleAdjustcost5.png "State of value entries in the scenario 2")</span></span>

 <span data-ttu-id="7f6f3-138">Vi har nu gennemgået konceptet for tildeling af bogføringsdatoer til værdiposter, der er oprettet af kørslen Juster kostpris - vareposter.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="7f6f3-139">Lad os fortsætte med at gennemse nogle scenarier, som vi i supportteamet støder på fra tid til anden i forbindelse med tilknyttede bogføringsdatoer i kørslen Juster kostpris – vareposter og de relaterede opsætninger.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="7f6f3-140">Eksempler</span><span class="sxs-lookup"><span data-stu-id="7f6f3-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="7f6f3-141">Scenarie I: "Bogføringsdatoen er ikke inden for intervallet af tilladte bogføringsdatoer..."</span><span class="sxs-lookup"><span data-stu-id="7f6f3-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="7f6f3-142">Dette er en scenarie, hvor en bruger får vist den nævnte fejlmeddelelse, under kørsel af Juster kostpris - vareposter.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="7f6f3-143">I det foregående afsnit, der beskriver konceptet med tildeling af bogføringsdatoer, var formålet med kørslen Juster kostpris - vareposter at oprette en værdipost med bogføringsdatoen 10. september.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="7f6f3-144">![Fejlmeddelelse om bogføringsdato](media/helene/TechArticleAdjustcost6.png "Fejlmeddelelse om bogføringsdato")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-144">![Error message about posting date](media/helene/TechArticleAdjustcost6.png "Error message about posting date")</span></span>

 <span data-ttu-id="7f6f3-145">Vi følger op på brugeropsætningen:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="7f6f3-146">![Brugerens tilladte opsætning af bogføringsdatoer](media/helene/TechArticleAdjustcost7.png "Brugerens tilladte opsætning af bogføringsdatoer")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-146">![User's allowed posting dates setup](media/helene/TechArticleAdjustcost7.png "User's allowed posting dates setup")</span></span>

 <span data-ttu-id="7f6f3-147">Brugeren har i dette tilfælde et tilladt bogføringsdatointerval fra 11. september til 30. september og må derfor ikke bogføre reguleringsværdiposten med bogføringsdatoen 10. september.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-147">The user in this case has an allowed posting date range from September 11th to September 30th and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="7f6f3-148">![Oversigt over opsætning af involveret bogføringsdato](media/helene/TechArticleAdjustcost8.png "Oversigt over opsætning af involveret bogføringsdato")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-148">![Overview of involved posting date setup](media/helene/TechArticleAdjustcost8.png "Overview of involved posting date setup")</span></span>

 <span data-ttu-id="7f6f3-149">Vidensbaseartikel [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) beskriver yderligere scenarier, der er relateret til nævnte fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses additional scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="7f6f3-150">Scenarie II: Bogføringsdato på reguleringsværdipost og bogføringsdatoen på post, der forårsager reguleringen, f.eks. værdiregulering eller varegebyr.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="7f6f3-151">Værdireguleringsscenarie:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="7f6f3-152">Forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-152">Prerequisites:</span></span>  

 <span data-ttu-id="7f6f3-153">Opsætning af lager:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-153">Inventory setup:</span></span>  

-   <span data-ttu-id="7f6f3-154">Aut. lagerværdibogføring = Ja</span><span class="sxs-lookup"><span data-stu-id="7f6f3-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="7f6f3-155">Automatisk kostregulering = Altid</span><span class="sxs-lookup"><span data-stu-id="7f6f3-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="7f6f3-156">Beregn.type for gnsn. kostpris = Vare</span><span class="sxs-lookup"><span data-stu-id="7f6f3-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="7f6f3-157">Gennemsnitlig omkostningsperiode = Dag</span><span class="sxs-lookup"><span data-stu-id="7f6f3-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="7f6f3-158">Opsætning af Finans:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="7f6f3-159">Bogf. tilladt fra = 1. januar 2014</span><span class="sxs-lookup"><span data-stu-id="7f6f3-159">Allow Posting From = January 1st, 2014</span></span>  

-   <span data-ttu-id="7f6f3-160">Bogf. tilladt til = tom</span><span class="sxs-lookup"><span data-stu-id="7f6f3-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="7f6f3-161">Brugeropsætning:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-161">User Setup:</span></span>  

-   <span data-ttu-id="7f6f3-162">Bogf. tilladt fra = 1. december 2013</span><span class="sxs-lookup"><span data-stu-id="7f6f3-162">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="7f6f3-163">Bogf. tilladt til = tom</span><span class="sxs-lookup"><span data-stu-id="7f6f3-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="7f6f3-164">Sådan testes scenariet</span><span class="sxs-lookup"><span data-stu-id="7f6f3-164">To test the scenario</span></span>  

1.  <span data-ttu-id="7f6f3-165">Opret varen TEST:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-165">Create item TEST:</span></span>  

     <span data-ttu-id="7f6f3-166">Basisenhed = STK</span><span class="sxs-lookup"><span data-stu-id="7f6f3-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="7f6f3-167">Kostmetode = Gennemsnit</span><span class="sxs-lookup"><span data-stu-id="7f6f3-167">Costing Method = Average</span></span>  

     <span data-ttu-id="7f6f3-168">Vælg valgfrie bogføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="7f6f3-169">Åbn varekladden, opret og bogfør en linje på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-169">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="7f6f3-170">Bogføringsdato = 15. december 2013</span><span class="sxs-lookup"><span data-stu-id="7f6f3-170">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="7f6f3-171">Vare = TEST</span><span class="sxs-lookup"><span data-stu-id="7f6f3-171">Item = TEST</span></span>  

     <span data-ttu-id="7f6f3-172">Posttype = Køb</span><span class="sxs-lookup"><span data-stu-id="7f6f3-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="7f6f3-173">Antal = 100</span><span class="sxs-lookup"><span data-stu-id="7f6f3-173">Quantity = 100</span></span>  

     <span data-ttu-id="7f6f3-174">Pris = 10</span><span class="sxs-lookup"><span data-stu-id="7f6f3-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="7f6f3-175">Åbn varekladden, opret og bogfør en linje på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-175">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="7f6f3-176">Dato = 20 December 2013</span><span class="sxs-lookup"><span data-stu-id="7f6f3-176">Date = December 20th, 2013</span></span>  

     <span data-ttu-id="7f6f3-177">Vare = TEST</span><span class="sxs-lookup"><span data-stu-id="7f6f3-177">Item = TEST</span></span>  

     <span data-ttu-id="7f6f3-178">Posttype = Nedregulering</span><span class="sxs-lookup"><span data-stu-id="7f6f3-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="7f6f3-179">Antal = 2</span><span class="sxs-lookup"><span data-stu-id="7f6f3-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="7f6f3-180">Åbn varekladden, opret og bogfør en linje på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-180">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="7f6f3-181">Dato = 15. januar 2014</span><span class="sxs-lookup"><span data-stu-id="7f6f3-181">Date = January 15th, 2014</span></span>  

     <span data-ttu-id="7f6f3-182">Vare = TEST</span><span class="sxs-lookup"><span data-stu-id="7f6f3-182">Item = TEST</span></span>  

     <span data-ttu-id="7f6f3-183">Posttype = Nedregulering</span><span class="sxs-lookup"><span data-stu-id="7f6f3-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="7f6f3-184">Antal = 3</span><span class="sxs-lookup"><span data-stu-id="7f6f3-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="7f6f3-185">Åbn værdireguleringskladden, opret og bogfør en linje på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-185">Open Revaluation Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="7f6f3-186">Vare = TEST</span><span class="sxs-lookup"><span data-stu-id="7f6f3-186">Item = TEST</span></span>  

     <span data-ttu-id="7f6f3-187">Udligningspost = Vælg købspost, der er bogført i trin 2.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="7f6f3-188">Bogføringsdatoen for værdireguleringen er den samme som for den post, den regulerer.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="7f6f3-189">Kostpris (reguleret) = 40</span><span class="sxs-lookup"><span data-stu-id="7f6f3-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="7f6f3-190">Følgende vare- og værdiposter er bogført:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="7f6f3-191">![Oversigt over resulterende vareposter og -værdier 1](media/helene/TechArticleAdjustcost9.png "Oversigt over resulterende vareposter og -værdier 1")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-191">![Overview of resulting item ledger and value entries 1](media/helene/TechArticleAdjustcost9.png "Overview of resulting item ledger and value entries 1")</span></span>

 <span data-ttu-id="7f6f3-192">![Oversigt over resulterende vareposter og -værdier 2](media/helene/TechArticleAdjustcost10.png "Oversigt over resulterende vareposter og -værdier 2")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-192">![Overview of resulting item ledger and value entries 2](media/helene/TechArticleAdjustcost10.png "Overview of resulting item ledger and value entries 2")</span></span>

 <span data-ttu-id="7f6f3-193">Kørslen Juster kostpris - vareposter har registreret en ændring i kostprisen og har justeret de negative reguleringer.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="7f6f3-194">**Gennemgang af bogføringsdatoer på oprettede poster med reguleringsværdier:** Den tidligst tilladte bogføringsdato, som kørslen Juster kostpris - vareposter skal forholde sig til, er 1. januar 2014 som angivet i Opsætning af Finans.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1st, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="7f6f3-195">**Negativ regulering i trin 3:** den tildelte bogføringsdato er 1. januar fra Opsætning af Finans.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1st, provided by General Ledger Setup.</span></span> <span data-ttu-id="7f6f3-196">Bogføringsdatoen for værdiposten i området til regulering er 20. december 2013.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="7f6f3-197">I henhold til Opsætning af Finans er datoen ikke inden for det tilladte bogføringsdatointerval.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-197">According to General Ledger Setup the date is not within allowed posting date range.</span></span> <span data-ttu-id="7f6f3-198">Derfor tildeles den bogføringsdato, der er angivet i feltet Bogf. tilladt fra i Opsætning af Finans, til værdireguleringsposten.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="7f6f3-199">**Negativ regulering i trin 4:** den tildelte bogføringsdato er 15. januar.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15th.</span></span> <span data-ttu-id="7f6f3-200">Værdiposten i reguleringen har bogføringsdatoen 15. januar, som er inden for det tilladte bogføringsdatointerval i henhold til Opsætning af Finans.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-200">The Value Entry in scope of adjustment has Posting Date January 15th, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="7f6f3-201">Reguleringen, der er foretaget for nedreguleringen i trin 3 giver problemer.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="7f6f3-202">Den favorable bogføringsdato for værdireguleringsposten ville have været 20. december eller i det mindste i december, da værdireguleringen som medfører ændringen i vareforbruget blev bogført i december.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20th or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="7f6f3-203">For at opnå regulering i december af nedreguleringen i trin 3, skal Opsætning af Finans i feltet Bogf. tilladt fra angive en dato i december.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="7f6f3-204">**Konklusion:**</span><span class="sxs-lookup"><span data-stu-id="7f6f3-204">**Conclusion:**</span></span>  

 <span data-ttu-id="7f6f3-205">Med oplevelserne fra dette scenarie, hvor vi overvejer den mest velegnede opsætning af tilladt bogføringsdatointerval for en virksomhed, kan følgende være nyttigt: Så længe ændringer i lagerværdien må bogføres i en periode, december i det tilfælde, skal den opsætning, virksomheden bruger til tilladte bogføringsdatointervaller, justeres i forhold til beslutningen.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, the following might be useful: As long as changes in inventory value is allowed to be posted in a period, December in this case, the setup the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="7f6f3-206">Bogf. tilladt fra i Opsætning af Finans angiver 1. december, og det tillader at, værdireguleringen foretaget i december kan sendes til berørte udgående poster i samme periode.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-206">The Allow Posting From in the General Ledger Setup, stating December 1st  would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="7f6f3-207">Brugergrupper, der ikke må bogføre i december, men i januar, hvilket sandsynligvis var beregnet til at være begrænset af Opsætning af Finans i dette scenarie, skal i stedet behandles via Brugeropsætning.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="7f6f3-208">Scenarie med varegebyr:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-208">Item charge scenario:</span></span>  
 <span data-ttu-id="7f6f3-209">Forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-209">Prerequisites:</span></span>  

 <span data-ttu-id="7f6f3-210">Opsætning af lager:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-210">Inventory setup:</span></span>  

-   <span data-ttu-id="7f6f3-211">Aut. lagerværdibogføring = Ja</span><span class="sxs-lookup"><span data-stu-id="7f6f3-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="7f6f3-212">Automatisk kostregulering = Altid</span><span class="sxs-lookup"><span data-stu-id="7f6f3-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="7f6f3-213">Beregn.type for gnsn. kostpris = Vare</span><span class="sxs-lookup"><span data-stu-id="7f6f3-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="7f6f3-214">Gennemsnitlig omkostningsperiode = Dag</span><span class="sxs-lookup"><span data-stu-id="7f6f3-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="7f6f3-215">Opsætning af Finans:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="7f6f3-216">Bogf. tilladt fra = 1. december 2013</span><span class="sxs-lookup"><span data-stu-id="7f6f3-216">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="7f6f3-217">Bogf. tilladt til = tom</span><span class="sxs-lookup"><span data-stu-id="7f6f3-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="7f6f3-218">Brugeropsætning:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-218">User Setup:</span></span>  

-   <span data-ttu-id="7f6f3-219">Bogf. tilladt fra = 1. december 2013</span><span class="sxs-lookup"><span data-stu-id="7f6f3-219">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="7f6f3-220">Bogf. tilladt til = tom</span><span class="sxs-lookup"><span data-stu-id="7f6f3-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="7f6f3-221">Sådan testes scenariet</span><span class="sxs-lookup"><span data-stu-id="7f6f3-221">To test the scenario</span></span>  

1.  <span data-ttu-id="7f6f3-222">Opret varegebyr:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-222">Create item charge:</span></span>  

     <span data-ttu-id="7f6f3-223">Basisenhed = STK</span><span class="sxs-lookup"><span data-stu-id="7f6f3-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="7f6f3-224">Kostmetode = Gennemsnit</span><span class="sxs-lookup"><span data-stu-id="7f6f3-224">Costing Method = Average</span></span>  

     <span data-ttu-id="7f6f3-225">Vælg valgfrie bogføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="7f6f3-226">Opret en ny købsordre</span><span class="sxs-lookup"><span data-stu-id="7f6f3-226">Create new purchase order</span></span>  

     <span data-ttu-id="7f6f3-227">Leverandørnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="7f6f3-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="7f6f3-228">Bogføringsdato = 15. december 2013</span><span class="sxs-lookup"><span data-stu-id="7f6f3-228">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="7f6f3-229">Kreditors fakturanr.: 1234</span><span class="sxs-lookup"><span data-stu-id="7f6f3-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="7f6f3-230">På købsordrelinje:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-230">On the purchase order line:</span></span>  

     <span data-ttu-id="7f6f3-231">Vare = GEBYR</span><span class="sxs-lookup"><span data-stu-id="7f6f3-231">Item = CHARGE</span></span>  

     <span data-ttu-id="7f6f3-232">Antal = 1</span><span class="sxs-lookup"><span data-stu-id="7f6f3-232">Quantity = 1</span></span>  

     <span data-ttu-id="7f6f3-233">Købspris = 100</span><span class="sxs-lookup"><span data-stu-id="7f6f3-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="7f6f3-234">Bogfør modtagelse og faktura.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="7f6f3-235">Opret en ny salgsordre:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-235">Create new sales order:</span></span>  

     <span data-ttu-id="7f6f3-236">Kundenr.: 10000</span><span class="sxs-lookup"><span data-stu-id="7f6f3-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="7f6f3-237">Bogføringsdato = 16. december 2013</span><span class="sxs-lookup"><span data-stu-id="7f6f3-237">Posting Date = December 16th, 2013</span></span>  

     <span data-ttu-id="7f6f3-238">På salgsordrelinjen:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-238">On the sales order line:</span></span>  

     <span data-ttu-id="7f6f3-239">Vare = GEBYR</span><span class="sxs-lookup"><span data-stu-id="7f6f3-239">Item = CHARGE</span></span>  

     <span data-ttu-id="7f6f3-240">Antal = 1</span><span class="sxs-lookup"><span data-stu-id="7f6f3-240">Quantity = 1</span></span>  

     <span data-ttu-id="7f6f3-241">Salgspris = 135</span><span class="sxs-lookup"><span data-stu-id="7f6f3-241">Unit Price = 135</span></span>  

     <span data-ttu-id="7f6f3-242">Bogfør levering og faktura.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="7f6f3-243">Opsætning af Finans:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="7f6f3-244">Bogf. tilladt fra = 1. januar 2014</span><span class="sxs-lookup"><span data-stu-id="7f6f3-244">Allow Posting From = January 1st, 2014</span></span>  

     <span data-ttu-id="7f6f3-245">Bogf. tilladt til = tom</span><span class="sxs-lookup"><span data-stu-id="7f6f3-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="7f6f3-246">Opret en ny købsordre:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-246">Create new purchase order:</span></span>  

     <span data-ttu-id="7f6f3-247">Leverandørnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="7f6f3-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="7f6f3-248">Bogføringsdato = 2. januar 2014</span><span class="sxs-lookup"><span data-stu-id="7f6f3-248">Posting Date = January 2nd, 2014</span></span>  

     <span data-ttu-id="7f6f3-249">Kreditors fakturanr.: 2345</span><span class="sxs-lookup"><span data-stu-id="7f6f3-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="7f6f3-250">På købsordrelinje:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-250">On the purchase order line:</span></span>  

     <span data-ttu-id="7f6f3-251">Varegebyr = JB-FRAGT</span><span class="sxs-lookup"><span data-stu-id="7f6f3-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="7f6f3-252">Antal = 1</span><span class="sxs-lookup"><span data-stu-id="7f6f3-252">Quantity = 1</span></span>  

     <span data-ttu-id="7f6f3-253">Købspris = 3</span><span class="sxs-lookup"><span data-stu-id="7f6f3-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="7f6f3-254">Tildele varegebyrer til købsleverance fra trin 2.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="7f6f3-255">Bogfør modtagelse og faktura.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="7f6f3-256">![Oversigt over resulterende vareposter og -værdier 3](media/helene/TechArticleAdjustcost11.png "Oversigt over resulterende vareposter og -værdier 3")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-256">![Overview of resulting item ledger and value entries 3](media/helene/TechArticleAdjustcost11.png "Overview of resulting item ledger and value entries 3")</span></span>

6.  <span data-ttu-id="7f6f3-257">På arbejdsdatoen 3. januar ankommer en købsfaktura, der indeholder et ekstra varegebyr for købet, der er oprettet i trin 2.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-257">On work date January 3rd a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="7f6f3-258">Fakturaen er dateret 30. december og bogføres derfor med bogføringsdato 30. december 2013.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-258">This invoice has document date December 30th and is therefore posted with Posting Date December 30th, 2013.</span></span>  

     <span data-ttu-id="7f6f3-259">Opret en ny købsordre:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-259">Create new purchase order:</span></span>  

     <span data-ttu-id="7f6f3-260">Leverandørnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="7f6f3-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="7f6f3-261">Bogføringsdato = 30. december 2013</span><span class="sxs-lookup"><span data-stu-id="7f6f3-261">Posting Date = December 30th, 2013</span></span>  

     <span data-ttu-id="7f6f3-262">Kreditors fakturanr.: 3456</span><span class="sxs-lookup"><span data-stu-id="7f6f3-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="7f6f3-263">På købsordrelinje:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-263">On the purchase order line:</span></span>  

     <span data-ttu-id="7f6f3-264">Varegebyr = JB-FRAGT</span><span class="sxs-lookup"><span data-stu-id="7f6f3-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="7f6f3-265">Antal = 1</span><span class="sxs-lookup"><span data-stu-id="7f6f3-265">Quantity = 1</span></span>  

     <span data-ttu-id="7f6f3-266">Købspris = 2</span><span class="sxs-lookup"><span data-stu-id="7f6f3-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="7f6f3-267">Tildele varegebyrer til købsleverance fra trin 2</span><span class="sxs-lookup"><span data-stu-id="7f6f3-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="7f6f3-268">Bogfør modtagelse og faktura.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="7f6f3-269">![Oversigt over resulterende vareposter og -værdier 4](media/helene/TechArticleAdjustcost12.png "Oversigt over resulterende vareposter og -værdier 4")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-269">![Overview of resulting item ledger and value entries 4](media/helene/TechArticleAdjustcost12.png "Overview of resulting item ledger and value entries 4")</span></span>

 <span data-ttu-id="7f6f3-270">Lageropgørelsesrapporten udskrives pr. dato 31. december 2013</span><span class="sxs-lookup"><span data-stu-id="7f6f3-270">Inventory Valuation report is printed as of Date December 31st , 2013</span></span>  

<span data-ttu-id="7f6f3-271">![Indhold i rapporten Lagerværdi](media/helene/TechArticleAdjustcost13.png "Indhold i rapporten Lagerværdi")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-271">![Content of the Inventory Valuation report](media/helene/TechArticleAdjustcost13.png "Content of the Inventory Valuation report")</span></span>

 <span data-ttu-id="7f6f3-272">**Oversigt over scenarie:**</span><span class="sxs-lookup"><span data-stu-id="7f6f3-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="7f6f3-273">Det beskrevne scenarie afsluttes med rapporten Lagerværdi, der viser Antal = 0, mens værdien = 2.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="7f6f3-274">Varegebyret, der er bogført i trin 11, er en del af lagerforøgelsesværdien i december, mens lagerfaldet i samme periode ikke påvirkes.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="7f6f3-275">Det var godt for det første varegebyr, at Opsætning af Finans angav Bogf. tilladt fra 1. januar.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-275">Having the General Ledger Setup stating Allow Posting From January 1st was a good thing for the first Item charge.</span></span> <span data-ttu-id="7f6f3-276">Omkostningerne til lagerforøgelse og -fald blev registreret i samme periode.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="7f6f3-277">For anden varegebyret medfører Opsætning af Finans dog, at ændringen i vareforbrug registreres i perioden efter.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="7f6f3-278">**Konklusion:**</span><span class="sxs-lookup"><span data-stu-id="7f6f3-278">**Conclusion:**</span></span>  

 <span data-ttu-id="7f6f3-279">Det er en udfordring, at rapporten Lagerværdi viser antal = 0, mens værdien er <> 0.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="7f6f3-280">I dette tilfælde er det også sværere at angive de optimale indstillinger, da købsfakturaer ankommer den samme dag, men drejer sig om forskellige perioder eller endda regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="7f6f3-281">Overgangen til et nyt regnskabsår kræver som regel nogen planlægning, og som en del af denne indsigt, skal processen Juster kostpris - vareposter, der genkender vareforbrug, tages i betragtning.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="7f6f3-282">I dette scenarie kunne det være en mulighed at lade feltet Bogf. tilladt fra i Opsætning af Finans angive en dato i december i et par dage til, og lade bogføringen af det første varegebyr vente for at tillade, at alle omkostninger fra den forrige periode/det forrige regnskabsår blev genkendt i den periode, hvor de hører til, og køre kørslen Juster kostpris - vareposter og derefter flytte den tilladte bogføringsdato til den nye periode\/det nye regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="7f6f3-283">Den første varegebyr med bogføringsdatoen 2. januar kan derefter bogføres.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-283">The first item charge with posting date January 2nd could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="7f6f3-284">Oversigt over kørslen Juster kostpris - vareposter</span><span class="sxs-lookup"><span data-stu-id="7f6f3-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="7f6f3-285">Nedenfor vises en oversigt over konceptet for tildeling af bogføringsdatoer til reguleringsværdier i kørslen Juster kostpris - vareposter siden version 3.0.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job since version 3.0.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="7f6f3-286">Fra version 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="7f6f3-286">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="7f6f3-287">I anmodningsformularen til kørslen Juster kostpris - vareposter skal der angives en bogføringsdato af brugeren.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-287">In the request form of the Adjust Cost - Item Entries batch job there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="7f6f3-288">Kørslen kører gennem alle nødvendige rettelser og oprettet værdiposter med den bogføringsdato, der er angivet i anmodningsformularen.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-288">The batch job runs through all necessary changes and creates value entries with the posting date entered in the request form.</span></span> <span data-ttu-id="7f6f3-289">Den foreslåede bogføringsdato, der skal bruges, er dags dato.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-289">Suggested posting date to use is today’s date.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="7f6f3-290">Version 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="7f6f3-290">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="7f6f3-291">I anmodningsformularen til kørslen Juster kostpris - vareposter skal der angives en bogføringsdato for postering i lukket periode af brugeren.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-291">In the request form of the Adjust Cost - Item Entries batch job there is a Closed Period Entry Posting Date to be entered by the user.</span></span> <span data-ttu-id="7f6f3-292">Kørslen kører gennem alle nødvendige rettelser og oprettet værdiposter med bogføringsdatoen for den overordnede post (leveringsdatoen for det salg, som reguleringen vedrører).</span><span class="sxs-lookup"><span data-stu-id="7f6f3-292">The batch job runs through all necessary changes and creates value entries with the posting date of the parent item ledger entry (shipment date of the sale that the adjustment address).</span></span> <span data-ttu-id="7f6f3-293">Hvis bogføringsdatoen for den overordnede post ikke inden for tilladte bogføringsdatointerval, tildeles den bogføringsdato, der er angivet som bogføringsdato for postering i lukket periode, til værdireguleringsposten.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-293">If the posting date of the parent item ledger entry is not within allowed posting date range the posting date stated as Closed Period Entry Posting Date will be assigned the Adjustment Value Entry.</span></span> <span data-ttu-id="7f6f3-294">En dato betragtes som værende i en lukket periode, hvis den er tidligere end datoen i feltet Bogf. tilladt fra i Opsætning af Finans.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-294">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span>  

### <a name="from-version-50"></a><span data-ttu-id="7f6f3-295">Fra version 5.0:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-295">From version 5.0:</span></span>  
 <span data-ttu-id="7f6f3-296">Der skal ikke længere angives en bogføringsdato i anmodningsformularen til kørslen Juster kostpris - vareposter.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-296">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="7f6f3-297">Kørslen kører gennem alle nødvendige rettelser og oprettet værdiposter med den bogføringsdato, der er angivet i den værdipost, som justeres.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-297">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="7f6f3-298">Hvis bogføringsdatoen ikke er inden for det tilladte bogføringsdatointerval, bruges bogføringsdatoen i feltet Bogf. tilladt fra i Opsætning af Finans, ELLER hvis der anvendes lagerperioder, bruges den seneste dato af disse to.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-298">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="7f6f3-299">Se det beskrevne koncept ovenfor.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-299">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="7f6f3-300">Oversigt over kørslen Bogfør lagerregulering</span><span class="sxs-lookup"><span data-stu-id="7f6f3-300">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="7f6f3-301">Kørslen Bogfør lagerregulering er tæt forbundet med kørslen Juster kostpris - vareposter, hvorfor oversigten over denne kørsel opsummeres og deles også her.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-301">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="7f6f3-302">Fra version 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="7f6f3-302">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="7f6f3-303">I anmodningsformularen til kørslen Bogfør lagerregulering skal der angives en bogføringsdato af brugeren.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-303">In the request form of the Post Inventory Cost to G/L there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="7f6f3-304">Kørslen kører gennem alle nødvendige værdiposter i filteret, hvis der er nogen, og opretter finansposter med den bogføringsdato, der er angivet i anmodningsformularen.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-304">The batch job runs through all value entries within the filter, if any, and creates General Ledger Entries with Posting Date entered in the request form.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="7f6f3-305">Version 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="7f6f3-305">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="7f6f3-306">I anmodningsformularen til kørslen Bogfør lagerregulering er datofeltet for bogføring i lukket periode tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-306">In the request form of the Post Inventory Cost to G/L the Closed Period Entry Posting Date field is available.</span></span> <span data-ttu-id="7f6f3-307">Programmet bruger den dato, du angiver i dette felt, som bogføringsdatoen for de finansposter, der oprettes for værdiposter, hvis bogføringsdatoer er i lukkede regnskabsperioder.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-307">The program uses the date you enter in this field as the posting date for the general ledger entries it creates for value entries whose posting dates are in closed accounting periods.</span></span> <span data-ttu-id="7f6f3-308">Ellers har finansposterne den samme bogføringsdato som de oprindelige værdiposter.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-308">Otherwise, the general ledger entries will have the same posting date as the original value entries.</span></span> <span data-ttu-id="7f6f3-309">En dato betragtes som værende i en lukket periode, hvis den er tidligere end datoen i feltet Bogf. tilladt fra i Opsætning af Finans.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-309">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span> <span data-ttu-id="7f6f3-310">Hvis du bogfører til F\/inans pr. bogføringsgruppe, har finansposterne den bogføringsdato, der er angivet i feltet Bogføringsdato i anmodningsformularen.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-310">If posting to G\/L Per Posting Group, the general ledger entries will have the posting date that is specified in the Posting Date field in the request form.</span></span>  

 <span data-ttu-id="7f6f3-311">I version 3 og 4 søger kørslen igennem alle værdiposter for at registrere, om der er nogen poster, hvor kostbeløb (faktisk) er forskellig fra bogført kostværdi.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-311">In version 3 and 4 the batch job scans all value entries to detect if there are any value entries where Cost Amount (Actual) differs from Cost Posted to G/L.</span></span> <span data-ttu-id="7f6f3-312">Hvis der registreres en forskel, bogføres forskelsbeløbet på en finanspost.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-312">If there is a difference detected the differing amount will be posted in a G/L entry.</span></span> <span data-ttu-id="7f6f3-313">Hvis forventet kostbogføring bruges, behandles de tilsvarende felter på samme måde.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-313">If expected cost posting is used corresponding fields are processed in the same way.</span></span>  

<span data-ttu-id="7f6f3-314">![Faktisk kostpris i forhold til forventet kostpris](media/helene/TechArticleAdjustcost14.png "Faktisk kostpris i forhold til forventet kostpris")</span><span class="sxs-lookup"><span data-stu-id="7f6f3-314">![Actual cost versus expected cost](media/helene/TechArticleAdjustcost14.png "Actual cost versus expected cost")</span></span>

### <a name="from-version-50"></a><span data-ttu-id="7f6f3-315">Fra version 5.0:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-315">From version 5.0:</span></span>  
 <span data-ttu-id="7f6f3-316">Der skal ikke længere angives en bogføringsdato i anmodningsformularen til kørslen Bogfør lagerregulering.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-316">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="7f6f3-317">Finansposten oprettes med samme bogføringsdato som den tilknyttede værdipost.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-317">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="7f6f3-318">Med henblik på at udføre kørslen skal det tilladte bogføringsdatointerval tillade bogføringsdatoen for den tilknyttede finanspost.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-318">In order to complete the batch job the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="7f6f3-319">Hvis ikke, skal det tilladte bogføringsdatointerval midlertidigt åbnes igen ved at ændre eller fjerne datoerne i felterne Bogf. tilladt fra og Bogf. tilladt til i Opsætning af Finans.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-319">If not, the allowed posting date range must be temporarily re-opened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="7f6f3-320">Det er nødvendigt for at undgå problemer med afstemningen, at bogføringsdato på finansposten svarer til bogføringsdatoen for værdiposten.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-320">To avoid reconciliation issues it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="7f6f3-321">Kørslen søger i tabel 5811 - Bogfør værdi for at identificere værdiposterne i området til bogføring i Finans.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-321">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="7f6f3-322">Tabellen tømmes efter korrekt gennemført kørsel.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-322">After successful run the table is emptied.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f6f3-323">Se også</span><span class="sxs-lookup"><span data-stu-id="7f6f3-323">See Also</span></span>  
[<span data-ttu-id="7f6f3-324">Designoplysninger: Lagerkostmetode</span><span class="sxs-lookup"><span data-stu-id="7f6f3-324">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="7f6f3-325">Designoplysninger: Vareudligning</span><span class="sxs-lookup"><span data-stu-id="7f6f3-325">Design Details: Item Application</span></span>](design-details-item-application.md)  
