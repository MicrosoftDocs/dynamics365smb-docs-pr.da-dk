---
title: Import af mange varebilleder fra en zip-fil | Microsoft Docs
description: Du kan importere flere varebilleder på en gang. Navngiv blot dine billedfiler svarende til dine varenumre, komprimer dem til en zip-fil, og benyt siden Importer varebilleder for at styre, hvilke varebilleder, der skal importeres.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fa859d3e350cedb845df47521ee58ba8d2e4aade
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243062"
---
# <a name="import-multiple-item-pictures"></a>Importer flere varebilleder
Du kan importere flere varebilleder på en gang. Navngiv blot dine billedfiler svarende til dine varenumre, komprimer dem til en zip-fil, og benyt siden **Importer varebilleder** for at styre, hvilke varebilleder, der skal importeres.

Alle standardfilformater er understøttet.

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a>Navngivning af billedfiler efter varenavne og klargøring af zip-filen
1. Navngiv hver fil i henhold til den pågældende vares nummer på lokationen, hvor du dine varebilleder er gemt. Eksempler:

    |Varenr.|Filnavn|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Saml alle filerne i en zip-fil. F.eks.: I Windows Explorer vælger du filerne, og derefter vælger du **Send til**, **Komprimeret (zipped) mappe**.     

## <a name="to-import-item-pictures"></a>Importer varebilleder
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af Lager**, og vælg derefter det relaterede link.
2. Vælg handlingen **Importer billeder**.
3. Find feltet **Vælg en zip-fil**, vælg den relevante zip-mappe, og vælg dernæst knappen **Åbn**.

    Der oprettes en linje for hver vare og billede på siden **Importer varebilleder**.

    > [!NOTE]
    > For varekort, der allerede har et billede, vælges afkrydsningsfeltet **Billede findes allerede**. Hvis du ikke ønsker, at eksisterende billeder erstattes, fravælges afkrydsningsfeltet **Erstat billeder**. Hvis du ikke ønsker, at individuelle eksisterende billeder erstattes, skal du slette de pågældende linjer.

3. Vælg handlingen **Importer billeder**.

Feltet **Importstatus** opdateres for at vise, om billedimporten blev annulleret eller gennemført.       

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Oprette nummerserie](ui-create-number-series.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)