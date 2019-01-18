---
title: Konfigurere kontoplanen
description: "Du kan ændre standardkontiene i kontoplanen, og du kan tilføje nye konti."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 9ed8bc069fc702a1b2d8d893531baca5eab7a903
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Konfigurere eller ændre kontoplanen
Kontoplanen viser de finanskonti, hvor dine finansielle data er gemt. [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en standardkontoplan, der er klar til at understøtte din virksomhed.
Men du kan ændre standardkontiene, og du kan tilføje nye konti.  

## <a name="adding-or-changing-accounts"></a>Tilføjelse eller ændring af konti
Fra kontoplanen kan du åbne hver finanskonto og tilføje eller ændre indstillinger for hver konto.

> [!NOTE]  
>   Du kan slette en finanskonto. Men før du sletter den, skal følgende være opfyldt:  

* Saldoen på kontoen skal være nul.  
* Feltet **Tillad sletning af finanskonti før** skal være indstillet på siden **Opsætning af Finans**, og der må ikke bogføres poster på kontoen på eller efter den pågældende dato.  
* Hvis feltet **Kontroller brug af finanskonto** på siden **Opsætning af Finans** er markeret, må kontoen ikke bruges i nogen bogføringsgrupper eller bogføringsopsætning.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] forhindrer, at du kan slette en finanskonto, der indeholder data, der skal bruges i kontoplanen.  

## <a name="see-also"></a>Se også
[Finans- og kontoplanen](finance-general-ledger.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Import af data fra andre økonomisystemer](across-import-data-configuration-packages.md)(across-import-data-configuration-packages.md)  
[Arbejde med kontoskemaer](bi-how-work-account-schedule.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

