---
title: Rapportvalg i Business Central
description: Få mere at vide om, hvordan du opretter de rapporter, som bruges til at udskrive forskellige typer dokumenter i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 01/18/2021
ms.author: edupont
ms.openlocfilehash: d30baa44894658c03c3deffdf24a7923293b88fd
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024633"
---
# <a name="report-selection-in-business-central"></a><span data-ttu-id="3ef61-103">Rapportvalg i Business Central</span><span class="sxs-lookup"><span data-stu-id="3ef61-103">Report Selection in Business Central</span></span>

<span data-ttu-id="3ef61-104">Du kan angive standardrapporter, der kan anvendes til at udskrive de forskellige dokumenter til salg og køb, f.eks. ordrer, tilbud, fakturaer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="3ef61-104">You can set up default reports that will be used to print the various documents for sales and purchases, such as orders, quotes, invoices, and credit memos.</span></span> <span data-ttu-id="3ef61-105">Hvis du f. eks. har et bestemt layout til salgsfakturaer, kan du angive den rapport i **Rapportvalg - salg**-siden, så de bruges til at sende eller udskrive salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="3ef61-105">For example, if you have a specific layout for sales invoices, you can specify that report in the **Report Selections - Sales** page so that it will be used to send or print sales invoices.</span></span>  

<span data-ttu-id="3ef61-106">På **Rapportvalg**-siderne kan du angive, hvilken rapport der skal udskrives i forskellige situationer.</span><span class="sxs-lookup"><span data-stu-id="3ef61-106">The **Report Selections** pages specify which report will be printed in different situations.</span></span> <span data-ttu-id="3ef61-107">[!INCLUDE [prod_short](includes/prod_short.md)] indeholder standardkonfigurationer, men du kan selvfølgelig ændre disse standarder.</span><span class="sxs-lookup"><span data-stu-id="3ef61-107">[!INCLUDE [prod_short](includes/prod_short.md)] includes default configurations, but of course you can change these defaults.</span></span> <span data-ttu-id="3ef61-108">Du kan også tilføje rapporter til **Rapportvalg**-siderne, hvis du f.eks. vil udskrive mere end en rapport pr.dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="3ef61-108">You can also add reports to the **Report Selection** pages if you want to print more than one report per document type, for example.</span></span>  

## <a name="available-report-selections"></a><span data-ttu-id="3ef61-109">Tilgængelige rapportvalg</span><span class="sxs-lookup"><span data-stu-id="3ef61-109">Available report selections</span></span>

<span data-ttu-id="3ef61-110">[!INCLUDE [prod_short](includes/prod_short.md)] indeholder forskellige **rapportvalg**-sider til forskellige områder.</span><span class="sxs-lookup"><span data-stu-id="3ef61-110">[!INCLUDE [prod_short](includes/prod_short.md)] includes different **Report Selection** pages for different areas.</span></span> <span data-ttu-id="3ef61-111">I følgende tabel beskrives det, hvor du kan finde oplysninger om de forskellige sider.</span><span class="sxs-lookup"><span data-stu-id="3ef61-111">The following tables describes where you can find information about the different pages.</span></span>  

