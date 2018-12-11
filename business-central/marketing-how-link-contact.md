---
title: Tilknytning af kontakter til debitorer og kreditorer | Microsoft Docs
description: "Beskriver, hvordan du sammenkæder en kontakt med en debitor, kreditor eller bankkonto fra samme virksomhed, så du kan synkronisere fælles data."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: ae6b02e7ce73d4a13cdc7dd42858ac791d4bf1c2
ms.contentlocale: da-dk
ms.lasthandoff: 12/11/2018

---
# <a name="link-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="29cac-103">Sammenkæde kontakter med debitorer, kreditorer og bankkonti</span><span class="sxs-lookup"><span data-stu-id="29cac-103">Link Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="29cac-104">Hvis du har en kontakt og enten en debitor, kreditor eller bankkonto til samme virksomhed, kan du knytte de to poster til hinanden.</span><span class="sxs-lookup"><span data-stu-id="29cac-104">If you have contact and either a customer, vendor, or bank account for the same company, you can link the two entities.</span></span> <span data-ttu-id="29cac-105">Når du knytter de to poster til hinanden, kan du synkronisere data, som er fælles, så det er de samme i begge steder.</span><span class="sxs-lookup"><span data-stu-id="29cac-105">Linking the two entities enables you to synchronize data that is common so that it is the same in both places.</span></span>

## <a name="link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a><span data-ttu-id="29cac-106">Knytte en kontakt til en eksisterende debitor, kreditor eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="29cac-106">Link a Contact to an Existing Customer, Vendor, or Bank Account</span></span>
1. <span data-ttu-id="29cac-107">Åbn den kontakt, du vil tilknytte.</span><span class="sxs-lookup"><span data-stu-id="29cac-107">Open the contact that you want to link.</span></span>
2. <span data-ttu-id="29cac-108">Vælg handlingen **Opret kæde til eksist.**, og vælg derefter **Debitor**, **Kreditor** eller **Bank**.</span><span class="sxs-lookup"><span data-stu-id="29cac-108">Choose the **Link with existing** action, and then choose **Customer**, **Vendor**, or **Bank**.</span></span>
3. <span data-ttu-id="29cac-109">Vælg den debitor, kreditor eller bankkonto, der skal oprettes en tilknytning til.</span><span class="sxs-lookup"><span data-stu-id="29cac-109">Select the customer, vendor, or bank account to link to.</span></span>

   <span data-ttu-id="29cac-110">I **Aktuelle overord. felter** kan du angive, hvilke felter der skal have prioritet i tilfælde af uoverensstemmende oplysninger i felter, som er fælles for kontakten og debitoren, kreditoren eller kontoen.</span><span class="sxs-lookup"><span data-stu-id="29cac-110">In the **Current Master Fields**, you specify which fields should prioritize in case of conflicting information in fields common to the contact and customer, vendor, or account.</span></span> <span data-ttu-id="29cac-111">Hvis sælgerkoden f.eks. ikke er ens for kontakten og debitoren, kan du ved at markere **Kontakt** bestemme, at det er oplysningerne for kontakten, som skal bruges.</span><span class="sxs-lookup"><span data-stu-id="29cac-111">For example, if the salesperson code is different in the contact than the customer, you can decide, by selecting **Contact**, to use the information in the contact.</span></span>

## <a name="see-also"></a><span data-ttu-id="29cac-112">Se også</span><span class="sxs-lookup"><span data-stu-id="29cac-112">See Also</span></span>
[<span data-ttu-id="29cac-113">Synkronisering af kontakter med debitorer, kreditorer og bankkonti</span><span class="sxs-lookup"><span data-stu-id="29cac-113">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="29cac-114">Oprette og administrere kontakter</span><span class="sxs-lookup"><span data-stu-id="29cac-114">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="29cac-115">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="29cac-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

