---
title: "Automatisk overførsel og kombinerede poster | Microsoft Docs"
description: "I omkostningsregnskab kan du overføre finansposter til en pristype ved hjælp af kombineret bogføring. Du kan angive, om en pristype modtager samlede poster i feltet **Saml poster** i pristypedefinitionen. Den følgende tabel beskriver de forskellige indstillinger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bd80d0a7a701256dfdae3346e899b84eeb990a40
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="automatic-transfer-and-combined-entries"></a>Automatisk overførsel og kombinerede poster
I omkostningsregnskab kan du overføre finansposter til en pristype ved hjælp af kombineret bogføring. Du kan angive, om en pristype modtager samlede poster i feltet **Saml poster** i pristypedefinitionen. Den følgende tabel beskriver de forskellige indstillinger.  

|Saml poster|Beskrivelse|  
|---------------------|-----------------|  
|Ingen|Alle finansposter overføres individuelt til den tilsvarende pristype.|  
|DAG|Finansposter med den samme bogføringsdato overføres som én post til den tilsvarende pristype.|  
|Måned|Alle finansposter i den samme kalendermåned overføres som én post til den tilsvarende pristype.|  

> [!IMPORTANT]  
>  Hvis du har markeret afkrydsningsfeltet **Automatisk overførsel fra finans** i vinduet **Konfiguration af omkostningsregnskab**, opdaterer [!INCLUDE[d365fin](includes/d365fin_md.md)] omkostningsregnskabet efter hver bogføring i regnskabet. Kombinerede poster er ikke mulige.  

## <a name="see-also"></a>Se også  
 [Sådan overføres finansposter til omkostningsposter](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Kriterier for overførsel af finansposter til omkostningsposter.](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Resultater af overførslen](finance-results-of-the-transfer.md)   
 [Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

