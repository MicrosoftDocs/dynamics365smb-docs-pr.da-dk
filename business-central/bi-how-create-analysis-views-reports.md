---
title: Oprette analyserapporter
description: 'Beskriver, hvordan du opretter nye analyserapporter for salg, køb og lager og opretter analyseskabeloner.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: edupont
---
# <a name="create-analysis-reports"></a><a name="create-analysis-reports"></a>Oprette analyserapporter

Salgschefer har behov for løbende at kunne analysere omsætning, bruttoavance og andre nøgletal om salgsresultater. Indkøbere er mere interesseret i udviklingen inden for købsmængder, leverandørernes præstation og købspriser. Logistik- og lagerchefer har på den anden side brug for oplysninger om lageromsætning, analyser af lagerbevægelser og statistik om lagerværdi. På den måde er der ingen analyserapport, der passer til alle.

Du kan tilpasse analyserapporter til at lave tilpassende rapporter på grundlag af poster for bogførte transaktioner, f.eks. salg, køb, overflytninger og lagerreguleringer. I en tilpasset rapport kan du kombinere, sammenligne og præsentere kildeoplysninger fra en varekladde (med tilhørende værdiposter) på mange forskellige måder, så du får meningsfulde oplysninger. Analyserapporten minder i den henseende meget om en rapport af typen Pivottabel i Microsoft Excel.  

Du kan f.eks. oprette en tilpasset rapport, der fokuserer på dine nøglekonti med hensyn til den samlede produktomsætning i beløb og solgte mængder, bruttoavance og bruttoavanceprocent i den aktuelle måned. Derefter kan du få den til at sammenligne tallene med resultaterne fra de foregående måneder eller den samme måned sidste år og beregne afvigelser. Alt dette kan gøres i en og samme visning, så du har mulighed for at finde frem til årsagen til identificerede problemområder og vælge rullelisten for at få adgang til detaljer helt ned til de individuelle transaktionsniveauer.  

Analyserapporten består af de objekter, som du vil analysere (f.eks. kunder, kundegrupper, sælgere m.m., repræsenteret ved linjer) og analyseparametrene, som er den måde, du vil analysere objekterne på (f.eks. avanceberegning, periodisk sammenligning af salgsbeløb og -mængder eller af faktiske og budgetterede tal i kolonner). 

Ud over analyserapporter, kan du oprette og få vist ensartede oplysninger i analysevisninger (baseret på dimensioner). Få mere at vide i [Analysere data efter dimensioner](bi-how-analyze-data-dimension.md).

## <a name="example"></a><a name="example"></a>Eksempel

Du kan oprette linjerne (objekter, som du vil analysere):  

- Computere  
- Skærme  
- Reservedele  

Derefter kan du opsætte disse kolonner (hvordan objekterne skal analyseres):  

- Salg indeværende måned  
- Salg foregående måned  
- Salg i % af foregående måned  

## <a name="setting-up-line-and-column-layouts"></a><a name="setting-up-line-and-column-layouts"></a>Opsætte linje- og kolonneformater

På siden **Analyserapport** kan du få vist forskellige linje- og kolonneformater, som du opretter på:

* Siden **Analyselinjeskabeloner**, hvor du definerer navnet på rapporten og de objekter, der skal vises på linjerne i rapporten, og
* Siden **Analysekolonneskabeloner**, hvor du kan definere navnet på kolonneskabelonen og de analyseparametre, der skal vises i rapporten i form af kolonner. På siden repræsenterer hver linje en kolonne i rapporten. 

Bemærk, at analyselinjer og analysekolonner er uafhængige af hinanden.  

[!INCLUDE[prod_short](includes/prod_short.md)] samler resultaterne af rapporten på siden **Analyserapport** på grundlag af de linjer og kolonner, du har angivet, som i følgende tabel.  

|- |Salg indeværende måned|Salg foregående måned|Salg foregående måned i %|  
|-|-|-|-|  
|Computere| | | |  
|Skærme| | | |  
|Reservedele| | | |  
|Totalbeløb| | | |  

Du kan f.eks. oprette et sæt linjer og flere forskellige sæt kolonneformater, så du får vist henholdsvis månedlige og årlige rapporter.

## <a name="set-up-analysis-column-templates"></a><a name="set-up-analysis-column-templates"></a>Oprette analysekolonneskabeloner

