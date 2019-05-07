---
title: Arbejde med indgående bilag | Microsoft Docs
description: Du kan administrere indgående eksterne virksomhedsdokumenter, f.eks. betalingskvitteringer eller PDF-filer, styre OCR-opgaver og konvertere filerne til elektroniske dokumenter og poster.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7d5da0999a2e1b549018b104bd02830939154884
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "923365"
---
# <a name="incoming-documents"></a>Indgående bilag
Nogle forretningstransaktioner registreres ikke i [!INCLUDE[d365fin](includes/d365fin_md.md)] fra begyndelsen. I stedet sendes et eksternt forretningsdokument til din virksomhed som en vedhæftet fil i mail eller som en papirkopi, som du indscanne i en fil. Dette er typisk for køb, hvor sådanne indgående dokumentfiler repræsenterer betalingskvitteringer for udgifter eller mindre køb.

Fra PDF-filer eller billedfiler, der repræsenterer indgående bilag, kan du få en ekstern OCR-tjeneste (Optical Character Recognition) til at oprette elektroniske dokumenter, som derefter kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].

På siden **Indkommende dokumenter** kan du bruge forskellige funktioner til at gennemgå udgiftsbilag, administrere OCR-opgaver og konvertere indgående dokumentfiler, manuelt eller automatisk, til de relevante købs- og salgsdokumenter eller kladdelinjer. Eksterne filer kan tilknyttes i enhver procesfase, herunder til bogførte dokumenter og til de derved oprettede kreditor-, debitor- og finansposter.

Det indgående dokument kan bestå af følgende primære aktiviteter:

* Registrer eksterne dokumenter i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at oprette linjer på siden **Indgående bilag** på en af følgende måder:
  * Manuelt ved at bruge simple funktioner fra en pc eller fra en mobilenhed på en af følgende måder:
    * Brug knappen **Opret fra fil**, og udfyld derefter de relevante felter på siden **Indgående dokument**. Filen vedhæftes automatisk.  
    * Brug knappen **Ny**, og udfyld derefter de relevante felter på siden **Indgående dokument**, og vedhæft manuelt den relaterede fil.
    * Fra en tablet eller telefon skal du bruge knappen **Opret fra kamera** til at oprette en ny indgående dokumentpost og derefter sende billedet til OCR-tjenesten f.eks.
  * Automatisk ved at modtage dokumentet fra OCR-tjenesten som et elektronisk dokument, når du har sendt en mail med den relaterede PDF- eller billedfil til OCR-tjenesten. Oversigtspanelet **Finansielle oplysninger** udfyldes automatisk på siden **Indgående dokument**.
* Bruge OCR-tjenesten til at omdanne PDF- eller billedfiler til elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Opret nye dokumenter eller finanskladdelinjer for indgående bilagsrecords ved at angive oplysninger, mens du læser dem fra indgående dokumentfiler.
* Vedhæfte indgående dokumentfiler for købs- og salgsdokumenter af enhver status, herunder til de kreditor-, debitor- og finansposter, der stammer fra bogføring.
* Få vist indgående dokumentposter og de vedhæftede filer fra ethvert købs- og salgsdokument eller post eller finde alle finansposter uden indgående dokumentposter fra siden **Kontoplan**.

| Hvis du vil | Se |
| --- | --- |
| Konfigurer funktionen indgående dokumenter og oprette OCR tjenesten. |[Konfigurere indgående bilag](across-how-setup-income-documents.md) |
| Opret indgående dokumentposter, tilknyt filer, brug OCR til at omdanne PDF-filer til elektroniske dokumenter, konverter elektroniske dokumenter til bilagsposter, overvåg bogførte salgs- og købsdokumenter fra indgående dokumentposter. |[Behandle indgående bilag](across-process-income-documents.md) |

## <a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
