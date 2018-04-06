---
title: Synkronisering af kontakter med debitorer og kreditorer | Microsoft Docs
description: "Du kan sammenkæde eller synkronisere kontaktoplysninger for kontakter, der også er debitorer, kreditorer eller bankkonti, så du kun opdaterer oplysninger ét sted."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2b85c52378a351dbc1a0809ec540b1f53c8074ef
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="2dc2e-103">Synkronisering af kontakter med debitorer, kreditorer og bankkonti</span><span class="sxs-lookup"><span data-stu-id="2dc2e-103">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="2dc2e-104">Hvis nogle af dine kontakter også er debitorer, kreditorer eller bankkonti, kan du synkronisere kontaktoplysningerne med den relaterede debitor, kreditor eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-104">If some of your contacts are also customers, vendors, or bank accounts, you can synchronize the contact information with the related customer, vendor, or bank account.</span></span> <span data-ttu-id="2dc2e-105">Synkroniseringen gør oplysninger, der er fælles for kontakter og debitorer, kreditorer eller bankkonti, ens.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-105">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>  

<span data-ttu-id="2dc2e-106">Du skal angive en forretningsrelationskode for debitorer, kreditorer eller bankkonti i vinduet **Marketingopsætning**, før du kan synkronisere kontakter med disse.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-106">Before you can synchronize your contacts with customers, vendors, or bank accounts, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="2dc2e-107">Du kan finde flere oplysninger under [Konfigurere Relationsstyring](marketing-setup-marketing.md).</span><span class="sxs-lookup"><span data-stu-id="2dc2e-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="2dc2e-108">Forskellige måder at synkronisere kontakter med debitorer, kreditorer og bankkonti</span><span class="sxs-lookup"><span data-stu-id="2dc2e-108">Different Ways to Synchronize Contacts with Customers, Vendors and Bank Accounts</span></span>
<span data-ttu-id="2dc2e-109">Du kan synkronisere kontakter med debitorer, kreditorer eller bankkonti på tre måder:</span><span class="sxs-lookup"><span data-stu-id="2dc2e-109">You can synchronize your contacts with customers, vendors, or bank accounts by three methods:</span></span>

* <span data-ttu-id="2dc2e-110">knytte kontakter sammen med eksisterende debitorer, kreditorer eller bankkonti fra kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-110">Link contacts with existing customers, vendors, or bank accounts from the contact card.</span></span> <span data-ttu-id="2dc2e-111">Du kan finde flere oplysninger under [Knytte kontakter til debitorer, kreditorer og bankkonti](marketing-how-link-contact.md).</span><span class="sxs-lookup"><span data-stu-id="2dc2e-111">For more information, see [Link Contacts With Customers, Vendors, and Bank Accounts](marketing-how-link-contact.md).</span></span>
* <span data-ttu-id="2dc2e-112">Opret debitorer, kreditorer eller bankkonti ud fra kontakten.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-112">Create customers, vendors, or bank accounts from the contact.</span></span> <span data-ttu-id="2dc2e-113">Du kan finde flere oplysninger under [Oprette en debitor, kreditor eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="2dc2e-113">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>
* <span data-ttu-id="2dc2e-114">Oprette kontakter ud fra debitorer, kreditorer eller bankkonti.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-114">Create contacts from customers, vendors or bank accounts.</span></span> <span data-ttu-id="2dc2e-115">Du kan finde flere oplysninger under [Oprette en virksomhedskontakt ud fra en debitor, kreditor eller bankkonto](marketing-how-create-contact-companies.md).</span><span class="sxs-lookup"><span data-stu-id="2dc2e-115">For more information, see [Create a company contact from a customer, vendor, or bank account](marketing-how-create-contact-companies.md).</span></span>

## <a name="consequences-of-synchronization"></a><span data-ttu-id="2dc2e-116">Resultater af synkronisering</span><span class="sxs-lookup"><span data-stu-id="2dc2e-116">Consequences of Synchronization</span></span>
<span data-ttu-id="2dc2e-117">Hvis kontakten synkroniseres med debitoren, kreditoren, bankkontoen:</span><span class="sxs-lookup"><span data-stu-id="2dc2e-117">When the contact is synchronized with the customer, vendor, bank account:</span></span>

* <span data-ttu-id="2dc2e-118">Du behøver kun opdatere oplysninger ét sted.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-118">You only have to update information in one place.</span></span> <span data-ttu-id="2dc2e-119">Ændrer du f.eks. telefonnummeret på kontakten, opdateres telefonnummeret automatisk med samme ændring på debitoren, kreditoren eller bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-119">For example, if you modify the phone number on the contact, the phone number is automatically updated with the same modification on the customer, the vendor, or the bank account.</span></span>
* <span data-ttu-id="2dc2e-120">Hvis du har angivet en nummerserie til kontakter, og du opretter et debitor-, kreditor- eller bankkontokort, oprettes der automatisk et kontaktkort for den pågældende debitor, kreditor eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-120">If you have specified a number series for contacts, when you create a customer card, a vendor card, or a bank account card, a contact card is automatically created for the customer, vendor or bank account.</span></span>
* <span data-ttu-id="2dc2e-121">Du kan oprette salgstilbud og -ordrer og købsrekvisitioner og -ordrer ud fra kontakten.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-121">You can create sales quotes and orders, and purchase quotes and orders from the contact.</span></span>
* <span data-ttu-id="2dc2e-122">Du kan automatisk få registreret dine interaktioner, når du udfører handlinger, f.eks. udskriver ordrer, rammeordrer, opretter serviceordrer, sender mails osv.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-122">You can have your interactions recorded when you perform actions such as printing orders, blanket orders, creating sales service orders, sending e-mails, and so on.</span></span>
* <span data-ttu-id="2dc2e-123">Hvis du sletter en kontakt, som er knyttet sammen med en debitor, kreditor eller bankkonto, er det kun kontakten, som bliver slettet.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-123">If you delete a contact linked to a customer, vendor or bank account, only the contact is removed.</span></span> <span data-ttu-id="2dc2e-124">Debitor, kreditor eller bankkonto slettes ikke.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-124">The customer, vendor, or bank account remains.</span></span>
* <span data-ttu-id="2dc2e-125">Hvis du sletter en debitor, kreditor eller bankkonto, som er knyttet til en kontakt, forbliver kontakten.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-125">If you delete a customer, vendor, bank account linked to a contact, the contact remains.</span></span>

> [!NOTE]  
>   <span data-ttu-id="2dc2e-126">Visse detaljer, som fakturerings og bogføringsoplysninger, vises ikke på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-126">Some details, such as invoicing and posting details, do not appear on the contact card.</span></span> <span data-ttu-id="2dc2e-127">Derfor kan du tilføje dem manuelt på debitorkortet, kreditorkortet eller bankkontokortet, når du opretter kontakter som debitorer, kreditorer eller bankkonti.</span><span class="sxs-lookup"><span data-stu-id="2dc2e-127">Therefore, you may want to add them manually on the customer card, vendor card, or bank account card when you create contacts as customers, vendors or bank accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="2dc2e-128">Se også</span><span class="sxs-lookup"><span data-stu-id="2dc2e-128">See Also</span></span>
[<span data-ttu-id="2dc2e-129">Administrere kontakter</span><span class="sxs-lookup"><span data-stu-id="2dc2e-129">Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="2dc2e-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2dc2e-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

