---
title: Oprette analyserapporter | Microsoft Docs
description: "Beskriver, hvordan du opretter nye analyserapporter for salg, køb og lager og opretter analyseskabeloner."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ec1f03555db4e370bf19da41bcb33e9b1d286f82
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017

---
#  <a name="how-to-create-analysis-reports"></a>Fremgangsmåde: Oprette analyserapporter
Salgschefer har behov for løbende at kunne analysere omsætning, bruttoavance og andre nøgletal om salgsresultater. Indkøbere er mere interesseret i udviklingen inden for købsmængder, leverandørernes præstation og købspriser. Logistik- og lagerchefer har på den anden side brug for oplysninger om lageromsætning, analyser af lagerbevægelser og statistik om lagerværdi.  

Du kan bruge analyserapporter til at lave tilpassende rapporter på grundlag af poster for bogførte transaktioner, f.eks. salg, køb, overflytninger og lagerreguleringer. I en tilpasset rapport kan du kombinere, sammenligne og præsentere kildeoplysninger fra fra en varekladde (med tilhørende værdiposter) på mange forskellige måder, så du får meningsfulde oplysninger. Analyserapporten minder i den henseende meget om en rapport af typen Pivottabel i Microsoft Excel.  

Du kan oprette en tilpasset rapport, der fokuserer på dine nøglekonti med hensyn til indeværende måneds totale omsætning, både i afsat beløb og mængde, bruttoavance og bruttoavanceprocent, og få sammenlignet tallene med resultaterne for de foregående måneder eller med samme måned forrige år og beregne afvigelser. Alt dette kan gøres i en og samme visning, og du har stadig mulighed for at finde frem til årsagen til identificerede problemområder ved at vælge rulleknappen for at få adgang til oplysningerne på de individuelle transaktioners niveau.  

Analyserapporten består af de objekter, som du vil analysere, f.eks. kunder, kundegrupper, sælgere m.m., repræsenteret ved linjer, og analyseparametrene, dvs. den måde, som du vil analysere objekterne på, repræsenteret ved kolonner, f.eks. avanceberegning, periodisk sammenligning af salgsbeløb og -mængder eller af faktiske og budgetterede tal.

Ud over analyserapporter, kan du oprette og få vist ensartede oplysninger i analysevisninger, som er baseret på dimensioner. Du kan finde flere oplysninger under [Fremgangsmåde: Analyser data efter dimensioner](bi-how-analyze-data-dimension.md).

## <a name="example"></a>Eksempel  
Du kan oprette linjer som følgende:  
- Computere  
- Skærme  
- Reservedele  

Derefter kan du oprette kolonner som disse:  

- Salg indeværende måned  
- Salg foregående måned  
- Salg i % af foregående måned  

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Pakke**. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="setting-up-line-and-column-layouts"></a>Opsætte linje- og kolonneformater  
 I vinduet **Analyserapport** kan du få vist forskellige linje- og kolonneformater alt efter din opsætning. Du opretter linjer eller linjeskabeloner i vinduet **Analyselinjeskabeloner**. I dette vindue kan du definere navnet på rapporten og de objekter, der skal vises på linjerne i rapporten. Kolonnerne angiver du i vinduet **Analysekolonneskabeloner**. I dette vindue kan du definere navnet på kolonneskabelonen og de analyseparametre, der skal vises i rapporten i form af kolonner. I vinduet **Analysekolonneskabeloner** repræsenterer hver linje en kolonne i rapporten. Bemærk, at analyselinjer og analysekolonner er uafhængige af hinanden.  

Programmet samler resultaterne af rapporten i matrixvinduet **Analyserapport** på grundlag af de linjer og kolonner, som du har angivet, som i dette eksempel:  

|||||  
|-|-|-|-|  
||Salg indeværende måned|Salg foregående måned|Salg foregående måned i %|  
|Computere||||  
|Skærme||||  
|Reservedele||||  
|I alt||||  

 Du kan f.eks. oprette et sæt linjer og flere forskellige sæt kolonneformater, så du får vist henholdsvis månedlige og årlige rapporter.

 ## <a name="to-set-up-analysis-column-templates"></a>Sådan oprettes analysekolonneskabeloner
Følgende procedure er baseret på analysevisninger for salg. Trinene er de samme for købs- og lageranalysevisninger.

I en analyserapport vises analyseparametrene som kolonner. Du kan angive, hvilke kolonner der skal med i analyserapporten, ved at opsætte analysekolonneskabeloner.  

