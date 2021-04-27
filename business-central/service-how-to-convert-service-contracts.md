---
title: Sådan konverteres servicekontrakter | Microsoft Docs
description: Da momssatsændringsværktøjet ikke kan konvertere servicekontrakter, skal disse kontrakter konverteres manuelt. Dette emne beskriver flere alternative metoder, der kan bruges til konvertering af servicekontrakter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3da6d4144b1e35da864de7b69a425bb65800b2cb
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770734"
---
# <a name="convert-service-contracts-that-include-vat-amounts"></a><span data-ttu-id="4b1ab-104">Konvertere servicekontrakter, som omfatter momsbeløb</span><span class="sxs-lookup"><span data-stu-id="4b1ab-104">Convert Service Contracts that Include VAT Amounts</span></span>
<span data-ttu-id="4b1ab-105">Da momssatsændringsværktøjet ikke kan konvertere servicekontrakter, skal disse kontrakter konverteres manuelt.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-105">Because the VAT rate change tool cannot convert service contracts, these contracts must be converted manually.</span></span> <span data-ttu-id="4b1ab-106">Dette emne beskriver flere alternative metoder, der kan bruges til konvertering af servicekontrakter.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-106">This topic describes several alternative methods that you can use for service contract conversion.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4b1ab-107">Dette emne giver en overordnet arbejdsproces.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-107">This topic provides a high-level workflow.</span></span>  

 <span data-ttu-id="4b1ab-108">Følgende procedure beskriver, hvordan du retter en faktura til en forudbetalt servicekontrakt, der er oprettet et år i forvejen.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-108">The following procedure describes how to correct an invoice for a prepaid service contract that has been created a year in advance.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4b1ab-109">I dette eksempel skal du ændre din arbejdsdato til 01.01.2017.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-109">For this example, you must change your work date to 01.01.2017.</span></span>  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a><span data-ttu-id="4b1ab-110">Sådan rettes en faktura for en forudbetalt servicekontrakt</span><span class="sxs-lookup"><span data-stu-id="4b1ab-110">To correct an invoice for a prepaid service contract</span></span>  
1. <span data-ttu-id="4b1ab-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontraktstyring**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Contract Management**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4b1ab-112">Under **Lister** skal du vælge **Servicekontrakter**.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-112">Under **Lists**, choose **Service Contracts**.</span></span>  
3. <span data-ttu-id="4b1ab-113">Opret en ny forudbetalt servicekontrakt.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-113">Create a new prepaid service contract.</span></span> <span data-ttu-id="4b1ab-114">Angiv en startdato til **01.01.2017** og et fakturaperiodeåret for debitor **20000**.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-114">Enter a start date of **01.01.2017** and an invoice period year for customer **20000**.</span></span>  
4. <span data-ttu-id="4b1ab-115">Hvis du vil underskrive kontrakten, skal du vælge handlingen **Underskriv kontrakt**.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-115">To sign the contract, choose the **Sign Contract** action.</span></span>  
5. <span data-ttu-id="4b1ab-116">Opret en servicefaktura.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-116">Create a service invoice.</span></span>
6. <span data-ttu-id="4b1ab-117">Fakturaen er angivet som en ikke-bogførte servicefaktura.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-117">The invoice is listed as an unposted service invoice.</span></span> <span data-ttu-id="4b1ab-118">For at se servicefakturaen skal du vælge handlingen **Service**, vælge handlingen **Kontraktstyring** og derefter vælge handlingen **Servicefakturaer**.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-118">To view the service invoice, choose the **Service** action, choose the **Contract Management** action, and then choose the **Service Invoices** action.</span></span>  
7. <span data-ttu-id="4b1ab-119">Bogfør servicefakturaen.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-119">Post the service invoice.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4b1ab-120">Ændr ikke den ikke-bogførte servicefaktura.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-120">Do not change the unposted service invoice.</span></span> <span data-ttu-id="4b1ab-121">Da serviceposterne oprettes, når fakturaen oprettes, vil en ændring af den ikke-bogførte faktura ikke ændre de allerede oprettede serviceposter.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-121">Since the service ledger entries are created when the invoice is created, a change in the unposted invoice will not change the already created service ledger entries.</span></span> <span data-ttu-id="4b1ab-122">Momsposter oprettes dog, når fakturaen bogføres.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-122">However, the VAT entries are created when the invoice is posted.</span></span> <span data-ttu-id="4b1ab-123">Dermed kan du ændre den generelle produktbogføringsgruppe og GSP-produktbogføringsgruppe på den ikke-bogførte servicefaktura.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-123">This lets you change the general product posting group and the GSP product posting group on the unposted service invoice.</span></span>  

