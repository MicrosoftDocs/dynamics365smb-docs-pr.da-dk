---
title: Designoplysninger – Varesporing i lageret | Microsoft Docs
description: Serienummer og lotnummer håndteres primært som lageropgave, så alle indgående og udgående lagerdokumenter har derfor standardfunktioner til at tildele og markere varesporingsnumre. Da reservationssystemet er baseret på vareposter, understøttes lageraktivitetsdokumenter, der kun registrerer lagerposter, dog ikke fuldt ud.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a482e0fed80d5e9380b6c6e0ec03557abbc02953
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "917812"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a>Designoplysninger: Varesporing i lageret
Serienummer og lotnummer håndteres primært som lageropgave, så alle indgående og udgående lagerdokumenter har derfor standardfunktioner til at tildele og markere varesporingsnumre.  

Da reservationssystemet er baseret på vareposter, understøttes lageraktivitetsdokumenter, der kun registrerer lagerposter, dog ikke fuldt ud. Da reservationer og varesporingsnumre kun kan håndteres på lokationsniveau, og ikke på placerings- og zoneniveau, kan siden **Varesporingslinjer** ikke åbnes fra lageraktivitetsdokumenter. Det samme gælder for siden **Reservation**.  

Efter et serienummer eller et lotnummer er føjet til en vare på en placering i lageret, kan det frit flyttes og omposteres inden for lageret ved hjælp af en uafhængig varesporingsstruktur, som ikke er relateret til reservationssystemet. **Serienr.** og **Lotnr.** er felter med direkte adgang på lagerdokumentlinjer. Når serie- eller lotnummer senere indgår i udgående bogføring, synkroniseres det med reservationssystemet som en del af den almindelige placeringsregulering. Du kan finde flere oplysninger i [Designoplysninger: Integration med lager](design-details-integration-with-inventory.md).  

Dog tager reservationssystemet lageraktiviteter i betragtning ved beregning af tilgængelighed. Varer, der allokeres til pluk eller registreres som plukket, kan f.eks. ikke reserveres. Du kan finde flere oplysninger i [Designoplysninger: Lagertilgængelighed](design-details-availability-in-the-warehouse.md).

## <a name="see-also"></a>Se også  
[Designoplysninger: Varesporing](design-details-item-tracking.md)  
[Designoplysninger: Integration med lager](design-details-integration-with-inventory.md)  
[Designoplysninger - Lagertilgængelighed](design-details-availability-in-the-warehouse.md)  
[Designoplysninger: Design af varesporing](design-details-item-tracking-design.md)
