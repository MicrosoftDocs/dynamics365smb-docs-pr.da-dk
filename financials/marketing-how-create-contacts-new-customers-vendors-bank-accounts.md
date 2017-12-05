---
title: Oprette en debitor eller kreditor fra en kontakt | Microsoft Docs
description: Du kan registrere en eksisterende kontakt som debitor, kreditor eller bankkonto med eksisterende data og angive en forretningsrelation.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 289213b9c44b07387fd0dcf315b9d08750bdd9f7
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-a-customer-vendor-or-bank-account-from-a-contact"></a><span data-ttu-id="ff0cf-103">Fremgangsmåde: Oprette en debitor, kreditor eller bankkonto fra en kontakt</span><span class="sxs-lookup"><span data-stu-id="ff0cf-103">How to: Create a Customer, Vendor, or Bank Account From a Contact</span></span>
<span data-ttu-id="ff0cf-104">Du har mulighed for at registrere eksisterende kontakter som debitorer, kreditorer eller bankkonti.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-104">You may want to record some of your existing contacts as customers, vendors, or bank accounts.</span></span> <span data-ttu-id="ff0cf-105">Når du opretter en debitor, kreditor eller bankkonto fra en kontakt, kan bruge du eksisterende data.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-105">Creating a customer, vendor, or bank account from a contact enables you use existing data.</span></span> <span data-ttu-id="ff0cf-106">Når du opretter en debitor, kreditor eller bankkonto på denne måde, synkroniseres den med kontakten.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-106">When you create a customer, vendor, or bank account this way, it is synchronized with the contact.</span></span> <span data-ttu-id="ff0cf-107">Synkroniseringen gør oplysninger, der er fælles for kontakter og debitorer, kreditorer eller bankkonti, ens.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-107">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>

<span data-ttu-id="ff0cf-108">Før du kan registrere kontakter på denne måde, skal du angive en forretningsrelationskode for debitorer, kreditorer og bankkonti i vinduet **Marketingopsætning**.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-108">Before you can record contacts this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="ff0cf-109">Hvis du vil registrere kontakter som bankkonti, skal du også angive nummerserier for bankkonti i vinduet **Regnskabsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-109">If you will be recording contacts as bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a><span data-ttu-id="ff0cf-110">Sådan oprettes en kontakt som debitor, kreditor eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-110">To create a contact as a customer, vendor, or bank account</span></span>
1. <span data-ttu-id="ff0cf-111">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontakter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ff0cf-112">Marker den kontakt, du vil oprette som debitor, kreditor eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-112">Select the contact you want to create as a customer, vendor, or bank account.</span></span>
3. <span data-ttu-id="ff0cf-113">Vælg handlingen **Opret som**, og vælg derefter enten **Debitor**, **Kreditor** eller **Bank**.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-113">Choose the **Create As** action, and then choose either **Customer**, **Vendor**, or **Bank**.</span></span>
4. <span data-ttu-id="ff0cf-114">Bekræft den efterfølgende meddelelse.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-114">Confirm the subsequent message.</span></span>

<span data-ttu-id="ff0cf-115">Kontaktoplysningerne overføres fra kortet **Kontakt** til kortet **Bankkonto**, kortet **Debitor** eller kortet **Kreditor**.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-115">The contact information is transferred from the **Contact** card to the **Bank Account** card, the **Customer** card, or the **Vendor** card.</span></span> <span data-ttu-id="ff0cf-116">Du kan tilføje specifikke oplysninger til hvert kort, f.eks. fakturering og betalingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="ff0cf-116">You may want to add specific information to each of the cards, such as invoicing and payment details.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff0cf-117">Se også</span><span class="sxs-lookup"><span data-stu-id="ff0cf-117">See Also</span></span>
[<span data-ttu-id="ff0cf-118">Fremgangsmåde: Oprette kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="ff0cf-118">How to: Create Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="ff0cf-119">Fremgangsmåde: Oprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="ff0cf-119">How to: Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="ff0cf-120">Opsætning af Relationsstyring</span><span class="sxs-lookup"><span data-stu-id="ff0cf-120">Setting Up Relationship Management</span></span>](marketing-setup-marketing.md)  
[<span data-ttu-id="ff0cf-121">Synkronisering af kontakter med debitorer, kreditorer og bankkonti</span><span class="sxs-lookup"><span data-stu-id="ff0cf-121">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="ff0cf-122">Fremgangsmåde: Knytte kontakter til debitorer, kreditorer og bankkonti</span><span class="sxs-lookup"><span data-stu-id="ff0cf-122">How to: Link Contacts to Existing Customers, Vendors, or Bank Accounts</span></span>](marketing-how-link-contact.md)  
[<span data-ttu-id="ff0cf-123">Tildele forretningsrelationer til en kontakt</span><span class="sxs-lookup"><span data-stu-id="ff0cf-123">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="ff0cf-124">Arbejde med Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ff0cf-124">Working with Dynamics 365</span></span>](ui-work-product.md)

