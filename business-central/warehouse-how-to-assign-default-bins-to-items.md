---
title: Sådan tildeles standardplaceringer til varer | Microsoft Docs
description: Hvis du bruger placeringer på en lokation, kan du levere, modtage og flytte varerne meget mere effektivt ved at tildele varerne standardplaceringer. Når en vare tildeles en standardplacering, foreslås denne placering, hver gang du starter en transaktion for denne vare.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f3374929434876cee088f046efc6d5f950671cc8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756313"
---
# <a name="assign-default-bins-to-items"></a>Tildele standardplaceringer til varer
Hvis du bruger placeringer på en lokation, kan du levere, modtage og flytte varerne meget mere effektivt ved at tildele varerne standardplaceringer. Når en vare tildeles en standardplacering, foreslås denne placering, hver gang du starter en transaktion for denne vare. Standardplaceringer er defineret på siden **Placeringsindhold**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Sådan tildeles en standardplacering til en vare
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opr.kladde til placeringsindh.**, og vælg det relaterede link.  
2.  Udfyld oplysningerne om placeringskoden og varen for hver placering, du vil angive som standard for en vare. Sørg for at vælge feltet **Standard**.  
3.  Vælg handlingen **Opret placeringsindhold**. Varen tildeles nu standardplaceringer.  

> [!NOTE]  
>  Når en vare lægges på lager, og varen ikke er tildelt en standardplacering, bliver den placering, som varen lægges på lager på, standardplaceringen.  

## <a name="to-change-the-default-bin-for-an-item"></a>Sådan ændres standardplaceringen for en vare  
Det kan være nødvendigt at ændre den tildelte standardplacering for en vare eller at tildele en standardplacering til en ny vare.    
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **placeringsindhold**, og vælg derefter det relaterede link.  
2.  Vælg den relevante lokationskode i feltet **Lokationsfilter**.  
3.  Søg efter den aktuelle post for standardplaceringsindholdet for varen, og fjern markeringen i afkrydsningsfeltet **Standardplacering**.  
4.  Søg efter linjen Placeringsindhold for den placering, du vil anvende som den nye standardplacering. Marker afkrydsningsfeltet **Standardplacering**.  

> [!NOTE]  
>  Når en vare lægges på lager første gang, og varen ikke er tildelt en standardplacering, bliver den placering, som varen lægges på lager på, standardplaceringen for varen.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]