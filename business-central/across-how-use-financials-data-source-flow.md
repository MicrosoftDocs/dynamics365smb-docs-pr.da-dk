---
title: Forbinde dataene med Flow | Microsoft Docs
description: Du kan gøre dine Business Central-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette et automatiseret workflow.
documentationcenter: ''
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: 86178bafa806fb8cba531d5b78157437c242d432
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305020"
---
# <a name="using-included365finincludesd365fin_mdmd-in-an-automated-workflow"></a>Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i et automatisk workflow
Du kan bruge dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del af en arbejdsproces i Microsoft Flow.

> [!NOTE]
> Ud over Microsoft Flow kan du bruge funktionen Workflow i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vær opmærksom på, at selvom det er to separate workflowsystemer, tilføjes en Flow-skabelon, du opretter med Microsoft Flow, på listen over workflows i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Workflow](across-workflow.md).  

> [!NOTE]  
> Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Flow.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-flow"></a>Sådan tilføjes [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow
1. Gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/) i din webbrowser, og log på.
2. Vælg **Mine Flows** på båndet øverst på siden.
3. Der er tre måder at oprette et flow på. **Start fra skabelon**, **Start fra grunden** og **Start fra en connector**. En skabelon er et foruddefineret flow, der er oprettet for dig. Hvis du vil bruge skabelonen, skal du blot vælge den og oprette en forbindelse for hver tjeneste, skabelonen bruger. Med indstillingerne **Start fra grunden** og **Start fra en connector** kan du oprette et nyt flow helt fra grunden.
4. Hvis du vil oprette fra grunden, skal du på siden **Mine Flows** vælge indstillingerne **Start fra grunden** og **Automatiseret flow**.
5. Søg efter **Konnektor til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
6. Angiv et navn, og vælg den udløser, du vil bruge til flowet.
7. På listen over tilgængelige udløsere, skal du vælge en af de [!INCLUDE[d365fin](includes/d365fin_md.md)]-udløsere, der er tilgængelige:  
    
    *Når der anmodes om godkendelse af en kreditor*    
    *Når der anmodes om godkendelse af en finanskladdelinje*    
    *Når en post slettes*    
    *Når en post ændres*    
    *Når en post oprettes*    
    *Når en post redigeres*    
    *Når der anmodes om godkendelse af en finanskladdekørsel*   
    *Når der anmodes om godkendelse af en debitor*   
    *Når der anmodes om godkendelse af en vare*    
    *Når der anmodes om godkendelse af et købsdokument* eller     
     *Når der anmodes om godkendelse af et salgsdokument*.
     
8. Du bliver bedt om at vælge et miljø eller en virksomhed i din [!INCLUDE[d365fin](includes/d365fin_md.md)]-lejer samt de betingelser i dine data, du vil overvåge.

> [!NOTE]  
>   [!INCLUDE[d365fin](includes/d365fin_md.md)]-connectoren til Microsoft Flow understøtter flere produktions- og sandkassemiljøer. Hvis du ikke har oprettet flere produktions- eller sandkassemiljøer, er **Produktion** den eneste tilgængelige indstilling. 

Nu har du oprettet forbindelse til dine Business Central-data og er klar til at opbygge dit flow.

9. Hvis du vil oprette fra en skabelon, skal du vælge indstillingen **Start fra skabelon**.
10. Søg efter **Skabeloner til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
11. På listen over tilgængelige skabeloner, skal du vælge en af skabelonerne og derefter vælge **Opret**.  

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
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-finanskladdekørsel* eller    
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-finanskladdelinjer*.  
12. Flow viser en liste over de tjenester, der er anvendt i Flow-skabelonen og vil automatisk forsøge at oprette forbindelse til disse tjenester. Hvis du ikke tidligere har oprettet forbindelse til en tjeneste, bliver du bedt om at logge på hver af de tjenester, du har brug for at oprette forbindelse til. Der vises en grøn markering ud for hver enkelt tjeneste, når der er oprettet en forbindelse. Vælg **Fortsæt**.
13. Flow beder dig om at vælge et miljø eller en virksomhed i din [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-lejer. Da hvert trin i flowet er uafhængigt af det næste, kan du blive nødt til at definere miljøet og virksomheden flere gange, når du bruger en [!INCLUDE[d365fin_md](includes/d365fin_md.md)] Flow-skabelon.

Du kan finde flere oplysninger i [Flow-dokumentationen](/flow/getting-started).

## <a name="see-also"></a>Se også
[Introduktion](product-get-started.md)  
[Workflow](across-workflow.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Administrere brugere og rettigheder](ui-how-users-permissions.md)   
[Administrere [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-workflows](across-use-workflows.md)  
[Brugeropsætning af godkendelser](across-how-to-set-up-approval-users.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
