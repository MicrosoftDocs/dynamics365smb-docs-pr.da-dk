---
title: "Sådan plukkes til produktion i grundlæggende lageropsætninger | Microsoft Docs"
description: "Når lagerlokationen kræver pluk, men ikke leverance, skal du bruge vinduet **Pluk (lager)** til at organisere og registrere pluk af komponenter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 68702e384ea750535a8d7e5b83ee619856b6a34b
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="pick-for-production-or-assembly"></a>Plukke til produktion eller montage
Hvordan du skal lægge komponenter på lager til produktions- eller montageordrer afhænger af den måde, som lagerstedet er sat op på som en lokation. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).

I grundlæggende lageropsætninger, hvor lokationen kræver pluk, men ikke leverance, skal du bruge vinduet **Pluk (lager)** til at organisere og registrere pluk af komponenter.  

I grundlæggende lageropsætninger skal du plukke til montageordrer i vinduet **Flytning (lager)**. Du kan finde flere oplysninger i afsnittet "Håndtering af montage til ordre-varer med pluk (lager)" i [Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).  

I avancerede lageropsætninger, hvor lokationer kræver både pluk og leverancer, skal du bruge vinduet **Lagerpluk** til at flytte komponenter til produktions- eller montageordrer.

> [!NOTE]  
>  Der er følgende vigtige forskelle mellem plukninger fra lager og lagerbevægelser:  
>   
>  -   Når du registrerer et pluk for en intern handling, såsom produktion, bogføres forbrug af de komponenter, der er plukket på samme tid. Når du registrerer en flytning (lager) for en intern handling, registrerer du kun fysisk flytning af nødvendige komponenter til en placering i handlingsområdet uden bogføring af forbrug.  
> -   Når du bruger pluk fra lager definerer feltet **Placeringskode** på en produktionsordrekomponentlinje den *hente*-placering, som komponenter tages fra, når forbruget posteres. Når du bruger lagerbevægelser, definerer feltet **Placeringskode** på produktionsordrekomponentlinjerne den *område*-placering i handlingsområdet, hvor lagermedarbejderen skal placere komponenterne.  

