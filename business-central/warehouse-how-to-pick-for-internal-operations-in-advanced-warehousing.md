---
title: Plukke til interne operationer i avancerede lageropsætninger
description: Hvis lokationerne bruger pluk og levering, skal du plukke komponenter til produktions-og montage aktiviteter på siden pluk (logistik).
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/02/2022
ms.author: bholtorf
ms.openlocfilehash: 2ef879e5dbabb9281114d62a956ad4b10113c199
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607549"
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Pluk til produktion, montage eller jobs i avancerede lageropsætninger

I avancerede lageropsætninger, hvor placeringen er konfigureret til at bruge både pluk og levering, kan du plukke komponenter til produktions- og montageaktiviteter på siden **Lagerpluk**.  

Du kan også bruge siden **Bevægelseskladden** til at flytte varer mellem placeringer og ad hoc, dvs. uden henvisning til et kildedokument. Du kan finde flere oplysninger i [Flytte varer i avancerede lageropsætninger](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Du kan finde oplysninger om pluk af varer på grundlæggende lagerlokationer, der er konfigureret kun til plukning, i [Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

> [!NOTE]
> Du kan ikke oprette et lagerplukdokument fra bunden, fordi en plukaktivitet altid er en del af en arbejdsproces, enten i et pull- eller push-scenario.  

Du kan oprette lagerplukdokument på en push-måde ved at vælg **Opret pluk (logistik)** i kildedokumentet, som f.eks. en frigivet montageordre eller lagerleverance. Du kan finde flere oplysninger i [Plukke varer med Pluk (logistik)](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Du kan også oprette et plukdokument (logistik) på en pull-måde ved at bruge siden **Plukkladde** til at registrere plukanmodninger. Denne metode er nyttig i forbindelse med levering og intern drift. Derefter kan du oprette de krævede lagerplukdokumenter.  

Følgende procedure beskriver et pull-scenario, hvor du plukker komponenter til en frigivet produktionsordre via siden **Plukkladde**. Fremgangsmåden gælder også for en montageordre.  

Hvis du vil oprette pluk-anmodninger, både for pull- og push-scenarier, skal de pågældende kildedokumenter være frigivet. Frigiv kildedokumenter for interne operationer på følgende måder.  

|Kildedokument|Frigivelsesmetode|  
|---------------------|--------------------|  
|Produktionsordre|Skift ordretype til frigivet produktionsordre.|  
|Montageordre|Skift status til Frigivet.|
|Sager | Skift status til Åben.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Sådan plukkes komponenter ved hjælp af plukkladden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Plukkladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Hent lagerdokumenter**, og vælg derefter komponentlinjerne fra den frigivne produktionsordre.  
3. Sortér linjerne for at sikre en effektiv plukning. Du kan også vælge at samle linjer for at spare tid.  
4. Vælg handlingen **Opret pluk**.  
5. Definer, hvordan du vil oprette lagerplukdokumenterne, og hvordan du vil sortere pluklinjer ved at udfylde felter på siden **Opret pluk**.  
6. Vælg knappen **OK**. Lagerplukdokumenter oprettes med pluklinjer for hver komponent, der kræves i den interne operation.  

Operationsområder som f. eks. produktionsanlæg kan have en standardplacering for de komponenter, de kræver. Hvis det er tilfældet, føjes standardplaceringskoden til lagerplukdokumentet for at angive, hvor varerne skal lægges til. Du kan finde flere oplysninger i felterne **Produktionsplaceringskode** eller **Placeringskode til til-montage**.

## <a name="filling-the-consumption-bin"></a>Udfylde forbrugsplaceringen

Dette flow-diagram viser, hvordan feltet **Placeringskode** i produktionsordrekomponenter udfyldes i henhold til din lokationsopsætning.

![Placeringsrutediagram.](media/binflow.png "BinFlow")  

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Se også

[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
