---
title: "Bruge udvidelsen QuickBooks-overførsel | Microsoft Docs"
description: Beskriver, hvordan du bruger udvidelsen til at importere debitorer, kreditorer, varer og konti fra QuickBooks Desktop til Dynamics 365 for Financials.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4775c945a7721b8f4e52a187840a585396611e47
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a>Udvidelsen Overførsel af QuickBooks-data til Dynamics 365 for Financials
Denne udvidelse gør det nemt at overflytte debitorer, kreditorer, varer og konti fra QuickBooks Desktop til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis din virksomhed bruger QuickBooks i dag, kan du eksportere de relevante oplysninger og derefter åbne en assisteret opsætningsvejledning for at overføre dataene til [!INCLUDE[d365fin](includes/d365fin_md.md)].  
Du kan finde flere oplysninger under [Importere virksomhedsdata fra andre økonomisystemer](upload-data.md).

## <a name="exporting-data-from-quickbooks-desktop"></a>Udlæse data fra QuickBooks Desktop
Du skal have udlæst nogle eller alle eksisterende kunder, leverandører, lagervarer og konti til en IIF-fil (Intuit Interchange Format). Udvidelsen Overførsel af QuickBooks-data indeholder en standardtilknytning af QuickBooks-data, så du kan bruge dine eksisterende data til at teste den nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-virksomhed. Standardtilknytningen er tilstrækkelig i de fleste tilfælde, men du kan ændre tilknytningen i den assisterede opsætningsvejledning.  
I QuickBooks indeholder menuen Filer et værktøj til eksport af lister. I forbindelse med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du eksportere følgende lister:

* Debitoroversigt  
* Kreditoroversigt  
* Vareoversigt  
* Kontooversigt  

De eksporterede data gemmes som en IIF-fil, som du derefter kan overføre til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="finding-the-quickbooks-data-migration-extension"></a>Sådan finder du udvidelsen Overførsel af QuickBooks-data
Udvidelsen Overførsel af QuickBooks-data er installeret og klar til brug som en integreret del af den assisterende opsætningsvejledning til dataoverførsel. Hvis du er klar til at komme i gang nu og har eksporteret dine data fra QuickBooks, skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Assisteret opsætning** og derefter vælge det relaterede link. Vælg **Overflyt forretningsdata**, og følg derefter trinnene i vejledningen.  

## <a name="see-also"></a>Se også
[Importere virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser ](ui-extensions.md)  

