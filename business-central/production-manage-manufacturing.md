---
title: Udføre produktion | Microsoft Docs
description: Når der er planlagt for behovet, og materialerne er udstedt i henhold til produktionsstyklisterne, kan de faktiske produktionsoperationer starte, og de kan så udføres i den rækkefølge, der er defineret i produktionsordrens rute.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: ac871665486260c02ab01dda8d893e30b34e8c4d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312984"
---
# <a name="manufacturing"></a>Produktion
> [!NOTE]
> Funktioner, der beskrives i dette emne og underordnede emner, er kun synlige i brugergrænsefladen, hvis du har oplevelsen **Premium**. Du kan finde flere oplysninger i [Ændre, hvilke funktioner der vises](ui-experiences.md).

Når der er planlagt for behovet, og materialerne er udstedt i henhold til produktionsstyklisterne, kan de faktiske produktionsoperationer starte, og de kan så udføres i den rækkefølge, der er defineret i produktionsordrens rute.  

En vigtig del af produktionsudførelsen, fra et systemmæssigt synspunkt, er at bogføre produktionsafgang til databasen, så status kan rapporteres og lageret kan opdateres med de færdige dele. Afgangsbogføring kan udføres manuelt, når du udfylder og bogfører kladdelinjer efter produktionsoperationer. Det kan også udføres automatisk med brug af baglæns træk. Hvis det er tilfældet, bogføres materialeforbrug automatisk sammen med afgang, når produktionsordren ændres til færdig.  

Som et alternativ til massekladden til afgangsbogføring for flere produktionsordrer kan du bruge siden **Produktionskladde** til at bogføre forbrug og/eller afgang for én produktionsordrelinje.

Før du kan begynde at producere varer, skal du foretage forskellige opsætninger, f.eks. af arbejdscentre, ruter og produktionsstyklister. Du kan finde flere oplysninger i [Konfigurere produktion](production-configure-production-processes.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Forstå, hvordan produktionsordrer fungerer.|[Om produktionsordrer](production-about-production-orders.md)|
|Opret produktionsordrer manuelt.|[Oprette produktionsordrer](production-how-to-create-production-orders.md)|
|Outsource alle eller udvalgte operationer i en produktionsordre til en underleverandør.|[Produktion hos underleverandør](production-how-to-subcontract-manufacturing.md)|
|Registrere og bogføre produktionsoutput sammen med materiale- og tidsforbrug for en enkelt frigivet produktionsordrelinje.|[Bogføre forbrug og afgang for den frigivne produktionsordrelinje](production-how-to-register-consumption-and-output.md)|  
|Massebogfør antallet af komponenter, der anvendes pr. operation i en kladde, der kan behandle flere planlagte produktionsordrer.|[Massebogføre forbrug](production-how-to-post-consumption.md)|
|Bogfør antallet af færdige varer og tidsforbruget pr. operation i en kladde, der kan behandle flere frigivne produktionsordrer.|[Massebogføre afgang og operationstider](production-how-to-post-output-quantity.md)|
|Fortryde afgang, for eksempel på grund af en dataindtastningsfejl og forkerte beløb.  |[Tilbageføre bogføring af afgang](production-how-to-reverse-output-posting.md)|  
|Bogføre antallet af varer, der er fremstillet i hver enkelt færdiggjort operation, som ikke er kvalificeret som færdigt output men som spildmateriale.|[Bogføre spild](production-how-to-post-scrap.md)|
|Få vist belastningen for produktionen som følge af planlagte og frigivne produktionsordrer.|[Vise belastningen på arbejdscentre og produktionsressourcer](production-how-to-view-the-load-on-work-centers.md)|      
|Bruge siden **Kapacitetskladde** til at bogføre forbrugt kapacitet, der ikke er tilknyttet en produktionsordre, f.eks. vedligeholdelsesarbejde.|[Bogføre kapaciteter](production-how-to-post-capacities.md)|  
|Beregne og justere prisen på færdigproducerede varer og forbrugte komponenter til økonomisk afstemning.|[Om de færdige produktionsomkostninger](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a>Se også  
[Konfigurere produktion](production-configure-production-processes.md)  
[Planlægning](production-planning.md)      
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
