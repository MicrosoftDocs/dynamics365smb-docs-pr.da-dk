---
title: "Designoplysninger - Forblive under overløbsniveauet | Microsoft Docs"
description: "Når du bruger Maks. antal og Fast genbestil.antal, fokuserer planlægningssystemet kun på den planlagte lagerbeholdning i det angivne tidsinterval. Det betyder, at planlægningssystemet kan foreslå overflødig forsyning, når der forekommer negative behovs- eller positive forsyningsændringer uden for det angivne tidsinterval."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bbfafc41f22a5582b90683bdacf8135e78e46843
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-staying-under-the-overflow-level"></a>Designoplysninger: Forblive under overløbsniveauet
Når du bruger metoderne Maks. antal og Fast genbestil.antal, fokuserer planlægningssystemet kun på den planlagte lagerbeholdning i det angivne tidsinterval. Det betyder, at planlægningssystemet kan foreslå overflødig forsyning, når der forekommer negative behovs- eller positive forsyningsændringer uden for det angivne tidsinterval. Hvis der derfor foreslås en overflødig forsyning, beregner planlægningssystemet, hvilket antal forsyningen skal reduceres til (eller slettes) for at undgå overflødig forsyning. Dette antal kaldes "overløbsniveauet". Overløbet kommunikeres som en planlægningslinje med en handling i form af **Ret antal (reducering)** eller **Annuller** og følgende advarselsmeddelelse:  

*Bemærk: Den forventede lagerbeholdning [xx] er højere end overløbsniveauet [xx] på forfaldsdatoen [xx].*  

![Lageroverløbsniveau](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")  

##  <a name="calculating-the-overflow-level"></a>Beregning af overløbsniveau  
Overløbsniveauet beregnes på forskellige måder afhængig af planlægningsopsætningen.  

### <a name="maximum-qty-reordering-policy"></a>Maksimalt antal som genbestillingsmetode  
Overløbsniveau = Maks. lagerbeholdning  

> [!NOTE]  
>  Hvis der findes en min. ordrestørrelse bliver den tilføjet som følger: overløbsniveau = maks. lagerbeholdning + min. ordrestørrelse.  

### <a name="fixed-reorder-qty-reordering-policy"></a>Fast genbestil.antal-genbestillingsmetode  
Overløbsniveau = Ordrekvantum + Genbestillingspunkt  

> [!NOTE]  
>  Hvis den mindste ordrestørrelse er højere end genbestillingspunktet, vil det erstatte på følgende måde: Overløbsniveau = genbestil.antal + min. ordrestørrelse  

### <a name="order-multiple"></a>Oprundingsfaktor  
Hvis en ordre findes flere gange, vil den justere overløbsniveauet for både maks. og fast genbestillingsantal som genbestillingsmetoder.  

##  <a name="creating-the-planning-line-with-overflow-warning"></a>Oprettelse af planlægningslinjen med overløbsadvarsel  
Når en eksisterende forsyning medfører, at den projekterede lagerbeholdning bliver større end overløbsniveauet ved slutningen af et interval, oprettes der en planlægningslinje. For at advare om potentiel overflødig levering indeholder planlægningslinjen en advarselsmeddelelse, feltet **Accepter aktionsmeddelelse** er ikke markeret, og aktionsmeddelelsen er enten Annuller eller Ret antal.  

### <a name="calculating-the-planning-line-quantity"></a>Beregning af antallet af planlægningslinjer.  
Planlægning af linjeantallet = aktuel forsyningsmængde – (projekteret lagerbeholdning – overløbsniveau)  

> [!NOTE]  
>  Som med alle advarselslinjer vil alle maksimale/minimale ordremængder eller oprundingsfaktorer blive ignoreret.  

### <a name="defining-the-action-message-type"></a>Definition af aktionsmeddelelsestypen  

-   Hvis antallet på planlægningslinjen er højere end 0, er aktionsmeddelelsen Ret antal  
-   Hvis antallet på planlægningslinjen er lig med eller mindre end 0, er aktionsmeddelelsen Annuller  

### <a name="composing-the-warning-message"></a>Oprettelse af advarselsmeddelelsen  
I forbindelse med overløb vises der i vinduet **Ikke-sporede planlægningselementer** en advarsel med følgende oplysninger:  

-   Det planlagte lagerniveau, der udløste advarslen  
-   Det beregnede overløbsniveau  
-   Forfaldsdatoen for forsyningshændelsen.  

Eksempel: "Den planlagte beholdning 120 er større end overløbsniveauet 60 på 28-01-11"  

## <a name="scenario"></a>Scenarie  
I dette scenario ændrer en kunde en salgsordre fra 70 til 40 stykker mellem to kørsler af planlægning. Overløbsfunktionen begynder at reducere det køb, der blev foreslået for det oprindelige salgsantal.  

### <a name="item-setup"></a>Vareopsætning  

|Genbestillingsmetode|Maks. antal|  
|-----------------------|------------------|  
|Maks. ordrestørrelse|100|  
|Genbestillingspunkt|50|  
|Lagerbeholdning|80|  

### <a name="situation-before-sales-decrease"></a>Situationen før salgsreducering  

|Begivenhed|Ret antal|Planlagt beholdning|  
|-----------|-----------------|-------------------------|  
|Dag et|Ingen|80|  
|Salg|-70|10|  
|Slutning på interval|Ingen|10|  
|Foreslå ny købsordre|+90|100|  

### <a name="situation-after-sales-decrease"></a>Situationen efter salgsreducering  

|Ændring|Ret antal|Planlagt beholdning|  
|------------|-----------------|-------------------------|  
|Dag et|Ingen|80|  
|Salg|-40|40|  
|Køb|+90|130|  
|Slutning på interval|Ingen|130|  
|Foreslå at reducere køb<br /><br /> ordre fra 90 til 60|-30|100|  

### <a name="resulting-planning-lines"></a>Resulterende planlægningslinjer  
 Der oprettes en planlægningslinje (advarsel) for at reducere køb med 30 fra 90 til 60 for at bevare den projekterede lagerbeholdning på 100 i henhold til overløbsniveauet.  

![Planlægge efter overløbsniveauet](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")  

> [!NOTE]  
>  Uden overløbsfunktionen vises der ingen advarsel, hvis den projekterede lagerbeholdning ligger over maks. Dette kan medføre en overflødig forsyning på 30.  

## <a name="see-also"></a>Se også  
[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md)   
[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)

