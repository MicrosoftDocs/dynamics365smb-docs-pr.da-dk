---
title: Finde bogførte dokumenter uden indgående dokumenter
description: 'Du kan søge efter finansposter for bogførte købs- og salgsdokumenter, der ikke har indgående elektroniske dokumenter, f.eks. importerede fakturaer.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="find-posted-documents-without-incoming-document-records" />Finde bogførte dokumenter uden indgående bilagsposter

Fra på siderne **Kontoplan** og **Finansposter** kan du bruge en søgefunktionen til at finde finansposter for bogførte og købs- og salgsbilag, som ikke har indgående bilagsposter og derefter knytte centralt til eksisterende poster eller oprette nye med vedhæftede bilagsfiler.

## <a name="to-find-posted-documents-without-incoming-document-records" />Sådan findes bogførte bilag uden indgående bilagsposter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.
2. Vælg en linje for en finanskonto, for hvis finansposter du vil se bogførte købs- og salgsbilag uden indgående bilagsposter, og vælg derefter handlingen **Bogførte bilag uden indgående bilag**.
3. Alternativt kan du vælge handlingen **Poster**.
4. På siden **Finansposter** skal du vælge handlingen **Bogførte bilag uden indgående bilag**.

Siden **Bogførte bilag uden indgående bilag** åbnes og viser bogførte købs- åbnes og salgsbilag uden indgående bilagsposter repræsenteret af finansposter på den finanskonto, som du åbnede siden for. Siden kan vise højst 1000 linjer. Som standard indeholder feltet **Datofilter** derfor et filter, der begrænser linjerne til poster med bogføringsdatoer fra begyndelsen af den aktuelle regnskabsperiode til arbejdsdatoen.

## <a name="to-connect-found-documents-to-existing-incoming-document-records" />Sådan knyttes fundne bilag til eksisterende indgående bilagsposter

1. På siden **Bogførte bilag uden indgående bilag** skal du vælge linjen for et bogført dokument, du vil knytte til en eksisterende indgående bilagspost og derefter vælge handlingen **Vælg indgående bilag**.
2. Vælg den indgående bilagspost, som du vil knytte til det bogførte fundne bilag, på siden **Indgående bilag**, og vælg derefter **OK**.
3. På siden **Bogførte bilag uden indgående bilag** er den valgte indgående bilagspost nu tilknyttet det bogførte bilag, som du kan se i faktaboksen **Indgående bilagsfiler**.

Hvis der ikke findes en relevant indgående bilagspost på siden **Indgående bilag** kan du oprette den. Du kan finde flere oplysninger i [Oprette indgående bilagsposter](across-how-create-income-document-records.md).

## <a name="see-related-microsoft-trainingtrainingmodulesincoming-documents-dynamics-365-business-central" />Se relateret [Microsoft-træning](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Oprette indkommende bilagsposter](across-how-create-income-document-records.md)
[Brug OCR til at omdanne PDF-og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md)
[Oprette indkommende bilagsposter direkte fra dokumenter og poster](across-how-connect-disconnect-income-document-records.md)
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
