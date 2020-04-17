---
title: Planlægge en rapport til kørsel på en bestemt dato og et bestemt klokkeslæt | Microsoft Docs
description: Få mere at vide om, hvordan du angiver en rapport i en opgavekø og planlægger, at den skal afvikles på en bestemt dato og tidspunkt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2bafaa9f4bda392309a76470df5290857327e59c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189287"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Arbejde med rapporter, kørsler og XMLporte
En rapport indsamler oplysninger, der er baseret på et bestemt sæt kriterier, og organiserer og præsenterer oplysningerne i et format, der er let at læse, og som du kan udskrive eller gemme som en fil. Der er mange rapporter, du kan få adgang til, i hele programmet. Rapporterne indeholder typisk oplysninger i forhold til konteksten for den viste side. For eksempel indeholder siden **Debitor** rapporter om de 10 bedste kunder, salgsstatistik og mere.

Kørsler og XMLporte udfører mere eller mindre det samme som rapporter, men med henblik på at udføre en proces eller eksportere data. F.eks. opretter kørslen **Opret rykkere** rykkerdokumenter til debitorer med forfaldne betalinger.  

> [!NOTE]
> I dette emne omtales hovedsageligt "rapport", men lignende oplysninger gælder for kørsler og XMLporte.

Du kan finde rapporter under fanen **Rapporter** på markerede sider, eller du kan bruge søgefunktionen ![ Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") til at finde rapporter efter navn.

## <a name="specifying-the-data-to-include-in-reports"></a>Angive dataene, der skal medtages i rapporter
Når du åbner en rapport, en kørsel eller XMLport, får du typisk vist en anmodningsside, hvor du kan angive forskellige indstillinger og filtre, som bestemmer, hvad der skal med i rapporten.

Du kan angive filtre i en rapport mere eller mindre på samme måde, som du angiver filtre på lister. Du kan finde flere oplysninger i [Filtrering](ui-enter-criteria-filters.md#filtering).

> [!Caution]
> Sektionen **Filtrer listen efter** på en anmodningsside indeholder en generel filtreringsfunktion for rapporter. Disse filtre er valgfrie.<br /><br /> Nogle rapporter ignorerer disse filtre, hvilket vil sige, at uanset hvilket filter der er angivet i sektionen **Filtrer listen efter**, er resultatet af rapporten det samme. Det er ikke muligt at vise en oversigt over, hvilke felter ignoreres i rapporterne, så du må prøve dig frem med filtrene, når du bruger dem.<br /><br />
**Eksempel**: Når du bruger kørslen **Opret rykkere**, bliver et filter for feltet **Debitorposter** i **Niv. for sidst udstedte rykker** ignoreret, fordi filtrene er fastsat for kørslen.

## <a name="using-saved-settings"></a><a name="SavedSettings"></a>Bruge gemte indstillinger
Anmodningssiden kan indeholde sektionen **Gemte indstillinger**, der indeholder en eller flere poster i feltet **Brug standardværdi fra**. En gemt indstilling er grundlæggende en foruddefineret gruppe af indstillinger og filtre, som du kan anvende i rapporten, før du ser et rapporteksempel eller sender rapporten til en fil. Posten for gemte indstillinger, som kaldes **Sidst anvendte indstillinger og filtre**, er altid tilgængelig. Denne post konfigurerer rapporten til at bruge indstillinger og filtre, der blev brugt sidste gang, du brugte rapporten.

Med gemte indstillinger kan du hurtigt og pålideligt generere ensartede rapporter, der indeholder de korrekte data. Når du har indstillet feltet **Brug standardværdier fra** til en post med gemte indstillinger, kan du ændre indstillingerne og filtrene, før du ser rapporten eksemplificeret eller gemmer den. De ændringer, du udfører, bliver ikke gemt i den post med gemte indstillinger, du har valgt, men de gemmes i posten **Seneste anvendte indstillinger og filtre**.

>[!NOTE]
>Hvis du er administrator, kan du oprette og administrere de gemte indstillinger for rapporter for alle brugere. Du kan finde flere oplysninger i [Administrere gemte indstillinger for rapporter og kørsler](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Visning af en rapport
Vælg knappen **Eksempel** for at få vist rapporten i. Brug menulinjen i rapporteksemplet til at:

-   Bladre gennem sider
-   Zoome ind og ud
-   Tilpasse til siden
-   Vælg tekst

    Du kan kopiere tekst fra en rapport og derefter indsætte den et andet sted, f.eks. som en side i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller Microsoft Word.  Ved hjælp af musen f.eks., skal du trykke og holde nede på det sted, hvor du vil starte, og derefter bevæge musen for at markere et eller flere ord, sætninger eller afsnit. Du kan derefter trykke på højre museknap og vælge **Kopiér**. Du kan derefter indsætte den markerede tekst, hvor du ønsker.
-   Panorer over dokumentet

    Du kan flytte det synlige område af rapporten i en vilkårlig retning, så du kan se andre områder eller rapporten. Dette er nyttigt, når du har zoomet ind for at få vist detaljer.  Ved hjælp af musen f.eks. skal du trykke på og holde museknappen nede et vilkårligt sted i rapporteksemplet og derefter bevæge musen.

-   Hent til en PDF-fil på din computer eller netværket.
-   Udskriv

## <a name="saving-a-report"></a>Gemme en rapport
Du kan gemme en rapport som et PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument ved at vælge knappen **Send til**, og derefter vælge den ønskede indstilling.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Planlægge kørsel af en rapport
Du kan planlægge kørsel af en rapport på en bestemt dato og et bestemt klokkeslæt. Planlagte rapporter og kørsler indsættes i jobkøen og behandles på det planlagte tidspunkt, ligesom andre job. Du vælger indstillingen **Skema**, når du har valgt knappen **Send til**, og derefter angiver du oplysninger som f.eks. printer og klokkeslæt og dato. Rapporten føjes derefter til opgavekøen og køres på det angivne tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobkøen. Du kan finde flere oplysninger i [Brug af opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

Du kan vælge at gemme den behandlede rapport i en fil, f.eks. Excel, Word eller PDF, udskrive den til den ønskede printer eller kun behandle rapporten. Hvis du vælger at gemme rapporten i en fil, bliver den behandlede rapport sendt til området **Rapportindbakke** i dit rollecenter, hvor du kan se den.

## <a name="printing-a-report"></a><a name="PrintReport"></a>Udskrive en rapport
Du kan udskrive en rapport ved at vælge knappen **Udskriv** på rapportanmodningssiden eller på menulinjen på siden **Eksempel**.

Da [!INCLUDE[prodshort](includes/prodshort.md)] er en cloud-tjeneste, kan den ikke nå lokale printere med forbindelse til brugernes maskiner. Men den kan oprette forbindelse til cloud-kompatible printere. I den generelle version af [!INCLUDE[prodshort](includes/prodshort.md)] er der installeret en cloud-printer med navnet **Mailprinter** som en udvidelse, og den er klar til brug efter den første installation.

Hvis der ikke er installeret og konfigureret en cloud-printer, eller hvis der opstår fejl på en installeret printer, vil udskrivningen som standard benytte browserens udskriftsindstillinger. Dette angives med denne værdi i feltet **Printer** på rapportanmodningssiden: *(ingen, håndteres af browseren)*.

På siden **Printerstyring** kan du se de printere, der er konfigurerede. Du kan finde flere oplysninger i [Oprette printere](ui-specify-printer-selection-reports.md).

> [!NOTE]
> Du kan ikke ændre feltet **Printer** på rapportanmodningssiden. Hvis du vil bruge en anden printer, skal du vælge den på siden **Printerstyring**.

### <a name="printing-reports-in-thai"></a>Udskrive rapporter på thailandsk
Knappen **Udskriv** er specifik for Thai-versionen af [!INCLUDE[prodshort](includes/prodshort.md)], men kan ikke udskrive rapporter korrekt pga. begrænsninger i den tjeneste, der genererer PDF-filen, som kan udskrives. Du kan i stedet åbne rapporten i Word og derefter gemme rapporten som en PDF-fil, der kan udskrives.  

Du kan også bede administratoren om at oprette et Word-rapportlayout til de mest anvendte rapporter. Du kan finde flere oplysninger under [Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Ændre rapportlayout
Et rapportlayout bestemmer, hvad der skal vises i en rapport, hvor den arrangeres, og hvilken typografi der anvendes. Hvis du vil skifte til et andet layout, kan du se [Ændre det aktuelle rapportlayout](ui-how-change-layout-currently-used-report.md). Eller du kan tilpasse din egen rapportlayout, skal du se [Oprette et brugerdefineret rapportlayout](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se også
[Installation af printere](ui-specify-printer-selection-reports.md)  
[Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md)  
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
