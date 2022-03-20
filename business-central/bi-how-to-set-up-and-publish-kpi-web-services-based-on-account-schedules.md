---
title: Konfigurere og udgive KPI-webtjenester til kontoskemaer
description: Dette emne beskriver, hvordan du får vist kontoskemaets KPI-data ud fra bestemte kontoskemaer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 103, 104, 197, 196, 195, 198, 490, 764, 765, 766
ms.date: 06/15/2021
ms.author: bholtorf
ms.openlocfilehash: b02b8fe9aeee685f65cf82ad66c9492d241c6711
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381269"
---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Konfigurere og udgive KPI-webtjenester, der er baseret på kontoskemaer
På siden **Konfiguration af webtjenesten Kontoskema, KPI** skal du angive, hvordan kontoskema-KPI-dataene skal vises, og hvilke specifikke kontoskemaer KPI'erne skal baseres på. Når du vælger knappen **Publicer webtjeneste**, føjes de angivne kontoskema-KPI-data til listen over publicerede webtjenester på siden **Webtjenester**.  

> [!NOTE]
> Når du bruger denne webtjeneste, medtages ultimodatoen ikke i datasættet. Det giver dig mulighed for at bruge filtre i Power BI til at analysere forskellige tidsperioder.

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Sådan konfigureres og publiceres en KPI-webtjeneste, der er baseret på kontoskemaer  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Konfiguration af webtjenesten Kontoskema, KPI**, og vælg derefter det relaterede link.  
2.  På oversigtspanelet **Generelt** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Start på prognosticerede værdier**|Angiv, hvornår prognosticerede værdier vises på den grafiske visning af kontoskema-KPI'en.<br /><br /> De prognosticerede værdier hentes fra finansbudgetposter, som du vælger i feltet **Finansbudgetnavn**. **Bemærk:** Hvis du ønsker at få KPI'er, der viser prognosticerede tal efter en bestemt dato og faktiske tal før datoen, kan du ændre feltet **Bogf. tilladt fra** på siden **Opsætning af Finans**. Du kan finde flere oplysninger i Bogf. tilladt fra.|  
    |**Finansbudgetnavn**|Angiv navnet på det finansbudget, der indeholder budgetterede værdier til kontoskema-KPI-webtjenesten.|  
    |**Periode**|Angiv den periode, som kontoskema-KPI-webtjenesten er baseret på.|  
    |**Vis efter**|Angiv, hvilket tidsinterval kontoskema-KPI'en vises i.|  
    |**Navn på webtjeneste**|Angiv navnet på kontoskema-KPI-webtjenesten.<br /><br /> Dette navn vises i feltet **Servicenavn** på siden **Webtjeneste**.|  

    Angiv et eller flere kontoskemaer, som du vil publicere som en KPI-webtjeneste i henhold til opsætningen, som du foretog i tabellen ovenfor.  

3.  På oversigtspanelet **Kontoskemaer** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kontoskemanavn**|Angiv det kontoskema, som KPI-webtjenesten er baseret på.|  
    |**Beskrivelse af kontoskema**|Angiv beskrivelsen af det kontoskema, som KPI-webtjenesten er baseret på.|  

4.  Gentag trin 3 for alle de kontoskemaer, som du vil basere kontoskema-KPI-webtjenesten på.  
5.  Hvis du ønsker at få vist det valgte kontoskema, skal du vælge handlingen **Rediger kontoskema** på oversigtspanelet **Kontoskema**.  
6.  Hvis du ønsker at få vist de kontoskema-KPI-data, som du har konfigureret, skal du vælge handlingen **Webtjenesten Kontoskema, KPI**.  
7.  Hvis du vil udgive kontoskema-KPI-webtjenesten, skal du vælge handlingen **Publicer webtjeneste**. Webtjenesten føjes til listen over publicerede webtjenester på siden **Webtjeneste**.  

> [!NOTE]  
>  Du kan også publicere KPI-webtjenesten ved at pege på sideobjektet **Konfiguration af webtjenesten Kontoskema, KPI** fra siden **Webtjeneste**. Du kan finde flere oplysninger i [Udgive en webtjeneste](across-how-publish-web-service.md).  

## <a name="see-also"></a>Se også  
[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]