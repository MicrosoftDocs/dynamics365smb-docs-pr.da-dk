---
title: "Designoplysninger – Forsyningsplanlægning | Microsoft Docs"
description: "Dette emne indeholder en oversigt over de begreber og principper, der bruges inden for forsyningsplanlægningsfunktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)]."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, planning, reordering, replenishment
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b8a44ff374338c79bd2e1aa31ee60e172f06da5e
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-supply-planning"></a><span data-ttu-id="97630-103">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="97630-103">Design Details: Supply Planning</span></span>
<span data-ttu-id="97630-104">Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges inden for forsyningsplanlægningsfunktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="97630-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Supply Planning features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="97630-105">Det forklarer, hvordan planlægningssystemet fungerer, og hvordan du justerer algoritmer for at opfylde planlægningsbehov i forskellige miljøer.</span><span class="sxs-lookup"><span data-stu-id="97630-105">It explains how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span> <span data-ttu-id="97630-106">Det introducerer først centrale løsningsbegreber og beskriver derefter logikken i den centrale mekanisme, forsyningsafstemning, før du fortsætter med at forklare, hvordan lagerplanlægningen udføres med brug af genbestillingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="97630-106">It first introduces central solution concepts and then describes the logic of the central mechanism, supply balancing, before proceeding to explain how inventory planning is performed with the use of reordering policies.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="97630-107">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="97630-107">In This Section</span></span>  
[<span data-ttu-id="97630-108">Designoplysninger: Centrale begreber i planlægningssystemet</span><span class="sxs-lookup"><span data-stu-id="97630-108">Design Details: Central Concepts of the Planning System</span></span>](design-details-central-concepts-of-the-planning-system.md)  
[<span data-ttu-id="97630-109">Designoplysninger: Reservation, ordresporing og aktionsmeddelelser</span><span class="sxs-lookup"><span data-stu-id="97630-109">Design Details: Reservation, Order Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
[<span data-ttu-id="97630-110">Designoplysninger: Afstemning mellem behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="97630-110">Design Details: Balancing Demand and Supply</span></span>](design-details-balancing-demand-and-supply.md)  
[<span data-ttu-id="97630-111">Designoplysninger: Håndtering af genbestillingsmetoder</span><span class="sxs-lookup"><span data-stu-id="97630-111">Design Details: Handling Reordering Policies</span></span>](design-details-handling-reordering-policies.md)  
[<span data-ttu-id="97630-112">Designoplysninger: Planlægningsparametre</span><span class="sxs-lookup"><span data-stu-id="97630-112">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
[<span data-ttu-id="97630-113">Designoplysninger: Tabellen Planlægningsopgave</span><span class="sxs-lookup"><span data-stu-id="97630-113">Design Details: Planning Assignment Table</span></span>](design-details-planning-assignment-table.md)  
[<span data-ttu-id="97630-114">Designoplysninger: Behov på lokationen TOM</span><span class="sxs-lookup"><span data-stu-id="97630-114">Design Details: Demand at Blank Location</span></span>](design-details-demand-at-blank-location.md)  
[<span data-ttu-id="97630-115">Designoplysninger: Overførsler i planlægning</span><span class="sxs-lookup"><span data-stu-id="97630-115">Design Details: Transfers in Planning</span></span>](design-details-transfers-in-planning.md)

