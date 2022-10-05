---
title: Workflows i Dynamics 365 Business Central
description: Brug de indbyggede workflowfunktioner til at konfigurere godkendelsesworkflows for at supplere automatiserede workflows baseret på Power Automate. Du kan definere trin, der skal tildeles opgaver til forskellige personer som en del af de forskellige forretningsproces opgaver.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: ecaaf9bbb56e1c1b47f9f617319b32f32a2920fd
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585617"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Workflows i Dynamics 365 Business Central

Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.

Standardversionen af [!INCLUDE [prod_short](includes/prod_short.md)] understøtter tre typer arbejdsgange:

* Godkendelsesworkflows baseret på indbyggede workflowskabeloner

  På siden **workflow-skabeloner** kan du se alle tilgængelige arbejdsprocesser. Prøveversionen af [!INCLUDE[prod_short](includes/prod_short.md)] indeholder mange forudkonfigurerede workflows, som repræsenteres af workflowskabeloner, som du kan kopiere for at oprette nye. Når du åbner en skabelon fra siden **workflow-skabeloner**, og navnet på arbejdsprocessen starter med *MS-*, er skabelonen tilføjet af Microsoft.
  
* Power Automate-flows, som du selv opretter

  Alle workflowskabeloner, som du opretter med, Microsoft Power Automate, føjes til listen over workflowskabeloner i [!INCLUDE[prod_short](includes/prod_short.md)]. Flere oplysninger i [Bruge [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate-flows](across-how-use-financials-data-source-flow.md). 
  
* Øjeblikkelige flows udløses manuelt af handlingen **Automatiser** ([!INCLUDE [prod_short](includes/prod_short.md)] kun online).

  Oprette og manuelt udløse et Power Automate-flow for en [!INCLUDE[prod_short](includes/prod_short.md)]-post, f. eks. en debitor, vare eller salgsordre, med mulighed for at manipulere både internt og eksternt og ved hjælp af integrerede værktøjer. Der er flere oplysninger i [Øjeblikkelige flows](across-how-use-financials-data-source-flow.md#instant-flows)-afsnittet.

## <a name="power-automate-flows"></a>Power Automate-flows

Du kan bruge [!INCLUDE [prod_short](includes/prod_short.md)] online til at tilmelde dig Power Automate effektive automatiserede arbejdsgange. Du kan køre disse arbejdsprocesser fra [!INCLUDE [prod_short](includes/prod_short.md)], forbinde interne og eksterne datakilder og værktøjer uden at kode viden.

Power Automate-flows kan udløses af hændelser (f. eks. post-eller dokumentoprettelse, ændring eller sletning) og kørsel på en brugerdefineret tidsplan eller efter behov (også kaldet et **øjeblikkeligt flow**).

## <a name="approval-workflows"></a>Godkendelsesworkflows

Du opretter et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer med faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden.<!--What are the "values"? Can we give an example?-->

Eksempler på hændelser med godkendelsesworkflows omfatter bl.a. oprettelse af salgs-eller købsordrer/tilbud/fakturaer, prisændringer og kreditor- eller debitorredigeringer.

[!INCLUDE[workflow](includes/workflow.md)]

| **Hvis du vil** | **Se** |
|--|--|
| Oprette godkendelsesworkflowbrugere, angive, hvordan brugere modtager notifikationer, og oprette nye arbejdsgange. (Sådan oprettes nye workflows til ikke-understøttede scenarier, implementeres de krævede workflowelementer ved at tilpasse programkoden.) | [Konfigurer godkendelsesworkflow](across-set-up-workflows.md) |
| Aktiver godkendelsesworkflows, behandl meddelelser i arbejdsgangen, herunder godkendelser og godkendelsesanmodninger om at udføre trin i en arbejdsgang. Arkiver og slet arbejdsgange. | [Bruge godkendelsesworkflows](across-use-workflows.md) |
| Integrere virksomhedsdata med Power Automate-workflows med både interne og eksterne kilder og hændelser for at oprette og automatisere opgaver og arbejdsgange. | [Brug Power Automate-flows i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Administrere projekter](projects-manage-projects.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Fejlfinde dine [!INCLUDE[prod_short](includes/prod_short.md)] Automatiserede workflows](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
