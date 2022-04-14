---
title: Køre og udskrive rapporter
description: Få mere at vide om, hvordan du angiver en rapport i en opgavekø og planlægger, at den skal afvikles på en bestemt dato og tidspunkt.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 03/24/2022
ms.author: jswymer
ms.openlocfilehash: fade19b2ecb4d2c17b5d5775074f2f715496a908
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512676"
---
# <a name="run-and-print-reports"></a>Køre og udskrive rapporter

En rapport indsamler oplysninger baseret på et nærmere angivet sæt kriterier. Den organiserer og præsenterer oplysninger i det læsevenlige format, som du kan udskrive eller gemme som en fil. Der er mange rapporter, du kan få adgang til, i hele programmet. Rapporterne indeholder typisk oplysninger i forhold til konteksten for den viste side. For eksempel indeholder siden **Debitor** rapporter om de 10 bedste kunder, salgsstatistik og mere.

Kørsler og XMLporte udfører mere eller mindre det samme som rapporter, men som bruges med henblik på at udføre en proces eller eksportere data. F.eks. opretter kørslen **Opret rykkere** rykkerdokumenter til debitorer med forfaldne betalinger.  

> [!NOTE]
> I dette emne omtales hovedsageligt "rapport", men lignende oplysninger gælder for kørsler og XMLporte.

## <a name="get-started"></a>Kom i gang

