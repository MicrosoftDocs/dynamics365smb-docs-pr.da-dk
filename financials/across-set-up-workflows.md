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
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 59805de35ca1ebe01255eafeb4fff12efacde934
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-workflows"></a>Opsætte workflows
Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin. Der er flere oplysninger i [Anvende workflows](across-use-workflows.md).  

 Inden du kan bruge arbejdsprocesser, skal du oprette arbejdsgangbrugere og godkendelsesbrugere, angive, hvordan brugere modtager notifikationer om trin i arbejdsgange, og derefter oprette arbejdsgange, eventuelt efter tilpasning af koder.  

 I vinduet **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden.  

 Hvis et virksomhedsscenarie kræver en workflowhændelse eller et svar, der ikke understøttes, skal en Microsoft-partner implementere dem ved at tilpasse programkoden. Du kan finde flere oplysninger i [Gennemgang: implementering af nye arbejdsgangshændelser og -svar](https://msdn.microsoft.com/en-us/library/mt574349.aspx) på MSDN.

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

|**For at**|**Se**|  
|------------|-------------|  
|Opret arbejdsgangbrugere og brugergrupper.|[Fremgangsmåde: Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md)|  
|Konfigurer arbejdsgangbrugere, der indgår i godkendelsesarbejdsgange.|[Fremgangsmåde: Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)|  
|Angiv, hvordan arbejdsgang brugere skal have besked om trin i arbejdsgangen, herunder godkendelsesanmodninger.|[Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)|  
|Angiv, hvornår brugerne modtager notifikationer, og om notifikationer skal samles i en periode for at reducere antallet af notifikationer.|[Fremgangsmåde: Angive, hvornår og hvordan notifikationer modtages](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Konfigurer layoutet og det generelle indhold for nye mails med arbejdsgangsnotifikationer, eller eksportér, rediger og genimportér eksisterende skabeloner.|[Fremgangsmåde: Administrere notifikationsskabeloner](across-how-to-manage-notification-templates.md)|  
|Konfigurer en SMTP-server til at aktivere mailkommunikation til og fra [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Fremgangsmåde: Konfigurere mail](madeira-how-setup-email.md)|
|Angiv de forskellige trin i en arbejdsgang ved at forbinde arbejdsgangshændelser med arbejdsgangsvar.|[Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md)|  
|Brug workflowskabeloner til at oprette nye workflows.|[Fremgangsmåde: Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md)|  
|Del workflows med andre [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser.|[Fremgangsmåde: Importere og eksportere workflows](across-how-to-export-and-import-workflows.md)|  
|Lær, hvordan du konfigurerer en arbejdsgang til godkendelse af salgsdokumenter ved at følge en hel procedure.|[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Tilføj understøttelse af et forretningsscenarie, der kræver nye workflowhændelser eller -responses ved at tilpasse programkoden.|[Gennemgang: Implementering af nye workflowhændelser og -responser](https://msdn.microsoft.com/en-us/library/mt574349.aspx) på MSDN.|  

## <a name="see-also"></a>Se også  
 [Anvende workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   
 [Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Arbejde med Financials](ui-work-product.md)

