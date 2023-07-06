---
title: Analysere data på listesider ved hjælp af dataanalysetilstand
description: 'Få mere at vide om, hvordan du kan bruge dataanalysetilstand i Business central til at analysere data.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/30/2023
ms.custom: bap-template
ms.service: dynamics365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-list-data-using-data-analysis-mode"></a><a name="analyze-list-data-using-data-analysis-mode"></a><a name="analyze-list-data-using-data-analysis-mode"></a>Analysere listedata ved hjælp af dataanalysetilstand

I denne artikel kan du lære, hvordan du analyserer data fra listesider ved hjælp af *dataanalysetilstand*. Dataanalysetilstanden giver dig mulighed for at analysere data direkte fra siden uden at skulle køre en rapport eller skifte andet program, f.eks. Excel. Det er en interaktiv og alsidig måde at beregne, opsummere og gennemgå data på. I stedet for at køre rapporter med forskellige indstillinger og filtre kan du tilføje flere faner, der repræsenterer forskellige opgaver eller visninger på dataene. Eksempler kan være "mine kunder", "følge op på varer", "senest tilføjede leverandører", "Salgsstatistik" eller andre visninger, du kan forestille sig.

> [!TIP]
> Et godt indtryk af dataanalyse tilstanden er, at den ikke ændrer nogen af de underliggende data på listesiden eller sidens layout, når den ikke er i dataanalyse tilstand. Så den bedste måde at lære mere om, hvad du kan foretage dig i dataanalysetilstand, er at prøve noget.

## <a name="prerequisite"></a><a name="prerequisite"></a><a name="prerequisite"></a>Forudsætninger

