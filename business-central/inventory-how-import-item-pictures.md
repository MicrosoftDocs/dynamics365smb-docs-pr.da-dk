---
title: Importere mange varebilleder fra en zip-fil
description: Du kan importere flere varebilleder svarende til dine varenumre ved at komprimere dem til en zip-fil, og benyt siden Importer varebilleder for at styre, hvilke varebilleder, der skal importeres.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.search.form: 30, 461
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 5a43d696eab27a72c9f9b3c224d08feb9e99ccf4
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059670"
---
# <a name="import-multiple-item-pictures"></a>Importer flere varebilleder
Du kan importere flere varebilleder på en gang. Navngiv blot dine billedfiler svarende til dine varenumre, komprimer dem til en zip-fil, og benyt siden Importer varebilleder for at styre, hvilke varebilleder, der skal importeres.

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
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af Lager**, og vælg derefter det relaterede link.
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
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]