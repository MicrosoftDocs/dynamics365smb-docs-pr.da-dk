---
title: Brug af udvidelsen Betalinger og afstemninger (DK) | Microsoft Docs
description: Udvidelsen gør det let at eksportere filer, der forud er formateret til at opfylde bankkravene til elektroniske afsendelser.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: c8dd465213a9882a98c1ac1623d8a093f3eecb9a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757488"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a><span data-ttu-id="48ade-103">Udvidelsen Betalinger og afstemninger (DK)</span><span class="sxs-lookup"><span data-stu-id="48ade-103">The Payments and Reconciliations (DK) Extension</span></span>

<span data-ttu-id="48ade-104">Foretag hurtige, fejlfrie betalinger ved at eksportere filer, der er formateret specielt til udveksling med dine kreditorer eller bank.</span><span class="sxs-lookup"><span data-stu-id="48ade-104">Make fast, error-free payments by exporting files that are formatted specifically for exchanges with your vendor or bank.</span></span> <span data-ttu-id="48ade-105">Disse filer giver hurtigere betaling og afstemningsprocesser og fjerner fejl, der kan ske, når du manuelt angivet oplysningerne på en banks websted.</span><span class="sxs-lookup"><span data-stu-id="48ade-105">These files speed up the payment and reconciliation processes, and eliminate errors that can happen when you manually enter the information on a bank website.</span></span>  

<span data-ttu-id="48ade-106">Udvidelsen understøtter filformater for flere danske banker.</span><span class="sxs-lookup"><span data-stu-id="48ade-106">This extension supports file formats for several Danish banks.</span></span> <span data-ttu-id="48ade-107">Når du eksporterer betalingsoplysninger til en fil, pakker udvidelsen data til det format, der kræves af din bank.</span><span class="sxs-lookup"><span data-stu-id="48ade-107">When you export payment information to a file, the extension packages the data into the format that your bank requires.</span></span> <span data-ttu-id="48ade-108">Formaterne omfatter f.eks. Bankdata-V3, BEC, SDC og FIK, som mange forskellige banker anvender, og nogle, der er mere specialiserede til visse banker, f.eks. Danske Bank og Nordea.</span><span class="sxs-lookup"><span data-stu-id="48ade-108">For example, the formats include Bankdata-V3, BEC, SDC, and FIK, which many different banks use, and some that are more specialized for certain banks, for example, Danske Bank and Nordea.</span></span> <span data-ttu-id="48ade-109">Udvidelsen indeholder også nogle formater til at importere og afstemme bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="48ade-109">The extension also includes some formats for importing and reconciling bank statements.</span></span>  

> [!Note]
> <span data-ttu-id="48ade-110">Hvis du vil bruge udvidelsen, skal du kende det format, som din bank eller leverandør kræver.</span><span class="sxs-lookup"><span data-stu-id="48ade-110">To use the extension, you must know the format that your bank or vendor requires.</span></span> <span data-ttu-id="48ade-111">Nogle banker eller leverandører angiver disse oplysninger på deres websted, men du skal muligvis kontakte deres kundeservice for at få oplysningerne.</span><span class="sxs-lookup"><span data-stu-id="48ade-111">Some banks or vendors provide this information on their websites; however, you might need to contact their customer service to get the information.</span></span>  

## <a name="supported-bank-formats"></a><span data-ttu-id="48ade-112">Understøttede bankformater</span><span class="sxs-lookup"><span data-stu-id="48ade-112">Supported Bank Formats</span></span>
<span data-ttu-id="48ade-113">Udvidelsen kan anvende følgende filformater for betalingsfiler:</span><span class="sxs-lookup"><span data-stu-id="48ade-113">This extension can apply the following file formats for payment files:</span></span>  

