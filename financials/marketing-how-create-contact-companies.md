---
title: Oprette kontaktvirksomheder | Microsoft Docs
description: Beskriver, hvordan du kan oprette en kontaktperson for hver ny virksomhed eller potentielle virksomhed, du arbejder sammen med eller har en relation til.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6a1141c352dd93657d32bb83067ce32077901a47
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-contact-companies"></a><span data-ttu-id="54796-103">Fremgangsmåde: Oprette kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="54796-103">How to: Create Contact Companies</span></span>
<span data-ttu-id="54796-104">Du kan oprette en kontakt for hver ny virksomhed, du er i interaktion med, f.eks. kunde, leverandør, kundeemne, bank, advokatfirma eller konsulentfirma.</span><span class="sxs-lookup"><span data-stu-id="54796-104">You can create a contact for each new company you interact with, for example, a customer, vendor, prospective customer, bank, law firm, consultant, and so on.</span></span>

<span data-ttu-id="54796-105">Du kan oprette en kontakt på to måder: forfra eller fra en eksisterende debitor, kreditor eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="54796-105">There are two ways to create a contact: from scratch or from an existing customer, vendor, or bank account.</span></span>

<span data-ttu-id="54796-106">Kontroller eventuelt indstillingerne i vinduet **Marketingopsætning**, før du opretter en kontakt.</span><span class="sxs-lookup"><span data-stu-id="54796-106">Before creating a contact, you may want to check the settings in the **Marketing Setup** window.</span></span> <span data-ttu-id="54796-107">Du kan finde flere oplysninger under [Konfigurere Relationsstyring](marketing-setup-marketing.md).</span><span class="sxs-lookup"><span data-stu-id="54796-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="create-a-company-contact-from-scratch"></a><span data-ttu-id="54796-108">Oprette en virksomhedskontakt fra bunden</span><span class="sxs-lookup"><span data-stu-id="54796-108">Create a company contact from scratch</span></span>
1. <span data-ttu-id="54796-109">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontakter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="54796-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="54796-110">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="54796-110">Choose the **New** action.</span></span>
3. <span data-ttu-id="54796-111">I feltet **Nummer** skal du skrive et nummer på kontakten.</span><span class="sxs-lookup"><span data-stu-id="54796-111">In the **No. field**, enter a number for the contact.</span></span>

    <span data-ttu-id="54796-112">Hvis du har defineret en nummerserie for kontakter i vinduet **Marketingopsætning**, kan du i stedet trykke på Enter og vælge det næste tilgængelige nummer.</span><span class="sxs-lookup"><span data-stu-id="54796-112">Alternatively, if you have set up a number series for contacts in the **Marketing Setup** window, you can press the Enter key to select the next available contact number.</span></span>  
4. <span data-ttu-id="54796-113">Indstil **Type** til **Virksomhed**.</span><span class="sxs-lookup"><span data-stu-id="54796-113">Set **Type** to **Company**.</span></span>
5. <span data-ttu-id="54796-114">Udfyld de øvrige felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="54796-114">Fill in the other fields as required.</span></span>

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a><span data-ttu-id="54796-115">Sådan oprettes en virksomhedskontakt fra en debitor, kreditor eller bankkonto</span><span class="sxs-lookup"><span data-stu-id="54796-115">To create a company contact from a customer, vendor, or bank account</span></span>
<span data-ttu-id="54796-116">Hvis du allerede har defineret en række debitorer, kreditorer eller bankkonti, kan du oprette kontakter på grundlag af de eksisterende kreditordata.</span><span class="sxs-lookup"><span data-stu-id="54796-116">If you have already set up a number of customers, vendors, and bank accounts, you can create contacts on the basis of the existing data.</span></span> <span data-ttu-id="54796-117">Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne med oplysningerne om debitor, kreditor eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="54796-117">When you create a contact this way, the contact information is synchronized with the customer, vendor, or bank account information.</span></span>

