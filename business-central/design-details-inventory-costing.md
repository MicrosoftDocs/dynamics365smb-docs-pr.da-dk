---
title: Designoplysninger – Lagerkostmetode | Microsoft Docs
description: Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges inden for lageromkostningsfunktionerne i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8bfcf2b10d9b302c9a65b7cf27c7fb336be68617
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215974"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="9a1d9-103">Designoplysninger: Lagerkostmetode</span><span class="sxs-lookup"><span data-stu-id="9a1d9-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="9a1d9-104">Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges inden for lageromkostningsfunktionerne i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9a1d9-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="9a1d9-105">Lagerkostmetode, også kendt som "omkostningsstyring", vedrører registrering og rapportering af virksomhedens driftsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="9a1d9-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="9a1d9-106">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="9a1d9-106">In This Section</span></span>  
[<span data-ttu-id="9a1d9-107">Designoplysninger: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="9a1d9-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="9a1d9-108">Designoplysninger: Vareudligning</span><span class="sxs-lookup"><span data-stu-id="9a1d9-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="9a1d9-109">Designoplysninger: Kendt problem med vareudligning</span><span class="sxs-lookup"><span data-stu-id="9a1d9-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="9a1d9-110">Designoplysninger: Omkostningsregulering</span><span class="sxs-lookup"><span data-stu-id="9a1d9-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="9a1d9-111">Designoplysninger: Bogføringsdato på post med reguleringsværdi</span><span class="sxs-lookup"><span data-stu-id="9a1d9-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="9a1d9-112">Designoplysninger: Bogføring af forventet kostpris</span><span class="sxs-lookup"><span data-stu-id="9a1d9-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="9a1d9-113">Designoplysninger: Gennemsnitlig kostpris</span><span class="sxs-lookup"><span data-stu-id="9a1d9-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="9a1d9-114">Designoplysninger: Afvigelse</span><span class="sxs-lookup"><span data-stu-id="9a1d9-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="9a1d9-115">Designoplysninger: Afrunding</span><span class="sxs-lookup"><span data-stu-id="9a1d9-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="9a1d9-116">Designoplysninger: Omkosntingskomponenter</span><span class="sxs-lookup"><span data-stu-id="9a1d9-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="9a1d9-117">Designoplysninger: Lagerperioder</span><span class="sxs-lookup"><span data-stu-id="9a1d9-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="9a1d9-118">Designoplysninger: Varekladde</span><span class="sxs-lookup"><span data-stu-id="9a1d9-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="9a1d9-119">Designoplysninger: Bogføring af produktionsordre</span><span class="sxs-lookup"><span data-stu-id="9a1d9-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="9a1d9-120">Designoplysninger: Bogføring af montageordre</span><span class="sxs-lookup"><span data-stu-id="9a1d9-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="9a1d9-121">Designoplysninger: Afstemning med Finans</span><span class="sxs-lookup"><span data-stu-id="9a1d9-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="9a1d9-122">Designoplysninger: Konti i Finans</span><span class="sxs-lookup"><span data-stu-id="9a1d9-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="9a1d9-123">Designoplysninger: Lagerværdi</span><span class="sxs-lookup"><span data-stu-id="9a1d9-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="9a1d9-124">Designoplysninger: Regulering</span><span class="sxs-lookup"><span data-stu-id="9a1d9-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]