---
title: "Fremgangsmåde: Arbejde med vareattributter | Microsoft Docs"
description: Beskriver, hvordan du konfigurerer vareattributter og tildeler dem til varer og varekategorier.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.date: 04/20/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 82fee2e5b1ae3e87e607cd930973a8be32045e71
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-work-with-item-attributes"></a>Fremgangsmåde: Arbejde med vareattributter
Når kunder forespørger om en vare, enten via korrespondance eller en integreret en webshop, kan de spørge eller søge ud fra egenskaber som f.eks højde og modelår. For at yde denne kundeservice kan du tildele vareattributværdier af forskellige typer til dine varer, som kan bruges ved søgning efter varer.

Du kan også tildele vareattributter til varekategorier, som derefter gælder for de varer, der bruger varekategorier. Yderligere oplysninger findes under [Fremgangsmåde: Kategorisere vare](inventory-how-categorize-items.md).

## <a name="to-create-item-attributes"></a>Sådan oprettes vareattributter
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Vareattributter** og derefter vælge det relaterede link.
2. I vinduet **Vareattributter** skal du vælge handlingen **Ny**.
3. I vinduet **Vareattribut** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Bemærk**! Hvis du vælger **Indstilling** i feltet **Type**, kan du vælge handlingen **Vareattributværdier** for at oprette værdier for vareattributten. Du kan finde flere oplysninger i afsnittet "Sådan oprettes værdier for vareattributter af typen Indstilling".  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Sådan oprettes værdier for vareattributter af typen Indstilling
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Vareattributter** og derefter vælge det relaterede link.
2. I vinduet **Vareattributter** skal du vælge en vareattribut af typen **Indstilling**, som du vil oprette værdier for, og derefter vælge handlingen **Vareattributværdier**.
3. I vinduet **Vareattributværdier** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Sådan tildeles vareattributter til varer
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Varer** og derefter vælge det relaterede link.
2. I vinduet **Varer** skal du vælge den vareattribut, du vil tildele vareattributter til, og derefter vælge handlingen **Attributter**.
3. I vinduet **Vareattributværdier** skal du vælge handlingen **Ny**.
4. Vælg opslagsknappen i feltet **Attribut**, og vælg en eksisterende vareattribut. Du kan også vælge handlingen **Ny** for først at oprette en ny vareattribut som beskrevet i afsnittet "Sådan oprettes vareattributter".
5. I feltet **Værdi** skal du angive vareattributværdien som "2010" for attributten **Modelår**.
6. For vareattributter af typen **Indstilling** skal du vælge opslagsknappen i feltet **Værdi** og vælge en vareattributværdi. Du kan også vælge handlingen **Ny** for først at oprette en ny vareattributværdi som beskrevet i afsnittet "Sådan oprettes værdier for vareattributter af typen Indstilling".
7. Gentag trin 4-6 for alle vareattributter, du vil tildele til varen.

## <a name="to-assign-item-attributes-to-item-categories"></a>Sådan tildeles vareattributter til varekategorier
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Varekategorier** og derefter vælge det relaterede link.
2. I vinduet **Varekategorier** skal du vælge den varekategori, som du vil tildele vareattributter til, og derefter vælge handlingen **Rediger**.
3. I vinduet **Varekategorikort** i oversigtspanelet **Attributter** skal du vælge handlingen **Ny**.
4. Vælg opslagsknappen i feltet **Attribut**, og vælg en eksisterende vareattribut. Du kan også vælge handlingen **Ny** for først at oprette en ny vareattribut som beskrevet i afsnittet "Sådan oprettes en vareattribut".
5. I feltet **Standardværdi** skal du klikke på opslagsknappen og vælge en vareattributværdi.
6. Gentag trin 4 og 5 for alle vareattributter, som du vil tildele til varekategorien.

**Bemærk**! Vareattributter for overordnede varekategorier bliver overført til underordnede varekategorier. Dette er angivet med feltet **Overført fra** på oversigtspanelet **Attributter**. Du kan finde flere oplysninger under [Fremgangsmåde: Kategorisere varer](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Sådan filtreres varer efter vareattributter
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Varer** og derefter vælge det relaterede link.
2. I vinduet **Varer** skal du vælge handlingen **Filtrer efter attributter**.
3. I vinduet **Filtrer efter attributter** skal du vælge opslagsknappen i feltet **Attribut** og vælge en vareattribut.
4. I feltet **Værdi** skal du klikke på opslagsknappen og vælge en attributværdi, som varerne skal filtreres efter.

    **Bemærk**: Du kan kun vælge værdier direkte for vareattributter som faste værdier som f.eks. Farve. Du skal angive vareattributværdien for vareattributter med variable værdier, som f.eks. Bredde, ved først at vælge en betingelse. Se trin 5.
5. I feltet **Værdi** for en variabel vareattribut skal du vælge opslagsknappen.
6. I vinduet **Angiv filterværdi** skal du i feltet **Betingelse** vælge rullepilen og vælge en betingelse.
7. I feltet **Værdi** skal du angive en attributværdi, som varer skal filtreres efter.

    **Eksempel**: Hvis du vil filtrere varer, hvor materialebeskrivelsen begynder med "blå", skal du udfylde felterne på følgende måde: feltet **Attribut**: Materialebeskrivelse, feltet **Betingelse**: Begynder med, feltet **Værdi**: blå.
8. Vælg knappen **OK**.   

Varerne i vinduet **Varer** filtreres efter de angivne vareattributværdier.

## <a name="see-also"></a>Se også
[Fremgangsmåde: Kategorisere varer](inventory-how-categorize-items.md)    
[Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

