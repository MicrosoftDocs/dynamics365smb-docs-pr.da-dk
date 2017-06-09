---
title: "Fremgangsmåde: Oprette et brugerdefineret rapport- eller dokumentlayout | Microsoft Docs"
description: "Få mere at vide om, hvordan du kan designe udseendet af rapporter."
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
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 79c1e5c1ea01077e2e5012ba07618760ccf2a4af
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-create-a-custom-report-or-document-layout"></a>Fremgangsmåde: Oprette et brugerdefineret rapport- eller dokumentlayout
Som standard har en rapport et indbygget rapportlayout, som enten kan være et RDLC-rapportlayout eller Word-rapportlayout eller begge typer. Du kan ikke ændre indbyggede layout. Du kan dog oprette dine egne brugerdefinerede layout, der gør det muligt at ændre udseendet af rapporten, når den vises, udskrives eller gemmes. Du kan oprette flere brugerdefinerede rapportlayout til samme rapport og derefter skifte det layout, der bruges af en rapport, efter behov.

**Bemærk!** I [!INCLUDE[d365fin](includes/d365fin_md.md)] omfatter "rapporter" også eksternt orienterede dokumenter, f.eks. salgsfakturaer og ordrebekræftelser, som du sender til kunder som PDF-filer.

Hvis du vil oprette et brugerdefineret layout, kan du enten oprette en kopi af et eksisterende brugerdefineret layout eller tilføje et nyt brugerdefineret layout, som i de fleste tilfælde er baseret på et indbygget layout. Når du tilføjer et nyt brugerdefineret layout, kan du tilføje en RDLC-rapportlayouttype, Word-rapportlayouttype eller begge dele. Det nye brugerdefinerede layout vil automatisk blive baseret på det indbyggede layout for rapporten, hvis det findes. Hvis der er ingen indbyggede layout for typen, bliver et tomt layout oprettet, som du skal ændre og designe fra bunden. Find flere oplysninger om RDLC- og Word-rapportlayout, indbyggede og brugerdefinerede layout og mere under [Administration af rapportlayout](ui-manage-report-layouts.md).  

## <a name="to-create-a-custom-layout"></a>Sådan opretter du et brugerdefineret layout
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Search for Page or Report icon"), angive **Valg af rapportlayout** og derefter vælge det relaterede link.  
   Vinduet **Valg af rapportlayout** viser en liste over alle de rapporter, der er tilgængelige i det firma, der er angivet i feltet Virksomhed øverst i vinduet.
2. Indstil feltet **Virksomhed** til den virksomhed, hvor du vil oprette rapportlayoutet.
3. Vælg rækken med den rapport, du vil oprette layoutet for, og vælg derefter **Brugerdefinerede layout**.  
   Vinduet **Brugerdefinerede layout** vises med alle brugerdefinerede layout, der er tilgængelige for den valgte rapport.
4. Hvis du vil oprette en kopi af et eksisterende brugerdefineret layout, skal du vælge det eksisterende brugerdefinerede layout på listen og derefter vælge **Kopiér**.  
   Kopien af det brugerdefinerede layout vises i vinduet **Brugerdefinerede layout** og indeholder ordene Kopi af i feltet Beskrivelse.
5. Hvis du vil tilføje et nyt brugerdefineret layout, der er baseret på et indbygget layout, skal du gøre følgende:  
   1. Vælg **Ny**. Vinduet **Indsæt indbygget layout til en rapport** åbnes. Felterne **Id** og **Navn** udfyldes automatisk.
   2. Hvis du vil tilføje en brugerdefineret Word-rapportlayouttype, skal du markere afkrydsningsfeltet **Indsæt Word-layout**.
   3. Hvis du vil tilføje en brugerdefineret RDLC-rapportlayouttype, skal du markere afkrydsningsfeltet **Indsæt RDLC-layout**.
   4. Vælg knappen **OK**.  
      De nye brugerdefinerede layout vises i vinduet **Tilpassede rapportlayouts**. Hvis et nyt layout er baseret på et indbygget layout, så har den ordene **Kopi af et indbygget layout** i feltet **Beskrivelse**. Hvis der ikke var noget indbygget layout for rapporten, har det nye layout ordene **Nyt layout** i feltet **Beskrivelse**, fordi det brugerdefinerede layout er tomt.
6. Som standard er feltet **Virksomhedsnavn** tomt, hvilket betyder, at det brugerdefinerede layout bliver tilgængeligt for rapporten i alle firmaer. Hvis du kun vil gøre det brugerdefinerede layout tilgængeligt i en bestemt virksomhed, skal du vælge **Rediger** og derefter indstille feltet **Virksomhedsnavn** til den ønskede virksomhed.

## <a name="see-also"></a>Se også
[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Fremgangsmåde: Ændre, hvilket layout der aktuelt bruges i en rapport](ui-how-change-layout-currently-used-report.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

