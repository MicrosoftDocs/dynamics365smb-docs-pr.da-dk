---
title: Afskrive eller amortisere anlægsaktiver
description: Du skal definere, hvordan du vil nedskrive, afskrive eller amortisere hvert af dine anlæg, f. eks. maskiner og udstyr, over deres afskrivningslevetid.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.search.form: 5610, 5611, 5629, 5633, 5659, 5660, 5663, 5619, 5666
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 3202fb5906328da08eed10ad722b914eb5b5afcb
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511073"
---
# <a name="depreciate-or-amortize-fixed-assets"></a>Afskrive på eller amortisere anlægsaktiver
Afskrivning bruges til at allokere prisen for et anlægsaktiv, f.eks. maskiner og udstyr, over anlæggets afskrivningslevetid. For hvert anlæg skal du definere, hvordan det skal afskrives.  

 Der er to måder at bogføre afskrivning på:  

* Automatisk ved at udføre kørslen **Beregn afskrivning**.  
* Manuelt ved at bruge anlægskassekladden.  

[!INCLUDE[prod_short](includes/prod_short.md)] kan beregne daglig afskrivning, så du kan beregne afskrivningen for enhver periode. Du kan derfor analysere aktuelle driftsresultater f.eks. hver måned, hvert kvartal eller år. I beregningen anvendes et standardår på 360 dage og en standardmåned på 30 dage. Du kan finde flere oplysninger i [Afskrivningsmetoder](fa-depreciation-methods.md).  

Hvis flere afdelinger bruger et anlægsaktiv, kan periodisk afskrivning allokeres automatisk til disse afdelinger ud fra en brugerdefineret allokeringstabel.  

Du kan annullere fejlbehæftede afskrivningsposter ved at udføre kørslen **Annuller anlægsfinansposter**. Bagefter kan du bogføre det korrekte beløb ved igen at udføre kørslen **Beregn afskrivninger**. De fejl, du retter, bogføres som anlægsfejlposter.  

Indeksering anvendes til at justere for ændringer af det generelle prisniveau. Du kan bruge kørslen **Indekser anlæg** til at genberegne afskrivningsbeløbene.  

## <a name="to-calculate-depreciation-automatically"></a>Sådan beregnes afskrivning automatisk
Du kan når som helst, f.eks. en gang om måneden, udføre kørslen **Beregn afskrivning**. Kørslen ignorerer anlæg, der er blevet solgt, er spærret eller er inaktive, eller som bruger den manuelle afskrivningsmetode.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Beregn afskrivning**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Vælg knappen **OK**.  

    Kørslen beregner afskrivningen og opretter linjer i anlægskassekladden.

4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsfinanskladder**, og vælg derefter det relaterede link.  

    I feltet **Antal afskrivningsdage** på siden **Anlægskassekladde** kan du se, hvor mange afskrivningsdage, der er blevet beregnet.  
5. Vælg handlingen **Bogfør**.  

