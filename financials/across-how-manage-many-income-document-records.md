---
title: "Fremgangsmåde: Administrere mange indgående dokumentposter | Microsoft Docs"
description: "Fremgangsmåde: Oprette indgående dokumentposter"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 05/12/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 821efd8c95d05fc5d93c79dd75942f61daa91683
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-many-incoming-document-records"></a>Fremgangsmåde: Administrere mange indgående dokumentposter
Efterhånden som du opretter eller behandler indgående dokumentposter, kan antal linjer i vinduet **Indkommende dokumenter** vokse til et omfang, hvor du mister overblikket. Derfor kan du indstille indgående dokumentposter til Behandlet for at fjerne dem fra standardvisningen. Når du vælger handlingen **Vis alle**, kan du få vist både behandlede og ikke-behandlede poster.

**Bemærk**: Du kan ikke redigere oplysningerne, vedhæfte filer eller udføre andre processer på indgående dokumentposter, der er indstillet til Behandlet. Du skal først indstille dem til Ikke-behandlet.

Afkrydsningsfeltet **Behandlet** markeres automatisk på indgående dokumentposter, der er blevet behandlet, men du kan også markere eller fjerne markeringen i feltet manuelt. Afhængigt af din forretningsproces kan en indgående dokumentpost blive behandlet, når der er oprettet et relateret dokument til den, eller der er vedhæftet en fil.

**Bemærk**: Når du åbner vinduet **Indkommende dokumenter** med handlingen **Indkommende dokumenter** i Rollecenter, vises kun ikke-behandlede indgående dokumentposter som standard. I dette emne omtales det som "standardvisningen".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Sådan fjernes indgående dokumentposter fra standardvisningen
1. I feltet **Indkommende dokumenter** skal du vælge en eller flere linjer for indgående dokumentposter, du vil fjerne fra standardvinduet.
2. Vælg handlingen **Indstil til behandlet**.

Indgående dokumentposter fjernes fra standardvisningen og afkrydsningsfeltet **Behandlet** markeres på linjerne.

**Bemærk**: Du kan også udføre handlingen for den individuelle post i vinduet **Indgående bilagskort**.

## <a name="to-view-all-incoming-document-records"></a>Sådan vises alle indgående dokumentposter
1. I vinduet **Indgående dokumenter** skal du vælge handlingen **Vis alle**.

Alle indgående dokumentposter vises, herunder dem, hvor feltet **Behandlet** ikke er markeret.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Sådan føjes indgående dokumentposter til standardvisningen
1. I vinduet **Indgående dokumenter** skal du vælge handlingen **Vis alle**.
2. Vælg en eller flere linjer for indgående dokumentposter, der skal vises i standardvisningen.
3. Vælg handlingen **Indstil til ikke-behandlet**.  

**Bemærk**: Du kan også udføre handlingen for den individuelle post i vinduet **Indgående bilagskort**.

## <a name="see-also"></a>Se også
[Behandle indgående bilag](across-process-income-documents.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

