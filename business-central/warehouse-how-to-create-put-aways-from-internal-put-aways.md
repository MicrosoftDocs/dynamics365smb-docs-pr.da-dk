---
title: Sådan oprettes læg-på-lager-aktiviteter fra interne læg-på-lager-aktiviteter | Microsoft Docs
description: Når varer er blevet lagt på plads, og indtil de plukkes til en produktionsordre eller leverance, opbevares de på lagerstedet og indgår i den disponible lagerbeholdning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5095b4dde92b2d6982bfc8a984f10f5b62454800
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756238"
---
# <a name="pick-and-put-away-without-a-source-document"></a>Plukke og lægge på lager uden et kildedokument
Når varer er blevet lagt på plads, og indtil de plukkes til en produktionsordre eller leverance, opbevares de på lagerstedet og indgår i den disponible lagerbeholdning.  

Der kan være tilfælde, hvor varer midlertidigt fjernes fra lagerplaceringer, f.eks. fordi de skal fungere som demonstrationsvarer ved en salgspræsentation. Sådanne varer ejes stadig af virksomheden og er en del af lageret, men de er ikke tilgængelige til pluk. De registreres på en specialplacering, som du opretter til formålet; og er teknisk set stadig på lager, selvom de rent fysisk befinder sig på en messe eller i et demonstrationsrum.  

I andre situationer kan produktionsenheden mod forventning have brug for et par ekstra komponenter til en proces. Du kan plukke varer til produktionsplaceringer ved interne pluk. Når produktionen er færdig, og afgangen er oprettet, bogfører du forbruget af varerne og tømmer produktionsplaceringen, hvilket nedsætter antallet af varer på din lokation.  

På samme måde kan der returneres varer til lagerstedet for at blive lagt på plads. Varerne kan f.eks. være blevet taget fra den disponible beholdning til en produktionsordre, men alligevel ikke være brugt til formålet. De kan blive en del af den disponible beholdning igen, hvis du lægger dem på lager på placeringen.  

Ved hjælp af **Interne pluk**-aktiviteter kan du udføre læg-på-lager-aktiviteter uden at henvise til et bestemt kildedokument. Du kan nemt angive alle de nødvendige oplysninger til oprettelse af en lagerinstruktion.  

> [!NOTE]  
>  Hvis du ikke benytter interne pluk og interne læg-på-lager-aktiviteter, kan du udføre disse reguleringer ved hjælp af metoden til flytning af varer fra placering til placering eller til bogføring af mængdereguleringer på en placering.  
>   
>  Når lokationen bruger styret læg-på-lager og pluk og derfor placeringstyper, kan du ikke manuelt flytte varer ind eller ud af en placering af typen MODTAG, fordi varer, der findes på en placering af typen MODTAG, skal registreres som lagt på lager, før de bliver en del af den tilgængelige lagerbeholdning.  

## <a name="to-create-an-internal-pick"></a>Sådan oprettes et internt pluk  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Internt lagerpluk**, og vælg derefter det relaterede link.  
2.  Udfyld feltet **Nummer**. og **Til placeringskode** i oversigtspanelet **Generelt**. Feltet **Til placeringskode** angiver den placering, hvor varerne skal hentes. I forbindelse med produktion er denne placering placeringen for indgående produktion eller åben produktion. I andre forbindelser skal du vælge en Til placeringskode med en placeringstype, som ikke bruges til pluk, sandsynligvis en leveranceplacering eller specialplacering.  
3.  Vælg en vare i feltet **Varenr.** , og indtast de antal, der skal plukkes.  
4. Vælg handlingen **Opret pluk**. Der er nu en lagerplukinstruktion klar til en lagermedarbejder.  

## <a name="to-create-an-internal-put-away"></a>Sådan oprettes en intern læg-på-lager-aktivitet  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Intern læg-på-lager-aktivitet**, og vælg derefter det relaterede link.  
2.  Udfyld feltet **Nummer**. og **Fra placeringskode** i oversigtspanelet **Generelt**. Feltet **Fra placeringskode** angiver stedet for den placering, som varerne returneres fra til lagerstedet, f.eks. fra produktionsenheden.  
3.  Angiv varenumre og antal på linjerne.  
4.  Vælg handlingen **Opret læg-på-lager**. Der er nu en læg-på-lager-instruktion klar til en lagermedarbejder.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]