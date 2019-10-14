---
title: Angive, hvilke indgående dokumenter der skal vises | Microsoft Docs
description: Tilpas standardvisningen af indgående dokumenter, f.eks. e-fakturaer, for at forbedre din oversigt over behandlede og ikke-behandlede poster.
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
ms.openlocfilehash: 5401b8049e13d594f3429c97cfff915fc944c733
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305568"
---
# <a name="manage-many-incoming-document-records"></a>Administrere mange indgående dokumentposter
Efterhånden som du opretter eller behandler indgående dokumentposter, kan antal linjer på siden **Indkommende dokumenter** vokse til et omfang, hvor du mister overblikket. Derfor kan du indstille indgående dokumentposter til Behandlet for at fjerne dem fra standardvisningen. Når du vælger handlingen **Vis alle**, kan du få vist både behandlede og ikke-behandlede poster.

> [!NOTE]  
>   Du kan ikke redigere oplysningerne, vedhæfte filer eller udføre andre processer på indgående dokumentposter, der er indstillet til Behandlet. Du skal først indstille dem til Ikke-behandlet.

Afkrydsningsfeltet **Behandlet** markeres automatisk på indgående dokumentposter, der er blevet behandlet, men du kan også markere eller fjerne markeringen i feltet manuelt. Afhængigt af din forretningsproces kan en indgående dokumentpost blive behandlet, når der er oprettet et relateret dokument til den, eller der er vedhæftet en fil.

> [!NOTE]  
>   Når du åbner siden **Indkommende dokumenter** med handlingen **Indkommende dokumenter** i Rollecenter, vises kun ikke-behandlede indgående dokumentposter som standard. I dette emne omtales det som "standardvisningen".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Sådan fjernes indgående dokumentposter fra standardvisningen
1. På siden **Indkommende dokumenter** skal du vælge en eller flere linjer for indgående dokumentposter, du vil fjerne fra standardvinduet.
2. Vælg handlingen **Indstil til behandlet**.

    Indgående dokumentposter fjernes fra standardvisningen og afkrydsningsfeltet **Behandlet** markeres på linjerne.

> [!NOTE]  
>   Du kan også udføre handlingen for den individuelle post på siden **Indgående bilagskort**.

## <a name="to-view-all-incoming-document-records"></a>Sådan vises alle indgående dokumentposter
1. På siden **Indgående dokumenter** skal du vælge handlingen **Vis alle**.

Alle indgående dokumentposter vises, herunder dem, hvor feltet **Behandlet** ikke er markeret.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Sådan føjes indgående dokumentposter til standardvisningen
1. På siden **Indgående dokumenter** skal du vælge handlingen **Vis alle**.
2. Vælg en eller flere linjer for indgående dokumentposter, der skal vises i standardvisningen.
3. Vælg handlingen **Indstil til ikke-behandlet**.  

> [!NOTE]  
>   Du kan også udføre handlingen for den individuelle post på siden **Indgående bilagskort**.

## <a name="see-also"></a>Se også
[Behandle indgående bilag](across-process-income-documents.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
