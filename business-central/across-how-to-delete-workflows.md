---
title: Sådan slettes godkendelsesworkflows
description: 'Hvis du er sikker på, at en arbejdsgang ikke længere bruges, kan du slette den. Alle forekomster af trin i arbejdsgangen, der er defineret i arbejdsgangen, skal have status **Afsluttet**.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '1500,'
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Slette godkendelsesworkflows

Hvis du er sikker på, at en arbejdsgang ikke længere bruges, kan du slette den. Alle forekomster af trin i workflowet, der er defineret i arbejdsgangen, skal have status **Afsluttet**.

> [!CAUTION]
> Når du sletter en arbejdsgang, mistes alle oplysninger i arbejdsgangen.

På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer med faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden. Flere oplysninger i [Oprette godkendelsesworkflows](across-how-to-create-workflows.md).

## Slette et workflow

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflows**, og vælg derefter det relaterede link.
2. Vælg det workflow, du vil slette.
3. Vælg handlingen **Slet**.
4. Du kan også åbne det workflow, du vil slette.
5. På siden **Workflow** skal du vælge handlingen **Slet**.

> [!NOTE]
> Sletning af et workflow kræver, at det er deaktiveret. Hvis du vil deaktivere et workflow, skal du åbne den på siden **Workflows** og derefter slå **Aktiveret** til/fra.

## Se også

[Opret godkendelsesworkflows](across-how-to-create-workflows.md)  
[Aktivere godkendelsesworkflows](across-how-to-enable-workflows.md)  
[Bruge godkendelsesworkflows](across-use-workflows.md)  
[Vise arkiverede forekomster af workflowtrin](across-how-to-view-archived-workflow-step-instances.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurere godkendelsesworkflows](across-set-up-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
