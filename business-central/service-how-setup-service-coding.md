---
title: Definere koder for standardservices | Microsoft Docs
description: "Få at vide, hvordan du definerer koder for serviceaktiviteter, du udfører ofte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f73f5b9d74e7b6a75be6320697aa1a4ad84fb4a1
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---

# <a name="set-up-standard-service-codes"></a><span data-ttu-id="65544-103">Konfigurere standardservicekoder</span><span class="sxs-lookup"><span data-stu-id="65544-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="65544-104">Når der foretages standardservice, skal der ofte oprettes servicedokumenter, der bruger servicelinjer, der indeholder ensartede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="65544-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="65544-105">For at gøre det nemmere at oprette disse linjer kan du oprette standardservicekoder, der har et foruddefineret sæt af servicelinjer.</span><span class="sxs-lookup"><span data-stu-id="65544-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="65544-106">Når du vælger koden i et servicedokument, indsættes linjerne automatisk.</span><span class="sxs-lookup"><span data-stu-id="65544-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="65544-107">Du kan oprette et hvilket som helst antal standardservicekoder, og hver kode kan have et ubegrænset antal servicelinjer af forskellige typer, herunder vare, ressource, pris eller tekst, tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="65544-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="65544-108">Du opretter servicelinjer for hver standardservicekode på kortet **Standardservicekode**.</span><span class="sxs-lookup"><span data-stu-id="65544-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="65544-109">Derefter tildeler du standardservicekoder til serviceartikelgrupper i vinduet **Koder til standardserv.varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="65544-109">You then assign standard service codes to service item groups in the **Standard Serv. Item Gr. Codes** window.</span></span> <span data-ttu-id="65544-110">Senere, når du opretter et servicedokument, du kan bruge handlingen **Hent standardservicekoder** til at tilføje servicelinjer.</span><span class="sxs-lookup"><span data-stu-id="65544-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="65544-111">Du kan bruge den samme fremgangsmåde til at oprette linjer på salgs- og købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="65544-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="65544-112">Du kan finde flere oplysninger i [Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="65544-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="65544-113">Sådan oprettes standardservicekoder</span><span class="sxs-lookup"><span data-stu-id="65544-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="65544-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Standardservicekoder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="65544-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="65544-115">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="65544-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="65544-116">Udfyld de servicelinjer, der er knyttet til denne servicekode.</span><span class="sxs-lookup"><span data-stu-id="65544-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="65544-117">Tildele en standardservicekode til en serviceartikelgruppe</span><span class="sxs-lookup"><span data-stu-id="65544-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="65544-118">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceartikelgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="65544-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="65544-119">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="65544-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="65544-120">Udfyld de servicelinjer, der er knyttet til denne servicekode.</span><span class="sxs-lookup"><span data-stu-id="65544-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="65544-121">Se også</span><span class="sxs-lookup"><span data-stu-id="65544-121">See Also</span></span>
[<span data-ttu-id="65544-122">Service</span><span class="sxs-lookup"><span data-stu-id="65544-122">Service Management</span></span>](service-service.md)
