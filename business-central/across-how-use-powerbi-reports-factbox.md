---
title: Vis brugerdefinerede Power BI-rapporter
description: Du kan bruge Power BI-faktaboksen til at vise Power BI-rapporter og få ekstra indblik i data i nøgle lister.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 06/11/2021
ms.author: jswymer
---
# Oprettelse af Power BI-rapporter til visning af listedata i [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] indeholder et kontrolelement for Power BI-faktaboksen på mange nøglelistesider. Formålet med denne faktaboks er at vise Power BI-rapporter, der er relateret til poster på listerne, hvilket giver ekstra indblik i dataene. Formålet er, at rapporten opdateres for den valgte post, når du bevæger dig mellem rækkerne på listen.

[!INCLUDE[prod_long](includes/prod_long.md)] er klar med nogle af disse rapporter. Du kan også oprette dine egne brugerdefinerede rapporter, der skal vises i denne faktaboks. Oprettelse af disse rapporter svarer til andre rapporter. Men der er nogle få designregler, som du skal følge for at sikre, at rapporterne vises som forventet. Reglerne beskrives i denne artikel.

> [!NOTE]
> Generelle oplysninger om oprettelse og udgivelse af Power BI-rapporter til Business Central finder du i [Oprettelse af Power BI-rapporter for at vise [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md). 

## Forudsætninger

- En Power BI-konto.
- Power BI Desktop.

<!-- 
For more information about getting started, see [Use [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## Oprette en rapport til en listeside

1. Start Power BI Desktop.
2. Vælg **Hent data**, og begynd at vælge datakilden for rapporten.

    Angiv, hvilke listesider for Business Central, der skal indeholde de data, du vil have med i rapporten. Hvis du f. eks. vil oprette en rapport til listen **Salgsfakturaer**, skal du medtage sider, der vedrører salg.

    Du kan finde flere oplysninger ved at følge instruktioner i [Tilføje [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).

3. Angive rapportfilteret.

    Sådan foretager du dataopdatering til den valgte post på listen ved at føje et filter til rapporten. Filteret skal indeholde et felt i den datakilde, der bruges til entydigt at identificere hver post på listen. I forhold til udviklere er dette felt den *primære nøgle*. I de fleste tilfælde er primærnøglen for en liste feltet **Nr.** .

    Sådan kan du benytte følgende fremgangsmåde for at angive filteret:

    1. I **Filtre** skal du vælge feltet for den primære nøgle på listen over tilgængelige felter.
    2. Træk feltet til ruden **Filter**, og slip den i boksen **Filtrer på alle sider**.
    3. Indstil **Filtertype** til **Grundlæggende filtrering**. Det kan ikke være sidefilter, visuelt eller avanceret filter.

    ![Indstilling af rapportfilteret for rapporten Salgsfakturaaktivitet.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. Design rapportlayoutet.

    Opret layoutet ved at trække felter og tilføje visuelle effekter. Du kan finde flere oplysninger i [Arbejde med rapportvisning i Power BI Desktop](/power-bi/create-reports/desktop-report-view) i dokumentationen til Power BI.

5. Se de næste afsnit om at tilpasning af rapporten og brug af flere sider.

6. Gem og navngiv rapporten.

    Giv rapporten et navn, der indeholder navnet på den listeside, der er tilknyttet rapporten, da det er i klienten. Navnet skelner ikke mellem store og små bogstaver. Antag, at rapporten er til listesiden **Salgsfakturaer**. Hvis det er tilfældet, skal du indsætte ordene **Salgsfakturaer** et sted i navnet, f. eks. **Mine salgsfakturaer.pbix** eller **my_Sales Invoices_list.pbix**.

    Denne navngivningskonvention er ikke et krav. Det gør imidlertid hurtigere at vælge rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]. Når siden til valg af rapporter åbnes fra en listeside, tilføres automatisk et filter på basis af navnet på siden. Filteret har syntaksen: `@*<caption>*` som `@*Sales Invoices*`. Denne filtrering sker for at begrænse de viste rapporter. Brugerne kan rydde filteret for at se en komplet liste over tilgængelige rapporter i Power BI.

7. Udgiv rapporten, når du er færdig.

    Du kan få flere oplysninger [Udgivelse af en rapport](across-how-use-financials-data-source-powerbi.md#publish-reports).

8. Test rapporten.

    Når rapporten er udgivet til dit arbejdsområde, skal de være tilgængelige fra Power BI-faktaboksen på listesiden i [!INCLUDE[prod_short](includes/prod_short.md)].

    Benyt følgende fremgangsmåde for at teste den.

    1. Åbn [!INCLUDE[prod_short](includes/prod_short.md)], og gå til listesiden.
    2. Hvis du ikke kan se Power BI-faktaboksen, skal du på handlingslinjen og derefter vælge **Handlinger** > **Vis** > **Vis/skjul Power BI-rapporter**.
    3. I Power BI-faktaboksen skal du vælge **Vælg rapporter**, markere boksen **Aktivér** for rapporten og derefter klikke på **OK**.

    Hvis rapporten er designet korrekt, vises den.  

## Angive størrelse og farve for rapporten

Størrelsen på rapporten skal angives til 325 x 310 pixel. Denne størrelse angiver rapportens korrekte skalering på den ledige plads i Power BI-faktaboksens kontrolelementet i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil angive størrelsen på rapporten, skal du placere fokus uden for rapportens layoutområde og derefter vælge malerulleikonet.

![Angive rapportbredde og højde for rapporten Salgsfakturaaktivitet.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Du kan ændre bredden og højden for rapporten ved at vælge **Brugerdefineret** i feltet **Type**.

Hvis baggrunden for rapporten skal passe ind i baggrundsfarven for kontrolelementet for Power BI-faktaboksen, skal du angive rapportens baggrundsfarve til *#FFFFFF* (hvid). 

> [!TIP]
> Brug [!INCLUDE [prod_short](includes/prod_short.md)]-temafilen til at oprette rapporter med samme farveskema som [!INCLUDE [prod_short](includes/prod_short.md)]-apps. Du kan finde flere oplysninger i [Brug [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttema](across-how-use-financials-data-source-powerbi.md#theme).

## Rapporter med flere sider

Med Power BI kan du oprette en enkelt rapport med flere sider. Men i forbindelse med rapporter, der vises med listesider, kan vi ikke anbefale, at de har mere end én side. Power BI-faktaboksen viser kun den første side i rapporten.

## Løsning af problemer

Denne sektion forklarer, hvordan du løser problemer, som du kan støde på, når du forsøger at få vist en Power BI-rapport for en listeside i [!INCLUDE[prod_short](includes/prod_short.md)].  

### Du kan ikke se Power BI-faktaboksen på en listeside

Power BI-faktaboksen er som standard skjult. Hvis du vil have vist faktaboksen på en side, skal du vælge **Handlinger** > **Vis** > **Vis/skjul Power BI-rapporter** på handlingslinjen.

### Du kan ikke se rapporten i ruden Vælg rapport

Rapportens navn indeholder ikke navnet på den viste listeside. Ryd filteret for at se en komplet liste over tilgængelige Power BI-rapporter.  

### Rapporten er indlæst, men tom, ikke filtreret eller filtreret forkert

Kontrollér, at rapportfilteret indeholder den rette primære nøgle. I de fleste tilfælde er dette felt **Nr.** men i tabellen **Finanspost** skal du f.eks. bruge feltet **Løbenr.**

### Rapporten indlæses, men viser en side, du ikke forventede

Kontrollér, at den side, du vil have vist, er den første side i rapporten.  

### Rapporten vises med en uønsket grå kant, er for lille eller for stor

Kontroller, at rapportstørrelse er indstillet til 325 x 310 pixel. Gem rapporten, og opdater derefter oversigtssiden.  

## Se også

[Aktivering af dine virksomhedsdata for Power BI](admin-powerbi.md)  
[Brug af [!INCLUDE[prod_short](includes/prod_short.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
