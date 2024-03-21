---
title: Sælge montage til ordre-varer og lagervarer sammen
description: 'Men hvis en del af montage til lager ikke er tilgængeligt, har du mulighed for at oprette en montageordre for det resterende antal.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.service: dynamics-365-business-central
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Sælge montage til ordre-varer og lagervarer sammen

Hvis feltet **Montagepolitik** på varekortet til et montageelement indeholder **Montage til lager**, standardsalgsordreprocessen forudsætte, at elementet allerede er monteret og kan plukkes fra lageret, hvis det er tilgængeligt. Derfor er ingen montageordre automatisk oprettet og tilknyttet salgsordrelinjen. Men hvis en del af montage til lager ikke er tilgængeligt, har du mulighed for at oprette en montageordre for det resterende antal. Indtast den samlede mængde i feltet **Antal til montage til ordre** på rammemontageordrelinjen. Med denne indstilling kan du montere varen efter ordre, selvom den som standard er indstillet til montage til lager.  

Du har lignende fleksibilitet, når du sælger montage efter ordre-varer, og noget af antallet allerede er på lager. Du skal trække dette antal fra montageordren. Du kan lære mere om montage efter ordre ved at gå til [Sælge varer, der er samlet til ordre](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
> Der gælder bestemte regler for feltet **Levér antal** på salgsordrelinjer, der indeholder en kombination af montage til ordre-antal og lagerantal. Hvis du vil vide mere om reglerne, skal du gå til [kombinationsscenarier](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

> [!NOTE]  
> Følgende procedure omfatter ikke de salgsordretrin, du skal følge, før du opretter en montageordre for mængder, der ikke er tilgængelige.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Sådan sælger du montage efter ordre-varer og lagervarer sammen

1. På en salgsordrelinje for en vare, der er konfigureret til samling til lageret, skal du angive det antal i feltet **Antal**, der overskrider lageret. Siden **Kontroller tilgængelighed** vises. Hvis du vil vide mere om varedisponering, kan du gå til [Vis varedisponering](inventory-how-availability-overview.md).
2. I feltet **Antal til montage efter ordre** skal du indtaste værdien fra feltet **I alt**.  
3. Udfør alle nødvendige ændringer af montagekomponenterne. Lær mere i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md)  
4. Frigiv salgsordren for at gøre varerne tilgængelige til pluk af lagervarer og montage af utilgængelige elementer. Yderligere oplysninger om disse trin til standardmontage finder du i [Montere varer](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Feltet **Placeringskode** på salgsordren kan være udfyldt på forhånd i henhold til feltet **Pla.kode til ordremontagelev.** eller feltet **Placeringskode til fra-montage** på lokationskortet. I så fald kan feltet **Placeringskode** på salgsordrelinjen være forkert i denne kombination af mængder til montage efter ordre og montage til lager. Det er en god idé at undersøge feltet **Placeringskode** og kontrollere, at placeringen fungerer for alle mængder. Du kan også angive de to forskellige mængder på separate salgsordrelinjer.  

## <a name="see-also"></a>Se også

[Montagestyring](assembly-assemble-items.md)  
[Arbejde med montagestyklister](assembly-how-work-assembly-boms.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
