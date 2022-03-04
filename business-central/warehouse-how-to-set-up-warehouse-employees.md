---
title: Definere lagermedarbejdere
description: Hver bruger, som udfører lageraktiviteter, skal være defineret som en lagermedarbejder, der er tildelt én standardlokation og evt. flere ikke-standardlokationer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7328, 7348
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 668b34e011ec103689b45bdc864a7e726d4d8082
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141921"
---
# <a name="set-up-warehouse-employees"></a>Definere lagermedarbejdere

Hver bruger, som udfører lageraktiviteter, skal være defineret som en lagermedarbejder, der er tildelt én standardlokation og evt. flere ikke-standardlokationer. Denne brugeropsætning filtrerer alle lageraktiviteter på tværs af databasen til medarbejderens lokation, så medarbejderen kun kan udføre lageraktiviteterne på standardlokationen. En bruger kan være tildelt yderligere ikke-standard-lokationer, som medarbejderen kan få vist aktivitetslinjer for men ikke udføre aktiviteterne.

## <a name="to-set-up-warehouse-employees"></a>Sådan defineres lagermedarbejdere  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Vælg feltet **Bruger-ID**, og vælg derefter brugeren, der skal tilføjes som lagermedarbejder. Vælg knappen **OK**.  
4. Angiv i feltet **Lokationskode** koden for den lokation, hvor brugeren skal arbejde.  
5. Marker afkrydsningsfeltet **Standard** for at definere lokationen som den eneste lokation, hvor medarbejderen kan udføre lageraktiviteter.  
6. Gentag disse trin for at tildele andre medarbejdere til lokationer eller for at tildele ikke-standardlokationer til eksisterende lagermedarbejdere.  

## <a name="see-also"></a>Se også

[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Konfigurere Warehouse Management](warehouse-setup-warehouse.md) 
[Montagestyring](assembly-assemble-items.md)
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]