En systemforudsætning for plukning eller flytning af komponenter til kildedokumenter er, at der findes en udgående lageranmodning til at give lagerområdet besked om komponentbehovet. Den udgående lageranmodning oprettes, hver gang produktionsordrestatus ændres til Frigivet, eller når en frigivet produktionsordre oprettes.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Sådan plukkes komponenter i grundlæggende lageropsætninger
I grundlæggende lageropsætninger, hvor placeringen er konfigureret til kun at bruge pluk, kan du plukke komponenter til produktionsaktiviteter i vinduet **Pluk (lager)**. Du kan finde flere oplysninger i [Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Pluk (lager)**, og vælg derefter det relaterede link.  
2.  Du kan få adgang til produktionsordrekomponenterne ved at vælge handlingen **Hent kildedokumenter** og derefter vælge den frigivne produktionsordre.  
3.  Foretag plukningen, og registrer derefter de faktiske plukoplysninger i feltet **Plukket antal**.  
4.  Når linjerne er klar til at blive bogført, skal du vælge handlingen **Bogfør**. Bogføringen opretter de nødvendige lagerposter og bogfører forbruget af varer.  

Du kan også oprette et **Pluk (lager)** direkte fra den frigivne produktionsordre. Vælg handlingen **Opret læg-på-lager/pluk**, marker afkrydsningsfeltet **Opret pluk (lager)**, og vælg derefter knappen **OK**.

Du kan også bruge vinduet **Flytning (lager)** til at flytte varer mellem placeringer og ad hoc, dvs. uden henvisning til et kildedokument.
Du kan finde flere oplysninger i [Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Håndtering af montage til ordre-varer med pluk (lager)
Vinduet **Pluk (lager)** bruges også til at plukke og afsende salg, hvor varerne skal monteres, inden de kan leveres. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).

Varer, der skal leveres, findes ikke fysisk i en placering, før de er monteret og bogført som afgang til en placering i montageområdet. Det betyder, at pluk af ordremontagevarer til levering følger en speciel strøm. Lagermedarbejderne fra en placering fragter montageelementerne til afsendelsesområdet og bogfører derefter lagerpluk. Den bogførte lagerpluk bogfører derefter montageafgang, komponentforbrug og salgsleverance.

Du kan konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)] til automatisk at oprette en flytning (lager), når lagerpluk for varen montageelementet oprettes. Når du vil gøre det, skal du vælge feltet **Opret bevægelser automatisk** i vinduet **Montagekonfiguration**. Du kan finde flere oplysninger i [Flytte komponenter til et handlingsområde i basislogistik](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Lagerpluklinjer for salgsvarer oprettes på forskellige måder afhængigt af, om ingen, nogle eller alle salgslinjemængderne samles til ordre.

Ved almindeligt salg, hvor du bruger pluk fra lager til at bogføre leverancer af lagerantal, oprettes der én lagerpluklinje – eller flere, hvis varen lægges på flere placeringer – for hver salgsordrelinje. Denne pluklinje er baseret på mængden i feltet **Lever (antal)**.

I montage efter ordre-salg hvor hele mængden i salgsordrelinjen monteres efter ordre, oprettes der en lagerpluklinje for den mængde. Det betyder, at værdien i feltet Antal til montage svarer til værdien i feltet **Lever (antal)**. Feltet **Montage til ordre** vælges på linjen.

Hvis montageoutputflow er konfigureret for lokationen, så indsættes værdien i feltet **Pla.kode til ordremontagelev.** eller værdien i feltet **Placeringskode til fra-montage**, i den rækkefølge, i feltet **Placeringskode** i lagerpluklinjen.

Hvis en placeringskode ikke er angivet på salgsordrelinjen, og montageafgangsstrøm ikke er konfigureret for lokationen, så er feltet **Placeringskode** i lagerpluklinjen tomt. Lagermedarbejderen skal åbne vinduet **Placeringsindhold** og vælge den placering, hvor montageelementerne monteres.

I kombinationsscenarier, hvor en del af mængden først skal samles, og en anden skal plukkes fra lageret, oprettes minimum to lagerpluklinjer. En pluklinje er for ordremontageantal. De andre pluklinje afhænger af, hvilke placeringer der kan opfylde restantal fra lageret. Placeringskoder på de to linjer udfyldes på forskellige måder, som beskrevet for de to forskellige salgtyper. Du kan finde flere oplysninger i afsnittet "Kombinationsscenarier" i [Om montage til ordre og montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="to-pick-components-in-advanced-warehouse-configurations"></a>Sådan plukkes komponenter i avancerede lageropsætninger
I avancerede lageropsætninger, hvor placeringen er konfigureret til at bruge både pluk og levering, kan du plukke komponenter til produktions- og montageaktiviteter i vinduet **Lagerpluk**. Du kan finde flere oplysninger i [Plukke varer med Pluk (logistik)](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Du kan også bruge vinduet **Bevægelseskladden** til at flytte varer mellem placeringer og ad hoc, dvs. uden henvisning til et kildedokument. Du kan finde flere oplysninger i [Flytte varer i avancerede lageropsætninger](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Du kan ikke oprette et lagerplukdokument fra bunden, fordi en plukaktivitet altid er en del af en arbejdsproces, enten i et pull- eller push-scenario.  

Du kan oprette lagerplukdokument på en push-måde ved at vælge handlingen **Opret pluk (logistik)** i kildedokumentet, som f.eks. en frigivet montageordre eller lagerleverance. Du kan finde flere oplysninger i [Plukke varer med Pluk (logistik)](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Du kan også oprette lagerplukdokument på en pull-måde fra vinduet **Plukkladde** for at registrere plukanmodninger, både for forsendelse og interne operationer, og derefter oprette de krævede lagerplukdokumenter.  

Følgende procedure beskriver et pull-scenario, hvor du plukker komponenter til en frigivet produktionsordre via vinduet **Plukkladde**. Fremgangsmåden gælder også for montageordrer.  

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
6.  Vælg knappen **OK**.

Lagerplukdokumenter oprettes nu med pluklinjer for hver komponent, der kræves i den interne operation.

Hvis det interne operationsområde, f.eks en produktionshal, er sat op med en standardplacering til placering af komponenter, der skal bruges i handlingen, indsættes placeringskoden i Placer-linjerne til lagerplukdokumentet, så lagermedarbejderne kan se, hvor de skal placere elementerne. Du kan finde flere oplysninger i [Oprette grundlæggende lagersteder med handlingsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

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

