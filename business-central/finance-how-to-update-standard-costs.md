---
title: Opdatere standardkostpriser
description: Du skal regelmæssigt opdatere standardkostprisen for komponenter og akkumulere de nye omkostninger til den overordnede vare.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5841
ms.date: 10/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Opdatere standardkostpriser
Du skal regelmæssigt opdatere standardkostprisen for komponenter og akkumulere de nye omkostninger til den overordnede vare. Processen består normalt af følgende fire trin:  

1.  Opdatere omkostninger på komponent- og kapacitetsniveau. Du kan finde flere oplysninger i kørslen **Foreslå kostpris (standard)**.  
2.  Konsolidering og akkumulering af komponent- og kapacitetsomkostninger til beregning af de samlede fremstillings- eller montageomkostninger for varerne.  
3.  Implementere de standardkostpriser, der angives, når du kører de tidligere kørsler. Standardkostpriserne træder ikke i kraft, før de er implementeret. Med **Implementer std.kostprisændringer**-kørslen, der opdaterer ændringerne i standardkostprisen for varer med ændringerne i tabellen Standardkostpriskladde.  
4.  Implementere ændringer for at opdatere feltet **Kostpris** på varekortet og udføre regulering af lagerværdi. Du kan finde flere oplysninger i [Regulere lagerbeholdningen](inventory-how-revalue-inventory.md).  

Du kan finde flere oplysninger i [Om beregning af standardkostpris](finance-about-calculating-standard-cost.md).
  
## Sådan opdateres standardkostpriser

1.  Udfør kørslen **Juster kostpris - vareposter**. Start jobbet ved at vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **uster kostpris – Vareposter**, og vælg derefter det relaterede link. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Gennemse resultaterne, og foretag de nødvendige ændringer.  
2.  Udfør kørslen **Bogfør lagerregulering**. Start jobbet ved at vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogfør lagerregulering**, og vælg derefter det relaterede link. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Gennemse resultaterne, og foretag de nødvendige ændringer.  
3.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Standardkostpriskladde**, og brug en eller flere af følgende funktioner:

    1.  Udfør kørslen **Foreslå kostpris (standard)**.  
    2.  Gennemse resultaterne, og foretag de nødvendige ændringer.  
    3.  Udfør kørslen **Foreslå kapacitetkostpris (standard)**.  
    4.  Gennemse resultaterne, og foretag de nødvendige ændringer.
    5. Udfør kørslen **Akkum. standardkostpris**.
    6.  Gennemse resultaterne, og foretag de nødvendige ændringer.
    7.  Udfør kørslen **Implementer std.kostprisændringer**.  
4.  Gennemse og bogfør siden **Værdireguleringskladde** , som er blevet udfyldt med posterne fra det forrige trin i processen.  

## Se også

 [Om beregning af standardomkostning](finance-about-calculating-standard-cost.md)   
 [Administrere lageromkostninger](finance-manage-inventory-costs.md)   
 [Designoplysninger: Kostmetoder](design-details-costing-methods.md)   
 [Finans](finance.md)  
 [Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]