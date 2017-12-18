---
title: "Sådan oprettes læg-på-lager-aktiviteter fra interne læg-på-lager-aktiviteter | Microsoft Docs"
description: "Når varer er blevet lagt på plads, og indtil de plukkes til en produktionsordre eller leverance, opbevares de på lagerstedet og indgår i den disponible lagerbeholdning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2a6829c5a67f1121ecc135e1183af78b0e602f8f
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-pick-and-put-away-without-a-source-document"></a>Fremgangsmåde: Plukke og lægge på lager uden et kildedokument
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
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Internt lagerpluk**, og vælg derefter det relaterede link.  
2.  Udfyld feltet **Nummer**. og **Til placeringskode** i oversigtspanelet **Generelt**. Feltet **Til placeringskode** angiver den placering, hvor varerne skal hentes. I forbindelse med produktion er denne placering placeringen for indgående produktion eller åben produktion. I andre forbindelser skal du vælge en Til placeringskode med en placeringstype, som ikke bruges til pluk, sandsynligvis en leveranceplacering eller specialplacering.  
3.  Vælg en vare i feltet **Varenr.** , og indtast de antal, der skal plukkes.  
4. Vælg handlingen **Opret pluk**. Der er nu en lagerplukinstruktion klar til en lagermedarbejder.  

## <a name="to-create-an-internal-put-away"></a>Sådan oprettes en intern læg-på-lager-aktivitet  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Intern læg-på-lager (logistik)**, og vælg derefter det relaterede link.  
2.  Udfyld feltet **Nummer**. og **Fra placeringskode** i oversigtspanelet **Generelt**. Feltet **Fra placeringskode** angiver stedet for den placering, som varerne returneres fra til lagerstedet, f.eks. fra produktionsenheden.  
3.  Angiv varenumre og antal på linjerne.  
4.  Vælg handlingen **Opret læg-på-lager**. Der er nu en læg-på-lager-instruktion klar til en lagermedarbejder.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