* <span data-ttu-id="48ade-114">BANKDATA V3</span><span class="sxs-lookup"><span data-stu-id="48ade-114">BANKDATA-V3</span></span>  
* <span data-ttu-id="48ade-115">BEC-INDLAND</span><span class="sxs-lookup"><span data-stu-id="48ade-115">BEC-INDLAND</span></span>  
* <span data-ttu-id="48ade-116">BEC-CSV</span><span class="sxs-lookup"><span data-stu-id="48ade-116">BEC-CSV</span></span>  
* <span data-ttu-id="48ade-117">DANSKEBANK CMKV</span><span class="sxs-lookup"><span data-stu-id="48ade-117">DANSKEBANK-CMKV</span></span>  
* <span data-ttu-id="48ade-118">DANSKEBANK CMKXKSX</span><span class="sxs-lookup"><span data-stu-id="48ade-118">DANSKEBANK-CMKXKSX</span></span>  
* <span data-ttu-id="48ade-119">DANSKEBANK</span><span class="sxs-lookup"><span data-stu-id="48ade-119">DANSKEBANK</span></span>  
* <span data-ttu-id="48ade-120">FIK71</span><span class="sxs-lookup"><span data-stu-id="48ade-120">FIK71</span></span>  
* <span data-ttu-id="48ade-121">NORDEA-ERHVERV-CSV</span><span class="sxs-lookup"><span data-stu-id="48ade-121">NORDEA-ERHVERV-CSV</span></span>  
* <span data-ttu-id="48ade-122">NORDEA</span><span class="sxs-lookup"><span data-stu-id="48ade-122">NORDEA</span></span>  
* <span data-ttu-id="48ade-123">NORDEA-UNITEL-V3</span><span class="sxs-lookup"><span data-stu-id="48ade-123">NORDEA-UNITEL-V3</span></span>  
* <span data-ttu-id="48ade-124">SDC</span><span class="sxs-lookup"><span data-stu-id="48ade-124">SDC</span></span>  
* <span data-ttu-id="48ade-125">SDC-CSV</span><span class="sxs-lookup"><span data-stu-id="48ade-125">SDC-CSV</span></span>  

## <a name="to-set-up-the-extension"></a><span data-ttu-id="48ade-126">Sådan konfigureres udvidelsen</span><span class="sxs-lookup"><span data-stu-id="48ade-126">To set up the extension</span></span>

<span data-ttu-id="48ade-127">Det kræver nogle trin at komme i gang.</span><span class="sxs-lookup"><span data-stu-id="48ade-127">There are a few steps to get started.</span></span>  

* <span data-ttu-id="48ade-128">Tillade eksport af betalingdata.</span><span class="sxs-lookup"><span data-stu-id="48ade-128">Allow payment data exports.</span></span> <span data-ttu-id="48ade-129">For at beskytte dine data, er dette ikke umiddelbart tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="48ade-129">To help protect your data, this is not readily available.</span></span>  
* <span data-ttu-id="48ade-130">Konfigurer køb og skyldige beløb, så du ikke har brug for eksterne bilagsnumre på fakturaer.</span><span class="sxs-lookup"><span data-stu-id="48ade-130">Set up purchase and payables so that you do not require external document numbers on invoices.</span></span> <span data-ttu-id="48ade-131">Hvis det er nødvendigt, kan du kan bruge referencenummeret til at referere til en bestemt faktura.</span><span class="sxs-lookup"><span data-stu-id="48ade-131">If needed, you can use the reference number to refer to a specific invoice.</span></span>  
* <span data-ttu-id="48ade-132">Angiv betalingsformen for hver kreditor.</span><span class="sxs-lookup"><span data-stu-id="48ade-132">Specify the payment method for each vendor.</span></span> <span data-ttu-id="48ade-133">Betalingsformer definerer, hvordan du betaler fakturaer fra kreditoren.</span><span class="sxs-lookup"><span data-stu-id="48ade-133">Payment methods define how you pay invoices from the vendor.</span></span> <span data-ttu-id="48ade-134">F.eks. Bank, Kontant, Check eller Konto.</span><span class="sxs-lookup"><span data-stu-id="48ade-134">For example, Bank, Cash, Check, or Account.</span></span>  
* <span data-ttu-id="48ade-135">Angiv den type format, der skal bruges til hver af dine bankkonti.</span><span class="sxs-lookup"><span data-stu-id="48ade-135">Specify the type of format to use for each of your bank accounts.</span></span> <span data-ttu-id="48ade-136">F.eks. NORDEA, DANSKEBANK, SDC osv.</span><span class="sxs-lookup"><span data-stu-id="48ade-136">For example, NORDEA, DANSKEBANK, SDC, and so on.</span></span>  

