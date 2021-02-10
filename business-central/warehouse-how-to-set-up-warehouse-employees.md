---
title: Sådan defineres lagermedarbejdere | Microsoft Docs
description: Hver bruger, som udfører lageraktiviteter, skal være defineret som en lagermedarbejder, der er tildelt én standardlokation og evt. flere ikke-standardlokationer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7ebb81abd7e16e0c4aaa3f7cd52ab1b6f1a664c3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755915"
---
# <a name="set-up-warehouse-employees"></a>Definere lagermedarbejdere
Hver bruger, som udfører lageraktiviteter, skal være defineret som en lagermedarbejder, der er tildelt én standardlokation og evt. flere ikke-standardlokationer. Denne brugeropsætning filtrerer alle lageraktiviteter på tværs af databasen til medarbejderens lokation, så medarbejderen kun kan udføre lageraktiviteterne på standardlokationen. En bruger kan være tildelt yderligere ikke-standard-lokationer, som medarbejderen kan få vist aktivitetslinjer for men ikke udføre aktiviteterne.

## <a name="to-set-up-warehouse-employees"></a>Sådan defineres lagermedarbejdere  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Vælg feltet **Bruger-ID**, og vælg derefter brugeren, der skal tilføjes som lagermedarbejder. Vælg knappen **OK**.  
6.  Angiv i feltet **Lokationskode** koden for den lokation, hvor brugeren skal arbejde.  
7.  Marker afkrydsningsfeltet **Standard** for at definere lokationen som den eneste lokation, hvor medarbejderen kan udføre lageraktiviteter.  
8.  Gentag disse trin for at tildele andre medarbejdere til lokationer eller for at tildele ikke-standardlokationer til eksisterende lagermedarbejdere.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
