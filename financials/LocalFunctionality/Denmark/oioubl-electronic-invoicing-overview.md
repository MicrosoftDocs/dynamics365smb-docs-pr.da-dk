---
title: Oversigt over elektronisk OIOUBL-fakturering | Microsoft Docs
description: "Virksomheder skal sende salgsfakturaer, kreditnotaer, rentenotaer og rykkere til den danske offentlige sektor elektronisk i OIOUBL-format (Offentlig Information Online UBL). Hvis en virksomhed ikke sender disse dokumenter elektronisk, kan myndighederne nægte at betale."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 47c79423dd590c5c8128c51c6a4f159ac6c2c5e8
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="oioubl-electronic-invoicing-overview"></a><span data-ttu-id="923cd-104">Oversigt over elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="923cd-104">OIOUBL Electronic Invoicing Overview</span></span>
<span data-ttu-id="923cd-105">Virksomheder skal sende salgsfakturaer, kreditnotaer, rentenotaer og rykkere til den danske offentlige sektor elektronisk i OIOUBL-format (Offentlig Information Online UBL).</span><span class="sxs-lookup"><span data-stu-id="923cd-105">Companies must send sales invoices, credit memos, finance charge memos, and reminders to the Danish public sector electronically in the Offentlig Information Online UBL (OIOUBL) format.</span></span> <span data-ttu-id="923cd-106">Hvis en virksomhed ikke sender disse dokumenter elektronisk, kan myndighederne nægte at betale.</span><span class="sxs-lookup"><span data-stu-id="923cd-106">If a company does not send these documents electronically, the authorities can deny payment.</span></span>  

