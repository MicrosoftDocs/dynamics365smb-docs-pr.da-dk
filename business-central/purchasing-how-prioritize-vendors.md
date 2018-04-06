---
title: Angive et prioritetsniveau for en kreditor | Microsoft Docs
description: "Du kan tildele numre til kreditorer eller leverandører for at prioritere dem og lette betalingsforslag i Business Central."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f7834f0f99b775125425eb7209c3c648de4ccd1f
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="prioritize-vendors"></a>Tildele kreditorer prioritet
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan foreslå forskellige betalinger til kreditorer. Det kan f.eks. være betalinger, som snart forfalder, eller som omfatter rabat. Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).

Du skal først at prioritere dine kreditorer ved at tildele numre til dem.

## <a name="to-prioritize-vendors"></a>Sådan tildeler du kreditorer prioritet
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Vælg den relevante kreditor, og vælg derefter **Rediger**.
3. Angiv et nummer i feltet **Prioritet**.

[!INCLUDE[d365fin](includes/d365fin_md.md)] betragter det laveste nummer, bortset fra 0, som den højeste prioritet. Bruger du f.eks. 1, 2 og 3, har 1 den højeste prioritet.

Hvis der er en kreditor, du ikke vil tildele prioritet, skal du lade feltet **Prioritet** stå tomt. Hvis du bruger betalingsforslag figurerer den pågældende kreditor i så fald efter alle andre kreditorer, som har et prioritetstal. Der er ingen begrænsninger på, hvor mange prioritetsniveauer du kan angive.

## <a name="see-also"></a>Se også
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

