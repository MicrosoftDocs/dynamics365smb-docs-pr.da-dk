---
title: Definere prissætning og omkostninger for services | Microsoft Docs
description: Få at vide, hvordan du konfigurere prissætning og ekstra omkostninger for services
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8683d82b4a6f56f415f3b66efa5be11b003fe878
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "926602"
---
# <a name="set-up-pricing-and-additional-costs-for-services"></a>Konfigurere prissætning og ekstra omkostninger for services
Du kan bruge prisfastsætningsfunktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] til at konfigurere og tilpasse programmet, så du kan anvende og regulerer priser på serviceartikler, reparationer og ordrer. Disse prisbeslutninger kan derefter let overføres til fakturaprocessen.  
  
I overensstemmelse med implementeringen kan du konfigurere prisgrupper og knytte dem til bestemte tidsperioder, debitorer eller en bestemt valuta. Du kan konfigurere faste priser, minimum- eller maksimumspriser, afhængigt af de servicekontrakter du har med kunderne. Når du regulerer priserne, kan du desuden få vist og godkende ændringer, før de bogføres i Finans.  

## <a name="to-set-up-a-service-price-group"></a>Sådan oprettes serviceprisgrupper
Du kan konfigurere grupper, der indeholder serviceartikler, som du vil give samme særlige serviceprissætning. Du tildeler serviceprisgrupper til serviceartikler på serviceartikellinjer. Du kan også tildele serviceprisgrupper til serviceartikelgrupper.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceprisgrupper**, og vælg derefter det relaterede link.  
2. Opret en ny serviceprisgruppe.  
3. Udfyld felterne **Kode** og **Beskrivelse**.  
4. Vælg handlingen **Konfigurer**.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > Felterne **Reguleringstype** og **Beløb** arbejder sammen om at angive, om en regulering gælder for et fast beløb, eller om den kun gælder, når den samlede servicepris er større eller mindre end beløbet i feltet **Beløb**.  

## <a name="to-set-up-a-service-price-adjustment-group"></a>Sådan oprettes serviceprisreguleringsgrupper  
Du kan konfigurere prisreguleringsgrupper, hvis du vil regulere serviceprissætning for serviceartikler. Du kan for eksempel konfigurere prisreguleringsgrupper, der regulerer prisen på fragt eller reservedele.  
  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceprisreguleringsgrupper**, og vælg derefter det relaterede link.  
2. Opret en ny serviceprisreguleringsgruppe.  
3. Udfyld felterne **Kode** og **Beskrivelse**.  
4. Angiv typen på den post, du vil regulere, i feltet **Type**.  
  
    * Hvis du vil regulere én bestemt post, skal du angive nummeret på post i feltet **Nr.** . Hvis du lader feltet stå tomt, regulerer reguleringsgruppen alle posterne af den type, der er defineret i feltet **Type**.  
    * Hvis du vil regulere de servicepriser, der kun vedrører én bestemt service, skal du udfylde feltet **Arbejdstype**. Hvis du lader dette felt stå tomt, ignoreres det.  
  
5. I feltet **Beskrivelse** kan du skrive en kort beskrivelse til serviceprisreguleringen.  
6. Hvis du vil regulere de servicepriser, der kun vedrører én bestemt generel produktbogføringsgruppe, skal du udfylde feltet **Produktbogføringsgruppe**.

> [!Tip]
> Du kan vælge **Detaljer** for at tilføje flere oplysninger om reguleringsgruppen. Du kan for eksempel angive, hvilken vare der tilhører serviceprisreguleringsgruppen, og om dette er en vare, en ressource, en ressourcegruppe eller et gebyr.  

## <a name="to-set-up-additional-costs-for-services"></a>Sådan konfigureres ekstra omkostninger for tjenester
Når du arbejder med serviceartikler og serviceordrer, skal du evt. registrere andre omkostninger, f.eks. rejseomkostninger i bestemte servicezoner eller startgebyrer. Når du opretter en serviceordre, du kan indsætte disse omkostninger, så føjes der en linje med typen **Omkostninger** til ordren. Du kan også oprette en standardomkostning, hvis du vil anvende omkostningen på alle serviceordrer. F.eks. hvis du altid vil anvende et startgebyr.
  
### <a name="to-set-up-service-costs"></a>Sådan defineres serviceomkostninger
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceomkostninger**, og vælg derefter det relaterede link. 
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a>Sådan angives en standardomkostning for serviceordrer
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceopsætning**, og vælg derefter det relaterede link. 
2. I feltet **Startgebyr på serviceordrer** skal du vælge den relevante serviceomkostning.

## <a name="see-also"></a>Se også
[Konfigurere Service](service-setup-service.md)  
[Service Management](service-service.md)  
