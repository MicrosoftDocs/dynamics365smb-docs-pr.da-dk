---
title: Arbejdsgange i dynamisk 365 Business central
description: Brug de indbyggede arbejdsgangsfunktioner til at konfigurere godkendelsesarbejdsgange for at supplere automatiserede arbejdsprocesser baseret på Power Automate. Du kan definere trin, der skal tildeles opgaver til forskellige personer som en del af de forskellige forretningsproces opgaver.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/12/2022
ms.author: edupont
ms.openlocfilehash: 84d4a87a0edab18be342b9ed5732de0350a31645
ms.sourcegitcommit: bc645e7ecb1940a85b2c433aa894d3494c9b10df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743667"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Workflows i Dynamics 365 Business Central

Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.  

Standardversionen af [!INCLUDE [prod_short](includes/prod_short.md)] understøtter tre typer arbejdsgange:

* Automatiserede godkendelsesarbejdsprocesser baseret på indbyggede arbejdsprocesskabeloner  

  På siden **workflow-skabeloner** kan du se alle tilgængelige arbejdsprocesser. Prøveversionen af [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en række forudkonfigurerede workflows, som repræsenteres af workflowskabeloner, som du kan kopiere for at oprette workflows. Når du åbner en arbejdsprocesskabelon fra siden **workflow-skabeloner**, og navnet på arbejdsprocessen starter med *MS-*, er arbejdsprocesskabelonen tilføjet af Microsoft.  
* Automatiske flows, som du selv opretter  

  Alle workflowskabeloner, som du opretter med, Power Automate, føjes til listen over workflowskabeloner i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Bruge Business Central i Power Automate Flows](across-how-use-financials-data-source-flow.md).  
* Manuelt udløste flows fra handlingen **Automatiser** ([!INCLUDE [prod_short](includes/prod_short.md)] kun online). Du kan finde flere oplysninger i [Manuelle øjeblikkelige flows](across-how-use-financials-data-source-flow.md#manual-instant-flows).  

## <a name="power-automate-flows"></a>Power Automate-flows

Du kan tilmelde dig [!INCLUDE [prod_short](includes/prod_short.md)] online Power Automate og derefter bygge effektive, automatiserede flow, som du kan køre fra [!INCLUDE [prod_short](includes/prod_short.md)]. Der er flere oplysninger i [Bruge [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate flows](across-how-use-financials-data-source-flow.md).  

## <a name="automated-approval-workflows"></a>Automatiserede godkendte workflows

Du opretter et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden.  

Hvis et virksomhedsscenarie kræver en arbejdsgangs hændelse eller-svar, som ikke understøttes i standardversionen, skal du tilmelde dig Power Automate. Der er flere oplysninger i [Bruge [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate flows](across-how-use-financials-data-source-flow.md). Du kan også få en app eller arbejde med en Microsoft-partner for at tilpasse programkoden.  

Hvis du vil oprette og bruge arbejdsprocesser, der ikke er defineret i Power Automate, skal du kontrollere følgende artikler:  

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Oprette arbejdsgangbrugere, angive, hvordan brugere modtager notifikationer, og oprette nye arbejdsgange. Implementer de krævede arbejdsgangelementer ved at tilpasse programkoden for nye arbejdsgange for ikke-understøttede scenarier.|[Opsætning af arbejdsgange](across-set-up-workflows.md)|  
|Aktiver arbejdsgange, behandl meddelelser i arbejdsgangen, herunder godkendelser og godkendelsesanmodninger om at udføre trin i en arbejdsgang. Arkiver og slet arbejdsgange.|[Bruge arbejdsgange](across-use-workflows.md)|  

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Administrere projekter](projects-manage-projects.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Brug [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate Flows](across-how-use-financials-data-source-flow.md)  
[Fejlfinde dine [!INCLUDE[prod_short](includes/prod_short.md)] Automatiserede workflows](across-flow-troubleshoot.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]