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
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 113c081e60b825c48cfb85ae3475a713a1a1e215
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "937942"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a>Oprette et sandkassemiljø
Et sandkassemiljø (eksempelvisning) er en ikke-produktiv forekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)]. Isoleret fra produktion er et sandkassemiljø stedet, hvor du sikkert kan udforske, lære, demonstrere, udvikle og teste tjenesten uden risiko for at påvirke data og indstillinger i dit produktionsmiljø.

## <a name="to-create-a-sandbox-environment"></a>Sådan opretter du et sandkassemiljø
Du skal have abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)] for at kunne oprette et sandkassemiljø. Der kan kun være ét sandkassemiljø pr. abonnement.

1. Log ind på din produktionsforekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)]-tjenesten.
2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sandkassemiljø**, og vælg derefter det relaterede link.
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Vælg **Opret**.  
  Der åbnes en anden fane i din webbrowser, hvor du kan afslutte opsætningen af sandkassemiljøet.
> [!NOTE]  
>  Hvis blokering af pop op-vinduer er aktiveret i din webbrowser, kan du ændre denne indstilling, så URL-adresser fra *.businesscentral.dynamics.com-adressen tillades.   

4. Når sandkassemiljøet er klar, omdirigeres du til miljøet velkomstguide.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. Vælg **Lær mere** for at læse om scenarier, som du kan prøve i et sandkassemiljø. Eller du kan vælge **Luk** for at fortsætte til rollecenteret for din [!INCLUDE[d365fin](includes/d365fin_md.md)]-sandkasseforekomst.
6. Der vises en meddelelse om, at dette er et sandkassemiljø, øverst i rollecenteret. Du kan også se miljøtypen i titellinjen i klienten.
<!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) --> I sandkassemiljøet er der blevet oprettet en ny lejer. Denne lejer er indlæst med standarddemodata for virksomheden CRONUS. Ingen data kopieres eller på anden måde overføres fra produktionsmiljøet under oprettelsen af sandkassen.

7. Du kan når som helst vende tilbage til siden **Sandkassemiljø** og nulstille sandkassemiljøet.
> [!NOTE]  
>  Nulstilling af sandkassemiljøet vil fjerne miljøet helt, og derefter oprettes det igen med standarddemodata.  

8. Hvis du vil skifte mellem produktions- og sandkassemiljøerne, kan du bruge Business Central-appstarter.
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

9. Det er muligt for en administrator eller en anden bruger at begrænse eller endda blokere adgangen for bestemte brugere til sandkassemiljøet. Dette kan gøres ved hjælp af standardsikkerhedsfunktionerne i produktet, f.eks. brugerkort, brugergrupper og rettighedssæt.

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avancerede funktioner i sandkassemiljøet
### <a name="designer"></a>Designer
I et sandkassemiljø er **Designer** aktiveret. Du kan aktivere funktionen ved at vælge designikonet ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side.

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="enable-the-advanced-user-experience"></a>Aktivere den avancerede brugeroplevelse
Du kan aktivere og prøve alle de avancerede funktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] i en sandkasselejer ved at indstille feltet **Oplevelse** på siden **Virksomhedsoplysninger**.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Når du har aktiveret de avancerede funktioner i en sandkasselejer, kan du få adgang til alle standardprofiler og rollecentre. Du kan også oprette en evalueringsvirksomhed, der er fuldt defineret, herunder med demodata og adgang til avancerede områder af produktet.

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
