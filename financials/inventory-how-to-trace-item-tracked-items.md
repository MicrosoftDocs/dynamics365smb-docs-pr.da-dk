---
title: "Sådan spores varesporede varer | Microsoft Docs"
description: "Du kan se, hvor en vare med varesporing blev brugt, herunder hvordan og hvornår den blev modtaget eller fremstillet, overflyttet, solgt, forbrugt eller returneret. Du kan også finde alle aktuelle forekomster af et bestemt serienummer eller lotnummer i databasen. Du kan gøre dette ved hjælp af funktionerne Varesporing og Naviger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cc24989d2cf770cd88bbde23d483e3859ff4a68a
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="trace-item-tracked-items"></a>Spore vare via varesporing
Du kan se, hvor en vare med varesporing blev brugt, herunder hvordan og hvornår den blev modtaget eller fremstillet, overflyttet, solgt, forbrugt eller returneret. Du kan også finde alle aktuelle forekomster af et bestemt serienummer eller lotnummer i databasen. Du kan gøre dette ved hjælp af funktionerne Varesporing og Naviger.  

 Disse funktioner kan især være praktiske i kvalitetskontrol, når du vil finde ud af, hvilke kunder der har modtaget produkter med et bestemt lotnummer, eller du vil finde ud af, hvilken lot en defekt komponent stammer fra.  

 Du kan spore fremad og bagud i en sekvens af bogførte lagertransaktioner for serie- eller lotnummer i vinduet **Varesporing**.  

 I vinduet **Naviger** kan du ikke se sekvensen af transaktioner, men du kan se alle poster for serie- eller lotnummeret, både bogførte poster og åbne poster.  

 De to funktioner kan bruges i kombination ved at overføre sporede serienummer eller lotnummer til vinduet **Naviger** for at afslutte et komplet sporingsscenarie. Du kan finde flere oplysninger i [Gennemgang: Sporing af serie-/lotnumre](walkthrough-tracing-serial-lot-numbers.md).  

## <a name="to-trace-item-tracked-items"></a>Sådan spores varer via varesporing  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varesporing**, og vælg derefter det relaterede link.  
2.  Du kan angive bestemte varenumre i filterfelterne øverst i vinduet, eller du kan angive et filter for et interval af de varenumre, du vil spore.  
3.  I feltet **Vis komponenter** kan du vælge, om du også vil se, hvor komponenterne til varerne stammer fra. Der er følgende indstillinger i feltet.  

    |Felt|Description|  
    |----------------------------------|---------------------------------------|  
    |**Nej**|Vælg denne indstilling, hvis du ikke vil have vist nogen komponenter.|  
    |**Kun varesporing**|Vælg denne indstilling, hvis du kun vil se de komponenter, der har lot- eller serienumre.|  
    |**Alle**|Vælg denne indstilling, hvis du vil se alle komponenter.|  

4.  Vælg den metode i feltet **Sporingsmetode**, du vil bruge til sporing af varen. Der findes følgende indstillinger  

    |Felt|Description|  
    |----------------------------------|---------------------------------------|  
    |**Forbrug->Oprindelse**|Denne metode sporer varen ved at starte med, hvor den blev brugt til, hvor den kom fra. Hvis f.eks. en produceret vare blev solgt til en debitor, viser vinduet **Varesporing** dette med salgsleverancelinjen først, som du derefter kan udvide, så du kan se, hvilken produktionsordre den kom fra.|  
    |**Oprindelse->Forbrug**|Denne metode sporer varen ved at starte med, hvor den ankommer til lageret, til hvor den blev brugt. Hvis f.eks. en produceret vare blev solgt til en debitor, viser vinduet **Varesporing** dette med den færdige produktionsordre først, som du derefter kan udvide, så du kan se, hvilken produktionsordre den kom fra.|  

5.  Vælg handlingen **Sporing** for at udføre sporingen.  

> [!NOTE]  
>  Hvis du har modtaget det samme parti på flere transaktioner, viser vinduet **Varesporing** måske ikke alle transaktioner. Der vises kun de udlignede transaktioner.  

> [!NOTE]  
>  Hvis du allerede har sporet yderligere transaktionsoversigt under en varelinje fra en anden linje ovenfor, så vil afkrydsningsfeltet **Allerede sporet** være markeret. For at give en enklere visning, vises sådanne underliggende linjer ikke.  
>   
>  Hvis du vil finde de varesporingslinjer, hvor transaktionsoversigten allerede er sporet, skal du vælge knappen **Gå til allerede sporede**. Den pågældende varesporingslinje er markeret, og alle underliggende linjer er udvidet.  

## <a name="to-find-item-tracked-items-with-navigate"></a>Sådan findes varesporede varer med Naviger  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Naviger**, og vælg derefter det relaterede link.  
2.  Angiv de varesporingsnumre, du ønsker at spore, i felterne **Serienr.** og **Lotnr.** i oversigtspanelet **Varesporing**.  
3.  Vælg handlingen **Find** for at finde alle forekomster af serienummer eller lotnummer i databasen.  

## <a name="see-also"></a>Se også  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Varesporing](design-details-item-tracking.md)
[Designoplysninger: Varesporing og reservationer](design-details-item-tracking-and-reservations.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Gennemgang: Sporing af serie-/lotnumre](walkthrough-tracing-serial-lot-numbers.md)

