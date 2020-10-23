---
title: Designoplysninger | Microsoft Docs
description: Dette indhold indeholder detaljerede tekniske oplysninger om komplekse programfunktioner i Business Central.
author: SorenGP
documentationcenter: ''
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b473da21e35ee09b2ffad16a1acd01c03ac92a7f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924299"
---
# <a name="design-details"></a><span data-ttu-id="40d36-103">Designoplysninger</span><span class="sxs-lookup"><span data-stu-id="40d36-103">Design Details</span></span>
<span data-ttu-id="40d36-104">Dette indhold indeholder detaljerede tekniske oplysninger om komplekse programfunktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="40d36-104">This content contains detailed technical information about complex application features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

 <span data-ttu-id="40d36-105">Indholdet af designoplysningerne er rettet mod iværksættere, udviklere og superbrugere, der har brug for en dybere indsigt i at implementere, tilpasse eller opsætte de pågældende funktioner.</span><span class="sxs-lookup"><span data-stu-id="40d36-105">Design details content is aimed at implementers, developers, and super users who need deeper insight to implement, customize, or set up the features in question.</span></span>  

|<span data-ttu-id="40d36-106">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="40d36-106">**To**</span></span>|<span data-ttu-id="40d36-107">**Se**</span><span class="sxs-lookup"><span data-stu-id="40d36-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="40d36-108">Lær, hvordan planlægningssystemet fungerer, og hvordan du justerer algoritmer for at opfylde planlægningsbehov i forskellige miljøer.</span><span class="sxs-lookup"><span data-stu-id="40d36-108">Learn how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="40d36-109">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="40d36-109">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|  
|<span data-ttu-id="40d36-110">Forstå mekanismerne i prisberegningsprogrammet, f.eks. kostmetode og kostregulering, samt hvilke regnskabsprincipper, de er designet til.</span><span class="sxs-lookup"><span data-stu-id="40d36-110">Understand mechanisms in the costing engine, such as costing method and cost adjustment, and which accounting principles they are designed for.</span></span>|[<span data-ttu-id="40d36-111">Designoplysninger: Lagerkostmetode</span><span class="sxs-lookup"><span data-stu-id="40d36-111">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  
|<span data-ttu-id="40d36-112">Lær om de centrale principper bag avancerede og grundlæggende lagerfunktioner, og hvordan de integreres med andre forsyningskædefunktioner.</span><span class="sxs-lookup"><span data-stu-id="40d36-112">Learn about central principles behind advanced and basic warehouse features and how they integrate with other supply chain features.</span></span>|[<span data-ttu-id="40d36-113">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="40d36-113">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)|  
|<span data-ttu-id="40d36-114">Få mere at vide om historisk og aktuelt design af varesporingsfunktionalitet, og hvordan den integreres med reservationssystemet for at medtage serienumre/lotnumre i disponeringsberegninger.</span><span class="sxs-lookup"><span data-stu-id="40d36-114">Learn about historic and the current design of item tracking functionality and how it integrates with the reservation system to include serial/lot numbers in availability calculations.</span></span>|[<span data-ttu-id="40d36-115">Designoplysninger: Varesporing</span><span class="sxs-lookup"><span data-stu-id="40d36-115">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)|  
|<span data-ttu-id="40d36-116">Få mere at vide om funktionen for bogføringslinjer til finanskladder, herunder de seneste forenklinger til design af codeunit 12.</span><span class="sxs-lookup"><span data-stu-id="40d36-116">Learn about the General Journal Posting Line feature, including recent simplifications to the design of codeunit 12.</span></span>|[<span data-ttu-id="40d36-117">Designoplysninger: Bogføringslinje i finanskladde</span><span class="sxs-lookup"><span data-stu-id="40d36-117">Design Details: General Journal Post Line</span></span>](design-details-general-journal-post-line.md)|
|<span data-ttu-id="40d36-118">Få mere at vide om designet til lagrings- og bogføringsdimensioner, herunder kodeeksempler på at overflytte og opgradere dimensionskode.</span><span class="sxs-lookup"><span data-stu-id="40d36-118">Learn about the design for storing and posting dimensions, including code examples on how to migrate and upgrade dimension code.</span></span>|[<span data-ttu-id="40d36-119">Designoplysninger: Dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="40d36-119">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)| 

## <a name="see-also"></a><span data-ttu-id="40d36-120">Se også</span><span class="sxs-lookup"><span data-stu-id="40d36-120">See Also</span></span>  
 <span data-ttu-id="40d36-121">[Planlægning](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="40d36-121">[Planning](production-planning.md) </span></span>  
 <span data-ttu-id="40d36-122">[Administrere lageromkostninger](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="40d36-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="40d36-123">[Logistik](warehouse-manage-warehouse.md) </span><span class="sxs-lookup"><span data-stu-id="40d36-123">[Warehouse Management](warehouse-manage-warehouse.md) </span></span>  
 [<span data-ttu-id="40d36-124">Konfigurere komplekse moduler ved hjælp af bedste praksis</span><span class="sxs-lookup"><span data-stu-id="40d36-124">Setting Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="40d36-125">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="40d36-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

 ## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
