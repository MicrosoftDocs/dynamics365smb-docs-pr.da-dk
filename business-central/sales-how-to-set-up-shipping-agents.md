---
title: Sådan oprettes speditører
description: 'Få mere at vide om, hvordan du opretter en kode for hver speditør og angiver beskrivende oplysninger om hver af dem og de tjenester, de yder.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Oprette speditører
Du kan angive en kode for hver speditør og angive oplysninger om dem.  

Hvis du angiver en internetadresse for speditøren, og denne tilbyder pakkesporing over internettet, kan du anvende programmets automatiske pakkesporingsfunktion. Du kan finde flere oplysninger i [Spore pakker](sales-how-track-packages.md).

Når du angiver speditører i salgsordrerne, kan du også angive den service, som den enkelte speditør tilbyder.  
Du kan angive et ubegrænset antal serviceydelser for hver speditør, og du kan angive en transporttid for hver service.  

Når du har tilknyttet en speditørservice til salgsordrelinjen, medtages transporttiden for den pågældende service i beregningen af ordrebekræftelsen for linjen. Du kan finde flere oplysninger i [Beregne ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md).

## Sådan oprettes en speditør  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Speditører**, og vælg derefter det relaterede link.  
2.  Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Vælg handlingen **Speditørservice**.
4. I feltet **Speditørservice** skal du udfylde felterne efter behov.

> [!NOTE]  
>  Hvis du sletter speditøren på ordrelinjen, slettes speditørservicekoden også. Derefter beregnes oplysningerne i de felter, der er baseret på speditørservicen, igen.  

## Se også
[Oprette leveringsformer](sales-how-set-up-shipment-methods.md)  
[Spore pakker](sales-how-track-packages.md)    
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]