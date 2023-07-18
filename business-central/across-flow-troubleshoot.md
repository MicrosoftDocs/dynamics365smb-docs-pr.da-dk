---
title: Fejlfinding i forbindelse med dine automatiserede workflows
description: 'Få mere at vide om, hvordan du foretager fejlfinding af forbindelsen mellem Business Central og Power Automate, når du opretter et automatiseret workflow.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions, Power Automate,'
ms.date: 07/03/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: d365-business-central
---

# <a name="troubleshoot-your--automated-workflows"></a>Fejlfinde dine [!INCLUDE[prod_short](includes/prod_short.md)] automatiserede workflows

Når du opretter forbindelse [!INCLUDE [prod_short](includes/prod_short.md)] med Power Automate for at oprette automatiserede arbejdsproces, kan du få brug for fejlmeddelelser. Denne artikel giver løsningsforslag til tilbagevendende problemer.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Flow kører ikke på alle poster, der er oprettet eller ændret

### <a name="problem"></a>Problem

Hvis en hændelse opretter eller ændrer mange poster, køres flowet ikke på nogle eller alle poster.

### <a name="possible-cause"></a>Mulig årsag

Der er i øjeblikket en grænse for, hvor mange poster et flow kan behandle. Hvis der oprettes eller ændres mere end 1000 poster inden for 30 sekunder, udløses flowet ikke.

> [!NOTE]
> For udviklere udføres flow-udløseren via webhook-beskeder, og denne begrænsning skyldes den måde, Business Central-connector håndterer `collection` meddelelser på. Flere oplysninger under [Arbejde med Webhooks i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) i hjælp til udvikler og administrator.

## <a name="the-response-from-the-business-central-service-is-too-large-error"></a>Fejlen "Svaret fra Business Central-tjenesten er for langt"

### <a name="problem-1"></a>Problem

Når du bruger en handling, der interagerer med poster (som f. eks. *Opret post (v3)* og *Hent post (v3)*), vises der muligvis en fejl i Power Automate, som ligner denne:

`The response from the Business Central service is too large`

### <a name="possible-cause-1"></a>Mulig årsag

Selvom Business Central ikke har angivet en grænse for størrelsen på poster, der returneres af API'er, kan Dynamics 365 Business Central-connectoren til Power Automate kun håndtere poster på op til 8 MB.

Alle de Business Central-API'er, der leveres af Microsoft, returnerer poster under denne grænse, men det gør API'er, der leveres af partnere, muligvis ikke. Hvis du får vist fejlmeddelelsen "Svaret fra Business Central-tjenesten er for langt", skal du kontakte den partner, der har oprettet den API, du bruger.

## <a name="entity-set-not-found-error"></a>Fejlen "Enhedssæt blev ikke fundet"

### <a name="problem-2"></a>Problem

Når du opretter et nyt Power Automate-flow ved hjælp af en [!INCLUDE[prod_short](includes/prod_short.md)]-godkendelsesudløser som f.eks. *Når der anmodes om godkendelse af et købsdokument*, vises der evt. en fejlmeddelelse i stil med:

`Entity set not found: \<name\>`

Pladsholderen `\<name\>` er er navnet på den manglende webtjeneste, f.eks. *workflowWebhookSubscriptions* eller *workflowPurchaseDocumentLines*.

### <a name="possible-cause-2"></a>Mulig årsag

Brug af Power Automate til godkendelser kræver, at visse side- og codeunit-objekter udgives som webtjenester. Som standard udgives de fleste nødvendige objekter som webtjenester. Men i nogle tilfælde kan miljøet være blevet tilpasset, så disse objekter ikke længere udgives.

### <a name="fix"></a>Ret

Gå til siden **Webtjenester**, og kontroller, at følgende objekter er udgivet som webtjenester. Der skal være en post på listen for hvert objekt, hvor afkrydsningsfeltet **Udgivet** er markeret.  

| Objekttype | Objekt-id | Objektnavn | Tjenestenavn |
|--|--|--|--|
| Codeunit | 1544 | WorkflowWebhookSubscription | WorkflowActionResponse |
| Side | 6408 | workflowCustomers | workflowCustomers |
| Side | 6406 | workflowGenJournalBatches | workflowGenJournalBatches |
| Side | 6407 | workflowGenJournalLines | workflowGenJournalLines |
| Side | 6409 | workflowItems | workflowItems |
| Side | 6405 | Enhed for købsdokumentlinje | workflowPurchaseDocumentLines |
| Side | 6404 | workflowPurchaseDocuments | workflowPurchaseDocuments |
| Side | 6403 | Enhed for salgsdokumentlinje | workflowSalesDocumentLines |
| Side | 6402 | workflowSalesDocuments | workflowSalesDocuments |
| Side | 6410 | workflowVendors | workflowVendors |
| Side | 831 | workflowWebhookSubscriptions | workflowWebhookSubscriptions |

> [!NOTE]
> Værdien for **Tjenestenavn** skal være nøjagtigt som vist i tabellen. Undlad at ændre eller oversætte navnet på tjenesten.

Flere oplysninger om udgivelse af webtjenester under [Udgive en webtjeneste](across-how-publish-web-service.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/use-power-automate/).

## <a name="see-also"></a>Se også

[Brug Power Automate-flows i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)  
[Workflow](across-workflow.md)  
[Konfigurere automatiserede workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Skift til hurtige flows](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  
[Håndtér Power Automate-flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
