---
title: Organisere varer i kategorier | Microsoft Docs
description: "Du kan tildele vareattributter og organisere varerne i kategorier for at gøre det nemmere at søge efter og finde varer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: da87c427033d58d92a6a5222bc323c68c4bc3f4e
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-categorize-items"></a>Fremgangsmåde: Kategorisere elementer
Hvis du vil have en oversigt over dine varer og hjælp til at sortere og finde varer, er det nyttigt at arrangere varerne i varekategorier.

Hvis du vil kunne finde varer ud fra egenskaber, kan du tildele vareattributter til varer og til varekategorier. Du kan finde flere oplysninger under [Fremgangsmåde: Arbejde med vareattributter](inventory-how-work-item-attributes.md).

## <a name="to-create-an-item-category"></a>Sådan oprettes en varekategori
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kategorier**, og vælg derefter det relaterede link.
2. I vinduet **Varekategorier** skal du vælge handlingen **Ny**.
3. Udfyld felterne efter behov i vinduet **Varekategorikort** i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I oversigtspanelet **Attributter** skal du angive eventuelle vareattributter for varekategorien. Hvis du vil finde flere oplysninger, skal du se afsnittet "Sådan tildeles vareattributter til en varekategori" i [Fremgangsmåde: Arbejde med vareattributter](inventory-how-work-item-attributes.md).

> [!NOTE]  
>   Hvis varekategorikoden har en overordnet varekategori som angivet af feltet **Overordnet kategori**, udfyldes de vareattributter på forhånd i oversigtspanelet **Attributter**, som er tildelt den pågældende overordnede varekategori.

> [!NOTE]  
>   Vareattributter, som du tildeler til en varekategori, anvendes automatisk til den vare, der er tildelt varekategorien.

## <a name="to-assign-an-item-category-to-an-item"></a>Sådan tildeles en varekategori til en vare
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for den vare, du vil tildele til en varekategori.
3. Vælg opslagsknappen i feltet **Kategorikode**, og vælg en eksisterende varekategori. Du kan også vælge handlingen **Ny** for først at oprette en ny varekategori som beskrevet i afsnittet "Sådan oprettes en varekategori".

## <a name="see-also"></a>Se også
[Fremgangsmåde: Arbejde med vareattributter](inventory-how-work-item-attributes.md)  
[Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

