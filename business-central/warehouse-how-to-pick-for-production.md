---
title: Plukke til produktion, montage eller jobs i grundlæggende lageropsætninger
description: Når lagerlokationen kræver pluk, men ikke leverance, skal du bruge siden Pluk (lager) til at organisere og registrere pluk af komponenter.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/02/2022
ms.author: bholtorf
ms.openlocfilehash: 859c70ebc51f2649000d41817d173292ed5b0870
ms.sourcegitcommit: b4da421c19c3aa3031b0344ec2829d2038be6642
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617872"
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Plukke til produktion, montage eller jobs i grundlæggende lageropsætninger

Hvordan du skal lægge komponenter på lager til produktions- eller montageordrer afhænger af den måde, som lagerstedet er sat op på som en lokation. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Plukke til produktion i grundlæggende lageropsætninger

Hvis lokationen kræver pluk, men ikke leverancebehandling, kan du bruge siden **Lagerpluk**. Du kan bruge siden **pluk (lager)** til at organisere og registrere plukningen af varer, hvis Trækmetode er indstillet til **Manuel**. Når du registrerer et lagerpluk, bogføres forbruget af de plukkede komponenter. Du kan også bruge **Flytning (lager)** med henvisning til et kildedokument for at placere komponenter, hvor trækmetoden er indstillet til **Manuel**, **Pluk + Forlæns** eller **Pluk + Tilbage** for produktionsordrer.

Når produktionsoperationer er integreret i lagerprocesser, enten efter placeringer eller styret læg-på-lager og pluk, er den placering, hvorfra komponenterne forbruges den placering, der er defineret på hver produktionsordres komponentlinje. Alle nødvendige komponenter skal være tilgængelige på den pågældende placering. Ellers stopper den manuelle eller udtrukne forbrugsbogføring for den pågældende komponent.

> [!NOTE]  
> Der er følgende vigtige forskelle mellem pluk fra lagerbeholdning, flytninger af lagerbeholdning og pluk fra lagersted:  
>
> - Når du registrerer et pluk for en intern handling, såsom produktion, bogføres forbrug af de komponenter, der er plukket på samme tid. Når du registrerer en flytning af lagerbehold eller et pluk fra et lagersted for en intern handling, registrerer du kun den fysiske flytning af de krævede komponenter til en placering i operationsområdet uden at bogføre forbruget.  
> - Når du bruger pluk fra lager definerer feltet **Placeringskode** på en produktionsordrekomponentlinje den *hente*-placering, som komponenter tages fra, når forbruget posteres. Når du bruger flytninger af lagerbeholdning eller pluk fra lagerstedet, definerer feltet **Placeringskode** på produktionsordrens komponentlinjer den *placering* i operationsområdet, hvor lagermedarbejderen skal placere komponenterne.  

Hvis du skal plukke eller flytte komponenter til kildedokumenter er, at der findes en udgående lageranmodning til at give lagerområdet besked om komponentbehovet. Den udgående lageranmodning oprettes, når du gør følgende:

- Ændre status på en produktionsordre til Frigivet.
- Opret en frigivet produktionsordre.  

