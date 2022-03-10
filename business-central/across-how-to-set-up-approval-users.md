---
title: Konfigurere godkendelsesbrugere
description: Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen med opsætning af godkendelser.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 7602481a357a9b9e362a7b6fc0d605de04f44537
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8129203"
---
# <a name="set-up-approval-users"></a>Konfigurere godkendelsesbrugere

Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen. På siden **Konfiguration af godkendelsesbruger** skal du også angive beløbsgrænser for bestemte typer anmodninger og angive stedfortrædende godkendere, som godkendelsesanmodninger skal uddelegeres til, når den oprindelige godkender er fraværende.  

> [!NOTE]  
> Godkendelsesbrugerne, dvs. både godkendelsesanmodere og godkendere, skal først konfigureres som workflowbrugere på siden **Brugergruppe for workflow**. Der er flere oplysninger i [Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md).  

 Når du har angivet godkendelsesbrugere, kan du bruge opsætningen til at oprette arbejdsgangssvar for godkendelsesarbejdsgange. Du kan finde flere oplysninger i trin 9 i [Oprette arbejdsgange](across-how-to-create-workflows.md).  

> [!NOTE]  
> Hvis du vil angive, at en godkendelsesanmodning ikke er godkendt, før flere godkendere i en godkendelseskæde har godkendt den, skal du konfigurere godkendere i et hierarki. For godkendertypen **Godkender** skal du konfigurere godkendere på siden **Konfiguration af godkendelsesbruger**. For godkendertypen **Brugergruppe for workflow** skal du konfigurere godkendere på siden **Brugergrupper for workflow** og definere hierarkiet ved at tildele trinvise tal til hver enkelt godkender i feltet **Rækkefølgenr.**. . Du kan finde flere oplysninger i dette emne og i [Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Sådan konfigureres en godkendelsesbruger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Godkendelse af brugerkonfiguration**, og vælg derefter det relaterede link.  
2. Opret en ny linje på siden **Konfiguration af godkendelsesbruger**, og udfyld felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Bruger-id**|Vælg bruger-id'et for den bruger, der er involveret i godkendelsesprocessen.|  
    |**Sælger/indkøberkode**|Angiv den sælger- eller indkøberkode, der gælder for brugeren, i feltet **Sælger/indkøberkode**.<br /><br /> Du udfylder typisk feltet **Sælger/indkøberkode**, hvis den sælger eller indkøber, der er ansvarlig for kunden eller leverandøren, også er den person, der skal godkende salgs- eller købsanmodningen.|  
    |**Godkender-id**|Vælg bruger-id'et for den bruger, der skal godkende anmodninger fra brugeren, i feltet **Bruger-id**.|  
    |**Godkendelsesgrænse for salgsbeløb**|Angiv det maksimale salgsbeløb i RV, som brugeren i feltet **Bruger-id** kan godkende.|  
    |**Ubegrænset salgsgodkendelse**|Angiv, at brugeren i feltet **Bruger-id** kan godkende alle salgsanmodninger uanset deres beløb.<br /><br /> Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for salgsbeløb**.|  
    |**Godkendelsesgrænse for indkøbsbeløb**|Angiv det maksimale købsbeløb i RV, som brugeren i feltet **Bruger-id** kan godkende.|  
    |**Ubegrænset indkøbsgodkendelse**|Angiv, at brugeren i feltet **Bruger-id** kan godkende alle købsanmodninger uanset deres beløb.<br /><br /> Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for salgsbeløb**.|  
    |**Godkendelsesgrænse for anmodet beløb**|Angiv det maksimale beløb i RV, som brugeren i feltet **Bruger-id** kan godkende for købsrekvisitioner.<br /><br /> Hvis du vil bruge dette felt, skal du vælge indstillingen **Godkenderkæde** i feltet **Godkenders grænsetype** på siden **Workflowrespons**.|  
    |**Ubegrænset anmodningsgodkendelse**|Angiv, at brugeren i feltet **Bruger-id** kan godkende alle købsrekvisitioner uanset deres beløb.<br /><br /> Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for anmodet beløb**.|  
    |**Stedfortræder**|Vælg bruger-id'et for den bruger, der skal godkende anmodninger fra brugeren, i feltet **Bruger-id**, hvis brugeren i **Godkender-id** ikke er tilgængelig. <br /><br />**Bemærk:** Stedfortræderen kan enten være brugeren i feltet **Stedfortræder**, den direkte godkender eller godkendelsesadministratoren, i nævnte rækkefølge. Du kan finde flere oplysninger i [Bruge godkendelsesworkflows](across-how-use-approval-workflows.md).|  
    |**Mailadresse**|Angiv mailadressen for brugeren i feltet **Bruger-id**.|  
    |**Godkendelsesadministrator**|Angiv den bruger, der har tilladelse til at genåbne godkendelsesarbejdsgange, f.eks. ved at uddelegere godkendelsesanmodninger til nye stedfortrædende godkendere og slette forfaldne godkendelsesanmodninger.|

    > [!Note]
    > Kun én person kan være godkendelsesadministrator.

3. Hvis du vil teste brugeropsætningen af godkendelsen, skal du vælge handlingen **Brugeropsætning af godkendelser - kontrol**.  
4. Gentag trin 2 og 3 for hver bruger, du vil angive som en godkendelsesbruger.  

## <a name="see-also"></a>Se også

[Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md)   
[Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)   
[Oprette arbejdsgange](across-how-to-create-workflows.md)   
[Opsætte workflows](across-set-up-workflows.md)   
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Workflow](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]