Følgende procedure er baseret på analysevisninger for salg. Trinene er de samme for købs- og lageranalysevisninger.

En analysekolonneskabelon indeholder et sæt linjer, der hver repræsenterer en analysekolonne, du vil se i analyserapporten. Hvis du vil definere en kolonne, skal du tildele en analysetypekode til en linje. Denne analysetypekode bestemmer typen af kildedata i de vareposter, analyse baseres på. Kildedataene kan indeholder pris, salgsbeløb eller antal og deres tilknyttede værdiposter. Du kan oprette et ubegrænset antal kolonneskabeloner og derefter bruge dem til at oprette nye analyserapporter.    

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salgskolonneskabeloner**, og vælg derefter det relaterede link.  
2. Vælg den første tomme linje, og udfyld felterne efter behov.
3. Vælg handlingen **Kolonner**.  
4. Udfyld felterne på siden **Analysekolonner** for at angive de kolonner, som du vil have med i analyserapporten.  

    > [!NOTE]  
    > For at definere en kolonne skal du udfylde feltet **Analysetypekoder** for alle kolonnetyper undtagen **Formel**. Angiv analysetypekoderne på siden **Analysetyper**.  
    
    Hvis du vælger **Vareposter** i feltet **Posttype**, kopieres de faktiske tal desuden fra vareposten. Hvis du vælger **Varebudgetposter**, kopieres de budgetterede tal fra budgettet.  
5. Vælg **OK** for at gemme ændringerne.  

## <a name="set-up-analysis-line-templates"></a><a name="set-up-analysis-line-templates"></a>Konfigurere analyselinjeskabeloner

Følgende procedure er baseret på analyserapporter for salg. Trinene er de samme for købs- og lageranalyserapporter.

En analyselinjeskabelon indeholder et sæt linjer, der hver repræsenterer en analyselinje, du vil se i analyserapporten. En linje kan angive en eller flere varer, kunder, leverandører eller grupper. Du kan også oprette en formular på en linje for at opsummere de andre linjer. Du kan oprette et ubegrænset antal linjeskabeloner og derefter bruge dem til at oprette nye analyserapporter.   

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salgslinjeskabeloner**, og vælg derefter det relaterede link.  
2. Vælg den første tomme linje, og udfyld derefter felterne efter behov.
3. Vælg handlingen **Linjer**.  
4. Brug siden **Analyselinjer** til at oprette linjer for de varer, kunder, leverandører eller sælgere, som du vil se oplysninger for i analyserapporten. Du skal udfylde felterne **Type**, **Interval** og **Beskrivelse**.  

> [!NOTE]  
> Hvis du skal oprette mange individuelle linjer for hver vare, kunde osv., kan du i stedet klikke på den relevante indsættelsesfunktion for at udfylde alle de relevante felter på linjen. Hvis du vil, kan du derefter redigere linjerne manuelt. Hvis du vil indsætte linjer, skal du vælge handlingen **Indsæt varer** eller **Indsæt varegrupper**.  

## <a name="create-a-new-sales-analysis-report"></a><a name="create-a-new-sales-analysis-report"></a>Oprette en ny salgsanalyserapport

Følgende procedure er baseret på analyserapporter for salg. Trinene er de samme for købs- og lageranalyserapporter.

Med analyserapporter kan du analysere dynamikken i dit salg i henhold til nøglesalgsindikatorer, som du vælger, f.eks. salgsomsætningen i både beløb og antal, dækningsbidrag, det aktuelle salgs forløb i forhold til budgettet. Du kan også anvende analyserapporter til at analysere dine gennemsnitlige salgspriser og evaluere din salgsstyrkes præstationer.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salgsanalyserapporter**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** på siden **Analyserapport - salg**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg handlingen **Rediger analyserapport**.
5. Vælg handlingen **Vis matrix** på siden **Salgsanalyserapport**.  

> [!NOTE]  
> Det er valgfrit at opbygge kombinationer af linje- og kolonneskabeloner for at oprette rapporter og tildele dem unikke navne. Hvis du gør dette, har du ikke har brug for at vælge linje- og kolonneskabeloner på siden **Salgsanalyserapport**. Når du har valgt et rapportnavn, kan du ændre linje- og kolonneskabeloner uafhængigt og derefter senere vælge rapportnavnet igen for at gendanne den oprindelige kombination.

## <a name="see-also"></a><a name="see-also"></a>Se også

[Financial Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
