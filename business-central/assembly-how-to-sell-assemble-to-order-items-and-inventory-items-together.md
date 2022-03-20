---
title: Sælge montage til ordre-varer og lagervarer sammen
description: Men hvis en del eller alle af antallet, ikke er tilgængeligt, har du mulighed for at oprette en montageordre for det resterende antal løbende.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 9409c33858f32628c9f8a85fe6d19fd5afb5986f
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381879"
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Sælge montage til ordre-varer og lagervarer sammen
Hvis feltet **Montagepolitik** på varekortet til et montageelement indeholder **Montage til lager**, standardsalgsordreprocessen forudsætte, at elementet allerede er monteret og kan plukkes fra lageret, hvis det er tilgængeligt. Derfor er ingen montageordre automatisk oprettet og tilknyttet salgsordrelinjen. Men hvis en del eller alle af mængden ikke er tilgængelige, har du fleksibilitet til at oprette en montageordre for den resterende del ved at udfylde feltet **Antal til montage efter ordre** på salgsordrelinjen. På den måde kan du montere varen efter ordre, selvom den som standard er indstillet til montage til lager.  

Der findes lignende fleksibilitet, når du sælger varer, der skal samles til ordren, og der er en del af mængden på lageret, som du vil modregne i montageordren. Du kan finde flere oplysninger i [Sælge lagervarer i montage til ordre-flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
>  Der gælder bestemte regler for feltet **Lever antal** på salgsordrelinjer, der indeholder en kombination af montage til ordre-antal og lagerantal. Du kan finde flere oplysninger i afsnittet Kombinationsscenarier i [Om Montage til ordre og Montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

> [!NOTE]  
>  Følgende procedure omfatter ikke de standardsalgsordretrin, du skal følge, før du opretter en montageordre for mængder, der ikke er tilgængelige.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Sådan sælger du montage efter ordre-varer og lagervarer sammen  
1.  På en salgsordrelinje for en vare, der er konfigureret til samling til lageret, skal du angive det antal i feltet **Antal**, der overskrider lageret. Siden **Kontroller tilgængelighed** vises. Du kan finde flere oplysninger i [Vise tilgængeligheden af varer](inventory-how-availability-overview.md).
2.  Bemærk feltet **Samlet antal** med en negativ værdi, som du skal angive i næste trin.  
3.  I feltet **Antal til montage efter ordre** skal du indtaste værdien fra det forrige trin.  
4.  Udfør alle ændringer af montagekomponenterne. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).  
5.  Fortsæt med at frigive salgsordren, for at gøre den klar til pluk af lagervarer og montage af utilgængelige elementer. Yderligere oplysninger om disse trin til standardmontage finder du i [Montere varer](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  Feltet **Placeringskode** på salgsordren kan være udfyldt på forhånd i henhold til feltet **Pla.kode til ordremontagelev.** eller feltet **Placeringskode til fra-montage** på lokationskortet. I så fald kan feltet **Placeringskode** på salgsordrelinjen være forkert i denne kombination af mængder til montage efter ordre og montage til lager. Det er en god idé at undersøge feltet **Placeringskode** og kontrollere, at placeringen fungerer for alle mængder. Du kan også angive de to forskellige mængder på separate salgsordrelinjer.  

## <a name="see-also"></a>Se også  
[Montagestyring](assembly-assemble-items.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]