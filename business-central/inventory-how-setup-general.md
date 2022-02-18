---
title: Konfigurere generelle lageroplysninger
description: Beskriver, hvordan du definerer den generelle Lageropsætning, så du kan administrere lagerstedet og lagerbeholdningen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.search.form: 30, 456, 461
ms.date: 07/28/2021
ms.author: edupont
ms.openlocfilehash: a4912baa7dc9bfd69c5306b95b63312bc1d29f10
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115025"
---
# <a name="set-up-general-inventory-information"></a>Konfigurere generelle lageroplysninger

Du kan angive dine generelle lageropsætning på siden **Lageropsætning**.

## <a name="to-set-up-general-inventory-information"></a>Sådan konfigurerer du generelle lageroplysninger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af Lager**, og vælg derefter det relaterede link.
2. På siden **Lageropsætning** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Hvis du vil have detaljerede oplysninger om omkostningsfelterne **Aut. lagerværdibogføring**, **Bogf. af forventet kostpris** og **Standardmetode for kostprisberegning**, skal du se [Afstemme lageromkostninger med finansregnskabet](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md) og [Designoplysninger: Bogføring af forventet kostpris](design-details-expected-cost-posting.md). Du kan finde flere oplysninger om kostpris i almindelighed under [Administrere lageromkostninger](finance-manage-inventory-costs.md).  

Hvis du automatisk vil inkludere lagerekspeditionstiden i beregningen af leveringstiden på købslinjen, kan du angive det som standardindstilling på siden **Opsætning af Lager** og for din lokation. Du kan finde flere oplysninger i [Beregne ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md).  

> [!NOTE]
> Feltet **Automatisk kostregulering** er indstillet til *Altid* som standard for at sikre, at lagerværdierne altid er korrekte i finansregnskabet, som samtidig sikrer, at salgs- og overskudsstatistikken er opdateret. Kostprisændringer fra indgående poster, f.eks. for køb eller produktionsoutput, er tilknyttet de relaterede udgående poster, f.eks. salg eller overførsler. Dette er nyttigt for nye [!INCLUDE[prod_short](includes/prod_short.md)] kunder og mindre virksomheder med relativt lave lagertransaktionsniveauer.
>
> Men i takt med at virksomhedens vækst vokser, og lagerniveauet stiger, kan det gøre systemets ydeevne langsommere. Hvis du vil minimere reduceret ydeevne under bogføringen, skal du vælge en tidsindstilling for at definere, hvor langt tilbage i forhold til arbejdsdatoen en indgående transaktion må forekomme for at udløse reguleringen af relaterede udgående værdiposter.
>
> Alternativt kan du ændre omkostningerne manuelt med kørslen Reguler kostværdi - vareposter. Du kan også slå automatisk omkostningbogføring fra eller angive feltet **Automatisk kostregulering** til *Aldrig*. I begge tilfælde vises en meddelelse, hvorfra du kan starte en assisteret opsætningsvejledning, der hjælper dig med at planlægge opgaver for opgavekøen. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se også

[Konfigurere lager](inventory-setup-inventory.md)  
[Designoplysninger: Kostmetoder](design-details-costing-methods.md)  
[Administrere lager](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]