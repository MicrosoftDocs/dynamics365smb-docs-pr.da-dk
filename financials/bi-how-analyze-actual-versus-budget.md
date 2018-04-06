---
title: Analysere faktisk kontra budget | Microsoft Docs
description: "Bruges til at analysere faktiske beløb sammenlignet med budgetterede beløb."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 1da2e94fa64d1daa3304b5266d54152563cfa283
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Analysere faktiske beløb sammenlignet med budgetterede beløb
Som et led i indsamling, analyse og deling af virksomhedens data kan du få vist faktiske beløb sammenlignet med budgetterede beløb for alle konti og for flere perioder.

Hvis du vil analysere budgetterede beløb, skal du først oprette finansbudgetter. Du kan finde flere oplysninger i [Oprette finansbudgetter](finance-how-create-budgets.md).

## <a name="to-view-a-gl-budget"></a>Sådan får du vist et finansbudget
budget med dimensioner kan du filtrere poster og få vist et bestemt budget.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finansbudgetter**, og vælg derefter det relaterede link.
2. I vinduet **Finansbudgetter** skal du åbne det budget, du ønsker at få vist.  
3. Øverst i vinduet skal du udfylde felterne efter behov for at definere, hvad der vises. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Hvis du har valgt **Periode** i feltet **Vis som linjer** eller feltet **Vis som kolonner**, skal du udfylde feltet **Vis efter**. Hvis du ikke har valgt **Periode** i feltet **Vis som linjer** eller **Vis som kolonner**, skal du angive den relevante periode i feltet **Datofilter**.  

> [!NOTE]  
>   Kun poster i finansbudgettet med de filterkoder, du har angivet i oversigtspanelet **Filtre**, medtages i beregningen. Budgetposter med andre filterkoder eller uden filterkoder medtages ikke. Så længe filtret bliver i vinduet, vises budgettet kun med de budgetposter, der har disse filterkoder.  

> [!TIP]  
>   Hvis du vil ændre budgettet, kan du redigere budgetposterne. Vælg et beløb for at få vist de underliggende finansbudgetposter.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Sådan får du vist aktuelle og budgetterede beløb for alle konti  
Du kan få vist finansbudgetter og sammenligne dem med faktiske tal i flere områder af [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.  
2. I vinduet **Kontoplan** skal du vælge handlingen **Finans - saldi/budget**.
3. Øverst i vinduet skal du udfylde felterne efter behov for at definere, hvad der vises.  
4. Vælg feltet, hvis du vil se en specifikation, der udgør det viste beløb.  

> [!NOTE]  
>   Det filter, du har angivet i vinduets hoved, anvendes til både finans- og budgetposter.

Den venstre kolonne indeholder kontoplanen. Af de fem kolonner i højre side, viser de første fire kolonner aktuelle budgetterede debet- og kreditbeløb for hver konto. Den femte kolonne viser den proportionale relation mellem de aktuelle og de budgetterede beløb på finanskontoen.  

> [!TIP]  
>   Brug feltet **Vis efter** i vinduet **Finans - saldi/budget** til at vælge periodelængden. Brug feltet **Vis som** til at vælge den måde, beløbene beregnes på, **Bevægelse** eller **Saldo til dato**. Vælg handlingen **Forrige periode** eller **Næste periode** for at ændre perioden.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Sådan får du vist aktuelle og budgetterede beløb for flere perioder  
Du kan få vist et antal perioder for en enkelt konto i stedet for at få vist aktuelle og budgetterede beløb for alle beløb i en enkelt periode.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.  
2. I vinduet **Kontoplan** skal du vælge den relevante finanskonto og derefter vælge handlingen **Finanskonto - saldo/budget**.  
3. Øverst i vinduet skal du udfylde felterne efter behov for at definere, hvad der vises.   
4. Vælg feltet, hvis du vil se en specifikation af et vist beløb.  

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Arbejde med kontoskemaer](bi-how-work-account-schedule.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