Trækmetoder påvirker også flowet af komponenter i produktionen. Du kan finde flere oplysninger i [Udtrække komponenter i henhold til operationsafgang](production-how-to-flush-components-according-to-operation-output.md). **Flytning (lager)** med henvisning til kildedokumentet og **Pluk (logistik)** kan ikke bruges til at plukke komponenter med trækmetoderne *Fremad* og *Tilbage*. **Pluk (lager)** kan ikke bruges til at plukke komponenter med en anden trækmetode end *Manuel*. Hvis du vil håndtere resterende komponenter, skal du bruge **Flytning (lager)** uden henvisning til et kildedokument. Du kan finde flere oplysninger i [Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

I avancerede lageropsætninger, hvor lokationer kræver både pluk og leverancer, skal du bruge siden **Pluk (logistik)** til at placere komponenter, hvor trækmetoden er indstillet til *Manuel*, *Pluk + Forlæns* eller *Pluk + Tilbage* for produktionsordrer. Du kan finde flere oplysninger i [Plukke til produktion eller montage i avancerede lageropsætninger](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

## <a name="to-pick-components-for-production-and-jobs-in-basic-warehouse-configurations"></a>Plukke komponenter til produktion eller montage i en grundlæggende lageropsætning

I grundlæggende lageropsætninger, hvor placeringen er konfigureret til kun at bruge pluk, kan du plukke komponenter til produktionsaktiviteter og jobplanlægningslinjer på siden **Pluk (lager)**. Du kan finde flere oplysninger i [Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).

> [!NOTE]
> Muligheden for at plukke komponenter til Sagsplanlægningslinjer blev tilføjet i [!INCLUDE[d365fin](includes/d365fin_md.md)] i 2022 udgivelsesbølge 2. Hvis du vil starte med at bruge funktionen, skal din administrator aktivere **Funktionsopdatering: Aktivér lagerbeholdning og lagerpluk fra job** på siden **Funktionsstyring**.
>
>[!INCLUDE[prod_short](includes/prod_short.md)] bruger værdien i feltet **Restantal** på sagsplanlægningslinjen, når der oprettes pluk (lager). Hvis du vil bruge pluk fra lager til sager, skal du aktivere funktionen **Anvend anvendelseslink** på siden **opgavekortet** for sagen. På den måde kan du spore forbruget i forhold til din plan. Hvis du ikke aktiverer til/fra, forbliver restantallet ved **0**, og lagerplukket bliver ikke oprettet. Du kan finde flere oplysninger i [Sådan konfigureres sagsforbrugssporing](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk fra lager**, og vælg derefter det relaterede link.  
2. Du kan få adgang til produktionsordrekomponenterne ved at vælge handlingen **Hent kildedokumenter** og derefter vælge den frigivne produktionsordre.  
3. Foretag plukningen, og registrer derefter de faktiske plukoplysninger i feltet **Håndteringsantal**.  
4. Når linjerne er klar til at blive bogført, skal du vælge handlingen **Bogfør**. Bogføringen opretter de nødvendige lagerposter og bogfører forbruget af varer.  

Du kan også oprette et **Pluk (lager)** direkte fra den frigivne produktionsordre. Vælg handlingen **Opret læg-på-lager/pluk/flytning**, marker afkrydsningsfeltet **Opret pluk (lager)**, og vælg derefter knappen **OK**.

Som alternativ kan du bruge **Flytning (lager)** med henvisning til kildedokumentet for at flytte varer mellem placeringer. Du skal registrere forbruget særskilt. Du kan finde flere oplysninger i [Massebogføre produktionsforbrug](production-how-to-post-consumption.md).

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Plukke til montage i grundlæggende lageropsætninger

Brug følgende sider til at plukke til montageordrer:

- Siden **Flytning (lager)**.
- Hvis lokationen kræver pluk men ikke leveringer, skal du bruge siden **Pluk (lager)** til at plukke, samle og afsende salgsordrer, hvor varerne skal monteres, inden de kan leveres. Du kan finde flere oplysninger i [Håndtering af montage til ordre-varer med pluk (lager)](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

I avancerede lageropsætninger, hvor lokationer kræver både pluk og leverancer, skal du bruge siden **Pluk (logistik)** til at overføre komponenter til montageordrer. Du kan finde flere oplysninger i [Plukke til produktion eller montage i avancerede lageropsætninger](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Håndtering af montage til ordre-varer med pluk (lager)

Siden **Pluk (lager)** bruges også til at plukke og afsende salg, hvor varerne skal monteres, inden de kan leveres. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).

Lagervarer i montage til ordre-forløb findes ikke fysisk i en placering, før de er monteret og bogført som afgang til en placering i montageområdet. Plukning af disse varer til levering følger derfor en særlig strøm. Lagermedarbejderne fra en placering fragter montageelementerne til afsendelsesområdet og bogfører derefter lagerpluk. Den bogførte lagerpluk bogfører derefter montageafgang, komponentforbrug og salgsleverance.

Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til automatisk at oprette en flytning (lager), når lagerpluk for varen montageelementet oprettes. Hvis du vil oprette automatiske bevægelser, skal du vælge feltet **Opret bevægelser automatisk** på siden **Montagekonfiguration**. Du kan finde flere oplysninger i [Flytte komponenter til et handlingsområde i basislogistik](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

[!INCLUDE[prod_short](includes/prod_short.md)] opretter lagerpluklinjer for salgsvarer oprettes på forskellige måder afhængigt af, om ingen, nogle eller alle salgslinjemængderne samles til ordre.

- I det salg, hvor du bruger pluk (lager) til at bogføre lagerleverance, opretter [!INCLUDE[prod_short](includes/prod_short.md)] en lagerpluklinje for hver salgsordrelinje. Hvis varen placeres på forskellige placeringer, oprettes der mere end én linje. Pluklinjer er baseret på mængden i feltet **Lever (antal)**.
- I montage efter ordre-salg hvor hele mængden i salgsordrelinjen monteres efter ordre, oprettes der en lagerpluklinje for den mængde. Det betyder, at værdien i feltet Antal til montage svarer til værdien i feltet **Lever (antal)**. Feltet **Montage til ordre** vælges på linjen.

Hvis montageoutputflow er konfigureret for lokationen, så indsættes værdien i feltet **Pla.kode til ordremontagelev.** eller værdien i feltet **Placeringskode til fra-montage**, i den rækkefølge, i feltet **Placeringskode** i lagerpluklinjen.

Hvis en placeringskode ikke er angivet på salgsordrelinjen, og montageafgangsstrøm ikke er konfigureret for lokationen, så er feltet **Placeringskode** i lagerpluklinjen tomt. Lagermedarbejderen skal åbne siden **Placeringsindhold** og vælge den placering, hvor montageelementerne monteres.

Når en del af mængden først skal samles, og en anden skal plukkes fra lageret, opretter [!INCLUDE[prod_short](includes/prod_short.md)] som minimum to lagerpluklinjer. En pluklinje er for ordremontageantal. De andre pluklinje afhænger af, hvilke placeringer der kan opfylde restantal fra lageret. Placeringskoder på de to linjer udfyldes på forskellige måder, som beskrevet for de to forskellige salgtyper. Du kan finde flere oplysninger i afsnittet "Kombinationsscenarier" i [Om Montage til ordre og Montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

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
