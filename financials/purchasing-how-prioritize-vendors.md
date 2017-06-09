---
title: "Fremgangsmåde: Prioritere kreditorer | Microsoft Docs"
description: "Fremgangsmåde: Prioritere kreditorer"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ae80ae9ecc15838b59999ded775c7fa0063c8a54
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-prioritize-vendors"></a>Fremgangsmåde: Prioritere kreditorer
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan foreslå forskellige betalinger til kreditorer. Det kan f.eks. være betalinger, som snart forfalder, eller som omfatter rabat. Du kan finde flere oplysninger i [Fremgangsmåde: Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).

Du skal først at prioritere dine kreditorer ved at tildele numre til dem.

## <a name="to-prioritize-vendors"></a>Sådan prioriterer du kreditorer
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Kreditorer** og derefter vælge det relaterede link.
2. Vælg den relevante kreditor, og vælg derefter **Rediger**.
3. Angiv et nummer i feltet **Prioritet**.

[!INCLUDE[d365fin](includes/d365fin_md.md)] betragter det laveste nummer, bortset fra 0, som den højeste prioritet. Bruger du f.eks. 1, 2 og 3, har 1 den højeste prioritet.

Hvis der er en kreditor, du ikke vil tildele prioritet, skal du lade feltet **Prioritet** stå tomt. Hvis du bruger betalingsforslag figurerer den pågældende kreditor i så fald efter alle andre kreditorer, som har et prioritetstal. Der er ingen begrænsninger på, hvor mange prioritetsniveauer du kan angive.

## <a name="see-also"></a>Se også
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

