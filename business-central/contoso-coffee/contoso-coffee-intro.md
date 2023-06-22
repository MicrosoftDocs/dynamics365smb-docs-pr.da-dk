---
title: Introduktion til demonstrationsdata for Contoso Coffee
description: 'Oversigt over scenarier for, hvordan oplysninger om demonstrationsdata for Contoso Coffee kan hjælpe dig med at lære, hvordan du bruger funktionerne i Business central.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-demo-data" />Introduktion til demonstrationsdata for Contoso Coffee

Contoso Coffee er en fiktiv virksomhed, der producerer forbruger- og kommercielle kaffemaskine. Apps **Contoso Coffee** til Business Central tilføjer demodata, som du kan bruge til at lære, hvordan du bruger funktionerne i Business central.  


## <a name="set-up-contoso-coffee-data" />Opsætning af Contoso Coffee-data

Hvis du vil bruge demonstrationsdataene fra Contoso Coffee, skal du installere to apps i det relevante regnskab i [!INCLUDE [prod_short](../includes/prod_short.md)]:  

- **Demonstrationsdata for Contoso Coffee**  

    Denne app leverer demonstrationsdata til basisprogrammet.  
- **Demonstrationsdata for Contoso Coffee (lande-id)**  

    Denne app tilføjer landespecifik indhold oven på basisprogrammet.

Føj apps til et tomt firma i et betalt abonnement eller som en del af et prøveabonnement. Du kan f. eks. oprette en ny virksomhed uden eksempeldata fra guiden **Opret ny virksomhed**, som du kan åbne fra **virksomhedslisten**. Tilføj derefter apps fra [markedspladsen](../ui-extensions-install-uninstall.md#install), hvis de ikke allerede er angivet på siden **Udvidelsesstyring**.  

Derefter skal du gøre følgende:
 - [Produktionsopsætningen](manufacturing/contoso-coffee-manufacturing-intro.md) til forberedelse til brug af [produktionsscenarierne](#manufacturing-scenarios)
 - [Lagerstedsopsætningen](warehousing/contoso-coffee-warehousing-intro.md) til forberedelse til brug af [lagerstedsscenarierne](#warehousing-scenarios)

## <a name="manufacturing-scenarios" />Produktionsscenarier

Contoso Coffee-demodata understøtter i øjeblikket følgende produktionsscenarier for test og træning:

1. [Opret en ny produktionsstykliste og styklisteversion](manufacturing/create-new-production-bom-version.md)  
2. [Opret en ny rute](manufacturing/create-new-routing.md)  
3. [Opret en ny fastlagt produktionsordre og ændre den](manufacturing/create-firm-planned-production-order-change.md)  
4. [Kombinere automatisk og manuel træk](manufacturing/combine-automatic-manual-flushing.md)  
5. [Bruge Ordreplanlægning til at oprette og reservere levering](manufacturing/order-planning-create-reserve-supply.md)  
6. [Konfigurere og behandle en underleverandør operation](manufacturing/set-up-process-subcontracting-operation.md)  
7. [Opret ny kapacitet](manufacturing/set-up-new-capacity.md)  
8. [Prognosebehov for varevarianter med forskellige styklister tildelt](manufacturing/variants.md)  

Læs trinene for hvert scenarie i den relevante artikel.  

> [!IMPORTANT]
> Produktionsgennemgangen kræver, at brugeroplevelsen er sat til *Premium* på siden **Firmaoplysninger**.

## <a name="warehousing-scenarios" />Lagerstedsscenarier

Contoso Coffee-demodata understøtter i øjeblikket følgende lagerstedsscenarier for test og træning:

1.  Konfigurere standardplaceringer, modtagelse og læg-på-lager med læg-på-lager, pluk og Levér lager med pluk (lager) i ordre-til-ordre-måden med [gennemgang af indgående og udgående flow i grundlæggende lageropsætninger](warehousing/warehouse-basic-flow-putaway-pick.md)
2.  Modtagelse og læg-på-lager-flere indgående ordrer på én gang med lagermodtagelse, afsende flere ordrer på én gang med en lagerleverance, plukke med lagerpluk med [gennemgang af indgående og udgående flow i blandede lager konfigurationer](warehousing/warehouse-mixed-flow-receive-pick-ship.md)
3.  Konfigurere faste placeringer for vareenhed, direkte afsendelse af brugere for at reducere varernes fysiske bevægelser, optimere varer med genopfyldnings opfyldning, nedbrydnings enheder til mindre enheder, fordele plukning blandt lagersteder med Plukkladde med [gennemgang af indgående og udgående flow i avanceret Lageropsætning med styret læg-på-lager og pluk](warehousing/warehouse-directed-flow.md)

Læs trinene for hvert scenarie i den relevante artikel.
   
## <a name="see-also" />Se også

[Produktion](../production-manage-manufacturing.md)  
[Lagersted](../warehouse-manage-warehouse.md)  

