---
title: Analysere data på listesider og forespørgsler ved hjælp af dataanalysetilstand
description: 'Få mere at vide om, hvordan du kan bruge dataanalysetilstand i Business central til at analysere data.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 12/08/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# Analysere listeside ved forespørgselsdata ved hjælp af dataanalysetilstand

> **GÆLDER FOR:** Offentlig forhåndsversion i Business Central-udgivelsesbølge 1 i 2023 og nyere til analyse af listesider; Generelt tilgængelig i Business Central 2023-udgivelsesbølge 2 til analyse af data fra listesider og forespørgsler.

I denne artikel kan du lære, hvordan du analyserer data fra listesider og forespørgsler ved hjælp af *dataanalysetilstand*. Dataanalysetilstanden giver dig mulighed for at analysere data direkte fra siden uden at skulle køre en rapport eller skifte andet program, f.eks. Excel. Det er en interaktiv og alsidig måde at beregne, opsummere og gennemgå data på. I stedet for at køre rapporter med forskellige indstillinger og filtre kan du tilføje flere faner, der repræsenterer forskellige opgaver eller visninger på dataene. Eksempler kan være "mine kunder", "følge op på varer", "senest tilføjede leverandører", "Salgsstatistik" eller andre visninger, du kan forestille sig.

> [!TIP]
> Et godt indtryk af dataanalyse tilstanden er, at den ikke ændrer nogen af de underliggende data på listesiden eller forespørgslen eller sidens layout, når den ikke er i dataanalyse tilstand. Så den bedste måde at lære mere om, hvad du kan foretage dig i dataanalysetilstand, er at prøve noget.

## Forudsætninger 

- Hvis du bruger Business Central version 22, er dataanalysetilstanden i forhåndsversion. Så en administrator skal aktivere det, før du kan bruge det. Du kan aktivere det ved at gå til siden **funktionsadministration** og aktivere **Funktionsopdatering: analysetilstand og hurtigt analysere data direkte i Business central**. [Få mere at vide om Funktionsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management).
- I version 23 og nyere skal din konto tildeles tilladelsessættet **DATA ANALYSIS - EXEC** eller inkludere kørselstilladelse på systemobjektet **9640 Tillad dataanalysetilstand**. Som administrator kan du ekskludere disse tilladelser for brugere, som ikke skal have adgang til analysetilstanden.

> [!NOTE]
> Du bemærker muligvis nogle listesider, der ikke inkluderer parameteren **Analysér**, når du skifter til analysetilstand. Årsagen er, at udviklere kan deaktivere analysetilstand på bestemte sider ved hjælp af egenskaben [AnalysisModeEnabled](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) i AL.

## Kom i gang

1. Åbn listesiden eller forespørgslen.

   Hvis du f. eks. vil arbejde med siden **debitorposter**, skal du vælge ![Forstørrelsesglas, der åbner funktionen Fortæl mig](media/ui-search/search_small.png). ikon (<kbd>Alt</kbd>+<kbd>Q</kbd>), indtast *debitorposter*, og vælg derefter det relaterede link. 

