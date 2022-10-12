---
title: Rapportvalg i Business Central
description: Få mere at vide om, hvordan du opretter de rapporter, som bruges til at udskrive forskellige typer dokumenter i Business Central.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 06/09/2022
ms.author: bholtorf
ms.openlocfilehash: fc5bfe8b22d06455379dabd20723fb0ccfe4032b
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607495"
---
# <a name="report-selection-for-documents-in-business-central"></a>Rapportvalg til dokumenter i Business Central

Du kan oprette standardrapporter, der skal bruges til at udskrive dokumenter til salg, køb og service, f.eks. ordrer, tilbud og fakturaer. Hvis du f.eks. har et bestemt layout til salgsfakturaer, kan du angive den rapport i **Rapportvalg - salg**-siden, så de bruges til at sende eller udskrive salgsfakturaer.  

## <a name="available-report-selections"></a>Tilgængelige rapportvalg

På **Rapportvalg**-siderne kan du angive, hvilken rapport der skal udskrives i forskellige situationer. [!INCLUDE [prod_short](includes/prod_short.md)] indeholder standardkonfigurationer, men du kan ændre dem efter behov. Du kan også tilføje rapporter til **Rapportvalg**-siderne, hvis du f.eks. vil udskrive mere end en rapport pr.dokumenttype. 

I følgende tabel beskrives det, hvor du kan finde oplysninger om de forskellige sider.  

|Område eller en opgave  |Lær mere|
|--------------|----------|
|Eksempel på, hvordan rapportvalg fungerer (salg)|[Rapportvalg til salgsdokumenter](#example-report-selection-for-sales-documents) findes nedenfor|
|Standardlayout for e-mails med salgs-og købsdokumenter  |[Angiv genanvendelig e-mailtekst og layout til salgs-og købsdokumenter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Definere checklayout     |[Vælge et checklayout](finance-how-define-check-layouts.md) |
|Definere rapporter til momsrapportering (Tyskland)|[Konfigurere rapporter til moms og Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Din [!INCLUDE [prod_short](includes/prod_short.md)] kan f.eks. omfatte yderligere **Rapportvalg**-sider, afhængigt af f.eks. og branche. Du kan kontrollere din opsætning ved at vælge den ![lyspære, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Angiv **Rapportvalg**, og vælg derefter det relevante link.

Standardversionen af [!INCLUDE [prod_short](includes/prod_short.md)] inkluderer følgende **Rapportvalg**-sider:

* **Rapportvalg - salg**  
* **Rapportvalg - køb**  
* **Rapportvalg - lager**  
* **Rapportvalg - pengestrøm**  
* **Rapporten Valg - lager**  
* **Rapportvalg - bankkonto**  
* **Rapportvalg – sag**  
* **Rapportvalg - service**

## <a name="example-report-selection-for-sales-documents"></a>Eksempel: Rapportvalg til salgsdokumenter

**Rapportvalget - salg**-siden definerer de standardrapporter, der skal bruges i forskellige scenarier for hver relateret dokumenttype. Vælg en dokumenttype i feltet **Forbrug**, og tilføj eller gennemse rapportvalget. Du kan oprette mere end én rapport og angive den rækkefølge, som rapporter skal sendes eller udskrives i.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Du kan sende alle typer dokumenter som vedhæftede filer i mail. Til dem indeholder siden **Rapportvalg** ekstra felter.  

På siderne **Rapportvalg - salg** og **Rapportvalg - køb** kan du f.eks. oprette mail med følgende felter:

|Feltnavn |Beskrivelse  |
|-----------|-------------|
|**Brug til brødtekst i mail**| Indsæt opsummerede oplysninger, f.eks. fakturanummer, forfaldsdato eller et link til en betalingstjeneste, i en mail.        |
|**Brug til vedhæftet fil i mail**| Knyt det relaterede dokument til e-mailen.|
|**Layoutbeskrivelse for brødtekst i mail**|Angiv det e-mailformat, der skal bruges. Det er typisk et brugerdefineret rapportlayout. |

## <a name="see-also"></a>Se også

[Konfigurere genanvendelige e-mailtekster og -layout](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Vælge et checklayout](finance-how-define-check-layouts.md)  
[Konfigurere rapporter til moms og Intrastat (Tyskland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Angiv dokumentlayout for debitorer og leverandører](ui-define-customer-vendor-document-layouts.md)  
[Installation af printere](ui-specify-printer-selection-reports.md)  
[Finansrapporter og analyser i Business Central](finance-reports.md)  
[Rapporter og analyser for debitor i Business Central](receivables-reports.md)  
[Kreditorrapporter og -analyser i Business Central](payables-reports.md)  
[Anlægsrapporter og analyser i Business Central](fa-reports.md)  
[Rapporter og analyser i Business Central](project-reports.md)  
[Salgsrapporter og analyser i Business Central](sales-reports.md)  
[Købsrapporter og analyser i Business Central](purchase-reports.md)  
[Lager- og lagerstedrapporter og -analyse i Business Central](inventory-WMS-reports.md)  
[Samle rapporter og analyser i Business Central](assembly-reports.md)  
[Produktionsrapporter og analyser i Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
