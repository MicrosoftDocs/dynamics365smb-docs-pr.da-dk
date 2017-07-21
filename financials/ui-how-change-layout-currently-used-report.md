---
title: "Ændre udseendet af en rapport ved at vælge et andet layout | Microsoft Docs"
description: "Du kan bruge forskellige layout til en rapport og skifte mellem layout for at ændre udseendet af en rapport."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: de0c429e8a5e03124c5a20977a9723570879952a
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-change-which-layout-is-currently-used-on-a-report"></a>Fremgangsmåde: Ændre, hvilket layout der aktuelt bruges i en rapport
En rapport kan konfigureres med flere rapportlayout, som du kan skifte mellem efter behov.

Afhængig af de layout, der er tilgængelige for en rapport, kan du vælge at bruge et indbygget RDLC-rapportlayout, et indbygget Word-rapportlayout eller et brugerdefineret layout. Find flere oplysninger om RDLC- og Word-rapportlayout, indbyggede og brugerdefinerede layout og mere under [Administration af rapportlayout](ui-manage-report-layouts.md).

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Sådan ændrer du layoutet, der bruges i en rapport
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Search for Page or Report icon"), angiv **Valg af rapportlayout**, og vælg derefter det relaterede link.  
   Vinduet **Valg af rapportlayout** viser en liste over alle de rapporter, der er tilgængelige for det firma, der er angivet i feltet Virksomhed øverst i vinduet. Feltet Valgt layout angiver det layout, der aktuelt bruges af rapporten.
2. Angiv feltet **Virksomhed** øverst i vinduet til det firma, der indeholder rapporten.
3. Hvis du vil ændre layoutet for en rapport, skal du i rækken for rapporten på listen angive feltet **Valgt layout** til en af følgende indstillinger:
   * RDLC (indbygget), bruger det indbyggede RDLC-rapportlayout i rapporten.
   * Word (indbygget), bruger det indbyggede Word-rapportlayout i rapporten.
   * Brugerdefineret, bruger et brugerdefineret layout i rapporten.  
     Du kan se, hvilke brugerdefinerede layout der er tilgængelige for rapporten i faktaboksen Rapportlayoutdel. Hvis der ikke er nogen brugerdefinerede layout for rapporten, skal du først oprette ét. Hvis du vælger denne indstilling, kan du gå til den næste procedure for at angive et brugerdefineret layout, du vil bruge.
     > [!NOTE]  
>   Hvis du vælger **RDLC (indbygget)** eller **Word (indbygget)** , og du får en fejlmeddelelse om, at rapporten ikke har et layout med den angivne type, skal du vælge en anden layoutindstilling eller oprette en brugerdefineret rapport af den type, du vil bruge.

Hvis du har valgt et indbygget RDLC- eller Word-rapportlayout, kræves ingen yderligere handling, og layoutet bruges, næste gang rapporten køres.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Sådan angiver du et brugerdefineret layout i en rapport
1. Du kan angive, hvilket brugerdefinerede layout der skal bruges i rapporten, fra vinduet **Tilpassede rapportlayouts**. Hvis vinduet **Tilpassede rapportlayouts** ikke er åbent, skal du i feltet **Beskrivelse af rapportlayout** klikke på opslagsknappen.
2. Brug vinduet **Tilpassede rapportlayouts** til at vælge rækken med det brugerdefinerede layout, du vil bruge, og luk derefter vinduet.

Du kommer tilbage til vinduet **Valg af rapportlayout**. Navnet på det valgte brugerdefinerede layout vises i feltet **Beskrivelse af brugerdefineret layout**. Det brugerdefinerede layout, der skal bruges, næste gang du kører rapporten.

## <a name="see-also"></a>Se også
[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