Du kan finde rapporter under fanen **Rapporter** på markerede sider, eller du kan bruge søgefunktionen ![Elpære, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") for at finde rapporter efter navn.

Når du åbner en rapport, en kørsel eller XMLport, får du typisk vist en anmodningsside, hvor du kan angive forskellige indstillinger og filtre, som bestemmer, hvad der skal med i rapporten. I følgende afsnit forklares det, hvordan du kan bruge anmodningssiden til at oprette, få vist og udskrive en rapport.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Bruge standardværdier - foruddefinerede indstillinger

De fleste sider med anmodninger indeholder feltet **Brug standardværdier fra**. I dette felt kan du vælge foruddefinerede indstillinger for rapporten, som automatisk angiver indstillinger og filtre for rapporten. Vælg en post på rullelisten, og du kan se indstillingerne og filtrene på anmodningssiden i overensstemmelse med ændringerne.

Posten, som kaldes **Sidst anvendte indstillinger og filtre**, er altid tilgængelig. Denne post konfigurerer rapporten til at bruge indstillinger og filtre, der blev brugt sidste gang, du kørte rapporten.

feltet **Brug standardværdier fra** giver en hurtig og pålidelig metode til at oprette rapporter på, som indeholder de korrekte data. Når du har valgt en post, kan du ændre alle indstillinger og filtre, før du viser eller udskriver rapporten. De ændringer, du udfører, bliver ikke gemt i den post med foruddefinerede indstillinger, du har valgt, men de gemmes i posten **Seneste anvendte indstillinger og filtre**.

>[!NOTE]
> De foruddefinerede indstillinger konfigureres typisk og administreres af en administrator. Der er flere oplysninger i [Administrere gemte indstillinger for rapporter og kørsler](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-a-report"></a>Angive dataene, der skal medtages i rapporter

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

### <a name="work-with-the-preview"></a>Arbejde med forhåndsversion

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

Du kan gemme en rapport som et PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-arbejdsark eller XML-dokument ved at vælge knappen **Send til**, og derefter vælge den ønskede indstilling.

> [!TIP]
> **Microsoft Excel-dokument (kun data)** og **XML-dokument** er hovedsageligt til avancerede formål. Du bruger typisk disse indstillinger til at udføre detaljeret dataanalyse. Du kan finde flere oplysninger i [Analyse af rapportdata med Excel og XML](report-analyze-excel.md).
>
> Du kan også bruge **Microsoft Excel-dokumentet (kun data)** til at oprette nye Excel-layout til en bestemt rapport. Du kan finde flere oplysninger i [Arbejde med Excel-layout](ui-excel-report-layouts.md).  
  
<!--
### About sending to Word

Use the **Microsoft Word Document** option to generate a report as a Word document.  

> [!NOTE]
> You can specify the layout to use for each report on the **Report Selection** page in the **Selected Layout** field. The default setting for reports is **RDLC (built-in)**, which produces reports in the same, or similar, layout as the **Microsoft Word Document** layout. However, the key difference is whether you want to generate a single or multiple report documents. For single documents, you can use the RDLC (built-in) option. For multiple documents, set the **Microsoft Word Document** as the default layout for the report. For more information, see [Managing Report and Document Layouts](ui-manage-report-layouts.md).

-->

## <a name="scheduling-a-report-to-run-later"></a><a name="ScheduleReport"></a> Planlægge senere kørsel af en rapport

Du kan planlægge kørsel af en rapport på en bestemt dato og et bestemt klokkeslæt. Planlagte rapporter og kørsler indsættes i jobkøen og behandles på det planlagte tidspunkt, ligesom andre job. Du vælger indstillingen **Skema**, når du har valgt knappen **Send til**, og derefter angiver du oplysninger som f.eks. printer og klokkeslæt og dato. Rapporten føjes derefter til opgavekøen og køres på det angivne tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobkøen. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).  

Når du planlægger en rapport til kørsel, kan du angive, at den skal køre hver torsdag, ved at angive feltet **Datoformel for næste kørsel** til f.eks. *D4*. Du kan finde flere oplysninger i [Bruge datoformler](ui-enter-date-ranges.md#use-date-formulas).  

Du kan vælge at gemme den behandlede rapport i en fil (f.eks. Excel, Word eller PDF), udskrive den til den ønskede printer eller kun generere rapporten. Hvis du vælger at gemme rapporten i en fil, bliver den behandlede rapport sendt til området **Rapportindbakke** i dit rollecenter, hvor du kan se den.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Udskrive en rapport

Du kan udskrive en rapport ved at vælge knappen **Udskriv** på rapportanmodningssiden eller på menulinjen på siden **Eksempel**.

Når en rapport bruger Excel-layout, kan du ikke se feltet **Printer**, knappen **Udskriv** eller **Vis udskrift**. Der findes i stedet en knap **Download**. Hvis du vil udskrive, skal du vælge **Download** og derefter åbne den hentede fil i Excel og udskrive derfra.

### <a name="printer"></a><a name="Printer"></a>Printer

Feltet **Printer** på rapportanmodningssiden viser navnet på den printer, rapporten sendes til. Hvis du vil ændre en printer, skal du blot vælge printeren på listen.

> [!NOTE]
> **(Håndteres af browseren)** angiver, at der ikke er tildelt en printer til rapporten. I dette tilfælde vil browseren håndtere udskriften og vise en standard oplevelse, hvor du kan vælge en lokal printer, der er tilsluttet enheden. **(Håndteres af browseren)** er ikke tilgængelig i mobilappen [!INCLUDE[prod_short](includes/prod_short.md)] eller appen til Microsoft Teams.

> [!TIP]
> Den printer, der er valgt som standard, er konfigureret på siden **Printervalg**. Du kan finde flere oplysninger om ændring af standardprinteren i [Sådan vælger du, hvilke printere der skal udskrive hvilke rapporter](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Udskrive rapporter på thailandsk

Knappen **Udskriv** er specifik for Thai-versionen af [!INCLUDE[prod_short](includes/prod_short.md)], men kan ikke udskrive rapporter korrekt pga. begrænsninger i den tjeneste, der genererer PDF-filen, som kan udskrives. Du kan i stedet åbne rapporten i Word og derefter gemme rapporten som en PDF-fil, der kan udskrives.  

Du kan også bede administratoren om at oprette et Word-rapportlayout til de mest anvendte rapporter. Du kan finde flere oplysninger i [Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md).  

## <a name="switching-the-report-layout"></a>Skifte rapportlayoutet

Et rapportlayout bestemmer, hvad der skal vises i en rapport, hvordan det arrangeres, og hvilken typografi der anvendes. Hvis du vil skifte til et andet layout, kan du se [Angive det layout, der bruges af en rapport](ui-set-report-layout.md). Eller du kan tilpasse din egen rapportlayout, skal du se [Introduktion til oprettelse af layout](ui-get-started-layouts.md).

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
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]