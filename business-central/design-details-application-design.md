---
title: Designoplysninger | Microsoft Docs
description: Dette indhold indeholder detaljerede tekniske oplysninger om komplekse programfunktioner i Business Central.
author: SorenGP
documentationcenter: ''
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f669944766894e57a772e229a436953953f3892c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785185"
---
# <a name="design-details"></a><span data-ttu-id="fbcb5-103">Designoplysninger</span><span class="sxs-lookup"><span data-stu-id="fbcb5-103">Design Details</span></span>
<span data-ttu-id="fbcb5-104">Dette indhold indeholder detaljerede tekniske oplysninger om komplekse programfunktioner i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="fbcb5-104">This content contains detailed technical information about complex application features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

 <span data-ttu-id="fbcb5-105">Indholdet af designoplysningerne er rettet mod iværksættere, udviklere og superbrugere, der har brug for en dybere indsigt i at implementere, tilpasse eller opsætte de pågældende funktioner.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-105">Design details content is aimed at implementers, developers, and super users who need deeper insight to implement, customize, or set up the features in question.</span></span>  

|<span data-ttu-id="fbcb5-106">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="fbcb5-106">**To**</span></span>|<span data-ttu-id="fbcb5-107">**Se**</span><span class="sxs-lookup"><span data-stu-id="fbcb5-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="fbcb5-108">Lær, hvordan planlægningssystemet fungerer, og hvordan du justerer algoritmer for at opfylde planlægningsbehov i forskellige miljøer.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-108">Learn how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="fbcb5-109">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="fbcb5-109">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|  
|<span data-ttu-id="fbcb5-110">Forstå mekanismerne i prisberegningsprogrammet, f.eks. kostmetode og kostregulering, samt hvilke regnskabsprincipper, de er designet til.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-110">Understand mechanisms in the costing engine, such as costing method and cost adjustment, and which accounting principles they are designed for.</span></span>|[<span data-ttu-id="fbcb5-111">Designoplysninger: Lagerkostmetode</span><span class="sxs-lookup"><span data-stu-id="fbcb5-111">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  
|<span data-ttu-id="fbcb5-112">Lær om de centrale principper bag avancerede og grundlæggende lagerfunktioner, og hvordan de integreres med andre forsyningskædefunktioner.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-112">Learn about central principles behind advanced and basic warehouse features and how they integrate with other supply chain features.</span></span>|[<span data-ttu-id="fbcb5-113">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="fbcb5-113">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)|  
|<span data-ttu-id="fbcb5-114">Få mere at vide om historisk og aktuelt design af varesporingsfunktionalitet, og hvordan den integreres med reservationssystemet for at medtage serienumre/lotnumre i disponeringsberegninger.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-114">Learn about historic and the current design of item tracking functionality and how it integrates with the reservation system to include serial/lot numbers in availability calculations.</span></span>|[<span data-ttu-id="fbcb5-115">Designoplysninger: Varesporing</span><span class="sxs-lookup"><span data-stu-id="fbcb5-115">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)|  
|<span data-ttu-id="fbcb5-116">Få mere at vide om funktionen for bogføringslinjer til finanskladder, herunder de seneste forenklinger til design af codeunit 12.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-116">Learn about the General Journal Posting Line feature, including recent simplifications to the design of codeunit 12.</span></span>|[<span data-ttu-id="fbcb5-117">Designoplysninger: Bogføringslinje i finanskladde</span><span class="sxs-lookup"><span data-stu-id="fbcb5-117">Design Details: General Journal Post Line</span></span>](design-details-general-journal-post-line.md)|
|<span data-ttu-id="fbcb5-118">Få mere at vide om designet til lagrings- og bogføringsdimensioner, herunder kodeeksempler på at overflytte og opgradere dimensionskode.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-118">Learn about the design for storing and posting dimensions, including code examples on how to migrate and upgrade dimension code.</span></span>|[<span data-ttu-id="fbcb5-119">Designoplysninger: Dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="fbcb5-119">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries-overview.md)|

## <a name="see-also"></a><span data-ttu-id="fbcb5-120">Se også</span><span class="sxs-lookup"><span data-stu-id="fbcb5-120">See Also</span></span>

[<span data-ttu-id="fbcb5-121">Skabelon</span><span class="sxs-lookup"><span data-stu-id="fbcb5-121">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="fbcb5-122">Administrere lageromkostninger</span><span class="sxs-lookup"><span data-stu-id="fbcb5-122">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="fbcb5-123">Logistik</span><span class="sxs-lookup"><span data-stu-id="fbcb5-123">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="fbcb5-124">Konfigurere komplekse moduler ved hjælp af bedste praksis</span><span class="sxs-lookup"><span data-stu-id="fbcb5-124">Setting Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
<span data-ttu-id="fbcb5-125">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fbcb5-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
