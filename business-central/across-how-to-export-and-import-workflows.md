---
title: Sådan importerer og eksporterer du genkendelsesworkflows
description: 'Du kan overføre workflows til andre Business Central-databaser, f.eks. for at spare tid ved oprettelse af nye workflows, ved at eksportere og importere workflows.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: edupont
---
# <a name="export-and-import-approval-workflows"></a><a name="export-and-import-approval-workflows"></a>Eksportere og importere godkendelsesworkflows

Du kan overføre workflows til andre [!INCLUDE[prod_short](includes/prod_short.md)]-databaser, f.eks. for at spare tid ved oprettelse af nye workflows, ved at eksportere og importere workflows.  

En anden måde til hurtigt at oprette workflows er at bruge workflowskabeloner. Flere oplysninger [Oprette workflows fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).  

På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer med faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden. Flere oplysninger i [Oprette workflows](across-how-to-create-workflows.md).  

## <a name="export-a-workflow"></a><a name="export-a-workflow"></a>Eksportere et workflow

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflows**, og vælg derefter det relaterede link.  
2. Vælg et workflow, vælg derefter handlingen **Eksportér til fil**.  

## <a name="import-a-workflow"></a><a name="import-a-workflow"></a>Importere et workflow

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflows**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Importér fra fil**.  
3. Vælg den XML-fil, der indeholder workflowet, på siden **Importér**, vælg **Vælg**, vælg derefter **Åbn**.  

> [!CAUTION]  
> Hvis workflowkoden allerede findes i databasen, overskrives workflowtrinene med trinene i det indlæste workflow.  

## <a name="see-also"></a><a name="see-also"></a>Se også

[Opret godkendelsesworkflows](across-how-to-create-workflows.md)  
[Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md)  
[Vise arkiverede forekomster af workflowtrin](across-how-to-view-archived-workflow-step-instances.md)  
[Slette godkendelsesworkflows](across-how-to-delete-workflows.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurere godkendelsesworkflows](across-set-up-workflows.md)  
[Bruge godkendelsesworkflows](across-use-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
