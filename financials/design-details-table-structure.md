---
title: "Designdetaljer – Tabelstruktur | Microsoft Docs"
description: "Det er vigtigt at forstå tabelstrukturen for at forstå, hvordan dimensionspostlagring og -bogføring er omdesignet."
services: project-madeira
documentationcenter: 
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a1d7337abcb538ef310ea6f87312934d01540b00
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-table-structure"></a>Designoplysninger: Tabelstruktur
Det er vigtigt at forstå tabelstrukturen for at forstå, hvordan dimensionspostlagring og -bogføring er omdesignet.  

## <a name="new-tables"></a>Nye tabeller  
 Tre nye tabeller er blevet udviklet til at administrere dimensionsgruppeposter.  

### <a name="table-480-dimension-set-entry"></a>Tabel 480 Dimensionsgruppepost  
 Tabel 480 **Dimensionsgruppepost** er en ny tabel. Denne tabel kan ikke ændres. Når data er blevet skrevet i tabellen, kan du ikke slette eller redigere dem. Sletning af data kræver, at du kontrollerer mod alle forekomster af dimensionsgruppe-id'et i hele databasen, herunder partnerløsninger.  

|Feltnr.|Feltnavn|Datatype|Bemærkning|  
|---------------|----------------|---------------|-------------|  
|1|**Id**|Heltal|> 0,0 er reserveret til den tomme dimensionsgruppe. Refererer til felt 3 i tabel 481.|  
|2|**Dimensionskode**|Kode 20|Tabelrelation til tabel 348.|  
|3|**Dimensionsværdikode**|Kode 20|Tabelrelation til tabel 349.|  
|4|**Dimensionsværdi-id**|Heltal|Refererer til felt 12 i tabel 349. Det er den sekundære nøgle, der bruges, når de transporteres gennem tabellen 481.|  
|5|**Dimensionsnavn**|Tekst 30|CalcField. Opslag i tabel 348.|  
|6|**Dimensionsværdinavn**|Tekst 30|CalcField. Opslag i tabel 349.|  

#### <a name="table-481-dimension-set-tree-node"></a>Tabel 481 Trænode for dimensionsgruppe  
 Tabel 481 **Trænode for dimensionsgruppe** er en ny tabel. Denne tabel kan ikke ændres. Det bruges til at søge efter en dimensionsgruppe. Hvis dimensionssættet ikke findes, oprettes et nyt sæt.  

|Feltnr.|Feltnavn|Datatype|Bemærkning|  
|---------------|----------------|---------------|-------------|  
|1|**Overordnet dimensionsgruppe-id**|Heltal|0 for node på højeste niveau.|  
|2|**Dimensionsværdi-id**|Heltal|Tabelrelation til felt 12 i tabel 349.|  
|3|**Dimensionsgruppe-id**|Heltal|AutoIncrement. Bruges i felt 1 i tabel 480.|  
|4|**I brug**|Boolesk|Falsk, hvis ikke i brug.|  

##### <a name="table-482-reclas-dimension-set-buffer"></a>Tabel 482 Ompost. dimensionsgruppebuffer  
 Tabel 482 **Ompost. dimensionsgruppebuffer** er en ny tabel. Tabellen bruges til at redigere et dimensionsgruppe-id. Det er nødvendigt, når du redigerer en dimensionsværdikode og en ny dimensionsværdikode, for eksempel i tabellen **Vareomposteringskladde**.  

|Feltnr.|Feltnavn|Datatype|Bemærkning|  
|---------------|----------------|---------------|-------------|  
|1|**Dimensionskode**|Kode 20|Tabelrelation til tabel 348.|  
|2|**Dimensionsværdikode**|Kode 20|Tabelrelation til tabel 349.|  
|3|**Dimensionsværdi-id**|Heltal|Refererer til felt 12 i tabel 349.|  
|4|**Dimensionsværdikode**|Kode 20|Tabelrelation til tabel 349.|  
|5|**Nyt dimensionsværdi-id**|Heltal|Refererer til felt 12 i tabel 349.|  
|6|**Dimensionsnavn**|Tekst 30|CalcField. Opslag i tabel 348.|  
|7|**Dimensionsværdinavn**|Tekst 30|CalcField. Opslag i tabel 349.|  
|8|**Nyt dimensionsværdinavn**|Tekst 30|CalcField. Opslag i tabel 349.|  

## <a name="modified-tables"></a>Ændrede tabeller  
 Alle transaktions- og budgettabeller er blevet ændret til at administrere dimensionsgruppeposter.  

### <a name="changes-to-transaction-and-budget-tables"></a>Ændringer af transaktion og budgettabeller  
 Et nyt felt er blevet føjet til alle transaktions- og budgettabeller.  

|Feltnr.|Feltnavn|Datatype|Bemærkning|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensionsgruppe-id**|Heltal|Refererer til felt 1 i tabel 480.|  

#### <a name="changes-to-table-83-item-journal-line"></a>Ændringer i tabel 83-varekladdelinje  
 Der er tilføjet to nye felter i tabel 83 **Varekladdelinje**.  

|Feltnr.|Feltnavn|Datatype|Bemærkning|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensionsgruppe-id**|Heltal|Refererer til felt 1 i tabel 480.|  
|481|**Nyt dimensionsgruppe-id**|Heltal|Refererer til felt 1 i tabel 480.|  

##### <a name="changes-to-table-349-dimension-value"></a>Ændringer i tabel 349-dimensionsværdi  
 Et nyt felt er blevet føjet til tabel 349 **Dimensionsværdi**.  

