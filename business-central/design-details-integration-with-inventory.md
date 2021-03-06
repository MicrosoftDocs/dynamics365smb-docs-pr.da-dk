---
title: Designoplysninger – Integration med lager | Microsoft Docs
description: Modulet Logistik og modulet Lager interagerer med hinanden på det fysiske lager og i lager eller logistikregulering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7e1b7a922109155471c212d688ce3ab468977deb
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922113"
---
# <a name="design-details-integration-with-inventory"></a>Designoplysninger: Integration med lager
Modulet Logistik og modulet Lager interagerer med hinanden på det fysiske lager og i lager eller logistikregulering.  
  
## <a name="physical-inventory"></a>Lageropgørelse  
 Siden **Lagerplacering - opg.kladde** bruges sammen med siden **Lageropgørelseskladde** til alle avancerede lagerlokationer. Lageret på placeringsniveau er beregnet, og en udskrevet liste leveres for lagermedarbejderen. Listen viser, hvilke varer der skal tælles på hvilke placeringer.  
  
 Lagermedarbejderen indtaster det optalte antal på siden **Lagerplacering - opg.kladde** og bogfører derefter kladden.  
  
 Hvis det optalte antal er større end antallet på kladdelinjen, bogføres en bevægelse for denne forskel fra standardreguleringsplaceringen til den optalte placering. Dette øger antallet på den placering, der er optalt, og reducerer antallet på standardreguleringsplaceringen.  
  
 Hvis det optalte antal er mindre end antallet på kladdelinjen, bogføres en bevægelse for denne forskel fra den optalte placering til standardreguleringsplaceringen. Dette reducerer antallet på den placering, der er optalt, og øger antallet på standardreguleringsplaceringen.  
  
 I avancerede lageropsætninger bliver værdien i feltet **Antal (beregnet)** hentet fra vareposter, og værdien i feltet **Antal (optalt)** er hentet fra lagerposter, bortset fra justeringen af placeringsindholdet. Feltet **Antal** angiver forskellen mellem de to første felter, som skal være lig med indholdet af reguleringsplaceringen.  
  
 Når du bogfører lageropgørelseskladde, opdateres lageret og standardreguleringsplaceringen.  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a>Lagerreguleringer til vareposten  
 Du kan bruge siden **Varekladde** og funktionen **Beregn regulering (logistik)** til at regulere beholdningen på vareposten i henhold til den regulering, der er foretaget i vareantallet på en lagerplacering. Hvis du vil oprette en tilknytning mellem lageret og lagerstedet, skal du definere en standardreguleringsplacering pr. lokation.  
  
 Reguleringsplaceringens standard registrerer varer på lageret, når du bogfører en forøgelse af lageret. Men hvis du bogfører en reducering, reduceres antallet på standardplaceringen også. I begge tilfælde oprettes vareposter og lagerposter.  
  
> [!NOTE]  
>  Reguleringsplaceringen er ikke inkluderet i disponeringsberegningen.  
  
 Hvis du vil justere placeringsindholdet, kan du bruge lagerkladden, hvorfra du kan angive det varenummer, den zonekode, den placeringskode og det antal, du vil justere.  
  
 Hvis du angiver et positivt antal og bogfører linjen, øges det lager, der opbevares på placeringen, og antallet på reguleringsplaceringens standard reduceres tilsvarende.  
  
## <a name="see-also"></a>Se også  
 [Designoplysninger: Logistik](design-details-warehouse-management.md)   
 [Designoplysninger: Tilgængelighed i lageret](design-details-availability-in-the-warehouse.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]