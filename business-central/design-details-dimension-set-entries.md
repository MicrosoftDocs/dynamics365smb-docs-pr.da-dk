---
title: Designoplysninger – Dimensionsgruppeposter | Microsoft Docs
description: Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges til at omdesigne funktionen til dimensionspostlagring og -bogføring.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c6b66ecee87e1fd128733f541d46b97f44af0453
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242740"
---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="0480f-103">Designoplysninger: Dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="0480f-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="0480f-104">Denne dokumentation indeholder detaljeret teknisk indsigt i begreber og principper i funktionaliteten i dimensionspostlagring og -bogføring i [!INCLUDE[d365fin](includes/d365fin_md.md)] .</span><span class="sxs-lookup"><span data-stu-id="0480f-104">This documentation provides detailed technical insight into the concepts and principles of the dimension-entry storing and posting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0480f-105">Dokumentationen starter med at beskrive en grundlæggende oversigt.</span><span class="sxs-lookup"><span data-stu-id="0480f-105">The documentation starts by describing conceptual overviews.</span></span> <span data-ttu-id="0480f-106">Derefter følger en forklaring af den tekniske arkitektur.</span><span class="sxs-lookup"><span data-stu-id="0480f-106">Then it explains the technical architecture.</span></span> <span data-ttu-id="0480f-107">Endelig indeholder den kodeeksempler til at forberede dig på dimensionskodeoverflytning og -opgradering fra versioner, der er tidligere end Dynamics NAV 2013R2.</span><span class="sxs-lookup"><span data-stu-id="0480f-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade from versions earlier than Dynamics NAV 2013R2.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="0480f-108">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="0480f-108">In This Section</span></span>  
[<span data-ttu-id="0480f-109">Oversigt over dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="0480f-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="0480f-110">Designoplysninger: Søgning efter dimensionskombinationer</span><span class="sxs-lookup"><span data-stu-id="0480f-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="0480f-111">Designoplysninger: Tabelstruktur</span><span class="sxs-lookup"><span data-stu-id="0480f-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="0480f-112">Designoplysninger: Kodeenhed 408 Dimensionsstyring</span><span class="sxs-lookup"><span data-stu-id="0480f-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="0480f-113">Designoplysninger: Kodeeksempler af ændrede mønstre i Ændringer</span><span class="sxs-lookup"><span data-stu-id="0480f-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
