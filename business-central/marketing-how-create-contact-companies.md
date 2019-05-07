---
title: Oprette kontaktvirksomheder | Microsoft Docs
description: Beskriver, hvordan du kan oprette en kontaktperson for hver ny virksomhed eller potentielle virksomhed, du arbejder sammen med eller har en relation til.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 67945b8825ae94ff3a09a4072309c401abb41c6b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "920978"
---
# <a name="create-contacts"></a><span data-ttu-id="aa562-103">Oprette kontakter</span><span class="sxs-lookup"><span data-stu-id="aa562-103">Create Contacts</span></span>
<span data-ttu-id="aa562-104">Du kan oprette en kontakt for hver ny virksomhed, du er i interaktion med, f.eks. kunde, leverandør, kundeemne, bank, advokatfirma eller konsulentfirma.</span><span class="sxs-lookup"><span data-stu-id="aa562-104">You can create a contact for each new company you interact with, for example, a customer, vendor, prospective customer, bank, law firm, consultant, and so on.</span></span>

<span data-ttu-id="aa562-105">Du kan oprette en kontakt på to måder: forfra eller fra en eksisterende debitor, kreditor eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="aa562-105">There are two ways to create a contact: from scratch or from an existing customer, vendor, or bank account.</span></span>

## <a name="create-a-company-contact-from-scratch"></a><span data-ttu-id="aa562-106">Oprette en virksomhedskontakt fra bunden</span><span class="sxs-lookup"><span data-stu-id="aa562-106">Create a company contact from scratch</span></span>
1. <span data-ttu-id="aa562-107">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontakter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="aa562-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="aa562-108">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aa562-108">Choose the **New** action.</span></span>
3. <span data-ttu-id="aa562-109">I feltet **Nummer** skal du skrive et nummer på kontakten.</span><span class="sxs-lookup"><span data-stu-id="aa562-109">In the **No. field**, enter a number for the contact.</span></span>

    <span data-ttu-id="aa562-110">Hvis du har defineret en nummerserie for kontakter på siden **Marketingopsætning**, kan du i stedet trykke på Enter og vælge det næste tilgængelige nummer.</span><span class="sxs-lookup"><span data-stu-id="aa562-110">Alternatively, if you have set up a number series for contacts on the **Marketing Setup** page, you can press the Enter key to select the next available contact number.</span></span>  
4. <span data-ttu-id="aa562-111">Indstil **Type** til **Virksomhed**.</span><span class="sxs-lookup"><span data-stu-id="aa562-111">Set **Type** to **Company**.</span></span>
5. <span data-ttu-id="aa562-112">Udfyld de øvrige felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="aa562-112">Fill in the other fields as required.</span></span>

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a><span data-ttu-id="aa562-113">Sådan oprettes en virksomhedskontakt fra en debitor, kreditor eller bankkonto</span><span class="sxs-lookup"><span data-stu-id="aa562-113">To create a company contact from a customer, vendor, or bank account</span></span>
<span data-ttu-id="aa562-114">Hvis du allerede har defineret en række debitorer, kreditorer eller bankkonti, kan du oprette kontakter på grundlag af de eksisterende kreditordata.</span><span class="sxs-lookup"><span data-stu-id="aa562-114">If you have already set up a number of customers, vendors, and bank accounts, you can create contacts on the basis of the existing data.</span></span> <span data-ttu-id="aa562-115">Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne med oplysningerne om debitor, kreditor eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="aa562-115">When you create a contact this way, the contact information is synchronized with the customer, vendor, or bank account information.</span></span>

> [!NOTE]  
>   <span data-ttu-id="aa562-116">Før du kan oprette kontaktvirksomheder på denne måde, skal du angive en forretningsrelationskode for debitorer, kreditorer og bankkonti på siden **Marketingopsætning**.</span><span class="sxs-lookup"><span data-stu-id="aa562-116">Before you can create contact companies this way, you must specify a business relation code for customers, vendors, and bank accounts on the **Marketing Setup** page.</span></span> <span data-ttu-id="aa562-117">Hvis du vil oprette kontakter fra en bankkonto, skal du også angive nummerserier for bankkonti på siden **Opsætning af Finans**.</span><span class="sxs-lookup"><span data-stu-id="aa562-117">If you will be creating contacts from a bank accounts, you must also specify numbers series for bank accounts on the **General Ledger Setup** page.</span></span>

