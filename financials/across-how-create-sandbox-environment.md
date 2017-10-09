---
title: "Oprette et sandkassemiljø | Microsoft Docs"
description: "Oprette et miljø til udforskning, læring, demonstration, udvikling og test."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 08/18/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d7bcb866d5f69e77e5a175d0b73e8ac03cf09d98
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="how-to-create-a-sandbox-environment"></a>Fremgangsmåde: Oprette et sandkassemiljø
Et sandkassemiljø (eksempelvisning) er en ikke-produktiv forekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)]. Isoleret fra produktion er et sandkassemiljø stedet, hvor du sikkert kan udforske, lære, demonstrere, udvikle og teste tjenesten uden risiko for at påvirke data og indstillinger i dit produktionsmiljø.

## <a name="to-create-a-sandbox-environment"></a>Sådan opretter du et sandkassemiljø
Du skal have abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)] for at kunne oprette et sandkassemiljø. Der kan kun være ét sandkassemiljø pr. abonnement.

1. Log ind på din produktionsforekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)]-tjenesten.
2. Vælg den ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sandkassemiljø**, og vælg derefter det relaterede link.
![Konfiguration af sandkassemiljø](./media/across-sandbox/sandbox-environment-setup.png)
3. Vælg **Opret**.  
  Der åbnes en anden fane i din webbrowser, hvor du kan afslutte opsætningen af sandkassemiljøet.
> [!NOTE]  
>  Hvis blokering af pop op-vinduer er aktiveret i din webbrowser, kan du ændre denne indstilling, så URL-adresser fra *.financials.dynamics.com-adressen tillades.   

4. Når sandkassemiljøet er klar, omdirigeres du til miljøet velkomstguide.
![Velkomstguide i sandkassemiljø](./media/across-sandbox/sandbox-wizard.png)

5. Vælg **Lær mere** for at læse om scenarier, som du kan prøve i et sandkassemiljø. Eller du kan vælge **Luk** for at fortsætte til rollecenteret for din [!INCLUDE[d365fin](includes/d365fin_md.md)]-sandkasseforekomst.
6. Der vises en meddelelse om, at dette er et sandkassemiljø, øverst i rollecenteret. Du kan også se miljøtypen i titellinjen i klienten.
![Rollecentermeddelelse i sandkassemiljø](./media/across-sandbox/sandbox-rolecenter-notification.png)  
I sandkassemiljøet er der blevet oprettet en helt ny lejer. Denne lejer er indlæst med standarddemodata for virksomheden CRONUS. Ingen data kopieres eller på anden måde overføres fra produktionsmiljøet under oprettelsen af sandkassen.
7.  Du kan når som helst vende tilbage til siden **Sandkassemiljø** og nulstille sandkassemiljøet.
> [!NOTE]  
>  Nulstilling af sandkassemiljøet vil fjerne miljøet helt, og derefter oprettes det igen med standarddemodata.  

8.  Hvis du vil skifte mellem produktions- og sandkassemiljøerne, kan du bruge Dynamics 365-appstarter.
![Dynamics 365-menu i sandkassemiljø](./media/across-sandbox/sandbox-dynamics365-menu.png)

9.  Det er muligt for en administrator eller en anden bruger at begrænse eller endda blokere adgangen for bestemte brugere til sandkassemiljøet. Dette kan gøres ved hjælp af standardsikkerhedsfunktionerne i produktet, f.eks. brugerkort, brugergrupper og rettighedssæt.

![Rettighedssæt for sandkasser](./media/across-sandbox/sandbox-permission-sets.png)

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avancerede funktioner i sandkassemiljøet
### <a name="the-in-client-designer"></a>Designeren i klienten
I et sandkassemiljø er designerfunktionen i klienten aktiveret. Du kan aktivere den ved at vælge designikonet ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side.

![Designeren i klienten](./media/across-sandbox/sandbox-inclient-designer.png)

### <a name="enable-the-advanced-user-experience"></a>Aktivere den avancerede brugeroplevelse
Du kan aktivere og prøve alle de avancerede funktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] i en sandkasselejer ved at indstille feltet **Oplevelse** på siden **Virksomhedsoplysninger**.

![Avanceret sandkassemiljø](./media/across-sandbox/sandbox-advanced.png)

![Sandkasseproduktion](./media/across-sandbox/sandbox-production.png)

Når du har aktiveret de avancerede funktioner i en sandkasselejer, kan du få adgang til alle standardprofiler og rollecentre. Du kan også oprette en evalueringsvirksomhed, der er fuldt defineret, herunder med demodata og adgang til avancerede områder af produktet.

![Sandkasse, ny virksomhed](./media/across-sandbox/sandbox-newcompany.png)


## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

