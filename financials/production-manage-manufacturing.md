---
title: "Udføre produktion | Microsoft Docs"
description: "Når der er planlagt for behovet, og materialerne er udstedt i henhold til produktionsstyklisterne, kan de faktiske produktionsoperationer starte, og de kan så udføres i den rækkefølge, der er defineret i produktionsordrens rute."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: e27ceb91b25669a31d95256385cb7e5acd9160bd
ms.contentlocale: da-dk
ms.lasthandoff: 09/27/2017

---
# <a name="manufacturing"></a>Produktion
Når der er planlagt for behovet, og materialerne er udstedt i henhold til produktionsstyklisterne, kan de faktiske produktionsoperationer starte, og de kan så udføres i den rækkefølge, der er defineret i produktionsordrens rute.  

En vigtig del af produktionsudførelsen, fra et systemmæssigt synspunkt, er at bogføre produktionsafgang til databasen, så status kan rapporteres og lageret kan opdateres med de færdige dele. Afgangsbogføring kan udføres manuelt, når du udfylder og bogfører kladdelinjer efter produktionsoperationer. Det kan også udføres automatisk med brug af baglæns træk. Hvis det er tilfældet, bogføres materialeforbrug automatisk sammen med afgang, når produktionsordren ændres til færdig.  

Som et alternativ til massekladden til afgangsbogføring for flere produktionsordrer kan du bruge vinduet **Produktionskladde** til at bogføre forbrug og/eller afgang for én produktionsordrelinje.

Før du kan begynde at producere varer, skal du foretage forskellige opsætninger, f.eks. af arbejdscentre, ruter og produktionsstyklister. Du kan finde flere oplysninger i [Konfigurere produktion](production-configure-production-processes.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Forstå, hvordan produktionsordrer fungerer.|[Om produktionsordrer](production-about-production-orders.md)|
|Opret produktionsordrer manuelt.|[Fremgangsmåde: Oprette produktionsordrer](production-how-to-create-production-orders.md)|
|Outsource alle eller udvalgte operationer i en produktionsordre til en underleverandør.|[Fremgangsmåde: Produktion hos underleverandør](production-how-to-subcontract-manufacturing.md)|
|Registrere og bogføre produktionsoutput sammen med materiale- og tidsforbrug for en enkelt frigivet produktionsordrelinje.|[Fremgangsmåde: Bogføre forbrug og afgang for én frigivet produktionsordrelinje](production-how-to-register-consumption-and-output.md)|  
|Massebogfør antallet af komponenter, der anvendes pr. operation i en kladde, der kan behandle flere planlagte produktionsordrer.|[Fremgangsmåde: Massebogføre forbrug](production-how-to-post-consumption.md)|
|Bogfør antallet af færdige varer og tidsforbruget pr. operation i en kladde, der kan behandle flere frigivne produktionsordrer.|[Fremgangsmåde: Massebogføre afgang og operationstider](production-how-to-post-output-quantity.md)|  
|Bogføre antallet af varer, der er fremstillet i hver enkelt færdiggjort operation, som ikke er kvalificeret som færdigt output men som spildmateriale.|[Fremgangsmåde: Bogføre spild](production-how-to-post-scrap.md)|
|Få vist belastningen for produktionen som følge af planlagte og frigivne produktionsordrer.|[Fremgangsmåde: Vise belastningen på arbejdscentre og produktionsressourcer](production-how-to-view-the-load-on-work-centers.md)|      
|Bruge vinduet **Kapacitetskladde** til at bogføre forbrugt kapacitet, der ikke er tilknyttet en produktionsordre, f.eks. vedligeholdelsesarbejde.|[Fremgangsmåde: Bogføre kapaciteter](production-how-to-post-capacities.md)|  
|Beregne og justere prisen på færdigproducerede varer og forbrugte komponenter til økonomisk afstemning.|[Om de færdige produktionsomkostninger](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a>Se også  
[Konfigurere produktion](production-configure-production-processes.md)  
[Planlægning](production-planning.md)      
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