1. <span data-ttu-id="aa562-118">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv en af følgende, afhængigt af hvor du vil oprette kontakter, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="aa562-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter one of the following, depending on from where you want to create contacts, and then choose the related link.</span></span>
   * <span data-ttu-id="aa562-119">**Opret kontakter fra debitorer**</span><span class="sxs-lookup"><span data-stu-id="aa562-119">**Create Contacts from Customers**</span></span>
   * <span data-ttu-id="aa562-120">**Opret kontakter fra kreditorer**</span><span class="sxs-lookup"><span data-stu-id="aa562-120">**Create Contacts from Vendors**</span></span>
   * <span data-ttu-id="aa562-121">**Opret kontakter fra bankkonti**</span><span class="sxs-lookup"><span data-stu-id="aa562-121">**Create Contacts from Bank Accounts**</span></span>
2. <span data-ttu-id="aa562-122">I den kørselsside, der åbnes, skal du angive filtre i sektionen **Debitor**, **Kreditor** eller **Bankkonto**, hvis du vil oprette kontakter ud fra bestemte debitorer, kreditorer eller bankkonti.</span><span class="sxs-lookup"><span data-stu-id="aa562-122">In the batch job page that opens, in the **Customer**, **Vendor**, or **Bank Account** section, set filters if you want to create contacts from specific customers, vendors, or bank accounts.</span></span>
3. <span data-ttu-id="aa562-123">Vælg **OK** for at begynde at oprette kontakter.</span><span class="sxs-lookup"><span data-stu-id="aa562-123">Choose the **OK** button to start creating contacts.</span></span>

    <span data-ttu-id="aa562-124">De næste numre i nummerserien er tildelt de nye kontakter.</span><span class="sxs-lookup"><span data-stu-id="aa562-124">The next contact numbers in the number series are assigned to the new contacts.</span></span> <span data-ttu-id="aa562-125">Den forretningsrelation for kreditorer, som er angivet på siden **Marketingopsætning**, tildeles til de nyoprettede kontakter.</span><span class="sxs-lookup"><span data-stu-id="aa562-125">The business relation for vendors that is specified on the **Marketing Setup** page is assigned to the newly created contacts.</span></span>

> [!TIP]  
>   <span data-ttu-id="aa562-126">Du kan også oprette en debitor, kreditor eller bankkonto fra en kontakt.</span><span class="sxs-lookup"><span data-stu-id="aa562-126">You can also create a customer, vendor, or bank account from a contact.</span></span> <span data-ttu-id="aa562-127">Du kan finde flere oplysninger under [Oprette en debitor, kreditor eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="aa562-127">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="aa562-128">Se også</span><span class="sxs-lookup"><span data-stu-id="aa562-128">See Also</span></span>
[<span data-ttu-id="aa562-129">Synkronisering af kontakter med debitorer, kreditorer og bankkonti</span><span class="sxs-lookup"><span data-stu-id="aa562-129">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="aa562-130">Tildele forretningsrelationer til en kontakt</span><span class="sxs-lookup"><span data-stu-id="aa562-130">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="aa562-131">Tildele brancher til en kontakt</span><span class="sxs-lookup"><span data-stu-id="aa562-131">Assign Industry Groups to a Contact</span></span>](marketing-industry-groups.md#AssignIndustryGroupContact)  
[<span data-ttu-id="aa562-132">Tildele mailgrupper til en kontakt</span><span class="sxs-lookup"><span data-stu-id="aa562-132">Assign Mailing Groups to a Contact</span></span>](marketing-mailing-groups.md#AssignMailGroupContact)  
[<span data-ttu-id="aa562-133">Oprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="aa562-133">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="aa562-134">Arbejde med Business Central</span><span class="sxs-lookup"><span data-stu-id="aa562-134">Working with Business Central</span></span>](ui-work-product.md)
