---
title: "Afskrive eller amortisere anlæg | Microsoft Docs"
description: "Du skal definere, hvordan du vil nedskrive, afskrive eller amortisere hvert af anlægsaktiverne."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e9edb717c073a3b94d925ac0cc532824a848daf6
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="depreciate-or-amortize-fixed-assets"></a>Afskrive på eller amortisere anlægsaktiver
Afskrivning bruges til at allokere prisen for et anlægsaktiv, f.eks. maskiner og udstyr, over anlæggets afskrivningslevetid. For hvert anlæg skal du definere, hvordan det skal afskrives.  

 Der er to måder at bogføre afskrivning på:  

* Automatisk ved at udføre kørslen **Beregn afskrivning**.  
* Manuelt ved at bruge anlægskassekladden.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] kan beregne daglig afskrivning, så du kan beregne afskrivningen for enhver periode. Du kan derfor analysere aktuelle driftsresultater f.eks. hver måned, hvert kvartal eller år. I beregningen anvendes et standardår på 360 dage og en standardmåned på 30 dage. Du kan finde flere oplysninger i [Afskrivningsmetoder](fa-depreciation-methods.md).  

Hvis flere afdelinger bruger et anlægsaktiv, kan periodisk afskrivning allokeres automatisk til disse afdelinger ud fra en brugerdefineret allokeringstabel.  

Du kan annullere fejlbehæftede afskrivningsposter ved at udføre kørslen **Annuller anlægsfinansposter**. Bagefter kan du bogføre det korrekte beløb ved igen at udføre kørslen **Beregn afskrivninger**. De fejl, du retter, bogføres som anlægsfejlposter.  

Indeksering anvendes til at justere for ændringer af det generelle prisniveau. Du kan bruge kørslen **Indekser anlæg** til at genberegne afskrivningsbeløbene.  

## <a name="to-calculate-depreciation-automatically"></a>Sådan beregnes afskrivning automatisk
Du kan når som helst, f.eks. en gang om måneden, udføre kørslen **Beregn afskrivning**. Kørslen ignorerer anlæg, der er blevet solgt, er spærret eller er inaktive, eller som bruger den manuelle afskrivningsmetode.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Beregn afskrivninger**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Vælg knappen **OK**.  

    Kørslen beregner afskrivningen og opretter linjer i anlægskassekladden.  
4. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsfinanskladder**, og vælg derefter det relaterede link.  

    I feltet **Antal afskrivningsdage** i vinduet **Anlægskassekladde** kan du se, hvor mange afskrivningsdage, der er blevet beregnet.  
5. Vælg handlingen **Bogfør**.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Sådan bogføres afskrivning manuelt fra anlægskassekladden
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægskassekladde**, og vælg derefter det relaterede link.  
2. Opret en første kladdelinje, og udfyld felterne efter behov.  
3. I feltet **Anlægsbogføringstype** skal du vælge **Afskrivning**.  
4. Vælg handlingen **Indsæt anlægsmodkonto**. Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af afskrivning. Du kan finde flere oplysninger i afsnittet "Sådan oprettes anlægsbogføringsgrupper" i [Angive generelle oplysninger om anlægsaktiver](fa-how-setup-general.md).  
5. På fanen **Startside** skal du vælge **Bogfør** for at bogføre kladden.  

Hvis du har defineret anlægsallokeringsnøgler for at kunne allokere beløb til forskellige afdelinger eller projekter, allokeres beløbene under bogføringen. Du kan finde flere oplysninger i [Angive generelle oplysninger om anlægsaktiver](fa-how-setup-general.md).  

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Sådan beregnes allokeringer i anlægskassekladden
Hvis et anlæg bruges af flere afdelinger, kan periodisk afskrivning allokeres automatisk på disse afdelinger ud fra en brugerdefineret allokeringstabel.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægskassekladde**, og vælg derefter det relaterede link.  
2. Opret en første linje, og udfyld felterne efter behov.
3. I feltet **Anlægsbogføringstype** skal du vælge **Allokering**.  
4. Vælg handlingen **Indsæt anlægsmodkonto**. Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af allokering.  
5. På fanen **Startside** skal du vælge **Bogfør** for at bogføre kladden.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Bruge kopilister til at forberede bogføring af flere afskrivningsprofiler
Når du udfylder kladdelinjer, der skal bogføres til en afskrivningsprofil, kan du kopiere linjerne til en særskilt kladde, så du kan bogføre i en anden afskrivningsprofil. Du kan finde flere oplysninger i afsnittet "Sådan bogføres poster til forskellige afskrivningsprofiler".

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Afskrivningsprofiler**, og vælg derefter det relaterede link.  
2. Åbn afskrivningsprofilen, og markér derefter afkrydsningsfeltet **Del af kopiliste**.  

> [!IMPORTANT]  
>   Hvis du har markeret afkrydsningsfeltet **Brug kopiliste**, skal du ikke bruge nummerserier i kladden. Det skyldes, at nummerserien til anlægskassekladden ikke bruger nummerserien til anlægskladden.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Sådan bogføres poster til forskellige afskrivningsprofiler
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægskassekladde**, og vælg derefter det relaterede link.  
2. I den kladde, som du vil bogføre afskrivning med, skal du markere afkrydsningsfeltet **Brug kopiliste**.  
3. Udfyld de resterende felter efter behov.  
4. Vælg handlingen **Bogfør**.  
5. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægskladder**, og vælg derefter det relaterede link.  

    > [!NOTE]  
>   Vinduet **Anlægskladde** indeholder nye linjer til forskellige afskrivningsprofiler ifølge kopilisten.  
6. Gennemse eller rediger linjerne, og vælg derefter handlingen **Bogfør**.  

    > [!NOTE]  
>   En anden måde at kopiere en post til en separat profil er at angive en afskrivningsprofilkode i feltet **Kopier til afskr.profil**, når du udfylder en kladdelinje.  

Du kan kopiere poster fra én afskrivningsprofil til en anden vha. kørslen **Kopier afskrivningsprofil**. Kørslen opretter kladdelinjer i den kladde, du har angivet i vinduet **Anlægskladdeopsætning** for den afskrivningsprofil, du vil kopiere til. Du kan finde flere oplysninger i følgende procedure.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Sådan kopieres anlægsposter mellem afskrivningsprofiler
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Afskrivningsprofiler**, og vælg derefter det relaterede link.  
2. Åbn det relevante afskrivningsprofilkort, og vælg handlingen **Kopiér afskrivningsprofil**.  
3. I vinduet **Kopiér afskrivningsprofil** skal du udfylde felterne efter behov.  
4. Vælg knappen **OK**.  

De kopierede linjer oprettes enten i anlægskassekladden eller anlægskladden, afhængigt af, om finansintegration er aktiveret for den afskrivningsprofil, du er ved at kopiere.  

## <a name="see-also"></a>Se også
[Anlægsaktiver](fa-manage.md)  
[Opsætning af anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

