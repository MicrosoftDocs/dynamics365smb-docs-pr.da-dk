---
title: Ændre udseendet af en rapport ved at vælge et andet layout | Microsoft Docs
description: Du kan bruge forskellige layout til en rapport og skifte mellem layout for at ændre udseendet af en rapport.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 07de4be7bc516cf9f4b802a48dc59293b1992f5f
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315248"
---
# <a name="change-the-current-report-layout"></a>Ændre det aktuelle rapportlayout
En rapport kan konfigureres med flere rapportlayout, som du kan skifte mellem efter behov.

Afhængig af de layout, der er tilgængelige for en rapport, kan du vælge at bruge et indbygget RDLC-rapportlayout, et indbygget Word-rapportlayout eller et brugerdefineret layout. Find flere oplysninger om RDLC- og Word-rapportlayout, indbyggede og brugerdefinerede layout og mere under [Administration af rapportlayout](ui-manage-report-layouts.md).

> [!TIP]  
> Rapporter af typen dokument (ikke lister), der bruger et Word-rapportlayout, er typisk hurtigere end dem, der bruger et RDLC-rapportlayout. Så hvis du har mulighed for at vælge mellem et Word- eller et RDLC-rapportlayout for en rapport af typen dokument, skal du bruge Word-rapportlayoutet til at få den bedste ydeevne.  

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Sådan ændrer du layoutet, der bruges i en rapport
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Valg af rapportlayout**, og vælg derefter det relaterede link.  
   Siden **Valg af rapportlayout** viser en liste over alle de rapporter, der er tilgængelige i det firma, der er angivet i feltet Virksomhed øverst på siden. Feltet Valgt layout angiver det layout, der aktuelt bruges af rapporten.
2. Angiv feltet **Virksomhed** øverst på siden til det firma, der indeholder rapporten.
3. Hvis du vil ændre layoutet for en rapport, skal du i rækken for rapporten på listen angive feltet **Valgt layout** til en af følgende indstillinger:
   * RDLC (indbygget), bruger det indbyggede RDLC-rapportlayout i rapporten.
   * Word (indbygget), bruger det indbyggede Word-rapportlayout i rapporten.
   * Brugerdefineret, bruger et brugerdefineret layout i rapporten.  

Du kan se, hvilke brugerdefinerede layout der er tilgængelige for rapporten i faktaboksen **Rapportlayoutdel**. Hvis der ikke er nogen brugerdefinerede layout for rapporten, skal du først oprette ét. Hvis du vælger denne indstilling, kan du gå til den næste procedure for at angive et brugerdefineret layout, du vil bruge.

> [!NOTE]
> Hvis du vælger **RDLC (indbygget)** eller **Word (indbygget)** , og du får en fejlmeddelelse om, at rapporten ikke har et layout med den angivne type, skal du vælge en anden layoutindstilling eller oprette en brugerdefineret rapport af den type, du vil bruge.

Hvis du har valgt et indbygget RDLC- eller Word-rapportlayout, kræves ingen yderligere handling, og layoutet bruges, næste gang rapporten køres.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Sådan angiver du et brugerdefineret layout i en rapport
1. Du kan angive, hvilket brugerdefinerede layout der skal bruges i rapporten, fra siden **Tilpassede rapportlayouts**. Hvis siden **Tilpassede rapportlayouts** ikke er åbent, skal du i feltet **Beskrivelse af rapportlayout** klikke på opslagsknappen.
2. Brug siden **Tilpassede rapportlayouts** til at vælge rækken med det brugerdefinerede layout, du vil bruge, og luk derefter siden.

Du kommer tilbage til siden **Valg af rapportlayout**. Navnet på det valgte brugerdefinerede layout vises i feltet **Beskrivelse af brugerdefineret layout**. Det brugerdefinerede layout, der skal bruges, næste gang du kører rapporten.

## <a name="see-also"></a>Se også
[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
