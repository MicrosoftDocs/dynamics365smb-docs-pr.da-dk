---
title: Konfigurere statusser for serviceordrer og reparationer | Microsoft Docs
description: 'Du skal definere ni reparationsstatusindstillinger, som identificerer status for reparation og vedligeholdelse af serviceartikler i serviceordrer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Konfigurere statusser for serviceordrer og reparationer

Du skal definere reparationsstatusindstillinger, som identificerer status for reparation og vedligeholdelse af serviceartikler i serviceordrer. Du skal definere mindst ni indstillinger for reparationsstatus, som angiver de situationer eller handlinger, der udføres, når serviceartikler repareres.  

Du kan angive prioritetsniveauet for indstillinger for serviceordrestatus. De fire prioriteter er **Høj**, **Mellemhøj**, **Mellemlav** og **Lav**.  

Når du ændrer reparationsstatus for en serviceartikel i en serviceordre, opdateres serviceordrens status automatisk. Reparationsstatussen for hver enkelt serviceartikel er knyttet til serviceordrestatussen. Hvis serviceartiklerne er knyttet til to eller flere indstillinger for serviceordrestatus, vælges statussen med den højeste prioritet automatisk.  

Før du kan oprette en reparationsstatus, skal du oprette servicestatusprioriteter.

## <a name="to-set-up-service-status-priorities"></a>Sådan defineres statusprioriteter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordrestatus**, og vælg derefter det relaterede link.  
2. Marker den serviceordrestatus, du vil definere en prioritet for.  
3. Vælg den prioritet, som serviceordrestatussen skal have, i feltet **Prioritet**.  

Gentag trin 2 og 3, indtil du har defineret prioriteten for hver af de fire statusindstillinger: **Afventer**, **Igang**, **Afsluttet** og **Afventer**.  

## <a name="to-set-up-a-repair-status"></a>Definere reparationsstatus

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Reparationsstatus**, og vælg derefter det relaterede link.
2. Opret en ny reparationsstatus.  
3. Udfyld felterne **Kode** og **Beskrivelse**.  
4. I feltet **Serviceordrestatus** skal du vælge den ordrestatus, reparationsstatussen skal knyttes til. Feltet **Prioritet** viser prioriteten for den serviceordrestatus, du har valgt.  
5. Vælg en reparationsstatus. Du kan kun vælge en. En reparationsstatus kan ikke sammenkædes med mere end én indstilling for reparationsstatus.  
6. Hvis du vil kunne bogføre serviceordrer, der indeholder serviceartikler med denne reparationsstatus, skal du vælge feltet **Bogføring tilladt**.  
7. Hvis du manuelt kan ændre indstillingen for serviceordrestatus til **Igangsat** i serviceordrer, der indeholder serviceartikler med denne reparationsstatus, skal du markere afkrydsningsfeltet **Igangsat-status tilladt**.  
8. Marker afkrydsningsfelterne **I arbejde-status tilladt**, **Færdig-status tilladt** og **Afvent-status tilladt** på samme måde.

Gentag disse trin for hver af indstillingerne for reparationsstatus, du vil oprette.

## <a name="see-also"></a>Se også

[Serviceordrestatus og reparationsstatus](service-service-order-status-and-repair-status.md)  
[Konfigurere Service](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
