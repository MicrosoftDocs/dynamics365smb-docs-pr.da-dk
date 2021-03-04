---
title: Konfigurere ressourceallokering | Microsoft Docs
description: Få at vide, hvordan systemet kan hjælpe med at sikre, at den person, du tildeler en serviceydelse, har de nødvendige kvalifikationer til at udføre ydelsen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 48d0f9f9e51a0da3f82abdb43e8c4bb6044a5f29
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757988"
---
# <a name="set-up-resource-allocation"></a>Opsætte ressourceallokering
Det er vigtigt at finde en ressource, der er kvalificeret til at udføre arbejdet, for at sikre, at en serviceopgave udføres korrekt. Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)], så det er nemt at allokere en person, der har de korrekte kvalifikationer til sagen. I [!INCLUDE[prod_short](includes/prod_short.md)] kalder vi det _ressourceallokering_. Du kan allokere ressourcer, alt efter deres færdigheder og tilgængelighed, eller om de er i samme servicezone som kunden. 

Når du vil bruge ressourceallokering, skal du angive:  
  
* De kvalifikationer, der kræves til at reparere og vedligeholde serviceartikler. Du kan tildele dem til serviceartikler og ressourcer.  
* Geografiske områder, kaldet zoner, som du har defineret for dit marked. For eksempel øst, vest, centralt osv. Du tildeler grupperne til debitorer og ressourcer.  
* Om der skal vises ressourcekvalifikationer og zoner, og om der skal vises en advarsel, hvis en bruger vælger en ukvalificeret ressource eller en ressource, som ikke er i kundezonen.  

## <a name="to-set-up-skills"></a>Sådan oprettes kvalifikationer
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kvalifikationer**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a>Sådan tildeles kvalifikationer til serviceartikler og ressourcer
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceartikler** eller **Ressourcer**, og vælg derefter det relaterede link.  
2. Åbn kortet for serviceartiklen eller ressourcen, og vælg derefter en af følgende:  
  
    * Vælg **Ressourcekvalifikationer** for serviceartikler.  
    * Vælg **Kvalifikationer** for ressourcer.  

## <a name="to-set-up-zones"></a>Sådan defineres zoner
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Zoner**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a>Sådan tildeles zoner til kunder og ressourcer 
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer** eller **Ressourcer**, og vælg derefter det relaterede link.  
2. Åbn kortet for serviceartiklen eller ressourcen, og vælg derefter en af følgende:  
  
    * For kunder skal du vælge en zone i feltet **Servicezonekode**.  
    * For ressourcer skal du vælge handlingen **Servicezoner**.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>Sådan angiver du, hvad der skal vises, når en ressource vælges
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceopsætning**, og vælg derefter det relaterede link. 
2. I feltet **Indstilling for ressourcekval.** skal du vælge en af de indstillinger, der er beskrevet i følgende tabel.  
  
    |**Indstilling**|**Beskrivelse**|  
    |------------|-------------|  
    |Vis kode | Viser kun koden.|  
    |Vis advarsel | Viser oplysninger og en advarsel, hvis du vælger en ressource, som ikke er kvalificeret.|  
    |Bruges ikke | Viser ikke disse oplysninger.|  

## <a name="to-update-resource-capacity"></a>Sådan opdateres ressourcekapacitet  
Du skal muligvis ændre ressourcernes kapacitet.  
  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ressourcekapacitet**, og vælg derefter det relaterede link.  
2. Vælg ressourcen, og vælg derefter handlingen **Angiv kapacitet**.  
3. Foretag ændringerne, og vælg derefter **Opdater kapacitet**.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>Sådan opdateres kvalifikationer for artikler, serviceartikler eller serviceartikelgrupper
Hvis du vil ændre kvalifikationskoder, der er tildelt til varer, for eksempel fra **PC** til **PCS**, kan du gøre det for en vare, en serviceartikel eller for alle varer i en serviceartikelgruppe.  
  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer** eller **Serviceartikel** eller **Serviceartikelgruppe**, og vælg derefter det relaterede link.  
2. Vælg den enhed, der skal opdateres, og vælg derefter handlingen **Ressourcekvalifikationer**.  
3. Vælg den relevante kvalifikationskode i feltet **Kvalifikationskode** på linjen med den kode, der skal ændres.  
4.  Hvis artiklen er knyttet til serviceartikler, åbnes en dialogboks med følgende to indstillinger:  
  
    * Skift kvalifikationskoderne til den valgte værdi: Vælg denne indstilling, hvis du vil erstatte den gamle kvalifikationskode med den nye kode for alle relaterede serviceartikler.  
    * Slet kvalifikationskoderne, eller opdater deres relation: Vælg denne indstilling, hvis du kun vil ændre kvalifikationskode for denne vare. Kvalifikationskoden for de relaterede serviceartikler bliver tildelt igen, dvs. feltet **Tildelt fra** opdateres.  
  
## <a name="see-also"></a>Se også
[Allokere ressourcer](service-how-to-allocate-resources.md)  
[Konfigurere arbejdstimer og serviceåbningstider](service-how-setup-work-service-hours.md)  
[Konfigurere fejlrapportering](service-how-setup-fault-reporting.md)  
[Definere koder for standardservices](service-how-setup-service-coding.md)  
 



[!INCLUDE[footer-include](includes/footer-banner.md)]