---
title: Automatisk overførsel og kombinerede poster | Microsoft Docs
description: I omkostningsregnskab kan du overføre finansposter til en pristype ved hjælp af kombineret bogføring. Du kan angive, om en pristype modtager samlede poster i feltet **Saml poster** i pristypedefinitionen. Den følgende tabel beskriver de forskellige indstillinger.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 8f6b5328b3a7b8cdcb4582deda363bdd0361ed9a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "941150"
---
# <a name="automatic-transfer-and-combined-entries"></a>Automatisk overførsel og kombinerede poster
I omkostningsregnskab kan du overføre finansposter til en pristype ved hjælp af kombineret bogføring. Du kan angive, om en pristype modtager samlede poster i feltet **Saml poster** i pristypedefinitionen. Den følgende tabel beskriver de forskellige indstillinger.  

|Saml poster|Beskrivelse|  
|---------------------|-----------------|  
|Ingen|Alle finansposter overføres individuelt til den tilsvarende pristype.|  
|DAG|Finansposter med den samme bogføringsdato overføres som én post til den tilsvarende pristype.|  
|Måned|Alle finansposter i den samme kalendermåned overføres som én post til den tilsvarende pristype.|  

> [!IMPORTANT]  
>  Hvis du har markeret afkrydsningsfeltet **Automatisk overførsel fra finans** på siden **Konfiguration af omkostningsregnskab**, opdaterer [!INCLUDE[d365fin](includes/d365fin_md.md)] omkostningsregnskabet efter hver bogføring i regnskabet. Kombinerede poster er ikke mulige.  

## <a name="see-also"></a>Se også  
 [Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md)   
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
