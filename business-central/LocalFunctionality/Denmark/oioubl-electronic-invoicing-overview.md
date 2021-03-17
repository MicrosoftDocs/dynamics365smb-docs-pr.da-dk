---
title: Oversigt over elektronisk OIOUBL-fakturering | Microsoft Docs
description: Få mere at vide om, hvordan Business Central understøtter behovet for at sende salgsdokumenter til den danske offentlige sektor elektronisk i OIOUBL-format.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c438b1005963ce7b7538ae022c0949f4810eec38
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493141"
---
# <a name="oioubl-electronic-invoicing-overview"></a><span data-ttu-id="091dd-103">Oversigt over elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="091dd-103">OIOUBL Electronic Invoicing Overview</span></span>
<span data-ttu-id="091dd-104">Virksomheder skal sende salgsfakturaer, kreditnotaer, rentenotaer og rykkere til den danske offentlige sektor elektronisk i OIOUBL-format (Offentlig Information Online UBL).</span><span class="sxs-lookup"><span data-stu-id="091dd-104">Companies must send sales invoices, credit memos, finance charge memos, and reminders to the Danish public sector electronically in the Offentlig Information Online UBL (OIOUBL) format.</span></span> <span data-ttu-id="091dd-105">Hvis en virksomhed ikke sender disse dokumenter elektronisk, kan myndighederne nægte at betale.</span><span class="sxs-lookup"><span data-stu-id="091dd-105">If a company does not send these documents electronically, the authorities can deny payment.</span></span>  

