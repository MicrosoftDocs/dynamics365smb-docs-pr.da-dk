---
title: Brug Power Automate-flows i Business Central
description: Konfigurere og bruge Power Automate-flows til at oprette og redigere Business Central-data.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Power Automate,'
ms.search.form: '1500,'
ms.date: 06/07/2024
ms.custom: bap-template
---

<!-- Line 41 says there are three cloud flow types, but the table lists four. Should line 41 change? -->


# <a name="use-power-automate-flows-in-"></a>Brug Power Automate-flows i [!INCLUDE[prod_short](includes/prod_short.md)]

Med [!INCLUDE[prod_short](includes/prod_short.md)] får du en licens til Microsoft Power Automate. Med denne licens kan du bruge dine [!INCLUDE[prod_short](includes/prod_short.md)]-data som en del af en arbejdsproces i Microsoft Power Automate. Du opretter flows og opretter forbindelse til dine data fra interne og eksterne kilder med [!INCLUDE [prod_short](includes/prod_short.md)]-connectoren.

Power Automate-flows udløses af hændelser, f. eks. en post blev oprettet, ændret eller slettet. Flows kan også køres på en brugerdefineret plan eller efter behov.

> [!NOTE]
> Administratorer kan begrænse adgangen til Power Automate. Hvis du opdager, at du ikke har adgang til nogle af eller alle de funktioner, der er beskrevet i denne artikel, skal du kontakte din administrator. Hvis du vil vide, hvordan du kan styre Power Automate Access som administrator, skal du se [Konfigurere Power Automate-integration](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

<!-- You must have a valid account with both [!INCLUDE[prod_short](includes/prod_short.md)] and Power Automate. --> 

> [!TIP]
> Ud over Power Automate kan du bruge skabeloner til godkendelse af workflow i [!INCLUDE[prod_short](includes/prod_short.md)]. Vær opmærksom på, at selv om det er to separate workflowsystemer, tilføjes en hvilken som helst workflow-skabelon, du opretter med Power Automate, på listen over workflows i [!INCLUDE[prod_short](includes/prod_short.md)]. Flere oplysninger i [Workflows](across-workflow.md).

## <a name="about-power-automate-flows"></a>Om Power Automate-flows

Power Automate er en tjeneste, der hjælper dig med at oprette automatiserede arbejdsgange (eller flows) mellem apps og tjenester, som [!INCLUDE[prod_short](includes/prod_short.md)]. Power Automate-flows kræver lidt eller ingen viden om kodning De kan knyttes til en lang række hændelser og svar, f. eks.:

- Postændringer
- Opdateringer af eksterne filer
- Bogførte dokumenter
- Forskellige Microsoft-og tredjepartstjenester, f. eks Microsoft Outlook, Excel, Dataverse, Teams, SharePoint, Power Apps og meget mere.

Der er tre forskellige Cloudflow-typer, som du kan arbejde med:

|Flowtype|Beskrivelse|
|---------|-----------|
|Automatiserede flows|Denne flowtype køres automatisk af en hændelse. I [!INCLUDE[prod_short](includes/prod_short.md)] kan en hændelse være, når en post eller et dokument oprettes, ændres eller slettes. F.eks. kan en ny salgsfaktura udløse et flow for en godkendelsesanmodning, som kan angive forskellige hændelser afhængigt af godkenderens svar. Et negativ svar sender en besked og sender en e-mail til den, der har anmodet om godkendelse. Et positivt svar opdateres samtidig med et Excel-regneark, der er placeret i en SharePoint-mappe, og der sendes en opdatering til Teams-chatten. Automatiske flows kan startes af både interne og eksterne hændelser i [!INCLUDE[prod_short](includes/prod_short.md)].|
|Godkendelsesflow|Godkendelsesflow er også automatiserede flows i Power Automate, men de er designet specielt til at anmode om godkendelse, når der foretages ændringer af poster og data. Du kan bruge godkendelsesflow i Power Automate som et alternativ til den [godkendelsesarbejdsgangsfunktion](across-use-workflows.md), der er en del af [!INCLUDE[prod_short](includes/prod_short.md)]. |
|Planlagt flow|Denne type flow køres også automatisk, men kører periodisk på planlagt dato og klokkeslæt. |
|Øjeblikkeligt flow|Denne flowtype kører efter anmodning og kræver, at brugeren kører den manuelt fra en knap eller handling i en anden app eller enhed, i dette tilfælde [!INCLUDE[prod_short](includes/prod_short.md)]-klienten. Øjeblikkelige flows fungerer på samme måde som batch genveje, så der udføres flere længde trin med et par tryk på knappen og de startes fra bestemte sider eller tabeller. Et flow kan f.eks. føje en knap til menuen handling på siden **Kreditorer** for at blokere betalinger til en leverandør og samtidig sende brugerdefinerbare e-mails til leverandørens kontakt og din virksomheds indkøbere og opdatere kontakten i Outlook. |

## <a name="power-automate-features"></a>Power Automate-funktioner

Du kan gennemse alle de Power Automate-flow, der i øjeblikket er tilgængelige, ved at logge på [Power Automate](https://powerautomate.com) og vælge **Mine flows** fra navigationslinjen til venstre. Her finder du de flows, du allerede har oprettet, og som du har delt med dig af en administrator eller kollega.

- Du kan også bruge øjeblikkelige flows til at køre direkte fra de fleste liste-, kort-og dokumentsider i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde de øjeblikkelige flows i handlingsgruppen **Automatisering** på siderne i handlingspanelet. Hvis du vil køre et flow, skal du markere den og følge instruktionerne. Der er flere oplysninger i afsnittene herunder.

- Med automatiske flows i [!INCLUDE[prod_short](includes/prod_short.md)] er det ikke nødvendigt at gøre noget, medmindre du vil ændre dem eller deaktivere dem. Ellers fungerer de bare, når de udløses. 
<!--

## <a name="automated-flows"></a>Automated flows

With Power Automate, you can create business flows directly in-house and rely on citizen developers. Automated workflows can be started by both internal and external events in [!INCLUDE[prod_short](includes/prod_short.md)], and also be set to run periodically. Learn more and get instructions on how to create flows in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

-->

## <a name="run-instant-flows"></a>Kør øjeblikkelige flows

Øjeblikkelige flows åbnes online i [!INCLUDE [prod_short](includes/prod_short.md)], så du kan forblive inden for rammerne af den forretningsproces, du var midt i. Du kan køre et hurtigt flow fra de fleste lister, kort eller dokumenter.

1. Vælg **Automatiser** på handlingslinjen, og vælg derefter et flow fra listen over tilgængelige flows under **Power Automate**-handlingen.

    :::image type="content" source="media/power-automate-instant-menu.svg" alt-text="Viser handlingen Automatiser med øjeblikkelige flowhandlinger.":::

    På nogle sider er **automatiser** indlejret i de **Flere indstillinger (...)**. 
2. Udfyld alle obligatoriske felter i ruden **Kør flow**, og vælg derefter **Fortsæt** for at køre flowet.

> [!NOTE]
> Første gang du bruger elementet **Automatiser**, kan du kun se funktionen **Introduktion til Power Automate**. Du kan se denne handling, fordi der ikke er aftalt noget fortrolighedsvarsel for Microsoft Power Automate. Hvis du vil fortsætte, skal du vælge **Kom i gang med Power Automate** og følge instruktionerne for at acceptere eller blive enige om.  
>
> :::image type="content" source="media/power-automate-action.png" alt-text="Viser Automatiseringselementet på handlingslinjen.":::

<!--

[!INCLUDE [prod_short](includes/prod_short.md)] can run a Power Automate flow from most list, card, and document pages. Once the admin has connected [!INCLUDE [prod_short](includes/prod_short.md)] with Power Automate, you'll see any flows your organization has added when you choose the **Automate** action on the relevant pages. Instant flows are run without leaving [!INCLUDE [prod_short](includes/prod_short.md)]. Learn more in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

These instant flows open on a page inside [!INCLUDE [prod_short](includes/prod_short.md)] online so you can remain within the context of the business process you were in the middle of. Choose the **Automate** action—on some pages nested under the **More Options** menu—choose the **Power Automate** menu item, then choose the relevant link to trigger the workflow. The connection to Power Automate is already set up for you.

Most flows require you to fill in a field or two before you choose the **Run flow** action.

> [!TIP]
> If you don't see an **Automate** action, then your [!INCLUDE [prod_short](includes/prod_short.md)] probably hasn't yet been set up to use Power Automate. Learn more from your admin.-->

## <a name="create-edit-and-manage-flows"></a>Opret, rediger og administrer flows

Du kan oprette nye flows eller ændre og administrere eksisterende, f.eks. at aktivere eller deaktivere dem, direkte i Power Automate. Men du kan starte nogle af disse opgaver fra Automatiser handling-menuen i [!INCLUDE[prod_short](includes/prod_short.md)]:

:::image type="content" source="media/power-automate-menu.svg" alt-text="Viser handlingen Automatiser på handlingslinjen med udvidede handlinger.":::

- Hvis du vil oprette en automatiseret proces fra en liste, et kort eller en dokumentside, skal du vælge **Automatiser** > **Opret automatiseret flow**.
- Hvis du vil oprette et godkendelsesflow fra et kort eller en dokumentside, skal du vælge **Automatiser** > **Opret godkendelsesflow**.

  > [!TIP]
  > Denne handling er kun tilgængelig på kort- og dokumenttypesider. ikke lister.
- Hvis du vil oprette en hurtig proces fra en liste, et kort eller en dokumentside, skal du vælge **Automatiser** > **Opret handling baseret på et flow**.
- Hvis du vil åbne Power Automate fra en liste, et kort eller en dokumentside, skal du vælge **Automatiser** > **Administrer flows**.
<!--- To create new flows or manage existing flows from inside [!INCLUDE[prod_short](includes/prod_short.md)], got to the **Manage Power Automate Flows** page.-->

Disse opgaver udføres typisk kun af administratorer eller superbrugere. Opgaverne kræver en større viden om forretningsprocesserne i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i følgende artikler i Business Central hjælp til udviklere og it-eksperter:

- [Power Automate integration](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-overview)
- [Oprette automatiserede flows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) (dækker også godkendelsesflows)
- [Opret øjeblikkelige flows](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)
- [Håndtér Power Automate-flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)
<!-- 

## <a name="add-more-automated-flows-and-instant-flows"></a>Add more automated flows and instant flows

You can create flows through the [powerautomate.microsoft.com](https://powerautomate.microsoft.com) website. However, if your admin has switched on the capability to run Power Automate flows from inside [!INCLUDE [prod_short](includes/prod_short.md)] online, you can start the process of building a flow from the **Automate** action on the relevant pages, which can be found under the **More Options** menu depending on the page. Then choose the **Power Automate** menu item, and then choose the **Create a flow** action. Power Automate then opens in a new browser tab, and you're signed in automatically.

You can find sample templates to adapt to your company and all available trigger events, using both [!INCLUDE [prod_short](includes/prod_short.md)] and external tools, by choosing the **Connectors** menu on the Power Automate website. Learn more about available templates and triggers in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

## <a name="create-and-manage-power-automate-flows"></a>Create and manage Power Automate flows

You can create new flows or manage existing Power Automate flows in [!INCLUDE [prod_short](includes/prod_short.md)] on the **Manage Power Automate Flows** page. Learn more in the [Manage Power Automate Flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) article in the administration content.

<!--
You can also manage available Power Automate workflows on the **Workflows** page in [!INCLUDE[prod_short](includes/prod_short.md)]. The page lists both the built-in approval and Power Automate workflows, with options for the latter to enable/disable, delete, and view the workflow on the Power Automate website.-->

## <a name="see-also"></a>Se også

[Fejlfinde dine [!INCLUDE[prod_short](includes/prod_short.md)] Automatiserede workflows](across-flow-troubleshoot.md)  
[Gør dig klar til at komme i gang](ui-get-ready-business.md)  
[Workflows](across-workflow.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Økonomistyring](finance.md)  
[Håndtér Power Automate-flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Konfigurere automatiserede workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Skift til hurtige flows](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
