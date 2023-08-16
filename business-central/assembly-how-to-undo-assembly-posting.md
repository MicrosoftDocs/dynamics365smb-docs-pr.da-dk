---
title: Fortryde bogføring af montage
description: 'Få mere at vide om, hvordan du retter fejl i en bogført montageordre.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# Fortryde bogføring af montage

Annullere bogføringen af en montageordre for at rette en fejl eller fjerne en uønsket bogføring.

Når du fortryder en bogført montageordre, oprettes der et sæt korrigerende vareposter til at tilbageføre de oprindelige poster. Hver positive afgangspost for montageelementet tilbageføres af en negativ afgangspost. Hver negative forbrugspost for en montagekomponent tilbageføres af en positiv forbrugspost. Fast omkostningsanvendelse oprettes automatisk mellem korrigerende og oprindelige poster for at sikre præcis kostprisudligning.  

Når du fortryder en fuldt bogført montageordre, kan du genoprette den oprindelige ordre. Du kan f. eks. foretage rettelser, før du bogfører den igen.  

Når du fortryder en delvist bogført montageordre, gendannes alle berørte antalsfelter, f.eks i felterne **Monteret antal**, **Forbrugt antal** og **Restantal**, til de værdier, de havde, inden den pågældende bogføring.  

Hvis du vil genoprette eller gendanne montageordrer, skal følgende betingelser være opfyldt for det montageelement:  

* Det er stadig på lager. Det skal stadig være på lager, dvs. ikke solgt eller på anden måde forbrugt af udgående transaktioner.  
* Den ikke er reserveret.  
* Det skal findes på den placering, som det afgik til.  

Montageordrer kan desuden kun gendannes, hvis antallet af linjer og rækkefølgen af linjerne i den oprindelige montageordre ikke ændres.  

> [!TIP]  
> Hvis du vil løse konflikter som følge af linjeændringer, kan du manuelt tilbageføre ændringerne på de pågældende linjer, før du fortryder den relaterede bogførte montageordre. Du kan også bogføre montageordren fuldstændigt og derefter vælge at oprette den igen, når du annullerer bogføringen.  

Følgende procedure beskriver, hvordan du fortryder bogførte montageordrer, hvor der var tale om montage til lager-varer. Hvis du vil annullere bogførte montageordrer med varer, der er samlet til ordre, skal du bruge handlingen **Annuller leverance** på den relaterede bogførte leverance. Flere oplysninger i [Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md). Tilbageførslen af den bogførte montageordre sker så automatisk på samme måde som beskrevet i dette emne.  

## Sådan fortrydes bogføring af en montageordre

Du kan fortryde helt eller delvist bogførte montageordrer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte montageordrer**, og vælg derefter det relaterede link.  

   Hver delvis bogføring opretter en separat bogført montageordre.  
2. Åbn den bogførte montageordre, du vil tilbageføre, og vælg derefter handlingen **Fortryd montage**.  

    Hvis den bogførte montageordre henviser til en fuldt bogført montageordre, der er blevet slettet, kan du oprette en slettet ordre igen. Du kan f. eks. oprette ordren igen, fordi du vil genbehandle den.  
3. Hvis du vil oprette montageordren igen, skal du klikke på **Ja**. Du kan fortryde bogføringen uden at genoprette den relaterede montageordre ved at vælge knappen **Nej**.  

Feltet **Tilbageført** på montageordrehovedet ændres til **Ja**. Montageordre bogføringen er nu tilbageført. Du kan behandle hele montageordren, hvis du vælger at oprette den igen, eller hvis du har gendannet den oprindelige status i den oprindelige tilstand.  

> [!NOTE]  
> Hvis du vil gendanne mængder fra flere delvise bogføringer i en montageordre, skal du fortryde alle de pågældende bogførte montageordrer ved at følge trin 1 til 3.  

## Se også

[Montagestyring](assembly-assemble-items.md)  
[Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md)  
[Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md)  
[Arbejde med montagestyklister](assembly-how-work-assembly-boms.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]