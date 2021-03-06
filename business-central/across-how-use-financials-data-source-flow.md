---
title: Forbind dine data med Power Automate| Microsoft Docs
description: Du kan gøre dine Business Central-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette et automatiseret workflow.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f44b727a353208d1b2b8f5d918400de1687acc52
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754538"
---
# <a name="using-prod_short-in-an-automated-workflow"></a>Bruge [!INCLUDE[prod_short](includes/prod_short.md)] i et automatisk workflow

Du kan bruge dine [!INCLUDE[prod_short](includes/prod_short.md)]-data som en del af en arbejdsproces i Microsoft Power Automate.

> [!NOTE]
> Ud over Power Automate kan du bruge funktionen Workflow i [!INCLUDE[prod_short](includes/prod_short.md)]. Vær opmærksom på, at selv om det er to separate workflowsystemer, tilføjes en hvilken som helst workflow-skabelon, du opretter med Power Automate, på listen over workflows i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Workflow](across-workflow.md).  

> [!NOTE]  
> Du skal have en gyldig konto til [!INCLUDE[prod_short](includes/prod_short.md)] og til Power Automate.  

## <a name="to-add-prod_short-as-a-data-source-in-power-automate"></a>Sådan tilføjes [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power Automate

1. Gå til [flow.microsoft.com](https://flow.microsoft.com) i din webbrowser, og log på.
2. Vælg **Mine flows** på båndet øverst på siden.
3. Der er tre måder at oprette et flow på: **Start fra skabelon**, **Start fra bunden** og **Start fra en connector**. En skabelon er et foruddefineret flow, der er oprettet for dig. Hvis du vil bruge skabelonen, skal du blot vælge den og oprette en forbindelse for hver tjeneste, skabelonen bruger. Med indstillingerne **Start fra bunden** og **Start fra en connector** kan du oprette et nyt flow helt fra bunden.
4. Hvis du vil starte fra bunden, skal du på siden **Mine flows** vælge indstillingerne **Start fra bunden** og **Automatiseret flow**.
5. Søg efter **Konnektor til [!INCLUDE[prod_long](includes/prod_long.md)]**.
6. Angiv et navn, og vælg den udløser, du vil bruge til flowet.
7. På listen over tilgængelige udløsere, skal du vælge en af de [!INCLUDE[prod_short](includes/prod_short.md)]-udløsere, der er tilgængelige:  

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

8. Power Automate anmoder dig om at vælge et miljø og en virksomhed i din [!INCLUDE[prod_short](includes/prod_short.md)]-lejer samt de betingelser i dine data, som du vil holde øje med.

    > [!NOTE]
    > [!INCLUDE[prod_short](includes/prod_short.md)]-connectoren til Power Automate understøtter flere produktions- og sandkassemiljøer. Hvis du ikke har oprettet flere produktions- eller sandkassemiljøer, er **Produktion** den eneste tilgængelige indstilling.  

    Nu har du oprettet forbindelse til dine Business Central[!INCLUDE[prod_short](includes/prod_short.md)]-data og er klar til at opbygge dit flow.

9. Hvis du vil oprette fra en skabelon, skal du vælge indstillingen **Start fra skabelon**.
10. Søg efter **Skabeloner til [!INCLUDE[prod_long](includes/prod_long.md)]**.
11. På listen over tilgængelige skabeloner, skal du vælge en af skabelonerne og derefter vælge **Opret**.  

    *Anmode om godkendelse af Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-salgsordre*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-salgstilbud*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-salgsfaktura*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-salgskreditnota*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-debitor*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-købsordre*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-købsfaktura*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-købskreditnota*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-vare*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-kreditor*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-finanskladdekørsel* eller    
    *Anmode om godkendelse af Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-finanskladdelinjer*.  
12. Power Automate viser en liste over de tjenester, der er anvendt i flow-skabelonen og vil automatisk forsøge at oprette forbindelse til disse tjenester. Hvis du ikke tidligere har oprettet forbindelse til en tjeneste, bliver du bedt om at logge på hver af de tjenester, du har brug for at oprette forbindelse til. Der vises en grøn markering ud for hver enkelt tjeneste, når der er oprettet en forbindelse. Vælg **Fortsæt**.
13. Power Automate vil anmode dig om at vælge et miljø og en virksomhed i din [!INCLUDE[prod_short](includes/prod_short.md)]-lejer. Da hvert trin i flowet er uafhængigt af det næste, kan du blive nødt til at definere miljøet og virksomheden flere gange, når du bruger en [!INCLUDE[prod_short](includes/prod_short.md)] Power Automate-skabelon.

Du kan finde flere oplysninger under [Dokumentation for Power Automate](/power-automate/getting-started).

## <a name="see-also"></a>Se også

[Introduktion](product-get-started.md)  
[Workflow](across-workflow.md)  
[Importer virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md)  
[Administrere [!INCLUDE[prod_long](includes/prod_long.md)]-workflows](across-use-workflows.md)  
[Brugeropsætning af godkendelser](across-how-to-set-up-approval-users.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]