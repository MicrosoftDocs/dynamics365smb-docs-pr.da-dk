---
title: Oprette indgående bilagsposter fra Docs
description: Du kan gemme eksterne forretningsbilag ved at knytte dokumentfilerne til de relaterede indgående bilagsposter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 5bad6c920cc285dd7fb405b8075263229df778d1
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519914"
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries"></a>Oprette indgående bilagsposter direkte fra bilag og poster
Du kan gemme eksterne forretningsbilag i [!INCLUDE[prod_short](includes/prod_short.md)] ved at knytte dokumentfilerne til de relaterede indgående bilagsposter. Hvis dokumentet, f.eks en købsfaktura, ikke startede som en indgående bilagspost, kan du stadig oprette og knytte en indgående bilagspost til det senere. Du kan også tilknytte indgående bilagsfiler til bogførte købs- og salgsdokumenter og til kreditor-, debitor- og finansposter ved hjælp af faktaboksen **Indgående bilagsfiler** f.eks. på siderne **Bogf. købsfakturaer** og **Kreditorposter**.

Fra på siderne **Kontoplan** og **Finansposter** kan du bruge en søgefunktionen til at finde finansposter for bogførte og købs- og salgsdokumenter, som ikke har indgående bilagsposter og derefter knytte centralt til eksisterende poster eller oprette nye med vedhæftede bilagsfiler. Du kan finde flere oplysninger i [Finde bogførte bilag uden indgående bilagsposter](across-how-find-posted-documents-without-income-document-records.md).

Følgende procedurer viser, hvordan du vedhæfter en fil til en eksisterende købsfaktura, der ikke er oprettet fra en indgående bilagspost, og vedhæfter en fil til en kreditorpost. Vedhæftning af en fil til bogførte købs- eller salgsdokumenter fungerer på samme måde.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Sådan oprettes og tilknyttes en indgående bilagspost fra en indkøbsfaktura
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.
2. Vælg linjen for en købsfaktura, du vil knytte til en fil, og vælg derefter handlingen **Opret indgående bilag ud fra fil**.
3. Du kan også vælge linjen for en købsfaktura, du vil knytte til en fil, og derefter vælge handlingen **Vedhæft fil**.
4. På siden **Indsæt fil** , skal du vælge den fil, der repræsenterer det pågældende indgående bilag og derefter vælge knappen **Åbn**.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Sådan oprettes og tilknyttes en indgående bilagspost fra en kreditorpost
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Kreditorposter** i feltet Søg, og vælg derefter det relaterede link.
2. Vælg linjen for en kreditorpost, du vil knytte til en fil, og vælg derefter handlingen **Opret indgående bilag ud fra fil**.
3. Du kan også vælge en linje for en kreditorpost, du vil knytte til en fil, og derefter vælge handlingen **Vedhæft fil**.
4. På siden **Indsæt fil** , skal du vælge den fil, der repræsenterer det pågældende indgående bilag og derefter vælge knappen **Åbn**.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>Fjerne en forbindelse fra et indgående bilag til et bogført bilag
Du kan fjerne vedhæftede filer fra ikke-bogførte bilag til enhver tid ved at slette den relaterede indgående bilagspost. Hvis dokumentet er bogført, skal du først fjerne forbindelsen fra den indgående bilagspost.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Indgående bilag** og derefter vælge det relaterede link.
2. Vælg linjen for en indgående bilagspost, der er knyttet til et bogført bilag, du vil slette, og vælg derefter handlingen **Fjern reference til post**.

Forbindelsen til det bogførte bilag er fjernet. Du kan nu fortsætte med at knytte en andet indgående bilagspost til det bogførte bilag som beskrevet i dette emne.

## <a name="see-also"></a>Se også
[Behandle indgående bilag](across-process-income-documents.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]