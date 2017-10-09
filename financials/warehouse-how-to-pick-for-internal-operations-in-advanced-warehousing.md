---
title: "Sådan plukkes til interne operationer i avancerede lageropsætninger | Microsoft Docs"
description: "I avancerede lageropsætninger, hvor placeringen er konfigureret til at bruge både pluk og levering, kan du plukke komponenter til produktions- og montageaktiviteter i vinduet **Lagerpluk**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 94f45dd0b9d3a384fa0aafcc8f0555c52de25816
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-pick-for-assembly-or-production-in-advanced-warehouse-configurations"></a>Sådan plukkes til montage eller produktion i avancerede lageropsætninger
I avancerede lageropsætninger, hvor placeringen er konfigureret til at bruge både pluk og levering, kan du plukke komponenter til produktions- og montageaktiviteter i vinduet **Lagerpluk**.  

Du kan også bruge vinduet **Bevægelseskladden** til at flytte varer mellem placeringer og ad hoc, dvs. uden henvisning til et kildedokument. Du kan finde flere oplysninger i [Fremgangsmåde: Flytte varer i avancerede lageropsætninger](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Du kan finde oplysninger om pluk af varer til interne operationer på grundlæggende lagerlokationer, der er konfigureret kun til plukning, i [Fremgangsmåde: Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

Du kan ikke oprette et lagerplukdokument fra bunden, fordi en plukaktivitet altid er en del af en arbejdsproces, enten i et pull- eller push-scenario.  

Du kan oprette lagerplukdokument på en push-måde ved at vælg **Opret pluk (logistik)** i kildedokumentet, som f.eks. en frigivet montageordre eller lagerleverance. Du kan finde flere oplysninger i [Sådan plukkes varer med Pluk (logistik)](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Du kan også oprette lagerplukdokument på en pull-måde fra vinduet **Plukkladde** for at registrere plukanmodninger, både for forsendelse og interne operationer, og derefter oprette de krævede lagerplukdokumenter.  

Følgende procedure beskriver et pull-scenario, hvor du plukker komponenter til en frigivet produktionsordre via vinduet **Plukkladde**. Fremgangsmåden gælder også for en montageordre.  

Hvis du vil oprette pluk-anmodninger, både for pull- og push-scenarier, skal de pågældende kildedokumenter være frigivet. Frigiv kildedokumenter for interne operationer på følgende måder.  

|Kildedokument|Frigivelsesmetode|  
|---------------------|--------------------|  
|Produktionsordre|Skift ordretype til frigivet produktionsordre.|  
|Montageordre|Skift status til frigivet.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Sådan plukkes komponenter ved hjælp af plukkladden  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Plukkladde**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Hent lagerdokumenter**, og vælg derefter komponentlinjerne fra den frigivne produktionsordre.  
3.  Sorter linjerne for at opnå en effektiv plukrunde, og kombiner dem eventuelt med andre kladdelinjer for udnytte medarbejderens tid optimalt.  
4.  Vælg handlingen **Opret pluk**.  
5.  Definer, hvordan du vil oprette lagerplukdokumenterne, og hvordan du vil sortere pluklinjer ved at udfylde felter i vinduet **Opret pluk**.  
6.  Vælg knappen **OK**. Lagerplukdokumenter oprettes med pluklinjer for hver komponent, der kræves i den interne operation.  

Hvis det interne operationsområde, f.eks en produktionshal, er sat op med en standardplacering til placering af komponenter, der skal bruges i handlingen, indsættes placeringskoden i Placer-linjerne til lagerplukdokumentet, så lagermedarbejderne kan se, hvor de skal placere elementerne. Du kan finde flere oplysninger i felterne **Produktionsplaceringskode** eller **Placeringskode til til-montage**.

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

