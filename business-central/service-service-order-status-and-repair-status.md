---
title: Serviceordrestatus og reparationsstatus
description: Serviceordrens status afspejler reparationsstatus for alle serviceartikler i serviceordren.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="service-order-status-and-repair-status"></a>Serviceordrestatus og reparationsstatus

Der er en særlig relation mellem feltet **Status** på siden **Serviceordre** og den serviceartikelreparationsstatus, der er repræsenteret af feltet **Reparationsstatuskode** på siden **Serviceordre** i Service. Serviceordrens status afspejler reparationsstatus for alle serviceartikler i serviceordren.  

> [!NOTE]  
> Disse to statusfelter er ikke relateret til feltet **Frigivelsesstatus** på serviceordrehovedet, der styrer lagerets håndtering af serviceartikler.  

Når du ændrer reparationsstatus for en serviceartikel i en serviceordre, opdateres ordrens status automatisk. Hvis du vil have vist en status, som afspejler den generelle reparationsstatus for de enkelte serviceartikler, skal du angive følgende:  

* Den serviceordrestatus, som hver enkelt reparationsstatus er tilknyttet.  
* Prioritetsniveauet for hver enkelt serviceordrestatus.  

Når du konverterer et servicetilbud til en serviceordre, ændres reparationsstatussen automatisk for hver enkelt serviceartikel i ordren til **Ingen tidl. serv.** og serviceordrestatus til **Igangsat**.  

> [!NOTE]
> Før du kan oprette serviceordrer, skal du oprette reparationsstatus og servicestatusprioriteter. Du kan finde flere oplysninger i [Konfigurere statusser for serviceordrer og reparationer](service-order-repair-status.md).

## <a name="specifying-service-order-status-for-repair-status"></a>Angive serviceordrestatus for reparationsstatus

Hver reparationsstatus er knyttet til en bestemt serviceordrestatus. Indstillingerne for serviceordrestatus er som følger:

* **Igangsat**
* **Igangsat**
* **Afvent**
* **Færdig**

Der findes følgende reparationsstatusindstillinger

* **Oprettet**
* **Igangsat**
* **Henvist**
* **Delvist repareret**
* **Tilbud færdigt**
* **Venter på kunde**
* **Reservedel bestilt**
* **Reservedel modtaget**
* **Færdig**  

### <a name="pending"></a>Igangsat

Med serviceordrestatus **Igangsat** angives, at reparationen kan starte eller fortsætte når som helst. Indstillingerne for reparationsstatus, **Ingen tidl. serv.**, **Henvist**, **Delvist repareret** og **Reservedel modtaget**, kan derfor tilknyttes denne serviceordrestatus.  

### <a name="in-process"></a>I arbejde

Serviceordrestatussen **I arbejde** angiver, at reparationen er i gang. Indstillingerne for reparationsstatus, **I arbejde** og **Reservedel modtaget**, kan derfor begge tilknyttes denne serviceordrestatus. Hvis du tilknytter statussen **Reservedel bestilt** til statussen **I arbejde**, skal du også tilknytte statussen **Reservedel modtaget** til denne serviceordrestatus.  

### <a name="on-hold"></a>Afvent

Serviceordrestatussen **Afvent** angiver, at reparationen er midlertidigt i venteposition, fordi du venter på svar fra en kunde eller på en reservedel, før du kan påbegynde reparationen. Indstillingerne for reparationsstatus, **Tilbud færdigt**, **Reservedel bestilt** og **Venter på kunde**, kan derfor tilknyttes denne serviceordrestatus.  

### <a name="finished"></a>Udført

Serviceordrestatussen **Udført** angiver, at reparationen er gjort færdig. Derfor er reparationsstatussen **Udført** knyttet til denne status.  

## <a name="assigning-priority-to-service-order-status"></a>Tildele prioritet til serviceordrestatus

Når en reparationsstatus for en serviceartikel ændres, identificerer programmet automatisk den serviceordrestatus, der er tilknyttet de forskellige indstillinger for reparationsstatus for alle serviceartiklerne i ordren. Hvis serviceartiklerne er knyttet til to eller flere indstillinger for serviceordrestatus, skal du vælge statussen med den højeste prioritet automatisk.  

Du skal afgøre, hvilken serviceordrestatus der indeholder de vigtigste oplysninger om serviceordrens status, og tildele denne status den højeste prioritet, osv.  

Når du derefter opretter en ny serviceordre, og du føjer serviceartikler til den, opdateres feltet **Prioritet** på serviceordrehovedet på basis af prioriteterne for serviceartiklerne.  

### <a name="example"></a>Eksempel

Eksempel på en typisk tildeling af prioritetsniveau:  

* I arbejde – Meget høj  
* Igangsat - Høj  
* Afvent - Lav  
* Udført - Meget lav  

Hvis én serviceartikel f.eks. har reparationsstatus **Ingen tidl. serv.** tilknyttet serviceordrestatussen **Igangsat**, en anden har **I arbejde** tilknyttet serviceordrestatussen **I arbejde**, og en tredje har **Reservedel bestilt** tilknyttet serviceordrestatus **Afvent**, vil den resulterende serviceordrestatus så blive **I arbejde**, fordi det har den højeste prioritet.  

## <a name="see-also"></a>Se også

[Konfigurere statusser for serviceordrer og reparationer](service-order-repair-status.md)  
[Konfigurere Service](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
