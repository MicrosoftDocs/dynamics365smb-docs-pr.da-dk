---
title: Tildele standardplaceringer til varer
description: 'Hvis du bruger placeringer på en lokation, kan du levere, modtage og flytte varerne meget mere effektivt ved at tildele varerne standardplaceringer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '7371, 7374, 7379'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Tildele standardplaceringer til varer
Hvis du bruger placeringer på en lokation, kan du levere, modtage og flytte varerne meget mere effektivt ved at tildele varerne standardplaceringer. Når en vare tildeles en standardplacering, foreslås denne placering, hver gang du starter en transaktion for denne vare. Standardplaceringer er defineret på siden **Placeringsindhold**.  

## Sådan tildeles en standardplacering til en vare
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opr.kladde til placeringsindh.**, og derefter vælge det relaterede link.  
2.  Udfyld oplysningerne om placeringskoden og varen for hver placering, du vil angive som standard for en vare. Sørg for at vælge feltet **Standard**.  
3.  Vælg handlingen **Opret placeringsindhold**. Varen tildeles nu standardplaceringer.  

> [!NOTE]  
>  Når en vare lægges på lager, og varen ikke er tildelt en standardplacering, bliver den placering, som varen lægges på lager på, standardplaceringen.  

## Sådan ændres standardplaceringen for en vare  
Det kan være nødvendigt at ændre den tildelte standardplacering for en vare eller at tildele en standardplacering til en ny vare.
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Placeringsindhold**, og vælg derefter det relaterede link.  
2.  Vælg den relevante lokationskode i feltet **Lokationsfilter**.  
3.  Søg efter den aktuelle post for standardplaceringsindholdet for varen, og fjern markeringen i afkrydsningsfeltet **Standardplacering**.  
4.  Søg efter linjen Placeringsindhold for den placering, du vil anvende som den nye standardplacering. Marker afkrydsningsfeltet **Standardplacering**.  

> [!NOTE]  
>  Når en vare lægges på lager første gang, og varen ikke er tildelt en standardplacering, bliver den placering, som varen lægges på lager på, standardplaceringen for varen.  

## Se også  
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Konfigurere Warehouse Management](warehouse-setup-warehouse.md) 
[Montagestyring](assembly-assemble-items.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]