---
title: Organisere varer i kategorier (indeholder video) | Microsoft Docs
description: Du kan tildele vareattributter og organisere varerne i kategorier for at gøre det nemmere at søge efter og finde varer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.search.form: 5730, 5733, 5401
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 108f88cf9f068f28598d3b8ff8013b8879ca630a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514955"
---
# <a name="categorize-items"></a>Kategorisere varer

Hvis du vil have en oversigt over dine varer og hjælp til at sortere og finde varer, er det nyttigt at arrangere varerne i varekategorier.

Hvis du vil kunne finde varer ud fra egenskaber, kan du tildele vareattributter til varer og til varekategorier. Du kan finde flere oplysninger i [Arbejde med vareattributter](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a>Sådan oprettes en varekategori
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varekategorier**, og vælg derefter det relaterede link.
2. På siden **Varekategorier** skal du vælge handlingen **Ny**.
3. Udfyld felterne efter behov på siden **Varekategorikort** i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I oversigtspanelet **Attributter** skal du angive eventuelle vareattributter for varekategorien. Du kan finde flere oplysninger i [Sådan tildeles vareattributter til varekategorier](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
> Hvis varekategorikoden har en overordnet varekategori som angivet af feltet **Overordnet kategori**, udfyldes de vareattributter på forhånd i oversigtspanelet **Attributter**, som er tildelt den pågældende overordnede varekategori.

> [!NOTE]  
> Vareattributter, som du tildeler til en varekategori, anvendes automatisk til den vare, der er tildelt varekategorien.

Hvis du ændrer mening om en varekategori, kan du slette den. Hvis den allerede er tildelt til en vare, skal du fjerne denne tildeling, før du kan slette varekategorien.

## <a name="to-assign-an-item-category-to-an-item"></a>Sådan tildeles en varekategori til en vare

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for den vare, du vil tildele til en varekategori.
3. Vælg opslagsknappen i feltet **Kategorikode**, og vælg en eksisterende varekategori. Du kan også vælge handlingen **Ny** for først at oprette en ny varekategori som beskrevet i [Sådan oprettes en varekategori](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="categories-attributes-and-variants"></a>Kategorier, attributter og varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Se også

[Arbejde med vareattributter](inventory-how-work-item-attributes.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]