---
title: "Ompostering af anlægsaktiver | Microsoft Docs"
description: "Du omposterer et anlægsaktiv for at overføre det til en anden afdeling, opdele det eller kombinere det med andre anlægsaktiver."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a1db22bc990fc6438a11515f87f930be1eff252
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-split-or-combine-fixed-assets"></a>Overføre, opdele eller kombinere anlægsaktiver
Anlægsomposteringskladden bruges til at overføre, opdele og kombinere anlægsaktiver. Du kan få vist eller udskrive resultaterne af anlægsompostering med rapporten **Anlæg - bogført værdi 02**.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>Overføre et anlægsaktiv til en anden afdeling
Du kan overføre et anlægsaktiv til en anden afdeling, når du f.eks. placerer et aktiv i produktionsafdelingen, mens det er under opførelse, og derefter flytte det til administrationsafdelingen, når det er færdigbygget.  

1. Definer et nyt anlæg. Angiv den nye afdeling i feltet **Afdelingskode**.
2. Tildele en anlægsafskrivningsprofil til det nye anlægsaktiv. Du kan finde flere oplysninger i [Anskaffe anlægsaktiver](fa-how-acquire.md).
3. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omposteringskladder**, og vælg derefter det relaterede link.
4. Opret en omposteringskladde, hvor feltet **Anlægsnr.** viser det oprindelige anlægsaktiv, og feltet **Nyt anlægsnr.** indeholder det nye anlægsaktiv, der skal flyttes.  
5. Vælg handlingen **Ompostér**.

    Der oprettes nu to linjer i anlægskassekladden ved hjælp af den type og det navn, du har angivet i vinduet **Anlægskladdeopsætning** for den angivne afskrivningsprofil. Du kan finde flere oplysninger i [Konfigurere afskrivning af anlægsaktiver](fa-how-setup-depreciation.md).
6. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægsfinanskladder**, og vælg derefter det relaterede link.    
7. I vinduet **Anlægskassekladde** skal du vælge handlingen **Bogfør** for at bogføre den ompostering, du har udført i trin 4 og 5.

Hvis du har bogført en anskaffelsespris for ét anlæg, kan du bruge anlægsomposteringskladden til at opdele anskaffelsesprisen på flere anlægsaktiver.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>Sådan opdeles et anlægsaktiv i tre anlægsaktiver
Du kan opdele et anlægsaktiv i flere anlægsaktiver, f.eks. når du skal fordele et anlægsaktiv på tre forskellige afdelinger. I så fald kan du f.eks. flytte 25 procent af anskaffelsesprisen og afskrivningen for det oprindelige anlæg til det andet anlæg og 45 procent til det tredje anlæg. De resterende 30 procent bliver hos det oprindelige anlægsaktiv.

1. Definer to nye anlægsaktiver. Angiv den nye afdeling i feltet **Afdelingskode**.
2. Tildele anlægsafskrivningsprofiler til de nye anlægsaktiver. Du kan finde flere oplysninger i [Anskaffe anlægsaktiver](fa-how-acquire.md).
3. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omposteringskladder**, og vælg derefter det relaterede link.
4. Opret to omposteringskladdelinjer, én for hvert nyt anlægsaktiv.
5. På den første linje skal du angive det andet anlægsaktiv i feltet **Nyt anlægsnr.** og 25 i feltet **Ompost.pct. (anskaffelse)**.
6. På den anden linje skal du angive det tredje anlægsaktiv i feltet **Nyt anlægsnr.** og 40 i feltet **Ompost.pct. (anskaffelse)**.
7. På begge linjer skal du markere afkrydsningsfelterne **Omposter anskaffelse** og **Omposter afskrivning**.   
8. Vælg handlingen **Ompostér**.

    Der oprettes nu to linjer i anlægskassekladden ved hjælp af den type og det navn, du har angivet i vinduet **Anlægskladdeopsætning** for den angivne afskrivningsprofil. Du kan finde flere oplysninger i [Konfigurere afskrivning af anlægsaktiver](fa-how-setup-depreciation.md).    
9. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægsfinanskladder**, og vælg derefter det relaterede link.
10. I vinduet **Anlægskassekladde** skal du vælge handlingen **Bogfør** for at bogføre den ompostering, du har udført i trin 4-8.

## <a name="to-combine-two-fixed-assets-into-one"></a>Sådan kombineres to anlægsaktiver til ét
Du kan kombinere flere anlægsaktiver til ét anlægsaktiv, f.eks. når du skal flytte fordelte anlægsaktiver til en enkelt afdeling. Hvis du har bogført anskaffelsesprisen og afskrivningen for det anlægsaktiv, der skal flyttes, kombineres værdierne i det enkelte anlægsaktiv.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omposteringskladder**, og vælg derefter det relaterede link.
2. Opret en omposteringskladde, hvor feltet **Anlægsnr.** viser det oprindelige anlægsaktiv, der skal flyttes/kombineres, og feltet **Nyt anlægsnr.** indeholder det nye anlægsaktiv, det skal kombineres med.
3. Lad feltet **Ompost.pct. (anskaffelse)** være tomt for at flytte/kombinere hele anskaffelsesprisen.    
4. Markér afkrydsningsfelterne **Omposter anskaffelse** og **Omposter afskrivning**.
5. På fanen **Handlinger** skal du vælge **Omposter**.

    Der oprettes nu to linjer i anlægskassekladden ved hjælp af den type og det navn, du har angivet i vinduet **Anlægskladdeopsætning** for den angivne afskrivningsprofil. Du kan finde flere oplysninger i [Konfigurere afskrivning af anlægsaktiver](fa-how-setup-depreciation.md).   
6. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægsfinanskladder**, og vælg derefter det relaterede link.
7. I vinduet **Anlægskassekladde** skal du vælge handlingen **Bogfør** for at bogføre den ompostering, du har udført i trin 2-5.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>Sådan får du vist ændrede bogførte afskrivningsværdier på grund af ompostering af anlægsaktiver
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlæg - bogført værdi 02**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.
3. Vælg knappen **Udskriv** eller **Vis udskrift**.  

## <a name="see-also"></a>Se også
[Anlægsaktiver](fa-manage.md)  
[Opsætning af anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Introduktion](product-get-started.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

