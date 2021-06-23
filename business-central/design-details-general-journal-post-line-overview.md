---
title: Oversigt over bogføringslinje i finanskladde | Microsoft Docs
description: Dette emne introducerer ændringer af Codeunit 12, **Finanskladde-Bogføringslinje**, der er det vigtigste udligningsobjekt til finansbogføring, og er det eneste sted at indsætte finans-, moms- og debitor- og kreditorposter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1f6060eb7672b332fb570eb13fe027a3b58e6594
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215249"
---
# <a name="general-journal-post-line-overview"></a><span data-ttu-id="ade82-103">Oversigt over bogføringslinje i finanskladde</span><span class="sxs-lookup"><span data-stu-id="ade82-103">General Journal Post Line Overview</span></span>

<span data-ttu-id="ade82-104">Codeunit 12 **Finanskladde-Bogføringslinje** er det vigtigste udligningsobjekt til finansbogføring og er det eneste sted at indsætte finans-, moms- og debitor-og kreditorposter.</span><span class="sxs-lookup"><span data-stu-id="ade82-104">Codeunit 12, **Gen. Jnl.-Post Line**, is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.</span></span> <span data-ttu-id="ade82-105">Denne codeunit bruges også til alle handlinger med Udlign, Annuller udligning og Tilbagefør.</span><span class="sxs-lookup"><span data-stu-id="ade82-105">This codeunit is also used for all Apply, Unapply and Reverse operations.</span></span>  
  
<span data-ttu-id="ade82-106">I Microsoft Dynamics NAV 2013 R2 blev codeunit omdesignet, fordi den er blevet meget stor med ca. 7.600-kodelinjer.</span><span class="sxs-lookup"><span data-stu-id="ade82-106">In Microsoft Dynamics NAV 2013 R2, the codeunit was redesigned because it had become very large, with approximately 7,600 code lines.</span></span> <span data-ttu-id="ade82-107">Med denne version af er arkitekturen ændret, og codeunit er gjort enklere og nemmere at vedligeholde.</span><span class="sxs-lookup"><span data-stu-id="ade82-107">The architecture was changed and the codeunit has been made simpler and more maintainable.</span></span> <span data-ttu-id="ade82-108">Denne dokumentation beskriver ændringerne og oplysninger, du skal bruge til opgradering.</span><span class="sxs-lookup"><span data-stu-id="ade82-108">This documentation describes the changes and provides information that you will need for upgrade.</span></span>  
  
## <a name="old-architecture"></a><span data-ttu-id="ade82-109">Gammel arkitektur</span><span class="sxs-lookup"><span data-stu-id="ade82-109">Old Architecture</span></span>  
<span data-ttu-id="ade82-110">Den gamle arkitektur havde følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="ade82-110">The old architecture had the following features:</span></span>  
  
* <span data-ttu-id="ade82-111">Der var omfattende brug af globale variabler, som øgede risikoen for skjulte fejl pga. brug af variabler med det forkerte område.</span><span class="sxs-lookup"><span data-stu-id="ade82-111">There was extensive use of global variables, which increased the possibility of hidden errors due to use of variables with the wrong scope.</span></span>  
* <span data-ttu-id="ade82-112">Der var mange lange procedurer (med mere end 100 kodelinjer), der også havde høj cyklomatisk kompleksitet (dvs. en masse indlejrede CASE, REPEAT, IF-sætninger), der gjorde det meget vanskeligt at læse og vedligeholde koden.</span><span class="sxs-lookup"><span data-stu-id="ade82-112">There were many long procedures (with more than 100 code lines) that also had high cyclomatic complexity (that is, a lot of CASE, REPEAT, IF nested statements), which made the code very difficult to read and maintain.</span></span>  
* <span data-ttu-id="ade82-113">Flere procedurer, der kun blev anvendt lokalt og kun var beregnet til anvendelse lokalt, blev ikke markeret som lokale.</span><span class="sxs-lookup"><span data-stu-id="ade82-113">Several procedures that were only used locally and were only meant to be used locally were not marked as local.</span></span>  
* <span data-ttu-id="ade82-114">De fleste procedurer havde ingen parametre og brugte globale variabler.</span><span class="sxs-lookup"><span data-stu-id="ade82-114">Most procedures had no parameters and used global variables.</span></span> <span data-ttu-id="ade82-115">Nogle brugte parametre og tilsidesatte globale variabler med lokale.</span><span class="sxs-lookup"><span data-stu-id="ade82-115">Some used parameters and overrode global variables with locals.</span></span>  
* <span data-ttu-id="ade82-116">Kodemønstre til søgning i finanskonti og oprettelse af finans- og momsposter var ikke standardiseret og varierede fra område til område.</span><span class="sxs-lookup"><span data-stu-id="ade82-116">Code patterns for searching the general ledger accounts and creating general ledger and VAT entries was not standardized and varied from place to place.</span></span> <span data-ttu-id="ade82-117">Der var desuden en masse kodeduplikering og brudt symmetri mellem debitor- og kreditorkode.</span><span class="sxs-lookup"><span data-stu-id="ade82-117">In addition, there was a lot of code duplication and broken symmetry between customer and vendor code.</span></span>  
* <span data-ttu-id="ade82-118">En stor del af koden i codeunit 12, ca. 30 procent, der vedrører kontantrabat og toleranceberegninger, selvom disse funktioner ikke er nødvendige i mange lande eller områder.</span><span class="sxs-lookup"><span data-stu-id="ade82-118">A large part of the code in codeunit 12, approximately 30 percent, related to payment discount and tolerance calculations, although these features are not needed in many countries or regions.</span></span>  
* <span data-ttu-id="ade82-119">Bogføring, Udlign, Annuller udligning, Tilbagefør, Kontantrabat og Tolerance samt Valutakursregulering blev samlet i codeunit 12 ved hjælp af en lang liste af globale variabler.</span><span class="sxs-lookup"><span data-stu-id="ade82-119">Posting, Apply, Unapply, Reverse, Payment Discount and Tolerance, and Exchange Rate Adjustment were married together in codeunit 12 using a long list of global variables.</span></span>  
  
