---
title: Flere kontrakter | Microsoft Docs
description: "Afhængigt af dine serviceaftaler med en kunde, skal du evt. håndtere en serviceartikel under flere servicekontrakter."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c4abfbcb3bc182fa14c44c427bc41ebd9d67f6cf
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="multiple-contracts"></a><span data-ttu-id="9caf8-103">Flere kontrakter</span><span class="sxs-lookup"><span data-stu-id="9caf8-103">Multiple Contracts</span></span>
<span data-ttu-id="9caf8-104">Afhængigt af dine serviceaftaler med en kunde, skal du evt. håndtere en serviceartikel under flere servicekontrakter.</span><span class="sxs-lookup"><span data-stu-id="9caf8-104">Depending on your service level agreements with a customer, you may have to handle a service item under more than one service contract.</span></span>  
  
<span data-ttu-id="9caf8-105">Ved at håndtere en serviceartikel under flere kontrakter kan du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="9caf8-105">By handling a service item under multiple contracts, you can do the following:</span></span>  
  
* <span data-ttu-id="9caf8-106">Udstede forskellige kontrakter for samme serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="9caf8-106">Issue different contracts for the same service item.</span></span>  
* <span data-ttu-id="9caf8-107">Servicere delene separat.</span><span class="sxs-lookup"><span data-stu-id="9caf8-107">Service parts separately.</span></span>  
* <span data-ttu-id="9caf8-108">Tage forskellige kvalifikationer, der kræves til forskellige dele af serviceartiklen, i betragtning, f.eks. mekaniske komponenter og software.</span><span class="sxs-lookup"><span data-stu-id="9caf8-108">Consider different skills that are required to service different aspects of a service item, such as mechanical components and software.</span></span>  
* <span data-ttu-id="9caf8-109">Angive forskellige svartidspunkter og intervaller for servicering af forskellige dele af en serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="9caf8-109">Specify different response times and frequencies in servicing different parts of a service item.</span></span>  
* <span data-ttu-id="9caf8-110">Angive, at der skal foretages forskellige typer aktiviteter på en serviceartikel, når serviceartiklen kræver forskellige typer service på forskellige tidspunkter.</span><span class="sxs-lookup"><span data-stu-id="9caf8-110">Address different kinds of activities to be performed on a service item when the service item requires different types of service in different time periods.</span></span>  
* <span data-ttu-id="9caf8-111">Vælge og tildele det korrekte kontraktnummer til en serviceartikellinje, når du opretter en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="9caf8-111">Select and assign an appropriate contract number to a service item line when you are creating a service order.</span></span>  
* <span data-ttu-id="9caf8-112">Håndtere relevante finansielle oplysninger om serviceartikler og serviceaftaler.</span><span class="sxs-lookup"><span data-stu-id="9caf8-112">Handle relevant financial information about service items and service level agreements.</span></span>  
  
<span data-ttu-id="9caf8-113">Følgende viser eksempler på brugen af flere kontrakter.</span><span class="sxs-lookup"><span data-stu-id="9caf8-113">You can consider the following examples of using the multiple contracts functionality.</span></span>  
  
## <a name="creating-multiple-contracts-per-service-item"></a><span data-ttu-id="9caf8-114">Oprette flere kontrakter pr. serviceartikel</span><span class="sxs-lookup"><span data-stu-id="9caf8-114">Creating Multiple Contracts per Service Item</span></span>  
<span data-ttu-id="9caf8-115">Du kan oprette en servicekontrakt eller et kontrakttilbud manuelt for de serviceartikler, der allerede er registreret i ikke-annullerede kontrakter, der tilhører den samme kunde.</span><span class="sxs-lookup"><span data-stu-id="9caf8-115">You can manually create a service contract or contract quote for service items already registered in non-canceled contracts owned by the same customer.</span></span> <span data-ttu-id="9caf8-116">Det kan gøres ved at følge standardproceduren til oprettelse af servicekontrakter og servicekontrakttilbud.</span><span class="sxs-lookup"><span data-stu-id="9caf8-116">To do this, follow the standard procedure of creating service contracts and service contract quotes.</span></span> <span data-ttu-id="9caf8-117">Du kan finde flere oplysninger i [Fremgangsmåde: Arbejde med servicekontrakter og servicekontrakttilbud](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span><span class="sxs-lookup"><span data-stu-id="9caf8-117">For more information, see [How to: Work with Service Contracts and Service Contract Quotes](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span></span>  
  
<span data-ttu-id="9caf8-118">Når du tilføjer en serviceartikel på en kontraktlinje, som er registreret i andre servicekontrakter eller kontrakttilbud, vises en advarsel om, at serviceartiklen allerede tilhører en eller flere servicekontrakter eller et eller flere kontrakttilbud.</span><span class="sxs-lookup"><span data-stu-id="9caf8-118">When you add a service item on a contract line that is registered in other service contracts or contract quotes, a warning message is displayed stating that the service item already belongs to one or more service contracts or contract quotes.</span></span> <span data-ttu-id="9caf8-119">Hvis du bekræfter advarslen, kopieres alle relevante oplysninger om serviceartiklen til en nyoprettet kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="9caf8-119">If you confirm this message, all relevant service item information is copied to a newly created contract line.</span></span>  
  
## <a name="copying-documents"></a><span data-ttu-id="9caf8-120">Kopiere linjer</span><span class="sxs-lookup"><span data-stu-id="9caf8-120">Copying Documents</span></span>  
<span data-ttu-id="9caf8-121">Du kan automatisk oprette en servicekontrakt eller et kontrakttilbud for serviceartikler, der allerede er registreret i andre servicekontrakter eller kontrakttilbud ved hjælp af handlingen **Kopiér dokument**.</span><span class="sxs-lookup"><span data-stu-id="9caf8-121">You can automatically create a service contract or contract quote for service items that are already registered in other service contracts or contract quotes by using the **Copy Document** action.</span></span>  
  
## <a name="creating-service-orders-for-multiple-contracts"></a><span data-ttu-id="9caf8-122">Oprette serviceordrer for flere kontrakter</span><span class="sxs-lookup"><span data-stu-id="9caf8-122">Creating Service Orders for Multiple Contracts</span></span>  
<span data-ttu-id="9caf8-123">Du kan oprette en serviceordre manuelt for en serviceartikel, der er registreret i flere aktive kontrakter.</span><span class="sxs-lookup"><span data-stu-id="9caf8-123">You can manually create a service order for a service item that is registered in multiple active contracts.</span></span> <span data-ttu-id="9caf8-124">En servicekontrakt er aktiv, når den er underskrevet og ikke er udløbet.</span><span class="sxs-lookup"><span data-stu-id="9caf8-124">A service contract is active when it is signed and not expired.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9caf8-125">Se også</span><span class="sxs-lookup"><span data-stu-id="9caf8-125">See Also</span></span>  
[<span data-ttu-id="9caf8-126">Opfylde servicekontrakter</span><span class="sxs-lookup"><span data-stu-id="9caf8-126">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)  
[<span data-ttu-id="9caf8-127">Fremgangsmåde: Oprette serviceordrer</span><span class="sxs-lookup"><span data-stu-id="9caf8-127">How to: Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