|Feltnr.|Feltnavn|Datatype|Bemærkning|  
|---------------|----------------|---------------|-------------|  
|12|**Dimensionsværdi-id**|Heltal|AutoIncrement. Bruges til referencer i tabel 480 og 481.|  

###### <a name="tables-that-get-new-field-480-dimension-set-id"></a>Tabeller, der får nyt dimensionsgruppe-id i felt 480  
 Et nyt felt, 480 **Dimensionsgruppe-id**, er blevet føjet til følgende tabeller. For de tabeller, der gemmer bogførte data, indeholder feltet kun en skrivebeskyttet visning af dimensioner, som er markeret som Detailudledning. For de tabeller, der gemmer arbejdsdokumenuer, kan feltet redigeres. De buffertabeller, der bruges internt, behøver ikke redigerbare eller ikke-redigerbare egenskaber.  

 Felt 480 kan ikke redigeres i følgende tabeller.  

|Tabelnr.|Tabelnavn|  
|---------------|----------------|  
|17|**Finanspost**|  
|21|**Debitorpost**|  
|25|**Kreditorpost**|  
|32|**Varepost**|  
|110|**Salgsleverancehoved**|  
|111|**Salgsleverancelinje**|  
|112|**Salgsfakturahoved**|  
|113|**Salgsfakturalinje**|  
|114|**Salgskreditnotahoved**|  
|115|**Salgskreditnotalinje**|  
|120|**Købsleverancehoved**|  
|121|**Købsleverancelinje**|  
|122|**Købsfakturahoved**|  
|123|**Købsfakturalinje**|  
|124|**Købskreditnotahoved**|  
|125|**Købskreditnotalinje**|  
|169|**Sagspost**|  
|203|**Ressourcepost**|  
|271|**Bankposter**|  
|281|**Lageropgørelsespost**|  
|297|**Udstedt rykkerhoved**|  
|304|**Udstedt rentenotahoved**|  
|5107|**Salgshovedarkiv**|  
|5108|**Salgslinjearkiv**|  
|5109|**Købshovedarkiv**|  
|5110|**Købslinjearkiv**|  
|5601|**Anlægsfinanspost**|  
|5625|**Reparationspost**|  
|5629|**Forsikringspost**|  
|5744|**Overflytningsleverance (hoved)**|  
|5745|**Overflytningsleverance (linje)**|  
|5746|**Overflytningskvitteringshoved**|  
|5747|**Overflytningskvitteringslinje**|  
|5802|**Værdipost**|  
|5832|**Kapacitetspost**|  
|5907|**Servicepost**|  
|5908|**Serviceordrehoved**|  
|5933|**Bogf.buffer til serviceordre**|  
|5970|**Arkiveret servicekontrakthoved**|  
|5990|**Serviceleverancehoved**|  
|5991|**Serviceleverancelinje**|  
|5992|**Servicefakturahoved**|  
|5993|**Servicefakturalinje**|  
|5994|**Servicekreditnotahoved**|  
|5995|**Servicekreditnotalinje**|  
|6650|**Returvareleverancehoved**|  
|6651|**Returvareleverancelinje**|  
|6660|**Returvaremodt.hoved**|  
|6661|**Returvaremodt.linje**|  

 Felt 480 kan redigeres i følgende tabeller.  

|Tabelnr.|Tabelnavn|  
|---------------|----------------|  
|36|**Salgshoved**|  
|37|**Salgslinje**|  
|38|**Købshoved**|  
|39|**Købslinje**|  
|81|**Finanskladdelinje**|  
|83|**Varekladdelinje**|  
|89|**Styklistekladdelinje**|  
|96|**Finansbudgetpost**|  
|207|**Ressourcekladdelinje**|  
|210|**Sagskladdelinje**|  
|221|**Fordeling**|  
|246|**Disponeringslinje**|  
|295|**Rykkerhoved**|  
|302|**Rentenotahoved**|  
|5405|**Produktionsordre**|  
|5406|**Produktionsordrelinje**|  
|5407|**Produktionsordrekomponent**|  
|5615|**Anlægsfordeling**|  
|5621|**Anlægskladdelinje**|  
|5635|**Forsikringskladdelinje**|  
|5740|**Overflytningshoved**|  
|5741|**Overflytningslinje**|  
|5900|**Serviceordrehoved**|  
|5901|**Serviceartikellinje**|  
|5902|**Servicelinje**|  
|5965|**Servicekontrakthoved**|  
|5997|**Standardservicelinje**|  
|7134|**Varebudgetpost**|  
|99000829|**Planlægning - komponent**|  

 Felt 480 er føjet til følgende buffertabeller.  

|Tabelnr.|Tabelnavn|  
|---------------|----------------|  
|49|**Fakturabogf.buffer**|  
|212|**Sagsbogføringsbuffer**|  
|372|**Betalingsbuffer**|  
|382|**Kunde/leverandør - bogf.buffer**|  
|461|**Buffer for forudbetalingsfakturalinje**|  
|5637|**Anl-finansbogf.buffer**|  
|7136|**Varebudgetbuffer**|  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Dimensionsgruppeposter](design-details-dimension-set-entries.md)   
 [Oversigt over dimensionsgruppeposter](design-details-dimension-set-entries-overview.md)   
 [Designoplysninger: Søgning efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md)   
 [Designoplysninger: Kodeenhed 408 Dimensionsstyring](design-details-codeunit-408-dimension-management.md)   
 [Designoplysninger: Kodeeksempler af ændrede mønstre i Ændringer](design-details-code-examples-of-changed-patterns-in-modifications.md)

