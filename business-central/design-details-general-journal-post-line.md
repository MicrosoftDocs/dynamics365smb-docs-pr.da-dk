---
title: Designoplysninger – Bogføringslinje i finanskladde | Microsoft Docs
description: Dette emne giver indsigt i de begreber og principper, der bruges til at omdesigne funktionen til finanskladders bogføringslinjer i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8492c83437be4cd850bafdaaa5dc70d00a075674
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215224"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="41c1a-103">Designoplysninger: Bogføringslinje i finanskladde</span><span class="sxs-lookup"><span data-stu-id="41c1a-103">Design Details: General Journal Post Line</span></span>

<span data-ttu-id="41c1a-104">Denne dokumentation indeholder detaljeret teknisk indsigt i de begreber og principper, der bruges til at omdesigne funktionen til finanskladders bogføringslinjer i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="41c1a-104">This documentation provides detailed technical insight into the concepts and principles that were used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="41c1a-105">Ombygningen gør codeunit 12 enklere og nemmere at vedligeholde.</span><span class="sxs-lookup"><span data-stu-id="41c1a-105">The redesign made codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="41c1a-106">Dokumentationen starter med at beskrive en grundlæggende oversigt over det nye design.</span><span class="sxs-lookup"><span data-stu-id="41c1a-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="41c1a-107">Derefter beskrives den tekniske arkitektur for at vise de ændringer, der stammer fra ombygningen.</span><span class="sxs-lookup"><span data-stu-id="41c1a-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="41c1a-108">Oplysningerne i dette afsnit gælder for re-konstruktionen i en tidligere version af produktet Microsoft Dynamics NAV 2013 R2.</span><span class="sxs-lookup"><span data-stu-id="41c1a-108">The information in this section applies to the redesign in an earlier version of the product, Microsoft Dynamics NAV 2013 R2.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="41c1a-109">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="41c1a-109">In This Section</span></span>

[<span data-ttu-id="41c1a-110">Oversigt over bogføringslinje i finanskladde</span><span class="sxs-lookup"><span data-stu-id="41c1a-110">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="41c1a-111">Designoplysninger: Bogføring af grænsefladestruktur</span><span class="sxs-lookup"><span data-stu-id="41c1a-111">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="41c1a-112">Designoplysninger: Bogføringsprogramstruktur</span><span class="sxs-lookup"><span data-stu-id="41c1a-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  

## <a name="see-also"></a><span data-ttu-id="41c1a-113">Se også</span><span class="sxs-lookup"><span data-stu-id="41c1a-113">See Also</span></span>

<span data-ttu-id="41c1a-114">[Arbejde med generelle kladde](ui-work-general-journals.md)
[Designoplysninger: Finans postlinje (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span><span class="sxs-lookup"><span data-stu-id="41c1a-114">[Working with General Journals](ui-work-general-journals.md)
[Design Details: General Journal Post Line (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]