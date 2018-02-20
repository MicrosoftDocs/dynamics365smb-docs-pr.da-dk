---
title: "Fremgangsmåde: Oprette placeringer | Microsoft Docs"
description: "Den mest effektive metode til at oprette lagerplaceringer er at generere grupper af tilsvarende placeringer i oprettelseskladden, men du kan også oprette placeringer enkeltvist."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f8cd19f97c530397dd6b499157e13340331aa3ba
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="create-bins"></a>Oprette placeringer
Den mest effektive metode til at oprette lagerplaceringer er at generere grupper af tilsvarende placeringer i oprettelseskladden, men du kan også oprette placeringer enkeltvist fra lokationskortet. Du kan også bruge en funktion i vinduet **Placeringsopr.kladde** til at oprette placeringer automatisk.  

## <a name="to-create-a-bin-from-the-location-card"></a>Sådan oprettes en placering ud fra lokationskortet  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg det relaterede link.  
2.  Marker den lokation, du vil oprette en placering fra, og vælg derefter handlingen **Placeringer**.  
3. Vælg handlingen **Ny**.
4. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Sådan oprettes individuelle placeringer i placeringsoprettelseskladden  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Placeringsopr.kladde**, og vælg det relaterede link.  
2.  Udfyld de felter på hver linje, der er nødvendige for at navngive og karakterisere de placeringer, som du opretter.  
3.  Vælg handlingen **Opret placeringer**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Sådan oprettes placeringer automatisk i oprettelseskladden  
Du skal på forhånd have taget stilling til, hvilken slags placeringer der er brug for på lagerstedet, og den mest praktiske varestrøm gennem lagerstedets fysiske struktur, før du begynder at oprette placeringer automatisk.  

> [!NOTE]  
>  Når du først har brugt en placering, kan du ikke slette den, medmindre den er tom. Hvis du på et tidspunkt vil indføre et andet navngivningssystem til placeringerne, kan du dog bruge omposteringskladden til faktisk at flytte varer til et nyt placeringssystem. Det er derfor bedst, hvis du får sat placeringerne op korrekt allerede fra begyndelsen.  

Hvis du vil arbejde med vinduet **Placeringsopr.kladde**, skal du være oprettet som lagermedarbejder på det sted, hvor placeringerne findes. Du kan finde flere oplysninger i [Definere lagermedarbejdere](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Placeringsopr.kladde**, og vælg det relaterede link.  
2.  Vælg handlingen **Beregn placeringer**.
3. I vinduet **Beregn placeringer** i feltet **Placeringsskabelonkode**, og vælg den placeringsskabelon, der skal bruges som model for de placeringer, som du opretter.
4.  Indtast en beskrivelse af placeringerne.  
5.  For at oprette placeringskoderne, skal du udfylde felterne **Fra nr.** og **Til nr.** i de tre kategorier, der vises i vinduet: **Hylde**, **Afsnit** og **Niveau.** Placeringskoden kan være på op til 20 tegn.  

    > [!NOTE]  
    >  Det antal tegn, som du har indtastet i de tre kategorier for et felt, f.eks. de tegn, som du har indtastet i de tre felter **Fra nr.**, plus eventuelle feltafgrænsere, skal være på 20 eller færre tegn.  

     Du kan bruge bogstaver i koden, men de anvendte bogstaver skal være de samme i felterne **Fra nr.** og **Til nr.** . Du kan f.eks. definere kodens hyldedel som **Fra nr. A01** og **Til nr. A10**. Programmet er ikke designet til at generere koder med bogstavserier, f.eks. fra A01 til F05.  

6.  Hvis du vil bruge et tegn, f.eks. bindestreg, til at adskille de kategorifelter, som du har defineret som en del af placeringskoden, skal du angive tegnet i feltet **Feltafgrænser**.  
7.  Marker feltet **Kontroller eksist. plac.**, hvis du ikke ønsker, at programmet skal oprette en linje for en placering, hvis denne allerede findes.  
8. Vælg knappen **OK**, når du er færdig med at udfylde felterne.

    Der oprettes en linje for hver placering i kladden. Du kan slette nogle af placeringerne, f.eks. hvis adgangen til en hylde er spærret.  

9. Vælg handlingen **Opret placeringer**, når du har slettet alle de unødvendige placeringer. Der oprettes nu placeringer for hver linje i kladden.  

Gentag processen, hvis det er nødvendigt med endnu et sæt placeringer, indtil du har oprettet alle placeringerne på lagerstedet.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

