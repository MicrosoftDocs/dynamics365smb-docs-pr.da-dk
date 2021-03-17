---
title: Konfigurere indgående bilag | Microsoft Docs
description: Du kan bruge funktionen Indgående bilag til at oprette elektroniske dokumenter, administrere OCR-opgaver, indlæse fakturaer og konvertere billedfiler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 00bfa89376a361bedc71ba76630906d761989ead
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384595"
---
# <a name="set-up-incoming-documents"></a>Konfigurere indgående bilag

Hvis du opretter finanskladdelinjer fra indgående bilagsposter, skal du på siden **Konfiguration af indgående bilag** angive hvilken kladdetype og hvilket kladdenavn der skal bruges.

Hvis du ikke ønsker, at brugere kan oprette fakturaer eller finanskladdelinjer fra indgående bilagsposter, medmindre bilagene først er godkendt, skal du konfigurere workflowgodkendere.

Hvis du vil aktivere PDF-og billedfiler til elektroniske dokumenter, som du kan konvertere til f.eks. købsfakturaer, skal du først definere OCR-funktionen og aktivere tjenesten i [!INCLUDE[prod_short](includes/prod_short.md)]. Vælg en servicepakke, der passer til din organisation og/eller dit land/område. Du kan også oprette poster manuelt, så de repræsenterer eksterne dokumenter.  

Når funktionen Indgående bilag er konfigureret, kan du bruge forskellige funktioner til at gennemgå udgiftsbilag, administrere OCR-opgaver og konvertere indgående bilagsfiler, manuelt eller automatisk, til de relevante købs- og salgsbilag eller kladdelinjer. Eksterne filer kan tilknyttes i enhver procesfase, herunder til bogførte dokumenter og til de derved oprettede kreditor-, debitor- og finansposter. Du kan finde flere oplysninger i [Behandle indgående bilag](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Sådan konfigureres funktionen for indgående bilag

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning for indgående bilag**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Som en del af konfigurationen skal du beslutte, om du vil kræve godkendelse af indgående dokumenter. Hvis du vil kræve godkendelse, skal du oprette godkendere og godkendelsesworkflow. Hvis din organisation ikke ønsker at kræve godkendelse, kan du springe den næste sektion over.  

Hvis du bruger en tjeneste til at konvertere PDF- eller billedfiler, der repræsenterer indgående dokumenter, skal du konfigurere den. Ellers kan du også ignorere denne sektion.  

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Sådan konfigureres godkendere af indgående bilagsposter

Du kan også vælge at oprette en godkendelsesproces for de indgående dokumenter. Godkendere af indgående bilag skal konfigureres som brugere i godkendelsesworkflow.

Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen. På siden **Konfiguration af godkendelsesbruger** skal du også angive beløbsgrænser for bestemte typer anmodninger og angive stedfortrædende godkendere, som godkendelsesanmodninger skal uddelegeres til, når den oprindelige godkender er fraværende. Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)

## <a name="to-set-up-an-ocr-service"></a>Sådan konfigureres en OCR-tjeneste

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af OCR-tjeneste**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Dine logondata krypteres automatisk.

Du kan finde flere oplysninger i [Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-also"></a>Se også

[Behandle indgående bilag](across-process-income-documents.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]