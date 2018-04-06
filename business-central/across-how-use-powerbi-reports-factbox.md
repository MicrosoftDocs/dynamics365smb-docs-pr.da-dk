---
title: "Få vist brugerdefinerede Power BI-rapporter | Microsoft Docs"
description: "Du kan bruge Power BI-rapporter til at få ekstra indsigt i data på lister i Financials."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 00629240e565da65ccc7d213d0e24cfebf33fac6
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="viewing-list-data-in-power-bi-reports-in-business-central"></a>Vise listedata i Power BI-rapporter i Business Central 
[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder et faktaboks-kontrolelement på en række vigtige sider, der giver ekstra indsigt i oplysningerne på listen. Når du flytter mellem rækkerne på listen, opdateres rapporten og filtreres for den valgte post. Du kan oprette brugerdefinerede rapporter, der kan vises i kontrolelementet, men du skal følge nogle særlige regler, når du opretter rapporterne, for at sikre, at de giver den ønskede funktionalitet.  

> [!NOTE]  
>   Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Power BI. Desuden skal du hente [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Du kan finde flere oplysninger i [Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md).  

## <a name="report-data-set"></a>Rapportdatasæt
Når du opretter rapporten i Power BI Desktop, skal du angive den kilde- eller datatjeneste, der indeholder de data, der er relateret til den liste, du vil knytte rapporten til. Hvis du f.eks. vil oprette en rapport i tilknytning til salgslisten, skal du sikre, at datasættet indeholder salgsrelaterede oplysninger.  

For at filtrere data i rapporterne baseret på den post, der er valgt på oversigtssiden, skal den primære nøgle bruges som et rapportfilter. De primære nøgler skal være en del af datasættet, hvis rapporterne skal filtreres korrekt. I de fleste tilfælde er primærnøglen for en liste feltet **Nr.** .  

## <a name="defining-the-report-filter"></a>Definere rapportfilteret
Rapporten skal have et grundlæggende rapportfilter (ikke et sidefilter eller visuelt filter og ikke et avanceret filter) for at filtrere korrekt i Power BI-faktabokskontrolelementet. Det filter, der sendes til Power BI-rapporten fra hver oversigtsside, baseres på primærnøglen som beskrevet ovenfor.  

Du kan definere et filter for rapporten, vælge primærnøglen på listen over tilgængelige felter og derefter trække og slippe direkte i sektionen **Rapportfilter**.  

![Angive rapportfilteret for rapporten Salgsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="report-size-and-color"></a>Rapportstørrelse og -farve
Størrelsen på rapporten skal angives til 325 x 310 pixel. Det er nødvendigt, for at rapporten kan skaleres korrekt på den plads, der er tilladt af Power BI-faktabokskontrolelementet. Hvis du vil angive størrelsen på rapporten, skal du placere fokus uden for rapportens layoutområde og derefter vælge malerulleikonet.

![Angive rapportbredde og højde for rapporten Salgsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

Du kan ændre bredden og højden for rapporten ved at vælge **Brugerdefineret** i feltet **Type**.

Hvis du på samme måde vil have, at baggrunden for rapporten kombineres med baggrundsfarven for Power BI-faktabokskontrolelementet, skal du angive den brugerdefinerede baggrundsfarve *E5E5E5* til rapporten. Denne indstilling er valgfri.  

## <a name="reports-with-multiple-pages"></a>Rapporter med flere sider
Med Power BI kan du oprette en enkelt rapport med flere sider. Grafik, der skal vises på [!INCLUDE[d365fin](includes/d365fin_md.md)]-oversigtssider, skal findes på den første side i rapporten i Power BI.  

> [!NOTE]  
>  Power BI-faktaboksen kan kun indeholde den første side i rapporten. Hvis du vil have vist andre sider, skal du udvide rapporten og bruge fanerne nederst i rapporten til at navigere til andre sider.  

## <a name="saving-your-report"></a>Gemme rapporten

Når du gemmer rapporten, er det bedst, at navnet på rapporten indeholder navnet på den oversigtsside, du vil have vist rapporten på. Ordet *Kreditor* skal f.eks. være indholdet et sted i rapportnavnet for rapporter, som du vil gøre tilgængelige i kreditoroversigten.  

Dette er ikke et krav, men det vil gøre processen med at vælge rapporter hurtigere. Når siden til valg af rapporter åbnes fra en oversigtsside, overfører vi i et filter, der er baseret på navnet på siden, for at begrænse de rapporter, der vises.  Du kan fjerne filteret for at få en komplet oversigt over rapporter, der er tilgængelige for dig i Power BI.  

## <a name="troubleshooting"></a>Fejlfinding
Denne sektion indeholder en løsning på de mest almindelige problemer, der kan opstå, når du opretter Power BI-rapporten.  

**Brugeren får ikke vist en rapport på siden Vælg rapport, som han eller hun vil vælge** Hvis du ikke kan vælge en rapport, kan du evt. kontrollere navnet på rapporten for at sikre, at det indeholder navnet på oversigtssiden. Du kan rydde filteret for at se en komplet oversigt over tilgængelige Power BI-rapporter.  

**Rapporten indlæses, men er tom, ikke filtreret eller filtreret forkert** Kontroller, at rapportfilteret indeholder den rigtige primærnøgle. I de fleste tilfælde er det feltet **Nr.** , men i tabellen **Finanspost** skal du f.eks. bruge feltet **Løbenr.**

**Rapporten indlæses, men viser en side, du ikke forventede** Kontroller, at den side, du vil have vist, er den første side i rapporten.  

**Rapporten vises med uønskede grå kanter, er for lille eller for stor**

Kontroller, at rapportstørrelse er indstillet til 325 x 310 pixel. Gem rapporten, og opdater derefter oversigtssiden.  

## <a name="see-also"></a>Se også
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)    
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)    
[Finans](finance.md)  

