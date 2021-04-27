---
title: Ændringer i procedurer for bogføring af finanskladder i Codeunit 12.
description: I tidligere versioner blev codeunit 12 ændret for at forbedre ydeevnen ved bogføring fra finanskladden. Få mere at vide om ændringerne i bogføringsprocedurerne i denne artikel.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0c50f9cb8f596c8f4569cfc5d595544cec2c8bef
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788354"
---
# <a name="historical-changes-to-codeunit-12-changes-in-general-journal-post-procedures"></a>Historiske ændringer til Codeunit 12: Ændringer i procedurer for bogføring af finanskladder

Følgende ændringer er implementeret i denne version af [!INCLUDE [navnow_md](includes/navnow_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Bemærkning**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GetGLReg|GetGLReg|Opdateret|  
|RunWithCheck|RunWithCheck|Opdateret|  
|RunWithoutCheck|RunWithoutCheck|Opdateret|  
|Code|Code|Opdateret|  
||PostGenJnlLine|Tilføjet|  
||InitAmounts|Tilføjet|  
||InitLastDocDate|Tilføjet|  
|InitVAT|InitVAT|Opdateret|  
|PostVAT|PostVAT|Opdateret|  
|InsertVAT|InsertVAT|Opdateret|  
|SummarizeVAT|SummarizeVAT|Opdateret|  
|InsertSummarizedVAT|InsertSummarizedVAT|Opdateret|  
|PostGLAcc|PostGLAcc|Opdateret|  
|PostCust|PostCust|Opdateret|  
|PostVend|PostVend|Opdateret|  
|PostBankAcc|PostBankAcc|Opdateret|  
|PostFixedAsset|PostFixedAsset|Opdateret|  
|PostICPartner|PostICPartner|Opdateret|  
|InitCodeUnit|StartPosting|Opdateret|  
||ContinuePosting|Tilføjet|  
|FinishCodeunit|FinishPosting|Opdateret|  
||PostUnrealizedVAT|Tilføjet|  
||CheckPostUnrealizedVAT|Tilføjet|  
||ExchangeAccounts|Tilføjet|  
|InitGLEntry|InitGLEntry|Opdateret|  
||InitGLEntryVAT|Tilføjet|  
||InitGLEntryVATCopy|Tilføjet|  
|InsertGLEntry|InsertGLEntry|Opdateret|  
||CreateGLEntry|Tilføjet|  
||CreateGLEntryBalAcc|Tilføjet|  
||CreateGLEntryVAT|Tilføjet|  
||CreateGLEntryVATCollectAdj|Tilføjet|  
||CreateGLEntryFromVATEntry|Tilføjet|  
||UpdateCheckAmounts|Tilføjet|  
|ApplyCustLedgEntry|ApplyCustLedgEntry|Opdateret|  
||CalcPmtDiscPossible|Tilføjet|  
||CalcPmtTolerancePossible|Tilføjet|  
|CalcPmtTolerance|CalcPmtTolerance|Opdateret|  
|CalcPmtDisc|CalcPmtDisc|Opdateret|  
|CalcPmtDiscIfAdjVAT|CalcPmtDiscIfAdjVAT|Opdateret|  
|CalcPmtDiscTolerance|CalcPmtDiscTolerance|Opdateret|  
||CalcPmtDiscVATBases|Tilføjet|  
||CalcPmtDiscVATAmounts|Tilføjet|  
||InsertPmtDiscVATForVATEntry|Tilføjet|  
||InsertPmtDiscVATForGLEntry|Tilføjet|  
|CalcCurrencyApplnRounding|CalcCurrencyApplnRounding|Opdateret|  
|FindAmtForAppln|FindAmtForAppln|Opdateret|  
|CalcCurrencyUnrealizedGainLoss|CalcCurrencyUnrealizedGainLoss|Opdateret|  
|CalcCurrencyRealizedGainLoss|CalcCurrencyRealizedGainLoss|Opdateret|  
|CalcApplication|CalcApplication|Opdateret|  
|CalcRemainingPmtDisc|CalcRemainingPmtDisc|Flyttet til Codeunit 426 Styring af betalingstolerance|  
|CalcAmtLCYAdjustment|CalcAmtLCYAdjustment|Tilføjet|  
|InitNewCVLedgEntry|InitFromGenJnlLine|Flyttet til tabel 383 Detalj. kunde/lev.bogf.buffer|  
|InitOldCVLedgEntry|CopyFromCVLedgEntryBuf|Flyttet til tabel 383 Detalj. kunde/lev.bogf.buffer|  
|InsertDtldCVLedgEntry|InsertDtldCVLedgEntry|Flyttet til tabel 383 Detalj. kunde/lev.bogf.buffer|  
||InitBankAccLedgEntry|Tilføjet|  
||InitCheckLedgEntry|Tilføjet|  
||InitCustLedgEntry|Tilføjet|  
||InitVendLedgEntry|Tilføjet|  
||InsertDtldCustLedgEntry|Tilføjet|  
||InsertDtldVendLedgEntry|Tilføjet|  
|CustUnrealizedVAT|CustUnrealizedVAT|Opdateret|  
|CustPostApplyCustLedgEntry|CustPostApplyCustLedgEntry|Opdateret|  
||PrepareTempCustLedgEntry|Tilføjet|  
|UnapplyCustLedgEntry|UnapplyCustLedgEntry|Opdateret|  
|TransferCustLedgEntry|CopyFromGenJnlLine|Flyttet til tabel 21 Debitorpost|  
|PostDtldCustLedgEntries|PostDtldCustLedgEntries|Opdateret|  
||PostDtldCustLedgEntry|Tilføjet|  
||PostDtldCustLedgEntryUnapply|Tilføjet|  
||GetDtldCustLedgEntryAccNo|Tilføjet|  
|ZeroTransNoDtldCustLedgEntries|SetZeroTransNo|Flyttet til tabel 379 Detaljeret debitorpost|  
|AutoEntrForDtldCustLedgEntries||Omstruktureret til PostDtldCustLedgEntryUnapply|  
|CustUpdateDebitCredit|UpdateDebitCredit|Flyttet til tabel 379 Detaljeret debitorpost|  
|ApplyVendLedgEntry|ApplyVendLedgEntry|Opdateret|  
||PrepareTempVendLedgEntry|Tilføjet|  
|VendPostApplyVendLedgEntry|VendPostApplyVendLedgEntry|Opdateret|  
|UnapplyVendLedgEntry|UnapplyVendLedgEntry|Opdateret|  
|TransferVendLedgEntry|CopyFromGenJnlLine|Flyttet til tabel 25 Kreditorpost|  
|PostDtldVendLedgEntries|PostDtldVendLedgEntries|Opdateret|  
||PostDtldVendLedgEntry|Tilføjet|  
||PostDtldVendLedgEntryUnapply|Tilføjet|  
||GetDtldVendLedgEntryAccNo|Tilføjet|  
||PostDtldCVLedgEntry|Tilføjet|  
||PostDtldCustVATAdjustment|Tilføjet|  
||PostDtldVendVATAdjustment|Tilføjet|  
|ZeroTransNoDtldVendLedgEntries|SetZeroTransNo|Flyttet til tabel 380 Detaljeret kreditorpost|  
|AutoEntrForDtldVendLedgEntries||Omstruktureret til PostDtldVendLedgEntryUnapply|  
|VendUpdateDebitCredit|UpdateDebitCredit|Flyttet til tabel 380 Detaljeret kreditorpost|  
|VendUnrealizedVAT|VendUnrealizedVAT|Opdateret|  
||PostUnrealVATEntry|Tilføjet|  
||PostApply|Tilføjet|  
|PostUnrealVATByUnapply|PostUnrealVATByUnapply|Opdateret|  
||PostUnapply|Tilføjet|  
||InsertDtldCustLedgEntryUnapply|Tilføjet|  
||InsertDtldVendLedgEntryUnapply|Tilføjet|  
||InsertTempVATEntry|Tilføjet|  
||ProcessTempVATEntry|Tilføjet|  
||UpdateCustLedgEntry|Tilføjet|  
||UpdateVendLedgEntry|Tilføjet|  
|UpdateCalcInterest|UpdateCalcInterest|Opdateret|  
|UpdateCalcInterest2|UpdateCalcInterest2|Opdateret|  
|GLCalcAddCurrency|GLCalcAddCurrency|Opdateret|  
|HandleAddCurrResidualGLEntry|HandleAddCurrResidualGLEntry|Opdateret|  
|CalcLCYToAddCurr|CalcLCYToAddCurr|Opdateret|  
|CalcAddCurrFactor||Slettet|  
|GetCurrencyExchRate|GetCurrencyExchRate|Opdateret|  
|ExchAmount|ExchangeAmount|Flyttet til tabel 330 Valutakurs|  
|ExchangeAmtLCYToFCY2|ExchangeAmtLCYToFCY2|Opdateret|  
|CalcAddCurrForUnapplication|CalcAddCurrForUnapplication|Opdateret|  
|CheckNonAddCurrCodeOccurred|CheckNonAddCurrCodeOccurred|Opdateret|  
|CheckCalcPmtDisc||Flyttet til Codeunit 426 Styring af betalingstolerance|  
|CheckCalcPmtDiscCVCust||Flyttet til Codeunit 426 Styring af betalingstolerance|  
|CheckCalcPmtDiscCust||Flyttet til Codeunit 426 Styring af betalingstolerance|  
|CheckCalcPmtDiscGenJnlCust||Flyttet til Codeunit 426 Styring af betalingstolerance|  
|CheckCalcPmtDiscCVVend||Flyttet til Codeunit 426 Styring af betalingstolerance|  
|CheckCalcPmtDiscVend||Flyttet til Codeunit 426 Styring af betalingstolerance|  
|CheckCalcPmtDiscGenJnlVend||Flyttet til Codeunit 426 Styring af betalingstolerance|  
|Reverse|Reverse|Flyttet til Codeunit 17 Finanskladde - Tilbagefør|  
|ReverseCustLedgEntry|ReverseCustLedgEntry|Flyttet til Codeunit 17 Finanskladde - Tilbagefør|  
|ReverseVendLedgEntry|ReverseVendLedgEntry|Flyttet til Codeunit 17 Finanskladde - Tilbagefør|  
|ReverseBankAccLedgEntry|ReverseBankAccLedgEntry|Flyttet til Codeunit 17 Finanskladde - Tilbagefør|  
|ReverseVAT|ReverseVAT|Flyttet til Codeunit 17 Finanskladde - Tilbagefør|  
|SetReversalDescription|SetReversalDescription|Flyttet til Codeunit 17 Finanskladde - Tilbagefør|  
|ApplyCustLedgEntryByReversal|ApplyCustLedgEntryByReversal|Flyttet til Codeunit 17 Finanskladde - Tilbagefør|  
|ApplyVendLedgEntryByReversal|ApplyVendLedgEntryByReversal|Flyttet til Codeunit 17 Finanskladde - Tilbagefør|  
|PostPmtDiscountVATByUnapply|PostPmtDiscountVATByUnapply|Flyttet til Codeunit 17 Finanskladde - Tilbagefør|  
||CheckDimComb|Tilføjet i Codeunit 17 Finanskladde - Tilbagefør|  
||CopyCustLedgEntry|Tilføjet i Codeunit 17 Finanskladde - Tilbagefør|  
||CopyVendLedgEntry|Tilføjet i Codeunit 17 Finanskladde - Tilbagefør|  
||CopyBankAccLedgEntry|Tilføjet i Codeunit 17 Finanskladde - Tilbagefør|  
|HandlDtlAddjustment|HandleDtldAdjustment|Opdateret|  
|CollectAddjustment|CollectAdjustment|Opdateret|  
|SetOverDimErr|SetOverDimErr|Opdateret|  
|PostJob|PostJob|Opdateret|  
|InsertVATEntriesFromTemp|InsertVATEntriesFromTemp|Opdateret|  
|CaptureOrRefundCreditCardPmnt|CaptureOrRefundCreditCardPmnt|Opdateret|  
|UpdateDOPaymentTransactEntry|UpdateDOPaymentTransactEntry|Opdateret|  
|ABSMin|ABSMin|Opdateret|  
|GetApplnRoundPrecision|GetApplnRoundPrecision|Opdateret|  
|CheckDimValueForDisposal|CheckDimValueForDisposal|Opdateret|  
|CalculateCurrentBalance|CalculateCurrentBalance|Opdateret|  
|IncludeVATAmount||Flyttet til tabel 81 kladdelinje|  
|CalcVATAmountFromVATEntry|CalcVATAmountFromVATEntry|Opdateret|  
||TotalVATAmountOnJnlLines|Tilføjet|  
||SetGLRegReverse|Tilføjet|  
||GetGLSetup|Tilføjet|  
||ReadGLSetup|Tilføjet|  
||CheckSalesExtDocNo|Tilføjet|  
||CheckPurchExtDocNo|Tilføjet|  
||CheckGLAccDimError|Tilføjet|  
||GetCurrency|Tilføjet|  
||PostDtldAdjustment|Tilføjet|  
||GetNextEntryNo|Tilføjet|  
||GetNextTransactionNo|Tilføjet|  
||GetNextVATEntryNo|Tilføjet|  
||IncrNextVATEntryNo|Tilføjet|  
||IsNotPayment|Tilføjet|  
||IsTempGLEntryBufEmpty|Tilføjet|  
||IsVATAdjustment|Tilføjet|  
||IsVATExcluded|Tilføjet|  
||UpdateDimensions|Tilføjet|  
||UpdateDimensionsFromCustLedgEntry|Tilføjet|  
||UpdateDimensionsFromVendLedgEntry|Tilføjet|  
||UpdateTotalAmounts|Tilføjet|  
||CreateGLEntriesForTotalAmounts|Tilføjet|  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Ændringer i Codeunit 12: Kobling af globale variabler for bogføringslinje i finanskladde](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]