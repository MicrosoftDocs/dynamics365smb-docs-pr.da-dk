---
title: Sådan konfigureres lagervarer
description: Brug lagervarer til at registrere oplysninger om dine varer på en bestemt lokation eller med en bestemt variant.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 06/10/2024
ms.custom: bap-template
ms.search.forms: '5704, 5700, 5702, 5701'
ms.service: dynamics-365-business-central
---

# Opsætte lagervarer

Brug lagervarer (SKU'er) til at registrere oplysninger om varer på en bestemt lokation eller med en variant. De giver dig mulighed for at tilføje forskellige oplysninger om en vare til en bestemt lokation, f. eks.:

* Et lagersted eller distributionscenter
* Varianter, f. eks. forskellige hyldenumre og forskellige genbestillingsoplysninger, for den samme vare  

## Sådan oprettes en SKU  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagervarer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov. Følgende felter er obligatoriske: **Varenr.**, **Lokationskode** og/eller **Variantkode**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Når du har angivet den første SKU, bliver afkrydsningsfeltet **Lagervare findes** automatisk markeret på kortet **Vare**.  

Brug kørslen **Opret lagervare**, hvis du vil oprette flere lagerførte varer. Få mere at vide om styring af batchjobs i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).  

> [!NOTE]  
> Oplysningerne på **lagervarekortet** tilsidesætter oplysningerne på **varekortet**.

> [!Warning]
> Hvis lagervaren angives via produktion, bruges feltet **Kostpris (standard)** ikke ved fakturering og justering af den faktiske kostpris for den producerede vare. I stedet anvender [!INCLUDE [prod_short](includes/prod_short.md)] værdien i feltet **kostpris (standard)** på det underliggende varekort, og eventuelle afvigelser beregnes mod kostprisfordelingen for den vare.<br><br>
> Selvom du kan tildele produktionsstyklister og rute til lagervarer, er kostprisakkumulering og den relaterede beregning af kostprisfordelingen ikke tilgængelig på lagervarer. Hvis du vil vide mere om standardkostpriser, skal du gå til [Om beregning af standardkostpris](finance-about-calculating-standard-cost.md)

## Se også

[Registrere nye varer](inventory-how-register-new-items.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Montagestyring](assembly-assemble-items.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
