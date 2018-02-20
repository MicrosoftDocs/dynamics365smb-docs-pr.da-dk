---
title: "Sådan konfigureres lokationer til at bruge placeringer | Microsoft Docs"
description: "Placeringer udgør den grundlæggende lagerstruktur og bruges til at fremsætte forslag om placeringen af varer. Når du har oprettet placeringerne, kan du meget præcist definere det indhold, du vil placere på hver placering, eller placeringen kan fungere som en løs placering uden angivet indhold."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2d84f1222dccca86f5906af1c82fc0e6192173d6
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-locations-to-use-bins"></a>Oprette lokationer til brug af placeringer
Placeringer udgør den grundlæggende lagerstruktur og bruges til at fremsætte forslag om placeringen af varer. Når du har oprettet placeringerne, kan du meget præcist definere det indhold, du vil placere på hver placering, eller placeringen kan fungere som en løs placering uden angivet indhold.  

Hvis du vil benytte placeringer på en lokation, skal du først aktivere funktionaliteten på kortet **Lokation**. Derefter kan du designe varestrømmen på placeringen ved at angive placeringskoder i konfigurationsfelter, der repræsenterer forskellige strømme.  

> [!NOTE]  
>  Placeringskoderne skal være oprettet, før du kan angive placeringskoder på lokationskortet. Du kan finde flere oplysninger under [Oprette placeringer](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a>Sådan konfigureres en lokation til at bruge placeringer  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg derefter det relaterede link.  
2.  Vælg den lokation, hvor du vil bruge placeringer.  
3.  Vælg handlingen **Rediger**.  
4.  Markér afkrydsningsfeltet **Tvungen placering** i oversigtspanelet **Lagersted**.  
5.  Hvis du ikke bruger styret læg-på-lager og pluk for lokationen, skal du udfylde feltet **Standardplacering** med den metode, der skal bruges, når en vare tildeles en standardplacering.  
6.  Åbn kortet for den lokation, du vil konfigurere placeringer for.
7.  I oversigtspanelet **Placeringer** skal du vælge de placeringer, der skal bruges som standardplaceringer for modtagelser, leverancer samt for indgående, udgående og åbne produktionsplaceringer.  
8.  De placeringskoder, som du angiver her, vises automatisk i hovederne og på linjerne af de forskellige lagerdokumenter. Standardplaceringerne definerer alle start- og slutplaceringer for varer på lagerstedet.  
9.  Hvis du bruger styret læg-på-lager og pluk, skal du vælge en placering til lagerreguleringerne. Placeringskoden i feltet **Reguleringsplaceringskode** angiver den virtuelle placering, hvor du skal registrere afvigelser i lagerbeholdningen, når du enten registrerer fundne afvigelser registreret i lagerkladden, eller afvigelser, der beregnes, når du registrerer en lagerplaceringsopgørelse.  
10. Udfyld felterne i oversigtspanelet **Plac.metode**, hvis de er relevante for lagerstedet. De vigtigste felter er **Placeringskap.regel**, **Tillad nedbrydning** og **Læg-på-lager-skabelonkode**.  
11. Vælg oversigtspanelet **Lagersted**, og udfyld felterne **Udgående lagerekspeditionstid**, **Indgående lagerekspeditionstid** og **Basiskalenderkode**. Du kan finde flere oplysninger i [Opsætte basiskalendere](across-how-to-assign-base-calendars.md).

## <a name="filling-the-consumption-bin"></a>Udfylde forbrugsplaceringen
Dette flow-diagram viser, hvordan feltet **Placeringskode** i produktionsordrekomponenter udfyldes i henhold til din lokationsopsætning.

![Placeringsrutediagram](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Se også
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

