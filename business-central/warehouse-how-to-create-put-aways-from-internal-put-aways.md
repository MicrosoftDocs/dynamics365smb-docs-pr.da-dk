---
title: Oprette læg-på-lager-aktiviteter fra interne læg-på-lager-aktiviteter
description: Dette emne beskriver, hvordan du plukker og lægger varer på lager uden et kildedokument, hvordan du opretter et internt pluk, og hvordan du opretter en intern læg-på-lager-aktivitet.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 7354, 7356, 7357, 7358, 7359, 7361
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: f812b988c0cb48cd49890c20ab59a8095327c52f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512572"
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
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Internt lagerpluk**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.
3. Udfyld feltet **Nummer**. feltet **Lokationskode** og feltet **Til placeringskode** i oversigtspanelet **Generelt**. Feltet **Til placeringskode** angiver den placering, hvor de plukkede varer skal hentes. I forbindelse med produktion er denne placering placeringen for indgående produktion eller åben produktion. I andre forbindelser skal du vælge en placeringskode med en placeringstype, som ikke bruges til pluk, sandsynligvis en leveranceplacering eller specialplacering.  
4.  Vælg en vare i feltet **Varenr.** , og indtast de antal, der skal plukkes.  
5. Vælg handlingen **Opret pluk**. Der er nu en lagerplukinstruktion klar til en lagermedarbejder. Alternativt kan du vælge handlingen **Frigiv** og oprette pluk (logistik) ved hjælp af **Plukkladde**. Du kan finde flere oplysninger i [Planlægge pluk i kladder](warehouse-how-to-plan-picks-in-worksheets.md)

## <a name="to-create-an-internal-put-away"></a>Sådan oprettes en intern læg-på-lager-aktivitet  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Intern læg-på-lager-aktivitet**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.
3. Udfyld hovedet for en ny intern læg-på-lager-aktivitet med **Nr.** og **Lokationskode**.
4. Udfyld en linje for hver vare, der skal flyttes til lagerstedet. Det er kun nødvendigt at udfylde felterne **Varenr.** og **Antal**.

  > [!NOTE]  
  > Når du vælger feltet **Varenr.**, åbnes vinduet **Placeringsindholdsoversigt** i stedet for **Vareoversigt**. Det er fordi, du lægger en vare på plads, der skal opbevares på en særlig placering - *Placeringsindhold* - ikke bare en vare, og du ved allerede, hvilken placering varen skal tags fra.  <!--If you filled in **From Bin Code** in the header, the bin content will be filtered by value defined in the **From Bin Code**.-->
5. For at udfylde kladdelinjerne med hele placeringsindholdet eller det filtrerede placeringsindhold for placeringer på lokationen skal du vælge handlingen **Hent placeringsindhold**.  
6. Vælg handlingen **Opret læg-på-lager**. Der er nu en læg-på-lager-instruktion klar til en lagermedarbejder. Alternativt kan du vælge handlingen **Frigiv** og oprette pluk (logistik) ved hjælp af **Plukkladde**. Du kan finde flere oplysninger i [Planlægge læg-på-lager-aktiviteter i kladder](warehouse-how-to-plan-put-aways-in-worksheets.md)

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
