---
title: "Sådan oprettes lagervarer | Microsoft Docs"
description: "Du kan bruge lagervarer til at registrere oplysninger om dine varer på en bestemt lokation eller med en bestemt variantkode."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4870e82d4390e0a96a137579d035fee0e54b19eb
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-stockkeeping-units"></a>Opsætte lagervarer
Du kan bruge lagervarer til at registrere oplysninger om dine varer på en bestemt lokation eller med en bestemt variantkode.  

 Lagervarer er et supplement til varekortene. De erstatter dem ikke, selvom de er relateret til dem. Med lagervarer kan du udskille oplysningerne om den samme vare, så de kun vedrører en bestemt lokation, f.eks. et lager eller distributionscenter, eller en bestemt variant, f.eks. forskellige hyldenumre og forskellige genbestillingsdata.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Sådan opsættes en lagervare  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagervarer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Udfyld felterne på kortet. Følgende felter er obligatoriske: **Varenr.**, **Lokationskode** og/eller **Variantkode**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Når du har angivet den første lagervare, bliver afkrydsningsfeltet **Lagervare findes** automatisk markeret på **Vare**-kortet.  

Brug kørslen **Opret lagervare**, hvis du vil oprette flere lagerførte varer.  

> [!NOTE]  
>  Oplysningerne på **lagervarekortet** tilsidesætter oplysningerne på **varekortet**.  

## <a name="see-also"></a>Se også  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