> [!NOTE]  
>   <span data-ttu-id="54796-118">Før du kan oprette kontaktvirksomheder på denne måde, skal du angive en forretningsrelationskode for debitorer, kreditorer og bankkonti i vinduet **Marketingopsætning**.</span><span class="sxs-lookup"><span data-stu-id="54796-118">Before you can create contact companies this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="54796-119">Hvis du vil oprette kontakter fra en bankkonto, skal du også angive nummerserier for bankkonti i vinduet **Regnskabsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="54796-119">If you will be creating contacts from a bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

1. <span data-ttu-id="54796-120">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv et af følgende, afhængigt af hvorfra du vil oprette kontakter, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="54796-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter one of the following, depending on from where you want to create contacts, and then choose the related link.</span></span>
   * <span data-ttu-id="54796-121">**Opret kontakter fra debitorer**</span><span class="sxs-lookup"><span data-stu-id="54796-121">**Create Contacts from Customers**</span></span>
   * <span data-ttu-id="54796-122">**Oprette kontakter fra kreditorer**</span><span class="sxs-lookup"><span data-stu-id="54796-122">**Create Contacts from Vendors**</span></span>
   * <span data-ttu-id="54796-123">**Oprette kontakter fra bankkonti**</span><span class="sxs-lookup"><span data-stu-id="54796-123">**Create Contacts from Bank Accounts**</span></span>
2. <span data-ttu-id="54796-124">I det kørselsvindue, der åbnes, skal du angive filtre i sektionen **Debitor**, **Kreditor** eller **Bankkonto**, hvis du vil oprette kontakter ud fra bestemte debitorer, kreditorer eller bankkonti.</span><span class="sxs-lookup"><span data-stu-id="54796-124">In the batch job window that opens, in the **Customer**, **Vendor**, or **Bank Account** section, set filters if you want to create contacts from specific customers, vendors, or bank accounts.</span></span>
3. <span data-ttu-id="54796-125">Vælg **OK** for at begynde at oprette kontakter.</span><span class="sxs-lookup"><span data-stu-id="54796-125">Choose the **OK** button to start creating contacts.</span></span>

    <span data-ttu-id="54796-126">De næste numre i nummerserien er tildelt de nye kontakter.</span><span class="sxs-lookup"><span data-stu-id="54796-126">The next contact numbers in the number series are assigned to the new contacts.</span></span> <span data-ttu-id="54796-127">Den forretningsrelation for kreditorer, som er angivet i vinduet **Marketingopsætning**, tildeles til de nyoprettede kontakter.</span><span class="sxs-lookup"><span data-stu-id="54796-127">The business relation for vendors that is specified in the **Marketing Setup** window is assigned to the newly created contacts.</span></span>

> [!TIP]  
>   <span data-ttu-id="54796-128">Du kan også oprette en debitor, kreditor eller bankkonto fra en kontakt.</span><span class="sxs-lookup"><span data-stu-id="54796-128">You can also create a customer, vendor, or bank account from a contact.</span></span> <span data-ttu-id="54796-129">Du kan finde flere oplysninger under [Oprette en debitor, kreditor eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="54796-129">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="54796-130">Se også</span><span class="sxs-lookup"><span data-stu-id="54796-130">See Also</span></span>
[<span data-ttu-id="54796-131">Synkronisering af kontakter med debitorer, kreditorer og bankkonti</span><span class="sxs-lookup"><span data-stu-id="54796-131">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="54796-132">Tildele forretningsrelationer til en kontakt</span><span class="sxs-lookup"><span data-stu-id="54796-132">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="54796-133">Tildele brancher til en kontakt</span><span class="sxs-lookup"><span data-stu-id="54796-133">Assign Industry Groups to a Contact</span></span>](marketing-industry-groups.md#AssignIndustryGroupContact)  
[<span data-ttu-id="54796-134">Tildele mailgrupper til en kontakt</span><span class="sxs-lookup"><span data-stu-id="54796-134">Assign Mailing Groups to a Contact</span></span>](marketing-mailing-groups.md#AssignMailGroupContact)  
[<span data-ttu-id="54796-135">Fremgangsmåde: Oprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="54796-135">How to: Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="54796-136">Arbejde med Financials</span><span class="sxs-lookup"><span data-stu-id="54796-136">Working with Financials</span></span>](ui-work-product.md)

