---
title: 'Designdetaljer – flows for produktion, montage og projekter'
description: Flere oplysninger om flow mellem placeringscentre i forbindelse med pluk af komponenter og placering af varer på lager for montage-eller produktionsordrer og projektordrer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 08/12/2024
ms.custom: bap-template
---
# <a name="flows-for-production-assembly-and-projects"></a>Flows til produktion, montage og projekter

Interne flow, f. eks. pluk af komponenter og placering af varer på lager for montage, projekter og produktionsordrer ligner indgående eller udgående flow. Mange af processerne kan virke velkendte. Denne artikel indeholder oplysninger om, hvordan du kan arbejde med interne lagerflows med forskellige kompleksitetsniveauer.

## <a name="overview-of-different-configuration-options"></a>Oversigt over forskellige konfigurationsindstillinger

Du kan konfigurere lagerfunktioner på forskellige måder. Det er vigtigt, at de indstillinger, du vælger, forbedrer processerne uden at medføre spild. I følgende tabel beskrives standardkonfigurationer for håndtering af fysiske varer for produktion, projekter og montageordrer.

### <a name="inbound-flow-put-away"></a>Indgående flow (læg-på-lager)

|Kompleksitetsniveau|Beskrivlse|Indstillinger|Placeringskode|Indgående flow for produktionsordre|Indgående flow for montageordre|Indgående flow af projekter|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen dedikeret lageraktivitet.|Bogføring af ordrer og kladder||Valgfri. Kontrolleret af **Placeringskoden er obligatorisk** til/fra.|Produktionskladde -> Afgangskladde</br><br/> **Bemærk**: Du kan bogføre afgang vha **Produktionskladden**.|Montageordre|Læg-på-lager gælder ikke for projekter|  
|Basis|Ordre for ordre|Håndtering af produktionsafgang: Læg-på-lager (lager). </br><br/> **BEMÆRK:** Du kan stadig bogføre output direkte fra kildedokumenterne på steder, hvor du aktiverede disse indstillinger. |Valgfri. Kontrolleret af **Placeringskoden er obligatorisk** til/fra.|Produktionsordre -> Læg-på-lager|Montageordre|Læg-på-lager gælder ikke for projekter|
|Avanceret|Konsoliderede læg-på-lager-aktiviteter for flere kildedokumenter.|Ingen dedikerede indstillinger|Valgfri. Kontrolleret af **Placeringskoden er obligatorisk** til/fra.|Produktionsordrer -> Afgangskladde|Montageordrer -> interne bevægelser | Læg-på-lager gælder ikke for projekter|
|Avanceret|Samme som ovenfor plus styrede afhentnings-/læg-på-lager-aktiviteter|Styret pluk og læg-på-lager (afhængige Skift aktiveres automatisk)|Obligatorisk|Samme som ovenfor|Samme som ovenfor| Læg-på-lager gælder ikke for projekter|

Nogle konfigurationer tillader ikke, at du kan bruge dedikerede lagerdokumenter til at registrere læg-på-lager-aktiviteter. Men hvis lokationen bruger placeringer, kan du bruge standard bevægelses dokumenter til at flytte producerede eller monterede varer til lagerstedet. Flere oplysninger i [Flytte varer](warehouse-move-items.md).

### <a name="outbound-flow-pick"></a>Udgående flow (pluk)

|Kompleksitetsniveau|Beskrivelse|Indstillinger|Placeringskode|Udgående flow for produktionsordre|Udgående flow for montageordre|Udgående flow af projekter|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen dedikeret lageraktivitet.|Bogføring af ordrer og kladder||Valgfri. Kontrolleret af **Placeringskoden er obligatorisk** til/fra.|Produktionskladde -> Forbrugskladde </br><br/> **Bemærk**: Du kan bogføre afgang vha **Produktionskladden**.|Montageordre|Projekt -> Projektkladde|  
|Basis|Ordre for ordre|Produktion, Montage, Projekter: Pluk (lager), Bevægelse af lagerbeholdning </br><br/> **BEMÆRK: Du kan stadig bogføre forbruget direkte fra kildedokumenterne på de lokationer,** hvor du har aktiveret disse indstillinger.|Valgfri. Kontrolleret af **Placeringskoden er obligatorisk** til/fra.|Produktionsordre -> Lagerpluk|Montageordre -> flytning (lager)</br><br/>**Lagerbevægelsen** kan kun bruges sammen med placeringer.|Projekt -> Lagerpluk|
|Avanceret|Konsoliderede plukaktiviteter for flere kildedokumenter.|Produktion, Montage, Projekter: Pluk (logistik)|Valgfri. Kontrolleret af Placeringskoden er obligatorisk til/fra|Produktionsordrer -> lagerpluk -> Forbrugskladde |Montageordrer -> lagerpluk| Projekt(er) -> Lagerpluk -> Projektkladde |
|Avanceret|Samme som over + Styret pluk/læg-på-lager-aktiviteter|Styret pluk og læg-på-lager (afhængige Skift aktiveres automatisk)|Obligatorisk|Samme som ovenfor|Samme som ovenfor| Styret pluk og læg-på-lager understøttes ikke for projekter|