<span data-ttu-id="091dd-106">Du kan finde flere oplysninger om elektronisk OIOUBL-fakturering i [oioubl.info](http://www.oioubl.info/classes/da/index.html).</span><span class="sxs-lookup"><span data-stu-id="091dd-106">For more information about OIOUBL electronic invoicing, see [oioubl.info](http://www.oioubl.info/classes/da/index.html).</span></span>  

## <a name="implementation-in-prod_short"></a><span data-ttu-id="091dd-107">Implementering i [!INCLUDE[prod_short](../../includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="091dd-107">Implementation in [!INCLUDE[prod_short](../../includes/prod_short.md)]</span></span>  
<span data-ttu-id="091dd-108">De aktuelle krav til at sende elektroniske fakturaer er baseret på OIOUBL, som er baseret på UBL (Universal Business Language) version 2.0-standarden.</span><span class="sxs-lookup"><span data-stu-id="091dd-108">The current requirements for sending electronic invoices are based on OIOUBL, which is based on the Universal Business Language (UBL) version 2.0 standard.</span></span> <span data-ttu-id="091dd-109">Du kan finde flere oplysninger på [OASIS UBL](https://aka.ms/OasisUblSite)-webstedet.</span><span class="sxs-lookup"><span data-stu-id="091dd-109">For more information, see the [OASIS UBL](https://aka.ms/OasisUblSite) web site.</span></span> <span data-ttu-id="091dd-110">De genererede XML-dokumenter kan derefter sendes til debitoren.</span><span class="sxs-lookup"><span data-stu-id="091dd-110">The generated XML documents can then be sent to the customer.</span></span>  

<span data-ttu-id="091dd-111">For at sende dokumenter elektronisk skal du knytte europæiske EAN-lokationsnumre (European Article Numbering) og kontokoder til de relevante debitorer på siden **Debitorkort**.</span><span class="sxs-lookup"><span data-stu-id="091dd-111">To send documents electronically, you must assign European Article Numbering (EAN) location numbers and account codes to the relevant customers on the **Customer Card** page.</span></span> <span data-ttu-id="091dd-112">Du kan få flere oplysninger i [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md).</span><span class="sxs-lookup"><span data-stu-id="091dd-112">For more information, see [Set Up Customers for OIOUBL](how-to-set-up-customers-for-oioubl.md).</span></span> <span data-ttu-id="091dd-113">Disse tal medtages, når du opretter dokumenter og bogfører eller udsteder dem.</span><span class="sxs-lookup"><span data-stu-id="091dd-113">These numbers are the included when you create documents, and post or issue them.</span></span> <span data-ttu-id="091dd-114">Når dokumenterne er bogførte eller udstedt, kan du oprette elektroniske versioner af dem, som kan sendes til debitoren.</span><span class="sxs-lookup"><span data-stu-id="091dd-114">After the documents have been posted or issued, you can create electronic versions to be sent to the customer.</span></span> <span data-ttu-id="091dd-115">Du kan sende følgende typer dokumenter:</span><span class="sxs-lookup"><span data-stu-id="091dd-115">You can submit the following types of documents:</span></span>  

- <span data-ttu-id="091dd-116">Salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="091dd-116">Sales invoice</span></span>  
- <span data-ttu-id="091dd-117">Servicefaktura</span><span class="sxs-lookup"><span data-stu-id="091dd-117">Service invoice</span></span>  
- <span data-ttu-id="091dd-118">Salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="091dd-118">Sales credit memo</span></span>  
- <span data-ttu-id="091dd-119">Servicekreditnota</span><span class="sxs-lookup"><span data-stu-id="091dd-119">Service credit memo</span></span>  
- <span data-ttu-id="091dd-120">Rentenota</span><span class="sxs-lookup"><span data-stu-id="091dd-120">Finance charge memo</span></span>  
- <span data-ttu-id="091dd-121">Rykker</span><span class="sxs-lookup"><span data-stu-id="091dd-121">Reminder</span></span>  

<span data-ttu-id="091dd-122">De elektroniske dokumenter gemmes på de placeringer, som er angivet i Salgsopsætning.</span><span class="sxs-lookup"><span data-stu-id="091dd-122">The electronic documents are stored in the locations that are defined in the Sales & Receivables Setup.</span></span>  

## <a name="oioubl-profiles"></a><span data-ttu-id="091dd-123">OIOUBL-profiler</span><span class="sxs-lookup"><span data-stu-id="091dd-123">OIOUBL Profiles</span></span>

<span data-ttu-id="091dd-124">Kunderne kan bruge en profil, der er baseret på de danske OIOUBL-definitioner, eller de kan bruge en profil, der er baseret på OIOUBL-implementering af NES-definitionerne (Northern European Subset).</span><span class="sxs-lookup"><span data-stu-id="091dd-124">Your customers can use a profile that is based on the Danish OIOUBL definitions, or they can use a profile that is based on the OIOUBL implementation of the Northern European Subset (NES) definitions.</span></span> <span data-ttu-id="091dd-125">Nogle profiler kræver, at der sendes svar, når et elektronisk dokument modtages.</span><span class="sxs-lookup"><span data-stu-id="091dd-125">Some profiles require responses to be sent when an electronic document is received.</span></span> <span data-ttu-id="091dd-126">Du kan angive, hvilken profil de fleste af dine kunder bruger.</span><span class="sxs-lookup"><span data-stu-id="091dd-126">You can set up which profile most of your customers use.</span></span> <span data-ttu-id="091dd-127">Hvis en kunde bruger en anden profil, kan du ændre dette på debitorkortet.</span><span class="sxs-lookup"><span data-stu-id="091dd-127">If a customer uses a different profile, you can change that in the customer card.</span></span> <span data-ttu-id="091dd-128">For eksempel kan du angive, at standardprofilen er Procurement-OrdSim-BilSim-1.0, men at kunden 10000 kræver profilen urn: urn:www.nesubl.eu:profiles:profile5:ver2.0.</span><span class="sxs-lookup"><span data-stu-id="091dd-128">For example, you can specify that the default profile is Procurement-OrdSim-BilSim-1.0, but that customer 10000 requires profile urn:www.nesubl.eu:profiles:profile5:ver2.0.</span></span> <span data-ttu-id="091dd-129">Der er flere oplysninger i [Konfigurere OIOUBL](how-to-set-up-oioubl.md).</span><span class="sxs-lookup"><span data-stu-id="091dd-129">For more information, see [Set Up OIOUBL](how-to-set-up-oioubl.md).</span></span>  

<span data-ttu-id="091dd-130">Du kan finde flere oplysninger i emnet om OIOUBL-profiler i afsnittet Ofte stillede spørgsmål på [Digitaliseringsstyrelsen](https://aka.ms/Digitaliseringsstyrelsen).</span><span class="sxs-lookup"><span data-stu-id="091dd-130">For more information, see the entry on OIOUBL profiles in the frequently asked questions section at [Digitaliseringsstyrelsen](https://aka.ms/Digitaliseringsstyrelsen).</span></span>  

## <a name="see-also"></a><span data-ttu-id="091dd-131">Se også</span><span class="sxs-lookup"><span data-stu-id="091dd-131">See Also</span></span>

[<span data-ttu-id="091dd-132">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="091dd-132">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  
 [<span data-ttu-id="091dd-133">Konfigurere OIOUBL</span><span class="sxs-lookup"><span data-stu-id="091dd-133">Set Up OIOUBL</span></span>](how-to-set-up-oioubl.md)  
 [<span data-ttu-id="091dd-134">Konfigurere kunder til OIOUBL</span><span class="sxs-lookup"><span data-stu-id="091dd-134">Set Up Customers for OIOUBL</span></span>](how-to-set-up-customers-for-oioubl.md)  
 [<span data-ttu-id="091dd-135">Oprette elektroniske dokumenter ved hjælp af OIOUBL</span><span class="sxs-lookup"><span data-stu-id="091dd-135">Create Electronic Documents by Using OIOUBL</span></span>](how-to-create-electronic-documents-by-using-oioubl.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]