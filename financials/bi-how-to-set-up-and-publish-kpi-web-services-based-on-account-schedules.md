---
title: "Fremgangsmåde: Konfigurere og publicere KPI-webtjenester, der er baseret på kontoskemaer | Microsoft Docs"
description: "I vinduet **Konfiguration af webtjenesten Kontoskema, KPI** skal du angive, hvordan kontoskema-KPI-dataene skal vises, og hvilke specifikke kontoskemaer KPI'erne skal baseres på."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 57f36592105faf0801864e034c3b930ae196ee62
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Konfigurere og udgive KPI-webtjenester, der er baseret på kontoskemaer
I vinduet **Konfiguration af webtjenesten Kontoskema, KPI** skal du angive, hvordan kontoskema-KPI-dataene skal vises, og hvilke specifikke kontoskemaer KPI'erne skal baseres på. Når du vælger knappen **Publicer webtjeneste**, føjes de angivne kontoskema-KPI-data til listen over publicerede webtjenester i vinduet **Webtjenester**.  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Sådan konfigureres og publiceres en KPI-webtjeneste, der er baseret på kontoskemaer  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Konfiguration af webtjenesten Kontoskema, KPI**, og vælg derefter det relaterede link.  
2.  På oversigtspanelet **Generelt** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Start på prognosticerede værdier**|Angiv, hvornår prognosticerede værdier vises på den grafiske visning af kontoskema-KPI'en.<br /><br /> De prognosticerede værdier hentes fra finansbudgetposter, som du vælger i feltet **Finansbudgetnavn**. **Bemærk:**  Hvis du ønsker at få KPI'er, der viser prognosticerede tal efter en bestemt dato og faktiske tal før datoen, kan du ændre feltet **Bogf. tilladt fra** i vinduet **Opsætning af Finans**. Du kan finde flere oplysninger i Bogf. tilladt fra.|  
    |**Finansbudgetnavn**|Angiv navnet på det finansbudget, der indeholder budgetterede værdier til kontoskema-KPI-webtjenesten.|  
    |**Periode**|Angiv den periode, som kontoskema-KPI-webtjenesten er baseret på.|  
    |**Vis efter**|Angiv, hvilket tidsinterval kontoskema-KPI'en vises i.|  
    |**Navn på webtjeneste**|Angiv navnet på kontoskema-KPI-webtjenesten.<br /><br /> Dette navn vises i feltet **Servicenavn** i vinduet **Webtjeneste**.|  

    Fortsæt med at angive et eller flere kontoskemaer, som du vil publicere som en KPI-webtjeneste i henhold til opsætningen, som du foretog i tabellen ovenfor.  

3.  På oversigtspanelet **Kontoskemaer** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kontoskemanavn**|Angiv det kontoskema, som KPI-webtjenesten er baseret på.|  
    |**Beskrivelse af kontoskema**|Angiv beskrivelsen af det kontoskema, som KPI-webtjenesten er baseret på.|  

4.  Gentag trin 3 for alle de kontoskemaer, som du vil basere kontoskema-KPI-webtjenesten på.  
5.  Hvis du ønsker at få vist det valgte kontoskema, skal du vælge handlingen **Rediger kontoskema** på oversigtspanelet **Kontoskema**.  
6.  Hvis du ønsker at få vist de kontoskema-KPI-data, som du har konfigureret, skal du vælge handlingen **Webtjenesten Kontoskema, KPI**.  
7.  Hvis du vil udgive kontoskema-KPI-webtjenesten, skal du vælge handlingen **Publicer webtjeneste**. Webtjenesten føjes til listen over publicerede webtjenester i vinduet **Webtjeneste**.  

> [!NOTE]  
>  Du kan også publicere KPI-webtjenesten ved at pege på sideobjektet **Konfiguration af webtjenesten Kontoskema, KPI** fra siden **Webtjeneste**. Du kan finde flere oplysninger i [Udgive en webtjeneste](across-how-publish-web-service.md).  

## <a name="see-also"></a>Se også  
[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

