---
title: Definere koder for standardservices | Microsoft Docs
description: Få at vide, hvordan du definerer koder for serviceaktiviteter, du udfører ofte.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 766af833ddef09b72a520e97d47a32fb7b77fd86
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877419"
---
# <a name="set-up-standard-service-codes"></a><span data-ttu-id="4ccd0-103">Konfigurere standardservicekoder</span><span class="sxs-lookup"><span data-stu-id="4ccd0-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="4ccd0-104">Når der foretages standardservice, skal der ofte oprettes servicedokumenter, der bruger servicelinjer, der indeholder ensartede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="4ccd0-105">For at gøre det nemmere at oprette disse linjer kan du oprette standardservicekoder, der har et foruddefineret sæt af servicelinjer.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="4ccd0-106">Når du vælger koden i et servicedokument, indsættes linjerne automatisk.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="4ccd0-107">Du kan oprette et hvilket som helst antal standardservicekoder, og hver kode kan have et ubegrænset antal servicelinjer af forskellige typer, herunder vare, ressource, pris eller tekst, tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="4ccd0-108">Du opretter servicelinjer for hver standardservicekode på kortet **Standardservicekode**.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="4ccd0-109">Derefter tildeler du standardservicekoder til serviceartikelgrupper på siden **Koder til standardserv.varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="4ccd0-110">Senere, når du opretter et servicedokument, du kan bruge handlingen **Hent standardservicekoder** til at tilføje servicelinjer.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="4ccd0-111">Du kan bruge den samme fremgangsmåde til at oprette linjer på salgs- og købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="4ccd0-112">Du kan finde flere oplysninger i [Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="4ccd0-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="4ccd0-113">Sådan oprettes standardservicekoder</span><span class="sxs-lookup"><span data-stu-id="4ccd0-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="4ccd0-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Standardservicekoder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4ccd0-115">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="4ccd0-116">Udfyld de servicelinjer, der er knyttet til denne servicekode.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="4ccd0-117">Tildele en standardservicekode til en serviceartikelgruppe</span><span class="sxs-lookup"><span data-stu-id="4ccd0-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="4ccd0-118">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceartikelgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4ccd0-119">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="4ccd0-120">Udfyld de servicelinjer, der er knyttet til denne servicekode.</span><span class="sxs-lookup"><span data-stu-id="4ccd0-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4ccd0-121">Se også</span><span class="sxs-lookup"><span data-stu-id="4ccd0-121">See Also</span></span>
[<span data-ttu-id="4ccd0-122">Service Management</span><span class="sxs-lookup"><span data-stu-id="4ccd0-122">Service Management</span></span>](service-service.md)