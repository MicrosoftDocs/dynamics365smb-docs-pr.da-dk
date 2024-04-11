---
title: 'Designdetaljer - Flows til produktion, montage og projekter'
description: Flere oplysninger om flow mellem placeringscentre i forbindelse med pluk af komponenter og placering af varer på lager for montage-eller produktionsordrer og projektordrer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 02/05/2024
ms.custom: bap-template
---
# Flows til produktion, montage og projekter

Interne flow, f. eks. pluk af komponenter og placering af varer på lager for montage, projekter og produktionsordrer ligner indgående eller udgående flow. Derfor kan der være kendte mange af processerne. Denne artikel indeholder oplysninger om, hvordan du kan arbejde med interne lagerflows med forskellige kompleksitetsniveauer.

## Oversigt over forskellige konfigurationsindstillinger

Du kan konfigurere lagerfunktioner på forskellige måder. Det er vigtigt, at de indstillinger, du vælger, forbedrer processerne uden at medføre spild. I følgende tabel beskrives standardkonfigurationer for håndtering af fysiske varer for produktion, projekter og montageordrer.

### Indgående flow (læg-på-lager)

|Kompleksitetsniveau|Beskrivlse|Indstillinger|Placeringskode|Indgående flow for produktionsordre|Indgående flow for montageordre|Indgående flow af projekter|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen dedikeret lageraktivitet.|Bogføring af ordrer og kladder||Valgfri. Kontrolleret af **Placeringskoden er obligatorisk** til/fra.|Produktionskladde -> Afgangskladde</br><br/> **Bemærk**: Du kan bogføre afgang vha **Produktionskladden**.|Montageordre|Læg-på-lager er ikke relevant for projekter|  
|Basis|Ordre for ordre|Kræv læg-på-lager. </br><br/> **BEMÆRK**: Selv om indstillingen kaldes **Kræv pluk**, kan du bogføre leverancer direkte fra kildeforretningsdokumentet på den lokation, hvor du markerer dette afkrydsningsfelt. |Valgfri. Kontrolleret af **Placeringskoden er obligatorisk** til/fra.|Produktionsordre -> Læg-på-lager|Montageordre|Læg-på-lager er ikke relevant for projekter|
|Avanceret|Konsoliderede læg-på-lager-aktiviteter for flere kildedokumenter.|Kræv tilgang + Kræv læg-på-lager|Valgfri. Kontrolleret af **Placeringskoden er obligatorisk** til/fra.|Produktionsordrer -> Afgangskladde|Montageordrer -> interne bevægelser | Læg-på-lager er ikke relevant for projekter|
|Avanceret|Samme som over + Styret pluk/læg-på-lager-aktiviteter|Styret pluk og læg-på-lager (afhængige Skift aktiveres automatisk)|Obligatorisk|Samme som ovenfor|Samme som ovenfor| Læg-på-lager er ikke relevant for projekter|

