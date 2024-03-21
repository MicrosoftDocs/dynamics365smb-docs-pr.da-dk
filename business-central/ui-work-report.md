---
title: Køre og udskrive rapporter
description: 'Få mere at vide om, hvordan du angiver en rapport i en opgavekø og planlægger, at den skal afvikles på en bestemt dato og tidspunkt.'
author: jswymer
ms.author: jswymer
ms.reviewer: altotovi
ms.topic: conceptual
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.search.form: null
ms.date: 09/04/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Køre og udskrive rapporter

En rapport indsamler oplysninger baseret på et nærmere angivet sæt kriterier. Den organiserer og præsenterer oplysninger i det læsevenlige format, som du kan udskrive eller gemme som en fil. Der er mange rapporter, du kan få adgang til, i hele programmet. Rapporterne indeholder typisk oplysninger i forhold til konteksten for den viste side. For eksempel indeholder siden **Debitor** rapporter om de 10 bedste kunder, salgsstatistik og mere.

> [!NOTE]
> Kørsler og XMLporte udfører mere eller mindre det samme som rapporter, men som bruges med henblik på at udføre en proces eller eksportere data. F.eks. opretter kørslen **Opret rykkere** rykkerdokumenter til debitorer med forfaldne betalinger. I denne artikel omtales hovedsageligt "rapporter", men lignende oplysninger gælder for kørsler og XMLporte.

## Kom i gang

