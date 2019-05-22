---
title: Planlægge en rapport til kørsel på en bestemt dato og et bestemt klokkeslæt | Microsoft Docs
description: Få mere at vide om, hvordan du angiver en rapport i en opgavekø og planlægger, at den skal afvikles på en bestemt dato og tidspunkt.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 65fcba3f0222b324f132115ea7f1ec53b75d983f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250683"
---
# <a name="working-with-reports-and-batch-jobs"></a>Arbejde med rapporter og kørsler
En rapport indsamler oplysninger, der er baseret på et bestemt sæt kriterier, og organiserer og præsenterer oplysningerne i et format, der er let at læse og kan udskrives. Der er mange rapporter, du kan få adgang til, i hele programmet. Rapporterne indeholder typisk oplysninger i forhold til konteksten for den viste side. For eksempel indeholder siden **Debitor** rapporter om de 10 bedste kunder, salgsstatistik og mere.

Kørsler udfører mere eller mindre det samme som rapporter, men med henblik på at udføre en proces. F.eks. opretter kørslen **Opret rykkere** rykkerdokumenter til debitorer med forfaldne betalinger.  

> [!NOTE]
> I dette emne omtales hovedsageligt "rapport", men lignende oplysninger gælder for kørsler.

Du kan finde rapporter under fanen **Rapporter** på markerede sider, eller du kan bruge søgefunktionen ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") til at finde rapporter efter navn.


## <a name="specifying-the-data-to-include-in-the-report"></a>Angive dataene, der skal medtages i rapporten
Når du åbner en rapport, får du typisk vist en side, hvor du kan angive forskellige indstillinger og filtre, som bestemmer, hvad der skal med i rapporten. Denne side kaldes rapportanmodningssiden. For eksempel gør rapportanmodningssiden det muligt at oprette en rapport for en bestemt debitor, et bestemt datointerval eller sorteringsrækkefølge for oplysninger i rapporten. Her er et eksempel på en rapportanmodningsside:

![Rapportindstillinger](media/report_options.png "Rapportindstillinger")

> [!Caution]
> Sektionen **Vis resultater** på en anmodningsside indeholder en generel filtreringsfunktion for rapporter. Disse filtre er valgfrie.<br /><br /> Nogle rapporter ignorerer disse filtre, hvilket vil sige, at uanset hvilket filter der er angivet i sektionen **Vis resultater**, er resultatet af rapporten det samme. Det er ikke muligt at vise en oversigt over, hvilke felter ignoreres i rapporterne, så du må prøve dig frem med filtrene, når du bruger dem.<br /><br />
**Eksempel**: Når du bruger kørslen **Opret rykkere**, bliver et filter for feltet **Debitorposter** i **Niv. for sidst udstedte rykker** ignoreret, fordi filtrene er fastsat for kørslen.

### <a name="SavedSettings"></a>Bruge gemte indstillinger
I nogle rapporter, afhængigt af hvordan de er designet, kan rapportsiden indeholde sektionen **Gemte indstillinger**, der indeholder en eller flere poster i feltet **Brug standardværdier fra**. Posterne i feltet kaldes *gemte indstillinger*. En gemt indstilling er grundlæggende en foruddefineret gruppe af indstillinger og filtre, som du kan anvende i rapporten, før du ser et rapporteksempel eller sender rapporten til en fil. Posten for gemte indstillinger, som kaldes **Sidst anvendte indstillinger og filtre**, er altid tilgængelig. Denne post konfigurerer rapporten til at bruge indstillinger og filtre, der blev brugt sidste gang, du så på rapporten.

Med gemte indstillinger kan du hurtigt og pålideligt generere ensartede rapporter, der indeholder de korrekte data. Når du har indstillet feltet **Brug standardværdier fra** til en post med gemte indstillinger, kan du ændre indstillingerne og filtrene, før du ser rapporten eksemplificeret eller gemmer den. De ændringer, du udfører, bliver ikke gemt i den post med gemte indstillinger, du har valgt, men de gemmes i **Seneste anvendte indstillinger og filtre**.

>[!NOTE]
>Hvis du er administrator, kan du oprette og administrere de gemte indstillinger for rapporter for alle brugere. Du kan finde flere oplysninger i [Administrere gemte indstillinger i rapporter](reports-saving-reusing-settings.md).

### <a name="setting-options-and-filters"></a>Valg af indstillinger og filtre
Hvis du vil begrænse eller præcisere de data, der indgår i en rapport, yderligere, kan du angive flere indstillinger og filtre.

Med filtre kan du få vist data, der er baseret på bestemte kriterier. Filtre er grupperet efter den enhed, de tilhører, f.eks. **Debitor** i ovenstående illustration. Du definerer et filter ved at indstille feltet **Hvor** til det felt, du vil filtrere på, og derefter tilføje kriterierne i feltet **er:**.

Du kan tilføje flere filtre ved at klikke på felterne **Og** og **er**. Når du har mere end ét filter, er det kun de resultater, der opfylder kriterierne for alle filtre, der medtages i rapporten.

Afhængigt af hvilken type felt, du filtrerer, kan du angive filterkriterier for at søge efter et nøjagtigt match, delvist match, værdiintervaller og meget mere. Du kan få hjælp til at indstille filtre her:
-   [Filtrering](ui-enter-criteria-filters.md#FilterCriteria)
-   [Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md)

## <a name="previewing-a-report"></a>Visning af en rapport
Vælg **Vis udskrift** for at se rapporten i internetbrowseren. Peg på et område i rapporten for at få vist menulinjen.  

![Værktøjslinje til visning af rapporteksempel](media/report_viewer.png "Værktøjslinje til visning af rapporteksempel")

Brug menulinjen til at:

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
Du kan gemme en rapport som et PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument ved at vælge **Send til**, og derefter vælge den ønskede indstilling.

## <a name="ScheduleReport"></a> Planlægge kørsel af en rapport
Du kan planlægge en rapport til at køre på en bestemt dato og et bestemt klokkeslæt. Planlagte rapporter indsættes i jobkøen og behandles på det planlagte tidspunkt, ligesom andre job. Du kan vælge at gemme den behandlede rapport i en fil, f.eks. Excel, Word eller PDF, udskrive den til den ønskede printer eller kun behandle rapporten. Hvis du vælger at gemme rapporten i en fil, bliver den behandlede rapport sendt til området **Rapportindbakke** i dit rollecenter, hvor du kan se den.

Du kan planlægge en rapport, når du åbner en rapport. Du vælger handlingen **Skema**, og derefter angiver du oplysninger som printer og dato og klokkeslæt. Rapporten føjes derefter til opgavekøen og køres på det angivne tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobkøen. Hvis du har gemt den behandlede rapport til en fil, er den tilgængelig i området **Rapportindbakke**.

## <a name="PrintReport"></a>Udskrive en rapport
Du kan udskrive en rapport fra knappen **Udskriv** på siden Indstillinger, der vises, når du åbner rapporten eller på menulinjen i Vis udskrift.

## <a name="changing-the-layout-and-look-of-a-report"></a>Ændre layoutet og udseendet af en rapport
Et rapportlayout bestemmer, hvad der skal vises i en rapport, hvor den arrangeres, og hvilken typografi der anvendes. Hvis du vil skifte til et andet layout, kan du se [Ændre, hvilket layout der aktuelt bruges i en rapport](ui-how-change-layout-currently-used-report.md). Eller du kan tilpasse din egen rapportlayout, skal du se [Oprette et brugerdefineret rapportlayout](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se også
[Angive printervalg for rapporter](ui-specify-printer-selection-reports.md)  
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
