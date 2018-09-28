---
title: "Designoplysninger – Bogføringslinje i finanskladde | Microsoft Docs"
description: "Dette emne giver indsigt i de begreber og principper, der bruges til at omdesigne funktionen til finanskladders bogføringslinjer i Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 24df541a8f1d1cf5df3f53a00922ae0d88d7192f
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="71b56-103">Designoplysninger: Bogføringslinje i finanskladde</span><span class="sxs-lookup"><span data-stu-id="71b56-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="71b56-104">Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges til at omdesigne funktionen til finanskladders bogføringslinjer i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="71b56-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="71b56-105">Ombygningen gør codeunit 12 enklere og nemmere at vedligeholde.</span><span class="sxs-lookup"><span data-stu-id="71b56-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="71b56-106">Dokumentationen starter med at beskrive en grundlæggende oversigt over det nye design.</span><span class="sxs-lookup"><span data-stu-id="71b56-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="71b56-107">Derefter beskrives den tekniske arkitektur for at vise de ændringer, der stammer fra ombygningen.</span><span class="sxs-lookup"><span data-stu-id="71b56-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="71b56-108">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="71b56-108">In This Section</span></span>  
[<span data-ttu-id="71b56-109">Oversigt over bogføringslinje i finanskladde</span><span class="sxs-lookup"><span data-stu-id="71b56-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="71b56-110">Designoplysninger: Bogføring af grænsefladestruktur</span><span class="sxs-lookup"><span data-stu-id="71b56-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="71b56-111">Designoplysninger: Bogføringsprogramstruktur</span><span class="sxs-lookup"><span data-stu-id="71b56-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="71b56-112">Ændringer i Codeunit 12: Kobling af globale variabler for bogføringslinje i finanskladde</span><span class="sxs-lookup"><span data-stu-id="71b56-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="71b56-113">Codeunit 12-ændringer: Ændringer i procedurer for bogføring af finanskladder</span><span class="sxs-lookup"><span data-stu-id="71b56-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="71b56-114">Se også</span><span class="sxs-lookup"><span data-stu-id="71b56-114">See Also</span></span>  
[<span data-ttu-id="71b56-115">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="71b56-115">Working with General Journals</span></span>](ui-work-general-journals.md)

