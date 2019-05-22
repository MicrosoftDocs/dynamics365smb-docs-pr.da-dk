---
title: Forbinde dataene med Flow | Microsoft Docs
description: Du kan gøre dine Business Central-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette et automatiseret workflow.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 1652c4bc22425bd6df4ac303a96a2ab1b28bfaf9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241092"
---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i et automatisk workflow
Du kan bruge dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del af en arbejdsproces i Microsoft Flow.

> [!NOTE]
> Ud over Microsoft Flow kan du bruge funktionen Workflow i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vær opmærksom på, selvom det er to separate workflowsystemer, tilføjes en Flow-skabelon, du opretter med Microsoft Flow, på listen over workflowskabeloner i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Workflow](across-workflow.md).  

> [!NOTE]  
>   Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Sådan tilføjes [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow
1. Gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/) i din webbrowser, og log på.
2. Vælg **Mine Flows** på båndet øverst på siden.
3. Der er to måder at oprette et flow på: **Opret fra skabelon** og **Opret fra tom**. En skabelon er et foruddefineret flow, der er oprettet for dig.  Hvis du vil bruge skabelonen, skal du blot vælge den og oprette en forbindelse for hver tjeneste, skabelonen bruger. Med en tom skabelon kan du oprette et nyt flow helt forfra.
4. Hvis du vil oprette fra tom, skal du på siden **Mine Flows** vælge indstillingen **Opret fra tom**.
5. Søg efter **Konnektor til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
6. På listen over tilgængelige udløsere, skal du vælge en af de [!INCLUDE[d365fin](includes/d365fin_md.md)]-udløsere, der er tilgængelige:  
    *Når der anmodes om godkendelse af en debitor*,  
    *Når der anmodes om godkendelse af en finanskladdekørsel*,  
    *Når der anmodes om godkendelse af en finanskladdelinje*,  
    *Når der anmodes om godkendelse af en vare*,  
    *Når der anmodes om godkendelse af et købsdokument*,  
    *Når der anmodes om godkendelse af et salgsdokument* eller  
    *Når der anmodes om godkendelse af en kreditor*.
7. Du bliver bedt om at vælge en virksomhed i din [!INCLUDE[d365fin](includes/d365fin_md.md)]-lejer samt de betingelser i dine data, du vil overvåge.

Nu har du oprettet forbindelse til dine Business Central-data og er klar til at opbygge dit flow.

8. Hvis du vil oprette fra en skabelon, skal du vælge indstillingen **Opret fra skabelon**.
9. Søg efter **Skabeloner til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
10. På listen over tilgængelige skabeloner, skal du vælge en af skabelonerne.  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-salgsordre*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-salgstilbud*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-salgsfaktura*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-salgskreditnota*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-debitor*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-købsordre*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-købsfaktura*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-købskreditnota*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-vare*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-kreditor*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-finanskladdekørsel*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-finanskladdelinjer*.  
11. Flow beder dig om at vælge et firma i din [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-lejer. Da hvert trin i flowet er uafhængigt af det næste, kan du blive nødt til at definere virksomheden flere gange, når du bruger en [!INCLUDE[d365fin_md](includes/d365fin_md.md)] Flow-skabelon.

Du kan finde flere oplysninger i [Flow-dokumentationen](https://docs.microsoft.com/en-us/flow/getting-started).

For fejlfinding i forbindelse med din Microsoft Flow se [Fejlfinding af integration med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Se også
[Introduktion](product-get-started.md)  
[Workflow](across-workflow.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)   
[Administrere [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-workflows](across-use-workflows.md)  
[Brugeropsætning af godkendelser](across-how-to-set-up-approval-users.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
