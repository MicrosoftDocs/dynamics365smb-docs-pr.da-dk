---
title: Analysere faktiske beløb sammenlignet med budgetterede beløb
description: 'Denne artikel beskriver, hvordan du analyserer faktiske beløb vs. budgetterede beløb som en metode til at indsamle, analysere og dele virksomhedens data.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '120, 121, 422'
ms.date: 09/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Analysere faktiske beløb sammenlignet med budgetterede beløb

Som et led i indsamling, analyse og deling af virksomhedens data kan du få vist faktiske beløb sammenlignet med budgetterede beløb for alle konti og for flere perioder.

Hvis du vil analysere budgetterede beløb, skal du først oprette finansbudgetter. Flere oplysninger i [Oprette finansbudgetter](finance-how-create-budgets.md).

## <a name="view-a-gl-budget"></a>Vise et finansbudget

budget med dimensioner kan du filtrere poster og få vist et bestemt budget.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Angiv **Finansbudgetter**, og vælg derefter det relaterede link.
2. På siden **Finansbudgetter** skal du åbne det budget, du vil se.  
3. Øverst på siden skal du udfylde felterne efter behov for at definere, hvad der vises. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Hvis du har valgt **Periode** i feltet **Vis som linjer** eller feltet **Vis som kolonner**, skal du udfylde feltet **Vis efter**. Hvis du ikke har valgt **Periode** i et af felterne, skal du angive den relevante periode i feltet **Datofilter**.  

> [!NOTE]  
> Kun poster i finansbudgettet med de filterkoder, du har angivet i oversigtspanelet **Filtre**, medtages i beregningen. Budgetposter uden nogen eller med andre filterkoder medtages ikke. Så længe filtret bliver på siden, vises budgettet kun med de poster, der har disse filterkoder.  

> [!TIP]  
> Brug handlingen **Rediger budget** for at redigere budgettet. Vælg et beløb på budgetsiden for at få vist de underliggende finansbudgetposter.

## <a name="view-actual-and-budgeted-amounts-for-all-accounts"></a>Vise aktuelle og budgetterede beløb for alle konti

Du kan få vist finansbudgetter og sammenligne dem med faktiske tal i flere områder af [!INCLUDE[prod_short](includes/prod_short.md)].

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
2. På siden **Kontoplan** skal du vælge handlingen **Finans - saldi/budget**.
3. I oversigtspanelet **Indstillinger** skal du udfylde felterne efter behov for at definere, hvad der vises i tabellen.  
4. Hold markøren over et felt i tabellen for at læse en kort beskrivelse af det viste beløb.

> [!NOTE]  
> Det filter, du har angivet på sidens hoved, anvendes til både finans- og budgetposter.

Den venstre kolonne indeholder kontoplanen. Af de fem kolonner i højre side, viser de første fire kolonner aktuelle budgetterede debet- og kreditbeløb for hver konto. Den femte kolonne viser den proportionale relation mellem de aktuelle og de budgetterede beløb på finanskontoen.  

> [!TIP]  
> Brug feltet **Vis efter** på siden **Finans - saldi/budget** til at vælge periodelængden. Brug feltet **Vis som** til at vælge den måde, beløbene beregnes på, enten **Bevægelse** eller **Saldo til dato**. Vælg handlingen **Forrige periode** eller **Næste periode** for at ændre perioden.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Sådan får du vist aktuelle og budgetterede beløb for flere perioder

Du kan få vist et antal perioder for en enkelt konto i stedet for at få vist aktuelle og budgetterede beløb for alle beløb i en enkelt periode.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Angiv **Kontoplan**, og vælg derefter det relaterede link.  
2. På siden **Kontoplan** skal du vælge den relevante finanskonto og derefter vælge handlingen **Finanskonto - saldo/budget**.  
3. I oversigtspanelet **Indstillinger** skal du udfylde felterne efter behov for at definere, hvad der vises i tabellen.  
4. I oversigtspanelet **Linjer** skal du hold markøren over et felt i tabellen for at læse en kort beskrivelse af det viste beløb.  

## <a name="see-also"></a>Se også

[Økonomisk Business Intelligence](bi.md)  
[Arbejde med finansielle rapporter](bi-how-work-account-schedule.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
