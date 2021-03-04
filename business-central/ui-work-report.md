---
title: Planlægge en rapport til kørsel på en bestemt dato og et bestemt klokkeslæt | Microsoft Docs
description: Få mere at vide om, hvordan du angiver en rapport i en opgavekø og planlægger, at den skal afvikles på en bestemt dato og tidspunkt.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: e4b1615ebf177db94e3dfb372809fa71ed2f1459
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760163"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Arbejde med rapporter, kørsler og XMLporte

En rapport indsamler oplysninger, der er baseret på et bestemt sæt kriterier, og organiserer og præsenterer oplysningerne i et format, der er let at læse, og som du kan udskrive eller gemme som en fil. Der er mange rapporter, du kan få adgang til, i hele programmet. Rapporterne indeholder typisk oplysninger i forhold til konteksten for den viste side. For eksempel indeholder siden **Debitor** rapporter om de 10 bedste kunder, salgsstatistik og mere.

Kørsler og XMLporte udfører mere eller mindre det samme som rapporter, men med henblik på at udføre en proces eller eksportere data. F.eks. opretter kørslen **Opret rykkere** rykkerdokumenter til debitorer med forfaldne betalinger.  

> [!NOTE]
> I dette emne omtales hovedsageligt "rapport", men lignende oplysninger gælder for kørsler og XMLporte.

## <a name="getting-started"></a>Introduktion

Du kan finde rapporter under fanen **Rapporter** på markerede sider, eller du kan bruge søgefunktionen ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") til at finde rapporter efter navn.

Når du åbner en rapport, en kørsel eller XMLport, får du typisk vist en anmodningsside, hvor du kan angive forskellige indstillinger og filtre, som bestemmer, hvad der skal med i rapporten. I følgende afsnit forklares det, hvordan du kan bruge anmodningssiden til at oprette, få vist og udskrive en rapport.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Bruge standardværdier - foruddefinerede indstillinger 

De fleste sider med anmodninger indeholder feltet **Brug standardværdier fra**. I dette felt kan du vælge foruddefinerede indstillinger for rapporten, som automatisk angiver indstillinger og filtre for rapporten. Vælg en post på rullelisten, og du kan se indstillingerne og filtrene på anmodningssiden i overensstemmelse med ændringerne.

Posten, som kaldes **Sidst anvendte indstillinger og filtre**, er altid tilgængelig. Denne post konfigurerer rapporten til at bruge indstillinger og filtre, der blev brugt sidste gang, du kørte rapporten.

feltet **Brug standardværdier fra** giver en hurtig og pålidelig metode til at oprette rapporter på, som indeholder de korrekte data. Når du har valgt en post, kan du ændre alle indstillinger og filtre, før du viser eller udskriver rapporten. De ændringer, du udfører, bliver ikke gemt i den post med foruddefinerede indstillinger, du har valgt, men de gemmes i posten **Seneste anvendte indstillinger og filtre**.

>[!NOTE]
> De foruddefinerede indstillinger konfigureres typisk og administreres af en administrator. Der er flere oplysninger i [Administrere gemte indstillinger for rapporter og kørsler](reports-saving-reusing-settings.md).
<!--
Depending on the report, the request page might include the **Use default values from** field. This field lets you select a predefined set of can include the **Saved Settings** section that contains one or more entries in the **Use default value from** box. A saved setting is basically a predefined group of options and filters that you can apply to the report before previewing or sending the report to a file. The saved settings entry called **Last used options and filters** is always available. This entry sets the report to use options and filters that were used the last time you used the report.

Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data. After you set the **Use default value from** box to a saved settings entry, you can change any of the options and filters before previewing or saving the report. The changes that you make will not be saved to the saved settings entry you selected, but they will be saved to the **Last used options and filters** entry.

>[!NOTE]
>If you are an administrator, you can create and manage the saved settings for reports for all users. For more information, see [Manage Saved Settings for Reports and Batch Jobs](reports-saving-reusing-settings.md).
-->
## <a name="specifying-the-data-to-include-in-reports"></a>Angive de data, der skal medtages i rapporter

