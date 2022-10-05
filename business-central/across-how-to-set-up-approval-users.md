---
title: Konfigurere godkendelsesbrugere
description: Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen til siden med opsætning af godkendelser.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 09/08/2022
ms.author: edupont
ms.openlocfilehash: 2654dcb68b579d90fe3218bcd0bba3bde4cb5036
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585833"
---
# <a name="set-up-approval-users"></a>Konfigurere godkendelsesbrugere

Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen. På siden **Konfiguration af godkendelsesbruger** skal du også angive beløbsgrænser for bestemte typer anmodninger og angive stedfortrædende godkendere, som godkendelsesanmodninger skal uddelegeres til, når den oprindelige godkender er fraværende.  

> [!NOTE]  
> Begge godkendelsesanmodere og godkendere, skal først konfigureres som workflowbrugere på siden **Brugergruppe for workflow**. Flere oplysninger i [Konfigurere workflowbrugere](across-how-to-set-up-workflow-users.md).  

Når du har angivet godkendelsesbrugere, kan du oprette workflowsvar for godkendelsesworkflows. Flere oplysninger fra trin 9 i [Oprette godkendelsesworkflows](across-how-to-create-workflows.md).  

> [!NOTE]  
> Hvis du vil definere en godkendelsesanmodning som ikke-godkendt, før flere brugere har godkendt den, skal du konfigurere den i et hierarki. For godkendertypen **Godkender** skal du konfigurere godkendere på siden **Konfiguration af godkendelsesbruger**. For godkendertypen **Brugergruppe for workflow** skal du konfigurere godkendere på siden **Brugergrupper for workflow** og definere hierarkiet ved at tildele trinvise tal til hver enkelt godkender i feltet **Rækkefølgenr.** . Flere oplysninger herunder og i [Konfigurere workflowbrugere](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Sådan konfigureres en godkendelsesbruger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Godkendelse af brugerkonfiguration**, vælg det relaterede link.  
2. Opret en ny linje på siden **Konfiguration af godkendelsesbruger**, og udfyld felterne som beskrevet i følgende tabel.  

   |Felt|Beskrivelse|
   |-----|-----------|
   |**Bruger-id**|Vælg bruger-id'et for den person, der er involveret i godkendelsesprocessen.|
   |**Sælger/indkøberkode**|Angiv den sælger- eller indkøberkode, der gælder for brugeren.<br /><br /> Du udfylder typisk feltet **Sælger/indkøberkode**, hvis den sælger eller indkøber, der er ansvarlig for kunden eller leverandøren, også er den person, der skal godkende salgs- eller købsanmodningen.|
   |**Godkender-id**|Vælg bruger-id'et for den person, der skal godkende anmodninger fra den person, der er identificeret i feltet **Bruger-id**.|
   |**Godkendelsesgrænse for salgsbeløb**|Angiv det maksimale salgsbeløb i lokal valuta (RV), som personen, der er identificeret i feltet **Bruger-id** kan godkende.|
   |**Ubegrænset salgsgodkendelse**|Angiv, at den person, der er identificeret i feltet **Bruger-id** kan godkende alle salgsanmodninger uanset beløbet.<br /><br /> Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for salgsbeløb**.|
   |**Godkendelsesgrænse for indkøbsbeløb**|Angiv det maksimale købsbeløb i RV, som den person, der er identificeret i feltet **Bruger-id** kan godkende for købsrekvisitioner.|
   |**Ubegrænset indkøbsgodkendelse**|Angiv, at den person, der er identificeret i feltet **Bruger-id** kan godkende alle købsanmodninger uanset beløbet.<br /><br /> Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for købsbeløb**.|
   |**Godkendelsesgrænse for anmodet beløb**|Angiv det maksimale beløb i RV, som den person, der er identificeret i feltet **Bruger-id** kan godkende for købsrekvisitioner.<br /><br /> Hvis du vil bruge dette felt, skal du vælge indstillingen **Godkenderkæde** i feltet **Godkenders grænsetype** på siden **Workflowrespons**.|
   |**Ubegrænset anmodningsgodkendelse**|Angiv, at den person, der er identificeret i feltet **Bruger-id** kan godkende alle købsanmodninger uanset beløbet.<br /><br /> Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for anmodet beløb**.|
   |**Stedfortræder**|Vælg bruger-id'et for den person, der kan godkende anmodninger fra den person, der er identificeret, i feltet **Bruger-id**, hvis brugeren i **Godkender-id** ikke er tilgængelig. <br /><br />**Bemærk:** Stedfortræderen kan enten være brugeren i feltet **Stedfortræder**, den direkte godkender eller godkendelsesadministratoren, i nævnte rækkefølge. Flere oplysninger i [Bruge godkendelsesworkflows](across-how-use-approval-workflows.md).|
   |**Mailadresse**|Angiv mailadressen for personen i feltet **Bruger-id**.|
   |**Godkendelsesadministrator**|Angiv den bruger med tilladelse til at genåbne godkendelsesworkflow, f.eks. ved at uddelegere godkendelsesanmodninger til nye stedfortrædende godkendere eller slette forfaldne godkendelsesanmodninger.|

   > [!NOTE]
   > Kun én person kan være godkendelsesadministrator.

3. Hvis du vil teste brugeropsætningen af godkendelsen, skal du vælge handlingen **Brugeropsætning af godkendelser - kontrol**.  
4. Gentag trin 2 og 3 for hver person, du vil angive som en godkendelsesbruger.  

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Oprette brugere til workflow](across-how-to-set-up-workflow-users.md)  
[Konfiguration af workflownotifikationer](across-setting-up-workflow-notifications.md)  
[Opret godkendelsesworkflows](across-how-to-create-workflows.md)  
[Konfigurere godkendelsesworkflows](across-set-up-workflows.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
