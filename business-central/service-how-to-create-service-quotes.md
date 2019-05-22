---
title: Sådan oprettes servicetilbud | Microsoft Docs
description: Du kan bruge siden **Servicetilbud** til at oprette dokumenter, hvor du indtaster oplysninger om en serviceydelse, f.eks. reparation og vedligeholdelse, for serviceartikler efter kundeforespørgsel. Du kan bruge et servicetilbud som foreløbig kladde til en serviceordre og derefter konvertere tilbuddet til en serviceordre.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 44ffab92930237c5496860771f41b4951b15b0ff
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250660"
---
# <a name="create-service-quotes"></a><span data-ttu-id="58543-104">Oprette servicetilbud</span><span class="sxs-lookup"><span data-stu-id="58543-104">Create Service Quotes</span></span>
<span data-ttu-id="58543-105">Du kan betragte servicetilbud som grundlaget for serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="58543-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="58543-106">De er faktisk næsten identiske.</span><span class="sxs-lookup"><span data-stu-id="58543-106">In fact, they are almost identical.</span></span> <span data-ttu-id="58543-107">Begge indeholder oplysninger, f.eks. hvem debitoren er, ordretypen, den vare, der har behov for service, fakturerings- og leveringsoplysninger og oplysninger om det aktuelle servicearbejde.</span><span class="sxs-lookup"><span data-stu-id="58543-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="58543-108">Du kan bruge et servicetilbud som foreløbig kladde til en serviceordre og derefter konvertere tilbuddet til en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="58543-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="58543-109">Sådan oprettes servicetilbud</span><span class="sxs-lookup"><span data-stu-id="58543-109">To create a service quote</span></span>  
1. <span data-ttu-id="58543-110">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicetilbud**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="58543-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="58543-111">Opret et nyt servicetilbud.</span><span class="sxs-lookup"><span data-stu-id="58543-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="58543-112">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="58543-112">In the **No.**</span></span> <span data-ttu-id="58543-113">skal du indtaste et nummer på servicetilbuddet.</span><span class="sxs-lookup"><span data-stu-id="58543-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="58543-114">Hvis du har defineret en nummerserie for servicetilbud på siden **Serviceopsætning**, kan du trykke på Enter for at vælge det næste tilgængelige servicetilbudsnummer.</span><span class="sxs-lookup"><span data-stu-id="58543-114">Alternatively, if you have set up a number series for service quotes on the **Service Mgt. Setup** page, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="58543-115">I feltet **Debitornr.**</span><span class="sxs-lookup"><span data-stu-id="58543-115">In the **Customer No.**</span></span>  <span data-ttu-id="58543-116">skal du markere den relevante debitor på listen.</span><span class="sxs-lookup"><span data-stu-id="58543-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="58543-117">De debitorrelevante felter udfyldes automatisk med oplysninger fra **debitorkortet**.</span><span class="sxs-lookup"><span data-stu-id="58543-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="58543-118">Hvis der ikke findes et **debitorkort** for debitoren, og du har oprettet en debitorskabelon, kan du oprette debitoren fra servicetilbuddet.</span><span class="sxs-lookup"><span data-stu-id="58543-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="58543-119">Udfyld de relevante felter, og vælg derefter handlingen **Opret debitor**.</span><span class="sxs-lookup"><span data-stu-id="58543-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="58543-120">Afhængig af indstillingerne i oversigtspanelet **Obligatoriske felter** på siden **Serviceopsætning** kan det være nødvendigt at udfylde feltet **Serviceordretype** og feltet **Sælgerkode**.</span><span class="sxs-lookup"><span data-stu-id="58543-120">Depending on the settings on the **Mandatory Fields** FastTab on the **Service Mgt. Setup** page, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="58543-121">Udfyld serviceartikellinjerne.</span><span class="sxs-lookup"><span data-stu-id="58543-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="58543-122">Registrer de anslåede kostpriser på servicelinjerne.</span><span class="sxs-lookup"><span data-stu-id="58543-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58543-123">Se også</span><span class="sxs-lookup"><span data-stu-id="58543-123">See Also</span></span>  
[<span data-ttu-id="58543-124">Oprette serviceordrer</span><span class="sxs-lookup"><span data-stu-id="58543-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="58543-125">Arbejde med serviceopgaver</span><span class="sxs-lookup"><span data-stu-id="58543-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 