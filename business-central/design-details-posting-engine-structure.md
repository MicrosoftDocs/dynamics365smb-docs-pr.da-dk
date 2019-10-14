---
title: Designdetaljer – Bogføringsprogramstruktur | Microsoft Docs
description: Bogføringsgrænsefladen og visse andre funktioner i codeunit 12 bruger bogføringsfunktioner til at forberede og indsætte finansposter og momsposter. Bogføringsprogrammet er også ansvarlig for oprettelse af finansregister.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b4bc639675591bb91ad2fa4e56f4e3ed88fed975
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303072"
---
# <a name="design-details-posting-engine-structure"></a>Designoplysninger: Bogføringsprogramstruktur
Bogføringsgrænsefladen og visse andre funktioner i codeunit 12 bruger bogføringsfunktioner til at forberede og indsætte finansposter og momsposter. Bogføringsprogrammet er også ansvarlig for oprettelse af finansregister.  
  
 Funktionerne i følgende tabel giver en standardramme til design af bogføringsprocedurer (f.eks. Code, CustPostApplyCustledgEntry, VendPostApplyVendLedgEntry, UnapplyCustLedgEntry, UnapplyVendLedgEntry og Reverse) og udelt adgang til tabel 17, Finanspost.  
  
|Rutine|Beskrivelse|  
|-------------|---------------------------------------|  
|StartPosting|Initialiserer bufferen TempGLEntryBuf for bogføring, låser finanspost- og momsposttabeller og initialiserer regnskabsperiode, finansjournal og valutakurs. Bør kun kaldes én gang, så NextEntryNo er 0.|  
|ContinuePosting|Kontrollerer og bogfører urealiseret moms for tidligere transaktionsforøgelse NextTransactionNo og forbereder bogføring af næste linje.|  
|FinishPosting|Udfører bogføring ved at indsætte finansposter fra midlertidig buffer i databasetabellen. Bruges altid sammen med StartPosting. Kontrollerer for uoverensstemmelser.|  
|InitGLEntry|Bruges til at initialisere ny finanspost for finanskladdelinje. Returnerer GLEntry som parameter.|  
|InitGLEntryVAT|Samme som InitGLEntry, men tildeler også modkonto og SummarizeVAT.|  
|InitGLEntryVATCopy|Svarer til InitGLEntryVAT, men kopieret også bogføringsgruppedata fra momspost før SummarizeVAT.|  
|InsertGLEntry|Den eneste funktion, der indsætter finansposten i tabellen med globale TempGLEntryBuf. Brug altid denne funktion til Indsættelse.|  
|CreateGLEntry|Udfører en InitGLEntry, tildeler ekstra valutabeløb og udfører derefter InsertGLEntry. Erstatter flere kodelinjer med et enkelt funktionskald.|  
|CreateGLEntryBalAcc|Samme som CreateGLEntry, men tildeler også Modkontotype og Modkonto.|  
|CreateGLEntryVAT|Samme som CreateGLEntry, men med yderligere behandling for bogføringsgrupper og lagring til den midlertidige momsbuffer:<br /><br /> `GLEntry.CopyPostingGroupsFromDtldCVBuf(DtldCVLedgEntryBuf,GenJnlLine."Gen. Posting Type");`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryVATCollectAdj|Samme som CreateGLEntry, men med yderligere samling af justeringer og lagring til den midlertidige momsbuffer:<br /><br /> `CollectAdjustment(AdjAmount,GLEntry.Amount,GLEntry."Additional-Currency Amount",OriginalDateSet);`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryFromVATEntry|Samme som CreateGLEntry, men kopierer også bogføringsgrupper fra momspost.|  
  
## <a name="see-also"></a>Se også  
 [Designoplysninger: Bogføring af grænsefladestruktur](design-details-posting-interface-structure.md)