> [!NOTE]
> Kendt begrænsning: Hvis du angiver **Brug tvungent antal dage**-feltet, og feltet **Tvungent antal dage** er indstillet til en værdi, hvor **Bogføringsdato** minus **Antal dage** resulterer i en dato i det forrige kalenderår, lader systemet dig ikke bogføre afskrivningen.
> Du kan undgå dette ved at reducere værdien af felterne **Tvungent antal dage** til ikke mere end de dage, der er beregnet til bogføringsdatoen, med 30 dage pr. måned ELLER vælge feltet **Regnskabsår 365 dage** på afskrivningsprofilen.
> Vi anbefaler den første indstilling, da du måske ikke vil ændre brugen af 30 dage/måneder til afskrivning. Du kan finde flere oplysninger i [regnskabsåret 365 dage afskrivning](fa-how-setup-depreciation.md#fiscal-year-365-days-field-depreciation).


## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Sådan bogføres afskrivning manuelt fra anlægskassekladden
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskassekladde**, og vælg derefter det relaterede link.  
2. Opret en første kladdelinje, og udfyld felterne efter behov.  
3. I feltet **Anlægsbogføringstype** skal du vælge **Afskrivning**.  
4. Vælg handlingen **Indsæt anlægsmodkonto**. Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af afskrivning. Du kan finde flere oplysninger i [Sådan oprettes anlægsbogføringsgrupper](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Vælg handlingen **Bogfør** for at bogføre kladden.  

Feltet **Bogfør værdi** på siden **Anlægskort** opdateres tilsvarende.

Hvis du har defineret anlægsallokeringsnøgler for at kunne allokere beløb til forskellige afdelinger eller projekter, allokeres beløbene under bogføringen. Du kan finde flere oplysninger i [Angive generelle oplysninger om anlægsaktiver](fa-how-setup-general.md).  

## <a name="to-manage-the-ending-book-value"></a>Sådan administreres den slutbogførte værdi
I feltet **Slutbogført værdi** på siden **Anlægsafskrivningsprofiler** kan du angive den bogførte værdi, som anlægsaktivet skal have på den aktuelle afskrivningsprofil, når det er blevet afskrevet fuldt ud. Du kan gøre dette manuelt, eller du kan udfylde feltet **Standard slutbogført værdi** på den relaterede side **Afskrivningsprofil**, som derefter bruges til automatisk at udfylde feltet.

> [!NOTE]
> Hvis den sidste afskrivning betyder, at feltet **Bogført værdi** på siden **Anlægskort** bliver nul, reduceres den sidste afskrivning automatisk med denne værdi.<br /><br />
> Hvis værdien i feltet **Bogført værdi** er større end nul efter den seneste afskrivning, eksempelvis på grund af et afrundingsproblem eller fordi der findes en skrapværdi, ignoreres værdien i feltet **Slutbogført værdi** på siden **Anlægsafskrivningsprofiler**. Du kan finde flere oplysninger i [Sådan bogføres skrapværdien sammen med anskaffelsesprisen](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Sådan beregnes allokeringer i anlægskassekladden
Hvis et anlæg bruges af flere afdelinger, kan periodisk afskrivning allokeres automatisk på disse afdelinger ud fra en brugerdefineret allokeringstabel.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskassekladde**, og vælg derefter det relaterede link.  
2. Opret en første linje, og udfyld felterne efter behov.
3. I feltet **Anlægsbogføringstype** skal du vælge **Allokering**.  
4. Vælg handlingen **Indsæt anlægsmodkonto**. Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af allokering.  
5. Vælg handlingen **Bogfør** for at bogføre kladden.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Bruge kopilister til at forberede bogføring af flere afskrivningsprofiler
Når du udfylder kladdelinjer, der skal bogføres til en afskrivningsprofil, kan du kopiere linjerne til en særskilt kladde, så du kan bogføre i en anden afskrivningsprofil. Du kan finde flere oplysninger i [Sådan bogføres poster til forskellige afskrivningsprofiler](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afskrivningsprofiloversigt**, og vælg derefter det relaterede link.  
2. Åbn afskrivningsprofilen, og markér derefter afkrydsningsfeltet **Del af kopiliste**.  

> [!IMPORTANT]  
>   Hvis du har markeret afkrydsningsfeltet **Brug kopiliste**, skal du ikke bruge nummerserier i kladden. Det skyldes, at nummerserien til anlægskassekladden ikke bruger nummerserien til anlægskladden.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Sådan bogføres poster til forskellige afskrivningsprofiler
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskassekladde**, og vælg derefter det relaterede link.  
2. I den kladde, som du vil bogføre afskrivning med, skal du markere afkrydsningsfeltet **Brug kopiliste**.  
3. Udfyld de resterende felter efter behov.  
4. Vælg handlingen **Bogfør**.  
5. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskladder**, og vælg derefter det relaterede link.  

    > [!NOTE]  
    >   Siden **Anlægskladde** indeholder nye linjer til forskellige afskrivningsprofiler ifølge kopilisten.  
6. Gennemse eller rediger linjerne, og vælg derefter handlingen **Bogfør**.  

    > [!NOTE]  
    >   En anden måde at kopiere en post til en separat profil er at angive en afskrivningsprofilkode i feltet **Kopier til afskr.profil**, når du udfylder en kladdelinje.  

Du kan kopiere poster fra én afskrivningsprofil til en anden vha. kørslen **Kopier afskrivningsprofil**. Kørslen opretter kladdenumre i de kladder, du har angivet navnene på på siden **Anlægskladdeopsætning** for den afskrivningsprofil, du vil kopiere til. Du kan finde flere oplysninger i følgende procedure.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Sådan kopieres anlægsposter mellem afskrivningsprofiler
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afskrivningsprofiloversigt**, og vælg derefter det relaterede link.  
2. Åbn det relevante afskrivningsprofilkort, og vælg handlingen **Kopiér afskrivningsprofil**.  
3. På siden **Kopiér afskrivningsprofil** skal du udfylde felterne efter behov.  
4. Vælg knappen **OK**.  

De kopierede linjer oprettes enten i anlægskassekladden eller anlægskladden, afhængigt af, om finansintegration er aktiveret for den afskrivningsprofil, du er ved at kopiere.  

## <a name="see-also"></a>Se også
[Anlægsaktiver](fa-manage.md)  
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
