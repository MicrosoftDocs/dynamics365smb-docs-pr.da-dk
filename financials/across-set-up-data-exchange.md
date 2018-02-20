---
title: Konfigurere dataudveksling | Microsoft Docs
description: Konfigurere dataudvekslingsstrukturen i Finance and Operations, Business edition.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a043ad387455cf93182689b0c58025be7186c0cd
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-data-exchange"></a>Konfigurere dataudveksling
Før du kan sende og modtage elektroniske dokumenter eller importere og eksportere bankfiler, skal du konfigurere dataudvekslingsstrukturen for at behandle involverede filer. Desuden skal du konfigurere relaterede områder, såsom stamdata for debitorer, som du sender elektroniske fakturaer til, eller tjenesten til konvertering af bankdata, hvis du bruger den eksterne tjenesteudbyder til at konvertere dine bankfiler. Du kan finde flere oplysninger under [Udveksle data elektronisk](across-data-exchange.md).  

 Når [!INCLUDE[d365fin](includes/d365fin_md.md)] er sat op til at udveksle data med eksterne filer, kan brugere bruge opsætningen i almindelige forretningsrelaterede opgaver, f.eks afsendelse og modtagelse af elektroniske dokumenter og importere og eksportere bankfiler.  

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

|**For at**|**Skal du se**|  
|------------|-------------|  
|Oprette den forudkonfigurerede dokumentudvekslingstjeneste til at sende og modtage elektroniske dokumenter fra og til [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Konfigurere en dokumentudvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md)|  
|Indstille den forudkonfigurerede OCR-tjeneste til at omdanne PDF- eller billedfiler til elektroniske dokumenter, der kan konverteres til dokumentposter i  [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Konfigurere indgående bilag](across-how-setup-income-documents.md)|  
|Opret en af to forudkonfigurerede tjenester for opdaterede valutakurser for at få vist de seneste valutakurser i vinduet **Valutaer**.|[Opdatere valutakurser](finance-how-update-currencies.md)|  
|Konfigurer forskellige stamdata, såsom firmaoplysninger, debitorer, kreditorer, varer og enheder, der er relateret til tilknytning af data i  [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Konfigurere afsendelse og modtagelse af elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Oprette en bankkonto, en kreditor og en betalingskladde til SEPA-kreditoverførslen.|[Opsætte SEPA-kreditoverførsel](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Udarbejd bankkontoformater, betalingsformer og kundeaftaler til SEPA Direct Debit.|[Konfigurere SEPA Direct Debit](finance-how-to-set-up-sepa-direct-debit.md)|  
|Konfigurer brugergodkendelse og URL-adressen på bankdatakonverteringens serviceudbyder, der skal have bankfiler, der er konverteret til din banks format.|[Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-data-conversion-service.md)|  
|Konfigurer en ekstern tjeneste, hvor du kan indlæse bankkontoudtog som bankfeeds.|[Konfigurere tjenesten til bankkontoudtog](bank-how-setup-bank-statement-service.md)|  
|Når tjenesten Bankkontoudtog er aktiveret, kan du tilknytte bankkonti i  [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Konfigurere bankkonti](bank-how-setup-bank-accounts.md)|  
|Forbered konfigurationen af en ny dataudvekslingsdefinition for en datafil eller strøm ved hjælp af filens XML-skema for at forhåndsudfylde oversigtspanelet **Kolonnedefinitioner** i vinduet **Bogføringsudvekslingsdefinition**.|[Bruge XML-skemaer til at forberede dataudvekslingsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Konfigurer Exchange Data Framework for at gøre det muligt for brugerne at modtage et nyt købsdokumentformat, sende et nyt salgsdokumentformat, importere en ny bankfil eller anden dataudveksling.|[Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Se også  
[Udveksle data elektronisk](across-data-exchange.md)  
[Udveksle data](across-exchange-data.md)   
[Indgående bilag](across-income-documents.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  

