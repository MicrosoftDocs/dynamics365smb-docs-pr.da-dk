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
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2667b5d6d11172736a5dd6c3f7c810d42e3f2501
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="general-journal-post-line-overview"></a>Oversigt over bogføringslinje i finanskladde
Codeunit 12 **Finanskladde-Bogføringslinje** er det vigtigste udligningsobjekt til finansbogføring og er det eneste sted at indsætte finans-, moms- og debitor-og kreditorposter. Denne codeunit bruges også til alle handlinger med Udlign, Annuller udligning og Tilbagefør.  
  
Mens codeunit er blevet forbedret i hver udgave i de sidste ti år, er dens arkitektur i det væsentlige uændret. Codeunit blev meget stor med ca. 7.600 kodelinjer. Med denne version af [!INCLUDE[d365fin](includes/d365fin_md.md)] er arkitekturen ændret, og codeunit er gjort enklere og nemmere at vedligeholde. Denne dokumentation indeholder ændringerne og oplysninger, du skal bruge til opgradering.  
  
## <a name="old-architecture"></a>Gammel arkitektur  
Den gamle arkitektur havde følgende funktioner:  
  
* Der var omfattende brug af globale variabler, som øgede risikoen for skjulte fejl pga. brug af variabler med det forkerte område.  
* Der var mange lange procedurer (med mere end 100 kodelinjer), der også havde høj cyklomatisk kompleksitet (dvs. en masse indlejrede CASE, REPEAT, IF-sætninger), der gjorde det meget vanskeligt at læse og vedligeholde koden.  
* Flere procedurer, der kun blev anvendt lokalt og kun var beregnet til anvendelse lokalt, blev ikke markeret som lokale.  
* De fleste procedurer havde ingen parametre og brugte globale variabler. Nogle brugte parametre og tilsidesatte globale variabler med lokale.  
* Kodemønstre til søgning i finanskonti og oprettelse af finans- og momsposter var ikke standardiseret og varierede fra område til område. Der var desuden en masse kodeduplikering og brudt symmetri mellem debitor- og kreditorkode.  
* En stor del af koden i codeunit 12, ca. 30 procent, der vedrører kontantrabat og toleranceberegninger, selvom disse funktioner ikke er nødvendige i mange lande eller områder.  
* Bogføring, Udlign, Annuller udligning, Tilbagefør, Kontantrabat og Tolerance samt Valutakursregulering blev samlet i codeunit 12 ved hjælp af en lang liste af globale variabler.  
  
### <a name="new-architecture"></a>Ny arkitektur  
I [!INCLUDE[d365fin](includes/d365fin_md.md)] har codeunit 12 følgende forbedringer:  
  
* Codeunit 12 er blevet inddelt i mindre procedurer (alle under 100 kodelinjer).  
* Standardiserede mønstre for søgning på finanskonti er implementeret ved hjælp af hjælpefunktioner fra bogføringsgruppetabeller.  
* En bogføringsstruktur er blevet implementeret for at administrere start og afslutning af transaktioner og isolere oprettelsen til finans- og momsposter, indsamling af momsregulering og beregning af beløb i ekstra valuta.  
* Kopiering af koden er elimineret.  
* Mange hjælpefunktioner, der er overført til tilsvarende debitor- og kreditorposttabeller.  
* Brug af globale variabler er blevet minimeret, så hver enkelt procedure bruger parametre og indkapsler sin egen programlogik.  
  
## <a name="see-also"></a>Se også  
[Designoplysninger: Bogføring af grænsefladestruktur](design-details-posting-interface-structure.md)   
[Designoplysninger: Bogføringsprogramstruktur](design-details-posting-engine-structure.md)

