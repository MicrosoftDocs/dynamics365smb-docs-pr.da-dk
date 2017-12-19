---
title: "Designoplysninger – Codeunit 12-ændringer i tilknytning af globale variabler for bogføringslinje i finanskladde | Microsoft Docs"
description: "Følgende ændringer er implementeret i denne version af Dynamics 365."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 253043c8f3b2a15f2ed6d0990192977772e98b87
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="codeunit-12-changes-mapping-global-variables-for-general-journal-post-line"></a>Ændringer i Codeunit 12: Kobling af globale variabler for bogføringslinje i finanskladde
Følgende ændringer er implementeret i denne version af [!INCLUDE[d365fin](includes/d365fin_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Bemærkning**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Record 98;|GLSetup@1009 : Record 98;|Uændret|  
|SalesSetup@1010 : Record 311;||Ændret til lokal|  
|PurchSetup@1011 : Record 312;||Ændret til lokal|  
|AccountingPeriod@1012 : Record 50;||Ændret til lokal|  
|GLAcc@1013 : Record 15;||Ændret til lokal|  
|GLEntry@1014 : Record 17;|GlobalGLEntry@1014 : Record 17;|Omdøbt|  
|GLEntryTmp@1015 : MIDLERTIDIG record 17;|TempGLEntryBuf@1010 : MIDLERTIDIG record 17;|Omdøbt|  
|TempGLEntryVAT@1016 : MIDLERTIDIG record 17;|TempGLEntryVAT@1016 : MIDLERTIDIG record 17;|Uændret|  
|OrigGLEntry@1017 : Record 17;||Slettet|  
|VATPostingSetup@1019 : Record 325;||Ændret til lokal|  
|Cust@1020 : Record 18;||Ændret til lokal|  
|Vend@1021 : Record 23;||Ændret til lokal|  
|GenJnlLine@1022 : Record 81;||Ændret til lokal|  
|GLReg@1029 : Record 45;|GLReg@1029 : Record 45;|Uændret|  
|CustPostingGr@1030 : Record 92;||Ændret til lokal|  
|VendPostingGr@1031 : Record 93;||Ændret til lokal|  
|Currency@1032 : Record 4;||Ændret til lokal|  
|AddCurrency@1033 : Record 4;|AddCurrency@1033 : Record 4;|Uændret|  
|ApplnCurrency@1034 : Record 4;||Ændret til lokal|  
|CurrExchRate@1035 : Record 330;|CurrExchRate@1035 : Record 330;|Uændret|  
|VATEntry@1038 : Record 254;|VATEntry@1038 : Record 254;|Uændret|  
|BankAcc@1039 : Record 270;||Ændret til lokal|  
|BankAccLedgEntry@1040 : Record 271;||Ændret til lokal|  
|CheckLedgEntry@1041 : Record 272;||Ændret til lokal|  
|CheckLedgEntry2@1042 : Record 272;||Ændret til lokal|  
|BankAccPostingGr@1043 : Record 277;||Ændret til lokal|  
|GenJnlTemplate@1044 : Record 80;||Ændret til lokal|  
|TaxJurisdiction@1045 : Record 320;||Ændret til lokal|  
|TaxDetail@1046 : Record 322;|TaxDetail@1046 : Record 322;|Uændret|  
|FAGLPostBuf@1047 : MIDLERTIDIG record 5637;||Ændret til lokal|  
|UnrealizedCustLedgEntry@1084 : Record 21;|UnrealizedCustLedgEntry@1084 : Record 21;|Uændret|  
|UnrealizedVendLedgEntry@1085 : Record 25;|UnrealizedVendLedgEntry@1085 : Record 25;|Uændret|  
|GLEntryVATEntryLink@1087 : Record 253;|GLEntryVATEntryLink@1087 : Record 253;|Uændret|  
|TempVATEntry@1088 : MIDLERTIDIG record 254;|TempVATEntry@1088 : MIDLERTIDIG record 254;|Uændret|  
|ReversedGLEntryTemp@1089 : MIDLERTIDIG record 17;||Flyttet til Codeunit17|  
|CostAccSetup@1092 : Record 1108;||Ændret til lokal|  
|GenJnlCheckLine@1048 : Codeunit 11;|GenJnlCheckLine@1001 : Codeunit 11;|Uændret|  
|ExchAccGLJnlLine@1049 : Codeunit 366;||Ændret til lokal|  
|FAJnlPostLine@1050 : Codeunit 5632;||Ændret til lokal|  
|SalesTaxCalculate@1051 : Codeunit 398;||Ændret til lokal|  
|GenJnlApply@1052 : Codeunit 225;||Ændret til lokal|  
|DimMgt@1053 : Codeunit 408;||Ændret til lokal|  
|JobPostLine@1028 : Codeunit 1001;||Ændret til lokal|  
|TransferGlEntriesToCA@1091 : Codeunit 1105;||Ændret til lokal|  
||PaymentToleranceMgt@1002 : Codeunit 426;|Tilføjet|  
||AddCurrencyCode@1117 : Code[10];|Tilføjet|  
|FiscalYearStartDate@1054 : Dato;|FiscalYearStartDate@1011 : Dato;|Uændret|  
|NextEntryNo@1055 : Heltal;|NextEntryNo@1022 : Heltal;|Uændret|  
|BalanceCheckAmount@1056 : Decimal;|BalanceCheckAmount@1056 : Decimal;|Uændret|  
|BalanceCheckAmount2@1057 : Decimal;|BalanceCheckAmount2@1057 : Decimal;|Uændret|  
|BalanceCheckAddCurrAmount@1058 : Decimal;|BalanceCheckAddCurrAmount@1058 : Decimal;|Uændret|  
|BalanceCheckAddCurrAmount2@1059 : Decimal;|BalanceCheckAddCurrAmount2@1059 : Decimal;|Uændret|  
|CurrentBalance@1060 : Decimal;|CurrentBalance@1060 : Decimal;|Uændret|  
|SalesTaxBaseAmount@1061 : Decimal;||Ændret til lokal|  
|TotalAddCurrAmount@1062 : Decimal;|TotalAddCurrAmount@1062 : Decimal;|Uændret|  
|TotalAmount@1063 : Decimal;|TotalAmount@1063 : Decimal;|Uændret|  
|UnrealizedRemainingAmountCust@1086 : Decimal;|UnrealizedRemainingAmountCust@1086 : Decimal;|Uændret|  
|UnrealizedRemainingAmountVend@1074 : Decimal;|UnrealizedRemainingAmountVend@1074 : Decimal;|Uændret|  
|NextVATEntryNo@1064 : Heltal;|NextVATEntryNo@1064 : Heltal;|Uændret|  
|FirstNewVATEntryNo@1065 : Heltal;|FirstNewVATEntryNo@1065 : Heltal;|Uændret|  
|NextTransactionNo@1066 : Heltal;|NextTransactionNo@1066 : Heltal;|Uændret|  
|NextConnectionNo@1067 : Heltal;|NextConnectionNo@1067 : Heltal;|Uændret|  
|InsertedTempGLEntryVAT@1068 : Heltal;|InsertedTempGLEntryVAT@1027 : Heltal;|Uændret|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Uændret|  
|LastLineNo@1070 : Heltal;||Slettet|  
|LastDate@1071 : Dato;|LastDate@1021 : Dato;|Uændret|  
|LastDocType@1072 : ' ,Betaling,Faktura,Kreditnota,Rentenota,Rykker';|LastDocType@1025 : ' ,Betaling,Faktura,Kreditnota,Rentenota,Rykker';|Uændret|  
|NextCheckEntryNo@1073 : Heltal;|NextCheckEntryNo@1028 : Heltal;|Uændret|  
|AddCurrGLEntryVATAmt@1075 : Decimal;|AddCurrGLEntryVATAmt@1017 : Decimal;|Uændret|  
|CurrencyDate@1076 : Dato;|CurrencyDate@1020 : Dato;|Uændret|  
|CurrencyFactor@1077 : Decimal;|CurrencyFactor@1019 : Decimal;|Uændret|  
|UseCurrFactorOnly@1078 : Boolesk;|UseCurrFactorOnly@1078 : Boolesk;|Uændret|  
|NonAddCurrCodeOccured@1079 : Boolesk;|NonAddCurrCodeOccured@1079 : Boolesk;|Uændret|  
|FADimAlreadyChecked@1080 : Boolesk;|FADimAlreadyChecked@1080 : Boolesk;|Uændret|  
|AllApplied@1081 : Boolesk;||Ændret til lokal|  
|OverrideDimErr@1018 : Boolesk;|OverrideDimErr@1018 : Boolesk;|Uændret|  
|JobLine@1036 : Boolesk;|JobLine@1036 : Boolesk;|Uændret|  
|Prepayment@1037 : Boolesk;||Slettet|  
|CheckUnrealizedCust@1082 : Boolesk;|CheckUnrealizedCust@1082 : Boolesk;|Uændret|  
|CheckUnrealizedVend@1083 : Boolesk;|CheckUnrealizedVend@1083 : Boolesk;|Uændret|  
|GLEntryNo@1090 : Heltal;|GLEntryNo@1026 : Heltal;|Uændret|  
||GLSetupRead@1015 : Boolesk;|Tilføjet|  
||AmountRoundingPrecision@1012 : Decimal;|Tilføjet|  
||CrCardTransactionEntryNo@1013 : Heltal;|Tilføjet|  

## <a name="see-also"></a>Se også  
 [Designoplysninger – Codeunit 12-ændringer i procedurer for bogføring af finanskladder | Microsoft Docs](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)