### <a name="to-create-a-credit-memo-for-vat-difference"></a><span data-ttu-id="4b1ab-124">Sådan oprettes en kreditnota for momsdifference</span><span class="sxs-lookup"><span data-stu-id="4b1ab-124">To create a credit memo for VAT difference</span></span>  
<span data-ttu-id="4b1ab-125">Følgende procedure beskriver, hvordan du opretter en kreditnota , der kun omfatter momsdifference for den periode, der allerede er fakturerede, startende med **01.07.2017**.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-125">The following procedure describes how to create a credit memo that only includes the VAT difference for the already invoiced period starting on **01.07.2017**.</span></span> <span data-ttu-id="4b1ab-126">I dette eksempel bogføres momsbeløbet kun i modulet Økonomistyring, ikke i modulet Servicestyring.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-126">In this example, the VAT amount is only posted to the Financial Management module, not to the Service Management module.</span></span> <span data-ttu-id="4b1ab-127">De momsposter, der er knyttet til serviceposten, vil ikke blive rettet.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-127">The VAT entries that are linked to the service ledger entry will not be corrected.</span></span>  

1. <span data-ttu-id="4b1ab-128">Oprette en ny finanskonto for momsdifferencen.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-128">Create a new general ledger account for the VAT difference.</span></span> <span data-ttu-id="4b1ab-129">Denne konto bruges til direkte bogføring af momskorrektionen.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-129">This account will be used for direct posting of the VAT correction.</span></span>  
2. <span data-ttu-id="4b1ab-130">Tilføj en ny linje til momsbogføringsopsætningen.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-130">Add a new line to the VAT posting setup.</span></span>  

### <a name="to-create-contract-expiration-dates-in-contract-lines"></a><span data-ttu-id="4b1ab-131">Sådan oprettes kontraktudløbsdatoen i kontraktlinjer</span><span class="sxs-lookup"><span data-stu-id="4b1ab-131">To create contract expiration dates in contract lines</span></span>  
<span data-ttu-id="4b1ab-132">Følgende procedure beskriver, hvordan du opretter nye kontrakter ved at arbejde med kontraktudløbsdatoer i servicekontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-132">The following procedure describes how to create new contracts by working with contract expiration dates in service contract lines.</span></span>  

1. <span data-ttu-id="4b1ab-133">På siden **Servicekontrakt** angives kontraktens udløbsdato til **30.06.2017**.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-133">On the **Service Contract** page, set the contract expiration date to **30.06.2017**.</span></span>  
2. <span data-ttu-id="4b1ab-134">Vælg handlingen **Opret kreditnota** for automatisk at oprette en kreditnota for juli 2017 til december 2017.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-134">Choose the **Create Credit Memo** action to automatically create a credit memo for July 2017 to December 2017.</span></span>  
3. <span data-ttu-id="4b1ab-135">Da kontrakten er udløbet, skal du oprette en ny kontrakt for perioden med den nye momssats for 1 juli 2017 til 31. december 2017.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-135">Because the contract has expired, you need to create a new contract for the period with the new VAT rate for July 1, 2017 to December 31, 2017.</span></span>  

