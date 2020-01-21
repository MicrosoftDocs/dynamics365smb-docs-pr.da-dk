---
title: Brugerdefinerede og indbyggede layout til rapporter og bilag | Microsoft Docs
description: Du kan bruge rapportlayout til at tilpasse dokumenter, f.eks. for at tilpasse skrifttype, logo eller sideindstillinger for PDF-filer, som du sender til kunderne.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 79e3f15169f592c5e90aacfd3307794f226adeb2
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953199"
---
# <a name="managing-report-and-document-layouts"></a>Administrere rapport- og dokumentlayout
Et rapportlayout styrer indholdet og formatet af rapporten, herunder hvilke datafelter i et datasæt der vises i rapporten, og hvordan de er organiseret, teksttypografi, billeder og meget mere. Fra [!INCLUDE[d365fin](includes/d365fin_md.md)]-klienter kan du ændre, hvilket layout der skal bruges i en rapport, oprette et nyt layout eller ændre det aktuelle layout.

> [!NOTE]  
>   I [!INCLUDE[d365fin](includes/d365fin_md.md)] omfatter "rapporter" også eksternt orienterede dokumenter, f.eks. salgsfakturaer og ordrebekræftelser, som du sender til kunder som PDF-filer.

Et rapportlayout indstiller navnlig følgende:

* Navne- og datafelterne, der skal medtages fra datasættet for [!INCLUDE[d365fin](includes/d365fin_md.md)]-rapporten.
* Tekstformatet såsom skrifttype, størrelse og farve.
* Firmaets logo og dets placering.
* Generelle sideindstillinger såsom margener og baggrundsbilleder.

En rapport kan konfigureres med flere rapportlayout, som du kan skifte mellem efter behov. Du kan bruge et af de indbyggede rapportlayout, eller du kan oprette brugerdefinerede rapportlayout og tildele dem dine rapporter. Du kan finde flere oplysninger under [Oprette et brugerdefineret rapport- eller dokumentlayout](ui-how-create-custom-report-layout.md).

Der findes to typer rapportlayout, der kan bruges i rapporter: Word og RDLC.

## <a name="word-report-layout-overview"></a>Oversigt over Word-rapportlayout
Et rapportlayout til Word er baseret på Word-dokument (.docx-filtype). Med Word-rapportlayout kan du udforme rapportlayout ved hjælp af Microsoft Word 2013 eller senere. Et Word-rapportlayout bestemmer rapportens indhold og styrer, hvordan indholdselementerne skal placeres, og hvordan de ser ud. Et Word-dokument med rapportlayout vil normalt bruge tabeller til at arrangere indhold, hvor cellerne kan indeholde datafelter, tekst eller billeder.

 ![Eksempel på et dokument med Word-rapportlayout til NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")  

## <a name="rdlc-layout-overview"></a>Oversigt over RDLC-layout
RDLC-layout er baseret på klientrapportens definitionslayout (.rdlc- eller .rdl-filtyper). Disse layout oprettes og ændres ved hjælp af SQL Server Report Builder. Konceptet for RDLC-layoutdesign ligner Word-layout, hvor layoutet definerer det generelle format af rapporten og bestemmer, hvilke felter fra datasættet der skal medtages. RDLC-layoutdesign er mere avanceret end Word-layout. Du kan finde flere oplysninger i [Designe RDLC-rapportlayout](/dynamics-nav/Designing-RDLC-Report-Layouts).

## <a name="built-in-and-custom-report-layouts"></a>Indbyggede og brugerdefinerede rapportlayout
[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder flere indbyggede layout. Indbyggede layout er foruddefinerede layout, der er beregnet til bestemte rapporter. Rapporter i [!INCLUDE[d365fin](includes/d365fin_md.md)] har et indbygget layout, som enten en RDLC-rapportlayout, Word-rapportlayout eller i nogle tilfælde begge. Du kan ikke ændre et indbygget rapportlayout fra [!INCLUDE[d365fin](includes/d365fin_md.md)], men du kan bruge dem som udgangspunkt for opbygning af dine egne brugerdefinerede rapportlayout.

Brugerdefinerede layout er rapportlayout, du designer for at ændre udseendet af en rapport. Du opretter typisk et brugerdefineret layout, der er baseret på et indbygget layout, men du kan oprette dem fra bunden eller fra en kopi af et eksisterende brugerdefineret layout. Med brugerdefinerede layout kan du have flere layout til den samme rapport, som du kan skifte mellem efter behov. For eksempel kan du få forskellige layout for hvert [!INCLUDE[d365fin](includes/d365fin_md.md)]-firma, eller du kan have forskellige layout for samme firma til bestemte lejligheder eller begivenheder såsom en særlig kampagne eller feriesæson.

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a>Beslutte, om du vil bruge et Word- eller RDLC-rapportlayout
Et rapportlayout kan være baseret på et Word-dokument eller en RDLC-fil. Beslutning, om du skal bruge et Word-rapportlayout eller en RDLC-rapportlayouttype, afhænger af, hvordan den genererede rapport skal se ud, og dit kendskab til Word og SQL Server Report Builder.

De generelle designkoncepter for Word- og RDLC-layout er meget ens. Hver type har visse designfunktioner, der påvirker, hvordan den genererede rapport skal vises i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det betyder, at den samme rapport måske ser anderledes ud, når du bruger Word-rapportlayout sammenlignet med RDLC-rapportlayoutet.

Processen til oprettelse af Word-rapportlayout og RDLC-rapportlayout er den samme. Den væsentligste forskel er på den måde, du kan ændre layout på. Word-rapportlayout er typisk lettere at oprette og redigere end RDLC-rapportlayout, fordi du kan bruge Word. RDLC-rapportlayout ændres ved hjælp af SQL Server Report Builder, som er beregnet til mere avancerede brugere.

Du kan finde oplysninger om, hvordan du ændrer, hvilket layout der skal bruges, i [Ændre det aktuelle rapportlayout](ui-how-change-layout-currently-used-report.md).

## <a name="see-related-training-at-microsoft-learnlearnmoduleschange-documents-dynamics-365-business-centralindex"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Opdater brugerdefinerede rapportlayouts](ui-update-report-layouts.md)  
[Sådan opretter og ændrer du Brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md)  
[Importere og eksportere et brugerdefineret rapport- eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Angiv specielle dokumentlayout for debitorer og leverandører](ui-define-customer-vendor-document-layouts.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
