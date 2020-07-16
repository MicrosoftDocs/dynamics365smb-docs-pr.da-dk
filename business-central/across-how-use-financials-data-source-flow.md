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
ms.date: 04/01/2020
ms.author: bmeier
ms.openlocfilehash: c2fbd841332ff48bd4716a082b0c9ef2bb9ac6df
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528984"
---
# <a name="using-prodshort-in-an-automated-workflow"></a>Bruge [!INCLUDE[prodshort](includes/prodshort.md)] i et automatisk workflow

Du kan bruge dine [!INCLUDE[prodshort](includes/prodshort.md)]-data som en del af en arbejdsproces i Microsoft Power Automate.

> [!NOTE]
> Ud over Power Automate kan du bruge funktionen Workflow i [!INCLUDE[prodshort](includes/prodshort.md)]. Vær opmærksom på, at selv om det er to separate workflowsystemer, tilføjes en hvilken som helst workflow-skabelon, du opretter med Power Automate, på listen over workflows i [!INCLUDE[prodshort](includes/prodshort.md)]. Du kan finde flere oplysninger i [Workflow](across-workflow.md).  

> [!NOTE]  
> Du skal have en gyldig konto til [!INCLUDE[prodshort](includes/prodshort.md)] og til Power Automate.  

## <a name="to-add-prodshort-as-a-data-source-in-power-automate"></a>Sådan tilføjes [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power Automate

1. Gå til [flow.microsoft.com](https://flow.microsoft.com) i din webbrowser, og log på.
2. Vælg **Mine flows** på båndet øverst på siden.
3. Der er tre måder at oprette et flow på: **Start fra skabelon**, **Start fra bunden** og **Start fra en connector**. En skabelon er et foruddefineret flow, der er oprettet for dig. Hvis du vil bruge skabelonen, skal du blot vælge den og oprette en forbindelse for hver tjeneste, skabelonen bruger. Med indstillingerne **Start fra bunden** og **Start fra en connector** kan du oprette et nyt flow helt fra bunden.
4. Hvis du vil starte fra bunden, skal du på siden **Mine flows** vælge indstillingerne **Start fra bunden** og **Automatiseret flow**.
5. Søg efter **Konnektor til [!INCLUDE[prodlong](includes/prodlong.md)]**.
6. Angiv et navn, og vælg den udløser, du vil bruge til flowet.
7. På listen over tilgængelige udløsere, skal du vælge en af de [!INCLUDE[prodshort](includes/prodshort.md)]-udløsere, der er tilgængelige:  

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

8. Power Automate anmoder dig om at vælge et miljø og en virksomhed i din [!INCLUDE[prodshort](includes/prodshort.md)]-lejer samt de betingelser i dine data, som du vil holde øje med.

    > [!NOTE]
    > [!INCLUDE[prodshort](includes/prodshort.md)]-connectoren til Power Automate understøtter flere produktions- og sandkassemiljøer. Hvis du ikke har oprettet flere produktions- eller sandkassemiljøer, er **Produktion** den eneste tilgængelige indstilling.  

    Nu har du oprettet forbindelse til dine Business Central[!INCLUDE[prodshort](includes/prodshort.md)]-data og er klar til at opbygge dit flow.

9. Hvis du vil oprette fra en skabelon, skal du vælge indstillingen **Start fra skabelon**.
10. Søg efter **Skabeloner til [!INCLUDE[prodlong](includes/prodlong.md)]**.
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
12. Power Automate viser en liste over de tjenester, der er anvendt i flow-skabelonen og vil automatisk forsøge at oprette forbindelse til disse tjenester. Hvis du ikke tidligere har oprettet forbindelse til en tjeneste, bliver du bedt om at logge på hver af de tjenester, du har brug for at oprette forbindelse til. Der vises en grøn markering ud for hver enkelt tjeneste, når der er oprettet en forbindelse. Vælg **Fortsæt**.
13. Power Automate vil anmode dig om at vælge et miljø og en virksomhed i din [!INCLUDE[prodshort](includes/prodshort.md)]-lejer. Da hvert trin i flowet er uafhængigt af det næste, kan du blive nødt til at definere miljøet og virksomheden flere gange, når du bruger en [!INCLUDE[prodshort](includes/prodshort.md)] Power Automate-skabelon.

Du kan finde flere oplysninger under [Dokumentation for Power Automate](/power-automate/getting-started).

## <a name="see-also"></a>Se også

[Introduktion](product-get-started.md)  
[Workflow](across-workflow.md)  
[Importer virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md)  
[Administrere [!INCLUDE[prodlong](includes/prodlong.md)]-workflows](across-use-workflows.md)  
[Brugeropsætning af godkendelser](across-how-to-set-up-approval-users.md)  
[Opsætning af [!INCLUDE[prodshort](includes/prodshort.md)]](setup.md)  
[Finans](finance.md)  
