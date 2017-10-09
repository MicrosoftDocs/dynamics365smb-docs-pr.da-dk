---
title: EAN-lokationsnummer | Microsoft Docs
description: "Et EAN-lokationsnummer (European Article Numbering) er en elektronisk adresse, som du kan bruge, når du sender en elektronisk faktura. Dette nummer identificerer entydigt køberens faktureringsadresse. EAN-lokationsnumre kan bruges i lande uden for Europa og kaldes også GLN (Global Location Numbers)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f75e61cb9fdc3649698c68e83f4f861d30e797cd
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="ean-location-number"></a><span data-ttu-id="70c90-105">EAN-lokationsnummer</span><span class="sxs-lookup"><span data-stu-id="70c90-105">EAN Location Number</span></span>
<span data-ttu-id="70c90-106">Et EAN-lokationsnummer (European Article Numbering) er en elektronisk adresse, som du kan bruge, når du sender en elektronisk faktura.</span><span class="sxs-lookup"><span data-stu-id="70c90-106">A European Article Numbering (EAN) location number is an electronic address that you can use when you send an electronic invoice.</span></span> <span data-ttu-id="70c90-107">Dette nummer identificerer entydigt køberens faktureringsadresse.</span><span class="sxs-lookup"><span data-stu-id="70c90-107">This number uniquely identifies the buyer’s billing address.</span></span> <span data-ttu-id="70c90-108">EAN-lokationsnumre kan bruges i lande uden for Europa og kaldes også GLN (Global Location Numbers).</span><span class="sxs-lookup"><span data-stu-id="70c90-108">EAN location numbers can be used in countries/regions outside Europe and are also referred to as Global Location Numbers (GLN).</span></span>  

## <a name="ean-location-numbers-in-included365finincludesd365finmdmd"></a><span data-ttu-id="70c90-109">EAN-lokationsnumre i [!INCLUDE[d365fin](../../includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="70c90-109">EAN Location Numbers in [!INCLUDE[d365fin](../../includes/d365fin_md.md)]</span></span>  
 <span data-ttu-id="70c90-110">Afdelinger, direktorater, organer og andre organisationer i den danske offentlige sektor har EAN-lokationsnumre, som entydigt identificerer debitorens faktureringsadresse.</span><span class="sxs-lookup"><span data-stu-id="70c90-110">Departments, directorates, agencies, and other organizations in the Danish public sector have EAN location numbers, which uniquely identifies the bill-to address of the customer.</span></span> <span data-ttu-id="70c90-111">Hvis din virksomhed har en kunde i den offentlige sektor, skal du sende fakturaer og andre dokumenter elektronisk ved hjælp af Offentlig Information Online UBL (OIOUBL).</span><span class="sxs-lookup"><span data-stu-id="70c90-111">If your company has a customer who is in the public sector, you must submit invoices and other documents electronically by using Offentlig Information Online UBL (OIOUBL).</span></span> <span data-ttu-id="70c90-112">For at gøre det, skal du angive kundens EAN-lokationsnummer.</span><span class="sxs-lookup"><span data-stu-id="70c90-112">In order to do that, you must specify the customer’s EAN location number.</span></span> <span data-ttu-id="70c90-113">Du kan få flere oplysninger i [Fremgangsmåde: Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md).</span><span class="sxs-lookup"><span data-stu-id="70c90-113">For more information, see [How to: Set Up Customers for OIOUBL](how-to-set-up-customers-for-oioubl.md).</span></span>  

 <span data-ttu-id="70c90-114">Et EAN-lokationsnummer er en fast længde på 13 cifre.</span><span class="sxs-lookup"><span data-stu-id="70c90-114">An EAN location number has a fixed length of 13 digits.</span></span> <span data-ttu-id="70c90-115">Dette nummer skal behandles i sin helhed.</span><span class="sxs-lookup"><span data-stu-id="70c90-115">This number must be processed in its entirety.</span></span> <span data-ttu-id="70c90-116">Nedenfor vises et eksempel på et EAN-nummer.</span><span class="sxs-lookup"><span data-stu-id="70c90-116">The following is an example of an EAN number.</span></span>  

 <span data-ttu-id="70c90-117">**5790987654321**</span><span class="sxs-lookup"><span data-stu-id="70c90-117">**5790987654321**</span></span>  

 <span data-ttu-id="70c90-118">EAN-numre starter med et præfiks på tre cifre, som tildeles af EAN International.</span><span class="sxs-lookup"><span data-stu-id="70c90-118">EAN numbers start with a 3-digit prefix allocated by EAN International.</span></span> <span data-ttu-id="70c90-119">I Danmark er de tre første tal **579**.</span><span class="sxs-lookup"><span data-stu-id="70c90-119">For Denmark, the first three numbers are **579**.</span></span> <span data-ttu-id="70c90-120">EAN-nummeret slutter med et kontrolciffer, som beregnes på basis af de første 12 cifre.</span><span class="sxs-lookup"><span data-stu-id="70c90-120">The EAN number ends with a check digit that is calculated based on the first 12 digits.</span></span>  

## <a name="see-also"></a><span data-ttu-id="70c90-121">Se også</span><span class="sxs-lookup"><span data-stu-id="70c90-121">See Also</span></span>  
[<span data-ttu-id="70c90-122">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="70c90-122">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  
 <span data-ttu-id="70c90-123">[Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md) </span><span class="sxs-lookup"><span data-stu-id="70c90-123">[OIOUBL Electronic Invoicing Overview](oioubl-electronic-invoicing-overview.md) </span></span>  
 [<span data-ttu-id="70c90-124">Fremgangsmåde: Konfigurere kunder til OIOUBL</span><span class="sxs-lookup"><span data-stu-id="70c90-124">How to: Set Up Customers for OIOUBL</span></span>](how-to-set-up-customers-for-oioubl.md)

