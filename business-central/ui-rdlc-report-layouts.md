---
title: Arbejde med RDLC-layouts
description: Få en introduktion til RDLC-rapportlayout.
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 12/04/2023
ms.author: jswymer
ms.reviewer: jswymer
---
# Arbejde med RDLC-layouts

RDLC-layout er baseret på rapportens definitionslayoutfiler (.rdl- eller .rdlc-filtyper). Design begreberne for RDLC-layout ligner de andre layouttyper. Layoutet bestemmer, hvilke felter der skal vises, og hvordan de er arrangeret. Men RDLC-layoutdesign er mere avanceret end Word- og Excel-layout.

[![Viser forskellige elementer i et RDLC-layout.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## Krævede værktøjer

Hvis du vil ændre RDL-layout, kan du bruge enten Microsoft SQL Server Report Builder eller Microsoft Visual Studio med RDLC Report Designer-udvidelsen.

- Report Builder er en fritstående app, som er installeret på computeren af dig eller en administrator. Hvis du har lokal Business Central, installeres Report Builder automatisk med installationen af Business Central Server. Yderligere oplysninger om installation af Report Builder finder du i [Installere Report Builder ](/sql/reporting-services/install-windows/install-report-builder) i dokumentationen til SQL Server.

- RDLC Report Designer er et filtypenavn for Visual Studio 2019 og nyere. Du kan hente og installere RDLC Report Designer fra [Visual Studio-markedspladsen](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## Oprette og tilpasse RDLC-layouts

Oprettelse og ændring af RDLC-layout er en avanceret opgave, som typisk gøres af superbrugere eller udviklere. Grundlæggende begreber er ikke specifikke for Business Central-rapportlayout. Vi henviser derfor til følgende dokumentation:

- [Oprette rapporten RDL-layout](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

   I denne artikel forklares det, hvordan du opretter et RDLC-rapportlayout af AL kode.

- [Rapporter, Rapportdele og Rapportdefinitioner ](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

   Linkene til SQL Server Reporting Services-dokumentationen til RDL/RDLC. Denne artikel forklarer koncepterne bag RDL/RDLC, og hvordan du bruger Report Builder.

> [!NOTE]
> Report Builder kan kun genkende .rdl-filtypen, dvs. ikke .rdlc. Layoutfiler, der er eksporteret fra Business central, er .rdlc-filtyper. Hvis du vil ændre layoutet i Report Builder, skal du omdøbe filtypen til .rdl.

## Se også

[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Angive det layout, der bruges af en rapport](ui-set-report-layout.md)  
[Introduktion til oprettelse af rapportlayout](ui-get-started-layouts.md)  
[Arbejde med rapporter, kørsler og XML-porte](ui-work-report.md)  
[Business Intelligence](bi.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analyse af rapportdata med Excel](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
