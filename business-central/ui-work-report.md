---
title: Arbejde med rapporter, kørsler og XMLporte
description: Få mere at vide om, hvordan du angiver en rapport i en opgavekø og planlægger, at den skal afvikles på en bestemt dato og tidspunkt.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.date: 06/21/2021
ms.author: jswymer
ms.openlocfilehash: d62c16ef8c511464fde86a1766499e37f8a07b1f
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972196"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Arbejde med rapporter, kørsler og XMLporte

En rapport indsamler oplysninger baseret på et nærmere angivet sæt kriterier. Den organiserer og præsenterer oplysninger i det læsevenlige format, som du kan udskrive eller gemme som en fil. Der er mange rapporter, du kan få adgang til, i hele programmet. Rapporterne indeholder typisk oplysninger i forhold til konteksten for den viste side. For eksempel indeholder siden **Debitor** rapporter om de 10 bedste kunder, salgsstatistik og mere.

Kørsler og XMLporte udfører mere eller mindre det samme som rapporter, men som bruges med henblik på at udføre en proces eller eksportere data. F.eks. opretter kørslen **Opret rykkere** rykkerdokumenter til debitorer med forfaldne betalinger.  

> [!NOTE]
> I dette emne omtales hovedsageligt "rapport", men lignende oplysninger gælder for kørsler og XMLporte.

## <a name="getting-started"></a>Introduktion

