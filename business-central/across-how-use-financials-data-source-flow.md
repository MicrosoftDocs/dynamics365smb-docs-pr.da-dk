---
title: Brug Business Central i Power Automate-flows
description: Oprette og bruge Power Automate-flows, der opretter eller redigerer Business Central-data.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: 93eb177ff9ba102277a50f9686ea941df33d5563
ms.sourcegitcommit: 13ac10624bee47c73989b2b20942a01c849b4a6a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2022
ms.locfileid: "8744106"
---
# <a name="use-prod_short-in-power-automate-flows"></a>Brug [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate flows

Du kan bruge dine [!INCLUDE[prod_short](includes/prod_short.md)]-data som en del af en arbejdsproces i Microsoft Power Automate. Opret dine egne flow og opret forbindelse til dine data med [!INCLUDE [prod_short](includes/prod_short.md)]-connectoren.  

> [!NOTE]  
> Du skal have en gyldig konto til [!INCLUDE[prod_short](includes/prod_short.md)] og til Power Automate.  

> [!TIP]
> Ud over Power Automate kan du bruge skabeloner til godkendelse af workflow i [!INCLUDE[prod_short](includes/prod_short.md)]. Vær opmærksom på, at selv om det er to separate workflowsystemer, tilføjes en hvilken som helst workflow-skabelon, du opretter med Power Automate, på listen over workflows i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Workflow](across-workflow.md).  

## <a name="automated-workflows"></a>Automatiserede workflows

Med Power Automate kan du oprette forretningsflows direkte internt og stole på almindelige udviklere. Du kan finde flere oplysninger i [Konkfigurere automatiserede workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrationsindholdet.  

## <a name="manual-instant-flows"></a>Manuelle øjeblikkelige flows

Med start i maj 2022, kan en administrator via [!INCLUDE [prod_short](includes/prod_short.md)] online [aktivere en funktion](admin-feature-management.md) for at gøre det muligt at køre et Power Automate-flow fra de fleste sider. Du kan finde flere oplysninger i [Konkfigurere automatiserede workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrationsindholdet.  

Når administratoren har oprettet forbindelse [!INCLUDE [prod_short](includes/prod_short.md)] til Power Automate, kan du se de flow, som organisationen har tilføjet, når du vælger handlingen **Automatisering** på de relevante sider. Du kører flows uden at forlade [!INCLUDE [prod_short](includes/prod_short.md)].  

Disse automatiserede workflows åbnes i en rude i [!INCLUDE [prod_short](includes/prod_short.md)] onlinetilstand, så du forbliver inden for rammerne af den forretningsproces, du var midt i. På nogle sider kan funktionen **Automatisk** skjules under **Flere indstillinger**, men find den, vælg **Power Automate**-menupunktet og derefter vælge det relevante link, der udløser arbejdsprocessen. Forbindelsen til Power Automate er allerede konfigureret for dig.  

De fleste flows kræver, at du udfylder et felt eller to, før du vælger handlingen **Kør flow**.  

> [!TIP]
> Hvis du ikke kan se handlingen **Automatiser**, er din computer [!INCLUDE [prod_short](includes/prod_short.md)] muligvis ikke konfigureret til at bruge Power Automate. Kontakt administratoren for at få flere oplysninger.

## <a name="add-more-automated-flows-and-manual-instant-flows"></a>Tilføje flere automatiserede flows og manuelle øjeblikkelige flows

Du kan oprette flows på [powerautomate.microsoft.com](https://powerautomate.microsoft.com)-websted. Hvis administratoren har aktiveret muligheden for at køre Power Automate flows fra [!INCLUDE [prod_short](includes/prod_short.md)] online, kan du dog starte processen med at bygge et flow fra handlingen **Automatiser** på de relevante sider. På nogle sider kan handlingen **Automatiser** skjules under menuen **Flere indstillinger**, find den, vælg **Power Automate**-menupunktet og vælg derefter handlingen **Opret et flow**. Power Automate derefter åbnes en ny webbrowser-fane, og du bliver logget på automatisk.

## <a name="manage-workflows"></a>Administrere workflows

Du kan få vist en oversigt over alle de workflows, du har adgang til, ved at vælge handlingen **Administrer workflows** i menuen **Power Automate**. Listen åbnes i en ny webbrowser-fane, og du bliver automatisk logget på Power Automate. Der kan du se, hvornår hvert flow har kørt for nylig.  

## <a name="see-also"></a>Se også

[Fejlfinde dine [!INCLUDE[prod_short](includes/prod_short.md)] Automatiserede workflows](across-flow-troubleshoot.md)  
[Bliv klar til at agere](ui-get-ready-business.md)  
[Workflows](across-workflow.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  
[Konfigurere automatiserede workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]