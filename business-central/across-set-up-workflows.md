---
title: Opsætte workflows | Microsoft Docs
description: Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 6f73978c381075175d80c14c8aaaf2d66cb60ade
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188152"
---
# <a name="setting-up-workflows"></a>Opsætte workflows
Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin. Der er flere oplysninger i [Anvende workflows](across-use-workflows.md).  

 Inden du kan bruge arbejdsprocesser, skal du oprette arbejdsgangbrugere og godkendelsesbrugere, angive, hvordan brugere modtager notifikationer om trin i arbejdsgange, og derefter oprette arbejdsgange, eventuelt efter tilpasning af koder.  

 På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden.  

 Hvis et virksomhedsscenarie kræver en workflowhændelse eller et svar, der ikke understøttes, skal en Microsoft-partner implementere dem ved at tilpasse programkoden. Du kan finde flere oplysninger i [Gennemgang: Implementering af nye workflowhændelser og -responser](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) i hjælpen til udviklere og it-eksperter.

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

|**For at**|**Skal du se**|  
|------------|-------------|  
|Opret arbejdsgangbrugere og brugergrupper.|[Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md)|  
|Konfigurer arbejdsgangbrugere, der indgår i godkendelsesarbejdsgange.|[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)|  
|Angiv, hvordan arbejdsgang brugere skal have besked om trin i arbejdsgangen, herunder godkendelsesanmodninger.|[Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)|  
|Angiv, om brugerne får besked via e-mail, og noter, hvor ofte notifikationer sendes.|[Angive, hvornår og hvordan notifikationer modtages](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Tilpas indholdet af e-mailmeddelelserne ved at tilpasse rapport 1320, Notifikationsmail.|[Sådan opretter og ændrer du Brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md)|  
|Konfigurer en SMTP-server til at aktivere mailkommunikation til og fra [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Konfigurere mail](admin-how-setup-email.md)|
|Angiv de forskellige trin i en arbejdsgang ved at forbinde arbejdsgangshændelser med arbejdsgangsvar.|[Oprette arbejdsgange](across-how-to-create-workflows.md)|  
|Brug workflowskabeloner til at oprette nye workflows.|[Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md)|  
|Del workflows med andre [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser.|[Eksportere og importere workflows](across-how-to-export-and-import-workflows.md)|  
|Lær, hvordan du konfigurerer en arbejdsgang til godkendelse af salgsdokumenter ved at følge en hel procedure.|[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Tilføj understøttelse af et forretningsscenarie, der kræver nye workflowhændelser eller -responses ved at tilpasse programkoden.|[Gennemgang: Implementering af nye workflowhændelser og -responser](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="example-of-an-approval-workflow"></a>Eksempel på et godkendelsesworkflow
Denne video viser, hvordan du konfigurerer et workflow, der kræver, at en person anmoder om en andens godkendelse, før vedkommende kan ændre oplysninger om en eksisterende kunde eller oprette en ny kunde.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-also"></a>Se også  
 [Anvende workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   
 [Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Arbejde med Business Central](ui-work-product.md)
