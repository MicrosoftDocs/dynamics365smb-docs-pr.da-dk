---
title: Sådan oprettes workflows ud fra workflowskabeloner
description: 'Hvis du vil spare tid, når du opretter nye godkendelses-workflows, kan du oprette ikke-redigerbare workflows fra workflowskabeloner, der er blevet foranstillet med "MS".'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: edupont
---
# <a name="create-workflows-from-workflow-templates"></a>Oprette workflows ud fra workflowskabeloner

For at spare tid ved oprettelse af nye godkendelses-workflows kan du bruge workflowskabeloner.  

Workflowskabeloner er workflows, som ikke kan redigeres, og som findes i standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)]. Koderne for workflowskabeloner, som er oprettet af Microsoft, har "MS-" foran.  

En anden måde til hurtigt at oprette et workflow på er at importere et eksisterende workflow, som du har på en fil uden for [!INCLUDE[prod_short](includes/prod_short.md)]. Flere oplysninger under [Eksport og import af workflows](across-how-to-export-and-import-workflows.md).  

På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden. Flere oplysninger i [Oprette workflows](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template"></a>Sådan opretter du fra et workflow ud fra en workflowskabelon

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflows**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Nyt workflow fra skabelon**. Siden **Workflowskabeloner** åbnes.  
3. Vælg en workflowskabelon, og vælg derefter knappen **OK**.  

   Siden **Workflow** åbnes for et nyt workflow, der indeholder alle oplysninger fra den valgte skabelon. Værdien i feltet **Kode** er udvidet med f.eks. "-01" for at angive, at dette er det første workflow, som oprettes ud fra workflowskabelonen.  
4. Fortsæt med at oprette workflowet ved at redigere workflowtrinene eller tilføje nye trin. Flere oplysninger i [Oprette workflows](across-how-to-create-workflows.md).  

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Opret godkendelsesworkflows](across-how-to-create-workflows.md)  
[Eksportere og importere godkendelsesworkflows](across-how-to-export-and-import-workflows.md)  
[Vise arkiverede forekomster af workflowtrin](across-how-to-view-archived-workflow-step-instances.md)  
[Slette godkendelsesworkflows](across-how-to-delete-workflows.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurere godkendelsesworkflows](across-set-up-workflows.md)  
[Bruge godkendelsesworkflows](across-use-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
