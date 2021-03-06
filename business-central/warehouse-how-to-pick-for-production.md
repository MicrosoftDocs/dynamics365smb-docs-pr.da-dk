---
title: Sådan plukkes til produktion i grundlæggende lageropsætninger | Microsoft Docs
description: Når lagerlokationen kræver pluk, men ikke leverance, skal du bruge siden **Pluk (lager)** til at organisere og registrere pluk af komponenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a4ea3530a51ff7919118f436a8060f97d4056637
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759788"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Plukke til produktion eller montage i grundlæggende lageropsætninger
Hvordan du skal lægge komponenter på lager til produktions- eller montageordrer afhænger af den måde, som lagerstedet er sat op på som en lokation. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).

I grundlæggende lageropsætninger, hvor lokationen kræver pluk, men ikke leverance, skal du bruge siden **Pluk (lager)** til at organisere og registrere pluk af komponenter.  

I grundlæggende lageropsætninger skal du plukke til montageordrer på siden **Flytning (lager)**. Du kan finde flere oplysninger i [Håndtering af montage til ordre-varer med pluk (lager)](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

I avancerede lageropsætninger, hvor lokationer kræver både pluk og leverancer, skal du bruge siden **Lagerpluk** til at flytte komponenter til produktions- eller montageordrer. Du kan finde flere oplysninger i [Plukke til produktion eller montage i avancerede lageropsætninger](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

> [!NOTE]  
>  Der er følgende vigtige forskelle mellem plukninger fra lager og lagerbevægelser:  
>   
>  -   Når du registrerer et pluk for en intern handling, såsom produktion, bogføres forbrug af de komponenter, der er plukket på samme tid. Når du registrerer en flytning (lager) for en intern handling, registrerer du kun fysisk flytning af nødvendige komponenter til en placering i handlingsområdet uden bogføring af forbrug.  
> -   Når du bruger pluk fra lager definerer feltet **Placeringskode** på en produktionsordrekomponentlinje den *hente*-placering, som komponenter tages fra, når forbruget posteres. Når du bruger lagerbevægelser, definerer feltet **Placeringskode** på produktionsordrekomponentlinjerne den *område*-placering i handlingsområdet, hvor lagermedarbejderen skal placere komponenterne.  

En systemforudsætning for plukning eller flytning af komponenter til kildedokumenter er, at der findes en udgående lageranmodning til at give lagerområdet besked om komponentbehovet. Den udgående lageranmodning oprettes, hver gang produktionsordrestatus ændres til Frigivet, eller når en frigivet produktionsordre oprettes.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Sådan plukkes komponenter i grundlæggende lageropsætninger
I grundlæggende lageropsætninger, hvor placeringen er konfigureret til kun at bruge pluk, kan du plukke komponenter til produktionsaktiviteter på siden **Pluk (lager)**. Du kan finde flere oplysninger i [Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagerpluk**, og vælg derefter det relaterede link.  
2.  Du kan få adgang til produktionsordrekomponenterne ved at vælge handlingen **Hent kildedokumenter** og derefter vælge den frigivne produktionsordre.  
3.  Foretag plukningen, og registrer derefter de faktiske plukoplysninger i feltet **Plukket antal**.  
4.  Når linjerne er klar til at blive bogført, skal du vælge handlingen **Bogfør**. Bogføringen opretter de nødvendige lagerposter og bogfører forbruget af varer.  

Du kan også oprette et **Pluk (lager)** direkte fra den frigivne produktionsordre. Vælg handlingen **Opret læg-på-lager/pluk**, marker afkrydsningsfeltet **Opret pluk (lager)**, og vælg derefter knappen **OK**.

Du kan også bruge siden **Flytning (lager)** til at flytte varer mellem placeringer og ad hoc, dvs. uden henvisning til et kildedokument.
Du kan finde flere oplysninger i [Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Håndtering af montage til ordre-varer med pluk (lager)
Siden **Pluk (lager)** bruges også til at plukke og afsende salg, hvor varerne skal monteres, inden de kan leveres. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).

Varer, der skal leveres, findes ikke fysisk i en placering, før de er monteret og bogført som afgang til en placering i montageområdet. Det betyder, at pluk af ordremontagevarer til levering følger en speciel strøm. Lagermedarbejderne fra en placering fragter montageelementerne til afsendelsesområdet og bogfører derefter lagerpluk. Den bogførte lagerpluk bogfører derefter montageafgang, komponentforbrug og salgsleverance.

Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til automatisk at oprette en flytning (lager), når lagerpluk for varen montageelementet oprettes. Når du vil gøre det, skal du vælge feltet **Opret bevægelser automatisk** på siden **Montagekonfiguration**. Du kan finde flere oplysninger i [Flytte komponenter til et handlingsområde i basislogistik](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Lagerpluklinjer for salgsvarer oprettes på forskellige måder afhængigt af, om ingen, nogle eller alle salgslinjemængderne samles til ordre.

Ved almindeligt salg, hvor du bruger pluk fra lager til at bogføre leverancer af lagerantal, oprettes der én lagerpluklinje – eller flere, hvis varen lægges på flere placeringer – for hver salgsordrelinje. Denne pluklinje er baseret på mængden i feltet **Lever (antal)**.

I montage efter ordre-salg hvor hele mængden i salgsordrelinjen monteres efter ordre, oprettes der en lagerpluklinje for den mængde. Det betyder, at værdien i feltet Antal til montage svarer til værdien i feltet **Lever (antal)**. Feltet **Montage til ordre** vælges på linjen.

Hvis montageoutputflow er konfigureret for lokationen, så indsættes værdien i feltet **Pla.kode til ordremontagelev.** eller værdien i feltet **Placeringskode til fra-montage**, i den rækkefølge, i feltet **Placeringskode** i lagerpluklinjen.

Hvis en placeringskode ikke er angivet på salgsordrelinjen, og montageafgangsstrøm ikke er konfigureret for lokationen, så er feltet **Placeringskode** i lagerpluklinjen tomt. Lagermedarbejderen skal åbne siden **Placeringsindhold** og vælge den placering, hvor montageelementerne monteres.

I kombinationsscenarier, hvor en del af mængden først skal samles, og en anden skal plukkes fra lageret, oprettes minimum to lagerpluklinjer. En pluklinje er for ordremontageantal. De andre pluklinje afhænger af, hvilke placeringer der kan opfylde restantal fra lageret. Placeringskoder på de to linjer udfyldes på forskellige måder, som beskrevet for de to forskellige salgtyper. Du kan finde flere oplysninger i afsnittet "Kombinationsscenarier" i [Om Montage til ordre og Montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Udfylde forbrugsplaceringen
Dette flow-diagram viser, hvordan feltet **Placeringskode** i produktionsordrekomponenter udfyldes i henhold til din lokationsopsætning.

![Placeringsrutediagram](media/binflow.png "BinFlow")

## <a name="see-also"></a>Se også
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]