En skabelon indeholder et sæt linjer, der hver repræsenterer de analysekolonner, som du ser i analyserapporten. Hvis du vil definere en kolonne, skal du tildele en analysetypekode til en linje. Denne analysetypekode bestemmer typen af kildedata i de vareposter, analyse baseres på. Kildedataene indeholder pris, salgsbeløb eller antal og deres tilknyttede værdiposter. Du kan oprette et ubegrænset antal kolonneskabeloner og derefter bruge dem til at oprette nye analyserapporter.    

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsanalyse - Kolonneskabeloner**, og vælg derefter det relaterede link.  
2. Vælg den første tomme linje, og udfyld derefter felterne efter behov.
3. Vælg handlingen **Kolonner**.  
4. Udfyld felterne i vinduet **Analysekolonner** for at angive de kolonner, som du vil have med i analyserapporten.  

    > [!NOTE]  
>   For at definere en kolonne skal du udfylde feltet **Analysetypekoder** for alle kolonnetyper undtagen **Formel**. Angiv analysetypekoderne i vinduet **Analysetyper**.  

    **Bemærk**! Hvis du vælger **Vareposter** i feltet **Posttype**, kopieres de faktiske tal fra vareposten. Hvis du vælger **Varebudgetposter**, kopieres de budgetterede tal fra budgettet.  
5.  Vælg knappen **OK** for at gemme ændringerne.  

## <a name="to-set-up-analysis-line-templates"></a>Sådan opsættes analyselinjeskabeloner  
Følgende procedure er baseret på analyserapporter for salg. Trinene er de samme for købs- og lageranalyserapporter.

I en analyserapport vises analyseobjekterne på linjer. Du kan angive, hvilke linjer der skal med i analyserapporten, ved at opsætte analyselinjeskabeloner.  

En skabelon indeholder et sæt linjer, der repræsenterer de analyselinjer, som du ser i analyserapporten. En linje kan angive en eller flere varer, kunder, leverandører eller grupper. Du kan også oprette en formular på en linje for at opsummere de andre linjer. Du kan oprette et ubegrænset antal linjeskabeloner og derefter bruge dem til at oprette nye analyserapporter.    

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsanalyse - linjeskabeloner**, og vælg derefter det relaterede link.  
2. Vælg den første tomme linje, og udfyld derefter felterne efter behov.
3. Vælg handlingen **Linjer**.  
4. Brug vinduet **Analyselinjer** til at oprette linjer for de varer, kunder, leverandører eller sælgere, som du vil se oplysninger for i analyserapporten. Du skal udfylde felterne **Type**, **Interval** og **Beskrivelse**.  

> [!NOTE]  
>   Hvis du skal oprette mange individuelle linjer for hver vare, kunde osv., kan du i stedet klikke på den relevante indsættelsesfunktion for at udfylde alle de relevante felter på linjen. Hvis du vil, kan du derefter redigere linjerne manuelt. Hvis du vil indsætte linjer, skal du vælge handlingen **Indsæt varer** eller **Indsæt varegrupper**.  

## <a name="to-create-a-new-sales-analysis-report"></a>Sådan oprettes en ny salgsanalyserapport
Følgende procedure er baseret på analyserapporter for salg. Trinene er de samme for købs- og lageranalyserapporter.

Du kan anvende analyserapporter til at analysere dynamikken i dine salg i henhold til nøglesalgsindikatorer, som du vælger, f.eks. salgsomsætningen i både beløb og antal, dækningsbidrag, eller det aktuelle salgs forløb i forhold til budgettet. Du kan også anvende rapporten til at analysere dine gennemsnitlige salgspriser og evaluere din salgsstyrkes præstationer.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsanalyserapporter**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** i vinduet **Analyserapport - salg**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg handlingen **Rediger analyserapport**.
5. Vælg handlingen **Vis matrix** i vinduet **Salgsanalyserapport**.  

> [!NOTE]  
>   Det er valgfrit at opbygge kombinationer af linje- og kolonneskabeloner for at oprette rapporter og tildele dem unikke navne. Hvis du gør dette og vælger et rapportnavn, behøver du ikke vælge linje- og kolonneskabeloner i vinduet **Salgsanalyserapport**. Når du har valgt et rapportnavn, kan du ændre linje- og kolonneskabeloner uafhængigt og derefter senere vælge rapportnavnet igen for at gendanne den oprindelige kombination.

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

