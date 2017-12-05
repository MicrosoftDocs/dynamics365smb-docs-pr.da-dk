---
title: "Opsætning af Service | Microsoft Docs"
description: "Oversigt over opgaver til konfiguration af Service, så det passer til den måde, organisationen administrerer sine tjenester på."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service items, repairs, maintenance, fix
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7eac962e0c9863d8c6ed9bcff19f320687f217ff
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---

# <a name="setting-up-service-management"></a><span data-ttu-id="db554-103">Konfigurere Service</span><span class="sxs-lookup"><span data-stu-id="db554-103">Setting Up Service Management</span></span>
<span data-ttu-id="db554-104">Før du kan begynde at bruge Service-funktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)], der er et par ting, du skal konfigurere.</span><span class="sxs-lookup"><span data-stu-id="db554-104">Before you can start using Service Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)], there are a few things to set up.</span></span> <span data-ttu-id="db554-105">Du kan f.eks. oprette koder for standardservice, symptom- og fejlkoder, og de serviceartikler og serviceartikeltyper efter de behov, som virksomhedens debitorservice kræver.</span><span class="sxs-lookup"><span data-stu-id="db554-105">For example, you can establish coding for standard services, symptoms, and fault codes, and the service items and service item types that your company's customer service needs require.</span></span>  

<span data-ttu-id="db554-106">Når du konfigurerer service, skal du beslutte, hvilke serviceydelser du vil tilbyde kunderne, og fastlægge en plan for disse serviceydelser.</span><span class="sxs-lookup"><span data-stu-id="db554-106">When you set up Service Management, you must decide what services to offer customers and the schedule for those services.</span></span> <span data-ttu-id="db554-107">En service er en type arbejde, der udføres af en eller flere ressourcer og ydes til en kunde.</span><span class="sxs-lookup"><span data-stu-id="db554-107">A service is a type of work performed by one or more resources and provided to a customer.</span></span> <span data-ttu-id="db554-108">En service kan f.eks. være en type computerreparation.</span><span class="sxs-lookup"><span data-stu-id="db554-108">For example, a service could be a type of computer repair.</span></span> <span data-ttu-id="db554-109">En serviceartikel er det udstyr eller den artikel, der har brug for service, f.eks. den computer, der skal repareres, og som er installeret hos en bestemt kunde.</span><span class="sxs-lookup"><span data-stu-id="db554-109">A service item is the equipment or item needing servicing, for example, the computer needing repair, installed at a specific customer.</span></span> <span data-ttu-id="db554-110">Du kan konfigurere serviceydelser som en del af en gruppe af relaterede reparations- eller vedligeholdelsesydelser.</span><span class="sxs-lookup"><span data-stu-id="db554-110">You can set up services as part of a group of related repair or maintenance items.</span></span>  
  
<span data-ttu-id="db554-111">Når du definerer en service, kan du knytte den til de færdigheder, der kræves for at udføre den pågældende service.</span><span class="sxs-lookup"><span data-stu-id="db554-111">When you define a service, you can associate it with the skills required to perform the service.</span></span> <span data-ttu-id="db554-112">Hvis du vil hjælpe servicerepræsentanterne med at være effektive, kan du også konfigurere retningslinjer for fejlfinding i realtid og tildele typiske startgebyrer og transportgebyrer eller andre gebyrer.</span><span class="sxs-lookup"><span data-stu-id="db554-112">To help your service representatives be efficient, you can also set up real time troubleshooting guidelines and assign typical startup costs, such as travel costs or other fees.</span></span>  

<span data-ttu-id="db554-113">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="db554-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  
  
