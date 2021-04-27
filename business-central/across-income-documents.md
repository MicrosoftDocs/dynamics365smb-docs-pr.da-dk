---
title: Arbejde med indgående bilag | Microsoft Docs
description: Du kan administrere indgående eksterne virksomhedsdokumenter, f.eks. betalingskvitteringer eller PDF-filer, styre OCR-opgaver og konvertere filerne til elektroniske dokumenter og poster.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8e02cd4627219c7ea439155b2b91b61e03534dc2
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788479"
---
# <a name="incoming-documents"></a>Indgående bilag

Nogle forretningstransaktioner registreres ikke i [!INCLUDE[prod_short](includes/prod_short.md)] fra begyndelsen. I stedet sendes et eksternt forretningsdokument til din virksomhed som en vedhæftet fil i mail eller som en papirkopi, som du indscanne i en fil. Dette er typisk for køb, hvor sådanne indgående bilagsfiler repræsenterer betalingskvitteringer for udgifter eller mindre køb.

Fra PDF-filer eller billedfiler, der repræsenterer indgående bilag, kan du få en ekstern OCR-tjeneste (Optical Character Recognition) til at oprette elektroniske dokumenter, som derefter kan konverteres til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)]. Vælg en servicepakke, der passer til din organisation og/eller dit land/område. Du kan også oprette poster manuelt, så de repræsenterer eksterne dokumenter.  

På siden **Indgående bilag** kan du bruge forskellige funktioner til at gennemgå udgiftsbilag, administrere OCR-opgaver og konvertere indgående bilagsfiler, manuelt eller automatisk, til de relevante købs- og salgsdokumenter eller kladdelinjer. Eksterne filer kan tilknyttes i enhver procesfase, herunder til bogførte dokumenter og til de derved oprettede kreditor-, debitor- og finansposter.

Det indgående bilag kan bestå af følgende primære aktiviteter:

* Registrer eksterne dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)] ved at oprette linjer på siden **Indgående bilag** på en af følgende måder:
  * Manuelt ved at bruge simple funktioner fra en pc eller fra en mobilenhed på en af følgende måder:
    * Brug knappen **Opret fra fil**, og udfyld derefter de relevante felter på siden **Indgående bilag**. Filen vedhæftes automatisk.  
    * Brug knappen **Ny**, og udfyld derefter de relevante felter på siden **Indgående bilag**, og vedhæft manuelt den relaterede fil.
    * Fra en tablet eller telefon skal du bruge knappen **Opret fra kamera** til at oprette en ny indgående bilagspost og derefter sende billedet til OCR-tjenesten f.eks.
  * Automatisk ved at modtage dokumentet fra OCR-tjenesten som et elektronisk dokument, når du har sendt en mail med den relaterede PDF- eller billedfil til OCR-tjenesten. Oversigtspanelet **Finansielle oplysninger** udfyldes automatisk på siden **Indgående bilag**.
* Bruge OCR-tjenesten til at omdanne PDF- eller billedfiler til elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)].
* Opret nye dokumenter eller finanskladdelinjer for indgående bilagsposter ved at angive oplysninger, mens du læser dem fra indgående bilagsfiler.
* Vedhæfte indgående bilagsfiler for købs- og salgsdokumenter af enhver status, herunder til de kreditor-, debitor- og finansposter, der stammer fra bogføring.
* Få vist indgående bilagsposter og de vedhæftede filer fra ethvert købs- og salgsdokument eller post eller finde alle finansposter uden indgående bilagsposter fra siden **Kontoplan**.

| Hvis du vil | Se |
| --- | --- |
| Konfigurer funktionen indgående bilag og oprette OCR tjenesten. |[Konfigurere indgående bilag](across-how-setup-income-documents.md) |
| Opret indgående bilagsposter, tilknyt filer, brug OCR til at omdanne PDF-filer til elektroniske dokumenter, konverter elektroniske dokumenter til bilagsposter, overvåg bogførte salgs- og købsdokumenter fra indgående bilagsposter. |[Behandle indgående bilag](across-process-income-documents.md) |

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/incoming-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]