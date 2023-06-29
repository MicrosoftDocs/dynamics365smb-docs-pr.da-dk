---
title: Arbejde med RDLC-layouts
description: Få en introduktion til RDLC-rapportlayout.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/14/2022
ms.author: jswymer
---
# <a name="working-with-rdlc-layouts"></a><a name="working-with-rdlc-layouts"></a>Arbejde med RDLC-layouts

RDLC-layout er baseret på klientrapportens definitionslayoutfiler (.rdl- eller .rdlc-filtyper). Design begreberne for RDLC-layout ligner de andre layouttyper. Layoutet bestemmer, hvilke felter der skal vises, og hvordan de er arrangeret. Men RDLC-layoutdesign er mere avanceret end Word- og Excel-layout.

[![Viser forskellige elementer i et RDLC-layout.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## <a name="required-tools"></a><a name="required-tools"></a>Krævede værktøjer

Hvis du vil ændre RDL-layout, kan du bruge enten Microsoft SQL Server Report Builder eller Microsoft RDLC Report Designer.

- Report Builder er en fritstående app, som er installeret på computeren af dig eller en administrator. Hvis du har lokal Business Central, installeres Report Builder automatisk med installationen af Business Central Server. Yderligere oplysninger om installation af Report Builder finder du i [Installere Report Builder ](/sql/reporting-services/install-windows/install-report-builder) i dokumentationen til SQL Server.

- RDLC Report Designer er et filtypenavn for Visual Studio 2017 og nyere. Du kan hente og installere RDLC Report Designer fra [Visual Studio-markedspladsen](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## <a name="create-and-modify-rdlc-layouts"></a><a name="create-and-modify-rdlc-layouts"></a>Oprette og tilpasse RDLC-layouts

Oprettelse og ændring af RDLC-layout er en avanceret opgave, som typisk gøres af superbrugere eller udviklere. Grundlæggende begreber er ikke specifikke for Business Central-rapportlayout. Vi henviser derfor til følgende dokumentation:

- [Oprette rapporten RDL-layout](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

    I denne artikel forklares det, hvordan du opretter et RDLC-rapportlayout af AL kode.

- [Rapporter, Rapportdele og Rapportdefinitioner ](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

 Hyperlinkene til SQL Server Reporting Services-dokumentationen til RDL/RDLC. Denne dokumentation forklarer begreberne  
Bag RDL/RDLC, og hvordan Report Builder bruges.

> [!NOTE]
> Report Builder kan kun genkende .rdl-filtypen, dvs. ikke .rdlc. Layoutfiler, der er eksporteret fra Business central, er .rdlc-filtyper. Hvis du vil ændre layoutet i Report Builder, skal du omdøbe filtypen til .rdl.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Angive det layout, der bruges af en rapport](ui-set-report-layout.md)  
[Introduktion til oprettelse af rapportlayout](ui-get-started-layouts.md)  
[Arbejde med rapporter, kørsler og XML-porte](ui-work-report.md)  
[Business Intelligence](bi.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analyse af rapportdata med Excel](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
