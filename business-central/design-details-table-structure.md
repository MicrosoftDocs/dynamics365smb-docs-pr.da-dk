---
title: Designdetaljer – Tabelstruktur | Microsoft Docs
description: Det er vigtigt at forstå tabelstrukturen for at forstå, hvordan dimensionspostlagring og -bogføring er omdesignet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0423314fa123c931e98db37bcc6939b6fbbddf25
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381513"
---
# <a name="design-details-table-structure"></a>Designoplysninger: Tabelstruktur
Det er vigtigt at forstå tabelstrukturen for at forstå, hvordan dimensionsposter lagres og bogføres.  

## <a name="table-480-dimension-set-entry"></a>Tabel 480, Dimensionsgruppepost  
Denne tabel kan ikke ændres. Når data er blevet skrevet i tabellen, kan du ikke slette eller redigere dem.

|Feltnr.|Feltnavn|Datatype|Bemærkning|  
|---------------|----------------|---------------|-------------|  
|1|**Id**|Heltal|> 0,0 er reserveret til den tomme dimensionsgruppe. Refererer til felt 3 i tabel 481.|  
|2|**Dimensionskode**|Kode 20|Tabelrelation til tabel 348.|  
|3|**Dimensionsværdikode**|Kode 20|Tabelrelation til tabel 349.|  
|4|**Dimensionsværdi-id**|Heltal|Refererer til felt 12 i tabel 349. Det er den sekundære nøgle, der bruges, når de transporteres gennem tabellen 481.|  
|5|**Dimensionsnavn**|Tekst 30|CalcField. Opslag i tabel 348.|  
|6|**Dimensionsværdinavn**|Tekst 30|CalcField. Opslag i tabel 349.|  

## <a name="table-481-dimension-set-tree-node"></a>Tabel 481, Trænode for dimensionsgruppe  
Denne tabel kan ikke ændres. Det bruges til at søge efter en dimensionsgruppe. Hvis dimensionssættet ikke findes, oprettes et nyt sæt.  

|Feltnr.|Feltnavn|Datatype|Bemærkning|  
|---------------|----------------|---------------|-------------|  
|1|**Overordnet dimensionsgruppe-id**|Heltal|0 for node på højeste niveau.|  
|2|**Dimensionsværdi-id**|Heltal|Tabelrelation til felt 12 i tabel 349.|  
|3|**Dimensionsgruppe-id**|Heltal|AutoIncrement. Bruges i felt 1 i tabel 480.|  
|4|**I brug**|Boolesk|Falsk, hvis ikke i brug.|  

## <a name="table-482-reclas-dimension-set-buffer"></a>Tabel 482 Ompost. dimensionsgruppebuffer  
Denne tabel bruges, når du ændrer en dimensionsværdikode, for eksempel i en varepost, ved hjælp af siden **Vareomposteringskladde**.  

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

## <a name="transaction-and-budget-tables"></a>Transaktion og budgettabeller  
Ud over de andre dimensionsfelter i tabellen er dette felt også vigtigt:  

|Feltnr.|Feltnavn|Datatype|Bemærkning|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensionsgruppe-id**|Heltal|Refererer til felt 1 i tabel 480.|  

### <a name="table-83-item-journal-line"></a>Tabel 83, Varekladdelinje  
Ud over de andre dimensionsfelter i tabellen er disse felter også vigtige.  

|Feltnr.|Feltnavn|Datatype|Bemærkning|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensionsgruppe-id**|Heltal|Refererer til felt 1 i tabel 480.|  
|481|**Nyt dimensionsgruppe-id**|Heltal|Refererer til felt 1 i tabel 480.|  

### <a name="table-349-dimension-value"></a>Tabel 349, Dimensionsværdi  
Ud over de andre dimensionsfelter i tabellen er disse felter også vigtige.  

|Feltnr.|Feltnavn|Datatype|Bemærkning|  
|---------------|----------------|---------------|-------------|  
|12|**Dimensionsværdi-id**|Heltal|AutoIncrement. Bruges til referencer i tabel 480 og 481.|  

### <a name="tables-that-contain-the-dimension-set-id-field"></a>Tabeller, der indeholder feltet Dimensionsgruppe-id
 Feltet **Dimensionsgruppe-id** (480), der findes i følgende tabeller. For de tabeller, der gemmer bogførte data, indeholder feltet kun en skrivebeskyttet visning af dimensioner, som er markeret som Detailudledning. For de tabeller, der gemmer arbejdsdokumenuer, kan feltet redigeres. De buffertabeller, der bruges internt, behøver ikke redigerbare eller ikke-redigerbare egenskaber.  

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

Felt 480 findes i følgende buffertabeller.  

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
 


[!INCLUDE[footer-include](includes/footer-banner.md)]