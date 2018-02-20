---
title: "Sådan konverteres eksisterende lokationer til lagerlokationer | Microsoft Docs"
description: Du kan aktivere en eksisterende lagerlokation til at anvende zoner og placeringer og til at fungere som en lagerlokation.
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
ms.openlocfilehash: 7d4b2c86174386faa86ab6c09faa463d26d3d2ac
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="convert-existing-locations-to-warehouse-locations"></a>Konvertere eksisterende lokationer til lagerlokationer
Du kan aktivere en eksisterende lagerlokation til at anvende zoner og placeringer og til at fungere som en lagerlokation.  

Kørslen, der aktiverer en lokation til lagerhåndteringen, opretter lagerposter til lagerreguleringsplaceringen for alle varer med et lager på lokationen. De første poster afstemmes, når lagerstedets fysiske lagerposter bogføres, efter at kørslen er udført.  

Du kan oprette zoner og placeringer enten før eller efter konverteringen. Den eneste placering, som du skal oprette inden konverteringen, er den, som skal anvendes som fremtidig reguleringsplacering.  

> [!IMPORTANT]  
>  Du kan rydde alt negativt lager og alle åbne lagerdokumenter, før du konverterer lokationen for lagerekspedition ved at køre en rapport for at identificere varer med negativt lager og åbne lagerdokumenter, der hører til lokationen. Du kan finde flere oplysninger i Kontroller for negativt lager.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a>Sådan aktiveres en eksisterende lokation til at fungere som en lagerlokation  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opret lagerlokation**, og vælg derefter det relaterede link.  
2.  I feltet **Lokationskode** skal du angive den lokation, du vil aktivere til behandling af lageret.  
3.  I feltet **Reguleringsplaceringskode** skal du angive placeringen på den lokation, hvor ikke-synkroniserede lagerposter gemmes. Du kan finde flere oplysninger i afsnittet "Sådan synkroniseres de regulerede lagerposter med de relaterede vareposter" i [Tælle, justere og ompostere lager](inventory-how-count-adjust-reclassify.md).  

    Ved hjælp af åbne vareposter til den angivne lokation oprettes lagerkladdelinjer, der summerer hver kombination af Varenr., Variantkode, Enhedskode, og hvis det er relevant, Partinr. og Serienr. i vareposterne. Derefter bogføres lagerkladdelinjerne. Denne bogføring opretter lagerposter, som placerer lageret i lagerreguleringsplaceringen. **Reguleringsplaceringskoden** på lokationskortet er også angivet.  

4.  Hvis du vil se, hvilke varer der er føjet til reguleringsplaceringen, kan du køre rapporten **Regul.placering (logistik)**.  
5.  Når kørslen af **Opret lagerlokation** er afsluttet, skal du udføre og bogføre en lagerplaceringsopgørelseskladde. Du kan finde flere oplysninger i [Tælle, justere og ompostere inventar](inventory-how-count-adjust-reclassify.md).  

> [!NOTE]  
>  Det anbefales, at du udfører kørslen **Opret lagerlokation** på et tidspunkt, hvor det ikke influerer på det daglige arbejde i systemet. Denne opgave behandler hver post i **vareposttabellen**, og hvis der er et større antal vareposter, kan denne opgave tage flere timer.  

 For lokationer, der ikke anvendte lageradministrationsdokumenter inden konverteringen, skal du genåbne og frigive alle kildedokumenter, der blev delvist modtaget eller delvist leveret inden konverteringen.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

