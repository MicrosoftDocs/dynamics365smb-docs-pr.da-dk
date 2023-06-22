---
title: 'Konfigurere og udgive KPI-webtjenester, der er baseret på finansielle rapporter'
description: 'Denne artikel beskriver, hvordan du får vist en finansielle rapports KPI-data ud fra bestemte finansielle rapporter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="set-up-and-publish-kpi-web-services-based-on-financial-reports" />Konfigurere og udgive KPI-webtjenester, der er baseret på finansielle rapporter

På siden **Opsætning af webtjeneste for finansiel rapport-KPI** skal du angive, hvordan den finansielle rapports KPI-data skal vises, og hvilke specifikke finansielle rapporter KPI'erne skal baseres på. Når du vælger **Publicer webtjeneste**, føjes de angivne finansielle rapport-KPI-data til listen over publicerede webtjenester på siden **Webtjenester**.

> [!NOTE]
> Når du bruger denne webtjeneste, medtages ultimodatoen ikke i datasættet. Du kan derefter bruge filtre i Power BI til at analysere forskellige tidsperioder.

## <a name="set-up-and-publish-a-kpi-web-service-based-on-financial-reports" />Konfigurere og udgive KPI-webtjenester, der er baseret på finansielle rapporter
  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af webtjeneste for finansiel rapport-KPI**, og vælg derefter det relaterede link.
2. Udfyld felterne i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Udfyld felterne i oversigtspanelet **Dimensioner**.
4. Gentag trin 3 for alle de finansielle rapporter, som du vil basere den finansielle rapports KPI-webtjenesten på.  
5. Hvis du vil se eller redigere den valgte finansielle rapport, skal du vælge handlingen **Rediger rækkedefinition** i oversigtspanelet **Rækkedefinitioner**.
6. Hvis du vil se den finansielle rapports KPI-data, som du har konfigureret, skal du vælge handlingen **Webtjeneste for finansiel rapport-KPI**.
7. Hvis du vil udgive den finansielle rapports KPI-webtjenesten, skal du vælge handlingen **Publicer webtjeneste**.

Du kan nu oprette regnskabsrapporter i Power BI på basis af den webtjeneste eller de tjenester, du har oprettet.

> [!NOTE]  
> Du kan også publicere KPI-webtjenesten ved at pege på sideobjektet **Opsætning af webtjeneste for finansiel rapport-KPI** fra siden **Webtjenester**. Få mere at vide i [Udgive en webtjeneste](across-how-publish-web-service.md).

## <a name="see-also" />Se også

[Financial Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
