---
title: Feltkobling til eksport af bankbetalingsfiler | Microsoft Docs
description: "Når du eksporterer betalingsfiler ved hjælp af funktionen Tjeneste til konvertering af bankdata, bliver de data, du eksporterer, eksponeret for udbyderen af tjenesten til konvertering af bankdata."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 69ca175c1b73e18dfbad1d0682d877021b5d94d7
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="field-mapping-when-exporting-payment-files-using-bank-data-conversion-service"></a>Feltkobling, når du eksporterer betalingsfiler ved hjælp af tjeneste til konvertering af bankdata
Når du eksporterer betalingsfiler ved hjælp af funktionen Tjeneste til konvertering af bankdata, bliver de data, du eksporterer, eksponeret for udbyderen af tjenesten til konvertering af bankdata. Serviceudbyderen er ansvarlig for beskyttelsen af disse data. Du kan finde flere oplysninger om, hvordan tjenesten til konvertering af bankdata fungerer, i [Om Data Exchange Framework](across-about-the-data-exchange-framework.md).  

> [!CAUTION]  
>  Når du eksporterer betalingsfiler ved hjælp af funktionen Tjeneste til konvertering af bankdata, vil nogle af virksomhedens data blive eksponeret for udbyderen af tjenesten. Serviceudbyderen, AMC Consult A/S, er ansvarlig for beskyttelsen af disse data. Du kan finde flere oplysninger i [AMC's politik for beskyttelse af personlige oplysninger](http://go.microsoft.com/fwlink/?LinkId=510158).  

Følgende tabel viser felterne i [!INCLUDE[d365fin](includes/d365fin_md.md)], fra hvilke data kan eksporteres til serviceudbyderen.  

|Koblet felt|Felt i tabel|Sortbord|Beskrivelse]-->|  
|------------------|--------------------|-----------|---------------------------------------|  
|Kreditornummer|Kreditornummer|Bankkonto|Det id, der er tildelt din virksomhed af banken for at opkræve betalinger|  
|Afsenders bankkontonr.|Bankkontonr./IBAN|Bankkonto|Dit firmas bankkontonummer (IBAN eller andet), der er angivet på bankkontokortet|  
|Afsenderbanks clearingstandard|Bankclearingsstandard|Bankkonto|Nationalbanknavneregistret bruges til afsenderens bankkonto|  
|Afsenderbanks clearingkode|Kode for bankclearing|Bankkonto|Id for afsenderens bank i forbindelse med banknavneregisteret, der bruges|  
|Afsenders bank-BIC|SWIFT-kode|Bankkonto|SWIFT-identifikator for afsenderens bankkonto|  
|Afsenderbanks kontovaluta|Valutakode|Bankkonto|Afsenderbankkontoens valutakode|  
|Bilagsnr.|Bilagsnr.|Finanskladdelinje|Bilagsnummeret på betalingslinjen|  
|Eksternt udlign.bilagsnr.|Eksternt udlign.bilagsnr.|Finanskladdelinje|Det eksterne bilagsnummer på fakturaen eller kreditnotaen, som betalingslinjen udlignes med.|  
|Modtager-id|Kontonummer|Finanskladdelinje|Det debitor- eller kreditornummer, som er angivet på betalingslinjen.|  
|Betalingstype|Betalingstype for bankdatakonvertering|Betalingsform|Typen af bankoverførsel såsom indenlandsk eller international|  
|Betalingsreference|Betalingsreference|Finanskladdelinje|Betalingsreferencen på betalingslinjen|  
|Modtagers adresse|Adresse|Debitor/Kreditor|Det modtageradresse, som er angivet på debitor- eller leverandørkortet|  
|Modtagers by|By|Debitor/Kreditor|Den modtagerby, som er angivet på debitor- eller leverandørkortet|  
|Modtagers navn|Navn|Debitor/Kreditor|Det modtagernavn, som er angivet på debitor- eller leverandørkortet|  
|Modtagers lande-/områdekode|Lande-/områdekode|Debitor/Kreditor|Modtagerens lande-/områdekode, som er angivet på debitor- eller leverandørkortet|  
|Modtagers postnr.|Postnr.|Debitor/Kreditor|Modtagerens postnummer, som er angivet på debitor- eller leverandørkortet|  
|Modtagers bankkontonr.|Bankkontonr./IBAN|Debitorbankkonto/Kreditorbankkonto|Modtagerens bankkontonummer (IBAN eller andet), der er angivet på debitor- eller kreditorbankkontokortet|  
|Modtagerbanks clearingkode|Bankclearingsstandard|Debitorbankkonto/Kreditorbankkonto|Nationalbanknavneregistret bruges til modtagerens bankkonto|  
|Modtagerbanks clearingstandard|Kode for bankclearing|Debitorbankkonto/Kreditorbankkonto|Id for modtagerens bankkonto i forbindelse med banknavneregisteret, der bruges|  
|Modtagers mailadresse|E-mail|Debitor/Kreditor|Modtagerens mailadresse|  
|Meddelelse til modtager 1|Meddelelse til modtager|Finanskladdelinje|Meddelelse til modtager, der er angivet på betalingslinjen|  
|Beløb|Beløb|Finanskladdelinje|Betalingslinjens beløb.|  
|Valutakode|Valutakode|Finanskladdelinje|Valutakoden på betalingslinjen|  
|Overflytningsdato|Bogføringsdato|Finanskladdelinje|Bogføringsdatoen for betalingslinjen|  
|Fakturabeløb|Oprindeligt beløb|Debitorpost/Kreditorpost|Beløbet på den post, som betalingen er udlignet på.|  
|Fakturadato|Bilagsdato|Debitorpost/Kreditorpost|Fakturadatoen på den post, som betalingen er udlignet på|  
|Modtagerbanks adresse|Adresse|Debitorbankkonto/Kreditorbankkonto|Modtagerens bankkontoadresse, der er angivet på debitor- eller kreditorbankkontokortet|  
|Modtagerens bankkontoadresse, der er angivet på debitor- eller kreditorbankkontokortet|By|Debitorbankkonto/Kreditorbankkonto|Modtagerens bankkontoby, der er angivet på debitor- eller kreditorbankkontokortet|  
|Modtagerbanks navn|Navn|Debitorbankkonto/Kreditorbankkonto|Modtagerens bankkontonavn, der er angivet på debitor- eller kreditorbankkontokortet|  
|Modtagerbanks land/område|Lande-/områdekode|Debitorbankkonto/Kreditorbankkonto|Modtagerens bankkontoland/-område, der er angivet på debitor- eller kreditorbankkontokortet|  
|Modtagerbanks postnr.|Postnr.|Debitorbankkonto/Kreditorbankkonto|Modtagerens bankkontopostnummer, der er angivet på debitor- eller kreditorbankkontokortet|  
|Afsenderbanks adresse|Adresse|Bankkonto|Afsenderens bankkontoadresse, der er angivet på bankkontokortet|  
|Afsenderbanks by|By|Bankkonto|Afsenderens bankkontoby, der er angivet på bankkontokortet|  
|Afsenderbanks navn|Navn|Bankkonto|Afsenderens bankkontonavn, der er angivet på bankkontokortet|  
|Afsenderbanks land/område|Lande-/områdekode|Bankkonto|Afsenderens bankkontoland/-område, der er angivet på bankkontokortet|  
|Afsenderbanks postnummer|Postnr.|Bankkonto|Afsenderens bankkontopostnummer, der er angivet på bankkontokortet|  
|Finanskladdetype|Kladdetypenavn|Finanskladdelinje|Finanskladdeskabelonen, der bruges til betalingslinjen|  
|Finanskladdenavn|Kladdenavn|Finanskladdelinje|Finanskladdenavnet, der bruges til betalingslinjen|  
|Afsenderbanks navn - datakonvertering|Banknavn - datakonvertering|Bankkonto|Afsenderens bankkontonavn, der er anmodet om af tjenesten til konvertering af bankdata og angivet på bankkontokortet|  

## <a name="see-also"></a>Se også  
[Konfigurere dataudveksling](across-set-up-data-exchange.md)  
[Udveksle data som elektroniske dokumenter](across-data-exchange.md)
[Fremgangsmåde: Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-data-conversion-service.md)   
[Foretag indbetalinger med tjenesten til konvertering af bankdata eller SEPA Kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   

