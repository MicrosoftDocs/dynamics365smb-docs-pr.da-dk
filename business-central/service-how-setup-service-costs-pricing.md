---
title: Konfigurere priser og omkostninger for tjenester
description: 'Lær at bruge prisfastsætningsfunktionerne til at konfigurere og tilpasse programmet, så du kan anvende og regulerer priser på serviceartikler, reparationer og ordrer.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'service, cost, service order'
ms.date: 06/25/2021
ms.author: edupont
---

# Konfigurere prissætning og ekstra omkostninger for services
Du kan bruge prisfastsætningsfunktionerne i [!INCLUDE[prod_short](includes/prod_short.md)] til at konfigurere og tilpasse programmet, så du kan anvende og regulerer priser på serviceartikler, reparationer og ordrer. Disse prisbeslutninger kan derefter let overføres til fakturaprocessen.  
  
I overensstemmelse med implementeringen kan du konfigurere prisgrupper og knytte dem til bestemte tidsperioder, debitorer eller en bestemt valuta. Du kan konfigurere faste priser, minimum- eller maksimumspriser, afhængigt af de servicekontrakter du har med kunderne. Når du regulerer priserne, kan du desuden få vist og godkende ændringer, før de bogføres i Finans.  

## Sådan oprettes serviceprisgrupper
Du kan konfigurere grupper, der indeholder serviceartikler, som du vil give samme særlige serviceprissætning. Du tildeler serviceprisgrupper til serviceartikler på serviceartikellinjer. Du kan også tildele serviceprisgrupper til serviceartikelgrupper.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Serviceprisgrupper**, og vælg derefter det relaterede link.  
2. Opret en ny serviceprisgruppe.  
3. Udfyld felterne **Kode** og **Beskrivelse**.  
4. Vælg handlingen **Konfigurer**.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > Felterne **Reguleringstype** og **Beløb** arbejder sammen om at angive, om en regulering gælder for et fast beløb, eller om den kun gælder, når den samlede servicepris er større eller mindre end beløbet i feltet **Beløb**.  

## Sådan oprettes serviceprisreguleringsgrupper  
Du kan konfigurere prisreguleringsgrupper, hvis du vil regulere serviceprissætning for serviceartikler. Du kan for eksempel konfigurere prisreguleringsgrupper, der regulerer prisen på fragt eller reservedele.  
  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Serviceprisreguleringsgrupper**, og vælg derefter det relaterede link.  
2. Opret en ny serviceprisreguleringsgruppe.  
3. Udfyld felterne **Kode** og **Beskrivelse**.  
4. Angiv typen på den post, du vil regulere, i feltet **Type**.  
  
    * Hvis du vil regulere én bestemt post, skal du angive nummeret på post i feltet **Nr.** . Hvis du lader feltet stå tomt, regulerer reguleringsgruppen alle posterne af den type, der er defineret i feltet **Type**.  
    * Hvis du vil regulere de servicepriser, der kun vedrører én bestemt service, skal du udfylde feltet **Arbejdstype**. Hvis du lader dette felt stå tomt, ignoreres det.  
  
5. I feltet **Beskrivelse** kan du skrive en kort beskrivelse til serviceprisreguleringen.  
6. Hvis du vil regulere de servicepriser, der kun vedrører én bestemt generel produktbogføringsgruppe, skal du udfylde feltet **Produktbogføringsgruppe**.

> [!Tip]
> Du kan vælge **Detaljer** for at tilføje flere oplysninger om reguleringsgruppen. Du kan for eksempel angive, hvilken vare der tilhører serviceprisreguleringsgruppen, og om dette er en vare, en ressource, en ressourcegruppe eller et gebyr.  

## Sådan konfigureres ekstra omkostninger for tjenester
Når du arbejder med serviceartikler og serviceordrer, skal du evt. registrere andre omkostninger, f.eks. rejseomkostninger i bestemte servicezoner eller startgebyrer. Når du opretter en serviceordre, du kan indsætte disse omkostninger, så føjes der en linje med typen **Omkostninger** til ordren. Du kan også oprette en standardomkostning, hvis du vil anvende omkostningen på alle serviceordrer. F.eks. hvis du altid vil anvende et startgebyr.
  
### Sådan defineres serviceomkostninger
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Serviceomkostninger**, og vælg derefter det relaterede link. 
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### Sådan angives en standardomkostning for serviceordrer
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceopsætning** og vælg derefter det relaterede link. 
2. I feltet **Startgebyr på serviceordrer** skal du vælge den relevante serviceomkostning.

## Se også
[Konfigurere Service](service-setup-service.md)  
[Service Management](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]