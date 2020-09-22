---
title: Oprette vareattributter og tildele dem til varer | Microsoft Docs
description: Bruges til at oprette vareattributværdier, der f.eks. kan bruges som søgeord, og knytte dem til varer og varekategorier.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1ca5b5632093205423654c78feeaffa86104c819
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786317"
---
# <a name="work-with-item-attributes"></a>Arbejde med vareattributter
Når kunder forespørger om en vare, enten via korrespondance eller en integreret en webshop, kan de spørge eller søge ud fra egenskaber som f.eks højde og modelår. For at yde denne kundeservice kan du tildele vareattributværdier af forskellige typer til dine varer, som kan bruges ved søgning efter varer.

Du kan også tildele vareattributter til varekategorier, som derefter gælder for de varer, der bruger varekategorier. Yderligere oplysninger findes under [Kategorisere vare](inventory-how-categorize-items.md).

> [!Tip]  
> Hvis du vil knytte billeder til varer, kan billedanalyseudvidelsen registrere attributter i billedet, og foreslå attributterne, så bliver du spurgt, om du vil tildele dem. Udvidelsen er klar til brug. Du skal blot aktivere den. Du kan finde flere oplysninger i [Billedanalyseudvidelsen](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>Sådan oprettes vareattributter
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Vareattributter**, og vælg derefter det relaterede link.
2. På siden **Vareattributter** skal du vælge handlingen **Ny**.
3. På siden **Vareattribut** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Hvis du vælger **Indstilling** i feltet **Type**, kan du vælge handlingen **Vareattributværdier** for at oprette værdier for vareattributten. Du kan finde flere oplysninger i [Sådan oprettes værdier for vareattributter af typen Indstilling](inventory-how-work-item-attributes.md#to-create-values-for-item-attributes-of-type-option).  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Sådan oprettes værdier for vareattributter af typen Indstilling
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Vareattributter**, og vælg derefter det relaterede link.
2. På siden **Vareattributter** skal du vælge en vareattribut af typen **Indstilling**, som du vil oprette værdier for, og derefter vælge handlingen **Vareattributværdier**.
3. På siden **Vareattributværdier** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Sådan tildeles vareattributter til varer
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. På siden **Varer** skal du vælge den vareattribut, du vil tildele vareattributter til, og derefter vælge handlingen **Attributter**.
3. På siden **Vareattributværdier** skal du vælge handlingen **Ny**.
4. Vælg opslagsknappen i feltet **Attribut**, og vælg en eksisterende vareattribut. Du kan også vælge handlingen **Ny** for først at oprette en ny vareattribut som beskrevet i [Sådan oprettes vareattributter](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. I feltet **Værdi** skal du angive vareattributværdien som "2010" for attributten **Modelår**.
6. For vareattributter af typen **Indstilling** skal du vælge opslagsknappen i feltet **Værdi** og vælge en vareattributværdi. Du kan også vælge handlingen **Ny** for først at oprette en ny vareattributværdi som beskrevet i [Sådan oprettes værdier for vareattributter af typen Indstilling](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-items).
7. Gentag trin 4-6 for alle vareattributter, du vil tildele til varen.

## <a name="to-assign-item-attributes-to-item-categories"></a>Sådan tildeles vareattributter til varekategorier
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varekategorier**, og vælg derefter det relaterede link.
2. På siden **Varekategorier** skal du vælge den varekategori, som du vil tildele vareattributter til, og derefter vælge handlingen **Rediger**.
3. På siden **Varekategorikort** i oversigtspanelet **Attributter** skal du vælge handlingen **Ny**.
4. Vælg opslagsknappen i feltet **Attribut**, og vælg en eksisterende vareattribut. Du kan også vælge handlingen **Ny** for først at oprette en ny vareattribut som beskrevet i [Sådan oprettes vareattributter](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. I feltet **Standardværdi** skal du klikke på opslagsknappen og vælge en vareattributværdi.
6. Gentag trin 4 og 5 for alle vareattributter, som du vil tildele til varekategorien.

> [!NOTE]  
>   Vareattributter for overordnede varekategorier bliver overført til underordnede varekategorier. Dette er angivet med feltet **Overført fra** på oversigtspanelet **Attributter**. Yderligere oplysninger findes under [Kategorisere varer](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Sådan filtreres varer efter vareattributter
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
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

## <a name="see-also"></a>Se også
[Kategorisere varer](inventory-how-categorize-items.md)    
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
