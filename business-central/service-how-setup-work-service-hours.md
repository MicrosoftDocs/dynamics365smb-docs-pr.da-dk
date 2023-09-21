---
title: 'Sådan gør du: Definere arbejdstimer og serviceåbningstider'
description: 'Se, hvordan du kan bruge betjenings- og serviceåbningstiderne til at beregne svardato og svartidspunkt for serviceordrer og tilbud.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# Konfigurere arbejdstimer og serviceåbningstider
Et servicestyringssystem bruges typisk til at holde styr på ressourcetimer og serviceordrestatus med det formål at kunne estimere arbejdsbelastning og servicebehov. [!INCLUDE[prod_short](includes/prod_short.md)] har indbyggede værktøjer, som kan tilpasses til at registrere denne type oplysninger.  
  
Når du angiver virksomhedens standardservicetimer, kan du beregne responstiden for serviceordrer eller sende advarsler og påmindelser, når der indløber servicebesøg. Påmindelsesfunktionen implementeres i forbindelse med Job Scheduler.   
  
Når du arbejder på en serviceordre, vil du gerne kunne opdatere dens status, så du kan overvåge fremdriften. Serviceordrens status afspejler reparationsstatus for alle serviceartikler i serviceordren. Du kan finde flere oplysninger i [Om serviceordre og reparationsstatus](service-order-repair-status.md). 

## Sådan angives standardserviceåbningstider  
Du kan bruge siden **Standardserv.åbningstider** til at angive almindelige serviceåbningstider i din virksomhed. Serviceåbningstiderne bruges til at beregne svardato og -tidspunkt for serviceordrer og tilbud og til at udsende advarsler vedr. svartid. Standardserviceåbningstiderne anvendes automatisk til servicekontrakter, medmindre du angiver særlige serviceåbningstider for en kontrakt.  
  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Standardserv.åbningstider**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  Hvis du lader linjerne på siden **Standardserv.åbningstider** være tomme, bruges 24 timer som standardværdi, og den vil kun gælde på almindelige arbejdsdage.  
  
## Sådan oprettes arbejdstidsskabeloner
Du kan bruge siden **Arbejdstidsskabelon** til at oprette skabeloner, der indeholder den typiske arbejdstid i din virksomhed. Du kan f.eks. oprette skabeloner for teknikere, der arbejder på fuld tid eller på deltid. Du kan bruge arbejdstidsskabeloner, når du føjer kapacitet til ressourcer.  
  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Skabeloner for arbejdstid**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> Når du har angivet arbejdstimer for hver dag, beregnes værdien i feltet **I alt pr. uge** automatisk.  

## Sådan angives kontraktspecifikke serviceåbningstider  
Du kan bruge siden **Serviceåbningstider** til at angive specifikke serviceåbningstider for den debitor, servicekontrakten tilhører. Serviceåbningstiderne bruges til at beregne svardato og svartidspunkt for serviceordrer og tilbud, som hører til servicekontrakten.  
  
Hvis du ikke angiver specifikke serviceåbningstider for servicekontrakten, anvendes standardserviceåbningstiderne.  
  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Servicekontrakter**, og vælg derefter det relaterede link.  
2. Åbn den servicekontrakt, du vil angive specifikke serviceåbningstider for, og vælg **Serviceåbningstider**.  
4. Hvis du vil angive serviceåbningstider baseret på standardserviceåbningstider, skal du vælge handlingen **Kopier stand.serv.åbningstider**.  
5. Rediger felterne i posterne for serviceåbningstider. Indsæt eller slet poster for at konfigurere serviceåbningstider for kontrakten. Bemærk, at felterne **Dag**, **Starttidspunkt** og **Sluttidspunkt** er påkrævede for hver linje.  
6. Hvis serviceåbningstiderne skal være gældende fra en bestemt dato, skal du udfylde feltet **Startdato**.  
7. Hvis serviceåbningstiderne skal gælde på fridage, skal du markere afkrydsningsfeltet **Gælder på fridage**.  

## Se også  
[Om allokeringsstatus og reparationsstatus](service-allocation-status-and-repair-status.md)  
[Konfigurere Service](service-setup-service.md)  
[Om serviceordre- og reparationsstatus](service-order-repair-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]