---
title: Oprette et sandkassemiljø | Microsoft Docs
description: Oprette et miljø til udforskning, læring, demonstration, udvikling og test.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 10/01/2019
ms.author: solsen
ms.openlocfilehash: d945a6b851c20479a4c8c83f38b8fc8ccdfd6765
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300421"
---
# <a name="creating-a-sandbox-environment"></a>Oprette et sandkassemiljø
Et sandkassemiljø (eksempelvisning) er en ikke-produktiv forekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)]. Isoleret fra produktion er et sandkassemiljø stedet, hvor du sikkert kan udforske, lære, demonstrere, udvikle og teste tjenesten uden risiko for at påvirke data og indstillinger i dit produktionsmiljø.

## <a name="to-create-a-sandbox-environment"></a>Sådan opretter du et sandkassemiljø
Du skal have abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)] for at kunne oprette et sandkassemiljø. Der kan kun være ét sandkassemiljø pr. abonnement.

1. Log ind på din produktionsforekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)]-tjenesten.

2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sandkassemiljø**, og vælg derefter det relaterede link.
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Vælg knappen **Opret**.  

    Der vises endnu en fane i [!INCLUDE[d365fin](includes/d365fin_md.md)], hvor du kan afslutte opsætningen af dit sandkassemiljø.

    > [!NOTE]  
    >  Hvis blokering af pop op-vinduer er aktiveret i din webbrowser, kan du ændre denne indstilling, så URL-adresser fra *.businesscentral.dynamics.com-adressen tillades.

4. Når sandkassemiljøet er klar, omdirigeres du til miljøet velkomstguide.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. Vælg knappen **Få mere at vide** for at læse om scenarier, som du kan afprøve i et sandkassemiljø, eller vælg knappen **Luk** for at fortsætte til rollecenteret i din sandkasseforekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)].

    Der vises en meddelelse om, at dette er et sandkassemiljø, øverst i rollecenteret. Du kan også se miljøtypen i titellinjen i klienten.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

    > [!NOTE]
    > Et sandkassemiljø, der oprettes på denne måde, indeholder kun standarddemonstrationsdataene for CRONUS-virksomheden. Der kopieres ikke eller på anden måde overføres data fra produktionsmiljøet.<br /><br />
    > Du kan også oprette et sandkassemiljø, der indeholder produktionsdataene. Dette skal gøres via Administrationscenter. Du kan finde flere oplysninger under [Administrere miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) i hjælpen til udviklere og it-eksperter.

6. Du kan når som helst vende tilbage til siden **Sandkassemiljø** og nulstille sandkassemiljøet.
    > [!NOTE]  
    >  Nulstilling af sandkassemiljøet vil fjerne miljøet helt, og derefter oprettes det igen med standarddemodata.  

7. Hvis du vil skifte mellem produktions- og sandkassemiljøerne, kan du bruge Business Central-appstarter.
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

8. Det er muligt for en administrator eller en anden bruger at begrænse eller endda blokere adgangen for bestemte brugere til sandkassemiljøet. Dette kan gøres ved hjælp af standardsikkerhedsfunktionerne i produktet, f.eks. brugerkort, brugergrupper og rettighedssæt.

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avancerede funktioner i sandkassemiljøet
### <a name="designer"></a>Designer
I et sandkassemiljø er **Designer** aktiveret. Du kan aktivere funktionen ved at vælge designikonet ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side.

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a>Sådan aktiveres den avancerede brugeroplevelse
Du kan aktivere og prøve alle de avancerede funktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] i en sandkasselejer ved at indstille feltet **Oplevelse** på siden **Virksomhedsoplysninger**.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Når du har aktiveret de avancerede funktioner i en sandkasselejer, kan du få adgang til alle standardprofiler (roller) og rollecentre. Du kan også oprette en evalueringsvirksomhed, der er fuldt defineret, herunder med demodata og adgang til avancerede områder af produktet.

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