<span data-ttu-id="923cd-107">Du kan finde flere oplysninger om elektronisk OIOUBL-fakturering i [oioubl.info](http://www.oioubl.info).</span><span class="sxs-lookup"><span data-stu-id="923cd-107">For more information about OIOUBL electronic invoicing, see [oioubl.info](http://www.oioubl.info).</span></span>  

## <a name="implementation-in-included365finincludesd365finmdmd"></a><span data-ttu-id="923cd-108">Implementering i [!INCLUDE[d365fin](../../includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="923cd-108">Implementation in [!INCLUDE[d365fin](../../includes/d365fin_md.md)]</span></span>  
<span data-ttu-id="923cd-109">De aktuelle krav til at sende elektroniske fakturaer er baseret på OIOUBL, som er baseret på UBL (Universal Business Language) version 2.0-standarden.</span><span class="sxs-lookup"><span data-stu-id="923cd-109">The current requirements for sending electronic invoices are based on OIOUBL, which is based on the Universal Business Language (UBL) version 2.0 standard.</span></span> <span data-ttu-id="923cd-110">Du kan finde flere oplysninger på [OASIS UBL](http://go.microsoft.com/fwlink/?LinkId=212593)-webstedet.</span><span class="sxs-lookup"><span data-stu-id="923cd-110">For more information, see the [OASIS UBL](http://go.microsoft.com/fwlink/?LinkId=212593) website.</span></span> <span data-ttu-id="923cd-111">De genererede XML-dokumenter kan derefter sendes til debitoren.</span><span class="sxs-lookup"><span data-stu-id="923cd-111">The generated XML documents can then be sent to the customer.</span></span>  

<span data-ttu-id="923cd-112">For at sende dokumenter elektronisk skal du knytte europæiske EAN-lokationsnumre (European Article Numbering) og kontokoder til de relevante debitorer i vinduet **Debitorkort**.</span><span class="sxs-lookup"><span data-stu-id="923cd-112">To send documents electronically, you must assign European Article Numbering (EAN) location numbers and account codes to the relevant customers in the **Customer Card** window.</span></span> <span data-ttu-id="923cd-113">Du kan få flere oplysninger i [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md).</span><span class="sxs-lookup"><span data-stu-id="923cd-113">For more information, see [Set Up Customers for OIOUBL](how-to-set-up-customers-for-oioubl.md).</span></span> <span data-ttu-id="923cd-114">Disse tal medtages, når du opretter dokumenter og bogfører eller udsteder dem.</span><span class="sxs-lookup"><span data-stu-id="923cd-114">These numbers are the included when you create documents, and post or issue them.</span></span> <span data-ttu-id="923cd-115">Når dokumenterne er bogførte eller udstedt, kan du oprette elektroniske versioner af dem, som kan sendes til debitoren.</span><span class="sxs-lookup"><span data-stu-id="923cd-115">After the documents have been posted or issued, you can create electronic versions to be sent to the customer.</span></span> <span data-ttu-id="923cd-116">Du kan sende følgende typer dokumenter:</span><span class="sxs-lookup"><span data-stu-id="923cd-116">You can submit the following types of documents:</span></span>  

-   <span data-ttu-id="923cd-117">Salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="923cd-117">Sales invoice</span></span>  
-   <span data-ttu-id="923cd-118">Servicefaktura</span><span class="sxs-lookup"><span data-stu-id="923cd-118">Service invoice</span></span>  
-   <span data-ttu-id="923cd-119">Salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="923cd-119">Sales credit memo</span></span>  
-   <span data-ttu-id="923cd-120">Servicekreditnota</span><span class="sxs-lookup"><span data-stu-id="923cd-120">Service credit memo</span></span>  
-   <span data-ttu-id="923cd-121">Rentenota</span><span class="sxs-lookup"><span data-stu-id="923cd-121">Finance charge memo</span></span>  
-   <span data-ttu-id="923cd-122">Rykker</span><span class="sxs-lookup"><span data-stu-id="923cd-122">Reminder</span></span>  

<span data-ttu-id="923cd-123">De elektroniske dokumenter gemmes på de placeringer, som er angivet i Salgsopsætning.</span><span class="sxs-lookup"><span data-stu-id="923cd-123">The electronic documents are stored in the locations that are defined in the Sales & Receivables Setup.</span></span>  

## <a name="oioubl-profiles"></a><span data-ttu-id="923cd-124">OIOUBL-profiler</span><span class="sxs-lookup"><span data-stu-id="923cd-124">OIOUBL Profiles</span></span>  
<span data-ttu-id="923cd-125">Kunderne kan bruge en profil, der er baseret på de danske OIOUBL-definitioner, eller de kan bruge en profil, der er baseret på OIOUBL-implementering af NES-definitionerne (Northern European Subset).</span><span class="sxs-lookup"><span data-stu-id="923cd-125">Your customers can use a profile that is based on the Danish OIOUBL definitions, or they can use a profile that is based on the OIOUBL implementation of the Northern European Subset (NES) definitions.</span></span> <span data-ttu-id="923cd-126">Nogle profiler kræver, at der sendes svar, når et elektronisk dokument modtages.</span><span class="sxs-lookup"><span data-stu-id="923cd-126">Some profiles require responses to be sent when an electronic document is received.</span></span> <span data-ttu-id="923cd-127">Du kan angive, hvilken profil de fleste af dine kunder bruger.</span><span class="sxs-lookup"><span data-stu-id="923cd-127">You can set up which profile most of your customers use.</span></span> <span data-ttu-id="923cd-128">Hvis en kunde bruger en anden profil, kan du ændre dette på debitorkortet.</span><span class="sxs-lookup"><span data-stu-id="923cd-128">If a customer uses a different profile, you can change that in the customer card.</span></span> <span data-ttu-id="923cd-129">For eksempel kan du angive, at standardprofilen er Procurement-OrdSim-BilSim-1.0, men at kunden 10000 kræver profilen urn: urn:www.nesubl.eu:profiles:profile5:ver2.0.</span><span class="sxs-lookup"><span data-stu-id="923cd-129">For example, you can specify that the default profile is Procurement-OrdSim-BilSim-1.0, but that customer 10000 requires profile urn:www.nesubl.eu:profiles:profile5:ver2.0.</span></span> <span data-ttu-id="923cd-130">Der er flere oplysninger i [Konfigurere OIOUBL](how-to-set-up-oioubl.md).</span><span class="sxs-lookup"><span data-stu-id="923cd-130">For more information, see [Set Up OIOUBL](how-to-set-up-oioubl.md).</span></span>  

<span data-ttu-id="923cd-131">Du kan finde flere oplysninger i emnet om OIOUBL-profiler i afsnittet Ofte stillede spørgsmål på [Digitaliseringsstyrelsen](http://go.microsoft.com/fwlink/?LinkId=267236).</span><span class="sxs-lookup"><span data-stu-id="923cd-131">For more information, see the entry on OIOUBL profiles in the frequently asked questions section at [Digitaliseringsstyrelsen](http://go.microsoft.com/fwlink/?LinkId=267236).</span></span>  

## <a name="see-also"></a><span data-ttu-id="923cd-132">Se også</span><span class="sxs-lookup"><span data-stu-id="923cd-132">See Also</span></span>  
[<span data-ttu-id="923cd-133">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="923cd-133">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  
 <span data-ttu-id="923cd-134">[Konfigurere OIOUBL](how-to-set-up-oioubl.md) </span><span class="sxs-lookup"><span data-stu-id="923cd-134">[Set Up OIOUBL](how-to-set-up-oioubl.md) </span></span>  
 <span data-ttu-id="923cd-135">[Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md) </span><span class="sxs-lookup"><span data-stu-id="923cd-135">[Set Up Customers for OIOUBL](how-to-set-up-customers-for-oioubl.md) </span></span>  
 <span data-ttu-id="923cd-136">[Oprette elektroniske dokumenter ved hjælp af OIOUBL](how-to-create-electronic-documents-by-using-oioubl.md) </span><span class="sxs-lookup"><span data-stu-id="923cd-136">[Create Electronic Documents by Using OIOUBL](how-to-create-electronic-documents-by-using-oioubl.md) </span></span>  
 [<span data-ttu-id="923cd-137">EAN-lokationsnummer</span><span class="sxs-lookup"><span data-stu-id="923cd-137">EAN Location Number</span></span>](ean-location-number.md)

