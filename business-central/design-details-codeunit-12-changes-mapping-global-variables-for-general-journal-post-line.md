---
title: Designoplysninger – Codeunit 12-ændringer i tilknytning af globale variabler for bogføringslinje i finanskladde | Microsoft Docs
description: Følgende ændringer er implementeret i denne version af Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: dd0246ada487fd59c51dcef7adb59becdd9ccefd
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "933859"
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
|GLEntryTmp@1015 : TEMPORARY Record 17;|TempGLEntryBuf@1010 : TEMPORARY Record 17;|Omdøbt|  
|TempGLEntryVAT@1016 : TEMPORARY Record 17;|TempGLEntryVAT@1016 : TEMPORARY Record 17;|Uændret|  
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
|FAGLPostBuf@1047 : TEMPORARY Record 5637;||Ændret til lokal|  
|UnrealizedCustLedgEntry@1084 : Record 21;|UnrealizedCustLedgEntry@1084 : Record 21;|Uændret|  
|UnrealizedVendLedgEntry@1085 : Record 25;|UnrealizedVendLedgEntry@1085 : Record 25;|Uændret|  
|GLEntryVATEntryLink@1087 : Record 253;|GLEntryVATEntryLink@1087 : Record 253;|Uændret|  
|TempVATEntry@1088 : TEMPORARY Record 254;|TempVATEntry@1088 : TEMPORARY Record 254;|Uændret|  
|ReversedGLEntryTemp@1089 : TEMPORARY Record 17;||Flyttet til Codeunit17|  
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
||AddCurrencyCode@1117 : Kode[10];|Tilføjet|  
|FiscalYearStartDate@1054 : Date;|FiscalYearStartDate@1011 : Date;|Uændret|  
|NextEntryNo@1055 : Integer;|NextEntryNo@1022 : Integer;|Uændret|  
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
|NextVATEntryNo@1064 : Integer;|NextVATEntryNo@1064 : Integer;|Uændret|  
|FirstNewVATEntryNo@1065 : Integer;|FirstNewVATEntryNo@1065 : Integer;|Uændret|  
|NextTransactionNo@1066 : Integer;|NextTransactionNo@1066 : Integer;|Uændret|  
|NextConnectionNo@1067 : Integer;|NextConnectionNo@1067 : Integer;|Uændret|  
|InsertedTempGLEntryVAT@1068 : Integer;|InsertedTempGLEntryVAT@1027 : Integer;|Uændret|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Uændret|  
|LastLineNo@1070 : Integer;||Slettet|  
|LastDate@1071 : Date;|LastDate@1021 : Date;|Uændret|  
|LastDocType@1072 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|LastDocType@1025 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|Uændret|  
|NextCheckEntryNo@1073 : Integer;|NextCheckEntryNo@1028 : Integer;|Uændret|  
|AddCurrGLEntryVATAmt@1075 : Decimal;|AddCurrGLEntryVATAmt@1017 : Decimal;|Uændret|  
|CurrencyDate@1076 : Date;|CurrencyDate@1020 : Date;|Uændret|  
|CurrencyFactor@1077 : Decimal;|CurrencyFactor@1019 : Decimal;|Uændret|  
|UseCurrFactorOnly@1078 : Boolean;|UseCurrFactorOnly@1078 : Boolean;|Uændret|  
|NonAddCurrCodeOccured@1079 : Boolean;|NonAddCurrCodeOccured@1079 : Boolean;|Uændret|  
|FADimAlreadyChecked@1080 : Boolean;|FADimAlreadyChecked@1080 : Boolean;|Uændret|  
|AllApplied@1081 : Boolean;||Ændret til lokal|  
|OverrideDimErr@1018 : Boolean;|OverrideDimErr@1018 : Boolean;|Uændret|  
|JobLine@1036 : Boolean;|JobLine@1036 : Boolean;|Uændret|  
|Prepayment@1037 : Boolean;||Slettet|  
|CheckUnrealizedCust@1082 : Boolean;|CheckUnrealizedCust@1082 : Boolean;|Uændret|  
|CheckUnrealizedVend@1083 : Boolean;|CheckUnrealizedVend@1083 : Boolean;|Uændret|  
|GLEntryNo@1090 : Integer;|GLEntryNo@1026 : Integer;|Uændret|  
||GLSetupRead@1015 : Boolean;|Tilføjet|  
||AmountRoundingPrecision@1012 : Decimal;|Tilføjet|  
||CrCardTransactionEntryNo@1013 : Integer;|Tilføjet|  

## <a name="see-also"></a>Se også  
 [Designoplysninger – Codeunit 12-ændringer i procedurer for bogføring af finanskladder](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)