| <span data-ttu-id="db554-114">Til</span><span class="sxs-lookup"><span data-stu-id="db554-114">To</span></span> | <span data-ttu-id="db554-115">Se</span><span class="sxs-lookup"><span data-stu-id="db554-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="db554-116">Definere koder, der automatisk tildeler linjer i servicedokumenter for tjenester, du leverer ofte.</span><span class="sxs-lookup"><span data-stu-id="db554-116">Set up codes that automatically assign lines on service documents for services you deliver often.</span></span> |[<span data-ttu-id="db554-117">Fremgangsmåde: Definere koder for standardservices</span><span class="sxs-lookup"><span data-stu-id="db554-117">How to: Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)|
| <span data-ttu-id="db554-118">Oprette generelle indstillinger, der styrer aspekter af Service-processer.</span><span class="sxs-lookup"><span data-stu-id="db554-118">Establish general settings that control aspects of Service Management Processes.</span></span>|[<span data-ttu-id="db554-119">Fremgangsmåde: Konfigurere serviceprocesser</span><span class="sxs-lookup"><span data-stu-id="db554-119">How to: Configure Service Processes</span></span>](service-setup-service-processes.md)|
| <span data-ttu-id="db554-120">Definere, hvordan virksomheden håndterer fejlrapportering.</span><span class="sxs-lookup"><span data-stu-id="db554-120">Define how your organization works with fault reporting.</span></span> |[<span data-ttu-id="db554-121">Fremgangsmåde: Definere fejlrapportering</span><span class="sxs-lookup"><span data-stu-id="db554-121">How to: Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md) |
| <span data-ttu-id="db554-122">Opret de servicetilbud, som din virksomhed leverer til kunder.</span><span class="sxs-lookup"><span data-stu-id="db554-122">Set up the service offerings that your company delivers to customers.</span></span>|[<span data-ttu-id="db554-123">Fremgangsmåde: Definere servicetilbud</span><span class="sxs-lookup"><span data-stu-id="db554-123">How to: Set Up Service Offerings</span></span>](service-how-setup-service-offerings.md)|
| <span data-ttu-id="db554-124">Give adgang til retningslinjer for fejlfinding, som hjælper servicerepræsentanter med at levere hurtigere service.</span><span class="sxs-lookup"><span data-stu-id="db554-124">Provide troubleshooting guidelines that help service reps deliver faster service.</span></span> |[<span data-ttu-id="db554-125">Sådan gør du: Definere fejlfinding</span><span class="sxs-lookup"><span data-stu-id="db554-125">How to: Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md) |
| <span data-ttu-id="db554-126">Oprette ressourceallokering, som gør det nemt at tildele den rigtige ressource til en serviceopgave.</span><span class="sxs-lookup"><span data-stu-id="db554-126">Set up resource allocation to make it easy to assign the right resource to a service task.</span></span> |[<span data-ttu-id="db554-127">Fremgangsmåde: Definere ressourceallokering</span><span class="sxs-lookup"><span data-stu-id="db554-127">How to: Set Up Resource Allocation</span></span>](service-how-setup-resource-allocation.md) |
| <span data-ttu-id="db554-128">Definere prissætning for services og oprette yderligere serviceomkostninger til vurdering på serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="db554-128">Define pricing for services, and set up additional service costs to assess on service orders.</span></span> |[<span data-ttu-id="db554-129">Fremgangsmåde: Konfigurere prissætning og ekstra omkostninger for services</span><span class="sxs-lookup"><span data-stu-id="db554-129">How to: Set Up Pricing and Additional Costs for Services</span></span>](service-how-setup-service-costs-pricing.md)|
| <span data-ttu-id="db554-130">Konfigurer tingene, så du kan spore ressourcetimer og serviceordrestatus med det formål at kunne estimere arbejdsbelastning og servicebehov.</span><span class="sxs-lookup"><span data-stu-id="db554-130">Set things up so you can track resource hours and service order status in order to forecast workloads and service needs.</span></span>|[<span data-ttu-id="db554-131">Sådan gør du: Definere arbejdstimer og serviceåbningstider</span><span class="sxs-lookup"><span data-stu-id="db554-131">How to: Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)|
| <span data-ttu-id="db554-132">Angiv indstillinger for reparationsstatus, så du kan overvåge status for reparationer.</span><span class="sxs-lookup"><span data-stu-id="db554-132">Set up repair status options so that you can monitor progress on repairs.</span></span> | [<span data-ttu-id="db554-133">Fremgangsmåde: Konfigurere statusser for serviceordrer og reparationer</span><span class="sxs-lookup"><span data-stu-id="db554-133">How to: Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)|
| <span data-ttu-id="db554-134">Oprette et udlånsprogram, så du kan låne en erstatning, mens du arbejder på en serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="db554-134">Set up a loaner program, so you can lend a substitute while you work on a service item.</span></span> |[<span data-ttu-id="db554-135">Fremgangsmåde: Oprette et udlånsprogram</span><span class="sxs-lookup"><span data-stu-id="db554-135">How to: Set Up a Loaner Program</span></span>](service-how-setup-loaner-program.md) |
| <span data-ttu-id="db554-136">Konfigurere serviceartikler og serviceartikelkomponenter.</span><span class="sxs-lookup"><span data-stu-id="db554-136">Set up service items and service item components.</span></span> |[<span data-ttu-id="db554-137">Sådan gør du: Definere serviceartikler</span><span class="sxs-lookup"><span data-stu-id="db554-137">How to: Set Up Service Items</span></span>](service-how-setup-service-items.md) |
| <span data-ttu-id="db554-138">Skab grundlaget for oprettelse af servicekontrakter og kontrakttilbud.</span><span class="sxs-lookup"><span data-stu-id="db554-138">Lay the groundwork for creating service contracts and contract quotes.</span></span> |[<span data-ttu-id="db554-139">Sådan gør du: Definere servicekontrakter</span><span class="sxs-lookup"><span data-stu-id="db554-139">How to: Set Up Service Contracts</span></span>](service-how-setup-service-contracts.md) |

## <a name="see-also"></a><span data-ttu-id="db554-140">Se også</span><span class="sxs-lookup"><span data-stu-id="db554-140">See also</span></span>
[<span data-ttu-id="db554-141">Service Management</span><span class="sxs-lookup"><span data-stu-id="db554-141">Service Management</span></span>](service-service.md)  
<span data-ttu-id="db554-142">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="db554-142">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
