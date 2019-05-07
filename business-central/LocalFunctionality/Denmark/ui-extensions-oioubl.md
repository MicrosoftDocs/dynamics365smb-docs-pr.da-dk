---
title: OIOUB-udvidelse til elektronisk fakturering | Microsoft Docs
description: Udvidelsen gør det let at sende salgs- og servicefakturaer, kreditnotaer, rentenotaer og rykkere til kunder i den danske offentlige sektor elektronisk i OIOUBL-format (Offentlig Information Online UBL).
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 6f2b9b8385ac003fc7186c26134d5401609dd12c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "917762"
---
# <a name="the-oioubl-extension-for-electronic-invoicing-in-denmark"></a><span data-ttu-id="77bf2-103">Udvidelsen OIOUBL til elektronisk fakturering i Danmark</span><span class="sxs-lookup"><span data-stu-id="77bf2-103">The OIOUBL Extension for Electronic Invoicing in Denmark</span></span>
<span data-ttu-id="77bf2-104">Når du sælger varer eller tjenesteydelser til debitorer i den danske offentlige sektor, skal du sende dokumenter til kunden elektronisk i en XML-fil, der er struktureret til at opfylde kravene i en eller flere OIOUBL-profiler (Offentlig oplysninger Online - Universal Business Language).</span><span class="sxs-lookup"><span data-stu-id="77bf2-104">When you sell goods or services to customers in the Danish public sector, you must submit documents to the customer electronically in an XML file that is structured to meet the requirements of one or more Offentlig Information Online - Universal Business Language (OIOUBL) profiles.</span></span>  

<span data-ttu-id="77bf2-105">Udvidelsen OIOUBL i [!INCLUDE[d365fin](../../includes/d365fin_md.md)] gør det nemt at oprette disse XML-dokumenter for bogførte salgs- og servicefakturaer, kreditnotaer og udstedte rykkere (som omfatter rentenotaer).</span><span class="sxs-lookup"><span data-stu-id="77bf2-105">The OIOUBL extension in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] makes it easy to generate these XML documents for posted sales and service invoices, credit memos, and issued reminders (which include finance charge memos).</span></span>  

<span data-ttu-id="77bf2-106">De aktuelle krav til at sende elektroniske fakturaer er baseret på UBL version 2.0-standarden.</span><span class="sxs-lookup"><span data-stu-id="77bf2-106">The current requirements for sending electronic invoices are based on UBL version 2.0 standard.</span></span> <span data-ttu-id="77bf2-107">Du kan finde flere oplysninger på webstedet https://aka.ms/OasisUblSite.</span><span class="sxs-lookup"><span data-stu-id="77bf2-107">For more information, see the https://aka.ms/OasisUblSite web site.</span></span>

<span data-ttu-id="77bf2-108">Yderligere oplysninger om OIOUBL generelt se webstedet for [OIOUBL-onlinedokumentation](https://www.oioubl.info), og siden [Ofte stillede spørgsmål](https://digst.dk/it-loesninger/nemhandel/anvendelse/send-en-e-faktura/spoergsmaal-og-svar/) på webstedet Digitaliseringsstyrelsen.</span><span class="sxs-lookup"><span data-stu-id="77bf2-108">For more information about OIOUBL in general, see the website for [Online OIOUBL Documentation](https://www.oioubl.info), and the [Frequently Asked Questions](https://digst.dk/it-loesninger/nemhandel/anvendelse/send-en-e-faktura/spoergsmaal-og-svar/) page on the Digitaliseringsstyrelsen website.</span></span>  

## <a name="getting-started-with-the-oioubl-extension"></a><span data-ttu-id="77bf2-109">Kom i gang med udvidelsen OIOUBL</span><span class="sxs-lookup"><span data-stu-id="77bf2-109">Getting Started with the OIOUBL Extension</span></span>  
<span data-ttu-id="77bf2-110">Som standard er OUOUBL-udvidelsen installeret i [!INCLUDE[d365fin](../../includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="77bf2-110">By default, the OIOUBL extension is installed in [!INCLUDE[d365fin](../../includes/d365fin_md.md)].</span></span> <span data-ttu-id="77bf2-111">Men, der er et par ting, du skal gøre, før du kan bruge udvidelsen:</span><span class="sxs-lookup"><span data-stu-id="77bf2-111">However, there are a few things to do before you can use the extension:</span></span>

* <span data-ttu-id="77bf2-112">Konfigurere betalingsformer, betalingsbetingelser og varegebyrer.</span><span class="sxs-lookup"><span data-stu-id="77bf2-112">Set up payment methods, payment terms, and item charges.</span></span>
* <span data-ttu-id="77bf2-113">Konfigurere kunder til OIOUBL ved at angive en kontokode, OIOUBL-profilen, der skal bruges til at udveksle dokumenter, og kundens geografiske placering nummer (GLN).</span><span class="sxs-lookup"><span data-stu-id="77bf2-113">Set up customers for OIOUBL by specifying an account code, the OILUBL profile to use to exchange documents, and the customer's Geographic Location Number (GLN).</span></span>

<span data-ttu-id="77bf2-114">Du kan få flere oplysninger i [Konfigurere udvidelsen OIOUBL](how-to-set-up-oioubl.md).</span><span class="sxs-lookup"><span data-stu-id="77bf2-114">For more information, see [Set Up the OIOUBL Extension](how-to-set-up-oioubl.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="77bf2-115">Se også</span><span class="sxs-lookup"><span data-stu-id="77bf2-115">See Also</span></span>  
[<span data-ttu-id="77bf2-116">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="77bf2-116">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  
[<span data-ttu-id="77bf2-117">Konfigurere OIOUBL-udvidelsen</span><span class="sxs-lookup"><span data-stu-id="77bf2-117">Set Up the OIOUBL Extension</span></span>](how-to-set-up-oioubl.md)  
[<span data-ttu-id="77bf2-118">Oprette elektroniske dokumenter i et OIOUBL-format</span><span class="sxs-lookup"><span data-stu-id="77bf2-118">Create Electronic Documents in an OIOUBL Format</span></span>](how-to-create-electronic-documents-by-using-oioubl.md)  
