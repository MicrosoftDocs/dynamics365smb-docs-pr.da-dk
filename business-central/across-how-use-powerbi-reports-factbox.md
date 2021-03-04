---
title: Vise brugerdefinerede Power BI-rapporter for Business Central-data| Microsoft Docs
description: Du kan bruge Power BI-rapporter til at få ekstra indsigt i data på lister.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 069efcef517cd442539f13fad5e5a2c89e1533ff
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754463"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a>Oprette Power BI-rapporter til visning af listedata i [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] indeholder et faktaboks-kontrolelement på en række vigtige sider, der giver ekstra indsigt i dataene på listen. Når du flytter mellem rækkerne på listen, opdateres rapporten og filtreres for den valgte post. Du kan oprette brugerdefinerede rapporter, der skal vises i dette kontrolelement. Der er dog nogle få regler, du skal følge for at sikre, at rapporter fungerer som forventet.  

## <a name="prerequisites"></a>Forudsætninger

- En Power BI-konto.
- Power BI Desktop.

Du kan finde flere oplysninger om at komme i gang under [Bruge [!INCLUDE[prod_short](includes/prod_short.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md).

## <a name="defining-the-report-data-set"></a>Definere rapportdatasættet

Angiv den datakilde, der indeholder de data, som vedrører listen. Hvis du f.eks. vil oprette en rapport til salgslisten, skal du sikre, at datasættet indeholder salgsrelaterede oplysninger.  

## <a name="defining-the-report-filter"></a>Definere rapportfilteret

Hvis du vil foretage dataopdatering til den valgte post på listen, skal du føje et filter til rapporten. Filteret skal indeholde et felt fra den datakilde, der bruges som *primær nøgle*. I de fleste tilfælde er primærnøglen for en liste feltet **Nr.** .

Du kan definere et filter for rapporten, vælge primærnøglen på listen over tilgængelige felter og derefter trække og slippe direkte i sektionen **Rapportfilter**. Filteret skal være et grundlæggende rapportfilter, som er defineret for alle sider. Det kan ikke være sidefilter, visuelt eller avanceret filter.

![Angive rapportfilteret for rapporten Salgsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a>Angive størrelse og farve på rapporten

Størrelsen på rapporten skal angives til 325 x 310 pixel. Denne størrelse angiver rapportens korrekte skalering på den ledige plads i Power BI-faktaboksens kontrolelementet i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil angive størrelsen på rapporten, skal du placere fokus uden for rapportens layoutområde og derefter vælge malerulleikonet.

![Angive rapportbredde og højde for rapporten Salgsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Du kan ændre bredden og højden for rapporten ved at vælge **Brugerdefineret** i feltet **Type**.

Hvis baggrunden for rapporten skal blende i med baggrundsfarven for Power BI-faktabokskontrolelementet, skal du angive baggrundsfarven *#FFFFFF* til rapporten. 

## <a name="using-reports-with-multiple-pages"></a>Bruge rapporter med flere sider

Med Power BI kan du oprette en enkelt rapport med flere sider. Men i forbindelse med rapporter, der vises med listesider, kan vi ikke anbefale, at de har mere end én side. Power BI-faktaboksen viser kun den første side i rapporten.

## <a name="naming-the-report"></a>Navngive rapporten

Giv rapporten et navn, der indeholder navnet på den listeside, der er tilknyttet rapporten. Hvis rapporten f.eks. er til **Kreditor**-listesiden, skal du medtage ordet *kreditor* et sted i navnet.  

Denne navngivningskonvention er ikke et krav. Det gør imidlertid hurtigere at vælge rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]. Når siden til valg af rapporter åbnes fra en listeside, filtreres den automatisk på basis af navnet på siden. Denne filtrering sker for at begrænse de viste rapporter. Brugerne kan rydde filteret for at se en komplet liste over tilgængelige rapporter i Power BI.  

## <a name="fixing-problems"></a>Løse problemer

Denne sektion indeholder en løsning på de mest almindelige problemer, der kan opstå, når du opretter Power BI-rapporten.  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a>Du kan ikke se en rapport på siden Vælg rapport

Det skyldes sandsynligvis, at rapportens navn ikke indeholder navnet på listesiden. Ryd filteret for at se en komplet liste over tilgængelige rapporter i Power BI.  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Rapporten er indlæst, men tom og ikke filtreret eller filtreret forkert

Kontrollér, at rapportfilteret indeholder den rette primære nøgle. I de fleste tilfælde er dette felt **Nr.** men i tabellen **Finanspost** skal du f.eks. bruge feltet **Løbenr.**

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Rapporten indlæses, men viser en side, du ikke forventede

Kontrollér, at den side, du vil have vist, er den første side i rapporten.  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Rapporten vises med en uønsket grå kant, er for lille eller for stor

Kontroller, at rapportstørrelse er indstillet til 325 x 310 pixel. Gem rapporten, og opdater derefter oversigtssiden.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Aktivere virksomhedens data til Power BI](admin-powerbi.md)  
[Bruge [!INCLUDE[prod_short](includes/prod_short.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Introduktion](product-get-started.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]