|<span data-ttu-id="3ef61-112">Område eller en opgave</span><span class="sxs-lookup"><span data-stu-id="3ef61-112">Area or task</span></span>  |<span data-ttu-id="3ef61-113">Lær mere</span><span class="sxs-lookup"><span data-stu-id="3ef61-113">Learn more</span></span>|
|--------------|----------|
|<span data-ttu-id="3ef61-114">Eksempel på, hvordan Rapportvalg fungerer (salg)</span><span class="sxs-lookup"><span data-stu-id="3ef61-114">Example of how report selection works (Sales)</span></span>|[<span data-ttu-id="3ef61-115">Rapportvalg til salgsdokumenter</span><span class="sxs-lookup"><span data-stu-id="3ef61-115">Report selection for sales documents</span></span>](#example-report-selection-for-sales-documents)|
|<span data-ttu-id="3ef61-116">Standardlayout for e-mails med salgs-og købsdokumenter</span><span class="sxs-lookup"><span data-stu-id="3ef61-116">Default layout for emails with sales and purchase documents</span></span>  |[<span data-ttu-id="3ef61-117">Angiv genanvendelig e-mailtekst og layout til salgs-og købsdokumenter</span><span class="sxs-lookup"><span data-stu-id="3ef61-117">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|<span data-ttu-id="3ef61-118">Definere checklayout</span><span class="sxs-lookup"><span data-stu-id="3ef61-118">Define check layouts</span></span>     |[<span data-ttu-id="3ef61-119">Vælge et checklayout</span><span class="sxs-lookup"><span data-stu-id="3ef61-119">Select a Check Layout</span></span>](finance-how-define-check-layouts.md) |
|<span data-ttu-id="3ef61-120">Definere rapporter for momsrapportering (Tyskland)</span><span class="sxs-lookup"><span data-stu-id="3ef61-120">Define reports for VAT reporting (Germany)</span></span>|[<span data-ttu-id="3ef61-121">Konfigurere rapporter til moms og Intrastat</span><span class="sxs-lookup"><span data-stu-id="3ef61-121">Set Up Reports for VAT and Intrastat</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> <span data-ttu-id="3ef61-122">Din [!INCLUDE [prod_short](includes/prod_short.md)]kan f.eks. omfatte yderligere **Rapportvalg**-sider, afhængigt af f. eks. og branche.</span><span class="sxs-lookup"><span data-stu-id="3ef61-122">Your [!INCLUDE [prod_short](includes/prod_short.md)] can include additional **Report Selection** pages, depending on your location and industry, for example.</span></span> <span data-ttu-id="3ef61-123">Du kan altid kontrollere opsætningen ved at vælge den ![Elpære, der åbner Fortæl mig-funktionsikonet](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), og skrive **Rapportvalg** og derefter vælge det relevante link.</span><span class="sxs-lookup"><span data-stu-id="3ef61-123">You can always check your setup by choosing the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, entering **Report Selections**, and then choose the relevant link.</span></span>

<span data-ttu-id="3ef61-124">Standardversionen af [!INCLUDE [prod_short](includes/prod_short.md)] inkluderer følgende **Rapportsektion**-sider:</span><span class="sxs-lookup"><span data-stu-id="3ef61-124">The default version of [!INCLUDE [prod_short](includes/prod_short.md)] includes the following **Report Section** pages:</span></span>

* <span data-ttu-id="3ef61-125">**Rapportvalg - salg**</span><span class="sxs-lookup"><span data-stu-id="3ef61-125">**Report Selection - Sales**</span></span>  
* <span data-ttu-id="3ef61-126">**Rapportvalg - køb**</span><span class="sxs-lookup"><span data-stu-id="3ef61-126">**Report Selection - Purchase**</span></span>  
* <span data-ttu-id="3ef61-127">**Rapportvalg - lager**</span><span class="sxs-lookup"><span data-stu-id="3ef61-127">**Report Selection - Inventory**</span></span>  
* <span data-ttu-id="3ef61-128">**Rapportvalg - pengestrøm**</span><span class="sxs-lookup"><span data-stu-id="3ef61-128">**Report Selection - Cash Flow**</span></span>  
* <span data-ttu-id="3ef61-129">**Rapporten Valg - lager**</span><span class="sxs-lookup"><span data-stu-id="3ef61-129">**Report Selection - Warehouse**</span></span>  
* <span data-ttu-id="3ef61-130">**Rapportvalg - bankkonto**</span><span class="sxs-lookup"><span data-stu-id="3ef61-130">**Report Selection - Bank Account**</span></span>  
* <span data-ttu-id="3ef61-131">**Rapportvalg - rykkere og rentenotaer**</span><span class="sxs-lookup"><span data-stu-id="3ef61-131">**Report Selections Reminder/Finance Charge**</span></span>  

## <a name="example-report-selection-for-sales-documents"></a><span data-ttu-id="3ef61-132">Eksempel: Rapportvalg til salgsdokumenter</span><span class="sxs-lookup"><span data-stu-id="3ef61-132">Example: Report selection for sales documents</span></span>

<span data-ttu-id="3ef61-133">**Rapportvalget - salg**-side definerer de standardrapporter, der skal bruges i forskellige scenarier for hver relateret dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="3ef61-133">The **Report Selection - Sales** page defines the default reports to use in different scenarios for each related document type.</span></span> <span data-ttu-id="3ef61-134">Vælge et dokumenttype i feltet **Forbrug** og tilføj eller gennemse rapportvalget.</span><span class="sxs-lookup"><span data-stu-id="3ef61-134">Choose a document type in the **Usage** field, and then add or review the report selection.</span></span> <span data-ttu-id="3ef61-135">Du kan oprette mere end én rapport og den rækkefølge, som rapporter skal sendes eller udskrives i.</span><span class="sxs-lookup"><span data-stu-id="3ef61-135">You can set up more than one report and the order of sequence that the reports must be sent or printed in.</span></span>  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="3ef61-136">Visse dokumenttyper kan sendes som vedhæftede filer i e-mails, og andre kan ikke.</span><span class="sxs-lookup"><span data-stu-id="3ef61-136">Some types of document can be sent as email attachments, and others cannot.</span></span> <span data-ttu-id="3ef61-137">Hver **Rapportvalg**-side viser yderligere felter, hvis typen understøtter e-mail fra kassen.</span><span class="sxs-lookup"><span data-stu-id="3ef61-137">Each **Report Selection** page shows additional fields if the type support email out of the box.</span></span>  

<span data-ttu-id="3ef61-138">I **Rapportvalget-salg** og **Rapportvalg-køb**-sider kan du f. eks. oprette e-mail med følgende felter:</span><span class="sxs-lookup"><span data-stu-id="3ef61-138">For example, in the **Report Selection - Sales** and **Report Selection - Purchase** pages, the following fields help you set up emailing:</span></span>

|<span data-ttu-id="3ef61-139">Feltnavn</span><span class="sxs-lookup"><span data-stu-id="3ef61-139">Field name</span></span> |<span data-ttu-id="3ef61-140">Description</span><span class="sxs-lookup"><span data-stu-id="3ef61-140">Description</span></span>  |
|-----------|-------------|
|<span data-ttu-id="3ef61-141">**Brug til brødtekst i mail**</span><span class="sxs-lookup"><span data-stu-id="3ef61-141">**Use for Email Body**</span></span>| <span data-ttu-id="3ef61-142">Angiver, at opsummerede oplysninger, f.eks. fakturanummer, forfaldsdato og tilknytning til betalingstjeneste, indsættes i meddelelsesteksten på den mail, som du sender.</span><span class="sxs-lookup"><span data-stu-id="3ef61-142">Specifies that summarized information, such as invoice number, due date, and payment service link, will be inserted in the body of the email that you send.</span></span>        |
|<span data-ttu-id="3ef61-143">**Brug til vedhæftet fil i mail**</span><span class="sxs-lookup"><span data-stu-id="3ef61-143">**Use for Email Attachment**</span></span>| <span data-ttu-id="3ef61-144">Angiver, at det relaterede bilag vedhæftes mailen.</span><span class="sxs-lookup"><span data-stu-id="3ef61-144">Specifies that the related document will be attached to the email.</span></span>|
|<span data-ttu-id="3ef61-145">**Layoutbeskrivelse for brødtekst i mail**</span><span class="sxs-lookup"><span data-stu-id="3ef61-145">**Email Body Layout Description**</span></span>|<span data-ttu-id="3ef61-146">Angiver det e-mail-tekstformat, der bruges, typisk et brugerdefineret rapportlayout.</span><span class="sxs-lookup"><span data-stu-id="3ef61-146">Specifies the email body layout that is used, typically a custom report layout.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3ef61-147">Se også</span><span class="sxs-lookup"><span data-stu-id="3ef61-147">See also</span></span>

[<span data-ttu-id="3ef61-148">Angiv genanvendelig e-mailtekst og layout til salgs-og købsdokumenter</span><span class="sxs-lookup"><span data-stu-id="3ef61-148">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[<span data-ttu-id="3ef61-149">Vælge et checklayout</span><span class="sxs-lookup"><span data-stu-id="3ef61-149">Select a Check Layout</span></span>](finance-how-define-check-layouts.md)  
[<span data-ttu-id="3ef61-150">Konfigurere rapporter til moms og Intrastat (Tyskland)</span><span class="sxs-lookup"><span data-stu-id="3ef61-150">Set Up Reports for VAT and Intrastat (Germany)</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[<span data-ttu-id="3ef61-151">Administrere rapport- og dokumentlayout</span><span class="sxs-lookup"><span data-stu-id="3ef61-151">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
[<span data-ttu-id="3ef61-152">Angiv dokumentlayout for debitorer og leverandører</span><span class="sxs-lookup"><span data-stu-id="3ef61-152">Define Document Layouts for Customers and Vendors</span></span>](ui-define-customer-vendor-document-layouts.md)  
[<span data-ttu-id="3ef61-153">Installation af printere</span><span class="sxs-lookup"><span data-stu-id="3ef61-153">Set Up Printers</span></span>](ui-specify-printer-selection-reports.md)  