Brug felterne under **Indstillinger** og **Filtre** til at ændre grænsen for de oplysninger, du vil have i rapporten. Du kan angive filtre i en rapport mere eller mindre på samme måde, som du angiver filtre på lister. Du kan finde flere oplysninger i [Filtrering](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Sektionen **Filtrer listen efter** på en anmodningsside indeholder en generel filtreringsfunktion for rapporter. Disse filtre er valgfrie.
>
> Nogle rapporter ignorerer disse filtre, hvilket vil sige, at uanset hvilket filter der er angivet i sektionen **Filtrer listen efter**, er resultatet af rapporten det samme. Det er ikke muligt at vise en oversigt over, hvilke felter ignoreres i rapporterne, så du må prøve dig frem med filtrene, når du bruger dem.
>
> **Eksempel**: Når du bruger kørslen **Opret rykkere**, bliver et filter for feltet **Debitorposter** i **Niv. for sidst udstedte rykker** ignoreret, fordi filtrene er fastsat for kørslen.

## <a name="previewing-a-report"></a>Visning af en rapport

Når du får vist et eksempel på en rapport, kan du se, hvordan rapporten vil se ud, før du udskriver den. Eksempelvisningen illustrerer rapporten på baggrund af den [printer](#Printer), der vises i feltet **Printer** på anmodningssiden. Når du har vist eksemplet, kan du gå tilbage til anmodningssiden og foretage ændringer af indstillinger og filtre efter behov.

Hvis du vil se et eksempel på en rapport, skal du vælge knappen **Eksempelvisning** eller **Vis udskrift og luk** på rapportanmodningssiden. Den knap, der vises, afhænger af rapporten, så nogle rapporter indeholder knappen **Eksempelvisning**, mens andre har knappen **Vis udskrift og luk**. Begge knapper åbner et eksempel på rapporten. Forskellen er, at i **Eksempelvisning** forbliver siden åben, så du kan gå tilbage til den, foretage ændringer, vise den igen eller udskrive. Med **Vis udskrift og luk**-anmodningssiden lukkes siden, så du skal åbne rapporten igen for at foretage ændringer eller udskrive.

> [!NOTE]
> Hvis du bruger Business Central 2020 release wave 1 eller tidligere, er der kun en **Vis udskrift**-knap, som lukker anmodningssiden i forbindelse med eksempelvisning, som beskrevet for **Vis udskrift og luk**.

### <a name="working-with-the-preview"></a>Arbejde med eksempelvisning

Brug menulinjen i rapporteksemplet til at:

- Bladre gennem sider
- Zoome ind og ud
- Tilpasse til siden
- Vælg tekst

    Du kan kopiere tekst fra en rapport og derefter indsætte den et andet sted, f.eks. som en side i [!INCLUDE[prod_short](includes/prod_short.md)] eller Microsoft Word.  Ved hjælp af musen f.eks., skal du trykke og holde nede på det sted, hvor du vil starte, og derefter bevæge musen for at markere et eller flere ord, sætninger eller afsnit. Tryk på højre museknap, og vælg **Kopiér**. Indsæt den markerede tekst, hvor du ønsker.
- Panorer over dokumentet

    Du kan flytte det synlige område af rapporten i en vilkårlig retning, så du kan se andre områder eller rapporten. Panorering er nyttigt, når du har zoomet ind for at få vist detaljer.  Ved hjælp af musen f.eks. skal du trykke på og holde museknappen nede et vilkårligt sted i rapporteksemplet og derefter bevæge musen.

- Hent til en PDF-fil på din computer eller netværket.
- Udskriv

## <a name="saving-a-report"></a>Gemme en rapport

Du kan gemme en rapport som et PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument ved at vælge knappen **Send til**, og derefter vælge den ønskede indstilling.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Planlægge kørsel af en rapport

Du kan planlægge kørsel af en rapport på en bestemt dato og et bestemt klokkeslæt. Planlagte rapporter og kørsler indsættes i jobkøen og behandles på det planlagte tidspunkt, ligesom andre job. Du vælger indstillingen **Skema**, når du har valgt knappen **Send til**, og derefter angiver du oplysninger som f.eks. printer og klokkeslæt og dato. Rapporten føjes derefter til opgavekøen og køres på det angivne tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobkøen. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).  

Når du planlægger en rapport til kørsel, kan du angive, at den skal køre hver torsdag, ved at angive feltet **Datoformel for næste kørsel** til f.eks. *D4*. Du kan finde flere oplysninger i [Bruge datoformler](ui-enter-date-ranges.md#using-date-formulas).  

Du kan vælge at gemme den behandlede rapport i en fil, f.eks. Excel, Word eller PDF, udskrive den til den ønskede printer eller kun generere rapporten. Hvis du vælger at gemme rapporten i en fil, bliver den behandlede rapport sendt til området **Rapportindbakke** i dit rollecenter, hvor du kan se den.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Udskrive en rapport

Du kan udskrive en rapport ved at vælge knappen **Udskriv** på rapportanmodningssiden eller på menulinjen på siden **Eksempel**.

<!--
### Printer selection

The report prints to the printer shown in the **Selected printer** field on the report request page. You can't change the printer from this page.

The selected printer is either set on the **Printer Selections** page or it's the default printer set up on the **Printer Management** page. If you want to use another printer, see  [Set Up Printers](ui-specify-printer-selection-reports.md).

If no printer is specified on the **Printer Selections** page or set as default on the **Printer Management** page, the browser printing feature is used. In this case, **Browser** appears in the **Selected printer** field on the report request page.
-->
### <a name="printer"></a><a name="Printer"></a>Printer

Feltet **Printer** på rapportanmodningssiden viser navnet på den printer, rapporten sendes til. **(Håndteres af browseren)** angiver, at der ikke er en udvalgt printer til rapporten. I dette tilfælde vil browseren håndtere udskriften og vise en standard oplevelse, hvor du kan vælge en lokal printer, der er tilsluttet enheden.

Du kan ikke ændre printeren ved hjælp feltet **Printer**. Hvis du vil skifte printer, skal du gå til **Printervalg** eller siderne **Printeradministration**. Indstilling af printeren er som regel en administratoropgave. Hvis du ønsker flere oplysninger, skal du se [Installation af printere](ui-specify-printer-selection-reports.md).

<!--
### Browser printing

Because [!INCLUDE[prod_short](includes/prod_short.md)] is a cloud service, it can't reach local printers connected to your computer. However, it can connect to cloud-enabled printers. In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a cloud printer named **Email Printer** is installed as an extension and is ready to use after initial setup.

If a cloud printer is not installed and set up, or if an installed printer fails, then printing will default to the printing options for the browser.

> [!NOTE]
> The browser printing options work independently of [!INCLUDE[prod_short](includes/prod_short.md)]. So any printer settings that might have been set up from printers in [!INCLUDE[prod_short](includes/prod_short.md)] aren't carried over to the browser print options.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Udskrive rapporter på thailandsk

Knappen **Udskriv** er specifik for Thai-versionen af [!INCLUDE[prod_short](includes/prod_short.md)], men kan ikke udskrive rapporter korrekt pga. begrænsninger i den tjeneste, der genererer PDF-filen, som kan udskrives. Du kan i stedet åbne rapporten i Word og derefter gemme rapporten som en PDF-fil, der kan udskrives.  

Du kan også bede administratoren om at oprette et Word-rapportlayout til de mest anvendte rapporter. Du kan finde flere oplysninger under [Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Ændre rapportlayout

Et rapportlayout bestemmer, hvad der skal vises i en rapport, hvor den arrangeres, og hvilken typografi der anvendes. Hvis du vil skifte til et andet layout, kan du se [Ændre det aktuelle rapportlayout](ui-how-change-layout-currently-used-report.md). Eller du kan tilpasse din egen rapportlayout, skal du se [Oprette et brugerdefineret rapportlayout](ui-how-create-custom-report-layout.md).

## <a name="advanced-options"></a>Avancerede indstillinger

Felterne under **Avanceret** angiver begrænsninger for den genererede rapport til styring af printerressourcer. Du behøver normalt ikke at ændre disse indstillinger, medmindre du har en stor rapport. Hvis en rapport overskrider disse begrænsninger, når du prøver at få vist eller udskrive, vises der en meddelelse om, hvilken begrænsning der er overskredet. Du kan derefter ændre indstillingerne, så de passer til din rapport. Hvert felt har imidlertid en maksimumværdi, som du skal være opmærksom på:

|Felt|Maksimumværdi|
|-----|-------------|
|Maksimal gengivelsestid:|12:00:00|
|Maks. antal rækker|1000000|
|Maksimalt antal dokumenter|500|

> [!NOTE]
> De maksimale værdier kan være forskellige for [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, og en administrator kan ændre dem. Du kan finde flere oplysninger under [Konfiguration af Business Central Server - Rapporter](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Du kan få vist en oversigt over rapporters begrænsninger [!INCLUDE[prod_short](includes/prod_short.md)] online i [Driftsgrænser](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Se også

[Installation af printere](ui-specify-printer-selection-reports.md)  
[Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md)  
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]