Du kan finde rapporter under fanen **Rapporter** på markerede sider, eller du kan bruge søgefunktionen ![Elpære, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") for at finde rapporter efter navn.

Når du åbner en rapport, en kørsel eller XMLport, får du typisk vist en anmodningsside, hvor du kan angive forskellige indstillinger og filtre, som bestemmer, hvad der skal med i rapporten. I følgende afsnit forklares det, hvordan du kan bruge anmodningssiden til at oprette, få vist og udskrive en rapport.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Bruge standardværdier - foruddefinerede indstillinger 

De fleste sider med anmodninger indeholder feltet **Brug standardværdier fra**. I dette felt kan du vælge foruddefinerede indstillinger for rapporten, som automatisk angiver indstillinger og filtre for rapporten. Vælg en post på rullelisten, og du kan se indstillingerne og filtrene på anmodningssiden i overensstemmelse med ændringerne.

Posten, som kaldes **Sidst anvendte indstillinger og filtre**, er altid tilgængelig. Denne post konfigurerer rapporten til at bruge indstillinger og filtre, der blev brugt sidste gang, du kørte rapporten.

feltet **Brug standardværdier fra** giver en hurtig og pålidelig metode til at oprette rapporter på, som indeholder de korrekte data. Når du har valgt en post, kan du ændre alle indstillinger og filtre, før du viser eller udskriver rapporten. De ændringer, du udfører, bliver ikke gemt i den post med foruddefinerede indstillinger, du har valgt, men de gemmes i posten **Seneste anvendte indstillinger og filtre**.

>[!NOTE]
> De foruddefinerede indstillinger konfigureres typisk og administreres af en administrator. Der er flere oplysninger i [Administrere gemte indstillinger for rapporter og kørsler](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-reports"></a>Angive dataene, der skal medtages i rapporter

Brug felterne under **Indstillinger** og **Filtre** til at ændre grænsen for de oplysninger, du vil have i rapporten. Du kan angive filtre i en rapport mere eller mindre på samme måde, som du angiver filtre på lister. Du kan finde flere oplysninger i [Filtrering](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Sektionen **Filtrer listen efter** på en anmodningsside indeholder en generel filtreringsfunktion for rapporter. Disse filtre er valgfrie.
>
> Nogle rapporter ignorerer disse filtre, hvilket vil sige, at uanset hvilket filter der er angivet i sektionen **Filtrer listen efter**, er resultatet af rapporten det samme. Det er ikke muligt at vise en oversigt over, hvilke felter der ignoreres i rapporterne, så du må prøve dig frem med filtrene.
>
> **Eksempel**: Når du bruger kørslen **Opret rykkere**, bliver et filter for feltet **Debitorposter** i **Niv. for sidst udstedte rykker** ignoreret, fordi filtrene er fastsat for kørslen.

## <a name="previewing-a-report"></a>Visning af en rapport

Når du får vist et eksempel på en rapport, kan du se, hvordan rapporten vil se ud, før du udskriver den. Eksemplet er ikke baseret på, at der vælges en printer i feltet **Printer** på anmodningssiden. Det styres af browseren. Når du har vist eksemplet, kan du gå tilbage til anmodningssiden og foretage ændringer af indstillinger og filtre efter behov.

Hvis du vil se et eksempel på en rapport, skal du vælge knappen **Eksempelvisning** eller **Vis udskrift og luk** på rapportanmodningssiden. Den knap, der vises, afhænger af rapporten, så nogle rapporter indeholder knappen **Eksempelvisning**, mens andre har knappen **Vis udskrift og luk**. Begge knapper åbner et eksempel på rapporten. Forskellen er, at i **Eksempelvisning** forbliver siden åben, så du kan gå tilbage til den, foretage ændringer, vise den igen eller udskrive. Med **Vis udskrift og luk**-anmodningssiden lukkes siden, så du skal åbne rapporten igen for at foretage ændringer eller udskrive.

> [!NOTE]
> Hvis du bruger Business Central 2020 udgivelsesbølge 1 eller ældre, vises kun knappen **Vis udskrift**, som lukker anmodningssiden ved eksempelvisning, som beskrevet for **Vis udskrift og luk**.

### <a name="working-with-the-preview"></a>Arbejde med forhåndsversion

Brug menulinjen i rapporteksemplet til at:

- Bladre gennem sider
- Zoome ind og ud
- Tilpasse til siden
- Vælg tekst

    Du kan kopiere tekst fra en rapport og derefter indsætte den et andet sted, f.eks. som en side i [!INCLUDE[prod_short](includes/prod_short.md)] eller Microsoft Word.  Hvis du bruger en mus, skal du f. eks. trykke på knappen og holde den nede, hvor du vil starte. Flyt derefter musen for at markere et eller flere ord, sætninger eller afsnit. Tryk på højre museknap, og vælg **Kopiér**. Indsæt den markerede tekst, hvor du ønsker.
- Panorer over dokumentet

    Du kan flytte det synlige område af rapporten i en vilkårlig retning, så du kan se andre områder eller rapporten. Panorering er nyttigt, når du har zoomet ind for at få vist detaljer.  Ved hjælp af musen f.eks. skal du trykke på og holde museknappen nede et vilkårligt sted i rapporteksemplet og derefter bevæge musen.

- Hent til en PDF-fil på din computer eller netværket.
- Udskriv

## <a name="saving-a-report-to-a-file"></a>Gemme en rapport i en fil

Du kan gemme en rapport som et PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-arbejdsark ved at vælge knappen **Send til**, og derefter vælge den ønskede indstilling.

### <a name="send-to-excel"></a>Send til Excel

<!-- The following table describes the options for saving the report results as a worksheet in an Excel workbook.

|Option  |Description  |
|---------|---------|
|Microsoft Excel Document (data and layout)|Export the report results with the RDLC layout applied. Use this option if you want to export the data one time, and only want to make minor changes to its appearance, such as font and color scheme. <br><br>**Note**: Some reports might export numbers as text, so it's a good idea to verify the numbers. |
|Microsoft Excel Document (data only)|Export the report results and the criteria that was used to generate them, such as the parameters you specified on the request page, metadata, and the fields that control the layout of the printed report. Use this option when you want to do ad hoc analysis of the data or diagnose data issues in reports. For example, you can filter the data and use Power Pivot to display it.<br><br>This option exports all columns, including columns that hold formatting instructions for other values and filters. In columns that hold binary data like images, instead of actually values, fields will include the text **Binary data ({0} bytes)**, where **{0}** indicates the number of bytes.<br><br>**NOTE** With Business Central on-premises, the Business Central Server includes a configurations setting, called **Max Data Rows Allowed to Send to Excel**. This setting limits the number of rows that can be exported to Excel. If you don't see the expected number of rows, it might be because of this setting. For more information, see [Configuring Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) or contact your administrator.|-->

Der er to indstillinger til at gemme rapportresultaterne som et regneark i en Excel-projektmappe: **Microsoft Excel-dokument (data og layout)** og **Microsoft Excel-dokument (kun data)**

#### <a name="microsoft-excel-document-data-and-layout"></a>[Microsoft Excel-dokument (data og layout)](#tab/data-and-layout)

Denne indstilling er kun tilgængelig i rapporter, der bruger et RDLC layout. Den eksporterer rapportresultaterne med det RDLC layout. Brug denne indstilling, hvis du vil eksportere dataene én gang og kun vil foretage mindre ændringer af dens udseende, f. eks. skrifttype og farveskema.

#### <a name="microsoft-excel-document-data-only"></a><a name="exportdataonly"></a>[Microsoft Excel-dokument (kun data)](#tab/data-only)

**Microsoft Excel-dokument (kun data)** eksporterer rapportresultaterne og de kriterier, der blev brugt til at oprette dem, men som ikke omfatter rapportlayoutet. Excel-filen vil indeholde hele datasættet, som rådata, arrangeret i rækker og kolonner. Alle datakolonner i rapportens datasæt medtages, uanset om de bruges i rapportlayoutet.  Brug denne indstilling, når du vil:

- Foretag ad hoc-analyse af dataene. Du kan f. eks. filtrere dataene og bruge Power Pivot til at få dem vist.

  Hver gang du eksporterer resultater, oprettes der et nyt regneark. Når du bruger **Microsoft Excel-dokument (kun data)** kan du udføre samme rapport og genbruge formateringsændringer. F.eks. for Power Pivot kan du køre rapporten igen i en anden tidsperiode, kopiere resultaterne til regnearket og derefter opdatere regnearket. Du kan også finde en app til rapportering på [AppSource](https://appsource.microsoft.com/).
- Undersøg rapportens datasæt, når du opretter eller ændrer brugerdefinerede rapportlayout.

  Oplysninger om oprettelse af brugerdefinerede rapportlayout finder du under [Oprette eller ændre brugerdefinerede rapport layouts](ui-how-create-custom-report-layout.md)
- Diagnosticere dataproblemer i rapporter.

##### <a name="for-administrators"></a>Til administratorer

- **Microsoft Excel-dokument (kun data)** blev introduceret som en valgfri funktion i 2021 Release Wave 1, opdatering 18,3. Hvis du vil give brugere adgang til denne funktion, skal du aktivere funktionen **Gem rapportdatasæt i Microsoft Excel-dokument** i **Funktionsstyring**. Du kan finde flere oplysninger i [Aktivere Upcoming Features Ahead of Time](/dynamics365/business-central/dev-itpro/administration/feature-management). I 2021: version Wave 2 er denne funktion permanent, så du behøver ikke at aktivere den.

- Brugerkonti har brug for **<!--Export Report Dataset To Excel-->Tillad handlingseksport af rapportdatasæt til Excel** tilladelse, som du kan anvende ved hjælp af tilladelsessættet **Fejlfinding** eller **Eksporter rapport til Excel**.  

- Du kan ikke eksportere en rapport, der indeholder mere end 1,048,576 rækker eller 16.384 kolonner.

    > [!NOTE]
    > Med Business Central lokalt kan det maksimale antal udlæste rækker være endnu mindre. Business central server indeholder en konfigurationsindstilling, der kaldes **Maks. antal tilladte datarækker, der kan sendes til Excel**, med henblik på at reducere grænsen fra maksimumværdien. Du kan finde flere oplysninger i [konfigurere Business central server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) eller ved at kontakte administratoren.

##### <a name="for-developers-and-advanced-users"></a>For udviklere og erfarne brugere

Funktionen **Microsoft Excel-dokument (kun data)** eksporterer alle kolonner, herunder kolonner, der indeholder filtre og oplysninger om formatering af andre værdier. Her er nogle af interessepunkterne:

- Binære data i et felt, f. eks. et billede, eksporteres ikke.

  I kolonner, der indeholder binære data, vil felter indeholde teksten **Binære data ({0} byte)**, hvor **{0}** angiver antallet af byte.
- Fra og med Business Central 2021 Release Wave 2 indeholder Excel-filen også regnearket **Rapport-metadata**.

  I dette regneark vises de filtre, der anvendes til rapporten, og de generelle rapportegenskaber, f. eks. navn, ID og udvidelsesdetaljer. Filtrene vises i kolonnen **Filter (dataelement::tabel::FilterGroupNo::feltnavn)**. Filtrene i denne kolonne indeholder filtersæt, der er angivet på rapportens anmodningsside. Den indeholder også filtre, der er defineret i AL kode, f. eks. ved at bruge [egenskaben DataItemLink](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) og [egenskaben DataItemTableView](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Du kan finde flere oplysninger om rapportdesign i [rapportoversigt](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

---

> [!NOTE]
> Nogle rapporter eksporterer tal som tekst, hvilket forhindrer dig i at foretage beregninger eller bruge Power Pivot på celler i Excel-regnearket. Når det er eksporteret, er det en god ide at kontrollere tallene i kladden. Hvis du vil analysere og planlægger tallene, skal du ændre formatet af de relevante celler fra **tekst** til **tal**. Du kan finde flere oplysninger om formatering af tal i celler i denne video [formateringsnumre i celler i Microsoft Excel](https://www.youtube.com/watch?v=2suE4YmZu_Q).

### <a name="microsoft-word-document"></a>Microsoft Word Dokument
Brug indstillingen **Microsoft Word Dokument** til at oprette en rapport som et Word-dokument.  

> [!NOTE]
> Du kan angive det layout, der skal bruges til hver rapport på siden **Rapportvalg**, i det **valgte layout**-felt. Standardindstillingen for rapporter er **RDLC (indbygget)**, som producerer rapporter i samme eller tilsvarende layout som **Microsoft Word Dokument**-layoutet. Men nøgleforskellen er, om du vil oprette et eller flere rapportdokumenter. Du kan bruge indstillingen RDLC (indbygget) til enkelte dokumenter. Hvis det er flere dokumenter, skal du angive **Microsoft Word Dokument** som standardlayout for rapporten. Du kan finde flere oplysninger i [Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md).

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Planlægge kørsel af en rapport

Du kan planlægge kørsel af en rapport på en bestemt dato og et bestemt klokkeslæt. Planlagte rapporter og kørsler indsættes i jobkøen og behandles på det planlagte tidspunkt, ligesom andre job. Du vælger indstillingen **Skema**, når du har valgt knappen **Send til**, og derefter angiver du oplysninger som f.eks. printer og klokkeslæt og dato. Rapporten føjes derefter til opgavekøen og køres på det angivne tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobkøen. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).  

Når du planlægger en rapport til kørsel, kan du angive, at den skal køre hver torsdag, ved at angive feltet **Datoformel for næste kørsel** til f.eks. *D4*. Du kan finde flere oplysninger i [Bruge datoformler](ui-enter-date-ranges.md#using-date-formulas).  

Du kan vælge at gemme den behandlede rapport i en fil (f.eks. Excel, Word eller PDF), udskrive den til den ønskede printer eller kun generere rapporten. Hvis du vælger at gemme rapporten i en fil, bliver den behandlede rapport sendt til området **Rapportindbakke** i dit rollecenter, hvor du kan se den.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Udskrive en rapport

Du kan udskrive en rapport ved at vælge knappen **Udskriv** på rapportanmodningssiden eller på menulinjen på siden **Eksempel**.

### <a name="printer"></a><a name="Printer"></a>Printer

Feltet **Printer** på rapportanmodningssiden viser navnet på den printer, rapporten sendes til. Hvis du vil ændre en printer, skal du blot vælge printeren på listen.

> [!NOTE]
> **(Håndteres af browseren)** angiver, at der ikke er tildelt en printer til rapporten. I dette tilfælde vil browseren håndtere udskriften og vise en standard oplevelse, hvor du kan vælge en lokal printer, der er tilsluttet enheden. **(Håndteres af browseren)** er ikke tilgængelig i mobilappen [!INCLUDE[prod_short](includes/prod_short.md)] eller appen til Microsoft Teams.

> [!TIP]
> Den printer, der er valgt som standard, er konfigureret på siden **Printervalg**. Du kan finde flere oplysninger om ændring af standardprinteren i [Sådan vælger du, hvilke printere der skal udskrive hvilke rapporter](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Udskrive rapporter på thailandsk

Knappen **Udskriv** er specifik for Thai-versionen af [!INCLUDE[prod_short](includes/prod_short.md)], men kan ikke udskrive rapporter korrekt pga. begrænsninger i den tjeneste, der genererer PDF-filen, som kan udskrives. Du kan i stedet åbne rapporten i Word og derefter gemme rapporten som en PDF-fil, der kan udskrives.  

Du kan også bede administratoren om at oprette et Word-rapportlayout til de mest anvendte rapporter. Du kan finde flere oplysninger i [Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Ændre rapportlayout

Et rapportlayout bestemmer, hvad der skal vises i en rapport, hvordan det arrangeres, og hvilken typografi der anvendes. Hvis du vil skifte til et andet layout, kan du se [Ændre det aktuelle rapportlayout](ui-how-change-layout-currently-used-report.md). Eller du kan tilpasse din egen rapportlayout, skal du se [Oprette et brugerdefineret rapportlayout](ui-how-create-custom-report-layout.md).

## <a name="advanced-options"></a>Avancerede indstillinger

Felterne under **Avanceret** angiver begrænsninger for den genererede rapport til styring af printerressourcer. Du behøver normalt ikke at ændre disse indstillinger, medmindre du har en stor rapport. Hvis en rapport overskrider disse begrænsninger, når du prøver at få vist eller udskrive, vises der en meddelelse om, hvilken begrænsning der er overskredet. Du kan derefter ændre indstillingerne, så de passer til din rapport. Hvert felt har imidlertid en maksimumværdi, som du skal være opmærksom på:

|Felt|Maksimumværdi|
|-----|-------------|
|Maksimal gengivelsestid:|12:00:00|
|Maks. antal rækker|1000000|
|Maksimalt antal dokumenter|500|

> [!NOTE]
> De maksimale værdier kan være forskellige for [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, og en administrator kan ændre dem. Du kan finde flere oplysninger i [Konfiguration af Business Central Server - Rapporter](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Du kan få vist en oversigt over rapporters begrænsninger [!INCLUDE[prod_short](includes/prod_short.md)] online i [Driftsgrænser](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Se også

[Installation af printere](ui-specify-printer-selection-reports.md)  
[Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md)  
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]