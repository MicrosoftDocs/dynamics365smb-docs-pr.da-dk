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
ms.date: 12/10/2019
ms.author: solsen
ms.openlocfilehash: 7d189ab6fa5aff518b643c797b7600570fcad43e
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910632"
---
# <a name="creating-a-sandbox-environment-in-include-prodshortincludesprodshortmd"></a>Opret et sandkassemiljø i [!INCLUDE [prodshort](includes/prodshort.md)]

Med [!INCLUDE [prodshort](includes/prodshort.md)] kan du nemt oprette et sikkert miljø, hvor du kan teste, træne eller foretage fejlfinding uden at forstyrre virksomhedens arbejdsprocesser eller forretningsdata. Et sådant ikke-produktionsmiljø kaldes en *sandkasse*. Isoleret fra produktion er et sandkassemiljø stedet, hvor du sikkert kan udforske, lære, demonstrere, udvikle og teste tjenesten uden risiko for at påvirke data og indstillinger i dit produktionsmiljø.  

Administratoren kan oprette sandkassemiljøer i [Administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), men hvis du hurtigt vil teste noget, kan du oprette et sandkasse-miljø fra [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> Teknisk set er sandkassemiljøer meget forskellige fra produktionsmiljøer, selvom administratoren opretter en sandkasse, som inkluderer produktionsdata. Du kan ikke bruge en sandkasse til benchmarking, og du kan f.eks. ikke anmode om at eksportere databaser. Hvis du vil oprette en sandkasse til benchmarking, kan administratoren oprette et dedikeret produktionsmiljø i Administrationscenter. Du kan finde flere oplysninger i [Miljøtyper](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).

## <a name="to-create-a-sandbox-environment-in-your-include-prodshortincludesprodshortmd"></a>Sådan opretter du et sandkassemiljø i din [!INCLUDE [prodshort](includes/prodshort.md)]

1. Log ind på din produktionsforekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)].

2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sandkassemiljø**, og vælg derefter det relaterede link.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Vælg knappen **Opret**.  

    Der vises endnu en fane i [!INCLUDE[d365fin](includes/d365fin_md.md)], hvor du kan afslutte opsætningen af dit sandkassemiljø.

    > [!NOTE]  
    >  Hvis blokering af pop op-vinduer er aktiveret i din webbrowser, kan du ændre denne indstilling, så URL-adresser fra *.businesscentral.dynamics.com-adressen tillades.

Når sandkassemiljøet er klar, omdirigeres du til miljøet velkomstguide.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Du kan vælge knappen **Få mere at vide** for at læse om udviklerscenarier, som du kan afprøve i et sandkassemiljø, eller vælg knappen **Luk** for at fortsætte til rollecenteret i din sandkasseforekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)].

Der vises en meddelelse om, at dette er et sandkassemiljø, øverst i rollecenteret. Du kan også se miljøtypen i titellinjen i klienten.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Et sandkassemiljø, der oprettes på denne måde, indeholder kun standarddemonstrationsdataene for CRONUS-virksomheden. Der kopieres ikke eller på anden måde overføres data fra produktionsmiljøet.<br /><br />
> Du kan også oprette et sandkassemiljø, der indeholder produktionsdataene. Dette skal gøres via Administrationscenter. Du kan finde flere oplysninger under [Administrere miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) i hjælpen til udviklere og it-eksperter.

Du kan når som helst vende tilbage til siden **Sandkassemiljø** og nulstille sandkassemiljøet.

> [!NOTE]  
> Nulstilling af sandkassemiljøet vil fjerne miljøet helt, og derefter oprettes det igen med standarddemodata.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

En administrator kan begrænse eller endda blokere adgangen for bestemte brugere til sandkassemiljøet. Dette kan gøres ved hjælp af standardsikkerhedsfunktionerne i produktet, f.eks. brugerkort, brugergrupper og rettighedssæt. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avancerede funktioner i sandkassemiljøet

Sandkassemiljøet er ikke mindst anvendelig, fordi det indeholder et par praktiske funktioner.

### <a name="designer"></a>Designer

I et sandkassemiljø er **Designer** aktiveret. Du kan aktivere Designer ved at vælge designikon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side eller ved at vælge menupunktet **Design** i menuen ![Indstillinger](media/ui-experience/settings_icon_small.png).

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a>Sådan aktiveres den avancerede brugeroplevelse
Du kan aktivere og prøve den fulde funktionalitet af standardversionen i [!INCLUDE[d365fin](includes/d365fin_md.md)] i en sandkasselejer ved at indstille feltet **Oplevelse** på siden **Virksomhedsoplysninger**.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Når du har aktiveret *Premium*-brugeroplevelsen, får du adgang til alle standardprofilerne (rollerne) og rollecentre i standardversionen. Du kan også oprette en evalueringsvirksomhed, der er fuldt defineret, herunder med demodata og adgang til avancerede områder af produktet. Alternativt kan du kontakte en videresalgspartner for at demonstrere mulighederne. Du kan finde flere oplysninger i [Hvordan finder jeg en videresalgspartner?](across-faq.md#findpartner).  

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a>Se også

[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Prøveversioner og abonnementer](across-preview.md)  
[Sådan styrer du Miljøer i Business Central Administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
