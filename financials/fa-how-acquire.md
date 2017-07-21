---
title: "Anskaffe anlægsaktiver | Microsoft Docs"
description: "Du kan oprette et anlægsaktiv, tildele en afskrivningsprofil og registrere anlægsaktivets anskaffelsespris."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 903c1a858fe66482cb4404e8b792abade6106489
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-acquire-fixed-assets"></a>Fremgangsmåde: Anskaffe anlægsaktiver
For hvert anlægsaktiv skal du definere et kort med oplysninger om aktivet. Du kan angive bygninger eller produktionsudstyr som et hovedanlæg med en komponentliste, og du kan gruppere dem på forskellige måder, f.eks efter art, afdeling eller lokation. Der skal oprettes en afskrivningsprofil, og den skal tildeles til hvert enkelt anlægsaktiv, før du kan hente det.

Når der er oprettet et anlægsaktiv, og der er tildelt en afskrivningsprofil, skal du anskaffe anlægsaktivet. For at få et anlægsaktiv skal du registrere dens anskaffelsespris i den relevante finanskonto, bankkonto eller leverandør ved at bogføre en anskaffelsestransaktion fra vinduet **Anlægskassekladde**. Du kan bruge den **Bistået anskaffelse af anlægsaktiv** til at oprette og bogføre de nødvendige finanskladdelinjer automatisk.

Skrapværdien er restværdien af et anlæg, der ikke længere kan bruges. Du kan bogføre skrapværdien samtidigt med, at du bogfører anskaffelsesprisen. Du kan finde flere oplysninger i [Fremgangsmåde: Afskrive eller amortisere anlægsaktiver](fa-how-depreciate-amortize.md).

Indeksering anvendes til at justere for ændringer af det generelle prisniveau. Kørslen **Indekser anlæg** kan bruges til at beregne anskaffelsespriser som genanskaffelsespriser.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a>Sådan oprettes og anskaffes et anlægsaktiv automatisk
Følgende procedure beskriver, hvordan du opretter et anlægsaktiv og derefter anskaffer det ved hjælp af vinduet **Bistået anskaffelse af anlægsaktiver** for at oprette og bogføre de nødvendige anlægskassekladdelinjer. Du kan også oprette og bogføre linjerne manuelt. Du kan finde flere oplysninger i afsnittet "Sådan bogføres anskaffelse af et anlægsaktiv manuelt med anlægskassekladden".

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** handling, og udfyld felterne på oversigtspanelet **Generelt** efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I oversigtspanelet **Afskrivningsprofil** skal du udfylde felterne efter behov. I dette trin tildeles en afskrivningsprofil til anlægsaktivet.  
4. Hvis du vil tildele mere end én afskrivningsprofil til anlægsaktivet, skal du vælge handlingen **Tilføj flere afskrivningsprofiler**. Du kan finde flere oplysninger i afsnittet "Sådan tildeles en afskrivningsprofil til et anlægsaktiv" i [Fremgangsmåde: Konfigurere afskrivning af anlægsaktiver](fa-how-setup-depreciation.md).

    Når alle felter, der kræves for at anskaffe et anlægsaktiv, er udfyldt, vises beskeden **Du er klar til at anskaffe anlægsaktivet. Anskaf** øverst på siden.
5. Vælg handlingen **Anskaf** i beskeden.
6. Følg trinnene i vinduet **Bistået anskaffelse af anlægsaktiver** for at fuldføre automatisk anskaffelse af anlægsaktivet.

> [!NOTE]  
>   Du kan også bogføre anskaffelsespriser som kreditposter. I så fald skal du huske, at værdien i feltet **Anskaffelsespris inkl. moms** skal have et minustegn for at angive en kredit.

Når du vælger **Udfør**, udfyldes feltet **Bogført værdi** i vinduet **Anlægskort**, hvilket angiver, at anlægsaktivet er anskaffet til den angivne anskaffelsespris.  

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>Sådan konfigureres en komponentliste for et hovedanlæg
Du kan gruppere anlægsaktiverne i hovedanlæg og de tilhørende komponenter. Du kan f.eks. have en produktionsmaskine, som består af mange dele, som du vil gruppere på denne måde.  

