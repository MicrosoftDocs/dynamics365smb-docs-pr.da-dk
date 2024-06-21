---
title: Oprette tilbud på montage til ordre-salg
description: Du kan bruge montagestyring til at tilpasse et montageelement på anmodning fra en kunde under salgsprocessen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Oprette tilbud på montage til ordre-salg

Du kan bruge montagestyring til at tilpasse et montageelement på anmodning fra en kunde under salgsprocessen. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

Du kan også oprette et salgstilbud for en tilpasset montageelement, som når du sælger en anden type emne, før det konverteres til en salgsordre. Denne proces omfatter flere ekstra trin, når du sammenligner med oprettelse af et normalt salgstilbud, og det bruger en variation af tilknyttet montageordre, som er et montagetilbud.

> [!NOTE]  
>  Ligesom alle typer tilbud bruges mængderne med montagetilbud ikke i forbindelse med tilgængelighed, planlægning eller reservationer.  

## Sådan oprettes et salgstilbud til et montage efter ordre-element

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgstilbud**, og vælg derefter det relaterede link.  
2.  Opret en ny salgstilbudslinje med en linje til et montageelement. Der er flere oplysninger i [Give salgstilbud](sales-how-make-offers.md).  
3.  I feltet **Antal til montage efter ordre** skal du angive den samlede mængde.

    > [!NOTE]  
    >  Du bør ikke give tilbud på en delmængde. Derfor skal du angive det samme antal, som du har angivet i feltet **Antal** på salgstilbudslinjen.  

4.  På oversigtspanelet **Linjer** skal du vælge **Linje**, vælg **Montage efter ordre**, og vælg derefter **Montage efter ordre-linjer**. Du kan også vælge feltet **Antal til montage efter ordre** på linjen.  
5.  På siden **Montage efter ordre-linjer** kan du gennemse eller ændre linjerne til montageordre efter det tilbud, som kunden anmoder om. Hvis du vil se flere oplysninger, kan du vælge handlingen **Vis dokument** for at åbne den samlede rammetilbudsordre. Du kan ikke ændre indholdet af de fleste felter, og du kan ikke bogføre.  
6.  Når du har reguleret montageordrelinjerne i overensstemmelse med tilbuddet, skal du lukke siden **Montage efter ordre-linjer** for at vende tilbage til siden **Salgstilbud**.  
7.  Hvis debitor accepterer tilbuddet, kan du oprette en salgsordre for det tilbudte montageelement. Der er flere oplysninger i [Give salgstilbud](sales-how-make-offers.md). Det sammenkædede montagetilbud og eventuelle tilpasninger er knyttet til den pågældende nye salgsordre for at forberede til montage af varen eller de varer, der skal sælges.  

## Se også

[Montagestyring](assembly-assemble-items.md)  
[Arbejde med montagestyklister](assembly-how-work-assembly-boms.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
