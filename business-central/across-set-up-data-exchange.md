---
title: Konfigurere dataudveksling | Microsoft Docs
description: Konfigurere dataudvekslingsstrukturen i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3453a29f403360c058c6e17d946f02f6df706a59
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753046"
---
# <a name="setting-up-data-exchange"></a>Konfigurere dataudveksling
Før du kan sende og modtage elektroniske dokumenter eller importere og eksportere bankfiler, skal du konfigurere dataudvekslingsstrukturen for at behandle involverede filer. Derudover skal du definere relaterede områder, f. eks. debitorer, som du sender elektroniske fakturaer til, eller AMC Banking 365 Fundamentals-udvidelsen, hvis du bruger den eksterne tjenesteudbyder til at konvertere dine bankfiler. Du kan finde flere oplysninger under [Udveksle data elektronisk](across-data-exchange.md).  

 Når [!INCLUDE[prod_short](includes/prod_short.md)] er sat op til at udveksle data med eksterne filer, kan brugere bruge opsætningen i almindelige forretningsrelaterede opgaver, f.eks afsendelse og modtagelse af elektroniske dokumenter og importere og eksportere bankfiler.  

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

|**Hvis du vil**|**Skal du se**|  
|------------|-------------|  
|Oprette den forudkonfigurerede dokumentudvekslingstjeneste til at sende og modtage elektroniske dokumenter fra og til [!INCLUDE[prod_short](includes/prod_short.md)].|[Konfigurere en dokumentudvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md)|  
|Indstille den forudkonfigurerede OCR-tjeneste til at omdanne PDF- eller billedfiler til elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)]|[Konfigurere indgående bilag](across-how-setup-income-documents.md)|  
|Opret en af to forudkonfigurerede tjenester for opdaterede valutakurser for at få vist de seneste valutakurser på siden **Valutaer**.|[Opdatere valutakurser](finance-how-update-currencies.md)|  
|Konfigurer forskellige stamdata, såsom firmaoplysninger, debitorer, kreditorer, varer og enheder, der er relateret til tilknytning af data i [!INCLUDE[prod_short](includes/prod_short.md)]|[Konfigurere afsendelse og modtagelse af elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Oprette en bankkonto, en kreditor og en betalingskladde til SEPA-kreditoverførslen.|[Opsætte SEPA-kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer)|  
|Udarbejd bankkontoformater, betalingsformer og kundeaftaler til SEPA Direct Debit.|[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)|  
|Konfigurer brugergodkendelse og URL-adressen på den AMC Banking 365 Fundamentals-udvidelsesudbyder, der skal have bankfiler, der er konverteret til din banks format.|[Brug af AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md)|  
|Konfigurer en ekstern tjeneste, hvor du kan indlæse bankkontoudtog som bankfeeds.|[Konfigurere tjenesten til bankkontoudtog](bank-how-setup-bank-statement-service.md)|  
|Når tjenesten Bankkontoudtog er aktiveret, kan du tilknytte bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)]|[Konfigurere bankkonti](bank-how-setup-bank-accounts.md)|  
|Forbered konfigurationen af en ny dataudvekslingsdefinition for en datafil eller strøm ved hjælp af filens XML-skema for at forhåndsudfylde oversigtspanelet **Kolonnedefinitioner** på siden **Bogføringsudvekslingsdefinition**.|[Bruge XML-skemaer til at forberede dataudvekslingsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Konfigurer Exchange Data Framework for at gøre det muligt for brugerne at modtage et nyt købsdokumentformat, sende et nyt salgsdokumentformat, importere en ny bankfil eller anden dataudveksling.|[Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Se også  
[Udveksle data elektronisk](across-data-exchange.md)  
[Indgående bilag](across-income-documents.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]