---
title: "Automatisk overførsel og kombinerede poster | Microsoft Docs"
description: "I omkostningsregnskab kan du overføre finansposter til en pristype ved hjælp af kombineret bogføring. Du kan angive, om en pristype modtager samlede poster i feltet **Saml poster** i pristypedefinitionen. Den følgende tabel beskriver de forskellige indstillinger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4f1bcf009b397438bb302a16a23be2f4638cefc4
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

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
 [Overføre finansposter til omkostningsposter](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Kriterier for overførsel af finansposter til omkostningsposter.](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Resultater af overførslen](finance-results-of-the-transfer.md)   
 [Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

