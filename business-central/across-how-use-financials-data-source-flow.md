---
title: Brug Power Automate-flows i Business Central
description: Konfigurere og bruge Power Automate-flows til at oprette og redigere Business Central-data.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Power Automate,
ms.search.form: 1500,
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: 369ee2b4aded272a8a3a21fe810b4b6c62dd1de0
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585425"
---
# <a name="use-power-automate-flows-in-prod_short"></a>Brug Power Automate-flows i [!INCLUDE[prod_short](includes/prod_short.md)]

Du kan bruge dine [!INCLUDE[prod_short](includes/prod_short.md)]-data som en del af en arbejdsproces i Microsoft Power Automate. Opret dine egne flows, og opret forbindelse til dine data fra interne og eksterne kilder med [!INCLUDE [prod_short](includes/prod_short.md)]-connectoren.

> [!NOTE]
> Du skal have en gyldig konto med både [!INCLUDE[prod_short](includes/prod_short.md)] og Power Automate.  

> [!TIP]
> Ud over Power Automate kan du bruge skabeloner til godkendelse af workflow i [!INCLUDE[prod_short](includes/prod_short.md)]. Vær opmærksom på, at selv om det er to separate workflowsystemer, tilføjes en hvilken som helst workflow-skabelon, du opretter med Power Automate, på listen over workflows i [!INCLUDE[prod_short](includes/prod_short.md)]. Flere oplysninger i [Workflows](across-workflow.md).

Power Automate-flows udløses af hændelser som f. eks. oprettelse, ændring eller sletning af dokumenter (automatiske flows). Flow kan også køres på en brugerdefineret plan (planlagte flows) eller efter behov (øjeblikkelige flows).

## <a name="power-automate-features-in-prod_short"></a>Power Automate-funktioner i [!INCLUDE[prod_short](includes/prod_short.md)]

Flows udvides på de indbyggede godkendelsesworkflows-funktioner, der er tilgængelige i [!INCLUDE[prod_short](includes/prod_short.md)] uden at skulle kode viden, og som kan knyttes til en lang række hændelser og svar, f. eks. postændringer, opdateringer af eksterne filer, bogførte dokumenter samt forskellige Microsoft-og tredjepartstjenester, f.eks. Microsoft Outlook, Microsoft Excel, Microsoft Dataverse, Microsoft Teams, Microsoft SharePoint, Microsoft Power Apps og meget mere.

F.eks. kan en ny salgsfaktura udløse et workflow for en godkendelsesanmodning, som kan angive forskellige hændelser afhængigt af godkenderens svar. Et negativ svar sender en besked og sender en e-mail til den, der har anmodet om godkendelse. Et positivt svar opdateres samtidig med et Excel-regneark, der er placeret i en SharePoint-mappe, og der sendes en opdatering til Teams-chatten.

Øjeblikkelige flows fungerer på samme måde som batch genveje, så der udføres flere længde trin med et par tryk på knappen og de startes fra bestemte sider eller tabeller. Et flow kan f.eks. føje en knap til menuen handling på siden **Kreditorer** for at blokere betalinger til en leverandør og samtidig sende brugerdefinerbare e-mails til leverandørens kontakt og din virksomheds indkøbere og opdatere kontakten i Outlook.

## <a name="automated-workflows"></a>Automatiserede workflows

Med Power Automate kan du oprette forretningsflows direkte internt og stole på almindelige udviklere. Automatiserede workflows kan startes af både interne og eksterne hændelser i [!INCLUDE[prod_short](includes/prod_short.md)] og indstilles til at køre regelmæssigt. Få mere at vide, og få instruktioner i, hvordan du opretter workflows, i artiklen [Konfigurere automatiserede arbejdsprocesser](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrationsindholdet.

## <a name="instant-flows"></a>Øjeblikkelige flows

Med start i 2022, udgivelsesbølge 1 (maj 2022) [!INCLUDE [prod_short](includes/prod_short.md)] kan online administratorer [aktivere en funktion](admin-feature-management.md) til at gøre det muligt at køre et Power Automate-flow fra de fleste lister, kort og dokumentsider. Du kan finde flere oplysninger i artiklen [Konfigurere automatiserede workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrationsindholdet.

Når administratoren har oprettet forbindelse mellem [!INCLUDE [prod_short](includes/prod_short.md)] og Power Automate, kan du se de flow, som organisationen har tilføjet, når du vælger handlingen **Automatisering** på de relevante sider. Øjeblikkelige flows kører uden at forlade [!INCLUDE [prod_short](includes/prod_short.md)].

Disse øjeblikkelige workflows åbnes på en side i [!INCLUDE [prod_short](includes/prod_short.md)] onlinetilstand, så du kan forblive inden for rammerne af den forretningsproces, du var midt i. På nogle sider kan funktionen **Automatisk** skjules under **Flere indstillinger**, men find den, vælg **Power Automate**-menupunktet og derefter vælge det relevante link, der udløser arbejdsprocessen. Forbindelsen til Power Automate er allerede konfigureret for dig.

De fleste flows kræver, at du udfylder et felt eller to, før du vælger handlingen **Kør flow**.

> [!TIP]
> Hvis du ikke kan se handlingen **Automatiser**, er din computer [!INCLUDE [prod_short](includes/prod_short.md)] muligvis ikke konfigureret til at bruge Power Automate. Få mere at vide fra din administrator.

## <a name="add-more-automated-flows-and-instant-flows"></a>Tilføje flere automatiserede flows og øjeblikkelige flows

Du kan oprette flows på [powerautomate.microsoft.com](https://powerautomate.microsoft.com)-websted. Hvis administratoren imidlertid har skiftet til muligheden for at køre Power Automate-flows fra [!INCLUDE [prod_short](includes/prod_short.md)] online, kan du starte processen med at bygge et flow fra den **automatiserede** handling på de relevante sider, som findes i menuen **Flere indstillinger**, der afhænger af siden. Vælg derefter menuemnet **Power Automate** og handlingen **Opret et flow**. Power Automate derefter åbnes en ny webbrowser-fane, og du bliver logget på automatisk.

Du kan finde eksempelskabeloner, der kan tilpasses din virksomhed, og alle tilgængelige udløserhændelser ved hjælp af både [!INCLUDE [prod_short](includes/prod_short.md)] og eksterne værktøjer ved at vælge menuen **Connectorer** på Power Automate-webstedet. Du kan finde flere oplysninger om tilgængelige skabeloner og udløsere i [Konfigurere automatiserede workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrationsindholdet.

## <a name="manage-automated-workflows"></a>Administrere automatiserede workflows

Du kan oprette nye flows eller administrere eksisterende Power Automate-flows i [!INCLUDE [prod_short](includes/prod_short.md)] på siden **Administrer Power Automate-flows**. Du kan finde flere oplysninger i artiklen [Administrere Power Automate-flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows.md) i administrationsindholdet.

Du kan også administrere tilgængelige Power Automate-workflows på siden **Workflows** i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden vises både indbyggede godkendelses- og Power Automate-workflows med indstillinger for den sidste for at aktivere/deaktivere, slette og få vist workflow på Power Automate-webstedet.

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/use-power-automate/)

## <a name="see-also"></a>Se også

[Fejlfinde dine [!INCLUDE[prod_short](includes/prod_short.md)] Automatiserede workflows](across-flow-troubleshoot.md)  
[Bliv klar til at agere](ui-get-ready-business.md)  
[Workflows](across-workflow.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  
[Håndtér Power Automate-flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Konfigurere automatiserede workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Skift til hurtige flows](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