<span data-ttu-id="48ade-137">Desuden skal du tildele kreditorer til en indenlandsk **Virksomhedsbogføringsgruppe** og en **Kreditorbogføringsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="48ade-137">Additionally, you must assign vendors to a domestic **Gen. Bus. Posting Group** and a **Vendor Posting Group**.</span></span> <span data-ttu-id="48ade-138">Indstillingen land/område for kreditoren skal være Danmark (DK).</span><span class="sxs-lookup"><span data-stu-id="48ade-138">The Country/Region setting for the vendor must be Denmark (DK).</span></span> <span data-ttu-id="48ade-139">Du kan finde flere oplysninger under [Konfigurere bogføringsgrupper](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="48ade-139">For more information, see [Setting Up Posting Groups](finance-posting-groups.md).</span></span>  

### <a name="to-allow-prod_short-to-export-payment-data"></a><span data-ttu-id="48ade-140">Sådan tillader du [!INCLUDE[prod_short](includes/prod_short.md)] at eksportere betalingsdata</span><span class="sxs-lookup"><span data-stu-id="48ade-140">To allow [!INCLUDE[prod_short](includes/prod_short.md)] to export payment data</span></span>

1. <span data-ttu-id="48ade-141">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="48ade-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="48ade-142">På siden **Rediger udbetalingskladde** skal du vælge kørslen **Bank**.</span><span class="sxs-lookup"><span data-stu-id="48ade-142">On the **Edit Payment Journal** page, choose the **Bank** batch.</span></span>  
3. <span data-ttu-id="48ade-143">Vælg afkrydsningsfeltet **Tillad eksport af betaling**.</span><span class="sxs-lookup"><span data-stu-id="48ade-143">Choose the **Allow Payment Export** check box.</span></span>  

### <a name="to-specify-a-payment-method-for-a-vendor"></a><span data-ttu-id="48ade-144">Sådan angives en betalingsform for en kreditor</span><span class="sxs-lookup"><span data-stu-id="48ade-144">To specify a payment method for a vendor</span></span>

<span data-ttu-id="48ade-145">Følgende tabel viser de kombinationer af FIK- og GIRO betalingsformer, som [!INCLUDE[prod_short](includes/prod_short.md)] understøtter.</span><span class="sxs-lookup"><span data-stu-id="48ade-145">The following table shows the combinations of FIK and GIRO payment methods that [!INCLUDE[prod_short](includes/prod_short.md)] supports.</span></span>

|<span data-ttu-id="48ade-146">Kombination</span><span class="sxs-lookup"><span data-stu-id="48ade-146">Combination</span></span>|<span data-ttu-id="48ade-147">Type 01</span><span class="sxs-lookup"><span data-stu-id="48ade-147">Type 01</span></span> | <span data-ttu-id="48ade-148">Type 04</span><span class="sxs-lookup"><span data-stu-id="48ade-148">Type 04</span></span> | <span data-ttu-id="48ade-149">Type 71</span><span class="sxs-lookup"><span data-stu-id="48ade-149">Type 71</span></span> | <span data-ttu-id="48ade-150">Type 73</span><span class="sxs-lookup"><span data-stu-id="48ade-150">Type 73</span></span> |
|----|--------|---------|---------|---------|
|<span data-ttu-id="48ade-151">Girokontonr. eller FIK-kreditornummer?</span><span class="sxs-lookup"><span data-stu-id="48ade-151">Giro Account No. or FIK Creditor No.?</span></span> | <span data-ttu-id="48ade-152">Girokontonr.</span><span class="sxs-lookup"><span data-stu-id="48ade-152">Giro Account No.</span></span> | <span data-ttu-id="48ade-153">Girokontonr.</span><span class="sxs-lookup"><span data-stu-id="48ade-153">Giro Account No.</span></span> | <span data-ttu-id="48ade-154">FIK-kreditornummer</span><span class="sxs-lookup"><span data-stu-id="48ade-154">FIK Creditor No.</span></span> | <span data-ttu-id="48ade-155">FIK-kreditornummer</span><span class="sxs-lookup"><span data-stu-id="48ade-155">FIK Creditor No.</span></span>|
|<span data-ttu-id="48ade-156">Tillader meddelelse til modtager?</span><span class="sxs-lookup"><span data-stu-id="48ade-156">Allows Message to Recipient?</span></span> | <span data-ttu-id="48ade-157">Ja</span><span class="sxs-lookup"><span data-stu-id="48ade-157">Yes</span></span> |<span data-ttu-id="48ade-158">Nej</span><span class="sxs-lookup"><span data-stu-id="48ade-158">No</span></span> |<span data-ttu-id="48ade-159">Nej</span><span class="sxs-lookup"><span data-stu-id="48ade-159">No</span></span> | <span data-ttu-id="48ade-160">Ja</span><span class="sxs-lookup"><span data-stu-id="48ade-160">Yes</span></span> |
|<span data-ttu-id="48ade-161">Indeholder betalingsreferencenummer?</span><span class="sxs-lookup"><span data-stu-id="48ade-161">Contains Payment Reference number?</span></span> | <span data-ttu-id="48ade-162">Nej</span><span class="sxs-lookup"><span data-stu-id="48ade-162">No</span></span> | <span data-ttu-id="48ade-163">Ja, 16 cifre.</span><span class="sxs-lookup"><span data-stu-id="48ade-163">Yes, 16 digits.</span></span> | <span data-ttu-id="48ade-164">Ja, 15 cifre.</span><span class="sxs-lookup"><span data-stu-id="48ade-164">Yes, 15 digits.</span></span> | <span data-ttu-id="48ade-165">Nej</span><span class="sxs-lookup"><span data-stu-id="48ade-165">No</span></span>|

1. <span data-ttu-id="48ade-166">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leverandører (Kreditorer)**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="48ade-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="48ade-167">Åbn kortet, udvid fanen **Betalinger** og vælg betalingsformen i feltet **Betalingsform**.</span><span class="sxs-lookup"><span data-stu-id="48ade-167">Open the card, expand the **Payments** tab, in the **Payment Method** field choose the payment method.</span></span>  
3. <span data-ttu-id="48ade-168">Afhængigt af dit valg, skal du udfylde andre felter.</span><span class="sxs-lookup"><span data-stu-id="48ade-168">Depending on your selection, you must complete other fields.</span></span> <span data-ttu-id="48ade-169">Se overstående tabel for en beskrivelse af kombinationerne.</span><span class="sxs-lookup"><span data-stu-id="48ade-169">See the table above for a description of the combinations.</span></span>  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a><span data-ttu-id="48ade-170">Sådan angives formatet, der skal bruges til en bankkonto</span><span class="sxs-lookup"><span data-stu-id="48ade-170">To specify the format to use for a bank account</span></span>

1. <span data-ttu-id="48ade-171">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="48ade-171">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="48ade-172">Åbn kortet for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="48ade-172">Open the card for the bank account.</span></span>  
3. <span data-ttu-id="48ade-173">I feltet **Format til eksport af betaling** skal du vælge formatet for udlæsningsfilen.</span><span class="sxs-lookup"><span data-stu-id="48ade-173">In the **Payment Export Format** field, choose the format for your export file.</span></span>  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a><span data-ttu-id="48ade-174">Vælg FIK- eller Giro-betalingsoplysningerne for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="48ade-174">Choosing the FIK or Giro payment information for vendor invoices</span></span>

1. <span data-ttu-id="48ade-175">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="48ade-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="48ade-176">Vælg kreditoren.</span><span class="sxs-lookup"><span data-stu-id="48ade-176">Choose the vendor.</span></span> <span data-ttu-id="48ade-177">Husk, at det skal være en dansk kreditor med en adresse i Danmark.</span><span class="sxs-lookup"><span data-stu-id="48ade-177">Remember, this must be a Danish vendor with an address in Denmark.</span></span>
3. <span data-ttu-id="48ade-178">Opret en faktura.</span><span class="sxs-lookup"><span data-stu-id="48ade-178">Create an invoice.</span></span> <span data-ttu-id="48ade-179">Felterne **Betalingsform** og **Kreditornummer** udfyldes på basis af indstillinger på kreditorkortet.</span><span class="sxs-lookup"><span data-stu-id="48ade-179">The **Payment Method** and **Vendor Number** fields are filled in based on settings on the Vendor card.</span></span> <span data-ttu-id="48ade-180">Du kan ændre dem, hvis du ønsker det.</span><span class="sxs-lookup"><span data-stu-id="48ade-180">You can change them if you want.</span></span>
4. <span data-ttu-id="48ade-181">I feltet **Betalingsreference** skal du angive tallet på 15 cifre fra kreditorfakturaen.</span><span class="sxs-lookup"><span data-stu-id="48ade-181">In the **Payment Reference** field, enter the 15-digit number from the vendor invoice.</span></span>  

    > [!Tip]
    > <span data-ttu-id="48ade-182">Du behøver kun at tilføje de sidste 11 cifre i nummeret.</span><span class="sxs-lookup"><span data-stu-id="48ade-182">You only have to add the last 11 digits of the number.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="48ade-183">tilføjer fire nuller i begyndelsen af nummeret.</span><span class="sxs-lookup"><span data-stu-id="48ade-183">will add four zeros to the beginning of the number.</span></span>  

5. <span data-ttu-id="48ade-184">Bogfør fakturaen.</span><span class="sxs-lookup"><span data-stu-id="48ade-184">Post the invoice.</span></span>

## <a name="to-use-the-extension-to-export-payment-data"></a><span data-ttu-id="48ade-185">Så bruges udvidelsen til at eksportere betalingsdata</span><span class="sxs-lookup"><span data-stu-id="48ade-185">To use the extension to export payment data</span></span>

1. <span data-ttu-id="48ade-186">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="48ade-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="48ade-187">Vælg handlingen **Lav kreditorbetalingsforslagskladder**.</span><span class="sxs-lookup"><span data-stu-id="48ade-187">Choose the **Suggest Vendor Payment Journals** action.</span></span>  

    > [!Tip]
    > <span data-ttu-id="48ade-188">Hvis du kun vil udlæse specifikke betalinger, kan du bruge indstillingerne til at filtrere dataene.</span><span class="sxs-lookup"><span data-stu-id="48ade-188">If you want to export only specific payments, use the options for filtering the data.</span></span>  

3. <span data-ttu-id="48ade-189">Hvis det er nødvendigt, kan du tilføje filtre for kun at eksportere specifikke betalinger.</span><span class="sxs-lookup"><span data-stu-id="48ade-189">If needed, you can add filters to export only specific payments.</span></span>  
4. <span data-ttu-id="48ade-190">I feltet **Bankbetalingstype** skal du vælge **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="48ade-190">In the **Bank Payment Type** field, choose **Electronic Payment**.</span></span>  
5. <span data-ttu-id="48ade-191">Vælg handlingen **Eksportér**.</span><span class="sxs-lookup"><span data-stu-id="48ade-191">Choose the **Export** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="48ade-192">Se også</span><span class="sxs-lookup"><span data-stu-id="48ade-192">See also</span></span>

<span data-ttu-id="48ade-193">[Tilpasse Business Central til [!INCLUDE[prod_short](includes/prod_short.md)] ved brug af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="48ade-193">[Customizing Business Central for [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="48ade-194">Indhente betalinger med SEPA Direct Debit</span><span class="sxs-lookup"><span data-stu-id="48ade-194">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="48ade-195">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="48ade-195">Working with General Journals</span></span>](ui-work-general-journals.md)  
