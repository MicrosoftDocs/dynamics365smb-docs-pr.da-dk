---
title: Finde sider og oplysninger (indeholder video)
description: 'Denne artikel beskriver, hvordan du kan bruge handlinger, sider, rapporter, dokumentation og data samt andre apps og konsulenttjenester.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'find, Tell Me, search'
ms.search.form: 'TellMe, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 06/14/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="finding-pages-and-information-with-tell-me"></a>Søge efter sider og oplysninger med Fortæl mig

I denne artikel beskrives, hvordan søgningen i produktet *Fortæl mig, hvad du vil gøre*, kan hjælpe dig med at: 

* Hurtigt gå til ting som handlinger, sider eller rapporter.
* Søg efter bestemte data, enten på en listeside eller i dem alle [!INCLUDE [prod_short](includes/prod_short.md)].
* Find [!INCLUDE [prod_short](includes/prod_short.md)] dokumentation om et emne, du er interesseret i.

<!-- ![!VIDEO https://go.microsoft.com/fwlink/?linkid=2086048] -->

Hvis du har brug for hjælp til at finde noget, skal du bruge funktionen ![Fortæl mig, hvad du vil gøre.](media/ui-search/search.png "Søg efter side eller rapport") **Søg** ikon for at søge efter det. Du kan også bruge <kbd>ALT</kbd>+<kbd>Q</kbd> for at start en søgning.

Når du begynder at skrive tegn på siden **Fortæl mig, hvad du vil gøre**, [!INCLUDE[prod_short](includes/prod_short.md)] viser straks søgeresultater. Resultaterne på listen ændres, mens du skriver flere tegn. Hvis du opdager det, når du indtaster ordet *produkt*, og resultaterne omfatter *varer*, skyldes det, at søgningen bruger synonymer og alternative søgeord for at gøre det nemmere at finde handlinger, sider og rapporter.

Kolonnen til højre angiver den generelle kategori for resultatet. F.eks. om det skal åbne en oversigtsside, eller om det er en administrativ opgave.  

Nederst på siden **Fortæl mig, hvad du vil gøre** findes handlingen **udforsk sider og rapporter**, som åbner en funktionsoversigt, hvor du kan se alle tilgængelige funktioner for din rolle eller for alle roller. Flere oplysninger [Søg efter sider med Rollestifinder](ui-role-explorer.md).

> [!TIP]  
> Hvis du vil bruge tastaturet, kan du bruge <kbd>Tab</kbd>-tasten og <kbd>piletasterne</kbd> til at vælge et element i resultaterne. Hvis du trykker på <kbd>Enter</kbd>-tasten på tastaturet uden at vælge et resultat, åbner [!INCLUDE[prod_short](includes/prod_short.md)] det resultat, der står først på listen.

Siden **Fortæl mig, hvad du vil gøre** kategoriserer resultater baseret på de data, du indtaster, og den side, du arbejder på. Følgende afsnit beskriver kategorierne.

## <a name="find-an-action-on-the-current-page"></a>Finde en handling på den aktuelle side

I sektionen **På den aktuelle side** kan du finde og udføre handlinger på den side, der er åben. Hvis f.eks. siden **Salgstilbud** er åben, og du skriver "debitor", indeholder sektionen en handling, der åbner debitorkortet for den debitor, der er valgt i salgstilbuddet.

> [!NOTE]  
> Listen indeholder kun de handlinger, der findes på navigationslinjen øverst på siden. Handlinger i oversigtspanelet medtages ikke.  

## <a name="find-a-page-or-a-task"></a>Finde en side eller en opgave

Resultaterne i sektionen **Gå til sider og opgaver** giver adgang til andre sider, hvor du kan udføre opgaver eller slå oplysninger op. Hvis du ofte bruger disse sider, kan du vælge bogmærkeikonet for at føje et link til en hvilken som helst side i dit rollecenter. Du kan finde flere oplysninger i [Føje en sidehandling til rollecenteret](ui-bookmarks.md).

De sider og opgaver, der er tilgængelige, afhænger af den brugeroplevelse, du vælger for din virksomhed. Oplevelsen **Essential** giver adgang til færre sider og opgaver end oplevelsen **Premium**. Første gang du logger på, bruger du oplevelsen **Essential**. Du kan få mere at vide om brugeroplevelser ved at gå til [Tilpasning af din [!INCLUDE[prod_short](includes/prod_short.md)] oplevelse](ui-experiences.md).

## <a name="find-a-report-or-archived-information"></a>Finde en rapport eller arkiverede oplysninger

Sektionen **Gå til rapporter og analyse** giver adgang til rapporteringsfunktioner. For eksempel kan du åbne rapporten **Balance** på listen eller få adgang til arkiverede dokumenter og andre oplysninger.  

## <a name="find-a-record-or-search-the-documentation"></a>Finde en post eller søge i dokumentationen

Afsnittet **Søg efter \<keyword\>**-sektionen [!INCLUDE [prod_short](includes/prod_short.md)] indeholder et par måder at søge på:

* Brug handlingen **Søg virksomhedsdata** til at søge på alle sider i [!INCLUDE [prod_short](includes/prod_short.md)].
* Brug handlingen **Søg i Hjælp** til at finde en artikel i Business Central-dokumentationen, der indeholder dit nøgleord.

  > [!NOTE]  
  > Dokumentationen til udvidelser fra tredjepart er ikke medtaget i resultaterne.

### <a name="use-tell-me-what-you-want-to-do"></a>Brug Fortæl mig, hvad du vil foretage dig

Brug ![Fortæl mig, hvad du vil foretage dig.](media/ui-search/search.png "Søg efter side eller rapport") **Søg**-ikon for at søge efter data på tværs af [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan f.eks. finde en kunde ved at angive vedkommendes navn eller adresse eller endda finde en bestemt post, f.eks. en salgsordre. Du kan også bruge den til at finde oplysninger i vores dokumentation.

Du skal blot indtaste mindst tre tegn i et nøgleord og derefter vælge **Søg i virksomhedsdata** eller **Søg i Hjælp**.

* Hvis du søger efter data, vises resultaterne på siden **Søg i virksomhedsdata**, hvor de sorteres efter type.  
* Hvis du søger i Hjælp, indeholder ruden **Hjælp** hyperlinks til artikler, der indeholder dine nøgleord. Du får også et uddrag fra artiklen, der kan hjælpe dig med at beslutte, om det er det, du er interesseret i.

> [!NOTE]
> For data kan det tage tid at søge i alt i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil gøre resultaterne hurtigere, skal du bruge handlingen **Vis tabeller til søgning** til at vælge de tabeller og felter, du vil medtage i dine søgninger. De tabeller og felter, du kan vælge mellem, varierer, afhængigt af dit rollecenter. Alle tabeller og felter vælges som standard, hvilket kan gøre søgningen langsommere. Det anbefales, at du udelukker lige så mange tabeller og felter, som du kan.

[!INCLUDE [ui-how-search-works](includes/ui-how-search-works.md)]

## <a name="get-more-functionality-from-apps"></a>Få mere funktionalitet fra apps

Vores partnercommunity har travlt med at udvikle apps, der føjer funktioner til [!INCLUDE[prod_short](includes/prod_short.md)]. I sektionen **Hent fra Microsoft AppSource** vises apps til [!INCLUDE[prod_short](includes/prod_short.md)], der er tilgængelige i Microsoft AppSource, og som er relateret til det nøgleord, du har søgt efter.

### <a name="use-search-on-list-pages"></a>Brug Søg på listesider

Det er ikke relateret til Fortæl mig, hvad du vil gøre, men der er en anden måde at søge efter specifikke data på. Når du bruger en listeside, kan du bruge feltet ![Søgeliste](media/ui-search/search-list.png "Ikonet Søgeoversigt") **Søg**-feltet i venstre hjørne af oversigtshovedet på listesiden for at søge efter data på siden. Søgningen gælder kun for den oversigt, du har åbnet. Du kan få mere at vide om at arbejde med data på listesider ved at gå til [Sortere, søge og filtrere lister](ui-enter-criteria-filters.md).  

> [!TIP]
> Du kan søge efter bogførte bilagslinjer, som f. eks. fakturalinjer, kreditnotalinjer, leverancelinjer og modtagelseslinjer. Søg efter den type dokumentlinjer, du vil finde, og markér dine links til dokumenterne på din hjemmeside, så du nemt kan få adgang til den oprindelige eller en filtreret visning. Flere oplysninger [Føje en sidehandling til rollecenteret](ui-bookmarks.md).

## <a name="questions"></a>Spørgsmål?

Vi har vist søgning efter en række interessenter, noteret de spørgsmål, de havde fælles, og lavet vores noter om til en oversigt over ofte stillede spørgsmål. Hvis du er interesseret, kan du se [Fortæl mig – ofte stillede spørgsmål](ui-search-faq.md).

## <a name="see-also"></a>Se også

[Arbejde med Business Central](ui-work-product.md)  
[Føje en sidehandling til rollecenteret](ui-bookmarks.md)  
[Gemme og tilpasse listevisninger](ui-views.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
