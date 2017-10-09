---
title: "Sådan angives kontantkunder | Microsoft Docs"
description: "Dette emne beskriver trinnene i opsætning af debitor, som betaler kontant."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6826c574bf63de70d76a29b45968c68c0b2e2d1f
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-cash-customers"></a><span data-ttu-id="023ac-103">Sådan angives kontantkunder</span><span class="sxs-lookup"><span data-stu-id="023ac-103">How to: Set Up Cash Customers</span></span>
<span data-ttu-id="023ac-104">Du kan ikke oprette en faktura uden et debitornummer.</span><span class="sxs-lookup"><span data-stu-id="023ac-104">You cannot create an invoice without a customer number.</span></span> <span data-ttu-id="023ac-105">Det gælder også, hvis du sælger kontant og ikke har noget at registrere i en kundekonto.</span><span class="sxs-lookup"><span data-stu-id="023ac-105">This is true, even if you make a cash sale and do not have anything to record in a customer account.</span></span>  

## <a name="to-set-up-a-cash-customer"></a><span data-ttu-id="023ac-106">Definere en kontantkunde</span><span class="sxs-lookup"><span data-stu-id="023ac-106">To set up a cash customer</span></span>  
1.  <span data-ttu-id="023ac-107">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitor**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="023ac-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="023ac-108">Opret et nyt **Debitor**kort.</span><span class="sxs-lookup"><span data-stu-id="023ac-108">Create a new **Customer** card.</span></span> <span data-ttu-id="023ac-109">Du kan finde flere oplysninger i [Fremgangsmåde: Registrere nye debitorer](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="023ac-109">For more information, see [How to: Register New Customers](sales-how-register-new-customers.md).</span></span>
3.  <span data-ttu-id="023ac-110">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="023ac-110">In the **No.**</span></span> <span data-ttu-id="023ac-111">skal du f.eks. angive **Kontant**.</span><span class="sxs-lookup"><span data-stu-id="023ac-111">field, enter **Cash**, for example.</span></span>  
4.  <span data-ttu-id="023ac-112">Angiv f.eks. **Kontantsalg** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="023ac-112">In the **Name** field, enter **Cash Sale**, for example.</span></span>  
5.  <span data-ttu-id="023ac-113">I oversigtspanelet **Fakturering** skal du udfylde felterne **Debitorbogføringsgruppe** og feltet **Virksomhedsbogføringsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="023ac-113">On the **Invoicing** FastTab, fill in the **Customer Posting Group** and the **Gen. Bus. Posting Group** fields.</span></span>  

 <span data-ttu-id="023ac-114">Du har nu angivet en debitor, der indeholder tilstrækkelige oplysninger til fakturering.</span><span class="sxs-lookup"><span data-stu-id="023ac-114">Now you have set up a customer that contains sufficient information for invoicing.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="023ac-115">Du kan vælge en bogføringsgruppe, der også anvendes til indenlandsk kreditsalg.</span><span class="sxs-lookup"><span data-stu-id="023ac-115">You may have chosen a posting group that is also used for domestic credit sales.</span></span> <span data-ttu-id="023ac-116">Hvis du vil have separate salgstal for kontantsalg, f.eks. på en særlig salgskonto, kan du angive en ekstra bogføringsgruppe til dette formål.</span><span class="sxs-lookup"><span data-stu-id="023ac-116">If you want to maintain separate data on cash sales, for example, with a special sales or receivables account, you can set up an extra posting group for this purpose.</span></span>  
>   
>  <span data-ttu-id="023ac-117">Du skal angive et nummer til salgskonto for bogføringsgruppen, også selvom saldoen altid vil være 0, når du har bogført en faktura.</span><span class="sxs-lookup"><span data-stu-id="023ac-117">You must enter a number for a receivables account for the posting group, even though the balance in this account will always be 0 after you post an invoice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="023ac-118">Se også</span><span class="sxs-lookup"><span data-stu-id="023ac-118">See Also</span></span>
[<span data-ttu-id="023ac-119">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="023ac-119">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="023ac-120">[Fremgangsmåde: Registrere nye debitorer](sales-how-register-new-customers.md)  </span><span class="sxs-lookup"><span data-stu-id="023ac-120">[How to: Register New Customers](sales-how-register-new-customers.md)  </span></span>  
[<span data-ttu-id="023ac-121">Finans</span><span class="sxs-lookup"><span data-stu-id="023ac-121">Finance</span></span>](finance.md)  


