---
title: "Sådan blokeres salg til debitor varer fra salg eller køb"
description: "I Business Central kan en vare være markeret som spærret for salg, spærret for køb eller spærret i alle sammenhænge."
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 268d098318b77cb89a369e8edc14729a44bedae6
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="block-customers"></a><span data-ttu-id="54c7c-103">Blokere debitorer</span><span class="sxs-lookup"><span data-stu-id="54c7c-103">Block Customers</span></span>
<span data-ttu-id="54c7c-104">Du kan spærre en debitor, for eksempel på grund af insolvens, så kunden ikke kan føjes til salgsdokumenter, eller ingen transaktioner kan bogføres for debitoren.</span><span class="sxs-lookup"><span data-stu-id="54c7c-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="54c7c-105">Foruden at blokere for en debitor kan du sætte tilgodehavendetransaktioner for kunden på hold i forbindelse med rykkere.</span><span class="sxs-lookup"><span data-stu-id="54c7c-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="54c7c-106">Du kan finde flere oplysninger under [Indhente udestående beløb](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="54c7c-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="54c7c-107">Den følgende tabel beskriver de forskellige blokeringsindstillinger.</span><span class="sxs-lookup"><span data-stu-id="54c7c-107">The following table describes the different blocking options.</span></span>  

|<span data-ttu-id="54c7c-108">Indstilling</span><span class="sxs-lookup"><span data-stu-id="54c7c-108">Option</span></span>|<span data-ttu-id="54c7c-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="54c7c-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="54c7c-110">**Tomt**</span><span class="sxs-lookup"><span data-stu-id="54c7c-110">**Blank**</span></span>|<span data-ttu-id="54c7c-111">Transaktioner er tilladt for kunden.</span><span class="sxs-lookup"><span data-stu-id="54c7c-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="54c7c-112">**Lever**</span><span class="sxs-lookup"><span data-stu-id="54c7c-112">**Ship**</span></span>|<span data-ttu-id="54c7c-113">Der kan ikke oprettes nye ordrer og nye leverancer til kunden.</span><span class="sxs-lookup"><span data-stu-id="54c7c-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="54c7c-114">Eksisterende leverancer, der ikke er faktureret, kan faktureres.</span><span class="sxs-lookup"><span data-stu-id="54c7c-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="54c7c-115">**Faktura**</span><span class="sxs-lookup"><span data-stu-id="54c7c-115">**Invoice**</span></span>|<span data-ttu-id="54c7c-116">Der kan ikke oprettes nye ordrer, nye leverancer og nye fakturaer til kunden.</span><span class="sxs-lookup"><span data-stu-id="54c7c-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="54c7c-117">Eksisterende leverancer, der ikke er faktureret, kan ikke faktureres.</span><span class="sxs-lookup"><span data-stu-id="54c7c-117">Existing shipments not yet invoiced cannot be invoiced.</span></span>|  
|<span data-ttu-id="54c7c-118">**Alle**</span><span class="sxs-lookup"><span data-stu-id="54c7c-118">**All**</span></span>|<span data-ttu-id="54c7c-119">Ingen transaktioner er tilladt for kunden – heller ikke indbetalinger.</span><span class="sxs-lookup"><span data-stu-id="54c7c-119">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="54c7c-120">Sådan blokeres en kunde</span><span class="sxs-lookup"><span data-stu-id="54c7c-120">To block a customer</span></span>  
1. <span data-ttu-id="54c7c-121">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="54c7c-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="54c7c-122">Vælg en kunde, og vælg derefter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="54c7c-122">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="54c7c-123">Udfyld feltet **Spærret** med en af følgende indstillinger, der er beskrevet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="54c7c-123">Fill in the **Blocked** field with one of the options described above.</span></span>

## <a name="see-also"></a><span data-ttu-id="54c7c-124">Se også</span><span class="sxs-lookup"><span data-stu-id="54c7c-124">See Also</span></span>  
[<span data-ttu-id="54c7c-125">Registrere nye debitorer</span><span class="sxs-lookup"><span data-stu-id="54c7c-125">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="54c7c-126">Indhente udestående beløb</span><span class="sxs-lookup"><span data-stu-id="54c7c-126">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="54c7c-127">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="54c7c-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  

