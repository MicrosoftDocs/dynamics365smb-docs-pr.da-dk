---
title: Konfigurere kontoplanen | Microsoft Docs
description: "Beskriver, hvordan du kan ændre kontoplanen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 03/28/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 48202a9e9a763dcb22bed9975aa9c4a39d2dc4ae
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Konfigurere eller ændre kontoplanen
Kontoplanen viser de finanskonti, hvor dine finansielle data er gemt. [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] indeholder en standardkontoplan, der er klar til at understøtte din virksomhed.
Men du kan ændre standardkontiene, og du kan tilføje nye konti.  

## <a name="adding-or-changing-accounts"></a>Tilføjelse eller ændring af konti
Fra kontoplanen kan du åbne hver finanskonto og tilføje eller ændre indstillinger for hver konto.

**Bemærk**: Du kan slette en finanskonto. Men før du sletter den, skal følgende være opfyldt:  

* Saldoen på kontoen skal være nul.  
* Feltet **Tillad sletning af finanskonti før** skal være indstillet i vinduet **Regnskabsopsætning**, og der må ikke bogføres poster på kontoen på eller efter den pågældende dato.  
* Hvis feltet **Kontroller brug af finanskonto** i vinduet **Regnskabsopsætning** er markeret, må kontoen ikke bruges i nogen bogføringsgrupper eller bogføringsopsætning.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] forhindrer, at du kan slette en finanskonto, der indeholder data, der skal bruges i kontoplanen.  

## <a name="see-also"></a>Se også
[Finans- og kontoplanen](finance-general-ledger.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Dimensioner](finance-dimensions.md)  
[Importere fra andre økonomisystemer](upload-data.md)  
[Fremgangsmåde: Arbejde med GIFI-koder i Canada](ca-finance-work-gifi-codes.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
