---
title: Konfigurere indgående bilag
description: 'Konfigurere Indgående bilag til at oprette elektroniske dokumenter, administrere OCR-opgaver, indlæse fakturaer og konvertere billedfiler.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="set-up-incoming-documents" />Konfigurere indgående bilag

Hvis du opretter finanskladdelinjer fra indgående bilagsposter, skal du på siden **Konfiguration af indgående bilag** angive hvilken kladdetype og hvilket kladdenavn der skal bruges.

Når funktionen **Indgående bilag** er konfigureret, kan du bruge forskellige funktioner til at gennemgå udgiftsbilag, administrere OCR-opgaver og konvertere indgående bilagsfiler, manuelt eller automatisk, til de relevante købs- og salgsbilag eller kladdelinjer. Eksterne filer kan tilknyttes i enhver procesfase, herunder til bogførte dokumenter og til de derved oprettede kreditor-, debitor- og finansposter. Du kan finde flere oplysninger i [Oprette indgående bilagsposter](across-how-create-income-document-records.md).

## <a name="to-set-up-the-incoming-documents-feature" />Sådan konfigureres funktionen for indgående bilag

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfiguration af indkommende dokumenter**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Som en del af konfigurationen skal du beslutte, om du vil kræve godkendelse af indgående dokumenter. Hvis du vil kræve godkendelse, skal du [oprette godkendere og godkendelsesworkflow](#to-set-up-approvers-of-incoming-document-records). Hvis din organisation ikke ønsker at kræve godkendelse, kan du springe den næste sektion over.

Hvis du bruger en OCR-tjeneste til at konvertere PDF- eller billedfiler, der repræsenterer indgående dokumenter, [skal du konfigurere den](#to-set-up-an-ocr-service). Ellers kan du også ignorere denne sektion.

## <a name="to-set-up-approvers-of-incoming-document-records" />Sådan konfigureres godkendere af indgående bilagsposter

Hvis du ikke ønsker, at brugere kan oprette fakturaer eller finanskladdelinjer fra indgående dokumentposter, medmindre dokumenterne godkendes, skal du konfigurere en godkendelsesproces til indkommende bilag. Godkendere af indgående bilag skal konfigureres som brugere i godkendelsesworkflow.

Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen. På siden **Konfiguration af godkendelsesbruger** skal du også angive beløbsgrænser for bestemte typer anmodninger og angive stedfortrædende godkendere, som godkendelsesanmodninger skal uddelegeres til, når den oprindelige godkender er fraværende. Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)

## <a name="to-set-up-an-ocr-service" />Sådan konfigureres en OCR-tjeneste

Hvis du vil ændre PDF-og billedfiler til elektroniske dokumenter, som du kan konvertere til fakturaer, kreditnotaer eller kladdelinjer, skal du angive OCR-funktionen. Du kan også oprette poster manuelt, så de repræsenterer eksterne dokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfiguration af OCR-service** og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Dine logondata krypteres automatisk.

Du kan finde flere oplysninger i [Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-related-microsoft-training" />Se relateret [Microsoft-træning](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
