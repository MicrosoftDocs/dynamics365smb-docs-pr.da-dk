---
title: Administrere rapport- og dokumentlayout
description: Du kan bruge rapportlayout til at tilpasse dokumenter, f.eks. for at tilpasse skrifttype, logo eller sideindstillinger for PDF-filer, som du sender til kunderne.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9652, 9650
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 5fed722bb5929da100c1c92e63aebb1f10cf53d0
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520678"
---
# <a name="report-and-document-layouts-overview"></a>Oversigt over rapport- og dokumentlayout

Et rapportlayout styrer indholdet og formatet af rapporten, herunder hvilke datafelter i et datasæt der vises i rapporten, og hvordan de er organiseret, teksttypografi, billeder og meget mere. Fra [!INCLUDE[prod_short](includes/prod_short.md)]-klienter kan du ændre, hvilket layout der skal bruges i en rapport, oprette et nyt layout eller ændre det aktuelle layout.

> [!NOTE]  
> I [!INCLUDE[prod_short](includes/prod_short.md)] omfatter "rapporter" også eksternt orienterede dokumenter, f.eks. salgsfakturaer og ordrebekræftelser, som du sender til kunder som PDF-filer.

## <a name="introduction"></a>Introduktion

Et rapportlayout indstiller navnlig følgende:

* Navne- og datafelterne, der skal medtages fra datasættet for [!INCLUDE[prod_short](includes/prod_short.md)]-rapporten.
* Tekstformatet såsom skrifttype, størrelse og farve.
* Firmaets logo og dets placering.
* Generelle sideindstillinger såsom margener og baggrundsbilleder.

En rapport kan konfigureres med flere rapportlayout, som du kan skifte mellem efter behov. 

<!--You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed. For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).-->

Der er to vigtige layout aspekter af rapportlayout, som vil påvirke den måde, du arbejder med dem på: *layouttypen* og *layoutkilden*. Layouttypen angiver den filtype, som layoutet er baseret på. Layout-kildet angiver layoutets oprindelse.

## <a name="layout-types"></a>Layouttyper

Der findes fire typer rapportlayout, der kan bruges i rapporter: Word, RDLC, Excel og ekstern.

### <a name="word"></a>Word

Et rapportlayout til Word er baseret på Word-dokumenter (.docx-filtype). Med Word-rapportlayout kan du udforme rapportlayout ved hjælp af Microsoft Word. Et Word-rapportlayout bestemmer rapportens indhold og styrer, hvordan indholdselementerne skal placeres, og hvordan de ser ud. Et Word-dokument med rapportlayout vil normalt bruge tabeller til at arrangere indhold, hvor cellerne kan indeholde datafelter, tekst eller billeder.