### <a name="to-create-a-new-credit-memo"></a><span data-ttu-id="4b1ab-136">Sådan oprettes en ny kreditnota</span><span class="sxs-lookup"><span data-stu-id="4b1ab-136">To create a new credit memo</span></span>  
<span data-ttu-id="4b1ab-137">Følgende procedure beskriver, hvordan du opretter en ny kreditnota ved hjælp af batchjobbet **Hent forudbetalte kontraktposter**.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-137">The following procedure describes how to create a new credit memo using the **Get Prepaid Contract Entries** batch job.</span></span> <span data-ttu-id="4b1ab-138">Poster, du ikke vil rette fra januar 2017 til juni 2017, vil blive slettet.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-138">Entries that you do not want to correct from January 2017 to June 2017 will be deleted.</span></span>  

1. <span data-ttu-id="4b1ab-139">Du kan køre momssatsændringsværktøjet på 1 juli 2017.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-139">Run the VAT rate change tool on July 1, 2017.</span></span> <span data-ttu-id="4b1ab-140">Den generelle produktbogføringsgruppe eller momsproduktbogføringsgruppen ændres.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-140">The general product posting group or the VAT product posting group is changed.</span></span> <span data-ttu-id="4b1ab-141">Du kan finde flere oplysninger i [Arbejde med moms af salg og køb](finance-work-with-vat.md).</span><span class="sxs-lookup"><span data-stu-id="4b1ab-141">For more information, see [Work with VAT on Sales and Purchases](finance-work-with-vat.md).</span></span>  
2. <span data-ttu-id="4b1ab-142">Når du har kørt momssatsændringsværktøjet skal du angive en kontraktudløbsdato for servicekontrakten.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-142">After running the VAT rate change tool, enter a contract expiration date for the service contract.</span></span> <span data-ttu-id="4b1ab-143">Du kan nu slette servicekontraktlinjen og oprette en ny linje, der er identisk med den gamle.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-143">You can now delete the service contract line and create a new line that is identical to the old one.</span></span>  
3. <span data-ttu-id="4b1ab-144">Opret en ny faktura for perioden januar 2017 til december 2012 ved hjælp af den nye momssats.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-144">Create a new invoice for the period of January 2017 to December 2012 using the new VAT rate.</span></span>  
4. <span data-ttu-id="4b1ab-145">Hvis du vil oprette en anden kreditnota skal du på siden **Servicekreditnotaer** vælge handlingen **Ny** for at oprette en ny servicekreditnota.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-145">To create another credit memo, on the **Service Credit Memos** page, choose the **New** action to create a new service credit memo.</span></span>  
5. <span data-ttu-id="4b1ab-146">Vælg handlingen **Hent forudbetalte kontraktposter**.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-146">Choose the **Get Prepaid Contract Entries** action.</span></span>  
6. <span data-ttu-id="4b1ab-147">Når konverteringen er fuldført, vil moms og serviceposter være korrekte.</span><span class="sxs-lookup"><span data-stu-id="4b1ab-147">After the conversion is complete, VAT and service ledger entries will be correct.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4b1ab-148">Se også</span><span class="sxs-lookup"><span data-stu-id="4b1ab-148">See Also</span></span>  
[<span data-ttu-id="4b1ab-149">Arbejde med servicekontrakter og servicekontrakttilbud</span><span class="sxs-lookup"><span data-stu-id="4b1ab-149">Work with Service Contracts and Service Contract Quotes</span></span>](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[<span data-ttu-id="4b1ab-150">Finans</span><span class="sxs-lookup"><span data-stu-id="4b1ab-150">Finance</span></span>](finance.md)  
[<span data-ttu-id="4b1ab-151">Rapportere moms til skattemyndighederne</span><span class="sxs-lookup"><span data-stu-id="4b1ab-151">Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)  
[<span data-ttu-id="4b1ab-152">Arbejde med moms af salg og køb</span><span class="sxs-lookup"><span data-stu-id="4b1ab-152">Work with VAT on Sales and Purchases</span></span>](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]