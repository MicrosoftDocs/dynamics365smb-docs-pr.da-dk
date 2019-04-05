---
title: Udveksle data | Microsoft Docs
description: Du kan udveksle data mellem Business Central og eksterne filer eller streams i forbindelse med almindelige forretningsrelaterede opgaver, f.eks. afsendelse og modtagelse af elektroniske dokumenter og importere og eksportere bankfiler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 678b15b8d15dba477ac09c2651964525f4afe26a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792341"
---
# <a name="exchanging-data"></a>Udveksle data
Du kan udveksle data mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og eksterne filer eller streams i forbindelse med almindelige forretningsrelaterede opgaver, f.eks. afsendelse og modtagelse af elektroniske dokumenter og importere og eksportere bankfiler.  

Før du kan sende og modtage elektroniske dokumenter eller importere og eksportere bankfiler, skal du konfigurere dataudvekslingsstrukturen for at behandle involverede filer eller streams. Derudover skal du oprette relaterede områder. De omfatter stamdata for debitorer, som du sender elektroniske fakturaer til og tjenesten til konvertering af bankdata, hvis du distribuere bankfilkonverteringer til en ekstern internetudbyder. Du kan finde flere oplysninger i [Konfiguration af dataudveksling](across-set-up-data-exchange.md).  

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

|**For at**|**Skal du se**|  
|------------|-------------|  
|Konvertere salgsdokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] til et standardiseret format, og send dem som elektroniske dokumenter, som kunderne kan modtage i deres system.|[Sende elektroniske dokumenter](sales-how-to-send-electronic-documents.md)|  
|Send PDF- eller billedfiler til en udbyder af OCR-tjenester og modtage dem igen som elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md)|  
|Modtag elektroniske dokumenter, enten fra OCR-tjenesten eller dokumentudvekslingstjenesten i et standardformat, som du konverterer til de relevante dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Modtage og konvertere elektroniske dokumenter](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Forbered indlæsning af en kontoudtogsfil på siden **Betalingsudligningskladde** som første trin i afstemning af betalinger eller på siden **Bankkontoafstemning** som første trin i afstemning af bankkonti.|[Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)|  
|Eksportér betalinger fra siden **Udbetalingskladde** til en bankfil, som du overfører til din elektroniske bankkonto til behandling.|[Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md)|
|Oprette elektroniske betalinger i henhold til standarden for EU-SEPA-kreditoverførsel.|[Foretage indbetalinger med tjenesten til konvertering af bankdata eller SEPA Kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Bed din bank om at overføre beløb fra din kundes bankkonti til dit firmas konto i overensstemmelse med konfigurationen af SEPA Direct Debit.|[Oprette poster i SEPA Direct Debit-opkrævning, og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Brug en udbyder af valutakurstjenester til at opdatere siden **Valutaer**.|[Opdatere valutakurser](finance-how-update-currencies.md)|  
|Få vist, hvilke elementer der er knyttet til felterne i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved import af SEPA CAMT-sætningsfiler.|[Feltkobling, når du importerer SEPA-CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Se, hvilke felter i [!INCLUDE[d365fin](includes/d365fin_md.md)], der er knyttet til filelementer, når du eksporterer betalingsfiler ved at bruge funktionen Tjeneste til konvertering af bankdata.|[Feltkobling, når du eksporterer betalingsfiler ved hjælp af tjeneste til konvertering af bankdata](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Se også  
[Konfigurere dataudveksling](across-set-up-data-exchange.md)  
[Udveksle data elektronisk](across-data-exchange.md)  
[Fakturere salg](sales-how-invoice-sales.md)   
[Registrere køb](purchasing-how-record-purchases.md)  
[Indgående bilag](across-income-documents.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
