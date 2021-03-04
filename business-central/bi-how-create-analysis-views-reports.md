---
title: Oprette analyserapporter | Microsoft Docs
description: Beskriver, hvordan du opretter nye analyserapporter for salg, køb og lager og opretter analyseskabeloner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 41c10e142d2a64a7e86a0bf3604af649978bef83
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752201"
---
#  <a name="create-analysis-reports"></a>Oprette analyserapporter
Salgschefer har behov for løbende at kunne analysere omsætning, bruttoavance og andre nøgletal om salgsresultater. Indkøbere er mere interesseret i udviklingen inden for købsmængder, leverandørernes præstation og købspriser. Logistik- og lagerchefer har på den anden side brug for oplysninger om lageromsætning, analyser af lagerbevægelser og statistik om lagerværdi.  

Du kan bruge analyserapporter til at lave tilpassende rapporter på grundlag af poster for bogførte transaktioner, f.eks. salg, køb, overflytninger og lagerreguleringer. I en tilpasset rapport kan du kombinere, sammenligne og præsentere kildeoplysninger fra fra en varekladde (med tilhørende værdiposter) på mange forskellige måder, så du får meningsfulde oplysninger. Analyserapporten minder i den henseende meget om en rapport af typen Pivottabel i Microsoft Excel.  

Du kan oprette en tilpasset rapport, der fokuserer på dine nøglekonti med hensyn til indeværende måneds totale omsætning, både i afsat beløb og mængde, bruttoavance og bruttoavanceprocent, og få sammenlignet tallene med resultaterne for de foregående måneder eller med samme måned forrige år og beregne afvigelser. Alt dette kan gøres i en og samme visning, og du har stadig mulighed for at finde frem til årsagen til identificerede problemområder ved at vælge rulleknappen for at få adgang til oplysningerne på de individuelle transaktioners niveau.  

Analyserapporten består af de objekter, som du vil analysere, f.eks. kunder, kundegrupper, sælgere m.m., repræsenteret ved linjer, og analyseparametrene, dvs. den måde, som du vil analysere objekterne på, repræsenteret ved kolonner, f.eks. avanceberegning, periodisk sammenligning af salgsbeløb og -mængder eller af faktiske og budgetterede tal.

Ud over analyserapporter, kan du oprette og få vist ensartede oplysninger i analysevisninger, som er baseret på dimensioner. Du kan finde flere oplysninger under [Analysere data efter dimensioner](bi-how-analyze-data-dimension.md).

## <a name="example"></a>Eksempel  
Du kan oprette linjer som følgende:  
- Computere  
- Skærme  
- Reservedele  

Derefter kan du oprette kolonner som disse:  

- Salg indeværende måned  
- Salg foregående måned  
- Salg i % af foregående måned  

## <a name="setting-up-line-and-column-layouts"></a>Opsætte linje- og kolonneformater  
 På siden **Analyserapport** kan du få vist forskellige linje- og kolonneformater i henhold til de linjer eller linjeskabeloner, som du har oprettet på siden **Analyselinjeskabeloner**. Du kan definere navnet på rapporten og de objekter, der skal vises på linjerne i rapporten. Kolonnerne angiver du på siden **Analysekolonneskabeloner**. Du kan definere navnet på kolonneskabelonen og de analyseparametre, der skal vises i rapporten i form af kolonner. På siden **Analysekolonneskabeloner** repræsenterer hver linje en kolonne i rapporten. Bemærk, at analyselinjer og analysekolonner er uafhængige af hinanden.  

[!INCLUDE[prod_short](includes/prod_short.md)] samler resultaterne af rapporten i på siden **Analyserapport** på grundlag af de linjer og kolonner, du har angivet, som i følgende tabel.  

|- |Salg indeværende måned|Salg foregående måned|Salg foregående måned i %|  
|-|-|-|-|  
|Computere| | | |  
|Skærme| | | |  
|Reservedele| | | |  
|I alt| | | |  

 Du kan f.eks. oprette et sæt linjer og flere forskellige sæt kolonneformater, så du får vist henholdsvis månedlige og årlige rapporter.

 ## <a name="to-set-up-analysis-column-templates"></a>Sådan oprettes analysekolonneskabeloner
Følgende procedure er baseret på analysevisninger for salg. Trinene er de samme for købs- og lageranalysevisninger.

I en analyserapport vises analyseparametrene som kolonner. Du kan angive, hvilke kolonner der skal med i analyserapporten, ved at opsætte analysekolonneskabeloner.  

