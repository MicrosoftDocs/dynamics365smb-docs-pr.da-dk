---
title: Massebogføre forbrug
description: 'Hvis trækmetoden er Manuel, skal du bogføre komponenterne manuelt ved at bruge en forbrugskladde.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000846, 99000850'
ms.date: 03/08/2023
ms.author: edupont
---
# <a name="batch-post-production-consumption"></a><a name="batch-post-production-consumption"></a><a name="batch-post-production-consumption"></a>Massebogføre produktionsforbrug

Hvis trækmetoden er **Manuel**, skal du bruge forbrugskladden til at bogføre komponenterne manuelt.  

> [!NOTE]
> Hvis du har markeret feltet **Kræv pluk** på lokationskortet for at angive, at lokationen kræver behandling af lagerpluk, behøver du ikke bruge denne kørsel. [!INCLUDE[prod_short](includes/prod_short.md)] håndterer forbruget, når du bogfører lagerpluk. Du kan finde flere oplysninger i [Plukke til produktion i grundlæggende lageropsætninger](warehouse-how-to-pick-for-production.md)  

Du kan også konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til automatisk at bogføre (*trække*) komponenterne, når du starter eller afslutter produktionsordrer. Du kan finde flere oplysninger i [Aktivere udtrækning af komponenter i henhold til operationsafgang](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><a name="to-post-consumption-for-one-or-more-production-order-lines"></a><a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Sådan bogføres forbrug for en eller flere produktionsordrelinjer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forbrugskladde**, og vælg derefter det relaterede link.  
2. Udfyld felterne med produktionsordredata og forbrugsdata. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Brug handlingen **Beregn forbrug** til at generere kladdelinjer fra produktionsordrer, der er baseres på den aktuelle afgang (mængden af færdige varer, der er rapporteret), eller den forventede afgang (mængden af færdige varer, du forventer at producere).

    > [!NOTE]
    > Hvis du har konfigureret lokationskortet til at kræve behandling af lagerpluk, er det kun de antal, der allerede er plukket via en lageraktivitet, der kan angives i feltet **Antal** på siden **Forbrugskladde**, ikke beregnede antal. Du kan finde flere oplysninger i [Plukke til produktion eller montage i avancerede lageropsætninger](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

3. Vælg handlingen **Bogfør** for at bogføre forbruget. De relaterede lagerbeholdninger er reduceret.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Produktion](production-manage-manufacturing.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Skabelon](production-planning.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
