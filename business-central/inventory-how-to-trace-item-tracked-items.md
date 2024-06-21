---
title: Spore vare via varesporing
description: 'Du kan se, hvor en vare med varesporing er brugt, herunder hvordan og hvornår den blev modtaget eller fremstillet, overflyttet med varesporing eller find poster.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.forms: '6520,'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="trace-item-tracked-items"></a>Spore vare via varesporing

Du kan se, hvor en vare med varesporing er brugt, herunder hvordan og hvornår den blev modtaget eller fremstillet, overflyttet, solgt, forbrugt eller returneret. Du kan også finde alle aktuelle forekomster af et bestemt serienummer eller lotnummer i databasen. Du kan gøre dette ved hjælp af funktionerne Varesporing og [Find poster](ui-find-entries.md).  

Disse funktioner kan især være praktiske i kvalitetskontrol, når du vil finde ud af, hvilke kunder der har modtaget produkter med et bestemt lotnummer, eller du vil finde ud af, hvilken lot en defekt komponent stammer fra.  

 Du kan spore fremad og bagud i en sekvens af bogførte lagertransaktioner for serie- eller lotnummer på siden **Varesporing**.  

 På siden **Find poster** kan du ikke se sekvensen af transaktioner, men du kan se alle poster for serie- eller lotnummeret, både bogførte poster og åbne poster.  

 De to funktioner kan bruges i kombination ved at overføre sporede serienummer eller lotnummer til siden **Find poster** for at afslutte et komplet sporingsscenarie. <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## <a name="to-trace-item-tracked-items"></a>Sådan spores varer via varesporing

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varesporing**, og vælg derefter det relaterede link.  
2.  Du kan angive bestemte varenumre i filterfelterne øverst på siden, eller du kan angive et filter for et interval af de varenumre, du vil spore.  
3.  I feltet **Vis komponenter** kan du vælge, om du vil se, hvor komponenterne til varerne stammer fra. Den følgende tabel beskriver indstillingerne.  

    |Felt|Beskrivlse|  
    |----------------------------------|---------------------------------------|  
    |**Nej**|Vis ikke komponenter.|  
    |**Kun varesporing**|Vis kun de komponenter, der har lot- eller serienumre.|  
    |**Alle**|Vis alle komponenter.|  

4.  Vælg den metode i feltet **Sporingsmetode**, du vil bruge til sporing af varen. Den følgende tabel beskriver indstillingerne.  

    |Felt|Beskrivlse|  
    |----------------------------------|---------------------------------------|  
    |**Forbrug->Oprindelse**|Spor varen fra der, hvor den blev brugt til, hvor den kom fra. Hvis f.eks. en produceret vare blev solgt til en debitor, viser siden **Varesporing** dette med salgsleverancelinjen først, som du derefter kan udvide, så du kan se, hvilken produktionsordre den kom fra.|  
    |**Oprindelse->Forbrug**|Spor varen fra der, hvor den kom til lagere til, hvor den kom blev anvendt. Hvis f.eks. en produceret vare blev solgt til en debitor, viser siden **Varesporing** dette med den færdige produktionsordre først, som du derefter kan udvide, så du kan se, hvilken produktionsordre den kom fra.|  

5.  Vælg handlingen **Sporing** for at udføre sporingen.  

> [!NOTE]  
>  Der vises kun de udlignede transaktioner. Hvis du har modtaget det samme parti på flere transaktioner, viser siden **Varesporing** måske ikke alle transaktioner.   

> [!NOTE]  
>  Hvis du allerede har sporet yderligere transaktionsoversigt under en varelinje fra en anden linje ovenfor, så vil afkrydsningsfeltet **Allerede sporet** være markeret. For at give en enklere visning, vises sådanne underliggende linjer ikke.  
>   
>  Hvis du vil finde de varesporingslinjer, hvor transaktionsoversigten allerede er sporet, skal du vælge knappen **Gå til allerede sporede**. Den pågældende varesporingslinje er markeret, og alle underliggende linjer er udvidet.  

## <a name="to-find-item-tracked-items-with-find-entries"></a>Sådan findes varesporede varer med Find poster

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Find poster**, og vælg derefter det relaterede link.  
2. Vælg **Handlinger** > **Find efter** > **Søg efter varereference**.
3. I felterne **Serienr.** og **Lotnr.** skal du angive de varesporingsnumre, du ønsker at spore.  
4. Vælg handlingen **Find** for at finde alle forekomster af serienummer eller lotnummer i databasen.  

## <a name="see-also"></a>Se også

[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med serie-, lot- og pakkenumre](inventory-how-work-item-tracking.md)  
[Designoplysninger: Varesporing](design-details-item-tracking.md)  
[Designoplysninger - Varesporing og reservationer](design-details-item-tracking-and-reservations.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[Find poster](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
