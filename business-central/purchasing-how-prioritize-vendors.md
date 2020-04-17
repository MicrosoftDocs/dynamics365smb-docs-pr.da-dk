---
title: Angive et prioritetsniveau for en kreditor | Microsoft Docs
description: Du kan tildele numre til kreditorer eller leverandører for at prioritere dem og lette betalingsforslag i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: cede9a43bb66d314640e0e28443c63c925fd575a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192719"
---
# <a name="prioritize-vendors"></a>Tildele kreditorer prioritet
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan foreslå forskellige betalinger til kreditorer. Det kan f.eks. være betalinger, som snart forfalder, eller som omfatter rabat. Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).

Du skal først at prioritere dine kreditorer ved at tildele numre til dem.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a>Sådan tildeler du kreditorer prioritet
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leverandører (Kreditorer)**, og vælg derefter det relaterede link.
2. Vælg den relevante kreditor, og vælg derefter **Rediger**.
3. Angiv et nummer i feltet **Prioritet**.

[!INCLUDE[d365fin](includes/d365fin_md.md)] betragter det laveste nummer, bortset fra 0, som den højeste prioritet. Bruger du f.eks. 1, 2 og 3, har 1 den højeste prioritet.

Hvis der er en kreditor, du ikke vil tildele prioritet, skal du lade feltet **Prioritet** stå tomt. Hvis du bruger betalingsforslag figurerer den pågældende kreditor i så fald efter alle andre kreditorer, som har et prioritetstal. Der er ingen begrænsninger på, hvor mange prioritetsniveauer du kan angive.

## <a name="see-also"></a>Se også
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
