---
title: OIOUB-udvidelse til elektronisk fakturering | Microsoft Docs
description: Udvidelsen gør det let at sende salgs- og servicefakturaer, kreditnotaer, rentenotaer og rykkere til kunder i den danske offentlige sektor elektronisk i OIOUBL-format (Offentlig Information Online UBL).
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 329767ec708ef54f5382fa67a570abe7af3f9706
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749664"
---
# <a name="the-oioubl-extension-for-electronic-invoicing-in-denmark"></a><span data-ttu-id="cc1c9-103">Udvidelsen OIOUBL til elektronisk fakturering i Danmark</span><span class="sxs-lookup"><span data-stu-id="cc1c9-103">The OIOUBL Extension for Electronic Invoicing in Denmark</span></span>
<span data-ttu-id="cc1c9-104">Når du sælger varer eller tjenesteydelser til debitorer i den danske offentlige sektor, skal du sende dokumenter til kunden elektronisk i en XML-fil, der er struktureret til at opfylde kravene i en eller flere OIOUBL-profiler (Offentlig oplysninger Online - Universal Business Language).</span><span class="sxs-lookup"><span data-stu-id="cc1c9-104">When you sell goods or services to customers in the Danish public sector, you must submit documents to the customer electronically in an XML file that is structured to meet the requirements of one or more Offentlig Information Online - Universal Business Language (OIOUBL) profiles.</span></span>  

<span data-ttu-id="cc1c9-105">Udvidelsen OIOUBL i [!INCLUDE[prod_short](../../includes/prod_short.md)] gør det nemt at oprette disse XML-dokumenter for bogførte salgs- og servicefakturaer, kreditnotaer og udstedte rykkere (som omfatter rentenotaer).</span><span class="sxs-lookup"><span data-stu-id="cc1c9-105">The OIOUBL extension in [!INCLUDE[prod_short](../../includes/prod_short.md)] makes it easy to generate these XML documents for posted sales and service invoices, credit memos, and issued reminders (which include finance charge memos).</span></span>  

<span data-ttu-id="cc1c9-106">De aktuelle krav til at sende elektroniske fakturaer er baseret på UBL version 2.0-standarden.</span><span class="sxs-lookup"><span data-stu-id="cc1c9-106">The current requirements for sending electronic invoices are based on UBL version 2.0 standard.</span></span> <span data-ttu-id="cc1c9-107">Du kan finde flere oplysninger på webstedet [https://aka.ms/OasisUblSite](https://aka.ms/OasisUblSite).</span><span class="sxs-lookup"><span data-stu-id="cc1c9-107">For more information, see the [https://aka.ms/OasisUblSite](https://aka.ms/OasisUblSite) web site.</span></span>

<span data-ttu-id="cc1c9-108">Du kan få yderligere oplysninger om OIOUBL generelt på webstedet med [OIOUBL-onlinedokumentationen](http://www.oioubl.info/classes/da/index.html) og webstedet til [Digitaliseringsstyrelsenl](https://digst.dk/).</span><span class="sxs-lookup"><span data-stu-id="cc1c9-108">For more information about OIOUBL in general, see the website for [Online OIOUBL Documentation](http://www.oioubl.info/classes/da/index.html), and the [Digitaliseringsstyrelsen](https://digst.dk/) website.</span></span>  

## <a name="getting-started-with-the-oioubl-extension"></a><span data-ttu-id="cc1c9-109">Kom i gang med udvidelsen OIOUBL</span><span class="sxs-lookup"><span data-stu-id="cc1c9-109">Getting Started with the OIOUBL Extension</span></span>  
<span data-ttu-id="cc1c9-110">Som standard er OUOUBL-udvidelsen installeret i [!INCLUDE[prod_short](../../includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="cc1c9-110">By default, the OIOUBL extension is installed in [!INCLUDE[prod_short](../../includes/prod_short.md)].</span></span> <span data-ttu-id="cc1c9-111">Men, der er et par ting, du skal gøre, før du kan bruge udvidelsen:</span><span class="sxs-lookup"><span data-stu-id="cc1c9-111">However, there are a few things to do before you can use the extension:</span></span>

* <span data-ttu-id="cc1c9-112">Konfigurere betalingsformer, betalingsbetingelser og varegebyrer.</span><span class="sxs-lookup"><span data-stu-id="cc1c9-112">Set up payment methods, payment terms, and item charges.</span></span>
* <span data-ttu-id="cc1c9-113">Konfigurere kunder til OIOUBL ved at angive en kontokode, OILUBL-profilen, der skal bruges til at udveksle dokumenter, og kundens geografiske placeringsnummer (GLN).</span><span class="sxs-lookup"><span data-stu-id="cc1c9-113">Set up customers for OIOUBL by specifying an account code, the OIOUBL profile to use to exchange documents, and the customer's Geographic Location Number (GLN).</span></span>

<span data-ttu-id="cc1c9-114">Du kan få flere oplysninger i [Konfigurere udvidelsen OIOUBL](how-to-set-up-oioubl.md).</span><span class="sxs-lookup"><span data-stu-id="cc1c9-114">For more information, see [Set Up the OIOUBL Extension](how-to-set-up-oioubl.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="cc1c9-115">Se også</span><span class="sxs-lookup"><span data-stu-id="cc1c9-115">See Also</span></span>

[<span data-ttu-id="cc1c9-116">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="cc1c9-116">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  
[<span data-ttu-id="cc1c9-117">Konfigurere OIOUBL-udvidelsen</span><span class="sxs-lookup"><span data-stu-id="cc1c9-117">Set Up the OIOUBL Extension</span></span>](how-to-set-up-oioubl.md)  
[<span data-ttu-id="cc1c9-118">Oprette elektroniske dokumenter i et OIOUBL-format</span><span class="sxs-lookup"><span data-stu-id="cc1c9-118">Create Electronic Documents in an OIOUBL Format</span></span>](how-to-create-electronic-documents-by-using-oioubl.md)  
