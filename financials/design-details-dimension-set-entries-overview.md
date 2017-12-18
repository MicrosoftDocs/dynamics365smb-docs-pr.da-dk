---
title: Oversigt over dimensionsgruppeposter | Microsoft Docs
description: "Dette emne beskriver, hvordan dimensionsgruppeposter gemmes og bogføres i [!INCLUDE[d365fin](includes/d365fin_md.md)]."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 53c85ecbb42db92e95921203d24781bcb82f942d
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="dimension-set-entries-overview"></a>Oversigt over dimensionsgruppeposter
Dette emne beskriver, hvordan dimensionsgruppeposter gemmes og bogføres i [!INCLUDE[d365fin](includes/d365fin_md.md)].  
  
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
  
![Oversigt over dimensionspost](media/dimensionentrynav7.png "DimensionEntryNAV7")  
  
Når du opretter en ny kladdelinje, et nyt bilagshoved eller en ny bilagslinje, kan du angive en kombination af dimensionsværdier. I stedet for at eksplicit at gemme hver dimensionsværdi i databasen, tildeles kladdelinjen, bilagshovedet eller bilagslinjen en dimensionsgruppe-id, der angiver dimensionsgruppen.  
  
Når du redigerer og lukker vinduet **Rediger dimensionsgruppeposter** udføres en kontrol for at se, om kombinationen af dimensionsværdier findes som en dimensionsgruppe i tabellen. Hvis kombinationen findes i tabellen, tildeles den tilsvarende dimensionsgruppe-id til kladdelinjen, bilagshovedet eller bilagslinjen. Ellers tilføjes en ny dimensionsgruppe til tabellen, og den nye dimensionsgruppe-id knyttes til kladdelinjen, bilagshovedet eller bilagslinjen.  
  
## <a name="performance-improvement"></a>Forbedring af ydeevne  
Ved at gemme dimensionsgrupper én gang i databasen, gemmes der plads i databasen, og den overordnede ydeevne forbedres.  
  
## <a name="see-also"></a>Se også  
[Designoplysninger: Søgning efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md)   
[Designoplysninger: Tabelstruktur](design-details-table-structure.md)   
[Designoplysninger: Kodeenhed 408 Dimensionsstyring](design-details-codeunit-408-dimension-management.md)   
[Designoplysninger: Kodeeksempler af ændrede mønstre i Ændringer](design-details-code-examples-of-changed-patterns-in-modifications.md)   
[Designoplysninger: Dimensionsgruppeposter](design-details-dimension-set-entries.md)   

