---
title: Sådan kombineres leverancer på én enkelt faktura | Microsoft Docs
description: 'Hvis du vil fakturere mere end én leverance samtidig, kan du bruge samlefunktionen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 12/16/2021
ms.author: edupont
---
# <a name="combine-shipments-on-a-single-invoice" />Kombinere leverancer på én enkelt faktura

Hvis du vil fakturere mere end én leverance samtidig, kan du bruge samlefunktionen.  

Før du kan oprette en samleleverance, skal der bogføres mere end én salgsleverance i samme valuta til den samme kunde. Du skal med andre ord oprette to eller flere salgsordrer og bogføre dem som leveret, men ikke faktureret. 

## <a name="to-manually-combine-shipments-on-a-single-invoice" />Sådan kombinerer du manuelt leverancer på én enkelt faktura

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md).
3. I feltet **Kundenr** skal du angive den kunde, der skal modtage fakturaen for de leverede varer.  
4. I oversigtspanelet **Linjer** skal du vælge handlingen **Hent salgsleverancelinjer**.  
5. Vælg de leverancelinjer, der skal indgå i fakturaen:  

    - Hvis alle linjer skal indsættes, skal du markere samtlige linjer og vælge knappen **OK**.  
    - Hvis specifikke linjer skal indsættes, skal du markere linjerne og vælge knappen **OK**. Du kan bruge Ctrl-tasten til at markere flere ikke-fortløbende linjer.  

    Hvis du kommer til at vælge en forkert leveringslinje eller vil begynde forfra, skal du bare slette linjerne på fakturaen og bruge funktionen **Hent salgsleverancelinjer** igen.  
7. Vælg handlingen **Bogfør** for at fakturere kladden.  

> [!TIP]  
> Hvis du har leveret ordrer, hvor feltet **Kundenr.** er forskellig fra feltet **Faktureres til kundenr.**, vises disse linjer ikke i rapporten **Hent salgsleverancelinjer**. Bruge personlige indstillinger til at føje feltet **kundenavn** på siden og fjerne filteret. Du kan nu føje leverancelinjer til fakturaen, uanset værdien i feltet **Kundenr.**, hvis feltet **Faktureres til kundenr.** på leverancelinjerne svarer til værdien på salgsfakturaen.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice" />Sådan kombinerer du automatisk leverancer på én enkelt faktura

[!INCLUDE[prod_short](includes/prod_short.md)] vælger kun salgsordrer, hvor **Tillad samlefaktura** er valgt. 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kombinere leverancer**, og vælg derefter det relaterede link. Kørselssiden åbnes.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vælg afkrydsningsfeltet **Bogfør fakturaer**.  
4. Vælg knappen **OK**.  

> [!NOTE]  
>  Du er nødt til at bogføre fakturaerne manuelt, hvis afkrydsningsfeltet **Bogfør fakturaer** ikke var markeret til kørslen.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting" />Sådan fjernes åbne salgsordrer efter bogføring af kombineret leverance

Når leverancer samles på en faktura og bogføres, oprettes der en bogført salgsfaktura for de fakturerede linjer. Feltet **Faktureret (antal)** på den oprindelige rammesalgsordre eller salgsordre opdateres på basis af det fakturerede antal.  

Når du fakturerer leverancer på denne måde, findes de ordrer, som leverancerne er bogført fra, stadig, selvom de er leveret og faktureret i fuldt omfang.   

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Slet fakturerede salgsordrer**, og vælg derefter det relaterede link.  
2. I feltet **Nummer** skal du angive, hvilke ordrer der skal slettes.  
3. Vælg knappen **OK**.  

Du kan også slette individuelle salgsordrer manuelt.  

Gentag trin 1 til 3 for eventuelle andre berørte dokumenter, f.eks. rammesalgsordrer.

## <a name="see-related-microsoft-trainingtrainingmodulesinvoicing-customers-dynamics--business-central" />Se relateret [Microsoft-træning](/training/modules/invoicing-customers-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
