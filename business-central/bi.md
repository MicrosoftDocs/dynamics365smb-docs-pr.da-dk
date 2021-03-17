---
title: Business Intelligence| Microsoft Docs
description: Du kan registrere og analysere forretningsdata, som f.eks. salgstal, køb, driftsudgifter, medarbejderlønninger og budgetter, som kan være værdifulde oplysninger for business intelligence eller beslutningstagere.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 245e77cb34f3b7b1a8f02c17f17ebd26269d3691
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389145"
---
# <a name="business-intelligence"></a>Business Intelligence
Firmaer opfanger en stor mængde data under de daglige aktiviteter. Disse data, som f.eks. afspejler organisationens salgstal, køb, driftsudgifter, medarbejderlønninger og budgetter, kan for beslutningstagere blive værdifulde oplysninger eller "business intelligence", dvs. forretningsindsigt. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en række funktioner, som kan være nyttige, når du skal indsamle, analysere og dele virksomhedens data.

Dimensionsfunktionerne spiller en vigtig rolle i business intelligence. En dimension er data, som du kan føje til en post som en slags markør. Disse data bruges til at gruppere poster med ens karakteristika, f.eks. debitorer, regioner, produkter og sælger, og disse grupper kan nemt hentes frem til analyse. Du kan blandt andre bruge dimensioner til at definere analysevisninger, og når du opretter kontoskemaer til rapportering. Du kan finde flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

> [!TIP]
> For hurtigt at analysere transaktionsdata efter dimensioner kan du filtrere totaler i kontoplanen og poster på alle sider af typen **Poster** efter dimensioner. Kig efter handlingen **Angiv dimensionsfilter**.  

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

| Hvis du vil | Se |
| --- | --- |
|Få vist budgetter, og faktiske beløb sammenlignet med budgetterede beløb for alle konti og for flere perioder.|[Analysere faktiske beløb sammenlignet med budgetterede beløb](bi-how-analyze-actual-versus-budget.md)|
|Oprette nye kontoskemaer for at definere regnskaber til rapportering eller visning som diagrammer.|[Forberede Financial Reporting med kontoskemaer og kontokategorier](bi-how-work-account-schedule.md)|
|Analyser din finansielle ydeevne ved at konfigurere KPI'er baseret på kontoplaner, som du derefter publicerer som webtjenester. De publicerede kontoskema-KPI'er kan ses på et websted eller importeres i Microsoft Excel ved hjælp af OData-webtjenester.|[Konfigurere og udgive KPI-webtjenester, der er baseret på kontoskemaer](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md)|
|Oprette analysevisninger for at analysere data vha. dimensioner.|[Analysere data efter dimensioner](bi-how-analyze-data-dimension.md)|
|Oprette nye analyserapporter for salg, køb og lager og oprette analyseskabeloner.|[Oprette analyserapporter](bi-how-create-analysis-views-reports.md)|
|Aktivere global finansiel rapportering til internationale revisionsfirmaer ved eXtensible Business Reporting Language.|[Oprette rapporter med XBRL](bi-create-reports-with-xbrl.md)|
|Rediger formål for adgang til databaser på rapporter, sider af typen API og forespørgsler for at reducere belastningen og forbedre ydeevnen.|[Administrere formål med adgang til database](admin-data-access-intent.md)|

## <a name="see-also"></a>Se også
[Finans](finance.md)    
[Bruge Business Central som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Afslutte regnskabsperioder](year-close-years-periods.md)  
[Importere data fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]