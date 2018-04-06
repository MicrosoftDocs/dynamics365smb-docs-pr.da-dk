---
title: "Resultaterne af overførslen | Microsoft Docs"
description: "Dette emne beskriver, hvad der sker, når du har overført finansposter til omkostningsposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bc693bf3f3339b54a5d8d8847beb06c3fc018a0f
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a>Resultater af overførsel af finansposter til omkostningsposter.
Under overførslen af regnskabsposter til omkostningsposter opretter [!INCLUDE[d365fin](includes/d365fin_md.md)] forbindelser i posterne i tabellen **Finanspost**, tabellen **Omkostningspost** og tabellen **Omkostningsregister** for at gøre det muligt at spore forbindelserne mellem omkostningsposter og regnskabsposter.  

## <a name="general-ledger-entries"></a>Finansposter  
For hver regnskabspost, der overføres til omkostningsregnskab, udfylder [!INCLUDE[d365fin](includes/d365fin_md.md)] omkostningsfeltet **Løbenr.**.  

## <a name="cost-entries"></a>Omkostningsposter  
For hver omkostningspost gemmer [!INCLUDE[d365fin](includes/d365fin_md.md)] løbenummeret på den tilsvarende regnskabspost i feltet **Finansløbenr.** i tabellen **Omkostningspost**.  

For samlede omkostningsposter gemmer [!INCLUDE[d365fin](includes/d365fin_md.md)] løbenummer på den sidste regnskabspost, som er posten med det højeste løbenummer.  

Feltet **Finanskonto** i tabellen **Omkostningspost** indeholder nummeret på den finanskonto, som omkostningsposten stammer fra.  

For enkelte omkostningsposter overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] bogføringsteksten fra regnskabsposten til tekstfeltet **Beskrivelse**. For kombinerede poster viser tekstfeltet, at disse poster er overfører som kombinerede poster. For eksempel kan teksten for en kombineret post for oktober 2013 være **Kombinerede poster, oktober 2013**.  

## <a name="cost-register"></a>Omkostningsregister  
I tabellen **Omkostningsregister** opretter [!INCLUDE[d365fin](includes/d365fin_md.md)] en post med kildeoverførsel fra regnskabet. Posten registrerer det første og sidste løbenummer for de finansposter, der overføres, foruden første og sidste postnummer på de omkostningsposter, der er oprettet.  

## <a name="see-also"></a>Se også  
[Overføre finansposter til omkostningsposter](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
[Kriterier for overførsel af finansposter til omkostningsposter](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
[Automatisk overførsel og kombinerede poster](finance-automatic-transfer-combined-entries.md)   
[Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md)  

