---
title: Fejlfinding i forbindelse med dine automatiserede workflows
description: Få mere at vide om, hvordan du foretager fejlfinding af forbindelsen mellem Business Central og Power Automate, når du opretter et automatiseret workflow.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: b8fff95ced93e7ee2a3112969f45525532b19445
ms.sourcegitcommit: e86f0bd15604c2fb327e3182929c44a4172790c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786192"
---
# <a name="troubleshoot-your-prod_short-automated-workflows"></a>Fejlfinde dine [!INCLUDE[prod_short](includes/prod_short.md)] automatiserede workflows

Når du opretter forbindelse [!INCLUDE [prod_short](includes/prod_short.md)] med Power Automate for at oprette automatiserede arbejdsproces, kan du få brug for fejlmeddelelser. Denne artikel giver løsningsforslag til ofte tilbagevendende problemer.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Flow kører ikke på alle poster, der er oprettet eller ændret

### <a name="problem"></a>Problem

Hvis en hændelse opretter eller ændrer mange poster, køres flowet ikke på nogle eller alle poster.

### <a name="possible-cause"></a>Mulig årsag

Der er i øjeblikket en grænse for, hvor mange poster et flow kan behandle. Hvis der oprettes eller ændres mere end 100 poster inden for 30 sekunder, udløses strømmen ikke.

> [!NOTE]
> For udviklere udføres flow-udløseren via webhook-beskeder, og denne begrænsning skyldes den måde, Business Central-connector håndterer `collection` meddelelser på. Du kan finde flere oplysninger i [Arbejde med Webhooks i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) i hjælp til udvikler og administrator.

## <a name="entity-set-not-found-error"></a>Fejlen "Enhedssæt blev ikke fundet"

### <a name="problem"></a>Problem

Når du opretter et nyt Power Automate-flow ved hjælp af en [!INCLUDE[prod_short](includes/prod_short.md)]-godkendelsesudløser som f.eks. *Når der anmodes om godkendelse af et købsdokument*, vises der evt. en fejlmeddelelse i stil med:

`Entity set not found: \<name\>`

Pladsholderen `\<name\>` er er navnet på den manglende webtjeneste, f.eks. *workflowWebhookSubscriptions* eller *workflowPurchaseDocumentLines*.

### <a name="possible-cause"></a>Mulig årsag

Brug af Power Automate til dine godkendelser kræver, at visse side- og codeunit-objekter udgives som webtjenester. Som standard udgives de fleste nødvendige objekter som webtjenester for dig. Men i nogle tilfælde kan miljøet være blevet tilpasset, så disse objekter ikke længere udgives.

### <a name="fix"></a>Rettelse

Gå til siden **Webtjenester**, og kontroller, at følgende objekter er udgivet som webtjenester. Der skal være en post på listen for hvert objekt, hvor afkrydsningsfeltet **Udgivet** er markeret.  

|Objekttype|Objekt-id|Objektnavn|Tjenestenavn|
|-----------|---------|-----------|------------|
|Codeunit|  1544    |WorkflowWebhookSubscription|WorkflowActionResponse|
|Side|  6408|   workflowCustomers|  workflowCustomers|
|Side   |6406   |workflowGenJournalBatches| workflowGenJournalBatches|
|Side   |6407   |workflowGenJournalLines|workflowGenJournalLines|
|Side   |6409   |workflowItems| workflowItems|
|Side   |6405   |Enhed for købsdokumentlinje|workflowPurchaseDocumentLines|
|Side|  6404    |workflowPurchaseDocuments| workflowPurchaseDocuments|
|Side|  6403    |Enhed for salgsdokumentlinje |workflowSalesDocumentLines|
|Side|  6402|   workflowSalesDocuments| workflowSalesDocuments|
|Side|  6410    |workflowVendors|   workflowVendors|
|Side|  831 |workflowWebhookSubscriptions|  workflowWebhookSubscriptions|

> [!NOTE]
> Værdien for **Tjenestenavn** skal være nøjagtigt som vist i tabellen. Undlad at ændre eller oversætte navnet på tjenesten.

Du kan finde flere oplysninger om udgivelse af webtjenester under [Udgive en webtjeneste](across-how-publish-web-service.md).

## <a name="see-also"></a>Se også

[Brug [!INCLUDE[prod_short](includes/prod_short.md)] i et autoamtisk workflow](across-how-use-financials-data-source-flow.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]