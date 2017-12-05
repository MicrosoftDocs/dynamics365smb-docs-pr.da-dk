---
title: "Angive, hvilke indgående dokumenter der skal vises | Microsoft Docs"
description: "Tilpas standardvisningen af indgående dokumenter, f.eks. e-fakturaer, for at forbedre din oversigt over behandlede og ikke-behandlede poster."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2016
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 99f4ec1b3b02ec88bc10fd21988af8e6683867cb
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-manage-many-incoming-document-records"></a>Fremgangsmåde: Administrere mange indgående dokumentposter
Efterhånden som du opretter eller behandler indgående dokumentposter, kan antal linjer i vinduet **Indkommende dokumenter** vokse til et omfang, hvor du mister overblikket. Derfor kan du indstille indgående dokumentposter til Behandlet for at fjerne dem fra standardvisningen. Når du vælger handlingen **Vis alle**, kan du få vist både behandlede og ikke-behandlede poster.

> [!NOTE]  
>   Du kan ikke redigere oplysningerne, vedhæfte filer eller udføre andre processer på indgående dokumentposter, der er indstillet til Behandlet. Du skal først indstille dem til Ikke-behandlet.

Afkrydsningsfeltet **Behandlet** markeres automatisk på indgående dokumentposter, der er blevet behandlet, men du kan også markere eller fjerne markeringen i feltet manuelt. Afhængigt af din forretningsproces kan en indgående dokumentpost blive behandlet, når der er oprettet et relateret dokument til den, eller der er vedhæftet en fil.

> [!NOTE]  
>   Når du åbner vinduet **Indkommende dokumenter** med handlingen **Indkommende dokumenter** i Rollecenter, vises kun ikke-behandlede indgående dokumentposter som standard. I dette emne omtales det som "standardvisningen".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Sådan fjernes indgående dokumentposter fra standardvisningen
1. I feltet **Indkommende dokumenter** skal du vælge en eller flere linjer for indgående dokumentposter, du vil fjerne fra standardvinduet.
2. Vælg handlingen **Indstil til behandlet**.

    Indgående dokumentposter fjernes fra standardvisningen og afkrydsningsfeltet **Behandlet** markeres på linjerne.

> [!NOTE]  
>   Du kan også udføre handlingen for den individuelle post i vinduet **Indgående bilagskort**.

## <a name="to-view-all-incoming-document-records"></a>Sådan vises alle indgående dokumentposter
1. I vinduet **Indgående dokumenter** skal du vælge handlingen **Vis alle**.

Alle indgående dokumentposter vises, herunder dem, hvor feltet **Behandlet** ikke er markeret.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Sådan føjes indgående dokumentposter til standardvisningen
1. I vinduet **Indgående dokumenter** skal du vælge handlingen **Vis alle**.
2. Vælg en eller flere linjer for indgående dokumentposter, der skal vises i standardvisningen.
3. Vælg handlingen **Indstil til ikke-behandlet**.  

> [!NOTE]  
>   Du kan også udføre handlingen for den individuelle post i vinduet **Indgående bilagskort**.

## <a name="see-also"></a>Se også
[Behandle indgående bilag](across-process-income-documents.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

