---
title: Sådan konfigureres kunder til OIOUBL | Microsoft Docs
description: Hvis du vil oprette OIOUBL-dokumenter (Offentlig Information Online UBL) for debitorer i den offentlige sektor, skal du tilføje OIOUBL-oplysninger for de relevante debitorer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 348ac1d2b731553edff42624329fb943d44a6f28
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379457"
---
# <a name="set-up-customers-for-oioubl"></a><span data-ttu-id="df00d-103">Konfigurere kunder til OIOUBL</span><span class="sxs-lookup"><span data-stu-id="df00d-103">Set Up Customers for OIOUBL</span></span>
<span data-ttu-id="df00d-104">Hvis du vil oprette OIOUBL-dokumenter (Offentlig Information Online UBL) for debitorer i den offentlige sektor, skal du tilføje OIOUBL-oplysninger for de relevante debitorer.</span><span class="sxs-lookup"><span data-stu-id="df00d-104">To create Offentlig Information Online UBL (OIOUBL) documents for customers in the public sector, you must add OIOUBL information to the relevant customers.</span></span>  

 <span data-ttu-id="df00d-105">I dette emne beskrives kun de felter, der gælder for OIOUBL.</span><span class="sxs-lookup"><span data-stu-id="df00d-105">This topic only describes fields that apply to OIOUBL.</span></span> <span data-ttu-id="df00d-106">Du kan finde flere oplysninger i [Registrere nye debitorer](../../sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="df00d-106">For more information, see [Register New Customers](../../sales-how-register-new-customers.md).</span></span>  

### <a name="to-set-up-customers-for-oioubl"></a><span data-ttu-id="df00d-107">Sådan konfigureres kunder til OIOUBL</span><span class="sxs-lookup"><span data-stu-id="df00d-107">To set up customers for OIOUBL</span></span>  

1.  <span data-ttu-id="df00d-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="df00d-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="df00d-109">Åbn den kunde, du vil konfigurere aktivere til OIOUBL.</span><span class="sxs-lookup"><span data-stu-id="df00d-109">Open the customer that you want to enable for OIOUBL.</span></span>  
3.  <span data-ttu-id="df00d-110">Udfyld felterne i oversigtspanelet **Fakturering** som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="df00d-110">On the **Invoicing** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="df00d-111">Felt</span><span class="sxs-lookup"><span data-stu-id="df00d-111">Field</span></span>|<span data-ttu-id="df00d-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="df00d-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="df00d-113">**GLN**</span><span class="sxs-lookup"><span data-stu-id="df00d-113">**GLN**</span></span>|<span data-ttu-id="df00d-114">Angiv debitorens GLN-lokationsnummer, der entydigt identificerer faktureringsadressen.</span><span class="sxs-lookup"><span data-stu-id="df00d-114">Enter the customer's Global Location Number, which uniquely identifies the billing address.</span></span> <span data-ttu-id="df00d-115">Et GLN har en fast længde på 13 cifre.</span><span class="sxs-lookup"><span data-stu-id="df00d-115">A GLN has a fixed length of 13 digits.</span></span> <span data-ttu-id="df00d-116">Det omfatter et tildelt præfiks for virksomheden, en placeringsreference og et kontrolciffer.</span><span class="sxs-lookup"><span data-stu-id="df00d-116">It includes an assigned company prefix, a location reference, and a check digit.</span></span>|  
    |<span data-ttu-id="df00d-117">**Kontokode**</span><span class="sxs-lookup"><span data-stu-id="df00d-117">**Account Code**</span></span>|<span data-ttu-id="df00d-118">Angiv kontokoden for kunden.</span><span class="sxs-lookup"><span data-stu-id="df00d-118">Enter the account code for the customer.</span></span><br /><br /> <span data-ttu-id="df00d-119">Kunder i den offentlige sektor angiver en kontokode, når de afgiver en bestilling eller rekvisition.</span><span class="sxs-lookup"><span data-stu-id="df00d-119">Customers in the public sector provide an account code when they place an order or requisition.</span></span> <span data-ttu-id="df00d-120">Baseret på værdien i dette felt medtages kontokoden i OIOUBL-dokumenter, du opretter i [!INCLUDE[prod_short](../../includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="df00d-120">Based on the value of this field, the account code is included in the OIOUBL documents that you create in [!INCLUDE[prod_short](../../includes/prod_short.md)].</span></span> <span data-ttu-id="df00d-121">Ifølge **Lov om Offentlige Betalinger** og relaterede love har kunden ret til at tilbageholde betaling, indtil der modtages en faktura med den relevante kontokode.</span><span class="sxs-lookup"><span data-stu-id="df00d-121">In accordance with **Lov om Offentlige Betalinger** and related statutes, the customer is entitled to withhold payment until they receive an invoice with the relevant account code.</span></span>|  
    |<span data-ttu-id="df00d-122">**OIOUBL-profilkode**</span><span class="sxs-lookup"><span data-stu-id="df00d-122">**OIOUBL Profile Code**</span></span>|<span data-ttu-id="df00d-123">Angiver den profil, som denne kunde kræver for elektroniske dokumenter, hvis den er anderledes end den standardprofil, du har angivet på siden **Salgsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="df00d-123">Specifies the profile that this customer requires for electronic documents if this is different from the default profile that you specified on the **Sales & Receivables Setup** page.</span></span>|  
    |<span data-ttu-id="df00d-124">**OIOUBL-profilkode kræves**</span><span class="sxs-lookup"><span data-stu-id="df00d-124">**OIOUBL Profile Code Required**</span></span>|<span data-ttu-id="df00d-125">Angiver, om debitoren kræver en profilkode til elektroniske bilag.</span><span class="sxs-lookup"><span data-stu-id="df00d-125">Specifies if this customer requires a profile code for electronic documents.</span></span> <span data-ttu-id="df00d-126">**Tip:** Hvis feltet **OIOUBL-profilkode kræves** er markeret, kan du ikke bogføre et salgsdokument for debitoren, medmindre du har angivet en profil.</span><span class="sxs-lookup"><span data-stu-id="df00d-126">**Tip:**  If the **OIOUBL Profile Code Required** field is selected, you cannot post a sales document for this customer unless you have specified a profile.</span></span>|  

 <span data-ttu-id="df00d-127">Disse felter er specifikke for OIOUBL.</span><span class="sxs-lookup"><span data-stu-id="df00d-127">These fields are specific to OIOUBL.</span></span> <span data-ttu-id="df00d-128">De værdier, der bruges i alle OIOUBL-dokumenter, du opretter for denne kunde.</span><span class="sxs-lookup"><span data-stu-id="df00d-128">The values are used in all OIOUBL documents that you create for this customer.</span></span> <span data-ttu-id="df00d-129">Du kan finde flere oplysninger i [Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="df00d-129">For more information, see [OIOUBL Electronic Invoicing Overview](oioubl-electronic-invoicing-overview.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="df00d-130">Se også</span><span class="sxs-lookup"><span data-stu-id="df00d-130">See Also</span></span>  
[<span data-ttu-id="df00d-131">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="df00d-131">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  
<span data-ttu-id="df00d-132">[Registrere nye debitorer](../../sales-how-register-new-customers.md) </span><span class="sxs-lookup"><span data-stu-id="df00d-132">[Register New Customers](../../sales-how-register-new-customers.md) </span></span>  
<span data-ttu-id="df00d-133">[Konfigurere OIOUBL](how-to-set-up-oioubl.md) </span><span class="sxs-lookup"><span data-stu-id="df00d-133">[Set Up OIOUBL](how-to-set-up-oioubl.md) </span></span>  
<span data-ttu-id="df00d-134">[Oprette elektroniske dokumenter ved hjælp af OIOUBL](how-to-create-electronic-documents-by-using-oioubl.md) </span><span class="sxs-lookup"><span data-stu-id="df00d-134">[Create Electronic Documents by Using OIOUBL](how-to-create-electronic-documents-by-using-oioubl.md) </span></span>  
[<span data-ttu-id="df00d-135">Oversigt over elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="df00d-135">OIOUBL Electronic Invoicing Overview</span></span>](oioubl-electronic-invoicing-overview.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]