---
title: "Sådan defineres arbejdstimer og serviceåbningstider | Microsoft Docs"
description: "Du kan angive de almindelige serviceåbningstider i din virksomhed. Serviceåbningstiderne bruges til at beregne svardato og -tidspunkt for serviceordrer og tilbud og til at udsende advarsler vedr. svartid."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 630875f80f4107522962c79734284569cbc2b6f7
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-work-hours-and-service-hours"></a>Konfigurere arbejdstimer og serviceåbningstider
Et servicestyringssystem bruges typisk til at holde styr på ressourcetimer og serviceordrestatus med det formål at kunne estimere arbejdsbelastning og servicebehov. [!INCLUDE[d365fin](includes/d365fin_md.md)] har indbyggede værktøjer, som kan tilpasses til at registrere denne type oplysninger.  
  
Når du angiver virksomhedens standardservicetimer, kan du beregne responstiden for serviceordrer eller sende advarsler og påmindelser, når der indløber servicebesøg. Påmindelsesfunktionen implementeres i forbindelse med Job Scheduler.   
  
Når du arbejder på en serviceordre, vil du gerne kunne opdatere dens status, så du kan overvåge fremdriften. Serviceordrens status afspejler reparationsstatus for alle serviceartikler i serviceordren. Du kan finde flere oplysninger i [Om serviceordre og reparationsstatus](service-order-repair-status.md). 

## <a name="to-set-up-default-service-hours"></a>Sådan angives standardserviceåbningstider  
Du kan bruge vinduet **Standardserv.åbningstider** til at angive almindelige serviceåbningstider i din virksomhed. Serviceåbningstiderne bruges til at beregne svardato og -tidspunkt for serviceordrer og tilbud og til at udsende advarsler vedr. svartid. Standardserviceåbningstiderne anvendes automatisk til servicekontrakter, medmindre du angiver særlige serviceåbningstider for en kontrakt.  
  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Standardserv.åbningstider**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  Hvis du lader linjerne i vinduet **Standardserv.åbningstider** være tomme, bruges 24 timer som standardværdi, og den vil kun gælde på almindelige arbejdsdage.  
  
## <a name="to-set-up-work-hour-templates"></a>Sådan oprettes arbejdstidsskabeloner
Du kan bruge vinduet **Arbejdstidsskabelon** til at oprette skabeloner, der indeholder den typiske arbejdstid i din virksomhed. Du kan f.eks. oprette skabeloner for teknikere, der arbejder på fuld tid eller på deltid. Du kan bruge arbejdstidsskabeloner, når du føjer kapacitet til ressourcer.  
  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Arbejdstidsskabeloner**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> Når du har angivet arbejdstimer for hver dag, beregnes værdien i feltet **I alt pr. uge** automatisk.  

## <a name="to-set-up-contract-specific-service-hours"></a>Sådan angives kontraktspecifikke serviceåbningstider  
Du kan bruge vinduet **Serviceåbningstider** til at angive specifikke serviceåbningstider for den debitor, servicekontrakten tilhører. Serviceåbningstiderne bruges til at beregne svardato og svartidspunkt for serviceordrer og tilbud, som hører til servicekontrakten.  
  
Hvis du ikke angiver specifikke serviceåbningstider for servicekontrakten, anvendes standardserviceåbningstiderne.  
  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Servicekontrakter**, og vælg derefter det relaterede link.  
2. Åbn den servicekontrakt, du vil angive specifikke serviceåbningstider for, og vælg **Serviceåbningstider**.  
4. Hvis du vil angive serviceåbningstider baseret på standardserviceåbningstider, skal du vælge handlingen **Kopier stand.serv.åbningstider**.  
5. Rediger felterne i posterne for serviceåbningstider. Indsæt eller slet poster for at konfigurere serviceåbningstider for kontrakten. Bemærk, at felterne **Dag**, **Starttidspunkt** og **Sluttidspunkt** er påkrævede for hver linje.  
6. Hvis serviceåbningstiderne skal være gældende fra en bestemt dato, skal du udfylde feltet **Startdato**.  
7. Hvis serviceåbningstiderne skal gælde på fridage, skal du markere afkrydsningsfeltet **Gælder på fridage**.  

## <a name="see-also"></a>Se også  
[Om allokeringsstatus og reparationsstatus](service-allocation-status-and-repair-status.md)  
[Konfigurere Service](service-setup-service.md)  
[Om serviceordre- og reparationsstatus](service-order-repair-status.md)  

