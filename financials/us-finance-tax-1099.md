---
title: Rapportering af 1099-transaktioner i USA | Microsoft Docs
description: "IRS kræver brug af skatteblanketten 1099 ved betalinger til kreditorer, og du kan angive, at et købsdokument er 1099-pligtigt, og angive 1099-koden for kreditoren."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c20c52927aa979e56aeef7975fbcee1564ca4dd7
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="reporting-transactions-as-1099-liable-in-the-us"></a><span data-ttu-id="1db07-103">Rapportering af transaktioner som 1099-pligtige i USA</span><span class="sxs-lookup"><span data-stu-id="1db07-103">Reporting Transactions as 1099 Liable in the US</span></span>

<span data-ttu-id="1db07-104">De interne skattemyndigheder (IRS) kræver en eller flere versioner af skatteformularen 1099 for betalinger til kreditorer.</span><span class="sxs-lookup"><span data-stu-id="1db07-104">The Internal Revenue Service (IRS) requires one or more versions of the 1099 tax form for payments to vendors.</span></span> <span data-ttu-id="1db07-105">Kopier af disse formularer skal sendes til kreditorer årligt på eller inden den sidste dag i januar.</span><span class="sxs-lookup"><span data-stu-id="1db07-105">Copies of these forms must be sent to vendors annually on or before the last day of January.</span></span> <span data-ttu-id="1db07-106">På købsdokumenterne kan du angive, at dokumentet er 1099-pligtigt, og du kan angive 1099-koden for kreditoren.</span><span class="sxs-lookup"><span data-stu-id="1db07-106">On your purchase documents, you can specify that the document is 1099 liable, and you can specify the 1099 code for the vendor.</span></span>  

## <a name="1099-codes"></a><span data-ttu-id="1db07-107">1099 koder</span><span class="sxs-lookup"><span data-stu-id="1db07-107">1099 codes</span></span>
<span data-ttu-id="1db07-108">I [!INCLUDE[d365fin](includes/d365fin_md.md)] er de mest almindelige 1099-koder allerede konfigureret for dig, så du er klar til at oprette de nødvendige rapporter.</span><span class="sxs-lookup"><span data-stu-id="1db07-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the most common 1099 codes are already set up for you so you are ready to generate the required reports.</span></span> <span data-ttu-id="1db07-109">Koderne er defineret i vinduet **IRS 1099-formular for**, hvor du også kan tilføje nye 1099-koder.</span><span class="sxs-lookup"><span data-stu-id="1db07-109">The codes are defined in the **IRS 1099 Form Box** window where you can also add new 1099 codes.</span></span> <span data-ttu-id="1db07-110">For hver skattepligtig kreditor kan du derefter angive den relevante 1099-kode på oversigtspanelet **Betalinger** på kreditorkortet.</span><span class="sxs-lookup"><span data-stu-id="1db07-110">For each tax liable vendor, you can then specify the relevant 1099 code on the **Payments** FastTab on the Vendor card.</span></span>  

<span data-ttu-id="1db07-111">Med rapporten **1099-oplysninger for kreditor** kan du gennemse 1099-transaktioner, der er betalt i en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="1db07-111">With the **Vendor 1099 Information** report, you can review 1099 transactions paid during a specified period.</span></span> <span data-ttu-id="1db07-112">Ved afslutningen på året kan du udskrive 1099-transaktioner på fortrykte formularer.</span><span class="sxs-lookup"><span data-stu-id="1db07-112">At the end of the year, you can print 1099 transactions on preprinted forms.</span></span>  

## <a name="printing-1099-tax-forms"></a><span data-ttu-id="1db07-113">Udskrivning af 1099-skatteformularer</span><span class="sxs-lookup"><span data-stu-id="1db07-113">Printing 1099 tax forms</span></span>
<span data-ttu-id="1db07-114">Fra vinduet **IRS 1099-formularfeltet** kan du få adgang til de følgende skatteformularer:</span><span class="sxs-lookup"><span data-stu-id="1db07-114">From the **IRS 1099 Form Box** window, you can access the following tax forms:</span></span>  

* <span data-ttu-id="1db07-115">Kreditor 1099-div</span><span class="sxs-lookup"><span data-stu-id="1db07-115">Vendor 1099 Div</span></span>  

  <span data-ttu-id="1db07-116">Udskriver den føderale formular 1099-DIV for udbytte og distribution.</span><span class="sxs-lookup"><span data-stu-id="1db07-116">Prints the federal form 1099-DIV for dividends and distribution.</span></span> <span data-ttu-id="1db07-117">Du kan udskrive alle eller specifikke 1099-DIV formularer.</span><span class="sxs-lookup"><span data-stu-id="1db07-117">You can print all or specific 1099-DIV forms.</span></span> <span data-ttu-id="1db07-118">Rapporten anvender de koder, der gælder for DIV-formularens beløbsfelter, fra vinduet **IRS 1099-formularfelt**.</span><span class="sxs-lookup"><span data-stu-id="1db07-118">The report uses the codes that apply to the DIV form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  
* <span data-ttu-id="1db07-119">Kreditor 1099 Int</span><span class="sxs-lookup"><span data-stu-id="1db07-119">Vendor 1099 Int</span></span>  

  <span data-ttu-id="1db07-120">Udskriver den føderale formular 1099-INT for renteindtægter.</span><span class="sxs-lookup"><span data-stu-id="1db07-120">Prints the federal form 1099-INT for interest income.</span></span> <span data-ttu-id="1db07-121">Du kan udskrive alle eller specifikke 1099-INT formularer.</span><span class="sxs-lookup"><span data-stu-id="1db07-121">You can print all or specific 1099-INT forms.</span></span> <span data-ttu-id="1db07-122">Rapporten anvender de koder, der gælder for INT-formularens beløbsfelter, fra vinduet **IRS 1099-formularfelt**.</span><span class="sxs-lookup"><span data-stu-id="1db07-122">The report uses the codes that apply to the INT form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  
