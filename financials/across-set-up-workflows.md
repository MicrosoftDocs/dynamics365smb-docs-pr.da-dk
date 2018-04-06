---
title: "Opsætte workflows | Microsoft Docs"
description: "Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/20/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e6e662ee13db1f9002e1c3e74a0d15e2aa2e2a98
ms.openlocfilehash: d837fb0b85f3b62c82fb63596e1299ffdd252b23
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-workflows"></a>Opsætte workflows
Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin. Der er flere oplysninger i [Anvende workflows](across-use-workflows.md).  

 Inden du kan bruge arbejdsprocesser, skal du oprette arbejdsgangbrugere og godkendelsesbrugere, angive, hvordan brugere modtager notifikationer om trin i arbejdsgange, og derefter oprette arbejdsgange, eventuelt efter tilpasning af koder.  

 I vinduet **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden.  

 Hvis et virksomhedsscenarie kræver en workflowhændelse eller et svar, der ikke understøttes, skal en Microsoft-partner implementere dem ved at tilpasse programkoden. Du kan finde flere oplysninger i [Gennemgang: Implementering af nye workflowhændelser og -responser](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) i hjælpen til udviklere og it-eksperter.

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

|**For at**|**Skal du se**|  
|------------|-------------|  
|Opret arbejdsgangbrugere og brugergrupper.|[Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md)|  
|Konfigurer arbejdsgangbrugere, der indgår i godkendelsesarbejdsgange.|[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)|  
|Angiv, hvordan arbejdsgang brugere skal have besked om trin i arbejdsgangen, herunder godkendelsesanmodninger.|[Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)|  
|Angiv, hvornår brugerne modtager notifikationer, og om notifikationer skal samles i en periode for at reducere antallet af notifikationer.|[Angive, hvornår og hvordan notifikationer modtages](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Konfigurer layoutet og det generelle indhold for nye mails med arbejdsgangsnotifikationer, eller eksportér, rediger og genimportér eksisterende skabeloner.|[Administrere notifikationsskabeloner](across-how-to-manage-notification-templates.md)|  
|Konfigurer en SMTP-server til at aktivere mailkommunikation til og fra [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Konfigurere mail](madeira-how-setup-email.md)|
|Angiv de forskellige trin i en arbejdsgang ved at forbinde arbejdsgangshændelser med arbejdsgangsvar.|[Oprette arbejdsgange](across-how-to-create-workflows.md)|  
|Brug workflowskabeloner til at oprette nye workflows.|[Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md)|  
|Del workflows med andre [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser.|[Eksportere og importere workflows](across-how-to-export-and-import-workflows.md)|  
|Lær, hvordan du konfigurerer en arbejdsgang til godkendelse af salgsdokumenter ved at følge en hel procedure.|[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Tilføj understøttelse af et forretningsscenarie, der kræver nye workflowhændelser eller -responses ved at tilpasse programkoden.|[Gennemgang: Implementering af nye workflowhændelser og -responser](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="see-also"></a>Se også  
 [Anvende workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   
 [Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Arbejde med Financials](ui-work-product.md)