## <a name="warehouses-without-dedicated-warehouse-activity"></a>Lagersteder uden dedikeret lageraktivitet

Selvom du ikke bruger dedikerede lageraktiviteter, kan det være en god ide at spore ting som forbrug og produktionsoutput. Følgende artikler indeholder oplysninger om, hvordan du behandler modtagelser af kildedokumenter.

* [Registrere forbrug og afgang for én frigivet produktionsordrelinje](production-how-to-register-consumption-and-output.md)
* [Montere varer](assembly-how-to-assemble-items.md)
* [Registrere forbrug eller anvendelse af projekter](projects-how-record-job-usage.md)

## <a name="basic-warehouse-configuration"></a>Grundlæggende lageropsætninger

### <a name="flows-to-and-from-production-in-a-basic-warehouse-configuration"></a>Flows til og fra produktion i en grundlæggende lageropsætning

De indgående og udgående flows i en grundlæggende lageropsætning omfatter følgende indstillinger på siden **Lokationskort** siden for lokationen:

* For det indgående flow (læg-på-lager) i **produktionsoutputlageret. skal** du vælge **Læg-på-lager (lager)**.
* For det udgående flow (pluk) i **produktionsforbrugslageret. i feltet Håndtering** skal du vælge **Pluk/bevægelse** (lager).

Brug **Lagerpluk**-dokumenter til at plukke produktionskomponenter i forløbet til produktion. Hvis du vil lægge produkterne på lager, skal du bruge **Læg-på-lager**-dokumenter.

