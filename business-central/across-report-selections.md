---
title: Rapportvalg i Business Central
description: Få mere at vide om, hvordan du opretter de rapporter, som bruges til at udskrive forskellige typer dokumenter i Business Central.
author: edupont04
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 16ad3480c10da544c7fdd3a6a299dc6d86cfce46
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134052"
---
# <a name="report-selection-in-business-central"></a>Rapportvalg i Business Central

Du kan angive standardrapporter, der kan anvendes til at udskrive de forskellige dokumenter til salg og køb, f.eks. ordrer, tilbud, fakturaer og kreditnotaer. Hvis du f.eks. har et bestemt layout til salgsfakturaer, kan du angive den rapport i **Rapportvalg - salg**-siden, så de bruges til at sende eller udskrive salgsfakturaer.  

På **Rapportvalg**-siderne kan du angive, hvilken rapport der skal udskrives i forskellige situationer. [!INCLUDE [prod_short](includes/prod_short.md)] indeholder standardkonfigurationer, men du kan selvfølgelig ændre disse standarder. Du kan også tilføje rapporter til **Rapportvalg**-siderne, hvis du f.eks. vil udskrive mere end en rapport pr.dokumenttype.  

## <a name="available-report-selections"></a>Tilgængelige rapportvalg

[!INCLUDE [prod_short](includes/prod_short.md)] indeholder forskellige **rapportvalg**-sider til forskellige områder. I følgende tabel beskrives det, hvor du kan finde oplysninger om de forskellige sider.  

|Område eller en opgave  |Lær mere|
|--------------|----------|
|Eksempel på, hvordan Rapportvalg fungerer (salg)|[Rapportvalg til salgsdokumenter](#example-report-selection-for-sales-documents)|
|Standardlayout for e-mails med salgs-og købsdokumenter  |[Angiv genanvendelig e-mailtekst og layout til salgs-og købsdokumenter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|Definere checklayout     |[Vælge et checklayout](finance-how-define-check-layouts.md) |
|Definere rapporter for momsrapportering (Tyskland)|[Konfigurere rapporter til moms og Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Din [!INCLUDE [prod_short](includes/prod_short.md)] kan f.eks. omfatte yderligere **Rapportvalg**-sider, afhængigt af f.eks. og branche. Du kan altid kontrollere din opsætning ved at vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Ikon, skriv **Rapportvalg** og vælg derefter det relevante link.

Standardversionen af [!INCLUDE [prod_short](includes/prod_short.md)] inkluderer følgende **Rapportsektion**-sider:

* **Rapportvalg - salg**  
* **Rapportvalg - køb**  
* **Rapportvalg - lager**  
* **Rapportvalg - pengestrøm**  
* **Rapporten Valg - lager**  
* **Rapportvalg - bankkonto**  
* **Rapportvalg - rykkere og rentenotaer**  

## <a name="example-report-selection-for-sales-documents"></a>Eksempel: Rapportvalg til salgsdokumenter

**Rapportvalget - salg**-side definerer de standardrapporter, der skal bruges i forskellige scenarier for hver relateret dokumenttype. Vælge et dokumenttype i feltet **Forbrug** og tilføj eller gennemse rapportvalget. Du kan oprette mere end én rapport og den rækkefølge, som rapporter skal sendes eller udskrives i.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Visse dokumenttyper kan sendes som vedhæftede filer i e-mails, og andre kan ikke. Hver **Rapportvalg**-side viser yderligere felter, hvis typen understøtter e-mail fra kassen.  

I **Rapportvalget-salg** og **Rapportvalg-køb**-sider kan du f.eks. oprette e-mail med følgende felter:

|Feltnavn |Description  |
|-----------|-------------|
|**Brug til brødtekst i mail**| Angiver, at opsummerede oplysninger, f.eks. fakturanummer, forfaldsdato og tilknytning til betalingstjeneste, indsættes i meddelelsesteksten på den mail, som du sender.        |
|**Brug til vedhæftet fil i mail**| Angiver, at det relaterede bilag vedhæftes mailen.|
|**Layoutbeskrivelse for brødtekst i mail**|Angiver det e-mail-tekstformat, der bruges, typisk et brugerdefineret rapportlayout. |

## <a name="see-also"></a>Se også

[Angiv genanvendelig e-mailtekst og layout til salgs-og købsdokumenter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[Vælge et checklayout](finance-how-define-check-layouts.md)  
[Konfigurere rapporter til moms og Intrastat (Tyskland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Angiv dokumentlayout for debitorer og leverandører](ui-define-customer-vendor-document-layouts.md)  
[Installation af printere](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]