Dataanalysetilstanden er i øjeblikket i forhåndsversion, hvilket betyder, at en administrator skal tænde den, før du kan bruge den. Hvis du er administrator, og du vil aktivere dataanalysetilstanden, skal du gå til siden **funktionsadministration** og aktivere **funktionsopdatering: analysetilstand og hurtigt analysere data direkte i Business central**. Du kan finde flere oplysninger om slå funktionsstyring til eller fra i [Funktionsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="get-started"></a><a name="get-started"></a><a name="get-started"></a>Kom i gang

1. Åbn listesiden.

   Hvis du f. eks. vil arbejde med **debitorposter**, skal du vælge ![Forstørrelsesglas, der åbner funktionen Fortæl mig](media/ui-search/search_small.png). ikon (<kbd>Alt</kbd>+<kbd>Q</kbd>), indtast *debitorposter*, og vælg derefter det relaterede link.  
2. Slå knappen **Analyser** til/fra i handlingslinjen øverst på siden.

    Dataanalysetilstand åbner dataene i en oplevelse, der er optimeret til dataanalyse.  Mens den normale handlingslinje i dataanalysetilstand erstattes af en særlig dataanalysetilstandslinje. I følgende figur vises de forskellige områder af siden i dataanalysetilstanden.

   [![Viser en oversigt over en side i dataanalysetilstand](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Hvert område forklares i de efterfølgende afsnit.

3. Brug de forskellige områder til at manipulere, opsummere og analysere data. Se de sektioner, der følger detaljer.

4. Når du vil afslutte analyse tilstanden, skal du deaktivere funktionen **Analysér** Skift.

   De analysefaner, du har tilføjet, gemmes, indtil du sletter dem. Så hvis du vender tilbage til dataanalysetilstand igen, kan du se dem nøjagtigt, som du forlod dem.

> [!NOTE]
> De data, der vises i analysetilstand, styres af de filtre eller visninger, der er angivet på listesiden. Dette giver dig mulighed for at oprette et foruddefineret data, før du skifter til analysetilstand.

## <a name="work-with-data-analysis-mode"></a><a name="work-with-data-analysis-mode"></a><a name="work-with-data-analysis-mode"></a>Arbejde med dataanalysetilstand

I dataanalysetilstand er siden opdelt i to områder:

- Hovedområdet, der består af dataområdet (1), oversigtslinjen (2) og tabulatorlinjen (5)
- Datamanipulationsområdet, der består af to ruder: kolonne (3) og analysefiltre (4).

### <a name="data-area-1"></a><a name="data-area-1"></a><a name="data-area-1"></a>Dataområde (1)

Dataområdet er det sted, hvor rækkerne og kolonnerne på listesiden vises, og dataene opsummeres. Dataområdet er en fleksibel måde at styre layoutet af kolonner og en hurtig måde at få et overblik over dataene på. For kolonner, der indeholder numeriske værdier, vises summen af alle værdierne i kolonnen i den sidste række, medmindre du har angivet rækkegrupper. I dette tilfælde vises summerne som en subtotal for grupperne.  

![Viser en oversigt over en dataområde i dataanalysetilstand](media/analysis-mode-data-area.png)

- Hvis du vil flytte en kolonne, skal du markere den og trække den til det sted, hvor der er størst mulig mening i analysen.
- Højreklik på kolonnen, eller hold markøren over den, og vælg menuknappen ![Viser ikonet på en kolonne i dataanalysetilstand, der åbner en menu med handlinger](media/analysis-mode-column-menu-icon.png) At få adgang til flere handlinger, som du kan udføre på kolonner. Eksempler:

  - Hvis du vil fastgøre en kolonne til venstre eller højre for dataområdet, så den ikke bevæger sig væk fra skærmen, når du ruller, vælg kolonnedelen ![Viser ikonet i en kolonne i dataanalysetilstand, der åbner en menu med handlinger](media/analysis-mode-column-menu-icon.png) > **Fastgør kolonne** > **Fastgør venstre**.
  - Du kan definere datafiltre direkte på kolonnedefinitionen i stedet for at gå til ruderne **Analysefiltre**. Du kan stadig finde oplysninger om relaterede data og for hver linje og åbne kortet for at få mere at vide om en bestemt enhed.
- Brug dataområdet til at interagere med dataene. For kolonner, der indeholder numeriske værdier, kan du beregne en beskrivelse af felterne ved at markere dem. Statistikken vises på statuslinjen (2) langs nederst på siden.
- Eksportér data i Excel- eller CSV-format. Du skal blot højreklikke på dataområdet eller med et udvalg af celler, der skal udlæses.

### <a name="summary-bar-2"></a><a name="summary-bar-2"></a><a name="summary-bar-2"></a>Oversigtspanel (2)

Oversigtspanelet er nederst på siden og viser statistik over dataene på listen. Når du interagerer med kolonner, hvis værdier kan sammentælles, f.eks. når du markerer flere rækker i en kolonne, der viser beløb, opdateres dataene.

![Viser en oversigt over en opsummeringslinje i dataanalysetilstand](media/analysis-mode-totals-row.png)

I følgende tabel beskrives de forskellige numre, der vises i området totaler:

|Antal|Beskrivlse|
|-|-|
|Rækker|Antallet af markerede rækker som en del af det samlede antal tilgængelige rækker. |
|Rækker i alt|Antal rækker på den ufiltrerede liste.|
|Filtreret|Det antal rækker, der vises som resultat af de filtre, der anvendes på listen.|
|Gennemsnit|Gennemsnitsværdien i alle de valgte felter, der kan summeres.|
|Antal|Antallet af udvalgte rækker.|
|Min|Minimumsværdien i alle de valgte felter, der kan summeres.|
|Maks.|Maksimumsværdien i alle de valgte felter, der kan summeres.|
|Sum|Den samlede sum af alle værdierne i de valgte felter, der kan summeres.|

### <a name="columns-3"></a><a name="columns-3"></a><a name="columns-3"></a>Kolonner (3)

**Kolonnerne** er en af to ruder, der kan bruges sammen for at definere analysen. Det andet område er ruden **Analysefiltre**. **Kolonnerne** bruges til at opsummere dataene. Brug ruden **Kolonner** til at angive, hvilke kolonner der skal medtages i analysen.

![Viser en oversigt over kolonneruden i dataanalysetilstand](media/analysis-mode-columns-2.png)

|Områder|Beskrivlse|
|-|-|
|Søg/Marker, eller Ryd alle bokse|Søg efter kolonner. Markér afkrydsningsfeltet for at vælge/rydde alle kolonner.|
|Afkrydsningsfelter|Området indeholder et afkrydsningsfelt for hvert felt i listens kildetabel. Brug dette område til at ændre, hvilke kolonner der vises på listen. Marker et afkrydsningsfelt for at få vist kolonne for feltet på siden. Fjern markeringen i afkrydsningsfeltet for at skjule kolonnen. |
|Rækkegrupper|Brug dette område til at gruppere og summere data efter et eller flere felter. Du kan kun medtage ikke-numeriske felter, f. eks. tekst, dato og klokkeslæt-felter. Række grupper bruges ofte i Pivot-tilstand.|
|Værdier|Du kan bruge dette område til at angive de felter, som du vil have en indsamlede beløb for. Du kan kun medtage felter, der indeholder numre, som kan tilføjes sammen. felterne tekst, dato eller klokkeslæt er f.eks.|

Hvis du vil flytte et felt fra et område til et andet, skal du vælge ikonet greb ![Viser en oversigt over en side i analysetilstand](media/column-grab-icon.png) ud for kolonnen på listen ovenfor, og træk den til destinationsområdet. Du kan ikke flytte et felt til et område, hvor det ikke er tilladt.

### <a name="analysis-filters-4"></a><a name="analysis-filters-4"></a><a name="analysis-filters-4"></a>Analysefiltre (4)

I ruden **analysefiltre** kan du angive yderligere datafiltre på kolonner for at begrænse posterne på listen. Indstil filtre på kolonner for at begrænse posterne på listen og efterfølgende summer til de poster, du er interesseret i, baseret på kriterier, som du angiver. Antag f.eks., at du kun er interesseret i data for en bestemt kunde eller salgsordre, der overstiger et bestemt beløb. Hvis du vil angive et filter, skal du markere kolonnen, vælge sammenlignings handlingen på listen (f.eks. **Lig med** eller **Starter med**) og derefter angive værdien.

![Viser en oversigt over filterruden i analysetilstand](media/analysis-mode-filters.png)

> [!NOTE]
> De ekstra filtre anvendes kun til fanen aktuel analyse. På den måde kan du definere nøjagtigt de ekstra datafiltre, der skal bruges til en bestemt analyse.

### <a name="tabs-5"></a><a name="tabs-5"></a><a name="tabs-5"></a>Faner (5)

Området med fanerne øverst giver dig mulighed for at oprette forskellige konfigurationer (kolonner og og analysefiltre) på separate faner, hvor du kan arbejde på fanerne uafhængigt af hinanden. Der er altid mindst én fane, der kaldes **Analyse 1**, som standard. Det er nyttigt at tilføje flere faner, når du vil gemme ofte anvendte analyse konfigurationer på et datasæt. Du kan f.eks. have faner til at analysere data i Pivot-tilstand og andre faner, der filtrerer til en delmængde af rækker. Nogle faner kan vise en detaljeret visning med mange kolonner, og andre får kun vist nogle få nøglekolonner.

Her er nogle punkter til arbejdet med flere analysefaner:

- Hvis du vil tilføje en ny fane, skal du vælge et stort **+** tegn ud for den sidste analyse fane.
- Vælg pil ned under en fane for at få adgang til en liste over handlinger, som du kan udføre på en fane som f.eks. omdøbe, duplikere, slette og flytte.

   - **Slet** sletter den fane, der aktuelt er åben. **Slet alle** sletter alle de faner, du har tilføjet, undtagen fanen standard-**analyse 1**.
- Du kan ikke fjerne **analyse 1** fuldstændigt, men du kan omdøbe den ved at bruge handlingen **Omdøb** og fjerne alle de ændringer, du har foretaget ved hjælp af **Slet** eller **Slet alt**.  

- De analysefaner, du har tilføjet og konfigureret, gemmes, indtil du sletter dem. Så hvis du vender tilbage til dataanalysetilstand igen, kan du se dem nøjagtigt, som du forlod dem.

   > [!TIP]
   > De faner, du opretter, er kun synlige for dig. Andre brugere kan kun se faner, som de har oprettet.
- Du kan kopiere analysefaner. Kopieringen kan være nyttig, hvis du vil eksperimentere med at ændre en tabulator uden at ændre originalen, eller hvis du vil oprette forskellige variationer af samme analyse.

## <a name="pivot-mode"></a><a name="pivot-mode"></a><a name="pivot-mode"></a>Pivot-tilstand

Du kan bruge Pivot-tilstanden til at analysere en stor mængde numeriske data, subtotalere data efter kategorier og underkategorier. Pivot-tilstanden er ligesom [pivot-tabeller i Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Hvis du vil aktivere og deaktivere Pivot-tilstanden, skal du vælge indstillingen **Pivot-tilstand** i ruden **Kolonner** (3). Når du aktiverer Pivot-tilstanden, vises området **kolonneetiketter** i ruden. Brug området **Kolonneetiketter** til at gruppere det samlede beløb for rækker i kategorier. De felter, du føjer til området **kolonneetiketter**, vises som kolonner i dataområdet (1).

Opbygning af dataanalyse i pivot-tilstand involverer flytning af felter til de tre områder: **Rækkegrupper**, **Kolonneetiketter** og **Værdier**. I følgende figur illustreres det, hvor felterne er tilknyttet dataområdet (1), hvor `sum` er de beregnede data, og evt. **Værdier**.

<table>
<tr><th></th><th>Kolonneetiket</th><th></th><th>Kolonneetiket</th><th></th></tr>
<tr><th>Rækkegruppe</th><th>Værdi</th><th>Værdi</th><th>Værdi</th><th>Værdi</th></tr>
<tr><td>række</td><td>sum</td><td>sum</td><td>sum</td><td>sum</td></tr>
<tr><td>række</td><td>sum</td><td>sum</td><td>sum</td><td>sum</td></tr>
<tr><td>række</td><td>sum</td><td>sum</td><td>sum</td><td>sum</td></tr>
<tr><td>række</td><td>sum</td><td>sum</td><td>sum</td><td>sum</td></tr>
</table>

> [!TIP]
> Kolonner, der kun har få få værdier, er de bedste kandidater til at bruge i kolonnen **Værdier**.

## <a name="limitations"></a><a name="limitations"></a><a name="limitations"></a>Begrænsninger

Analysen har i øjeblikket en begrænsning på 100.000 rækker. Hvis du overskrider denne grænse, får du vist en meddelelse om dette. Hvis du vil omgå denne begrænsning, skal du angive filtre på siden, før du skifter til dataanalysetilstand.  Du vil måske gerne analysere en bestemt gruppe af kunder eller måske kun vil have data fra indeværende år. Du kan også vælge en foruddefineret visning, hvis den kunne bruges til analysen.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Ad hoc-dataanalyse](reports-adhoc-analysis.md)  
[Vise og redigere i Excel](across-work-with-excel.md)  
