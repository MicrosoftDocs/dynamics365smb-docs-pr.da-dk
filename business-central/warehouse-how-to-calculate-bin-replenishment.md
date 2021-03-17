---
title: Sådan beregnes genopfyldning | Microsoft Docs
description: Når lokationen er konfigureret til at bruge styret læg-på-lager og pluk, tages prioriteterne i læg-på-lager-skabelonen for lokationen i betragtning, når leverancer lægges på lager.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d2b00766cb01a41678b3e39f361e550de8cf8132
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391970"
---
# <a name="calculate-bin-replenishment"></a>Beregn genopfyldning
Når lokationen er konfigureret til at bruge styret læg-på-lager og pluk, tages prioriteterne i læg-på-lager-skabelonen for lokationen i betragtning, når leverancer lægges på lager. Prioriteter omfatter de minimale og maksimale mængder af placeringsindhold, der er fastsat for en bestemt placering og placeringsniveauerne. Hvis varerne ankommer i en stadig strøm, fyldes de oftest benyttede plukplaceringer derfor op, efterhånden som de tømmes.  

Men lagervarer ankommer ikke altid i en stadig strøm. Nogle gange købes varer i store mængder, så virksomheden kan få en rabat, eller en produktionsenhed kan give mange af ét element for at opnå en lav kostpris. Derefter vil varer ikke blive modtaget på lageret igen i et stykke tid, og lageret skal med jævne mellemrum flytte varer til plukplaceringer fra massevarelageret.  

Det kan også være, at lagerstedet vil foregribe modtagelsen af nye varer ved at tømme massevarelageret for varer, før de nye varer ankommer.  

Hvis du udelukkende har fastsat placeringstypen for massevareplaceringer til **Læg-på-lager**, dvs. at handlingen **Pluk** ikke er markeret for placeringstypen, skal du altid sørge for, at plukplaceringerne genopfyldes, da typen Læg-på-lager ikke er foreslået for et pluk fra placeringer.  

## <a name="to-replenish-pick-bins"></a>Sådan genopfyldes plukplaceringer  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bevægelseskladde**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Beregn genopfyldning** for at åbne rapportanmodningssiden.  
3.  Udfyld de relevante felter på siden for at begrænse omfanget af genopfyldningsforslag, der skal beregnes. Det kan f.eks. være, at du kun vil have forslag, der berører bestemte varer, zoner eller placeringer.  
4.  Vælg knappen **OK**. Der oprettes nu linjer for de genopfyldningsbevægelser, der skal udføres ifølge de regler, der er defineret for placeringer og placeringsindhold varerne på placeringerne.  
5.  Vælg handlingen **Opret bevægelse**, hvis du vil udføre alle de foreslåede genopfyldninger. Der er nu oprettet instruktioner i menuen **Bevægelser**, som kan udføres og registreres af lagermedarbejderne.  
6.  Hvis du kun vil have udført nogle af forslagene, skal du slette de mindst vigtige og derefter oprette en bevægelse.  

Næste gang du beregner genopfyldning, vil de forslag, som du har slettet, blive genoprettet, hvis de stadig er gyldige til den tid.  

> [!NOTE]  
>  Hvis en vare opfylder følgende betingelser:  
>   
>  -   Varen har en udløbsdato.  
> -   Feltet **Vælg i overensstemmelse med FEFO** på lokationskortet er markeret, og  
> -   Du bruger funktionen **Beregn genopfyldning**  
>   
>  Hvis alle disse betingelser er opfyldt, vil felterne **Fra zonekode** og **Fra placeringskode** være tomme, fordi den algoritme, der beregner, hvorfra varerne skal bevæges, kun udløses, når du aktiverer funktionen **Opret bevægelse**.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Plukke efter FEFO](warehouse-picking-by-fefo.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]