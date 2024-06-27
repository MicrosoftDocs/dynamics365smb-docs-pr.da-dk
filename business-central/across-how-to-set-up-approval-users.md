---
title: Opsætte godkendelsesbrugere
description: 'Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.form: '663,'
ms.date: 05/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Opsætte godkendelsesbrugere

Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen, på siden **Brugeropsætning af godkendelser**. Du kan også angive beløbsgrænser for forskellige typer anmodninger, definere stedfortrædende godkendere og oprette notifikationer.  

Når du har angivet godkendelsesbrugere, kan du oprette workflowsvar for godkendelsesworkflow. Flere oplysninger i [Oprette godkendelsesworkflows](across-how-to-create-workflows.md).  

> [!TIP]
> Du kan kræve, at flere godkendere skal reagere på en godkendelsesanmodning, ved at oprette en gruppe godkendere på siden **Brugergruppe for workflow**. Flere oplysninger i [Konfigurere brugergrupper for workflow](across-how-to-set-up-workflow-users.md).  

## Sådan konfigureres en godkendelsesbruger

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Godkendelse af brugerkonfiguration**, vælg det relaterede link.  
2. Opret en ny linje på siden **Konfiguration af godkendelsesbruger**, og udfyld felterne som beskrevet i følgende tabel.  

   |Felt|Beskrivelse|
   |-----|-----------|
   |**Bruger-id**|Vælg bruger-id'et for den person, der er involveret i godkendelsesprocessen.|
   |**Sælger/indkøberkode**|Angiv den sælger- eller indkøberkode, der gælder for brugeren.<br /><br /> Du udfylder typisk feltet **Sælger/indkøberkode**, hvis den sælger eller indkøber, der er ansvarlig for kunden eller leverandøren, også er den person, der skal godkende en salgs- eller købsanmodning.|
   |**Godkender-id**|Vælg bruger-id'et for den person, der skal godkende anmodninger fra den person, du har angivet i feltet **Bruger-id**.|
   |**Beløbsgrænse for godkendelse af salg**|Angiv det maksimale salgsbeløb i lokal valuta (RV), som den person, der er valgt i feltet **Bruger-id**, kan godkende.|
   |**Ubegrænset godkendelse af salg**|Angiv, at den person, der er identificeret i feltet **Bruger-id** kan godkende alle salgsanmodninger uanset beløbet.<br /><br /> Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for salgsbeløb**.|
   |**Godkendelsesgrænse for indkøbsbeløb**|Angiv det maksimale købsbeløb i RV, som den person, der er identificeret i feltet **Bruger-id** kan godkende for købsrekvisitioner.|
   |**Ubegrænset indkøbsgodkendelse**|Angiv, at den person, der er identificeret i feltet **Bruger-id** kan godkende alle købsanmodninger uanset beløbet.<br /><br /> Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for indkøbsbeløb**.|
   |**Godkendelsesgrænse for anmodet beløb**|Angiv det maksimale beløb i RV, som den person, der er identificeret i feltet **Bruger-id** kan godkende for købsrekvisitioner.<br /><br /> Hvis du vil bruge dette felt, skal du vælge indstillingen **Godkenderkæde** i feltet **Godkenders grænsetype** på siden **Workflowrespons**.|
   |**Ubegrænset anmodningsgodkendelse**|Angiv, at den person, der er identificeret i feltet **Bruger-id** kan godkende alle købsanmodninger uanset beløbet.<br /><br /> Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for anmodet beløb**.|
   |**Stedfortræder**|Vælg bruger-id'et for den person, der skal godkende anmodninger fra den person, der er identificeret, i feltet **Bruger-id**, hvis brugeren i **Godkender-id** ikke er tilgængelig. <br /><br />**Bemærk:** Stedfortræderen kan enten være brugeren i feltet **Stedfortræder**, den direkte godkender eller godkendelsesadministratoren, i nævnte rækkefølge. Flere oplysninger i [Bruge godkendelsesworkflows](across-how-use-approval-workflows.md).|
   |**Mailadresse**|Angiv mailadressen for personen i feltet **Bruger-id**.|
   |**Godkendelsesadministrator**|Angiv den bruger, der har tilladelse til at genåbne godkendelsesworkflow, f.eks. ved at uddelegere godkendelsesanmodninger til nye stedfortrædende godkendere eller slette forfaldne godkendelsesanmodninger.<br /><br />**Bemærk!** Kun én person kan være godkendelsesadministrator.|

3. Hvis du vil teste brugeropsætningen af godkendelsen, skal du vælge handlingen **Brugeropsætning af godkendelser - kontrol**.  
4. Gentag trin 2 og 3 for hver person, du vil angive som en godkendelsesbruger.  

I næste trin skal du angive, hvordan du vil [!INCLUDE [prod_short](includes/prod_short.md)] give brugerne besked om, at en anmodning afventer deres opmærksomhed. Få mere at vide under [Konfiguration af workflownotifikationer](across-setting-up-workflow-notifications.md).

## Se også

[Konfigurere brugere til workflow](across-how-to-set-up-workflow-users.md)  
[Konfiguration af workflownotifikationer](across-setting-up-workflow-notifications.md)  
[Opret godkendelsesworkflows](across-how-to-create-workflows.md)  
[Konfigurere godkendelsesworkflows](across-set-up-workflows.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
