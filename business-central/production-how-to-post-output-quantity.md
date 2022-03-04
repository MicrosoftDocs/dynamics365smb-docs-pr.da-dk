---
title: Massebogføre produktionsafgang og operationstider
description: Afgangsantallet repræsenterer arbejdsforløbet i form af den færdige mængde og den anvendte kapacitet for arbejdscentret eller produktionsressourcen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000773, 99000778, 99000823, 99000827
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbd2a3bf8eae3ced2ad063b0baa3b138cac46401
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8135694"
---
# <a name="batch-post-output-and-run-times"></a>Massebogføre afgang og operationstider
Afgangsantallet repræsenterer arbejdsforløbet i form af den færdige mængde og den anvendte kapacitet for arbejdscentret eller produktionsressourcen.

Du kan bruge afgangskladden til at:

* Justere lagerbeholdningen i forbindelse med afgang af færdige varer fra produktion.
* Registrere antal og spild for hver operation i produktionsruten.
* Registrere opsætning og operationstid for arbejdscentre og produktionsressourcer.

> [!NOTE]
> Hvis produktionsrute anvendes, opdateres lagerbeholdningen kun, når du bogfører afgangsantal for den sidste operation.

Med vinduet **Produktionskladde** kan du udføre de samme opgaver som i vinduet **Afgangskladde** og samtidigt udføre relaterede forbrugsbogføringsopgaver. Du kan finde flere oplysninger i [Registrere forbrug og afgang for én frigivet produktionsordrelinje](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a>Sådan bogfører du afgangsantal og/eller registrerer du operationstider for en eller flere produktionsordrelinjer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afgangskladde**, og vælg derefter det relaterede link.  
2. Udfyld felterne med produktionsordredata, afgangsdata og/eller operationstid. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    Du kan bruge funktionen **Udfold rute** til at generere kladdelinjer fra produktionsordrer.
  
3. Hvis operationen er afsluttet, skal du markere feltet **Afsluttet**.  
4. Vælg handlingen **Bogfør** for at bogføre operationer. 

Kapacitetsposterne opdateres for de anvendte arbejdscentre eller produktionsressourcer med oplysninger om tid, antal og spild.  

Hvis du har bogført den sidste operation, føjes varen til lageret.  

## <a name="see-also"></a>Se også

[Bogføre spild manuelt](production-how-to-post-scrap.md)
[Tilbageføre bogføring af afgang](production-how-to-reverse-output-posting.md)
[Produktion](production-manage-manufacturing.md)
[Konfigurere produktion](production-configure-production-processes.md)  
[Skabelon](production-planning.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
