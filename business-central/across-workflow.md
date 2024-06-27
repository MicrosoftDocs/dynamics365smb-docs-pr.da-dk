---
title: Workflows i Dynamics 365 Business Central
description: 'Brug de indbyggede workflowfunktioner til at konfigurere godkendelsesworkflows for at supplere automatiserede workflows baseret på Power Automate. Du kan definere trin, der skal tildeles opgaver til forskellige personer som en del af de forskellige forretningsproces opgaver.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 06/13/2024
ms.custom: bap-template
---
# Workflows i Business Central

Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Du kan medtage systemopgaver, som f. eks. automatisk bogføring, i workflows. Systemopgaver kan indledes eller efterfølges af brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.

Standardversionen af [!INCLUDE [prod_short](includes/prod_short.md)] understøtter disse typer arbejdsgange:
  
* Power Automate-flows

  * Automatiserede flows, der udløses af hændelser (f.eks. oprettelse af post eller dokument, ændring eller sletning) i [!INCLUDE[prod_short](includes/prod_short.md)]. Inkluderede godkendelsesprocesser, der oprettes i Power Automate, udløses også, når der anmodes om godkendelse i [!INCLUDE[prod_short](includes/prod_short.md)].
  * Øjeblikkelige flows, der udløses manuelt af handlingen **Automatiser** fra lister, kort og dokumentsider.

    Oprette og manuelt udløse et Power Automate-flow for en [!INCLUDE[prod_short](includes/prod_short.md)]-post, f. eks. en debitor, vare eller salgsordre, med mulighed for at manipulere både internt og eksternt og ved hjælp af integrerede værktøjer.

* Godkendelsesworkflows baseret på indbyggede workflowskabeloner

  På siden **workflow-skabeloner** kan du se alle tilgængelige arbejdsprocesser. Prøveversionen af [!INCLUDE[prod_short](includes/prod_short.md)] indeholder mange forudkonfigurerede workflows, som repræsenteres af workflowskabeloner, som du kan kopiere for at oprette nye. Når du åbner en skabelon fra siden **workflow-skabeloner**, og navnet på arbejdsprocessen starter med *MS-*, er skabelonen tilføjet af Microsoft.

## Power Automate-flows

Med [!INCLUDE [prod_short](includes/prod_short.md)] online kan du tilmelde dig Power Automate for at oprette effektive automatiserede workflows. Du kører disse workflows fra [!INCLUDE [prod_short](includes/prod_short.md)]. Disse flows kan forbinde interne og eksterne datakilder og værktøjer uden kodning af viden.

|**For at** |**Skal du se**|
|-------|-------|
|Introduktion til Power Automate, oprettelse af flows og kørsel af øjeblikkelige flows|[Brug Power Automate-flows i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)|
|Få mere at vide om, hvordan du opretter, redigerer og administrerer flows|[Konfigurere automatiserede flows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) og [Konfigurere øjeblikkelige flows](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)|
|Konfigurere Power Automate-integration med [!INCLUDE[prod_short](includes/prod_short.md)] for brugere som administrator|[Konfigurere Power Automate Integration](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup)|

## Godkendelsesworkflows

Oprette en godkendelsesarbejdsgang ved at definere, hvad der starter arbejdsprocessen, og hvad der derefter sker, som følgende:

* En workflow-hændelse, der er begrænset af hændelsesbetingelser.
* Et workflow-svar, der er begrænset af svarindstillingerne.

Du definerer workflowtrin ved at udfylde felter om workflowlinjer med hændelses- og svarværdier, der repræsenterer understøttede scenarier.

Eksempler på hændelser med godkendelsesworkflow omfatter bl.a. oprettelse af salgs-eller købsordrer/tilbud/fakturaer, prisændringer og kreditor- eller debitorredigeringer med mere.

[!INCLUDE[workflow](includes/workflow.md)]

| **Hvis du vil** | **Se** |
|--|--|
| Oprette godkendelsesworkflowbrugere, angive, hvordan brugere modtager notifikationer, og oprette nye arbejdsgange. (Sådan oprettes nye workflows til ikke-understøttede scenarier, implementeres de krævede workflowelementer ved at tilpasse programkoden.) | [Konfigurer godkendelsesworkflow](across-set-up-workflows.md) |
| Aktiver godkendelsesworkflows, behandl meddelelser i arbejdsgangen, herunder godkendelser og godkendelsesanmodninger om at udføre trin i en arbejdsgang. Arkiver og slet arbejdsgange. | [Bruge godkendelsesworkflows](across-use-workflows.md) |

<!--
| Integrate company data with Power Automate workflows, using both internal and external sources and events to create and automate tasks or workflows. | [Use Power Automate Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |-->

## Se også

[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Administrere projekter](projects-manage-projects.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Fejlfinde dine [!INCLUDE[prod_short](includes/prod_short.md)] Automatiserede workflows](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
