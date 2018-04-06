---
title: "Designoplysninger – Dimensionsgruppeposter | Microsoft Docs"
description: "Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges til at omdesigne funktionen til dimensionspostlagring og -bogføring."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 66de44003ac66bad52a7b7e57d582659047bdbdf
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="7e5ee-103">Designoplysninger: Dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="7e5ee-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="7e5ee-104">Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges til at omdesigne funktionen til dimensionspostlagring og -bogføring i [!INCLUDE[d365fin](includes/d365fin_md.md)] .</span><span class="sxs-lookup"><span data-stu-id="7e5ee-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the dimension entry storing and posting feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7e5ee-105">Dokumentationen starter med at beskrive en grundlæggende oversigt over det nye design.</span><span class="sxs-lookup"><span data-stu-id="7e5ee-105">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="7e5ee-106">Derefter beskrives den tekniske arkitektur for at vise, hvordan ændringerne er foretaget.</span><span class="sxs-lookup"><span data-stu-id="7e5ee-106">Then it explains the technical architecture to show how the redesign is made.</span></span> <span data-ttu-id="7e5ee-107">Endelig indeholder den kodeeksempler til at forberede dig på dimensionskodeoverflytning og -opgradering.</span><span class="sxs-lookup"><span data-stu-id="7e5ee-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="7e5ee-108">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="7e5ee-108">In This Section</span></span>  
[<span data-ttu-id="7e5ee-109">Oversigt over dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="7e5ee-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="7e5ee-110">Designoplysninger: Søgning efter dimensionskombinationer</span><span class="sxs-lookup"><span data-stu-id="7e5ee-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="7e5ee-111">Designoplysninger: Tabelstruktur</span><span class="sxs-lookup"><span data-stu-id="7e5ee-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="7e5ee-112">Designoplysninger: Kodeenhed 408 Dimensionsstyring</span><span class="sxs-lookup"><span data-stu-id="7e5ee-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="7e5ee-113">Designoplysninger: Kodeeksempler af ændrede mønstre i Ændringer</span><span class="sxs-lookup"><span data-stu-id="7e5ee-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

