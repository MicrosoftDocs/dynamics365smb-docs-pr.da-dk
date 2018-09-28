---
title: "Oversigt over bogføringslinje i finanskladde | Microsoft Docs"
description: "Dette emne introducerer ændringer af Codeunit 12, **Finanskladde-Bogføringslinje**, der er det vigtigste udligningsobjekt til finansbogføring, og er det eneste sted at indsætte finans-, moms- og debitor- og kreditorposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: db90633823f12650f796735a9a83bec8edb60cb9
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="general-journal-post-line-overview"></a><span data-ttu-id="434cc-103">Oversigt over bogføringslinje i finanskladde</span><span class="sxs-lookup"><span data-stu-id="434cc-103">General Journal Post Line Overview</span></span>
<span data-ttu-id="434cc-104">Codeunit 12 **Finanskladde-Bogføringslinje** er det vigtigste udligningsobjekt til finansbogføring og er det eneste sted at indsætte finans-, moms- og debitor-og kreditorposter.</span><span class="sxs-lookup"><span data-stu-id="434cc-104">Codeunit 12, **Gen. Jnl.-Post Line**, is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.</span></span> <span data-ttu-id="434cc-105">Denne codeunit bruges også til alle handlinger med Udlign, Annuller udligning og Tilbagefør.</span><span class="sxs-lookup"><span data-stu-id="434cc-105">This codeunit is also used for all Apply, Unapply and Reverse operations.</span></span>  
  
<span data-ttu-id="434cc-106">Mens codeunit er blevet forbedret i hver udgave i de sidste ti år, er dens arkitektur i det væsentlige uændret.</span><span class="sxs-lookup"><span data-stu-id="434cc-106">While the codeunit has been improved in each release over the last ten years, its architecture remained essentially unchanged.</span></span> <span data-ttu-id="434cc-107">Codeunit blev meget stor med ca. 7.600 kodelinjer.</span><span class="sxs-lookup"><span data-stu-id="434cc-107">The codeunit became very large, with approximately 7,600 code lines.</span></span> <span data-ttu-id="434cc-108">Med denne version af [!INCLUDE[d365fin](includes/d365fin_md.md)] er arkitekturen ændret, og codeunit er gjort enklere og nemmere at vedligeholde.</span><span class="sxs-lookup"><span data-stu-id="434cc-108">With this release of [!INCLUDE[d365fin](includes/d365fin_md.md)], the architecture is changed and the codeunit has been made simpler and more maintainable.</span></span> <span data-ttu-id="434cc-109">Denne dokumentation indeholder ændringerne og oplysninger, du skal bruge til opgradering.</span><span class="sxs-lookup"><span data-stu-id="434cc-109">This documentation introduces the changes and provides information that you will need for upgrade.</span></span>  
  
## <a name="old-architecture"></a><span data-ttu-id="434cc-110">Gammel arkitektur</span><span class="sxs-lookup"><span data-stu-id="434cc-110">Old Architecture</span></span>  
<span data-ttu-id="434cc-111">Den gamle arkitektur havde følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="434cc-111">The old architecture had the following features:</span></span>  
  
* <span data-ttu-id="434cc-112">Der var omfattende brug af globale variabler, som øgede risikoen for skjulte fejl pga. brug af variabler med det forkerte område.</span><span class="sxs-lookup"><span data-stu-id="434cc-112">There was extensive use of global variables, which increased the possibility of hidden errors due to use of variables with the wrong scope.</span></span>  
* <span data-ttu-id="434cc-113">Der var mange lange procedurer (med mere end 100 kodelinjer), der også havde høj cyklomatisk kompleksitet (dvs. en masse indlejrede CASE, REPEAT, IF-sætninger), der gjorde det meget vanskeligt at læse og vedligeholde koden.</span><span class="sxs-lookup"><span data-stu-id="434cc-113">There were many long procedures (with more than 100 code lines) that also had high cyclomatic complexity (that is, a lot of CASE, REPEAT, IF nested statements), which made the code very difficult to read and maintain.</span></span>  
* <span data-ttu-id="434cc-114">Flere procedurer, der kun blev anvendt lokalt og kun var beregnet til anvendelse lokalt, blev ikke markeret som lokale.</span><span class="sxs-lookup"><span data-stu-id="434cc-114">Several procedures that were only used locally and were only meant to be used locally were not marked as local.</span></span>  
* <span data-ttu-id="434cc-115">De fleste procedurer havde ingen parametre og brugte globale variabler.</span><span class="sxs-lookup"><span data-stu-id="434cc-115">Most procedures had no parameters and used global variables.</span></span> <span data-ttu-id="434cc-116">Nogle brugte parametre og tilsidesatte globale variabler med lokale.</span><span class="sxs-lookup"><span data-stu-id="434cc-116">Some used parameters and overrode global variables with locals.</span></span>  
* <span data-ttu-id="434cc-117">Kodemønstre til søgning i finanskonti og oprettelse af finans- og momsposter var ikke standardiseret og varierede fra område til område.</span><span class="sxs-lookup"><span data-stu-id="434cc-117">Code patterns for searching the general ledger accounts and creating general ledger and VAT entries was not standardized and varied from place to place.</span></span> <span data-ttu-id="434cc-118">Der var desuden en masse kodeduplikering og brudt symmetri mellem debitor- og kreditorkode.</span><span class="sxs-lookup"><span data-stu-id="434cc-118">In addition, there was a lot of code duplication and broken symmetry between customer and vendor code.</span></span>  
* <span data-ttu-id="434cc-119">En stor del af koden i codeunit 12, ca. 30 procent, der vedrører kontantrabat og toleranceberegninger, selvom disse funktioner ikke er nødvendige i mange lande eller områder.</span><span class="sxs-lookup"><span data-stu-id="434cc-119">A large part of the code in codeunit 12, approximately 30 percent, related to payment discount and tolerance calculations, although these features are not needed in many countries or regions.</span></span>  
* <span data-ttu-id="434cc-120">Bogføring, Udlign, Annuller udligning, Tilbagefør, Kontantrabat og Tolerance samt Valutakursregulering blev samlet i codeunit 12 ved hjælp af en lang liste af globale variabler.</span><span class="sxs-lookup"><span data-stu-id="434cc-120">Posting, Apply, Unapply, Reverse, Payment Discount and Tolerance, and Exchange Rate Adjustment were married together in codeunit 12 using a long list of global variables.</span></span>  
  
