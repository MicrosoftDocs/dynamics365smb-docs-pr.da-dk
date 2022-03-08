---
title: Sådan oprettes lagervarer | Microsoft Docs
description: Du kan bruge lagervarer til at registrere oplysninger om dine varer på en bestemt lokation eller med en bestemt variantkode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: c94a02cdbd658efcf96c5cff443ebfe03cb3feef
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785892"
---
# <a name="set-up-stockkeeping-units"></a>Opsætte lagervarer
Du kan bruge lagervarer til at registrere oplysninger om dine varer på en bestemt lokation eller med en bestemt variantkode.  

 Lagervarer er et supplement til varekortene. De erstatter dem ikke, selvom de er relateret til dem. Med lagervarer kan du udskille oplysningerne om den samme vare, så de kun vedrører en bestemt lokation, f.eks. et lager eller distributionscenter, eller en bestemt variant, f.eks. forskellige hyldenumre og forskellige genbestillingsdata.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Sådan opsættes en lagervare  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagervarer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Udfyld felterne på kortet. Følgende felter er obligatoriske: **Varenr.**, **Lokationskode** og/eller **Variantkode**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Når du har angivet den første lagervare, bliver afkrydsningsfeltet **Lagervare findes** automatisk markeret på **Vare**-kortet.  

Brug kørslen **Opret lagervare**, hvis du vil oprette flere lagerførte varer.  

> [!NOTE]  
>  Oplysningerne på **lagervarekortet** tilsidesætter oplysningerne på **varekortet**.

> [!Warning]
> Hvis lagervaren angives via produktion, bruges feltet **Kostpris (standard)** ikke ved fakturering og justering af den faktiske kostpris for den producerede vare. I stedet anvendes feltet **Kostpris (standard)** på det underliggende varekort, og eventuelle afvigelser beregnes mod kostprisfordelingen for den vare.<br /><br />
> Fordi produktionsstyklister og rute ikke kan tildeles lagervarer, så er kostprisakkumulering og den relaterede beregning af kostprisfordelingen heller ikke tilgængelig på lagervarer. Du kan finde flere oplysninger i [Om beregning af standardkostpris](finance-about-calculating-standard-cost.md)

## <a name="see-also"></a>Se også  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
