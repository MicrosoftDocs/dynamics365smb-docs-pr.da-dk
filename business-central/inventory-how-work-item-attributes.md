---
title: Konfigurere vareattributter og tildele dem til varer
description: Bruges til at oprette vareattributværdier, der f.eks. kan bruges som søgeord, og knytte dem til varer og varekategorier.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.search.forms: 7507, 7509, 7506, 7505, 7503, 7502, 7510, 7504, 7501, 7500, 9110, 5734, 7508
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7268ac8ff38025dcd0b439e4ea6ae7d051ebc9d6
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077992"
---
# <a name="work-with-item-attributes"></a>Arbejde med vareattributter

Når kunder forespørger om en vare, enten via korrespondance eller en integreret en webshop, kan de spørge eller søge ud fra egenskaber som f.eks højde og modelår. For at yde denne kundeservice kan du tildele vareattributværdier af forskellige typer til dine varer, som kan bruges ved søgning efter varer.

Du kan også tildele vareattributter til varekategorier, som derefter gælder for de varer, der bruger varekategorier. Yderligere oplysninger findes under [Kategorisere vare](inventory-how-categorize-items.md).

> [!Tip]  
> Hvis du vil knytte billeder til varer, kan billedanalyseudvidelsen registrere attributter i billedet, og foreslå attributterne, så bliver du spurgt, om du vil tildele dem. Udvidelsen er klar til brug. Du skal blot aktivere den. Du kan finde flere oplysninger i [Billedanalyseudvidelsen](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>Sådan oprettes vareattributter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vareattributter**, og vælg derefter det relaterede link.
2. På siden **Vareattributter** skal du vælge handlingen **Ny**.
3. På siden **Vareattribut** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Hvis du vælger **Indstilling** i feltet **Type**, kan du vælge handlingen **Vareattributværdier** for at oprette værdier for vareattributten. Du kan finde flere oplysninger i [Sådan oprettes værdier for vareattributter af typen Indstilling](inventory-how-work-item-attributes.md#to-create-values-for-item-attributes-of-type-option).  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Sådan oprettes værdier for vareattributter af typen Indstilling

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vareattributter**, og vælg derefter det relaterede link.
2. På siden **Vareattributter** skal du vælge en vareattribut af typen **Indstilling**, som du vil oprette værdier for, og derefter vælge handlingen **Vareattributværdier**.
3. På siden **Vareattributværdier** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Sådan tildeles vareattributter til varer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
2. På siden **Varer** skal du vælge den vareattribut, du vil tildele vareattributter til, og derefter vælge handlingen **Attributter**.
3. På siden **Vareattributværdier** skal du vælge handlingen **Ny**.
4. Vælg opslagsknappen i feltet **Attribut**, og vælg en eksisterende vareattribut. Du kan også vælge handlingen **Ny** for først at oprette en ny vareattribut som beskrevet i [Sådan oprettes vareattributter](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. I feltet **Værdi** skal du angive vareattributværdien som "2010" for attributten **Modelår**.
6. For vareattributter af typen **Indstilling** skal du vælge opslagsknappen i feltet **Værdi** og vælge en vareattributværdi. Du kan også vælge handlingen **Ny** for først at oprette en ny vareattributværdi som beskrevet i [Sådan oprettes værdier for vareattributter af typen Indstilling](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-items).
7. Gentag trin 4-6 for alle vareattributter, du vil tildele til varen.

## <a name="to-assign-item-attributes-to-item-categories"></a>Sådan tildeles vareattributter til varekategorier

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varekategorier**, og vælg derefter det relaterede link.
2. På siden **Varekategorier** skal du vælge den varekategori, som du vil tildele vareattributter til, og derefter vælge handlingen **Rediger**.
3. På siden **Varekategorikort** i oversigtspanelet **Attributter** skal du vælge handlingen **Ny**.
4. Vælg opslagsknappen i feltet **Attribut**, og vælg en eksisterende vareattribut. Du kan også vælge handlingen **Ny** for først at oprette en ny vareattribut som beskrevet i [Sådan oprettes vareattributter](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. I feltet **Standardværdi** skal du klikke på opslagsknappen og vælge en vareattributværdi.
6. Gentag trin 4 og 5 for alle vareattributter, som du vil tildele til varekategorien.

> [!NOTE]  
>   Vareattributter for overordnede varekategorier bliver overført til underordnede varekategorier. Dette er angivet med feltet **Overført fra** på oversigtspanelet **Attributter**. Yderligere oplysninger findes under [Kategorisere varer](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Sådan filtreres varer efter vareattributter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
2. På siden **Varer** skal du vælge handlingen **Filtrer efter attributter**.
3. På siden **Filtrer efter attributter** skal du vælge opslagsknappen i feltet **Attribut** og vælge en vareattribut.
4. I feltet **Værdi** skal du klikke på opslagsknappen og vælge en attributværdi, som varerne skal filtreres efter.

    > [!NOTE]  
    >   Du kan kun vælge værdier direkte for vareattributter som faste værdier som f.eks. Farve. Du skal angive vareattributværdien for vareattributter med variable værdier, som f.eks. Bredde, ved først at vælge en betingelse. Se trin 5.
5. I feltet **Værdi** for en variabel vareattribut skal du vælge opslagsknappen.
6. På siden **Angiv filterværdi** skal du i feltet **Betingelse** vælge rullepilen og vælge en betingelse.
7. I feltet **Værdi** skal du angive en attributværdi, som varer skal filtreres efter.

    **Eksempel**: Hvis du vil filtrere varer, hvor materialebeskrivelsen begynder med "blå", skal du udfylde felterne på følgende måde: feltet **Attribut**: Materialebeskrivelse, feltet **Betingelse**: Begynder med, feltet **Værdi**: blå.
8. Vælg knappen **OK**.

Varerne på siden **Varer** filtreres efter de angivne vareattributværdier.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/trade-master-data-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Kategorisere varer](inventory-how-categorize-items.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]