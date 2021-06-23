---
title: Designoplysninger – Forsyningsplanlægning | Microsoft Docs
description: Dette emne indeholder en oversigt over de begreber og principper, der bruges inden for forsyningsplanlægningsfunktionerne i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, planning, reordering, replenishment
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 78b5700646d95d9cdc38a7a67663473fafddaa2c
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214824"
---
# <a name="design-details-supply-planning"></a><span data-ttu-id="9877f-103">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="9877f-103">Design Details: Supply Planning</span></span>
<span data-ttu-id="9877f-104">Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges inden for forsyningsplanlægningsfunktionerne i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9877f-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Supply Planning features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="9877f-105">Det forklarer, hvordan planlægningssystemet fungerer, og hvordan du justerer algoritmer for at opfylde planlægningsbehov i forskellige miljøer.</span><span class="sxs-lookup"><span data-stu-id="9877f-105">It explains how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span> <span data-ttu-id="9877f-106">Det introducerer først centrale løsningsbegreber og beskriver derefter logikken i den centrale mekanisme, forsyningsafstemning, før du fortsætter med at forklare, hvordan lagerplanlægningen udføres med brug af genbestillingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="9877f-106">It first introduces central solution concepts and then describes the logic of the central mechanism, supply balancing, before proceeding to explain how inventory planning is performed with the use of reordering policies.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="9877f-107">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="9877f-107">In This Section</span></span>  
[<span data-ttu-id="9877f-108">Designoplysninger: Centrale begreber i planlægningssystemet</span><span class="sxs-lookup"><span data-stu-id="9877f-108">Design Details: Central Concepts of the Planning System</span></span>](design-details-central-concepts-of-the-planning-system.md)  
[<span data-ttu-id="9877f-109">Designoplysninger: Reservation, ordresporing og aktionsmeddelelser</span><span class="sxs-lookup"><span data-stu-id="9877f-109">Design Details: Reservation, Order Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
[<span data-ttu-id="9877f-110">Designoplysninger: Afstemning mellem behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="9877f-110">Design Details: Balancing Demand and Supply</span></span>](design-details-balancing-demand-and-supply.md)  
[<span data-ttu-id="9877f-111">Designoplysninger: Håndtering af genbestillingsmetoder</span><span class="sxs-lookup"><span data-stu-id="9877f-111">Design Details: Handling Reordering Policies</span></span>](design-details-handling-reordering-policies.md)  
[<span data-ttu-id="9877f-112">Designoplysninger: Planlægningsparametre</span><span class="sxs-lookup"><span data-stu-id="9877f-112">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
[<span data-ttu-id="9877f-113">Designoplysninger: Tabellen Planlægningsopgave</span><span class="sxs-lookup"><span data-stu-id="9877f-113">Design Details: Planning Assignment Table</span></span>](design-details-planning-assignment-table.md)  
[<span data-ttu-id="9877f-114">Designoplysninger: Behov på lokationen TOM</span><span class="sxs-lookup"><span data-stu-id="9877f-114">Design Details: Demand at Blank Location</span></span>](design-details-demand-at-blank-location.md)  
[<span data-ttu-id="9877f-115">Designoplysninger: Overførsler i planlægning</span><span class="sxs-lookup"><span data-stu-id="9877f-115">Design Details: Transfers in Planning</span></span>](design-details-transfers-in-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]