[![Eksempel på et dokument med Word-rapportlayout til Business Central.](media/word-layout-overview.png)](media/word-layout-overview.png#lightbox) 

<!--![Example of a word report layout document for Business Central.](media/nav_wordreportlayout_edit_in_word_example.png) -->

Du kan finde flere oplysninger i [Arbejde med Word-layout](ui-how-add-fields-word-report-layout.md).

### <a name="excel"></a>Excel

Excel-rapportlayout er baseret på Microsoft Excel-projektmapper (.xlsx-filtype). De giver dig mulighed for at oprette rapporter ved hjælp af velkendte Excel-funktioner til sammenfatning, analyse og præsentation af data, f. eks. formler, pivottabeller og pivotdiagrammer.

[![Viser et eksempel på et Excel-layout.](media/excel-layout-2.png)](media/excel-layout-2.png#lightbox)

Du kan finde flere oplysninger i [Arbejde med Excel-layout](ui-excel-report-layouts.md).

### <a name="rdlc"></a>RDLC

RDLC-layout er baseret på klientrapportens definitionslayoutfiler (.rdl- eller .rdlc-filtyper). Disse layout oprettes og ændres ved hjælp af SQL Server Report Builder eller Microsoft RDLC Report Designer. Design konceptet til RDLC layout svarer til Word-layout, hvor layoutet bestemmer, hvilke felter der skal vises, og hvordan de er arrangeret. Men RDLC-layoutdesign er mere avanceret end Word-layout.

[![Viser et eksempel på et RDLC-layout.](media/rdlc-layout-overview.png)](media/rdlc-layout-overview.png#lightbox)

Du kan finde flere oplysninger i [Arbejde med RDLC-layouts](ui-rdlc-report-layouts.md).

### <a name="external"></a>Ekstern

En ekstern layouttype henviser til en avanceret type, der specielt er beregnet til bestemte rapporter. Selve rapporterne og layouts leveres typisk af partnere, ikke Microsoft. Det faktiske filtypeformat varierer, afhængigt af udbyderen.

Du kan finde flere oplysninger i [Udvikle en brugerdefineret rapportgengivelse](/dynamics365/business-central/dev-itpro/developer/devenv-report-custom-render).

## <a name="layout-sources"></a>Layoutkilder

Ud over teksten inddeles layout yderligere i tre kategorier baseret på kilde eller oprindelse.

* Udvidelseslayout

   Udvidelseslayout er de layout, som er en del af et filtypenavn, der er installeret på miljøet. Disse layouts er typisk standardlayout, der leveres af Microsoft, f. eks. i basis programmet. Det kan også være layout, der er inkluderet i udvidelser fra andre softwareleverandører. Du kan genkende udvidelses layout på siden **Rapportlayout**, fordi udvidelses navnet og Publisher vises i kolonnen **Udvidelse**.

* Brugerdefineret layouts

   Den anden kilde til layouts er slutbrugeren. Inde fra Business Central kan en bruger med de rette tilladelser tilføje nye layout på forskellige måder. Du kan f. eks. starte med et eksisterende udvidelseslayout eller et andet brugerdefineret layout. I **Rapportlayoutet** har brugerdefinerede layout en tom kolonne **Udvidelse**.

   Du kan finde flere oplysninger i [Kom i gang med at oprette rapportlayout](ui-get-started-layouts.md).

* Brugerdefinerede layout

  Brugerdefinerede layouts er også layout, der oprettes af brugere. Forskellen er, at disse layouts er oprettet ud fra den ældre side **Tilpassede rapportlayout**, og de kan kun være Word-og RDLC. Du kan stadig oprette brugerdefinerede layout, men de er ved at blive udfaset til fordel for brugerdefinerede layout.

  Du kan finde flere oplysninger i [(Ældre) Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md).

Du kan finde flere oplysninger om, hvordan du kan bestemme, hvilken type der passer dig bedst, i afsnittet [bestemme, hvilken type layout du vil bruge ](ui-get-started-layouts.md#decide).

> [!IMPORTANT]
> Det er vigtigt at huske på, at du ikke kan ændre udvidelses layout fra Business Central-klienten. Du kan f. eks. ikke ændre layout navnet eller-typen eller overføre og erstatte det med en anden version. Hvis du prøver, vises der en fejlmeddelelse. Du skal i stedet oprette et brugerdefineret eller brugerdefineret layout, der er baseret på udvidelses layoutet.

<!--
### Built-in and custom report layouts



[!INCLUDE[prod_short](includes/prod_short.md)] includes several built-in layouts. Built-in layouts are predefined layouts that are designed for specific reports. [!INCLUDE[prod_short](includes/prod_short.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both. You can’t modify a built-in report layout from [!INCLUDE[prod_short](includes/prod_short.md)] but you use them as a starting point for building your own custom report layouts.

Custom layouts are report layouts that you design to change the appearance of a report. You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout. Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed. For example, you can have different layouts for each [!INCLUDE[prod_short](includes/prod_short.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.


Deciding on whether to use a Word, Excel, or RDLC layout type will depend on how you want the generated report to look and your knowledge of tools for creating the layouts, like Word, Excel, and SQL Server Report Builder.

* The general design concepts for Word and RDLC layouts are similar. However each type has certain design features that affect how the generated report appears in [!INCLUDE[prod_short](includes/prod_short.md)]. This means that the same report might look different when using the Word report layout compared to the RDLC report layout.

* The process for setting up Word, Excel, and RDLC report layouts on reports is the same. The main difference is in the way you modify the layouts. Word and especially Excel layouts are typically easier to create and modify than RDLC report layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.

* Not all reports and document have a dataset that is optimized for use with an Excel layout. For example, aggregations and complex calculations work best with RDLC or Word layouts. The same is true for documents.

For information about how to switch the layout currently used on a report, see [Set the Layout Used by a Report](ui-set-report-layout.md).

-->



## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Opdater brugerdefinerede rapportlayouts](ui-update-report-layouts.md)  
[Sådan opretter og ændrer du Brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md)  
[Importere og eksportere et brugerdefineret rapport- eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Angiv specielle dokumentlayout for debitorer og leverandører](ui-define-customer-vendor-document-layouts.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]