I nogle konfigurationer kan du ikke bruge dedikerede lagerdokumenter til at registrere læg-på-lager-aktiviteter. Men hvis lokationen bruger placeringer, kan du bruge standard bevægelses dokumenter til at flytte producerede eller monterede varer til lagerstedet. Du kan finde flere oplysninger i [Flytte varer ad hoc i grundlæggende lageropsætninger](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### Udgående flow (pluk)

|Kompleksitetsniveau|Beskrivlse|Indstillinger|Placeringskode|Udgående flow for produktionsordre|Udgående flow for montageordre|Udgående flow af projekter|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen dedikeret lageraktivitet.|Bogføring af ordrer og kladder||Valgfri. Kontrolleret af **Placeringskoden er obligatorisk** til/fra.|Produktionskladde -> Forbrugskladde </br><br/> **Bemærk**: Du kan bogføre afgang vha **Produktionskladden**.|Montageordre|Projekt -> Projektkladde|  
|Basis|Ordre for ordre|Kræv pluk. </br><br/> **Bemærk**: Selv om indstillingen kaldes **Kræv pluk**, kan du bogføre leverancer direkte fra kildeforretningsdokumentet på den lokation, hvor du markerer dette afkrydsningsfelt. <!-- ToDo Test prod output-->|Valgfri. Kontrolleret af **Placeringskoden er obligatorisk** til/fra.|Produktionsordre -> Lagerpluk|Montageordre -> flytning (lager)</br><br/>**Lagerbevægelsen** kan kun bruges sammen med placeringer.|Projekt -> Lagerpluk|
|Avanceret|Konsoliderede plukaktiviteter for flere kildedokumenter.|Kræv leverance + Kræv pluk|Valgfri. Kontrolleret af Placeringskoden er obligatorisk til/fra|Produktionsordrer -> lagerpluk -> Forbrugskladde |Montageordrer -> lagerpluk| Projekt(er) -> Lagerpluk -> Projektkladde |
|Avanceret|Samme som over + Styret pluk/læg-på-lager-aktiviteter|Styret pluk og læg-på-lager (afhængige Skift aktiveres automatisk)|Obligatorisk|Samme som ovenfor|Samme som ovenfor| Dirigerede Læg-på-lager og pluk understøttes ikke for projekter|

Som indgående flow kan nogle konfigurationer ikke bruge dedikerede lagerdokumenter til at registrere læg-på-lager-aktiviteter. Men hvis lokationen bruger placeringer, kan du bruge standard bevægelses dokumenter til at flytte producerede eller monterede varer. Flere oplysninger i [Flytte varer](warehouse-move-items.md).

## Lagersteder uden dedikeret lageraktivitet

Selvom du ikke har dedikeret lageraktiviteter, vil du sikkert stadig gerne holde styr på ting, f. eks. forbrug og produktionsafgang. Følgende artikler indeholder oplysninger om, hvordan du behandler modtagelser af kildedokumenter.

* [Registrere forbrug og afgang for én frigivet produktionsordrelinje](production-how-to-register-consumption-and-output.md)
* [Montere varer](assembly-how-to-assemble-items.md)
* [Registrere forbrug eller anvendelse af projekter](projects-how-record-job-usage.md)

## Grundlæggende lageropsætninger

De indgående og udgående flows i en grundlæggende lageropsætning omfatter følgende indstillinger på siden **Lokationskort** siden for lokationen:

* Ved det indgående flow (læg-på-lager), skal du slå funktionen **Kræv læg-på-lager** fra, men slå **Kræv modtagelse** til/fra.
* Ved det indgående flow (læg-på-lager), skal du slå funktionen **Kræv læg-på-lager** fra, men slå **Kræv modtagelse** til/fra.

### Flows til og fra produktion i en grundlæggende lageropsætning  

Brug **Lagerpluk**-dokumenter til at plukke produktionskomponenter i forløbet til produktion. Hvis du vil lægge produkterne på lager, skal du bruge **Læg-på-lager**-dokumenter.

For lokationer, der bruger placeringer, er det især praktisk at trække lagerbevægelser. Hvis du ønsker yderligere oplysninger om, hvordan komponentforbrug tømmes fra produktionsplaceringen eller den åbne produktionsplacering, kan du se afsnittet [Træk af produktionskomponenter i lageret](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Lagerbevægelser er vigtige dokumenter, hvis du bruger **Pluk + Fremad** eller **Pluk + Baglæns**-metoder. Få mere at vide i [Trækmetoder](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Felterne **Til-produktionsplaceringskode**, **Fra-produktionsplaceringskode** og **Åben prod.placeringskode** på lokationskortet eller produktionsressource/arbejdscenterkortene definerer standardflow til og fra produktionsområder.
* Styre bevægelsen af fremstillede varer på siden **Intern overførsel** uden en relation til en produktionsordre.

### Flows til og fra montage i en grundlæggende lageropsætning  

Bogfør montageafgang og forbrug direkte fra en montageordre.

> [!NOTE]
> **Lagerpluk** og **Læg-på-lager**-dokumenter understøttes ikke for montageordrer.

Lokationer til brug af placeringer:

* Bruge **Flytning (lager)**-dokumenter af varer til at flytte montagekomponenter til montageområdet.
* Felterne **Placeringskode til til-montage** og **Placeringskode til fra-montage** på lokationskortet definerer standardflow til og fra montageområder.
* Administrere bevægelsen af fremstillede varer på siden **Intern overførsel** uden en relation til en produktionsordre.

[!INCLUDE [prod_short](includes/prod_short.md)] understøtter montage efter lager-og montage efter ordre-montage processer. Flere oplysninger i [Om montage til ordre og montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). I forbindelse med lokationsstyring er montage til lager en del af den interne lager strøm, og montage efter ordre er i den udgående lagergang. Flere oplysninger i [Håndtering af montage til ordre-varer med pluk](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### Flows til projektstyring i en grundlæggende lageropsætning

Brug **Lagerpluk**-dokumenter til at plukke projektkomponenter i forløbet til projektstyring.

For en lokation, der bruger placeringer, definerer feltet **Til-projekt Placeringskode** på lokationen de standardstrømme, der skal bruges til projektstyringen.

## Avancerede lageropsætninger  

De indgående og udgående flows i en grundlæggende lageropsætning omfatter følgende indstillinger på siden **Lokationskort** for lokationen:

* Ved det indgående flow (læg-på-lager), skal du slå funktionen **Kræv læg-på-lager** fra, men slå **Kræv modtagelse** til/fra.
* Ved det indgående flow (læg-på-lager), skal du slå funktionen **Kræv læg-på-lager** fra, men slå **Kræv modtagelse** til/fra.

### Flows til og fra produktion i en avanceret lageropsætning

Brug **Lagerpluk**- dokumenterne og siden **Plukkladde** til at plukke komponenter til produktion.

Lokationer til brug af placeringer:

* **Lagerbevægelse**-dokumenter og **Bevægelsesregneark**-siden er især nyttige ved træk med komponenter. Flere oplysninger i [Træk af produktionskomponenter i lageret](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
* Felterne **Til-produktionsplaceringskode**, **Fra-produktionsplaceringskode** og **Åben prod.placeringskode** på lokationskortet eller produktionsressource/arbejdscenterkortene definerer standardflow til og fra produktionsområder. 
* Styre bevægelsen af fremstillede varer på siderne **Bevægelseskladde** eller **Intern læg-på-lager-aktivitet** uden en relation til en produktionsordre.

### Flows til og fra montage i en avanceret lageropsætning

Brug **Lagerpluk**-dokumenterne og siden **Plukkladde** til at plukke komponenter til produktion.

Lokationer til brug af placeringer:

* Felterne **Placeringskode til montage** og **Placeringskode fra montage** på lokationskortet definerer standardflow til og fra montageområder.
* Styre bevægelsen af fremstillede varer på siderne **Bevægelseskladde** eller **Intern læg-på-lager-aktivitet** uden en relation til en produktionsordre.

[!INCLUDE [prod_short](includes/prod_short.md)] understøtter montage efter lager-og montage efter ordre-montage processer. Flere oplysninger i [Om montage til ordre og montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Montage til lager er en del af det interne lagerflow, og montage efter ordre er i det udgående lagerflow. Flere oplysninger i [Håndtering af montageordrevarer i lagerleverancer](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### Flows til projektstyring i en avancerede lageropsætninger

Brug **Lagerpluk**-dokumenterne og siden **Plukkladde** til at plukke komponenter til produktion.

For en lokation, der bruger placeringer, definerer feltet **Til-projekter Placeringskode** på lokationen de standardstrømme, der skal bruges til projektstyringen.

## Se også  

[Oversigt over Warehouse Management](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
