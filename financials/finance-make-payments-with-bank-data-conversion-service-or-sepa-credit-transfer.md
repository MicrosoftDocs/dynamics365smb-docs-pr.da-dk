---
title: "Foretage indbetalinger med tjenesten til konvertering af bankdata eller SEPA Kreditoverførsel | Microsoft Docs"
description: Du kan behandle betalinger til dine kreditorer ved at eksportere en fil sammen med betalingsoplysningerne fra kladdelinjerne.
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d9388a99585eea4e9e229a2f47982f9f690e3001
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a>Foretage indbetalinger med tjenesten til konvertering af bankdata eller SEPA Kreditoverførsel
I vinduet **Udbetalingskladde** kan du behandle betalinger til dine kreditorer ved at eksportere en fil sammen med betalingsoplysningerne fra kladdelinjerne. Derefter kan du uploade filen til din elektroniske bank, hvor de relaterede pengeoverførsler behandles. [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter SEPA-kreditoverførselsformatet, men i dit land/område anvendes der muligvis andre formater til elektroniske betalinger.   

 Hvis du vil aktivere SEPA-kreditoverførsler, skal du først angive en bankkonto, en kreditor og finanskladdenavnet, som betalingskladden er baseret på. Derefter forbereder du betalinger til kreditorer ved automatisk at udfylde vinduet **Udbetalingskladde** med forfaldne betalinger med angivne bogføringsdatoer.  

> [!NOTE]  
>  Når du har kontrolleret, at betalingerne er behandlet af banken, kan du fortsætte med at bogføre udbetalingskladdens linjer.  

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Aktiver funktionen Tjeneste til konvertering af bankdata for at konvertere en fil med bankkontoudtog til et format, som du kan importere, eller for at få dine eksporterede betalingsfiler konverteret tilbage til det format, som din bank kræver.|[Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-statement-service.md)|  
|Oprette en bankkonto, en kreditor og en betalingskladde til SEPA-kreditoverførslen.|[Opsætte SEPA-kreditoverførsel](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Udfyld betalingskladdelinjerne for forfaldne betalinger til kreditorer med mulighed for at indsætte bogføringsdatoer, der er baseret på forfaldsdatoen for de relaterede købsdokumenter.|[Administrere skyldige beløb](payables-manage-payables.md)|  
|Eksportér betalingskladdelinjer til en fil i SEPA-kreditoverførselsformat.|[Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md)|  
|Når elektronisk betaling er behandlet af banken, kan du bogføre betalingerne.|[Arbejde med finanskladder](ui-work-general-journals.md)|  

## <a name="see-also"></a>Se også  
[Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-statement-service.md)  
[Opsætte SEPA-kreditoverførsel](finance-how-to-set-up-sepa-credit-transfer.md)  
[Administrere skyldige beløb](payables-manage-payables.md)   
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)   

