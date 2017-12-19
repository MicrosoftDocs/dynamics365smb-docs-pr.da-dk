---
title: Udveksle data | Microsoft Docs
description: Du kan udveksle data mellem Dynamics 365 og eksterne filer eller streams i forbindelse med almindelige forretningsrelaterede opgaver, f.eks. afsendelse og modtagelse af elektroniske dokumenter og importere og eksportere bankfiler.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 41f42162499401693f30e37a736c4fe0afe24822
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="exchanging-data"></a>Udveksle data
Du kan udveksle data mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og eksterne filer eller streams i forbindelse med almindelige forretningsrelaterede opgaver, f.eks. afsendelse og modtagelse af elektroniske dokumenter og importere og eksportere bankfiler.  

Før du kan sende og modtage elektroniske dokumenter eller importere og eksportere bankfiler, skal du konfigurere dataudvekslingsstrukturen for at behandle involverede filer eller streams. Derudover skal du oprette relaterede områder. De omfatter stamdata for debitorer, som du sender elektroniske fakturaer til og tjenesten til konvertering af bankdata, hvis du distribuere bankfilkonverteringer til en ekstern internetudbyder. Du kan finde flere oplysninger i [Konfiguration af dataudveksling](across-set-up-data-exchange.md).  

 Følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

|**For at**|**Skal du se**|  
|------------|-------------|  
|Konvertere salgsdokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] til et standardiseret format, og send dem som elektroniske dokumenter, som kunderne kan modtage i deres system.|[Fremgangsmåde: Sende elektroniske dokumenter](sales-how-to-send-electronic-documents.md)|  
|Send PDF- eller billedfiler til en udbyder af OCR-tjenester og modtage dem igen som elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Fremgangsmåde: Bruge OCR til at gøre PDF og filer til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md)|  
|Modtag elektroniske dokumenter, enten fra OCR-tjenesten eller dokumentudvekslingstjenesten i et standardformat, som du konverterer til de relevante dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Fremgangsmåde: Modtage og konvertere elektroniske dokumenter](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Indlæs en kontoudtogsfil i vinduet **Betalingsudligningskladde** som første trin i afstemning af betalinger eller i vinduet **Bankkontoafstemning** som første trin i afstemning af bankkonti.|[Fremgangsmåde: Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)|  
|Eksportér betalinger fra vinduet **Udbetalingskladde** til en bankfil, som du overfører til din elektroniske bankkonto til behandling.|[Fremgangsmåde: Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md)|
|Oprette elektroniske betalinger i henhold til standarden for EU-SEPA-kreditoverførsel.|[Foretage indbetalinger med tjenesten til konvertering af bankdata eller SEPA Kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Bed din bank om at overføre beløb fra din kundes bankkonti til dit firmas konto i overensstemmelse med konfigurationen af SEPA Direct Debit.|[Fremgangsmåde: Opret poster i SEPA Direct Debit-opkrævning, og eksportér til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Brug en udbyder af valutakurstjenester til at opdatere vinduet **Valutaer**.|[Fremgangsmåde: Opdatere valutakurser](finance-how-update-currencies.md)|  
|Få vist, hvilke elementer der er knyttet til felterne i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved import af SEPA CAMT-sætningsfiler.|[Feltkobling, når du importerer SEPA-CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Se, hvilke felter i [!INCLUDE[d365fin](includes/d365fin_md.md)], der er knyttet til filelementer, når du eksporterer betalingsfiler ved at bruge funktionen Tjeneste til konvertering af bankdata.|[Feltkobling, når du eksporterer betalingsfiler ved hjælp af tjeneste til konvertering af bankdata](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Se også  
[Konfigurere dataudveksling](across-set-up-data-exchange.md)  
[Udveksle data elektronisk](across-data-exchange.md)  
[Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md)   
[Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md)  
[Indgående bilag](across-income-documents.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  

