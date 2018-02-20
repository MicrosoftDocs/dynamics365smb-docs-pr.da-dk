---
title: "Designoplysninger – Lagerkostmetode | Microsoft Docs"
description: Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges inden for lageromkostningsfunktionerne i Finance and Operations, Business edition.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4f14118e435051c6d63f95a05ebee2e7107ce054
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="ca852-103">Designoplysninger: Lagerkostmetode</span><span class="sxs-lookup"><span data-stu-id="ca852-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="ca852-104">Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges inden for lageromkostningsfunktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ca852-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="ca852-105">Lagerkostmetode, også kendt som "omkostningsstyring", vedrører registrering og rapportering af virksomhedens driftsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="ca852-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="ca852-106">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="ca852-106">In This Section</span></span>  
[<span data-ttu-id="ca852-107">Designoplysninger: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="ca852-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="ca852-108">Designoplysninger: Vareudligning</span><span class="sxs-lookup"><span data-stu-id="ca852-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="ca852-109">Designoplysninger: Kostregulering</span><span class="sxs-lookup"><span data-stu-id="ca852-109">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="ca852-110">Designoplysninger: Bogføring af forventet kostpris</span><span class="sxs-lookup"><span data-stu-id="ca852-110">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="ca852-111">Designoplysninger: Gennemsnitlig kostpris</span><span class="sxs-lookup"><span data-stu-id="ca852-111">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="ca852-112">Designoplysninger: Afvigelse</span><span class="sxs-lookup"><span data-stu-id="ca852-112">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="ca852-113">Designoplysninger: Afrunding</span><span class="sxs-lookup"><span data-stu-id="ca852-113">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="ca852-114">Designoplysninger: Omkosntingskomponenter</span><span class="sxs-lookup"><span data-stu-id="ca852-114">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="ca852-115">Designoplysninger: Lagerperioder</span><span class="sxs-lookup"><span data-stu-id="ca852-115">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="ca852-116">Designoplysninger: Varekladde</span><span class="sxs-lookup"><span data-stu-id="ca852-116">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="ca852-117">Designoplysninger: Bogføring af produktionsordre</span><span class="sxs-lookup"><span data-stu-id="ca852-117">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="ca852-118">Designoplysninger: Bogføring af montageordre</span><span class="sxs-lookup"><span data-stu-id="ca852-118">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="ca852-119">Designoplysninger: Afstemning med Finans</span><span class="sxs-lookup"><span data-stu-id="ca852-119">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="ca852-120">Designoplysninger: Konti i Finans</span><span class="sxs-lookup"><span data-stu-id="ca852-120">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="ca852-121">Designoplysninger: Regulering</span><span class="sxs-lookup"><span data-stu-id="ca852-121">Design Details: Revaluation</span></span>](design-details-revaluation.md)