* <span data-ttu-id="1db07-123">Diverse 1099 for kreditor - diverse indtægter</span><span class="sxs-lookup"><span data-stu-id="1db07-123">Vendor 1099 Misc - Miscellaneous income</span></span>  

  <span data-ttu-id="1db07-124">Udskriver den føderale formular 1099-MISC for diverse indtægter.</span><span class="sxs-lookup"><span data-stu-id="1db07-124">Prints the federal form 1099-MISC for miscellaneous income.</span></span> <span data-ttu-id="1db07-125">Du kan udskrive alle eller specifikke 1099-MISC formularer.</span><span class="sxs-lookup"><span data-stu-id="1db07-125">You can print all or specific 1099-MISC forms.</span></span> <span data-ttu-id="1db07-126">Rapporten anvender de koder, der gælder for MISC-formularens beløbsfelter, fra vinduet **IRS 1099-formularfelt**.</span><span class="sxs-lookup"><span data-stu-id="1db07-126">The report uses the codes that apply to the MISC form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  

<span data-ttu-id="1db07-127">Lovmæssige ændringer, der berører denne rapport og tabeldataene, håndteres normalt i opdateringer i slutningen af året.</span><span class="sxs-lookup"><span data-stu-id="1db07-127">Regulatory changes affecting this report and the table data are generally handled in end-of-year updates.</span></span>
<span data-ttu-id="1db07-128">Det kan være nyttigt at køre rapporten **1099-oplysninger for kreditor** for at gennemgå dataene, inden formularerne udskrives.</span><span class="sxs-lookup"><span data-stu-id="1db07-128">It may be helpful to run the **Vendor 1099 Information** report to review the data before printing the forms.</span></span>

## <a name="submitting-1099-tax-forms-electronically"></a><span data-ttu-id="1db07-129">Indsendelse af 1099-skatteformularer elektronisk</span><span class="sxs-lookup"><span data-stu-id="1db07-129">Submitting 1099 tax forms electronically</span></span>
<span data-ttu-id="1db07-130">Hvis du vil sende 1099-skatteformularer elektronisk, kan du bruge rapporten **Kreditor 1099 magnetiske medier**.</span><span class="sxs-lookup"><span data-stu-id="1db07-130">To submit the 1099 tax forms electronically, use the **Vendor 1099 Magnetic Media** report.</span></span> <span data-ttu-id="1db07-131">Angiver de 1099-formularer, som kan eksporteres.</span><span class="sxs-lookup"><span data-stu-id="1db07-131">Specifies the 1099 forms that can be exported.</span></span> <span data-ttu-id="1db07-132">De formularoplysninger, der eksporteres i denne rapport, er de samme, som de rapporter, der udskriver 1099-formularer, som er beskrevet i det foregående afsnit.</span><span class="sxs-lookup"><span data-stu-id="1db07-132">The form information exported by this report is the same as the reports that print 1099 forms that are described in the previous section.</span></span>  

<span data-ttu-id="1db07-133">Rapporten anvender de koder, der gælder for formularens beløbsfelter, fra vinduet **IRS 1099-formularfelt**.</span><span class="sxs-lookup"><span data-stu-id="1db07-133">The report uses the codes that apply to the form amount boxes from the **IRS 1099 Form-Box** window.</span></span> <span data-ttu-id="1db07-134">Koderne er knyttet til formularfelterne i de forskellige fillayout i denne rapport, og tabeldataene og rapportversionen for et bestemt momsår skal derfor stemme overens.</span><span class="sxs-lookup"><span data-stu-id="1db07-134">The codes are mapped to the form boxes in the file layouts of this report, therefore the table data and report version for a particular tax year must be in agreement.</span></span> <span data-ttu-id="1db07-135">Hvis der tilføjes brugerdefinerede koder til tabellen, skal disse knyttes til formularfelterne i dette objekt.</span><span class="sxs-lookup"><span data-stu-id="1db07-135">If any custom codes are added to the table these must be mapped to the form boxes inside this object.</span></span>  

<span data-ttu-id="1db07-136">Lovmæssige ændringer, der berører denne rapport og tabeldataene, håndteres normalt i opdateringer i slutningen af året.</span><span class="sxs-lookup"><span data-stu-id="1db07-136">Regulatory changes affecting this report and the table data are generally handled in end-of-year updates.</span></span>
<span data-ttu-id="1db07-137">Det kan være nyttigt at køre rapporten **Kreditor 1099-oplysninger** for at gennemgå dataene, inden den elektroniske fil genereres.</span><span class="sxs-lookup"><span data-stu-id="1db07-137">It may be helpful to run the **Vendor 1099 Information** report to review the data before generating the electronic file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1db07-138">Se også</span><span class="sxs-lookup"><span data-stu-id="1db07-138">See Also</span></span>
[<span data-ttu-id="1db07-139">Fremgangsmåde: Registrere nye kreditorer</span><span class="sxs-lookup"><span data-stu-id="1db07-139">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
[<span data-ttu-id="1db07-140">Fremgangsmåde: Registrere køb</span><span class="sxs-lookup"><span data-stu-id="1db07-140">How to: Record Purchase</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="1db07-141">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1db07-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

