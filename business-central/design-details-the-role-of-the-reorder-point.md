---
title: "Designoplysninger – Genbestillingspunktets rolle | Microsoft Docs"
description: "Dette emne beskriver vigtigheden af at angive et genbestillingspunkt, så du ved, hvornår du skal bestille mere til lager."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 34fac8c3c8f5223fef950cbbda51c26ffff41f94
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-the-role-of-the-reorder-point"></a><span data-ttu-id="43749-103">Designoplysninger: Genbestillingspunktets rolle</span><span class="sxs-lookup"><span data-stu-id="43749-103">Design Details: The Role of the Reorder Point</span></span>
<span data-ttu-id="43749-104">Udover den generelle afstemning af udbud og efterspørgsel, skal planlægningssystemet også overvåge lagerniveauer for de pågældende varer for at respektere de definerede genbestillingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="43749-104">In addition to the general balancing of supply and demand, the planning system must also monitor inventory levels for the affected items to respect the defined reordering policies.</span></span>  
  
<span data-ttu-id="43749-105">Et genbestillingspunkt repræsenterer behov under leveringstid.</span><span class="sxs-lookup"><span data-stu-id="43749-105">A reorder point represents demand during lead time.</span></span> <span data-ttu-id="43749-106">Når den projekterede lagerbeholdning kommer under den lagerbeholdning, der er defineret af genbestillingspunktet, er det tid til at bestille mere.</span><span class="sxs-lookup"><span data-stu-id="43749-106">When the projected inventory passes below the inventory level defined by the reorder point, it is time to order more quantity.</span></span> <span data-ttu-id="43749-107">I mellemtiden forventes lagerføring at reduceres gradvist og eventuelt nå nul (eller sikkerhedslagerniveau), indtil genopfyldningen ankommer.</span><span class="sxs-lookup"><span data-stu-id="43749-107">Meanwhile, the inventory is expected to decrease gradually and possibly reach zero (or the safety stock level), until the replenishment arrives.</span></span>  
  
<span data-ttu-id="43749-108">Planlægningssystemet vil derfor foreslå en forsyningsordre, der er planlagt fremad, når den forventede lagerbeholdning er under genbestillingspunktet.</span><span class="sxs-lookup"><span data-stu-id="43749-108">Accordingly, the planning system will suggest a forward-scheduled supply order at the point when the projected inventory passes below the reorder point.</span></span>  
  
<span data-ttu-id="43749-109">Genbestillingspunktet afspejler et bestemt lagerniveau.</span><span class="sxs-lookup"><span data-stu-id="43749-109">The reorder point reflects a certain inventory level.</span></span> <span data-ttu-id="43749-110">Lagerniveauer kan dog flytte betydeligt under intervallet, og planlægningssystemet skal derfor hele tiden overvåge den forventede disponible beholdning.</span><span class="sxs-lookup"><span data-stu-id="43749-110">However, inventory levels can move significantly during the time bucket and, therefore, the planning system must constantly monitor the projected available inventory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="43749-111">Se også</span><span class="sxs-lookup"><span data-stu-id="43749-111">See Also</span></span>  
<span data-ttu-id="43749-112">[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="43749-112">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="43749-113">[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="43749-113">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="43749-114">[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="43749-114">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="43749-115">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="43749-115">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
