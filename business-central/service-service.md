---
title: Service | Microsoft Docs
description: Lær at bruge funktioner, der er udviklet til at understøtte reparations- og teknisk service-handlinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 6490ad13833c97c79c232b6433b4b2f51e51bc4f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192359"
---
# <a name="service-management"></a><span data-ttu-id="e93b5-103">Service Management</span><span class="sxs-lookup"><span data-stu-id="e93b5-103">Service Management</span></span>
> [!NOTE]
> <span data-ttu-id="e93b5-104">Funktioner, der beskrives i dette emne og underordnede emner, er kun synlige i brugergrænsefladen, hvis du har oplevelsen **Premium**.</span><span class="sxs-lookup"><span data-stu-id="e93b5-104">Functionality described in this topic and sub topics is only visible in the user interface if you have the **Premium** experience.</span></span> <span data-ttu-id="e93b5-105">Du kan finde flere oplysninger i [Ændre, hvilke funktioner der vises](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="e93b5-105">For more information, see [Change Which Features are Displayed](ui-experiences.md).</span></span>

<span data-ttu-id="e93b5-106">En vigtig del af enhver virksomhed er at yde løbende service til kunderne, og det kan være en kilde til såvel kundetilfredshed og -loyalitet i tillæg til indtjening.</span><span class="sxs-lookup"><span data-stu-id="e93b5-106">Providing ongoing service to customers is an important part of any business and one that can be a source of customer satisfaction and loyalty, in addition to revenue.</span></span> <span data-ttu-id="e93b5-107">Administration og sporing af service er dog ikke altid let, men [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder et sæt værktøjer, der kan være en hjælp.</span><span class="sxs-lookup"><span data-stu-id="e93b5-107">However, managing and tracking service is not always easy, and [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a set of tools to help.</span></span> <span data-ttu-id="e93b5-108">Disse værktøjer er designet til at understøtte operationer for reparationsværksteder og feltservice og kan bruges i forretningsscenarier som f.eks. komplicerede servicedistributionssystemer, industrielle servicemiljøer med styklister og masseekspedition af serviceteknikere med behov for administration af reservedele.</span><span class="sxs-lookup"><span data-stu-id="e93b5-108">These tools are designed to support repair shop and field service operations, and can be used in business scenarios such as complex customer service distribution systems, industrial service environments with bills of materials, and high volume dispatching of service technicians with requirements for spare parts management.</span></span>  

 <span data-ttu-id="e93b5-109">Med disse værktøjer kan du udføre følgende:</span><span class="sxs-lookup"><span data-stu-id="e93b5-109">With these tools you can accomplish the following:</span></span>  

* <span data-ttu-id="e93b5-110">Planlæg servicebesøg og opret serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="e93b5-110">Schedule service calls and set up service orders.</span></span>  
* <span data-ttu-id="e93b5-111">Spor reservedele og forsyninger.</span><span class="sxs-lookup"><span data-stu-id="e93b5-111">Track repair parts and supplies.</span></span>  
* <span data-ttu-id="e93b5-112">Tildel servicepersonale baseret på færdigheder og tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="e93b5-112">Assign service personnel based on skill and availability.</span></span>  
* <span data-ttu-id="e93b5-113">Producer serviceestimater og servicefakturaer.</span><span class="sxs-lookup"><span data-stu-id="e93b5-113">Provide service estimates and service invoices.</span></span>  

<span data-ttu-id="e93b5-114">Derudover kan du standardisere brug af koder, oprette kontrakter, implementere rabatpolitikker og oprette rutekort for servicemedarbejdere.</span><span class="sxs-lookup"><span data-stu-id="e93b5-114">In addition, you can standardize coding, set up contracts, implement a discounting policy, and create route maps for service employees.</span></span>  

<span data-ttu-id="e93b5-115">Generelt er der to aspekter i servicestyring: Konfiguration og opsætning af systemet og brug af systemet til prissætning, kontrakter, ordrer, allokering af servicepersonale og sagsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="e93b5-115">In general, there are two aspects to service management: configuring and setting up your system, and using it for pricing, contracts, orders, service personnel dispatch, and job scheduler.</span></span>  

<span data-ttu-id="e93b5-116">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="e93b5-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="e93b5-117">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="e93b5-117">**To**</span></span>|<span data-ttu-id="e93b5-118">**Se**</span><span class="sxs-lookup"><span data-stu-id="e93b5-118">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="e93b5-119">Konfigurere Service, herunder fejlkoder, politikker, standarddokumenter og skabeloner.</span><span class="sxs-lookup"><span data-stu-id="e93b5-119">Set up Service Management, including fault codes, policies, default documents and templates.</span></span>|[<span data-ttu-id="e93b5-120">Konfigurere Service</span><span class="sxs-lookup"><span data-stu-id="e93b5-120">Setting Up Service Management</span></span>](service-setup-service.md)|  
|<span data-ttu-id="e93b5-121">Administrere serviceprissætning, oprette serviceartikler og forstå, hvordan status overvåges.</span><span class="sxs-lookup"><span data-stu-id="e93b5-121">Manage service pricing, create service items, and understand how to monitor progress.</span></span>|[<span data-ttu-id="e93b5-122">Planlægning af service</span><span class="sxs-lookup"><span data-stu-id="e93b5-122">Planning Service</span></span>](service-plan-service.md)|  
|<span data-ttu-id="e93b5-123">Oprette og administrere aftaler mellem dig og dine kunder.</span><span class="sxs-lookup"><span data-stu-id="e93b5-123">Create and manage contractual agreements between you and your customers.</span></span>|[<span data-ttu-id="e93b5-124">Opfylde servicekontrakter</span><span class="sxs-lookup"><span data-stu-id="e93b5-124">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)|  
|<span data-ttu-id="e93b5-125">Levere service til kunder og fakturere serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="e93b5-125">Provide service to customers, and invoice service orders.</span></span>|[<span data-ttu-id="e93b5-126">Levering af service</span><span class="sxs-lookup"><span data-stu-id="e93b5-126">Delivering Service</span></span>](service-deliver-service.md)|  

## <a name="see-also"></a><span data-ttu-id="e93b5-127">Se også</span><span class="sxs-lookup"><span data-stu-id="e93b5-127">See Also</span></span>  
<span data-ttu-id="e93b5-128">[Administrere tilgodehavender](receivables-manage-receivables.md) </span><span class="sxs-lookup"><span data-stu-id="e93b5-128">[Managing Receivables](receivables-manage-receivables.md) </span></span>  
<span data-ttu-id="e93b5-129">[Sager](projects-how-create-jobs.md) </span><span class="sxs-lookup"><span data-stu-id="e93b5-129">[Jobs](projects-how-create-jobs.md) </span></span>  
<span data-ttu-id="e93b5-130">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="e93b5-130">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] ](index.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
