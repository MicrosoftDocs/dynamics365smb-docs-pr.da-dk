---
title: Designoplysninger - Bogføringsprogramstruktur
description: Bogføringsgrænsefladen anvender bogføringsfunktioner til at forberede og indsætte finansposter og momsposter.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# Designoplysninger: Bogføringsprogramstruktur
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
  
## Se også  
 [Designoplysninger: Bogføring af grænsefladestruktur](design-details-posting-interface-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]