---
title: Tilknytning af kontakter til debitorer og kreditorer | Microsoft Docs
description: "Beskriver, hvordan du sammenkæder en kontakt med en debitor, kreditor eller bankkonto fra samme virksomhed, så du kan synkronisere fælles data."
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
ms.openlocfilehash: f5bbadb37a40dbc7b06668d940d2be9569aaa8e8
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-link-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="58db4-103">Fremgangsmåde: Knytte kontakter til debitorer, kreditorer og bankkonti</span><span class="sxs-lookup"><span data-stu-id="58db4-103">How to: Link Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="58db4-104">Hvis du har en kontakt og enten en debitor, kreditor eller bankkonto til samme virksomhed, kan du knytte de to poster til hinanden.</span><span class="sxs-lookup"><span data-stu-id="58db4-104">If you have contact and either a customer, vendor, or bank account for the same company, you can link the two entities.</span></span> <span data-ttu-id="58db4-105">Når du knytter de to poster til hinanden, kan du synkronisere data, som er fælles, så det er de samme i begge steder.</span><span class="sxs-lookup"><span data-stu-id="58db4-105">Linking the two entities enables you to synchronize data that is common so that it is the same in both places.</span></span>

## <a name="link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a><span data-ttu-id="58db4-106">Knytte en kontakt til en eksisterende debitor, kreditor eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="58db4-106">Link a Contact to an Existing Customer, Vendor, or Bank Account</span></span>
1. <span data-ttu-id="58db4-107">Åbn den kontakt, du vil tilknytte.</span><span class="sxs-lookup"><span data-stu-id="58db4-107">Open the contact that you want to link.</span></span>
2. <span data-ttu-id="58db4-108">Vælg handlingen **Opret kæde til eksist.**, og vælg derefter **Debitor**, **Kreditor** eller **Bank**.</span><span class="sxs-lookup"><span data-stu-id="58db4-108">Choose the **Link with existing** action, and then choose **Customer**, **Vendor**, or **Bank**.</span></span>
3. <span data-ttu-id="58db4-109">Vælg den debitor, kreditor eller bankkonto, der skal oprettes en tilknytning til.</span><span class="sxs-lookup"><span data-stu-id="58db4-109">Select the customer, vendor, or bank account to link to.</span></span>

   <span data-ttu-id="58db4-110">I **Aktuelle overord. felter** kan du angive, hvilke felter der skal have prioritet i tilfælde af uoverensstemmende oplysninger i felter, som er fælles for kontakten og debitoren, kreditoren eller kontoen.</span><span class="sxs-lookup"><span data-stu-id="58db4-110">In the **Current Master Fields**, you specify which fields should prioritize in case of conflicting information in fields common to the contact and customer, vendor, or account.</span></span> <span data-ttu-id="58db4-111">Hvis sælgerkoden f.eks. ikke er ens for kontakten og debitoren, kan du ved at markere **Kontakt** bestemme, at det er oplysningerne for kontakten, som skal bruges.</span><span class="sxs-lookup"><span data-stu-id="58db4-111">For example, if the salesperson code is different in the contact than the customer, you can decide, by selecting **Contact**, to use the information in the contact.</span></span>

## <a name="see-also"></a><span data-ttu-id="58db4-112">Se også</span><span class="sxs-lookup"><span data-stu-id="58db4-112">See Also</span></span>
[<span data-ttu-id="58db4-113">Synkronisering af kontakter med debitorer, kreditorer og bankkonti</span><span class="sxs-lookup"><span data-stu-id="58db4-113">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="58db4-114">Oprette og administrere kontakter</span><span class="sxs-lookup"><span data-stu-id="58db4-114">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="58db4-115">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="58db4-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