For lokationer, der bruger placeringer, er det især praktisk at trække lagerbevægelser. Hvis du ønsker yderligere oplysninger om, hvordan komponentforbrug tømmes fra produktionsplaceringen eller den åbne produktionsplacering, kan du se afsnittet [Træk af produktionskomponenter i lageret](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Lagerbevægelser er vigtige dokumenter, hvis du bruger **Pluk + Fremad** eller **Pluk + Baglæns**-metoder. Få mere at vide i [Trækmetoder](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Felterne **Til-produktionsplaceringskode**, **Fra-produktionsplaceringskode** og **Åben prod.placeringskode** på lokationskortet eller produktionsressource/arbejdscenterkortene definerer standardflow til og fra produktionsområder.
* Styre bevægelsen af fremstillede varer på siden **Intern overførsel** uden en relation til en produktionsordre.

### <a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration"></a>Flows til og fra montage i en grundlæggende lageropsætning

Det udgående flow i en grundlæggende lagerkonfiguration omfatter følgende indstillinger på siden Lokation **kort**  for lokationen:

* For det udgående flow (pluk) i Asm **. Forbrug Whse. skal** du vælge **Lagerbevægelse**.

Brug **dokumenterne Lagerbevægelser** til at plukke samlingskomponenter i flowet til montage. Bogfør montageafgang og forbrug direkte fra en montageordre.

> [!NOTE]
> **Lagerpluk** og **Læg-på-lager**-dokumenter understøttes ikke for montageordrer.

Lokationer til brug af placeringer:

* Bruge **Flytning (lager)**-dokumenter af varer til at flytte montagekomponenter til montageområdet.
* Felterne **Placeringskode til til-montage** og **Placeringskode til fra-montage** på lokationskortet definerer standardflow til og fra montageområder.
* Administrere bevægelsen af fremstillede varer på siden **Intern overførsel** uden en relation til en produktionsordre.

[!INCLUDE [prod_short](includes/prod_short.md)] understøtter montage efter lager-og montage efter ordre-montage processer. Flere oplysninger i [Om montage til ordre og montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). I forbindelse med lokationsstyring er montage til lager en del af den interne lager strøm, og montage efter ordre er i den udgående lagergang. Flere oplysninger i [Håndtering af montage til ordre-varer med pluk](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="flows-for-project-management-in-a-basic-warehouse-configuration"></a>Flows til projektstyring i en grundlæggende lageropsætning

Det udgående flow i en grundlæggende lagerkonfiguration omfatter følgende indstillinger på siden Lokation **kort**  for lokationen:

* For det udgående flow (pluk) i Projekt **forbrugslager. i feltet Håndtering** skal du vælge **Pluk** (lager).

Brug **Lagerpluk**-dokumenter til at plukke projektkomponenter i forløbet til projektstyring.

For en lokation, der bruger placeringer, definerer feltet **Til-projekt Placeringskode** på lokationen de standardstrømme, der skal bruges til projektstyringen.

## <a name="advanced-warehouse-configurations"></a>Avancerede lageropsætninger

### <a name="flows-to-and-from-production-in-advanced-warehouse-configurations"></a>Flows til og fra produktion i en avanceret lageropsætning

Det udgående flow i en avanceret lagerkonfiguration omfatter følgende indstillinger på siden Lokation **kort**  for lokationen:

* For det udgående flow (pluk) i **produktionsforbrugslageret. vælge**  **Pluk (valgfrit)**  eller **Pluk (obligatorisk).**

Brug **Lagerpluk**- dokumenterne og siden **Plukkladde** til at plukke komponenter til produktion.

> [!NOTE]
> **Læg-på-lager-dokumenter** understøttes ikke for produktionsafgang.

Lokationer til brug af placeringer:

* **Lagerbevægelse**-dokumenter og **Bevægelsesregneark**-siden er især nyttige ved træk med komponenter. Flere oplysninger i [Træk af produktionskomponenter i lageret](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
* Felterne **Til-produktionsplaceringskode**, **Fra-produktionsplaceringskode** og **Åben prod.placeringskode** på lokationskortet eller produktionsressource/arbejdscenterkortene definerer standardflow til og fra produktionsområder. 
* Styre bevægelsen af fremstillede varer på siderne **Bevægelseskladde** eller **Intern læg-på-lager-aktivitet** uden en relation til en produktionsordre.

### <a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations"></a>Flows til og fra montage i en avanceret lageropsætning

Det udgående flow i en avanceret lagerkonfiguration omfatter følgende indstillinger på siden Lokation **kort**  for lokationen:

* For det udgående flow (pluk) i Asm **. Forbrug Whse. vælge**  **Pluk (valgfrit)**  eller **Pluk (obligatorisk).** 

Brug **Lagerpluk**-dokumenterne og siden **Plukkladde** til at plukke komponenter til produktion.

> [!NOTE]
> **Dokumentet Læg-på-lager** understøttes ikke for montageordrer.

Lokationer til brug af placeringer:

* Felterne **Placeringskode til montage** og **Placeringskode fra montage** på lokationskortet definerer standardflow til og fra montageområder.
* Styre bevægelsen af fremstillede varer på siderne **Bevægelseskladde** eller **Intern læg-på-lager-aktivitet** uden en relation til en produktionsordre.

[!INCLUDE [prod_short](includes/prod_short.md)] understøtter montage efter lager-og montage efter ordre-montage processer. Flere oplysninger i [Om montage til ordre og montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Montage til lager er en del af det interne lagerflow, og montage efter ordre er i det udgående lagerflow. Flere oplysninger i [Håndtering af montageordrevarer i lagerleverancer](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### <a name="flows-to-project-management-in-advanced-warehouse-configurations"></a>Flows til projektstyring i en avancerede lageropsætninger

Det udgående flow i en avanceret lagerkonfiguration omfatter følgende indstillinger på siden Lokation **kort**  for lokationen:

* For det udgående flow (pluk) i Projekt **forbrugslager. vælge**  **Pluk (valgfrit)**  eller **Pluk (obligatorisk).**

Brug **Lagerpluk**-dokumenterne og siden **Plukkladde** til at plukke komponenter til produktion.

For en lokation, der bruger placeringer, definerer feltet **Til-projekter Placeringskode** på lokationen de standardstrømme, der skal bruges til projektstyringen.

## <a name="see-also"></a>Se også

[Oversigt over Warehouse Management](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