### <a name="new-architecture"></a><span data-ttu-id="434cc-121">Ny arkitektur</span><span class="sxs-lookup"><span data-stu-id="434cc-121">New Architecture</span></span>  
<span data-ttu-id="434cc-122">I [!INCLUDE[d365fin](includes/d365fin_md.md)] har codeunit 12 følgende forbedringer:</span><span class="sxs-lookup"><span data-stu-id="434cc-122">In [!INCLUDE[d365fin](includes/d365fin_md.md)], codeunit 12 has had the following improvements:</span></span>  
  
* <span data-ttu-id="434cc-123">Codeunit 12 er blevet inddelt i mindre procedurer (alle under 100 kodelinjer).</span><span class="sxs-lookup"><span data-stu-id="434cc-123">Codeunit 12 has been refactored into smaller procedures (all less than 100 code lines).</span></span>  
* <span data-ttu-id="434cc-124">Standardiserede mønstre for søgning på finanskonti er implementeret ved hjælp af hjælpefunktioner fra bogføringsgruppetabeller.</span><span class="sxs-lookup"><span data-stu-id="434cc-124">Standardized patterns for the search of general ledger accounts have been implemented by using helper functions from Posting Group tables.</span></span>  
* <span data-ttu-id="434cc-125">En bogføringsstruktur er blevet implementeret for at administrere start og afslutning af transaktioner og isolere oprettelsen til finans- og momsposter, indsamling af momsregulering og beregning af beløb i ekstra valuta.</span><span class="sxs-lookup"><span data-stu-id="434cc-125">A Posting Engine Framework has been implemented to manage the start and finish of transactions and to isolate the creation to general ledger and VAT entries, the collection of VAT adjustment, and the calculation of additional currency amounts.</span></span>  
* <span data-ttu-id="434cc-126">Kopiering af koden er elimineret.</span><span class="sxs-lookup"><span data-stu-id="434cc-126">Code duplication has been eliminated.</span></span>  
* <span data-ttu-id="434cc-127">Mange hjælpefunktioner, der er overført til tilsvarende debitor- og kreditorposttabeller.</span><span class="sxs-lookup"><span data-stu-id="434cc-127">Many helper functions have been transferred to corresponding customer and vendor ledger entry tables.</span></span>  
* <span data-ttu-id="434cc-128">Brug af globale variabler er blevet minimeret, så hver enkelt procedure bruger parametre og indkapsler sin egen programlogik.</span><span class="sxs-lookup"><span data-stu-id="434cc-128">The use of global variables has been minimized, so that each procedure uses parameters and encapsulates its own application logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="434cc-129">Se også</span><span class="sxs-lookup"><span data-stu-id="434cc-129">See Also</span></span>  
<span data-ttu-id="434cc-130">[Designoplysninger: Bogføring af grænsefladestruktur](design-details-posting-interface-structure.md) </span><span class="sxs-lookup"><span data-stu-id="434cc-130">[Design Details: Posting Interface Structure](design-details-posting-interface-structure.md) </span></span>  
[<span data-ttu-id="434cc-131">Designoplysninger: Bogføringsprogramstruktur</span><span class="sxs-lookup"><span data-stu-id="434cc-131">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

