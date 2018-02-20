---
title: "Sådan oprettes servicetilbud | Microsoft Docs"
description: "Du kan bruge vinduet **Servicetilbud** til at oprette dokumenter, hvor du indtaster oplysninger om en serviceydelse, f.eks. reparation og vedligeholdelse, for serviceartikler efter kundeforespørgsel. Du kan bruge et servicetilbud som foreløbig kladde til en serviceordre og derefter konvertere tilbuddet til en serviceordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9d4f8d21d0c79adbac238b2d26accc4c08656c77
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="create-service-quotes"></a><span data-ttu-id="6b3fa-104">Oprette servicetilbud</span><span class="sxs-lookup"><span data-stu-id="6b3fa-104">Create Service Quotes</span></span>
<span data-ttu-id="6b3fa-105">Du kan betragte servicetilbud som grundlaget for serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="6b3fa-106">De er faktisk næsten identiske.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-106">In fact, they are almost identical.</span></span> <span data-ttu-id="6b3fa-107">Begge indeholder oplysninger, f.eks. hvem debitoren er, ordretypen, den vare, der har behov for service, fakturerings- og leveringsoplysninger og oplysninger om det aktuelle servicearbejde.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="6b3fa-108">Du kan bruge et servicetilbud som foreløbig kladde til en serviceordre og derefter konvertere tilbuddet til en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="6b3fa-109">Sådan oprettes servicetilbud</span><span class="sxs-lookup"><span data-stu-id="6b3fa-109">To create a service quote</span></span>  
1. <span data-ttu-id="6b3fa-110">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Servicetilbud**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6b3fa-111">Opret et nyt servicetilbud.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="6b3fa-112">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="6b3fa-112">In the **No.**</span></span> <span data-ttu-id="6b3fa-113">skal du indtaste et nummer på servicetilbuddet.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="6b3fa-114">Hvis du har defineret en nummerserie for servicetilbud i vinduet **Serviceopsætning**, kan du trykke på Enter for at vælge det næste tilgængelige servicetilbudsnummer.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-114">Alternatively, if you have set up a number series for service quotes in the **Service Mgt. Setup** window, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="6b3fa-115">I feltet **Debitornr.**</span><span class="sxs-lookup"><span data-stu-id="6b3fa-115">In the **Customer No.**</span></span>  <span data-ttu-id="6b3fa-116">skal du markere den relevante debitor på listen.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="6b3fa-117">De debitorrelevante felter udfyldes automatisk med oplysninger fra **debitorkortet**.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="6b3fa-118">Hvis der ikke findes et **debitorkort** for debitoren, og du har oprettet en debitorskabelon, kan du oprette debitoren fra servicetilbuddet.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="6b3fa-119">Udfyld de relevante felter, og vælg derefter handlingen **Opret debitor**.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="6b3fa-120">Afhængig af indstillingerne i oversigtspanelet **Obligatoriske felter** i vinduet **Serviceopsætning** kan det være nødvendigt at udfylde feltet **Serviceordretype** og feltet **Sælgerkode**.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-120">Depending on the settings on the **Mandatory Fields** FastTab in the **Service Mgt. Setup** window, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="6b3fa-121">Udfyld serviceartikellinjerne.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="6b3fa-122">Registrer de anslåede kostpriser på servicelinjerne.</span><span class="sxs-lookup"><span data-stu-id="6b3fa-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6b3fa-123">Se også</span><span class="sxs-lookup"><span data-stu-id="6b3fa-123">See Also</span></span>  
[<span data-ttu-id="6b3fa-124">Oprette serviceordrer</span><span class="sxs-lookup"><span data-stu-id="6b3fa-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="6b3fa-125">Arbejde med serviceopgaver</span><span class="sxs-lookup"><span data-stu-id="6b3fa-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 