Du kan finde rapporter i menuen **Rapporter** på markerede sider, lister og kort, eller du kan bruge søgefunktionen ![Lightbulb, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"). for at finde rapporter efter navn. Du kan se en oversigt over indbyggede rapporter, som du kan bruge i [!INCLUDE[prod_short](includes/prod_short.md)]sorteret efter kategorier, i [Tilgængelige rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md).

Når du vælger en rapport, får du typisk vist en anmodningsside - opkaldt efter rapportens navn - hvor du kan angive forskellige indstillinger og filtre, som bestemmer, hvilke data der skal inkluderes. I følgende afsnit forklares det, hvordan du kan bruge anmodningssiden til at oprette, få vist og udskrive en rapport.

## <a name="SavedSettings"></a>Bruge standardværdier - foruddefinerede indstillinger

De fleste rapporter med anmodninger indeholder feltet **Brug standardværdier fra**. I dette felt kan du vælge foruddefinerede indstillinger for rapporten, som automatisk angiver indstillinger og filtre. Vælg en post på rullelisten, og du kan se indstillingerne og filtrene på anmodningssiden i overensstemmelse med ændringerne.

Posten, som kaldes **Sidst anvendte indstillinger og filtre**, er altid tilgængelig. Denne post konfigurerer rapporten til at bruge indstillinger og filtre, der blev brugt sidste gang, du kørte rapporten.

feltet **Brug standardværdier fra** giver en hurtig og pålidelig metode til at oprette rapporter på, som indeholder de korrekte data. Når du har valgt en post, kan du ændre alle indstillinger og filtre, før du viser eller udskriver rapporten. De ændringer, du udfører, bliver ikke gemt i den post med foruddefinerede indstillinger, du har valgt, men de gemmes i posten **Seneste anvendte indstillinger og filtre**.

> [!NOTE]
> De foruddefinerede indstillinger konfigureres typisk og administreres af en administrator. Flere oplysninger [Administrere gemte indstillinger for rapporter og kørsler](reports-saving-reusing-settings.md).

## Angive dataene, der skal medtages i rapporter

Brug felterne under **Indstillinger** og **Filtre** til at ændre eller begrænse de oplysninger, du vil have i rapporten. Du kan angive filtre i en rapport mere eller mindre på samme måde, som du angiver filtre på lister. Der er flere oplysninger i [Filtrering](ui-enter-criteria-filters.md#filtering)-afsnittet.

> [!CAUTION]
> Oversigtspanelet **Filtrer** på en rapportanmodningsside indeholder en generel filtreringsfunktion for rapporter. Disse filtre er valgfrie.
>
> Nogle rapporter ignorerer disse filtre, hvilket vil sige, at uanset hvilket filter der er angivet i oversigtspanelet **Filtrer**, er resultatet af rapporten det samme. Det er ikke muligt at vise en oversigt over, hvilke felter der ignoreres i rapporterne, så du må prøve dig frem med filtrene.
>
> **Eksempel**: Når du bruger kørslen **Opret rykkere**, bliver et filter for feltet **Debitorposter** i **Niv. for sidst udstedte rykker** ignoreret, fordi filtrene er fastsat for kørslen.

## Visning af en rapport

Når du får vist et eksempel på en rapport, kan du se, hvordan rapporten vil se ud, før du udskriver den. Eksemplet er ikke baseret på, at der vælges en printer i feltet **Printer** på anmodningssiden. Det styres af browseren. Når du har vist eksemplet, kan du gå tilbage til anmodningssiden og foretage ændringer af indstillinger og filtre efter behov.

Vælg Forhåndsversionsvalgene på siden **Rapportanmodning** afhænger af rapporten. Du kan vælge **Forhåndsversion** for nogle rapporter, men valget for andre er få **Forhåndsversion og luk**. Begge valg åbner et eksempel på rapporten. Forskellen er, at i **Eksempelvisning** forbliver siden åben, så du kan gå tilbage til den, foretage ændringer, vise den igen eller udskrive. Med **Forhåndsversion og luk**-anmodningssiden lukkes siden, så du skal åbne rapporten igen for at foretage ændringer eller udskrive.

> [!NOTE]
> Hvis du bruger Business Central 2020 udgivelsesbølge 1 eller ældre, vises kun knappen **Forhåndsversion**, som lukker anmodningssiden ved eksempelvisning, som beskrevet for **Forhåndsversion og luk**.

### Arbejde med forhåndsversion

Brug menulinjen i rapporteksemplet til at:

- Bladre gennem sider
- Zoome ind og ud
- Tilpasse til siden
- Vælg tekst

    Du kan kopiere tekst fra en rapport og derefter indsætte den et andet sted, f.eks. som en side i [!INCLUDE[prod_short](includes/prod_short.md)] eller Microsoft Word. Hvis du bruger en mus, skal du f. eks. vælge den vestre museknap og holde den nede, hvor du vil starte. Flyt derefter musen for at markere et eller flere ord, sætninger eller afsnit. Tryk derefter på højre museknap, og vælg **Kopiér**. Du kan nu indsætte den markerede tekst, hvor du ønsker.
- Panorer over dokumentet

    Du kan flytte det synlige område af rapporten i en vilkårlig retning, så du kan se andre områder eller rapporten. Panorering er nyttigt, når du har zoomet ind for at få vist detaljer. Ved hjælp af musen f.eks. skal du vælge og holde museknappen nede et vilkårligt sted i rapporteksemplet og derefter bevæge musen for at vælge et afsnit af rapporten.

- Hent til en PDF-fil på din computer eller netværket.
- Udskriv

## Gemme en rapport i en fil

Du kan gemme en rapport som et PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-projektmappe eller XML-dokument ved at vælge **Send til**, og derefter vælge den ønskede indstilling. En fil vil blive downloadet på din enhed.

Hvis organisationen har konfigureret OneDrive til systemfunktioner i stedet for at blive hentet, åbnes Excel-projektmapper og Word-dokumenter i browseren fra enten Microsoft Excel eller Microsoft Word til World Wide Web.

> [!TIP]
> **Microsoft Excel-dokument (kun data)** og **XML-dokument** er hovedsageligt til avancerede formål. Du bruger typisk disse indstillinger til at udføre detaljeret dataanalyse. Flere oplysninger [Analyse af rapportdata med Excel og XML](report-analyze-excel.md).
>
> Du kan også bruge **Microsoft Excel-dokumentet (kun data)** til at oprette nye Excel-layout til en bestemt rapport. Flere oplysninger i [Arbejde med Excel-layouts](ui-excel-report-layouts.md).  

## <a name="ScheduleReport"></a> Planlægge senere eller periodisk kørsel af en rapport

Du kan planlægge enkelt eller gentagne kørsel(ler) af en rapport på en bestemt dato og et bestemt klokkeslæt. Planlagte rapporter indsættes i jobkøen og behandles på det planlagte tidspunkt, ligesom andre job. Du vælger indstillingen **Skema**, når du har valgt knappen **Send til**, og derefter angiver du oplysninger som f.eks. printer og klokkeslæt og dato. Rapporten føjes derefter til opgavekøen og køres på det angivne tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobkøen. Flere oplysninger under [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).  

Når du planlægger en rapport til kørsel, kan du angive, at den skal køre hver torsdag, ved at angive feltet **Datoformel for næste kørsel** til f.eks. *D4*. Du kan finde flere oplysninger i [Bruge datoformler](ui-enter-date-ranges.md#use-date-formulas).  

Du kan vælge at gemme den behandlede rapport i en fil (f.eks. Excel, Word eller PDF), udskrive den til den ønskede printer eller kun generere rapporten. Hvis du vælger at gemme rapporten i en fil, bliver den behandlede rapport sendt til området **Rapportindbakke** i dit rollecenter, hvor du kan se den. Flere oplysninger i [Dele og eksportere rapporter med rapportindbakken](ui-work-report-inbox.md)

### Administrere planlagte gentagelsesrapporter

Planlagte rapporter genereres af batchjob, der administreres på siden **Opgavekøposter**. Du kan se status og andre oplysninger for hver rapport på siden, sætte en pause/genoptage rapport batchjobbet og generere rapporten efter behov.

Du kan også bruge siden **Opgavekøposter** til at ændre nogle rapportparametre, f. eks. outputfilens filtype, gentagelse, kørselsdato og start- og sluttidspunkt. Før du redigerer en eksisterende planlagt rapport, er det imidlertid nødvendigt at sætte rapport jobkøen i venteposition:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Opgavekøposter**, og vælg derefter det relaterede link.  
2. På siden **Opgavekøposter** skal du vælge den ønskede rapport.
3. Vælg handlingen **Indstil på Hold**.
4. Åbn og Rediger den planlagte rapport ved at vælge dens status (*i venteposition*).

Når du har redigeret rapportindstillingerne, skal du gentage de to første trin og derefter markere feltet **Angiv status som klar**-handling for at genoptage oprettelsen af rapporten.

Få mere at vide om styring af jobkøer i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).  

## <a name="PrintReport"></a>Udskrive en rapport

Du kan udskrive en rapport ved at vælge **Udskriv** på rapportanmodningssiden eller på menulinjen på siden **Eksempel**.

Når en rapport bruger Excel-layout, kan du ikke se feltet **Printer**, knappen **Udskriv** eller **Vis udskrift**. Der findes i stedet en knap **Download**. Hvis du vil udskrive, skal du vælge **Download** og derefter åbne den hentede fil i Excel og udskrive derfra.

### <a name="Printer"></a>Printer

Feltet **Printer** på rapportanmodningssiden viser navnet på den printer, rapporten sendes til. Hvis du vil ændre en printer, skal du blot vælge printeren på listen.

> [!NOTE]
> Indstillingen **(Håndteres af browseren)**, at der ikke er en udvalgt printer til rapporten. I dette tilfælde vil browseren håndtere udskriften og vise en standard oplevelse, hvor du kan vælge en lokal printer, der er tilsluttet enheden. Indstillingen **(Håndteres af browseren)** er ikke tilgængelig i mobilappen [!INCLUDE[prod_short](includes/prod_short.md)] eller appen til Microsoft Teams.

> [!TIP]
> Den printer, der er valgt som standard, er konfigureret på siden **Printervalg**. Få mere at vide om at ændre standardprinteren i [Konfigurere standardprintere](ui-specify-printer-selection-reports.md#default).

### Udskrive rapporter på thailandsk

Knappen **Udskriv** er specifik for Thai-versionen af [!INCLUDE[prod_short](includes/prod_short.md)], men kan ikke udskrive rapporter korrekt pga. begrænsninger i den tjeneste, der genererer PDF-filen, som kan udskrives. Du kan i stedet åbne rapporten i Word og derefter gemme rapporten som en PDF-fil, der kan udskrives.  

Du kan også bede administratoren om at oprette et Word-rapportlayout til de mest anvendte rapporter. Flere oplysninger i [Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md).  

## Skifte rapportlayoutet

Et rapportlayout bestemmer, hvad der skal vises i en rapport, hvordan det arrangeres, og hvilken typografi der anvendes. Dette kan gøres på et par måder:

- Når du opretter en rapport, kan du se det aktuelle layout i feltet **Rapportlayout** på anmodningssiden. Hvis du vil midlertidigt skifte til et andet layout, skal du markere feltet **Rapportlayout** og derefter vælge på en liste over de tilgængelige layout for denne rapport.
- Hvis du vil ændre det standardlayout, der anvendes af en rapport, skal du gå til siden med **rapportlayout** eller **markering af rapportlayout**.

Flere oplysninger [Angive det layout, der bruges af en rapport](ui-set-report-layout.md). Eller du kan tilpasse din egen rapportlayout, skal du se [Introduktion til oprettelse af layout](ui-get-started-layouts.md).

## Ændre sprog og format for tal, datoer og klokkeslæt

Sproget i tal og format af tal, datoer og klokkeslæt er som standard baseret på dine indstillinger for arbejdssprog og område, der er defineret på siden **Mine indstillinger**. Du kan imidlertid ændre sproget og formatområdet i tilfælde af, hvordan du får vist, udskriver eller sender en rapport. Vælg **Sprog** på anmodningssiden, og angiv derefter indstillingerne for **Formatområde** efter behov. Du kan også angive det sprog- og områdeformat, der som standard skal bruges for debitorer og kreditorer på deres kortsider.

Afhængigt af hvor du har angivet sprog- og formatindstillingerne, bestemmer [!INCLUDE [prod_short](includes/prod_short.md)] de indstillinger, der skal bruges i følgende rækkefølge:

1. De indstillinger, du angiver, når du genererer en rapport.
2. De indstillinger, der er angivet i dokumentet, og som stammer fra debitorens eller kreditorens indstillinger.
3. De indstillinger, der er angivet for objektet Rapport-AL.
4. De indstillinger, der er defineret i Mine indstillinger.

Du kan finde flere oplysninger om **Mine indstillinger** ved at gå til [Ændre basisindstillinger](ui-change-basic-settings.md#region).

## Avancerede indstillinger

Felterne under oversigtspanelet **Avanceret** angiver begrænsninger for den genererede rapport til styring af printerressourcer. Du behøver normalt ikke at ændre disse indstillinger, medmindre du har en stor rapport. Hvis en rapport overskrider disse begrænsninger, når du prøver at få vist eller udskrive, vises der en meddelelse om, hvilken begrænsning der er overskredet. Du kan derefter ændre indstillingerne, så de passer til din rapport. Hvert felt har imidlertid en maksimumværdi, som du skal være opmærksom på:

|Felt|Maksimumværdi|
|-----|-------------|
|Maksimal gengivelsestid:|12:00:00|
|Maks. antal rækker|1000000|
|Maksimalt antal dokumenter|500|

> [!NOTE]
> De maksimale værdier kan være forskellige for [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, og en administrator kan ændre dem. Flere oplysninger i [Konfiguration af Business Central Server - Rapporter](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Du kan få vist en oversigt over rapportbegrænsninger i [!INCLUDE[prod_short](includes/prod_short.md)] online i [Driftsgrænser](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## Se også

[Tilgængelige rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Bruge rapporter i dagligt arbejde](reports-use-reports.md)  
[Oversigt over Business Intelligence og rapportering](reports-bi-reporting.md)  
[Installation af printere](ui-specify-printer-selection-reports.md)  
[Udføre kørsler og XMLporte](ui-how-run-batch-jobs.md)  
[Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md)  
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Økonomisk Business Intelligence](bi.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
