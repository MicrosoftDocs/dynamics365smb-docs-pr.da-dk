---
title: Opret et sandkassemiljø
description: Oprette et miljø til udforskning, læring, demonstration, udvikling og test fra Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: a76ae33815b8e9368f45b72fd8703bfc47cbd079
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215624"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a>Opret et sandkassemiljø i [!INCLUDE[prod_short](includes/prod_short.md)]

Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du nemt oprette et sikkert miljø, hvor du kan teste, træne eller foretage fejlfinding uden at forstyrre virksomhedens arbejdsprocesser eller forretningsdata. Et sådant ikke-produktionsmiljø kaldes en *sandkasse*. Isoleret fra produktion er et sandkassemiljø stedet, hvor du sikkert kan udforske, lære, demonstrere, udvikle og teste tjenesten uden risiko for at påvirke data og indstillinger i dit produktionsmiljø.  

Administratoren kan administrere sandkassemiljøer i [Administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), men hvis du hurtigt vil teste noget, kan du oprette et sandkasse-miljø fra [!INCLUDE[prod_short](includes/prod_short.md)]. Når du er færdig, kan du fjerne sandkassen via Administrationscenter.  

> [!NOTE]
> Teknisk set er sandkassemiljøer meget forskellige fra produktionsmiljøer, selvom administratoren opretter en sandkasse, som inkluderer produktionsdata. Du kan ikke bruge en sandkasse til benchmarking, og du kan f.eks. ikke anmode om at eksportere databaser. Hvis du vil oprette en sandkasse til benchmarking, kan administratoren oprette et dedikeret miljø i Administrationscenter. Du kan finde flere oplysninger i afsnittet [produktion og sandkassemiljøer](/dynamics365/business-central/dev-itpro/administration/environment-types).

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a>Sådan opretter du et sandkassemiljø i din [!INCLUDE[prod_short](includes/prod_short.md)]

1. Log ind på din produktionsforekomst af [!INCLUDE[prod_short](includes/prod_short.md)].

2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sandkassemiljø**, og vælg derefter det relaterede link.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Vælg knappen **Opret**.  

    Der vises endnu en fane i [!INCLUDE[prod_short](includes/prod_short.md)], hvor du kan afslutte opsætningen af dit sandkassemiljø.

    > [!NOTE]  
    >  Hvis blokering af pop op-vinduer er aktiveret i din webbrowser, kan du ændre denne indstilling, så URL-adresser fra *.businesscentral.dynamics.com-adressen tillades.

Når sandkassemiljøet er klar, omdirigeres du til miljøet velkomstguide.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Du kan vælge knappen **Få mere at vide** for at læse om udviklerscenarier, som du kan afprøve i et sandkassemiljø, eller vælg knappen **Luk** for at fortsætte til rollecenteret i din sandkasseforekomst af [!INCLUDE[prod_short](includes/prod_short.md)].

Der vises en meddelelse om, at dette er et sandkassemiljø, øverst i rollecenteret. Du kan også se miljøtypen i titellinjen i klienten.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Et sandkassemiljø, der oprettes på denne måde, indeholder kun standarddemonstrationsdataene for CRONUS-virksomheden. Der kopieres ikke eller på anden måde overføres data fra produktionsmiljøet.
>
> Du kan også oprette et Sandbox-miljø baseret på produktionsdata. Dette skal gøres via Administrationscenter. Du kan finde flere oplysninger i [Administrere miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) i hjælpen til udviklere og administratorer.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

En administrator kan begrænse eller endda blokere adgangen for bestemte brugere til sandkassemiljøet. Dette kan gøres ved hjælp af standardsikkerhedsfunktionerne i produktet, f.eks. brugerkort, brugergrupper og rettighedssæt. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avancerede funktioner i sandkassemiljøet

Sandkassemiljøet er ikke mindst anvendelig, fordi det indeholder et par praktiske funktioner:

* [Udvidet brugeroplevelse](#advanced-user-experience)  
* [Komplette eksempeldata](#complete-sample-data)  
* [Designer](#designer)  

### <a name="advanced-user-experience"></a>Udvidet brugeroplevelse

Du kan aktivere og prøve den fulde funktionalitet af standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] i en sandkasselejer ved at indstille feltet **Oplevelse** på siden **Virksomhedsoplysninger** til *Premium*. Find siden **Virksomhedsoplysninger** i menuen :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Indstillinger":::.  

Når du har aktiveret *Premium*-brugeroplevelsen, får du adgang til alle standardprofilerne (rollerne) og rollecentre i standardversionen. Du kan også oprette en evalueringsvirksomhed, der er fuldt defineret, herunder med demodata og adgang til avancerede områder af produktet. Alternativt kan du kontakte en videresalgspartner for at demonstrere mulighederne. Du kan finde flere oplysninger i [Hvordan finder jeg en videresalgspartner?](/dynamics365/business-central/across-faq.yml#findpartner).  

### <a name="complete-sample-data"></a>Komplette eksempeldata

I de situationer, hvor du har brug for yderligere eksempeldata, skal du kontakte din forhandlerpartner.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>Sådan opretter du en virksomhed med komplette eksempeldata i en sandkasse

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomheder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og vælg derefter **Opret ny virksomhed**.  
3. Vælg **Næste** på siden **Assisteret opsætning af en virksomhed**.  
4. Angiv et navn til den nye virksomhed, og vælg **Avanceret evaluering - komplette eksempeldata** i feltet **Vælg data og konfiguration for at komme i gang**.  
5. Udfør trinnene i resten af guiden til assisteret opsætning.  

Når den assisterede opsætningsguide afsluttes, kan du begynde at udforske den nye virksomhed med de komplette eksempeldata. Du kan finde flere oplysninger om oprettelse af pluk under [Oprettelse af nye virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  

### <a name="designer"></a>Designer

I et sandkassemiljø er **Designer** aktiveret. Du kan aktivere Designer ved at vælge designikon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side eller ved at vælge menupunktet **Design** i menuen ![Indstillinger](media/ui-experience/settings_icon_small.png).  

Du kan finde flere oplysninger i [bruge designer ](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer)i Developer and admin Content (kun på engelsk).  

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Se også

[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)] Prøveversioner og abonnementer](across-preview.md)  
[Sådan styrer du Miljøer i Business Central Administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
