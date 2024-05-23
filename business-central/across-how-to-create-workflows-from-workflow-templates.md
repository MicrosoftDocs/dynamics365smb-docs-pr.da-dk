---
title: Sådan oprettes workflows ud fra workflowskabeloner
description: For at spare tid ved oprettelse af nye godkendte workflows kan du oprette workflows ud fra workflowskabeloner.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Oprette workflows ud fra workflowskabeloner

På siden **Workflow** opretter du et workflow ved at oprette en serie af workflowtrin på linjerne. Hvert trin består af en workflowhændelse (Når hændelse), begrænset af hændelsesbetingelser (På betingelse) og et workflowsvar (Så svar), begrænset af svarmuligheder. Felterne på workflowlinjer indeholder faste lister med hændelses- og svarværdier, der repræsenterer de scenarier, som [!INCLUDE [prod_short](includes/prod_short.md)] understøtter. Flere oplysninger i [Oprette workflows](across-how-to-create-workflows.md).

For at spare tid ved oprettelse af nye godkendelsesworkflows leverer [!INCLUDE [prod_short](includes/prod_short.md)] workflowskabeloner. Skabelonerne er tilgængelige på siden **Workflowskabeloner**. Du kan bruge skabelonerne, som de er, eller tilpasse dem, så de opfylder dine behov. Koderne for workflowskabeloner fra Microsoft, har **MS-** foran.

[!INCLUDE [workflow-next-step](includes/workflow-next-step.md)]

Hvis du ændrer en arbejdsprocesskabelon, men senere fortryder ændringen, skal du bruge handlingen **Nulstil Microsoft-skabeloner** til at vende tilbage til den oprindelige indstilling for arbejdsprocessen.

> [!CAUTION]
> Handlingen **Nulstil Microsoft-skabeloner** nulstiller alle Microsoft-arbejdsprocesskabeloner. Du kan ikke nulstille en enkelt skabelon.  

Du kan også hurtigt oprette en arbejdsproces ved at importere den, f.eks. hvis du har eksporteret den fra en anden forekomst af [!INCLUDE[prod_short](includes/prod_short.md)]. Flere oplysninger under [Eksport og import af workflows](across-how-to-export-and-import-workflows.md).  

## Sådan opretter du fra et workflow ud fra en workflowskabelon

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflows**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Nyt workflow fra skabelon**. Siden **Workflowskabeloner** åbnes.  
3. Vælg en workflowskabelon, og vælg derefter knappen **OK**.  

   Siden **Workflow** åbnes for et nyt workflow, der indeholder alle oplysninger fra den valgte skabelon. Værdien i feltet **Kode** er udvidet med f.eks. "-01" for at angive, at dette er det første workflow, som oprettes ud fra workflowskabelonen.  
4. Tilpas workflowet ved at redigere workflowtrinene eller tilføje nye trin. Flere oplysninger i [Oprette workflows](across-how-to-create-workflows.md).  

## Se også

[Oprette godkendelsesworkflows](across-how-to-create-workflows.md)  
[Eksportere og importere godkendelsesworkflows](across-how-to-export-and-import-workflows.md)  
[Vise arkiverede forekomster af workflowtrin](across-how-to-view-archived-workflow-step-instances.md)  
[Slette godkendelsesworkflows](across-how-to-delete-workflows.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurere godkendelsesworkflows](across-set-up-workflows.md)  
[Bruge godkendelsesworkflows](across-use-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
