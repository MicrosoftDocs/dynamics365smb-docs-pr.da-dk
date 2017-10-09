---
title: "Sådan konfigurerer du godkendelsesbrugere | Microsoft Docs"
description: "Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen. I feltet Konfiguration af godkendelsesbruger skal du også angive beløbsgrænser for bestemte typer anmodninger og angive stedfortrædende godkendere, som godkendelsesanmodninger skal uddelegeres til, når den oprindelige godkender er fraværende."
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
ms.openlocfilehash: 49ffa181e653377f3684d138b6ee7df3775a87f6
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-approval-users"></a>Fremgangsmåde: Konfigurere godkendelsesbrugere
Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen. I feltet **Konfiguration af godkendelsesbruger** skal du også angive beløbsgrænser for bestemte typer anmodninger og angive stedfortrædende godkendere, som godkendelsesanmodninger skal uddelegeres til, når den oprindelige godkender er fraværende.  

> [!NOTE]  
>  Godkendelsesbrugerne, dvs. både godkendelsesanmodere og godkendere, skal først konfigureres som workflowbrugere i vinduet **Brugergruppe for workflow**. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md).  

 Når du har angivet godkendelsesbrugere, kan du bruge opsætningen til at oprette arbejdsgangssvar for godkendelsesarbejdsgange. Du kan finde flere oplysninger i trin 9 i [Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md).  

> [!NOTE]  
>  Hvis du vil angive, at en godkendelsesanmodning ikke er godkendt, før flere godkendere i en godkendelseskæde har godkendt den, skal du konfigurere godkendere i et hierarki. For godkendertypen **Godkender** skal du konfigurere godkendere i vinduet **Konfiguration af godkendelsesbruger**. For godkendertypen **Brugergruppe for workflow** skal du konfigurere godkendere i vinduet **Brugergrupper for workflow** og definere hierarkiet ved at tildele trinvise tal til hver enkelt godkender i feltet **Rækkefølgenr.**. . Du kan finde flere oplysninger i dette emne og i [Fremgangsmåde: Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md).  
>   
>  Hvis du vil angive, at en godkendelsesanmodning ikke er godkendt, før flere lige godkendere har godkendt den, uanset et hierarki, skal du oprette en simpel brugergruppe til en arbejdsgang. For godkendertypen **Brugergruppe for workflow** skal du konfigurere godkendere i vinduet **Brugergrupper for workflow** og tildele det samme nummer til hver godkender feltet **Rækkefølgenr.**. . Du kan finde flere oplysninger i [Fremgangsmåde: Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Sådan konfigureres en godkendelsesbruger  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugeropsætning af godkendelser**, og vælg derefter det relaterede link.  
2. Opret en ny linje vinduet **Konfiguration af godkendelsesbruger**, og udfyld felterne som beskrevet i følgende tabel.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Bruger-id**|Vælg bruger-id'et for den bruger, der er involveret i godkendelsesprocessen.|  
    |**Sælger/indkøberkode**|Angiv den sælger- eller indkøberkode, der gælder for brugeren, i feltet **Sælger/indkøberkode**.<br /><br /> Du udfylder typisk feltet **Sælger/indkøberkode**, hvis den sælger eller indkøber, der er ansvarlig for kunden eller leverandøren, også er den person, der skal godkende salgs- eller købsanmodningen.|  
    |**Godkender-id**|Vælg bruger-id'et for den bruger, der skal godkende anmodninger fra brugeren, i feltet **Bruger-id**.|  
    |**Godkendelsesgrænse for salgsbeløb**|Angiv det maksimale salgsbeløb i RV, som brugeren i feltet **Bruger-id** kan godkende.|  
    |**Ubegrænset salgsgodkendelse**|Angiv, at brugeren i feltet **Bruger-id** kan godkende alle salgsanmodninger uanset deres beløb.<br /><br /> Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for salgsbeløb**.|  
    |**Godkendelsesgrænse for indkøbsbeløb**|Angiv det maksimale købsbeløb i RV, som brugeren i feltet **Bruger-id** kan godkende.|  
    |**Ubegrænset indkøbsgodkendelse**|Angiv, at brugeren i feltet **Bruger-id** kan godkende alle købsanmodninger uanset deres beløb.<br /><br /> Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for salgsbeløb**.|  
    |**Godkendelsesgrænse for anmodet beløb**|Angiv det maksimale beløb i RV, som brugeren i feltet **Bruger-id** kan godkende for købsrekvisitioner.<br /><br /> Hvis du vil bruge dette felt, skal du vælge indstillingen **Godkenderkæde** i feltet **Godkenders grænsetype** i vinduet **Workflowrespons**.|  
    |**Ubegrænset anmodningsgodkendelse**|Angiv, at brugeren i feltet **Bruger-id** kan godkende alle købsrekvisitioner uanset deres beløb.<br /><br /> Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for anmodet beløb**.|  
    |**Stedfortræder**|Vælg bruger-id'et for den bruger, der skal godkende anmodninger fra brugeren, i feltet **Bruger-id**, hvis brugeren i **Godkender-id** ikke er tilgængelig. **Bemærk:** Stedfortræderen kan enten være brugeren i feltet **Stedfortræder**, den direkte godkender eller godkendelsesadministratoren, i nævnte rækkefølge. Du kan finde flere oplysninger under [Fremgangsmåde: Bruge godkendelsesworkflows](across-how-use-approval-workflows.md).|  
    |**Mailadresse**|Angiv mailadressen for brugeren i feltet **Bruger-id**.|  
    |**Godkendelsesadministrator**|Angiv den bruger, der har tilladelse til at genåbne godkendelsesarbejdsgange, f.eks. ved at uddelegere godkendelsesanmodninger til nye stedfortrædende godkendere og slette forfaldne godkendelsesanmodninger.|  

    > [!NOTE]  
    >  Funktionen af feltet **Godkenders grænsetype** gælder kun for funktionalitetsområde, hvor grænser kan defineres, nemlig godkendelser af salg og køb. Alle andre godkendelsestyper, hvor grænser ikke gælder, fungerer altid som beskrevet for indstillingen **Direkte godkender**.  

3. Hvis du vil teste brugeropsætningen af godkendelsen, skal du vælge handlingen **Brugeropsætning af godkendelser - kontrol**.  
4. Gentag trin 2 og 3 for hver bruger, du vil angive som en godkendelsesbruger.  

## <a name="see-also"></a>Se også  
[Fremgangsmåde: Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md)   
[Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)   
[Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md)   
[Opsætte workflows](across-set-up-workflows.md)   
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Workflow](across-workflow.md)   

