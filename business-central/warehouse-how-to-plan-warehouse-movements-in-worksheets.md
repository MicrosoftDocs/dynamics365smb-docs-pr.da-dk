---
title: Sådan planlægges lagerbevægelser i kladder | Microsoft Docs
description: Planlæg bevægelser i en kladde vha. funktionen Placeringsgenopfyldning eller manuelt ved at planlægge de linjer, som du vil oprette bevægelsesinstruktioner til.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e779bb1d2916c031dea66a52ed7b3b9ccc006aee
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438153"
---
# <a name="plan-warehouse-movements-in-worksheets"></a>Planlægge lagerbevægelser i kladder
Planlæg bevægelser i en kladde vha. funktionen Placeringsgenopfyldning eller manuelt ved at planlægge de linjer, som du vil oprette bevægelsesinstruktioner til.  

## <a name="to-calculate-a-replenishment-movement"></a>Sådan beregnes placeringsgenopfyldning  
Efterhånden som lagerstedet afsender varer, bliver der færre og færre varer på placeringerne med de højeste placeringsniveauer. For at genopfylde disse placeringer med varer fra andre placeringer bruger du funktionen **Beregn genopfyldning** på siden **Bevægelseskladde**.

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bevægelseskladde**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Beregn genopfyldning**.  

    [!INCLUDE[prod_short](includes/prod_short.md)] opretter automatisk linjer, der præcist angiver, hvordan du skal flytte varer fra placeringer med lavt placeringsniveau til placeringer med højt placeringsniveau.  

    > [!NOTE]  
    >  Der foreslås en bevægelse i henhold til FEFO, når du aktiverer funktionen **Opret bevægelse**, hvis følgende betingelser er opfyldt for en vare:  
    >   
    >  -   Varen har en udløbsdato.  
    > -   Afkrydsningsfeltet **Vælg i overensstemmelse med FEFO** på lokationskortet er markeret.  
    > -   Afkrydsningsfeltet **Tvungen placering** på lokationskortet er markeret.  
    > -   Felterne **Fra zonekode** og **Fra placeringskode** er tomme.  

    Du kan finde flere oplysninger i [Plukke efter FEFO](warehouse-picking-by-fefo.md).  

3.  Kontroller linjerne, og ret dem efter behov, eller slet nogle af dem, hvis der ikke er tid nok til at udføre dem alle.  
4.  Vælg handlingen **Opret bevægelse** for at oprette en instruktion til lagermedarbejderne.  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a>Sådan kan du flytte hele indholdet af en eller flere placeringer ved hjælp af funktionen Hent placeringsindh.  
Du kan også bruge bevægelseskladden til at planlægge andre former for varebevægelser på lagerstedet. Hvis der f.eks. skal flyttes varer til en placering til kvalitetskontrol, kan du bruge bevægelseskladden til at planlægge handlingen og derefter oprette en bevægelse for at udarbejde instruktioner til en medarbejder.  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bevægelseskladde**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Hent placeringsindhold**. Du kan bruge anmodningssiden til at filtrere for de placeringer og varer, der skal vises på bevægelseskladdelinjerne.  
3.  Udfyld de relevante felter på kørselssiden. Hvis du f.eks. vil se placeringsindholdet af alle placeringer i en bestemt zone på en lokation, skal du udfylde feltet **Zonekode**. Hvis du vil hente linjerne for hver placering, der indeholder en bestemt vare, skal du udfylde feltet **Varenr.**.  

    > [!NOTE]  
    >  Du kan ikke manuelt flytte varer ind eller ud af en placering af typen MODTAG, fordi varer, der findes i en placering af typen MODTAG, skal registreres som lagt på lager, før de bliver en del af den tilgængelige lagerbeholdning.  

4.  Hvis du henter mange linjer, skal du vælge **Sorter** for at vælge en sorteringsmetode for de ordrelinjer, der vises i kladden, og derefter klikke på knappen **OK**.  

    > [!NOTE]  
    >  Bevægelseslinjer hentes i henhold til FEFO, når du aktiverer funktionen **Hent placeringsindh.**, hvis følgende betingelser er opfyldt for en vare:  
    >   
    >  -   Varen har en udløbsdato.  
    > -   Afkrydsningsfeltet **Vælg i overensstemmelse med FEFO** på lokationskortet er markeret.  
    > -   Afkrydsningsfeltet **Tvungen placering** på lokationskortet er markeret.  
    > -   Felterne **Fra zonekode** og **Fra placeringskode** er tomme.  

5.  Udfyld nogle af de hentede linjer, så de afspejler de ændringer, du vil foretage. Udfyld felterne **Varenr.**, **Fra placeringskode**, **Til placeringskode** og **Antal** for hver af de varer, du vil flytte.  
6.  Slet de ikke-udfyldte linjer, du har brugt til oplysninger.  
7.  Når bevægelseskladdelinjerne nøjagtigt beskriver, hvordan bevægelsen skal udføres af lagermedarbejderen, skal du vælge handlingen **Opret bevægelse** for at oprette instruktionerne til medarbejderen.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]