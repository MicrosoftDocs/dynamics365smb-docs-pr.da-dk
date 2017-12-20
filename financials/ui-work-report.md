---
title: "Planlægge en rapport til kørsel på en bestemt dato og et bestemt klokkeslæt | Microsoft Docs"
description: "Få mere at vide om, hvordan du angiver en rapport i en opgavekø og planlægger, at den skal afvikles på en bestemt dato og tidspunkt."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 07/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: de6cbcdc8e7ca4aff06461192e2038831ba6b5b3
ms.openlocfilehash: 16c9c8c896e3517f08a7326eef88ebc646834b1a
ms.contentlocale: da-dk
ms.lasthandoff: 12/20/2017

---
# <a name="working-with-reports"></a>Arbejde med rapporter
En rapport indsamler oplysninger, der er baseret på et bestemt sæt kriterier, og organiserer og præsenterer oplysningerne i et format, der er let at læse og kan udskrives. Der er mange rapporter, du kan få adgang til, i hele programmet. Rapporterne indeholder typisk oplysninger i forhold til konteksten for den viste side. For eksempel indeholder siden **Debitor** rapporter om de 10 bedste kunder, salgsstatistik og mere.

Du kan finde rapporter under fanen **Rapporter** på valgte sider, eller du kan bruge søgefunktionen til at finde rapporter efter navn. Når du åbner en rapport, får du vist en side, hvor du kan angive oplysninger (indstillinger og filtre), som bestemmer, hvad der skal med i rapporten. For eksempel, afhængigt af rapporten, kan du angive et datointerval, en bestemt post, f.eks. en kunde, eller sorteringsrækkefølge. Her er et eksempel:

![Rapportindstillinger](media/report_options.png "Rapportindstillinger")

## <a name="previewing-a-report"></a>Visning af et rapporteksempel
Vælg **Vis udskrift** for at se rapporten i internetbrowseren. Peg på et område i rapporten for at få vist menulinjen.  

![Værktøjslinje til visning af rapporteksempel](media/report_viewer.png "Værktøjslinje til visning af rapporteksempel")

Brug menulinjen til at:

-   Bladre gennem sider
-   Zoome ind og ud
-   Tilpasse til vinduet
-   Vælg tekst

    Du kan kopiere tekst fra en rapport og derefter indsætte den et andet sted, f.eks. som en side i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller Microsoft Word.  Ved hjælp af musen f.eks., skal du trykke og holde nede på det sted, hvor du vil starte, og derefter bevæge musen for at markere et eller flere ord, sætninger eller afsnit. Du kan derefter trykke på højre museknap og vælge **Kopier**. Du kan indsætte den markerede tekst, hvor du ønsker.
-   Panorer over dokumentet

    Du kan flytte det synlige område af rapporten i en vilkårlig retning, så du kan se andre områder eller rapporten. Dette er nyttigt, når du har zoomet ind for at få vist detaljer.  Ved hjælp af musen f.eks. skal du trykke på og holde museknappen nede et vilkårligt sted i rapporteksemplet og derefter bevæge musen.

-   Hent til en PDF-fil på din computer eller netværket.
-   Udskriv


## <a name="saving-a-report"></a>Gemme en rapport
Du kan gemme en rapport som et PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument ved at vælge **Send til**, og derefter vælge den ønskede indstilling.

## <a name="ScheduleReport"></a> Planlægge kørsel af en rapport
Du kan planlægge en rapport til at køre på en bestemt dato og et bestemt klokkeslæt. Planlagte rapporter indsættes i jobkøen og behandles på det planlagte tidspunkt, ligesom andre job. Du kan vælge at gemme den behandlede rapport i en fil, f.eks. Excel, Word eller PDF, udskrive den til den ønskede printer eller kun behandle rapporten. Hvis du vælger at gemme rapporten i en fil, bliver den behandlede rapport sendt til området **Rapportindbakke** på din startside, hvor du kan se den.

Du kan planlægge en rapport, når du åbner en rapport. Du vælger handlingen **Skema**, og derefter angiver du oplysninger som printer og dato og klokkeslæt. Rapporten føjes derefter til opgavekøen og køres på det angivne tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobkøen. Hvis du har gemt den behandlede rapport til en fil, er den tilgængelig i området **Rapportindbakke**.

## <a name="PrintReport"></a>Udskrive en rapport
Du kan udskrive en rapport fra knappen **Udskriv** på siden Indstillinger, der vises, når du åbner rapporten eller på menulinjen i Vis udskrift.

## <a name="using-saved-settings"></a>Bruge gemte indstillinger
En rapport kan omfatte en eller flere poster i feltet **Gemte indstillinger**. *Gemte indstillinger* er grundlæggende en foruddefineret gruppe af indstillinger og filtre, som du kan anvende i rapporten, før du ser et rapporteksempel eller sender rapporten til en fil. Med gemte indstillinger kan du hurtigt og pålideligt generere ensartede rapporter, der indeholder de korrekte data.

Posten for gemte indstillinger, som kaldes **Sidst anvendte indstillinger og filtre**, er altid tilgængelig. Denne post konfigurerer rapporten til at bruge indstillinger og filtre, der blev brugt sidste gang, du så på rapporten.

>[!NOTE]
>Som administrator kan du oprette og administrere de gemte indstillinger for rapporter for alle brugere. Du kan finde flere oplysninger i [Administrere gemte indstillinger i rapporter](reports-saving-reusing-settings.md).

## <a name="changing-the-layout-and-look-of-a-report"></a>Ændre layoutet og udseendet af en rapport
Et rapportlayout bestemmer, hvad der skal vises i en rapport, hvor den arrangeres, og hvilken typografi der anvendes. Hvis du vil skifte til et andet layout, kan du se [Fremgangsmåde: Ændre, hvilket layout der aktuelt bruges i en rapport](ui-how-change-layout-currently-used-report.md). Eller du kan tilpasse din egen rapportlayout, skal du se [Fremgangsmåde: Oprette et brugerdefineret rapportlayout](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se også
[Angive printervalg for rapporter](ui-specify-printer-selection-reports.md)  
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Arbejde med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

