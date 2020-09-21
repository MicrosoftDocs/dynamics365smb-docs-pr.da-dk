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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: f299c9c38211b4dc265402b4079fe283e318113c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780706"
---
# <a name="exchanging-data"></a>Udveksle data
Du kan udveksle data mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og eksterne filer eller streams i forbindelse med almindelige forretningsrelaterede opgaver, f.eks. afsendelse og modtagelse af elektroniske dokumenter og importere og eksportere bankfiler.  

Før du kan sende og modtage elektroniske dokumenter eller importere og eksportere bankfiler, skal du konfigurere dataudvekslingsstrukturen for at behandle datafiler eller -streams. Derudover skal du definere relaterede områder, f. eks. debitorer, som du sender elektroniske fakturaer til, og AMC Banking 365 Fundamentals-udvidelsen, hvis du distribuerer bankfiler til en ekstern tjenesteudbyder. Du kan finde flere oplysninger i [Konfiguration af dataudveksling](across-set-up-data-exchange.md).  

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

|**For at**|**Skal du se**|  
|------------|-------------|  
|Konvertere salgsdokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] til et standardiseret format, og send dem som elektroniske dokumenter, som kunderne kan modtage i deres system.|[Sende elektroniske dokumenter](sales-how-to-send-electronic-documents.md)|  
|Send PDF- eller billedfiler til en udbyder af OCR-tjenester og modtage dem igen som elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md)|  
|Modtag elektroniske dokumenter, enten fra OCR-tjenesten eller dokumentudvekslingstjenesten i et standardformat, som du konverterer til de relevante dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Modtage og konvertere elektroniske dokumenter](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Forbered indlæsning af en kontoudtogsfil på siden **Betalingsudligningskladde** som første trin i afstemning af betalinger eller på siden **Bankkontoafstemning** som første trin i afstemning af bankkonti.|[Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)|  
|Eksportér betalinger fra siden **Udbetalingskladde** til en bankfil, som du overfører til din elektroniske bankkonto til behandling.|[Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)|
|Oprette elektroniske betalinger i henhold til standarden for EU-SEPA-kreditoverførsel.|[Foretage betalinger med AMC Banking 365 Fundamentals-udvidelsen eller SEPA-kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Bed din bank om at overføre beløb fra din kundes bankkonti til dit firmas konto i overensstemmelse med konfigurationen af SEPA Direct Debit.|[Oprette poster i SEPA Direct Debit-opkrævning, og eksportere til en bankfil](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)|  
|Brug en udbyder af valutakurstjenester til at opdatere siden **Valutaer**.|[Opdatere valutakurser](finance-how-update-currencies.md)|  
|Få vist, hvilke elementer der er knyttet til felterne i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved import af SEPA CAMT-sætningsfiler.|[Feltkobling, når du importerer SEPA-CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Se, hvilke felter i [!INCLUDE[d365fin](includes/d365fin_md.md)], der er knyttet til filelementer, når du eksporterer betalingsfiler ved hjælp af AMC Banking 365 Fundamentals-udvidelsen.|[Felttilknytning ved eksport af betalingsfiler ved hjælp af AMC Banking 365 Fundamentals-udvidelsen](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Se også  
[Konfigurere dataudveksling](across-set-up-data-exchange.md)  
[Udveksle data elektronisk](across-data-exchange.md)  
[Fakturere salg](sales-how-invoice-sales.md)   
[Registrere køb](purchasing-how-record-purchases.md)  
[Indgående bilag](across-income-documents.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
