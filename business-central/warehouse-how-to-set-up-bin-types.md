---
title: Sådan oprettes placeringstyper | Microsoft Docs
description: Du kan dirigere varestrømmen til placeringer, som du har defineret til særlige lageraktiviteter. Du fastsætter disse aktiviteter ved at tildele placeringstyper, så du angiver, hvordan en placering skal brues.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c0339ec5d008f5994d64cf6162feda8144d06a67
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310200"
---
# <a name="set-up-bin-types"></a>Oprette placeringstyper
Du kan dirigere varestrømmen til placeringer, som du har defineret til særlige lageraktiviteter. Du fastsætter disse aktiviteter ved at tildele placeringstyper, så du angiver, hvordan en placering skal brues.  

Der er seks typer. Du kan bruge alle de seks mulige placeringstyper til lagerstedet, eller du kan vælge kun at operere med placeringstyperne MODTAG, LPLPLUK, LEVER og KK. Disse fire placeringstyper giver mulighed for forslag til aktiviteter og sætter dig i stand til at registrere afvigelser i lagerbeholdningen.  

## <a name="to-set-up-the-bin-types-you-want-to-use"></a>Sådan angives de placeringstyper, der skal bruges  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Placeringstyper**, og vælg derefter det relaterede link.  
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
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
