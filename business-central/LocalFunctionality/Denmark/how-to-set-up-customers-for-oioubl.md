---
title: "Sådan konfigureres kunder til OIOUBL | Microsoft Docs"
description: "Hvis du vil oprette OIOUBL-dokumenter (Offentlig Information Online UBL) for debitorer i den offentlige sektor, skal du tilføje OIOUBL-oplysninger for de relevante debitorer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: f23dc4dd4c3dee27771076a5968a155b3e85bd17
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-customers-for-oioubl"></a><span data-ttu-id="6f620-103">Konfigurere kunder til OIOUBL</span><span class="sxs-lookup"><span data-stu-id="6f620-103">Set Up Customers for OIOUBL</span></span>
<span data-ttu-id="6f620-104">Hvis du vil oprette OIOUBL-dokumenter (Offentlig Information Online UBL) for debitorer i den offentlige sektor, skal du tilføje OIOUBL-oplysninger for de relevante debitorer.</span><span class="sxs-lookup"><span data-stu-id="6f620-104">To create Offentlig Information Online UBL (OIOUBL) documents for customers in the public sector, you must add OIOUBL information to the relevant customers.</span></span>  

 <span data-ttu-id="6f620-105">I dette emne beskrives kun de felter, der gælder for OIOUBL.</span><span class="sxs-lookup"><span data-stu-id="6f620-105">This topic only describes fields that apply to OIOUBL.</span></span> <span data-ttu-id="6f620-106">Du kan finde flere oplysninger i [Registrere nye debitorer](../../sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="6f620-106">For more information, see [Register New Customers](../../sales-how-register-new-customers.md).</span></span>  

### <a name="to-set-up-customers-for-oioubl"></a><span data-ttu-id="6f620-107">Sådan konfigureres kunder til OIOUBL</span><span class="sxs-lookup"><span data-stu-id="6f620-107">To set up customers for OIOUBL</span></span>  

1.  <span data-ttu-id="6f620-108">Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6f620-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6f620-109">Åbn den kunde, du vil konfigurere aktivere til OIOUBL.</span><span class="sxs-lookup"><span data-stu-id="6f620-109">Open the customer that you want to enable for OIOUBL.</span></span>  
3.  <span data-ttu-id="6f620-110">Udfyld felterne i oversigtspanelet **Fakturering** som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="6f620-110">On the **Invoicing** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="6f620-111">Felt</span><span class="sxs-lookup"><span data-stu-id="6f620-111">Field</span></span>|<span data-ttu-id="6f620-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6f620-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="6f620-113">**EAN-nr.**</span><span class="sxs-lookup"><span data-stu-id="6f620-113">**EAN No.**</span></span>|<span data-ttu-id="6f620-114">Angiv EAN-lokationsnummeret (European Article Numbering) for kunden.</span><span class="sxs-lookup"><span data-stu-id="6f620-114">Enter the European Article Numbering (EAN) location number for the customer.</span></span>|  
    |<span data-ttu-id="6f620-115">**Kontokode**</span><span class="sxs-lookup"><span data-stu-id="6f620-115">**Account Code**</span></span>|<span data-ttu-id="6f620-116">Angiv kontokoden for kunden.</span><span class="sxs-lookup"><span data-stu-id="6f620-116">Enter the account code for the customer.</span></span><br /><br /> <span data-ttu-id="6f620-117">Kunder i den offentlige sektor angiver en kontokode, når de afgiver en bestilling eller rekvisition.</span><span class="sxs-lookup"><span data-stu-id="6f620-117">Customers in the public sector provide an account code when they place an order or requisition.</span></span> <span data-ttu-id="6f620-118">Baseret på værdien i dette felt medtages kontokoden i OIOUBL-dokumenter, du opretter i [!INCLUDE[d365fin](../../includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6f620-118">Based on the value of this field, the account code is included in the OIOUBL documents that you create in [!INCLUDE[d365fin](../../includes/d365fin_md.md)].</span></span> <span data-ttu-id="6f620-119">Ifølge **Lov om Offentlige Betalinger** og relaterede love har kunden ret til at tilbageholde betaling, indtil der modtages en faktura med den relevante kontokode.</span><span class="sxs-lookup"><span data-stu-id="6f620-119">In accordance with **Lov om Offentlige Betalinger** and related statutes, the customer is entitled to withhold payment until they receive an invoice with the relevant account code.</span></span>|  
    |<span data-ttu-id="6f620-120">**OIOUBL-profilkode**</span><span class="sxs-lookup"><span data-stu-id="6f620-120">**OIOUBL Profile Code**</span></span>|<span data-ttu-id="6f620-121">Angiver den profil, som denne kunde kræver for elektroniske dokumenter, hvis den er anderledes end den standardprofil, du har angivet på siden **Salgsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="6f620-121">Specifies the profile that this customer requires for electronic documents if this is different from the default profile that you specified on the **Sales & Receivables Setup** page.</span></span>|  
    |<span data-ttu-id="6f620-122">**OIOUBL-profilkode kræves**</span><span class="sxs-lookup"><span data-stu-id="6f620-122">**OIOUBL Profile Code Required**</span></span>|<span data-ttu-id="6f620-123">Angiver, om debitoren kræver en profilkode til elektroniske bilag.</span><span class="sxs-lookup"><span data-stu-id="6f620-123">Specifies if this customer requires a profile code for electronic documents.</span></span> <span data-ttu-id="6f620-124">**Tip:** Hvis feltet **OIOUBL-profilkode kræves** er markeret, kan du ikke bogføre et salgsdokument for debitoren, medmindre du har angivet en profil.</span><span class="sxs-lookup"><span data-stu-id="6f620-124">**Tip:**  If the **OIOUBL Profile Code Required** field is selected, you cannot post a sales document for this customer unless you have specified a profile.</span></span>|  

 <span data-ttu-id="6f620-125">Disse felter er specifikke for OIOUBL.</span><span class="sxs-lookup"><span data-stu-id="6f620-125">These fields are specific to OIOUBL.</span></span> <span data-ttu-id="6f620-126">De værdier, der bruges i alle OIOUBL-dokumenter, du opretter for denne kunde.</span><span class="sxs-lookup"><span data-stu-id="6f620-126">The values are used in all OIOUBL documents that you create for this customer.</span></span> <span data-ttu-id="6f620-127">Du kan finde flere oplysninger i [Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6f620-127">For more information, see [OIOUBL Electronic Invoicing Overview](oioubl-electronic-invoicing-overview.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="6f620-128">Se også</span><span class="sxs-lookup"><span data-stu-id="6f620-128">See Also</span></span>  
[<span data-ttu-id="6f620-129">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="6f620-129">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  
<span data-ttu-id="6f620-130">[Registrere nye debitorer](../../sales-how-register-new-customers.md) </span><span class="sxs-lookup"><span data-stu-id="6f620-130">[Register New Customers](../../sales-how-register-new-customers.md) </span></span>  
<span data-ttu-id="6f620-131">[Konfigurere OIOUBL](how-to-set-up-oioubl.md) </span><span class="sxs-lookup"><span data-stu-id="6f620-131">[Set Up OIOUBL](how-to-set-up-oioubl.md) </span></span>  
<span data-ttu-id="6f620-132">[Oprette elektroniske dokumenter ved hjælp af OIOUBL](how-to-create-electronic-documents-by-using-oioubl.md) </span><span class="sxs-lookup"><span data-stu-id="6f620-132">[Create Electronic Documents by Using OIOUBL](how-to-create-electronic-documents-by-using-oioubl.md) </span></span>  
[<span data-ttu-id="6f620-133">Oversigt over elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="6f620-133">OIOUBL Electronic Invoicing Overview</span></span>](oioubl-electronic-invoicing-overview.md)  

