---
title: Angive et prioritetsniveau for en kreditor (indeholder video) | Microsoft Docs
description: Du kan tildele numre til kreditorer eller leverandører for at prioritere dem og lette betalingsforslag i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7e68c56422f4f3de33006297ec396fdd34169e8d
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940047"
---
# <a name="prioritize-vendors"></a>Tildele kreditorer prioritet
[!INCLUDE[prod_short](includes/prod_short.md)] kan foreslå forskellige betalinger til kreditorer. Det kan f.eks. være betalinger, som snart forfalder, eller som omfatter rabat. Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).

Du skal først at prioritere dine kreditorer ved at tildele numre til dem.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a>Sådan tildeler du kreditorer prioritet
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link.
2. Vælg den relevante kreditor, og vælg derefter **Rediger**.
3. Angiv et nummer i feltet **Prioritet**.

[!INCLUDE[prod_short](includes/prod_short.md)] betragter det laveste nummer, bortset fra 0, som den højeste prioritet. Bruger du f.eks. 1, 2 og 3, har 1 den højeste prioritet.

Hvis der er en kreditor, du ikke vil tildele prioritet, skal du lade feltet **Prioritet** stå tomt. Hvis du bruger betalingsforslag figurerer den pågældende kreditor i så fald efter alle andre kreditorer, som har et prioritetstal. Der er ingen begrænsninger på, hvor mange prioritetsniveauer du kan angive.

## <a name="see-also"></a>Se også
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]