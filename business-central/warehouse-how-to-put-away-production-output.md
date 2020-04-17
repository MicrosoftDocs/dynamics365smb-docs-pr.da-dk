---
title: Sådan lægges produktionsafgange på lager | Microsoft Docs
description: Den måde, du lægger afgang på lager fra produktion, afhænger af, hvordan lagerstedet er sat op som en lokation.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e0acb1a8c1710b0b096c461f14f817957e4ee3af
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192863"
---
# <a name="put-away-production-or-assembly-output"></a>Lægge produktions- eller montageafgange på lager
Den måde, du lægger afgang på lager fra produktion, afhænger af, hvordan lagerstedet er sat op som en lokation. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).  

I grundlæggende lageropsætninger, hvor lokationen kræver læg-på-lager, men ikke modtagelse, skal du bruge dokumentet **Læg-på-lager (lager)** til at organisere og registrere afgangens læg-på-lager.  

I avancerede lageropsætninger, hvor lokationen kræver både læg-på-lager og modtagelse, kan du enten oprette et internt læg-på-lager-dokument eller et bevægelsesdokument for at lægge afgangen på lager.  

Det første trin til at lægge afgange på lager er at oprette den indgående lageranmodning. Denne anmodning oplyser lagerstedet om, at produktions- eller montageordreafgangen er klar til at blive lagt på lager.

## <a name="to-create-the-inbound-warehouse-request"></a>Sådan opretttes den indgående lageranmodning  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Frigivet produktionsordre**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Opret indgående lageranmodning** på den produktionsordre, der er klar til at blive lagt på lager.  

> [!NOTE]  
>  Du kan også oprette en indgående lageranmodning ved at markere afkrydsningsfeltet **Opret indgående anmodning**, når du opdaterer produktionsordren. Du kan finde flere oplysninger i [Forny eller omplanlægge produktionsordrer](production-how-to-replan-refresh-production-orders.md).  

## <a name="to-put-output-away-with-an-inventory-put-away"></a>Sådan lægges afgang på lager med en læg-på-lager-aktivitet  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Læg-på-lager**, og vælg derefter det relaterede link.  
2.  Opret en ny læg-på-lager-aktivitet. Du kan finde flere oplysninger i [Lægge varer på lager med Læg-på-lager](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Du kan få adgang til produktionsordreafgangen ved at vælge handlingen **Hent kildedokumenter** og derefter vælge den frigivne produktionsordre.  
4.  Udfyld læg-på-lager-linjerne efter behov.
5.  Når linjerne er klar til at blive bogført, skal du vælge handlingen **Bogfør**. Bogføringen opretter de nødvendige lagerposter og bogfører afgangen af varer.  

Du kan også oprette et **Læg-på-lager (lager)** direkte fra den frigivne produktionsordre. Du kan finde flere oplysninger i [Lægge varer på lager med Læg-på-lager](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Når du bogfører læg-på-lager, antages det, at alle operationer er bogført i overensstemmelse med standardruten, dvs., at afgangsantal er bogført i henhold til den seneste operation. Du kan bruge afgangskladde til at bogføre afvigelser i afgangsantal og opstillings- og operationstid. Hvis der er krav om delvis bogføring, efter du har oprettet læg-på-lager, kan du gøre dette under opstillingstid og antal for alle operationer undtagen den sidste. I det tilfælde kontrolleres den sidste operation af læg-på-lager.  

Hvis du kun har behov for at bogføre opstillings- og operationstid på den sidste operation, skal du angive afgangsantallet for den sidste operation til 0. Alternativt kan du vælge overhovedet ikke at bogføre den sidste linje ved simpelthen at slette den.  

## <a name="to-put-output-away-with-a-warehouse-internal-put-away"></a>Sådan lægges afgang på lager med en intern læg-på-lager-aktivitet
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Intern læg-på-lager-aktivitet**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.
3. Udfyld hovedet for en ny intern læg-på-lager-aktivitet med **Lokationskoden**.  
4. Udfyld en linje for hver vare, der skal flyttes til lagerstedet. Det er kun nødvendigt at udfylde felterne **Varenr.** og **Antal**.  

    > [!NOTE]  
    >  Når du vælger feltet **Varenr.**, åbnes vinduet **Placeringsindholdsoversigt** i stedet for **Vareoversigt**. Det er fordi, du lægger en vare på plads, der skal opbevares på en særlig placering ifølge det fastsatte placeringsindhold, og du ved allerede, hvilken placering varen skal tags fra.  

4.  For at udfylde kladdelinjerne med hele placeringsindholdet eller det filtrerede placeringsindhold for placeringer på lokationen skal du vælge handlingen **Hent placeringsindh.**.  
5.  Vælg handlingen **Opret læg-på-lager**. De varer, som du vil flytte fra produktionen, er nu angivet i læg-på-lager-instruktioner og venter på at blive lagt på plads på lagerstedet.  

> [!NOTE]  
>  Når lagerlokationen kræver styret læg-på-lager og pluk, er lagerstedet knyttet til produktionsfaciliteterne via standardproduktionsplaceringerne: de indgående og udgående produktionsplaceringer og den åbne produktion, som alle defineres i oversigtspanelet **Placeringer** på lokationskortet. Når du bogfører afgangen for en produktionsordre, anbringes afgangen på den **udgående produktionsplacering**. Du skal benytte samme fremgangsmåde som beskrevet ovenfor til at lægge produktionsafgangen på lager, bortset fra at i stedet for at bruge varens standardplacering skal du flytte eller lægge varerne på lager fra den **udgående produktionsplacering** til varens standardplacering.  

## <a name="to-manually-specify-a-bin-to-store-items-from-production-output"></a>Hvis du manuelt vil angive en placering til at gemme varerne fra produktionsafgang  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bevægelseskladde**, og vælg derefter det relaterede link.  
2.  Udfyld hovedet, og opret en linje for hver vare, der skal flyttes til lagerstedet.  
3.  Udfyld begge felterne **Fra placeringskode** og **Til placeringskode**, og indtast antal i feltet **Antal**.  
4.  For at udfylde kladdelinjerne med hele placeringsindholdet eller det filtrerede placeringsindhold for placeringer på lokationen skal du vælge handlingen **Hent placeringsindh.**.  
5. Vælg handlingen **Opret bevægelse**. Lagerbevægelsesinstruktionen oprettes med Hent- og Placer-linjer til lagermedarbejderne.  

> [!NOTE]  
>  Du kan ikke angive kildedokumentnummeret, f.eks. prod.ordrenr., i dokumenterne intern læg-på-lager, læg-på-lager eller bevægelse i disse to procedurer.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
