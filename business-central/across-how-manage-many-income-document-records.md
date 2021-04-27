---
title: Angive, hvilke indgående bilag der skal vises | Microsoft Docs
description: Tilpas standardvisningen af indgående bilag, f.eks. e-fakturaer, for at forbedre din oversigt over behandlede og ikke-behandlede poster.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 69c807a9c99b105782240c43d096a73ff01e2664
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775968"
---
# <a name="manage-many-incoming-document-records"></a>Administrere mange indgående bilagsposter
Efterhånden som du opretter eller behandler indgående bilagsposter, kan antal linjer på siden **Indgående bilag** vokse til et omfang, hvor du mister overblikket. Derfor kan du indstille indgående bilagsposter til Behandlet for at fjerne dem fra standardvisningen. Når du vælger handlingen **Vis alle**, kan du få vist både behandlede og ikke-behandlede poster.

> [!NOTE]  
>   Du kan ikke redigere oplysningerne, vedhæfte filer eller udføre andre processer på indgående bilagsposter, der er indstillet til Behandlet. Du skal først indstille dem til Ikke-behandlet.

Afkrydsningsfeltet **Behandlet** markeres automatisk på indgående bilagsposter, der er blevet behandlet, men du kan også markere eller fjerne markeringen i feltet manuelt. Afhængigt af din forretningsproces kan en indgående bilagspost blive behandlet, når der er oprettet et relateret bilag til den, eller der er vedhæftet en fil.

> [!NOTE]  
>   Når du åbner siden **Indgående bilag** med handlingen **Indgående bilag** i Rollecenter, vises kun ikke-behandlede indgående bilagsposter som standard. I dette emne omtales det som "standardvisningen".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Sådan fjernes indgående bilagsposter fra standardvisningen
1. På siden **Indgående bilag** skal du vælge en eller flere linjer for indgående bilagsposter, du vil fjerne fra standardvinduet.
2. Vælg handlingen **Indstil til behandlet**.

    Indgående bilagsposter fjernes fra standardvisningen og afkrydsningsfeltet **Behandlet** markeres på linjerne.

> [!NOTE]  
>   Du kan også udføre handlingen for den individuelle post på siden **Indgående bilagskort**.

## <a name="to-view-all-incoming-document-records"></a>Sådan vises alle indgående bilagsposter
1. På siden **Indgående bilag** skal du vælge handlingen **Vis alle**.

Alle indgående bilagsposter vises, herunder dem, hvor feltet **Behandlet** ikke er markeret.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Sådan føjes indgående bilagsposter til standardvisningen
1. På siden **Indgående bilag** skal du vælge handlingen **Vis alle**.
2. Vælg en eller flere linjer for indgående bilagsposter, der skal vises i standardvisningen.
3. Vælg handlingen **Indstil til ikke-behandlet**.  

> [!NOTE]  
>   Du kan også udføre handlingen for den individuelle post på siden **Indgående bilagskort**.

## <a name="see-also"></a>Se også
[Behandle indgående bilag](across-process-income-documents.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]