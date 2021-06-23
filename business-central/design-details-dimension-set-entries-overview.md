---
title: Oversigt over dimensionsgruppeposter | Microsoft Docs
description: Dette emne beskriver, hvordan dimensionsgruppeposter gemmes og bogføres i Dynamics 365.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: c6e3df748269e2f40e3acf0a28ce0f6bc48ca944
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215299"
---
# <a name="dimension-set-entries-overview"></a>Oversigt over dimensionsgruppeposter
Dette emne beskriver, hvordan dimensionsgruppeposter gemmes og bogføres i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="dimension-sets"></a>Dimensionsopsætninger  
En dimensionsgruppe er en entydig kombination af dimensionsværdier. Det er gemt som dimensionsgruppeposter i databasen. Hver dimensionsgruppepost repræsenterer en enkelt dimensionsværdi. Dimensionsgruppen er identificeret med en fælles dimensionsgruppe-id, der tildeles til hver dimensionsgruppepost, der hører til dimensionsgruppen.  

Følgende eksempel viser en dimensionsgruppe, der har tre poster for dimensionsgruppe . Dimensionsgruppe er identificeret med en dimensionsgruppe-id, som er 108.  

|Dimensionsgruppe-id|Dimensionskode|Dimensionsværdikode|Dimensionsværdinavn|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|OMRÅDE|70|Nordamerika|  
|108|FORRETNINGSGRUPPE|HOME|Start|  
|108|AFDELING|SALG|Salg|  

## <a name="dimension-set-entries"></a>Dimensionsgruppeposter  
Dimensionsgrupper er gemt i tabellen **Dimensionsgruppepost** som dimensionsgruppeposter med samme dimensionsgruppe-id.  

![Flow af dimensionsgruppeposter](media/dimensionentrynav7.png "Flow af dimensionsgruppeposter")  

Når du opretter en ny kladdelinje, et nyt bilagshoved eller en ny bilagslinje, kan du angive en kombination af dimensionsværdier. I stedet for at eksplicit at gemme hver dimensionsværdi i databasen, tildeles kladdelinjen, bilagshovedet eller bilagslinjen en dimensionsgruppe-id, der angiver dimensionsgruppen.  

Når du redigerer og lukker siden **Rediger dimensionsgruppeposter** udføres en kontrol for at se, om kombinationen af dimensionsværdier findes som en dimensionsgruppe i tabellen. Hvis kombinationen findes i tabellen, tildeles den tilsvarende dimensionsgruppe-id til kladdelinjen, bilagshovedet eller bilagslinjen. Ellers tilføjes en ny dimensionsgruppe til tabellen, og den nye dimensionsgruppe-id knyttes til kladdelinjen, bilagshovedet eller bilagslinjen.

## <a name="codeunit-408-dimension-management"></a>Codeunit 408 Dimensionsstyring
Codeunit 408 Dimensionsstyring er et funktionsbibliotek, der håndterer almindelige opgaver, der er relateret til dimensioner, f.eks. kopiering fra én tabel til en anden eller fra et dokument til en andet.

## <a name="performance-improvement"></a>Forbedring af ydeevne  
Ved at gemme dimensionsgrupper én gang i databasen gemmes der plads i databasen, og den overordnede ydeevne forbedres.  

## <a name="see-also"></a>Se også
[Designoplysninger: Søgning efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md)   
[Designoplysninger: Tabelstruktur](design-details-table-structure.md)   
[Designoplysninger: Dimensionsgruppeposter](design-details-dimension-set-entries.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
