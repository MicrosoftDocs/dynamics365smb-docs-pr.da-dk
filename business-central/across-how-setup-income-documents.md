---
title: "Konfigurere indgående dokumenter | Microsoft Docs"
description: "Du kan bruge funktionen Indgående dokumenter til at oprette elektroniske dokumenter, administrere OCR-opgaver, indlæse fakturaer og konvertere billedfiler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: ea5673f341954960852de33cb94ee5722c8dbe26
ms.contentlocale: da-dk
ms.lasthandoff: 06/11/2018

---
# <a name="set-up-incoming-documents"></a>Konfigurere indgående bilag
Hvis du opretter finanskladdelinjer fra indgående dokumentposter, skal du i vinduet **Konfiguration af indkommende dokumenter** angive hvilken kladdetype og hvilket kladdenavn der skal bruges.

Hvis du ikke ønsker, at brugere kan oprette fakturaer eller finanskladdelinjer fra indgående dokumentposter, medmindre dokumenterne godkendes, skal du konfigurere godkendere i vinduet **Konfiguration af indkommende dokumenter**.

Hvis du vil aktivere PDF-og billedfiler til elektroniske dokumenter, som du kan konvertere til f.eks. købsfakturaer, skal du først definere OCR-funktionen og aktivere tjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Når funktionen Indkommende dokumenter er konfigureret, kan du bruge forskellige funktioner til at gennemgå udgiftsbilag, administrere OCR-opgaver og konvertere indgående dokumentfiler, manuelt eller automatisk, til de relevante købs- og salgsdokumenter eller kladdelinjer. Eksterne filer kan tilknyttes i enhver procesfase, herunder til bogførte dokumenter og til de derved oprettede kreditor-, debitor- og finansposter. Du kan finde flere oplysninger i [Behandle indgående bilag](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Sådan konfigureres funktionen for indgående dokumenter
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af indgående bilag**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Sådan konfigureres godkendere af indgående dokumentposter
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af indgående bilag**, og vælg derefter det relaterede link.  
2. I vinduet **Konfiguration af indkommende dokumenter** skal du vælge handlingen **Godkendere**.

    Vinduet **Godkendere af indgående bilag** viser alle brugere, der er angivet i [!INCLUDE[d365fin](includes/d365fin_md.md)].  
3. Vælg en eller flere brugere, der kan godkende et indgående dokument, før et relateret dokument eller en kladdelinje kan oprettes.

Når godkendere er konfigureret i vinduet **Godkendere af indgående dokumenter**, så er det kun disse brugere, der kan godkende et indgående dokument, hvis afkrydsningsfeltet **Kræv godkendelse for at oprette** er markeret i vinduet **Konfiguration af indkommende dokumenter**.

> [!NOTE]  
>   Denne godkenderopsætning er ikke relateret til godkendelsesworkflows. Du kan finde flere oplysninger under [Bruge godkendelsesworkflows](across-how-use-approval-workflows.md).

## <a name="to-set-up-an-ocr-service"></a>Sådan konfigureres en OCR-tjeneste
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af indgående bilag**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Dine logondata krypteres automatisk.

## <a name="see-also"></a>Se også
[Behandle indgående bilag](across-process-income-documents.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