2. Slå knappen **Analyser** til/fra i handlingslinjen øverst på siden.

    Dataanalysetilstand åbner dataene i en oplevelse, der er optimeret til dataanalyse.  Mens den normale handlingslinje i dataanalysetilstand erstattes af en særlig dataanalysetilstandslinje. I følgende figur vises de forskellige områder af siden i dataanalysetilstanden.

   [![Viser en oversigt over en side i dataanalysetilstand](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Hvert område forklares i de efterfølgende afsnit.

3. Brug de forskellige områder til at manipulere, opsummere og analysere data. Se de sektioner, der følger detaljer.

4. Når du vil afslutte analyse tilstanden, skal du deaktivere funktionen **Analysér** Skift.

   De analysefaner, du har tilføjet, gemmes, indtil du sletter dem. Så hvis du vender tilbage til dataanalysetilstand igen, kan du se dem nøjagtigt, som du forlod dem.

> [!NOTE]
> De data, der vises i analysetilstand, styres af de filtre eller visninger, der er angivet på listesiden. Dette giver dig mulighed for at oprette et foruddefineret data, før du skifter til analysetilstand.

## Arbejde med dataanalysetilstand

I dataanalysetilstand er siden opdelt i to områder:

- Hovedområdet, der består af dataområdet (1), oversigtslinjen (2) og tabulatorlinjen (5)
- Datamanipulationsområdet, der består af to ruder: kolonne (3) og analysefiltre (4).

### Dataområde (1)

Dataområdet er det sted, hvor rækkerne og kolonnerne på listesidens forespørgsel vises, og dataene opsummeres. Dataområdet er en fleksibel måde at styre layoutet af kolonner og en hurtig måde at få et overblik over dataene på. For kolonner, der indeholder numeriske værdier, vises summen af alle værdierne i kolonnen i den sidste række, medmindre du har angivet rækkegrupper. I dette tilfælde vises summerne som en subtotal for grupperne.  

![Viser en oversigt over en dataområde i dataanalysetilstand](media/analysis-mode-data-area.png)

- Hvis du vil flytte en kolonne, skal du markere den og trække den til det sted, hvor der er størst mulig mening i analysen.
- For at sortere på en kolonne skal du vælge kolonneoverskriften. For at sortere på flere kolonner skal du vælge og holde <kbd>Shift</kbd> tasten nede, mens du vælger de kolonneoverskrifter, du vil sortere på.
- Højreklik på kolonnen, eller hold markøren over den, og vælg menuknappen ![Viser ikonet på en kolonne i dataanalysetilstand, der åbner en menu med handlinger](media/analysis-mode-column-menu-icon.png) At få adgang til flere handlinger, som du kan udføre på kolonner. Eksempler:

  - Hvis du vil fastgøre en kolonne til venstre eller højre for dataområdet, så den ikke bevæger sig væk fra skærmen, når du ruller, vælg kolonnedelen ![Viser ikonet i en kolonne i dataanalysetilstand, der åbner en menu med handlinger](media/analysis-mode-column-menu-icon.png) > **Fastgør kolonne** > **Fastgør venstre**.
  - Du kan definere datafiltre direkte på kolonnedefinitionen i stedet for at gå til ruderne **Analysefiltre**. Du kan stadig finde oplysninger om relaterede data og for hver linje og åbne kortet for at få mere at vide om en bestemt enhed.
- Brug dataområdet til at interagere med dataene. For kolonner, der indeholder numeriske værdier, kan du beregne en beskrivelse af felterne ved at markere dem. Statistikken vises på statuslinjen (2) langs nederst på siden.
- Eksportér data i Excel- eller CSV-format. Højreklik på dataområdet eller med et udvalg af celler, der skal udlæses.

### Oversigtspanel (2)

Oversigtspanelet er nederst på siden og viser statistik over dataene på listesiden eller forespørgslen. Når du interagerer med kolonner, hvis værdier kan sammentælles, f.eks. når du markerer flere rækker i en kolonne, der viser beløb, opdateres dataene.

![Viser en oversigt over en opsummeringslinje i dataanalysetilstand](media/analysis-mode-totals-row.png)

I følgende tabel beskrives de forskellige numre, der vises i området totaler:

|Antal|Beskrivlse|
|-|-|
|Rækker|Antallet af markerede rækker som en del af det samlede antal tilgængelige rækker. |
|Rækker i alt|Antal rækker på den ufiltrerede liste eller forespørgslen.|
|Filtreret|Det antal rækker, der vises som resultat af de filtre, der anvendes på listen eller forespørgslen.|
|Gennemsnit|Gennemsnitsværdien i alle de valgte felter, der kan summeres.|
|Antal|Antallet af udvalgte rækker.|
|Min|Minimumsværdien i alle de valgte felter, der kan summeres.|
|Maks.|Maksimumsværdien i alle de valgte felter, der kan summeres.|
|Sum|Den samlede sum af alle værdierne i de valgte felter, der kan summeres.|

### Kolonner (3)

**Kolonnerne** er en af to ruder, der kan bruges sammen for at definere analysen. Det andet område er ruden **Analysefiltre**. **Kolonnerne** bruges til at opsummere dataene. Brug ruden **Kolonner** til at angive, hvilke kolonner der skal medtages i analysen.

![Viser en oversigt over kolonneruden i dataanalysetilstand](media/analysis-mode-columns-2.png)

|Områder|Beskrivlse|
|-|-|
|Søg/Marker, eller Ryd alle bokse|Søg efter kolonner. Markér afkrydsningsfeltet for at vælge/rydde alle kolonner.|
|Afkrydsningsfelter|Området indeholder et afkrydsningsfelt for hvert felt i listens eller forespørgslens kildetabel. Brug dette område til at ændre, hvilke kolonner der vises. Marker et afkrydsningsfelt for at få vist kolonne for feltet på siden. Fjern markeringen i afkrydsningsfeltet for at skjule kolonnen. |
|Rækkegrupper|Brug dette område til at gruppere og summere data efter et eller flere felter. Du kan kun medtage ikke-numeriske felter, f. eks. tekst, dato og klokkeslæt-felter. Række grupper bruges ofte i Pivot-tilstand.|
|Værdier|Du kan bruge dette område til at angive de felter, som du vil have en indsamlede beløb for. Du kan kun medtage felter, der indeholder numre, som kan tilføjes sammen. felterne tekst, dato eller klokkeslæt er f.eks.|

Hvis du vil flytte et felt fra et område til et andet, skal du vælge greb-ikonet ![Viser en oversigt over en side i analysetilstand](media/column-grab-icon.png) ud for kolonnen på listen, og træk den til destinationsområdet. Du kan ikke flytte et felt til et område, hvor det ikke er tilladt.

### Analysefiltre (4)

I ruden **analysefiltre** kan du angive yderligere datafiltre på kolonner for at begrænse posterne på listen. Indstil filtre på kolonner for at begrænse posterne på listen og efterfølgende summer til de poster, du er interesseret i, baseret på kriterier, som du angiver. Antag f.eks., at du kun er interesseret i data for en bestemt kunde eller salgsordre, der overstiger et bestemt beløb. Hvis du vil angive et filter, skal du markere kolonnen, vælge sammenlignings handlingen på listen (f.eks. **Lig med** eller **Starter med**) og derefter angive værdien.

![Viser en oversigt over filterruden i analysetilstand](media/analysis-mode-filters.png)

> [!NOTE]
> De ekstra filtre anvendes kun til fanen aktuel analyse. På den måde kan du definere nøjagtigt de ekstra datafiltre, der skal bruges til en bestemt analyse.

### Faner (5)

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


## Datohierarkier

I analysetilstand genereres datofelter for datasættet i et hierarki for år og kvartal med tre separate felter. Dette hierarki er baseret på den normale kalender, ikke nogen regnskabskalendere, der er defineret i Business Central.

De ekstra felter hedder _\<field name\> År_, _\<field name\> Kvartal_ og _\<field name\> Måned_. Hvis datasættet f.eks. indeholder et felt med navnet _Bogføringsdato_, består det tilsvarende datohierarki af felter kaldet _Bogføringsdatoår_, _Bogføringsdatokvartal_ og _Bogføringsdatomåned_.

> [!NOTE]
> Datohierarkiet gælder i øjeblikket kun for felter af typen dato, ikke for felter af typen datetime.

## Pivot-tilstand

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


## Analysér store mængder data

Hvis det datasæt, du vil analysere, overstiger 100.000 rækker, foreslås det, at du skifter til en analysetilstand, der er optimeret til store datasæt. Der er i øjeblikket to begrænsninger, hvis du skifter til denne tilstand: 

- Formateringen af felter med følgende fire datatyper kan blive ændret: 

   - valuta 
   - decimaler (altid vist med to decimaler) 
   - datoer (vises altid i formatet ÅÅÅÅ-MM-DD)
   - tidszoner
- Felter, der bruges i pivottilstand og føjes til kolonnenavne, skal have et lavt antal særskilte værdier.

   Hvis du aktiverer pivottilstand og trækker et felt til området **Kolonnenavne**, hvor de underliggende data for det pågældende felt har for mange forskellige værdier, reagerer browserfanen muligvis ikke og lukkes til sidst, hvilket kræver, at du starter forfra i en ny session. I dette tilfælde skal du enten undlade at dreje på feltet eller angive et filter på feltet, før du føjer det til området **Kolonnenavne**.

## Del dataanalyse

Når du har udarbejdet en analyse på en fane, kan du dele den som et link med kolleger og andre i organisationen direkte fra klienten. Kun modtagere, der har tilladelse til virksomheden og dataene, kan bruge linket.

1. Vælg pil ned under fanen Analyse, og vælg derefter **Kopiér link**.

   ![Viser handlingen til kopiering af en analyse](media/copy-analysis.svg)

   Dialogboksen **Link til \<tab name\>** åbnes.

1. Som standard linker den analyse, du deler, til den side eller forespørgsel i det firma, du arbejder i, hvilket er angivet i URL-feltet ved siden af `company=<company_name>` **Kopier**-knappen. Hvis du vil sende et link til en analyse, der ikke er knyttet til et bestemt regnskab, skal du angive feltet **Regnskab:** til **Opret ikke et link til et bestemt regnskab**.

   ![Viser dialogboksen Kopiér link for en analysefane](media/analysis-link-copied.svg)

1. Vælg **Kopier**.

1. Indsæt linket i et kommunikationsmedie efter eget valg, f.eks. Word, Outlook, Teams OneNote osv. 

2. Når det er modtaget, kan modtagerne derefter vælge linket og åbne analysen for siden eller forespørgslen i Business Central. De bliver bedt om at angive et navn til den nye analysefane, der oprettes.  

## Begrænsninger i udgivelsesbølge 1 i 2023 (prøveversion)

Den offentlige prøveversion af denne funktion har følgende begrænsninger:

- Analysens tilstandsvisning har en begrænsning på 100.000 rækker. Hvis du overskrider denne grænse, får du vist en meddelelse om dette. Hvis du vil omgå denne begrænsning, skal du angive filtre på siden, før du skifter til analysetilstand. Du kan f.eks. analysere en bestemt gruppe af kunder eller måske kun vil have data fra indeværende år. Du kan også vælge en foruddefineret visning, hvis den kunne bruges til analysen.
- Funktionen til analyse af delte data er ikke tilgængelig.
- Muligheden for at gemme foretrukne dataanalysevalg på listesider og gemme analysemenuer pr. analysefane er i øjeblikket ikke tilgængelig.

## Se også

[Ad hoc-dataanalyse](reports-adhoc-analysis.md)  
[Redigere og analysere i Excel](across-work-with-excel.md)  
