---
title: Oprette placeringstyper
description: Tildel typer og grundlæggende flowaktiviteter til placeringer, og definer dermed, hvordan placeringerne skal bruges til bestemte lageraktiviteter.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7367
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 8fb409e9ca0a8540fa2ea997faae790f78086d6e
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520044"
---
# <a name="set-up-bin-types"></a>Oprette placeringstyper
Du kan dirigere varestrømmen til placeringer, som du har defineret til særlige lageraktiviteter. Du fastsætter disse aktiviteter ved at tildele placeringstyper, så du angiver, hvordan en placering skal bruges.  

Der er seks typer. Du kan bruge alle de seks mulige placeringstyper til lagerstedet, eller du kan vælge kun at operere med placeringstyperne MODTAG, LPLPLUK, LEVER og KK. Disse fire placeringstyper giver mulighed for forslag til aktiviteter og sætter dig i stand til at registrere afvigelser i lagerbeholdningen.  

## <a name="to-set-up-the-bin-types-you-want-to-use"></a>Sådan angives de placeringstyper, der skal bruges  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Placeringstyper**, og vælg derefter det relaterede link.  
2.  Angiv en kode på ti tegn for placeringstypen på siden **Placeringstyper**.  
3.  Marker de aktiviteter, der kan udføres for hver placeringstype.  

> [!NOTE]  
>  Placeringstyper er kun tilgængelige, hvis du bruger styret læg-på-lager og pluk til lokationen.  

Placeringstypen angiver, hvordan en placering skal bruges, når varestrømmen behandles på lagerstedet. Du kan til enhver tid tilsidesætte de forslag for hvert lagerdokument, og du kan altid flytte varer til eller fra en placering ved at foretage en lagerbevægelse.  

De placeringstyper, som du kan oprette, er angivet nedenfor.  

|Placeringstype|Beskrivelse|  
|------------------|---------------------------------------|  
|MODTAG|Varer, der er registreret som bogførte modtagelser, men endnu ikke er lagt på lager.|  
|LEVER|Varer, der er plukket til lagerleverancelinjer, men som endnu ikke er bogført som leveret.|  
|LGT-PÅ-LGR|Typisk varer, der skal opbevares i store måleenheder, men som du ikke ønsker, der skal oprettes pluk af. Da der ikke plukkes fra disse placeringer, hverken til produktionsordrer eller leverancer, kan brugen af placeringer af typen Læg-på-lager være begrænset, men denne type placering kan være nyttig, hvis du har købt en stort antal varer. Placeringer af denne type skal altid have et lavt placeringsniveau, hvilket medfører, at når modtagne varer lægges på lager, lægges andre først på lager på placeringer af typen LPLPLUK med et højere niveau, og som er fast tilknyttet varen. Hvis du bruger denne type placering, skal du regelmæssigt udføre placeringsgenopfyldning, så de varer, der opbevares på disse placeringer, også er tilgængelige på placeringer af typen LPLPLUK eller PLUK.|  
|PLUK|Varer, der udelukkende skal anvendes til pluk, f.eks. varer, hvor udløbsdatoen nærmer sig, og som du har flyttet til denne type placering. Der skal typisk angives et højt placeringsniveau til disse placeringer, så de foreslås til plukning først.|  
|LPLPLUK|Varer på placeringer, der foreslås for både læg-på-lager og pluk-funktioner. Placeringer af denne type har som regel forskellige placeringsniveau. Du kan fastsætte massevareplaceringer til denne placeringstype og give dem lave placeringsniveauer sammenlignet med de almindelige plukplaceringer eller forreste placeringer i plukområdet.|  
|KK|Denne placering bruges til lagerreguleringer, hvis du angiver placeringen i feltet **Reguleringsplaceringskode** på lokationskortet. Du kan også bruge denne type placeringer til defekte varer og varer, der skal kontrolleres. Du kan flytte varer til den type placering, hvis du ikke vil have, at de indgår i den normale varestrøm.<br /><br /> **BEMÆRK!** I modsætning til alle andre placeringstyper har placeringstypen **KK** ingen af afkrydsningsfelterne til håndtering af varen markeret som standard. Dette angiver, at ethvert indhold, du placerer i en KK-placering er udelukket fra vareforløb.|  

## <a name="see-also"></a>Se også
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
