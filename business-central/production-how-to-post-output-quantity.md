---
title: Massebogføre produktionsafgang og operationstider
description: Afgangsantallet repræsenterer arbejdsforløbet i form af den færdige mængde og den anvendte kapacitet for arbejdscentret eller produktionsressourcen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000773, 99000778, 99000823, 99000827'
ms.date: 03/08/2023
ms.author: bholtorf
---
# Massebogføre afgang og operationstider

Afgangsantallet repræsenterer arbejdsforløbet i form af den færdige mængde og den anvendte kapacitet for arbejdscentret eller produktionsressourcen.

Du kan bruge afgangskladden til at:

* Justere lagerbeholdningen i forbindelse med afgang af færdige varer fra produktion.
* Registrere antal og spild for hver operation i produktionsruten.
* Registrere opsætning og operationstid for arbejdscentre og produktionsressourcer.

> [!NOTE]
> Hvis produktionsrute anvendes, opdateres lagerbeholdningen kun, når du bogfører afgangsantal for den sidste operation.

på siden **Produktionskladde** kan du udføre de samme opgaver som på **Afgangskladde**-siden og også udføre forbrugsbogføring af opgaver. Du kan finde flere oplysninger i [Registrere forbrug og afgang for én frigivet produktionsordrelinje](production-how-to-register-consumption-and-output.md).

## Sådan bogfører du afgangsantal og/eller registrerer du operationstider for en eller flere produktionsordrelinjer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afgangskladde**, og vælg derefter det relaterede link.  
2. Udfyld felterne med produktionsordredata, afgangsdata og/eller operationstid. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    Du kan bruge funktionen **Udfold rute** til at generere kladdelinjer fra produktionsordrer.
  
3. Hvis operationen er afsluttet, skal du markere feltet **Afsluttet**.  
4. Vælg handlingen **Bogfør** for at bogføre operationer.

    Kapacitetsposterne opdateres for de anvendte arbejdscentre eller produktionsressourcer med oplysninger om tid, antal og spild. Hvis du har bogført den sidste operation, føjes varen til lageret.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Se også

[Bogføre spild manuelt](production-how-to-post-scrap.md)
[Tilbageføre bogføring af afgang](production-how-to-reverse-output-posting.md)
[Produktion](production-manage-manufacturing.md)
[Konfigurere produktion](production-configure-production-processes.md)  
[Skabelon](production-planning.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
