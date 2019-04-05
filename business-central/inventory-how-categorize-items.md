---
title: Organisere varer i kategorier | Microsoft Docs
description: Du kan tildele vareattributter og organisere varerne i kategorier for at gøre det nemmere at søge efter og finde varer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: a38b69451e05e2b76f4eaaa06044c8b30214c0f0
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792712"
---
# <a name="categorize-items"></a>Kategorisere varer
Hvis du vil have en oversigt over dine varer og hjælp til at sortere og finde varer, er det nyttigt at arrangere varerne i varekategorier.

Hvis du vil kunne finde varer ud fra egenskaber, kan du tildele vareattributter til varer og til varekategorier. Du kan finde flere oplysninger under [Arbejde med vareattributter](inventory-how-work-item-attributes.md).

## <a name="to-create-an-item-category"></a>Sådan oprettes en varekategori
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varekategorier**, og vælg derefter det relaterede link.
2. På siden **Varekategorier** skal du vælge handlingen **Ny**.
3. Udfyld felterne efter behov på siden **Varekategorikort** i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I oversigtspanelet **Attributter** skal du angive eventuelle vareattributter for varekategorien. Du kan finde flere oplysninger i [Sådan tildeles vareattributter til varekategorier](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
>   Hvis varekategorikoden har en overordnet varekategori som angivet af feltet **Overordnet kategori**, udfyldes de vareattributter på forhånd i oversigtspanelet **Attributter**, som er tildelt den pågældende overordnede varekategori.

> [!NOTE]  
>   Vareattributter, som du tildeler til en varekategori, anvendes automatisk til den vare, der er tildelt varekategorien.

## <a name="to-assign-an-item-category-to-an-item"></a>Sådan tildeles en varekategori til en vare
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for den vare, du vil tildele til en varekategori.
3. Vælg opslagsknappen i feltet **Kategorikode**, og vælg en eksisterende varekategori. Du kan også vælge handlingen **Ny** for først at oprette en ny varekategori som beskrevet i [Sådan oprettes en varekategori](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="see-also"></a>Se også
[Arbejde med vareattributter](inventory-how-work-item-attributes.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