En skabelon indeholder et sæt linjer, der hver repræsenterer de analysekolonner, som du ser i analyserapporten. Hvis du vil definere en kolonne, skal du tildele en analysetypekode til en linje. Denne analysetypekode bestemmer typen af kildedata i de vareposter, analyse baseres på. Kildedataene indeholder pris, salgsbeløb eller antal og deres tilknyttede værdiposter. Du kan oprette et ubegrænset antal kolonneskabeloner og derefter bruge dem til at oprette nye analyserapporter.    

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sales-kolonneskabeloner**, og vælg derefter det relaterede link.  
2. Vælg den første tomme linje, og udfyld derefter felterne efter behov.
3. Vælg handlingen **Kolonner**.  
4. Udfyld felterne på siden **Analysekolonner** for at angive de kolonner, som du vil have med i analyserapporten.  

    > [!NOTE]  
    >   For at definere en kolonne skal du udfylde feltet **Analysetypekoder** for alle kolonnetyper undtagen **Formel**. Angiv analysetypekoderne på siden **Analysetyper**.  
    Hvis du vælger **Vareposter** i feltet **Posttype**, kopieres de faktiske tal desuden fra vareposten. Hvis du vælger **Varebudgetposter**, kopieres de budgetterede tal fra budgettet.  
5.  Vælg knappen **OK** for at gemme ændringerne.  

## <a name="to-set-up-analysis-line-templates"></a>Sådan opsættes analyselinjeskabeloner  
Følgende procedure er baseret på analyserapporter for salg. Trinene er de samme for købs- og lageranalyserapporter.

I en analyserapport vises analyseobjekterne på linjer. Du kan angive, hvilke linjer der skal med i analyserapporten, ved at opsætte analyselinjeskabeloner.  

En skabelon indeholder et sæt linjer, der repræsenterer de analyselinjer, som du ser i analyserapporten. En linje kan angive en eller flere varer, kunder, leverandører eller grupper. Du kan også oprette en formular på en linje for at opsummere de andre linjer. Du kan oprette et ubegrænset antal linjeskabeloner og derefter bruge dem til at oprette nye analyserapporter.    

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sales-linjeskabeloner**, og vælg derefter det relaterede link.  
2. Vælg den første tomme linje, og udfyld derefter felterne efter behov.
3. Vælg handlingen **Linjer**.  
4. Brug siden **Analyselinjer** til at oprette linjer for de varer, kunder, leverandører eller sælgere, som du vil se oplysninger for i analyserapporten. Du skal udfylde felterne **Type**, **Interval** og **Beskrivelse**.  

> [!NOTE]  
>   Hvis du skal oprette mange individuelle linjer for hver vare, kunde osv., kan du i stedet klikke på den relevante indsættelsesfunktion for at udfylde alle de relevante felter på linjen. Hvis du vil, kan du derefter redigere linjerne manuelt. Hvis du vil indsætte linjer, skal du vælge handlingen **Indsæt varer** eller **Indsæt varegrupper**.  

## <a name="to-create-a-new-sales-analysis-report"></a>Sådan oprettes en ny salgsanalyserapport
Følgende procedure er baseret på analyserapporter for salg. Trinene er de samme for købs- og lageranalyserapporter.

Du kan anvende analyserapporter til at analysere dynamikken i dine salg i henhold til nøglesalgsindikatorer, som du vælger, f.eks. salgsomsætningen i både beløb og antal, dækningsbidrag, eller det aktuelle salgs forløb i forhold til budgettet. Du kan også anvende rapporten til at analysere dine gennemsnitlige salgspriser og evaluere din salgsstyrkes præstationer.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sales-analyserapporter**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** på siden **Analyserapport - salg**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg handlingen **Rediger analyserapport**.
5. Vælg handlingen **Vis matrix** på siden **Salgsanalyserapport**.  

> [!NOTE]  
>   Det er valgfrit at opbygge kombinationer af linje- og kolonneskabeloner for at oprette rapporter og tildele dem unikke navne. Hvis du gør dette, betyder valg af et rapportnavn, ar du ikke har brug for at vælge linje- og kolonneskabeloner på siden **Salgsanalyserapport**. Når du har valgt et rapportnavn, kan du ændre linje- og kolonneskabeloner uafhængigt og derefter senere vælge rapportnavnet igen for at gendanne den oprindelige kombination.

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]