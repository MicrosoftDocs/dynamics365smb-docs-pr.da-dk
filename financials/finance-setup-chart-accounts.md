---
title: Konfigurere kontoplanen | Microsoft Docs
description: "Du kan ændre standardkontiene i kontoplanen, og du kan tilføje nye konti."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 69d4a8d4482999ed9d622d73654c3d8a4c3d8394
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Konfigurere eller ændre kontoplanen
Kontoplanen viser de finanskonti, hvor dine finansielle data er gemt. [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] indeholder en standardkontoplan, der er klar til at understøtte din virksomhed.
Men du kan ændre standardkontiene, og du kan tilføje nye konti.  

## <a name="adding-or-changing-accounts"></a>Tilføjelse eller ændring af konti
Fra kontoplanen kan du åbne hver finanskonto og tilføje eller ændre indstillinger for hver konto.

> [!NOTE]  
>   Du kan slette en finanskonto. Men før du sletter den, skal følgende være opfyldt:  

* Saldoen på kontoen skal være nul.  
* Feltet **Tillad sletning af finanskonti før** skal være indstillet i vinduet **Regnskabsopsætning**, og der må ikke bogføres poster på kontoen på eller efter den pågældende dato.  
* Hvis feltet **Kontroller brug af finanskonto** i vinduet **Regnskabsopsætning** er markeret, må kontoen ikke bruges i nogen bogføringsgrupper eller bogføringsopsætning.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] forhindrer, at du kan slette en finanskonto, der indeholder data, der skal bruges i kontoplanen.  

## <a name="see-also"></a>Se også
[Finans- og kontoplanen](finance-general-ledger.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Importere fra andre økonomisystemer](upload-data.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

