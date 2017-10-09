---
title: "Designoplysninger – Bogføringslinje i finanskladde | Microsoft Docs"
description: "Dette emne indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges til at omdesigne funktionen til finanskladders bogføringslinjer i [!INCLUDE[d365fin](includes/d365fin_md.md)]."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a161a74018ce1b7b975bdacb9542a8b0ac9f37df
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="c1a9a-103">Designoplysninger: Bogføringslinje i finanskladde</span><span class="sxs-lookup"><span data-stu-id="c1a9a-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="c1a9a-104">Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges til at omdesigne funktionen til finanskladders bogføringslinjer i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c1a9a-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c1a9a-105">Ombygningen gør codeunit 12 enklere og nemmere at vedligeholde.</span><span class="sxs-lookup"><span data-stu-id="c1a9a-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="c1a9a-106">Dokumentationen starter med at beskrive en grundlæggende oversigt over det nye design.</span><span class="sxs-lookup"><span data-stu-id="c1a9a-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="c1a9a-107">Derefter beskrives den tekniske arkitektur for at vise de ændringer, der stammer fra ombygningen.</span><span class="sxs-lookup"><span data-stu-id="c1a9a-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="c1a9a-108">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="c1a9a-108">In This Section</span></span>  
[<span data-ttu-id="c1a9a-109">Oversigt over bogføringslinje i finanskladde</span><span class="sxs-lookup"><span data-stu-id="c1a9a-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="c1a9a-110">Designoplysninger: Bogføring af grænsefladestruktur</span><span class="sxs-lookup"><span data-stu-id="c1a9a-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="c1a9a-111">Designoplysninger: Bogføringsprogramstruktur</span><span class="sxs-lookup"><span data-stu-id="c1a9a-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="c1a9a-112">Ændringer i Codeunit 12: Kobling af globale variabler for bogføringslinje i finanskladde</span><span class="sxs-lookup"><span data-stu-id="c1a9a-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="c1a9a-113">Codeunit 12-ændringer: Ændringer i procedurer for bogføring af finanskladder</span><span class="sxs-lookup"><span data-stu-id="c1a9a-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="c1a9a-114">Se også</span><span class="sxs-lookup"><span data-stu-id="c1a9a-114">See Also</span></span>  
[<span data-ttu-id="c1a9a-115">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="c1a9a-115">Working with General Journals</span></span>](ui-work-general-journals.md)

