---
title: Designoplysninger – Logistik | Microsoft Docs
description: Dette emne giver et overblik over designet, begreberne og principperne bag logistikfunktionerne i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 36e8d8dadc52ab10492fb5ab1cbfe158b069cd9b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381463"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="13933-103">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="13933-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="13933-104">Denne dokumentation giver et overblik over de begreber og principper, der bruges i logistikfunktionerne i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="13933-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="13933-105">Det forklarer designet bag centrallagerfunktioner, og hvordan logistik integreres med andre funktioner i forsyningskæden.</span><span class="sxs-lookup"><span data-stu-id="13933-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="13933-106">Med henblik på at skelne mellem forskellige kompleksitetsniveauer af logistik er dette dokument opdelt i to generelle grupper, grundlæggende og avancerede lageropsætninger, angivet ved titlerne på afsnittene.</span><span class="sxs-lookup"><span data-stu-id="13933-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="13933-107">Denne simple differentiering dækker forskellige kompleksitetsniveauer, som defineret af produktdetaljer og lokationsopsætning.</span><span class="sxs-lookup"><span data-stu-id="13933-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="13933-108">Du kan finde flere oplysninger i [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md)</span><span class="sxs-lookup"><span data-stu-id="13933-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="13933-109">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="13933-109">In This Section</span></span>  
[<span data-ttu-id="13933-110">Designoplysninger: Oversigt over logistik</span><span class="sxs-lookup"><span data-stu-id="13933-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="13933-111">Designoplysninger: Opsætning af lager</span><span class="sxs-lookup"><span data-stu-id="13933-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="13933-112">Designoplysninger: Indgående lagerflow</span><span class="sxs-lookup"><span data-stu-id="13933-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="13933-113">Designoplysninger: Internt lagerflow</span><span class="sxs-lookup"><span data-stu-id="13933-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="13933-114">Designoplysninger: Tilgængelighed i lageret</span><span class="sxs-lookup"><span data-stu-id="13933-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="13933-115">Designoplysninger: Udgående lagerflow</span><span class="sxs-lookup"><span data-stu-id="13933-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="13933-116">Designoplysninger: Integration med lager</span><span class="sxs-lookup"><span data-stu-id="13933-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]