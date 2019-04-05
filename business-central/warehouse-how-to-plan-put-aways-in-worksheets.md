---
title: Sådan planlægges læg-på-lager-aktiviteter i kladder | Microsoft Docs
description: Hvis lokationen kræver både læg-på-lager og modtagelse, og du vil planlægge læg-på-lager-instruktioner til en række modtagelser – i stedet for at lade medarbejderne følge de instruktioner, der automatisk oprettes til separate bogførte modtagelser – kan du bruge læg-på-lager-kladden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: e0674c0c308cd83de8a6977e05445c22009f513c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792184"
---
# <a name="plan-put-aways-in-worksheets"></a>Planlægge læg-på-lager-aktiviteter i kladder
Hvis lokationen kræver både læg-på-lager og modtagelse, og du vil planlægge læg-på-lager-instruktioner til en række modtagelser – i stedet for at lade medarbejderne følge de instruktioner, der automatisk oprettes til separate bogførte modtagelser – kan du bruge læg-på-lager-kladden.  

Marker feltet **Brug læg-på-lager-kladde** i oversigtspanelet **Lager** på lokationskortet, hvis du vil sætte lageret op, så modtagelseslinjer bliver tilgængelige i læg-på-lager-kladden, så snart de er bogført. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).  

Hvis du ikke markerer feltet, oprettes der automatisk læg-på-lager-instruktioner for modtagelser, når disse bogføres.  

> [!NOTE]  
>  Uanset status for feltet **Brug læg-på-lager-kladde** på lokationskortet, kan du altid overføre læg-på-lager-instruktionslinjer, dvs. bogførte modtagelseslinjer, til læg-på-lager-kladden ved at gøre følgende:  
>   
>  1.  Tryk på siden **Læg-på-lager (logistik)** på Ctrl+D for at slette hele læg-på-lager-instruktionen, eller marker og slet de linjer, som du hellere vil behandle i kladden.  
> 2.  Fortsæt processen på så mange læg-på-lager-aktiviteter som ønsket, indtil du har slettet alle de linjer, som du vil arbejde med i kladden. Vælg derefter **Læg-på-lager-kladder**, og fortsæt med planlægningen der.  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a>Sådan planlægges instruktioner i læg-på-lager-kladden  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Læg-på-lager-kladde**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Hent lagerdokumenter**. Siden **Læg-på-lager-valg** åbnes.  

    Du kan se alle de bogførte modtagelser og registrerede interne læg-på-lager-aktiviteter, der er blevet overført til læg-på-lager-funktionen, herunder dem som der allerede er oprettet læg-på-lager-instruktioner til. Dokumenter med læg-på-lager-linjer, der fuldt ud er blevet lagt på plads og er blevet registreret, vises ikke i oversigten.  

3. Vælg de dokumenter, som du vil arbejde med i kladden. Du kan arbejde med linjer fra flere dokumenter samtidigt.  

    > [!NOTE]  
    >  Hvis du prøver at vælge et modtagelses- eller intern læg-på-lager-dokument, som der allerede er oprettet instruktioner for til samtlige linjer, får du besked på, at der ingenting er at håndtere.  

4. Udfyld feltet **Sorteringsmetode** for at sortere linjerne efter behov.  

    > [!NOTE]  
    >  Den måde, som linjerne er sorteret på i kladden, overføres ikke automatisk til læg-på-lager-instruktionen, men der er de samme muligheder for sortering og placeringsniveau. Du kan derfor nemt genskabe samme linjerækkefølge, når du opretter læg-på-lager-instruktionerne eller ved efterfølgende at sortere dem.  

5.  Udfyld feltet **Håndteringsantal**. Vælg handlingen **Autofyld håndteringsantal**, eller udfyld felterne manuelt.  
6.  Rediger eventuelt linjerne manuelt. Du kan også slette linjer, f.eks. hvis der er varer, der skal lægges på en placering, der ligger langt fra de andre placeringer.  

    > [!NOTE]  
    >  Linjerne slettes kun fra kladden, ikke fra læg-på-lager-oversigten.  

7.  Vælg handlingen **Opret læg-på-lager**. Siden **Opret dokument** åbnes, og her kan du tilføje flere oplysninger om den læg-på-lager-aktivitet, du opretter:  

    -   Du kan tildele læg-på-lager-aktiviteten til en bestemt medarbejder.  
    -   Du kan sortere læg-på-lager-instruktionslinjerne på samme måde som i kladden eller efter placeringsniveau. Hvis du sorterer efter placeringsniveau, står Hent-linjerne øverst, da de fleste modtagelsesplaceringer har et placeringsniveau på 0, og Placer-linjerne nederst, startende med de placeringer, der har det laveste placeringsniveau. Hvis lagerstedet er struktureret, så placeringer med omtrent samme placeringsniveau står ved siden af hinanden, vil en sådan sorteringsmetode spare tid for lagermedarbejderne.  
    -   Du kan vælge ikke at få vist de midlertidige linjer, der oprettes, når programmet opdeler en stor måleenhed i mindre enheder ved at markere feltet **Angiv nedbrydningsfilter**. Du kan finde flere oplysninger i [Aktivere automatisk nedbrydning med styret læg-på-lager og pluk](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    -   Du kan vælge, at feltet **Håndteringsantal** ikke skal udfyldes automatisk på læg-på-lager-instruktionerne.  
    -   Du kan vælge at få udskrevet dokumentet med det samme.  

8.  Klik på knappen **OK** for at oprette læg-på-lager-aktiviteten.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
