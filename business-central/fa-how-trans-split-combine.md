---
title: Genklassificere anlægsaktiver
description: Du omposterer et anlægsaktiv for at overføre det til en anden afdeling, opdele det eller kombinere det med andre anlægsaktiver.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5638, 5636, 5640, 5637
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 48f2735c39c3630611abcb785efc67cfd9473671
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511125"
---
# <a name="transfer-split-or-combine-fixed-assets"></a>Overføre, opdele eller kombinere anlægsaktiver

Anlægsomposteringskladden bruges til at overføre, opdele og kombinere anlægsaktiver. Du kan få vist eller udskrive resultaterne af anlægsompostering med rapporten **Anlæg - bogført værdi 02**.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>Overføre et anlægsaktiv til en anden afdeling

Du kan overføre et anlægsaktiv til en anden afdeling, når du f.eks. placerer et aktiv i produktionsafdelingen, mens det er under opførelse, og derefter flytte det til administrationsafdelingen, når det er færdigbygget.  

1. Definer et nyt anlæg. Angiv den nye afdeling som en dimension.  
2. Tildele en anlægsafskrivningsprofil til det nye anlægsaktiv. Du kan finde flere oplysninger i [Anskaffe anlægsaktiver](fa-how-acquire.md).
3. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsomposteringskladder**, og vælg derefter det relaterede link.
4. Opret en kladdelinje, hvor feltet **Anlægsnr.** viser det oprindelige anlægsaktiv, og feltet **Nyt anlægsnr.** indeholder det nye anlægsaktiv, der skal flyttes. Udfyld de andre felter efter behov.  
5. Vælg handlingen **Ompostér**.

    Der oprettes nu to linjer i anlægskassekladden ved hjælp af den type og det navn, du har angivet på siden **Anlægskladdeopsætning** for den angivne afskrivningsprofil. Du kan finde flere oplysninger i [Konfigurere afskrivning af anlægsaktiver](fa-how-setup-depreciation.md).
6. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsfinanskladder**, og vælg derefter det relaterede link.    
7. På siden **Anlægskassekladde** skal du vælge handlingen **Bogfør** for at bogføre den ompostering, du har udført i trin 4 og 5.

Hvis du har bogført en anskaffelsespris for ét anlæg, kan du bruge anlægsomposteringskladden til at opdele anskaffelsesprisen på flere anlægsaktiver.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>Sådan opdeles et anlægsaktiv i tre anlægsaktiver
Du kan opdele et anlægsaktiv i flere anlægsaktiver, f.eks. når du skal fordele et anlægsaktiv på tre forskellige afdelinger. I så fald kan du f.eks. flytte 25 procent af anskaffelsesprisen og afskrivningen for det oprindelige anlæg til det andet anlæg og 45 procent til det tredje anlæg. De resterende 30 procent bliver hos det oprindelige anlægsaktiv.

1. Definer to nye anlægsaktiver. Angiv de relevante afdelinger som dimensioner.  
2. Tildele anlægsafskrivningsprofiler til de nye anlægsaktiver. Du kan finde flere oplysninger i [Anskaffe anlægsaktiver](fa-how-acquire.md).
3. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsomposteringskladder**, og vælg derefter det relaterede link.
4. Opret to omposteringskladdelinjer, én for hvert nyt anlægsaktiv.
5. På den første linje skal du angive det andet anlægsaktiv i feltet **Nyt anlægsnr.** og 25 i feltet **Ompost.pct. (anskaffelse)**.
6. På den anden linje skal du angive det tredje anlægsaktiv i feltet **Nyt anlægsnr.** og 40 i feltet **Ompost.pct. (anskaffelse)**.
7. På begge linjer skal du markere afkrydsningsfelterne **Omposter anskaffelse** og **Omposter afskrivning**.  
8. Vælg handlingen **Ompostér**.  

    Der oprettes nu to linjer i anlægskassekladden ved hjælp af den type og det navn, du har angivet på siden **Anlægskladdeopsætning** for den angivne afskrivningsprofil. Du kan finde flere oplysninger i [Konfigurere afskrivning af anlægsaktiver](fa-how-setup-depreciation.md).    
9. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsfinanskladder**, og vælg derefter det relaterede link.
10. På siden **Anlægskassekladde** skal du vælge handlingen **Bogfør** for at bogføre den ompostering, du har udført i trin 4 til 8.

## <a name="to-combine-two-fixed-assets-into-one"></a>Sådan kombineres to anlægsaktiver til ét

Du kan kombinere flere anlægsaktiver til ét anlægsaktiv, f.eks. når du skal flytte fordelte anlægsaktiver til en enkelt afdeling. Hvis du har bogført anskaffelsesprisen og afskrivningen for det anlægsaktiv, der skal flyttes, kombineres værdierne i det enkelte anlægsaktiv.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsomposteringskladder**, og vælg derefter det relaterede link.
2. Opret en omposteringskladde, hvor feltet **Anlægsnr.** viser det oprindelige anlægsaktiv, der skal flyttes/kombineres, og feltet **Nyt anlægsnr.** indeholder det nye anlægsaktiv, det skal kombineres med.
3. Lad feltet **Ompost.pct. (anskaffelse)** være tomt for at flytte/kombinere hele anskaffelsesprisen.  
4. Markér afkrydsningsfelterne **Omposter anskaffelse** og **Omposter afskrivning**.
5. Vælg handlingen **Ompostér**.

    Der oprettes nu to linjer i anlægskassekladden ved hjælp af den type og det navn, du har angivet på siden **Anlægskladdeopsætning** for den angivne afskrivningsprofil. Du kan finde flere oplysninger i [Konfigurere afskrivning af anlægsaktiver](fa-how-setup-depreciation.md).   
6. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskasseklader**, og vælg derefter det relaterede link.
7. På siden **Anlægskassekladde** skal du vælge handlingen **Bogfør** for at bogføre den ompostering, du har udført i trin 2 til 5.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>Sådan får du vist ændrede bogførte afskrivningsværdier på grund af ompostering af anlægsaktiver

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlæg - bogført værdi 02**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.
3. Vælg knappen **Udskriv** eller **Vis udskrift**.  

## <a name="see-also"></a>Se også

[Anlægsaktiver](fa-manage.md)  
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]