Både hovedanlægget og alle dets komponenter skal oprettes som individuelle anlægskort. Når du har oprettet en komponentliste, udfylder [!INCLUDE[d365fin](includes/d365fin_md.md)] felterne **Hovedanlæg/underanl.** og **Hovedanlæg/underanl.** på anlægskortene.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, der er hovedanlægget, og vælg derefter handlingen **Hovedanlæg**.
3. I vinduet **Hovedanlæg** skal du vælge feltet **Anlægsnr.**. og derefter vælge det anlægsaktiv, du vil tilføje som en del af hovedanlægget.
4. Luk vinduet.
5. Gentag trin 3 til 4 for hver underdel til anlægget, du vil tilføje.
6. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsopsætning**, og vælg derefter det relaterede link.
7. Markér afkrydsningsfeltet **Tillad bogf. på hovedanlæg**.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a>Sådan bogføres anskaffelse af et anlægsaktiv manuelt med finanskassekladden
Følgende fremgangsmåde bruges til at anskaffe et anlægsaktiv manuelt ved at oprette og bogføre linjerne i vinduet **Anlægsfinanskladde**. Du kan også anskaffe et anlægsaktiv automatisk ved hjælp af vinduet **Bistået anskaffelse af anlægsaktiver**. Flere oplysninger under trin 5 i afsnittet "Sådan oprettes og anskaffes et anlægsaktiv automatisk".

> [!NOTE]  
>   Du kan også bogføre anskaffelsespriser som kreditposter. I så fald skal du huske, at værdien i feltet **Beløb** skal have et minustegn for at angive en kredit.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsfinanskladder**, og vælg derefter det relaterede link.
2. I vinduet **Anlægskassekladde** i feltet **Anlægsbogføringstype** skal du vælge **Anskaffelsespris**.
3. Udfyld de resterende felter efter behov.
4. Vælg handlingen **Bogfør**.  

> [!TIP]  
>   Hvis du udfylder feltet **Forsikringsnr.** i anlægskassekladden, når du bogfører en anskaffelsespris, bogfører [!INCLUDE[d365fin](includes/d365fin_md.md)] også anskaffelsesprisen for anlægsaktivet i forsikringsposten. Du kan finde flere oplysninger i [Fremgangsmåde: Forsikre anlægsaktiver](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Sådan annulleres bogføringen af en anskaffelsespris for et anlægsaktiv
Hvis du laver en fejl under bogføring af en anskaffelsespris, kan du fjerne posten vha. kørslen **Annuller anlægsposter** og derefter bogføre den korrekte anskaffelsespost. De forkerte poster overføres til vinduet **Anlægsfejlposter**.

Hvis du f.eks, bogfører en anskaffelse med den forkerte dato, skal du rette den snarest muligt, fordi bogføringsdatoen for anlægsaktivet bruges i mange vigtige beregninger.

> [!IMPORTANT]  
>   Du kan ikke bruge funktionen **Tilbagefør transaktioner** for anlægsposter.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Annuller anlægsposter**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vælg **OK** for at eksekvere kørslen.
4. Når den eller de forkerte poster annulleres, kan du fortsætte med at bogføre den korrekte anskaffelsespris.

Hvis du vil annullere poster for flere anlæg samtidigt, kan du bruge kørslen **Annuller anlægsposter**.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Sådan bogføres skrapværdien sammen med anskaffelsesprisen
Du kan bogføre skrapværdien sammen med anskaffelsesprisen fra en anlægskassekladde.    

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Annuller anlægsposter**, og vælg derefter det relaterede link.
2. Opret anskaffelseskladdelinjen. Du kan finde flere oplysninger i afsnittet "Sådan bogføres anskaffelse af et anlægsaktiv manuelt med anlægskassekladden".
3. Angiv beløbet for skrapværdien som en kreditpost (med et minustegn) i feltet **Skrapværdi** på kladdelinjen.
4. Vælg handlingen **Bogfør**.

> [!NOTE]  
>   Du kan kun vælge bogføringstypen **Skrapværdi** i vinduet **Anlægskladde**. Det er ikke tilgængeligt i vinduet **Anlægskassekladde**, fordi skrapværdi aldrig bogføres i finansregnskabet.

## <a name="see-also"></a>Se også
[Anlægsaktiver](fa-manage.md)  
[Opsætning af anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

