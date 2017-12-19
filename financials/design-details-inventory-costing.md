---
title: "Designoplysninger – Lagerkostmetode | Microsoft Docs"
description: Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges inden for lageromkostningsfunktionerne i Dynamics 365.
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
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: ef098c17ab54d45eec380548f70042a436c95128
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="d49db-103">Designoplysninger: Lagerkostmetode</span><span class="sxs-lookup"><span data-stu-id="d49db-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="d49db-104">Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges inden for lageromkostningsfunktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d49db-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="d49db-105">Lagerkostmetode, også kendt som "omkostningsstyring", vedrører registrering og rapportering af virksomhedens driftsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="d49db-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="d49db-106">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="d49db-106">In This Section</span></span>  
[<span data-ttu-id="d49db-107">Designoplysninger: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="d49db-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="d49db-108">Designoplysninger: Vareudligning</span><span class="sxs-lookup"><span data-stu-id="d49db-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="d49db-109">Designoplysninger: Kostregulering</span><span class="sxs-lookup"><span data-stu-id="d49db-109">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="d49db-110">Designoplysninger: Bogføring af forventet kostpris</span><span class="sxs-lookup"><span data-stu-id="d49db-110">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="d49db-111">Designoplysninger: Gennemsnitlig kostpris</span><span class="sxs-lookup"><span data-stu-id="d49db-111">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="d49db-112">Designoplysninger: Afvigelse</span><span class="sxs-lookup"><span data-stu-id="d49db-112">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="d49db-113">Designoplysninger: Afrunding</span><span class="sxs-lookup"><span data-stu-id="d49db-113">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="d49db-114">Designoplysninger: Omkosntingskomponenter</span><span class="sxs-lookup"><span data-stu-id="d49db-114">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="d49db-115">Designoplysninger: Lagerperioder</span><span class="sxs-lookup"><span data-stu-id="d49db-115">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="d49db-116">Designoplysninger: Varekladde</span><span class="sxs-lookup"><span data-stu-id="d49db-116">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="d49db-117">Designoplysninger: Bogføring af produktionsordre</span><span class="sxs-lookup"><span data-stu-id="d49db-117">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="d49db-118">Designoplysninger: Bogføring af montageordre</span><span class="sxs-lookup"><span data-stu-id="d49db-118">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="d49db-119">Designoplysninger: Afstemning med Finans</span><span class="sxs-lookup"><span data-stu-id="d49db-119">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="d49db-120">Designoplysninger: Konti i Finans</span><span class="sxs-lookup"><span data-stu-id="d49db-120">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="d49db-121">Designoplysninger: Regulering</span><span class="sxs-lookup"><span data-stu-id="d49db-121">Design Details: Revaluation</span></span>](design-details-revaluation.md)

