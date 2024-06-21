---
title: Sådan aktiveres pluk efter FEFO | Microsoft Docs
description: 'Første-udløbet-først ud (FEFO) er en sorteringsmetode, der sikrer, at de ældste elementer med den tidligste udløbsdato plukkes først.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Aktivere pluk af varer efter FEFO
Første-udløbet-først ud (FEFO) er en sorteringsmetode, der sikrer, at de ældste elementer med den tidligste udløbsdato plukkes først.  

 Denne funktionalitet fungerer kun, når følgende kriterier er opfyldt:  

-   Varen skal have et serie-/lotnummer.  
-   I opsætningen af varens varesporingskode skal feltet **SN-logistiksporing** eller feltet **Lot-lagersporing** være markeret.  
-   Varen skal bogføres til lageret med en udløbsdato.  
-   På lokationen skal du aktivere **Kræv pluk**, **Pluk i overensstemmelse med FEFO** og **Tvungen placering**.  

 Når alle kriterierne er opfyldt, sorteres serie-/lotnummererede varer, som skal plukkes, med de ældste først i alle pluk og bevægelser, undtagen for varer, der bruger SN-specifik eller lotspecifik sporing.  

> [!NOTE]  
> Hvis varer med serie- eller lotnumre bruger specifik sporing, vises disse først, og dernæst vises de resterende, ikke-specifikke serie - eller lotnumre i overensstemmelse med FEFO.
<br /><br />
Hvis der er to varer med serie- eller lotnumre, der har samme udløbsdato, vælges varen med det laveste serie- eller lotnummer.
<br /><br />
Når du plukker varer med serie- eller lotnumre på lokationer, der er konfigureret til styret læg-på-lager og pluk, er det kun antal på placeringer af typen *Pluk*, der plukkes i overensstemmelse med FEFO.  
<br /><br />
Hvis du vil aktivere bevægelser i overensstemmelse med FEFO, skal du lade feltet **Fra placeringskode** være tomt på siden **Flytning (lager)** eller **Bevægelseskladde**.  
<br /><br />
Hvis feltet **Nøje bogføring af udløbsdato** er markeret på **Varesporingskodekortet**, medtages kun varer, der ikke er udløbet, i plukket, og linjerne sorteres efter FEFO-princippet.

## Se også  
[Plukke varer til lagerleverance](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]