### <a name="new-architecture"></a><span data-ttu-id="ade82-120">Ny arkitektur</span><span class="sxs-lookup"><span data-stu-id="ade82-120">New Architecture</span></span>  
<span data-ttu-id="ade82-121">I [!INCLUDE[prod_short](includes/prod_short.md)] har codeunit 12 følgende forbedringer:</span><span class="sxs-lookup"><span data-stu-id="ade82-121">In [!INCLUDE[prod_short](includes/prod_short.md)], codeunit 12 has had the following improvements:</span></span>  
  
* <span data-ttu-id="ade82-122">Codeunit 12 er blevet inddelt i mindre procedurer (alle under 100 kodelinjer).</span><span class="sxs-lookup"><span data-stu-id="ade82-122">Codeunit 12 has been refactored into smaller procedures (all less than 100 code lines).</span></span>  
* <span data-ttu-id="ade82-123">Standardiserede mønstre for søgning på finanskonti er implementeret ved hjælp af hjælpefunktioner fra bogføringsgruppetabeller.</span><span class="sxs-lookup"><span data-stu-id="ade82-123">Standardized patterns for the search of general ledger accounts have been implemented by using helper functions from Posting Group tables.</span></span>  
* <span data-ttu-id="ade82-124">En bogføringsstruktur er blevet implementeret for at administrere start og afslutning af transaktioner og isolere oprettelsen til finans- og momsposter, indsamling af momsregulering og beregning af beløb i ekstra valuta.</span><span class="sxs-lookup"><span data-stu-id="ade82-124">A Posting Engine Framework has been implemented to manage the start and finish of transactions and to isolate the creation to general ledger and VAT entries, the collection of VAT adjustment, and the calculation of additional currency amounts.</span></span>  
* <span data-ttu-id="ade82-125">Kopiering af koden er elimineret.</span><span class="sxs-lookup"><span data-stu-id="ade82-125">Code duplication has been eliminated.</span></span>  
* <span data-ttu-id="ade82-126">Mange hjælpefunktioner, der er overført til tilsvarende debitor- og kreditorposttabeller.</span><span class="sxs-lookup"><span data-stu-id="ade82-126">Many helper functions have been transferred to corresponding customer and vendor ledger entry tables.</span></span>  
* <span data-ttu-id="ade82-127">Brug af globale variabler er blevet minimeret, så hver enkelt procedure bruger parametre og indkapsler sin egen programlogik.</span><span class="sxs-lookup"><span data-stu-id="ade82-127">The use of global variables has been minimized, so that each procedure uses parameters and encapsulates its own application logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ade82-128">Se også</span><span class="sxs-lookup"><span data-stu-id="ade82-128">See Also</span></span>

[<span data-ttu-id="ade82-129">Designoplysninger: Bogføring af grænsefladestruktur</span><span class="sxs-lookup"><span data-stu-id="ade82-129">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="ade82-130">Designoplysninger: Bogføringsprogramstruktur</span><span class="sxs-lookup"><span data-stu-id="ade82-130">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="ade82-131">Designoplysninger: Bogføringslinje i finanskladde (Dynamics NAV)</span><span class="sxs-lookup"><span data-stu-id="ade82-131">Design Details: General Journal Post Line (Dynamics NAV)</span></span>](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]