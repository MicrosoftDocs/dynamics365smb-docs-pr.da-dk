---
title: Oprette indgående dokumenter fra dokumenter | Microsoft Docs
description: Du kan oprette poster for indgående dokumenter, f.eks. e-fakturaer, og administrere OCR-opgaver eCommerce og dokumentudveksling.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 662395d9085588d145499a77dd9113b2fd341af7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300469"
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries"></a>Oprette indgående dokumentposter direkte fra dokumenter og poster
Du kan gemme eksterne forretningsbilag i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at knytte dokumentfilerne til de relaterede indgående dokumentposter. Hvis dokumentet, f.eks en købsfaktura ikke startede som en indgående dokumentpost, kan du stadig oprette og knytte en indgående dokumentpost til det senere. Du kan også tilknytte indgående bilagsfiler til bogførte købs- og salgsdokumenter og til kreditor-, debitor- og finansposter ved hjælp af faktaboksen **Indgående dokumentfiler** f.eks. på siderne **Bogf. købsfakturaer** og **Kreditorposter**.

Fra på siderne **Kontoplan** og **Finansposter** kan du bruge en søgefunktionen til at finde finansposter for bogførte og købs- og salgsdokumenter, som ikke har indgående dokument poster og derefter knytte centralt til eksisterende poster eller oprette nye med vedhæftede dokument filer. Du kan finde flere oplysninger under [Finde bogførte dokumenter uden indgående dokumentposter](across-how-find-posted-documents-without-income-document-records.md).

Følgende procedurer viser, hvordan du vedhæfter en fil til en eksisterende købsfaktura, der ikke er oprettet fra en indgående dokumentpost, og vedhæfter en fil til en kreditorpost. Vedhæftning af en fil til bogførte købs- eller salgsdokumenter fungerer på samme måde.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Sådan oprettes og tilknyttes en indgående dokumentpost fra en indkøbsfaktura
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.
2. Vælg linjen for en købsfaktura, du vil knytte til en fil, og vælg derefter handlingen **Opret indgående bilag ud fra fil**.
3. Du kan også vælge linjen for en købsfaktura, du vil knytte til en fil, og derefter vælge handlingen **Vedhæft fil**.
4. På siden **Indsæt fil** , skal du vælge den fil, der repræsenterer det pågældende indgående dokument og derefter vælge knappen **Åbn**.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Sådan oprettes og tilknyttes en indgående dokumentpost fra en kreditorpost
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kreditorposter**, og vælg derefter det relaterede link.
2. Vælg linjen for en kreditorpost, du vil knytte til en fil, og vælg derefter handlingen **Opret indgående bilag ud fra fil**.
3. Du kan også vælge en linje for en kreditorpost, du vil knytte til en fil, og derefter vælge handlingen **Vedhæft fil**.
4. På siden **Indsæt fil** , skal du vælge den fil, der repræsenterer det pågældende indgående dokument og derefter vælge knappen **Åbn**.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>Fjerne en forbindelse fra en indgående dokument til et bogført dokument
Du kan fjerne vedhæftede filer fra ikke-bogførte dokumenter til enhver tid ved at slette den relaterede indgående dokument post. Hvis dokumentet er bogført, skal du først fjerne forbindelsen fra den indgående dokument post.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Indgående bilag**, og vælg derefter det relaterede link.
2. Vælg linjen for en indgående dokumentpost, der er knyttet til et bogført dokument, du vil slette, og vælg derefter handlingen **Fjern reference til post**.

Forbindelsen til det bogførte dokument er fjernet. Du kan nu fortsætte med at knytte et andet indgående dokument post til det bogførte dokument som beskrevet i dette emne.

## <a name="see-also"></a>Se også
[Behandle indgående bilag](across-process-income-documents.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
