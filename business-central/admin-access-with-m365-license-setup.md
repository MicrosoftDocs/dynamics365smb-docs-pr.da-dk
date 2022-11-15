---
title: Konfigurere adgang til Microsoft 365-licenser
description: En vejledning til, hvordan administratorer kan konfigurere adgang til Business Central med Microsoft 365-licenser.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.openlocfilehash: f509c0a8bf5e9320eb0f2712863984221b7138b9
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2022
ms.locfileid: "9744975"
---
# <a name="set-up-access-with-microsoft-365-licenses"></a>Konfigurere adgang til Microsoft 365-licenser 

Administratorer skal udføre flere aktiviteter, før brugere kan få adgang til Business central med deres Microsoft 365-licens. Nedenstående trin repræsenterer den opsætning, der som minimum kræves for at komme i gang.  

## <a name="deploy-the-business-central-app-for-teams"></a>Udrulle Business Central-appen til Teams 

Hvis du vil have, at Business Central-indehavere skal dele data i Teams, og hvis Microsoft 365-licensindehavere skal have adgang til disse data, skal hver enkelt have installeret Business central-app til teams. Selvom brugerne kan installere appen alene, anbefales det, at administratorer bruger centraliseret udrulning. Centraliseret installation giver dig mulighed for at samle en app til et bredere publikum i hele organisationen og minimere den enkelte bruger indsats. 

Du kan få mere at vide om, hvordan du installerer Business central-appen til Teams i [Installation af Business central-appen ved hjælp af centraliseret installation](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Hvis du har kørt centraliseret installation, før og kun implementerer appen på en sikkerhedsgruppe af licenserede Business Central-brugere, skal du køre den igen for at implementere den i flere grupper eller hele organisationen, afhængigt af hvordan du konfigurerer adgangen.

> [!TIP]
> Er du på udkig efter en hurtigere måde at komme i gang på, når du prøver denne funktion? Testbrugere kan installere appen på [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## <a name="configure-permissions"></a>Konfigurere tilladelser

Business Central har et sikkert design og minimerer risikoen ved at give adgang til Microsoft 365-brugere som standard. Administratorer skal konfigurere objekttilladelser, der bestemmer, hvilke tabeller, sider og rapporter der er adgang til i Teams, der kun har en Microsoft 365-licens. Disse tilladelser er de starttilladelser, der tildeles, når en bruger logger på første gang med Microsoft 365-licensen. 

Konfigurere starttilladelser:

1. I Business central skal du søge efter **licenskonfiguration**.
2. Vælg Microsoft 365-licensen.
3. Klik på redigeringsikonet ![Rediger ikon](media/edit-pencil.png), øverst på siden **Microsoft 365**-licens, og aktiver **Tilpas tilladelser**. 
4. Tilføj de relevante tilladelsessæt i sektionen **brugerdefineret tilladelsessæt**, og vælg, om de gælder for en enkelt virksomhed eller alle virksomheder i miljøet.

> [!NOTE]
> Når listen med brugere i Business central synkroniseres med brugere i Microsoft 365, tilføjes kun brugere, der har en Business Central-licens, til Business Central-brugerliste. Brugere, der kun har en Microsoft 365-licens, føjes til listen med brugere, når de åbner Business central første gang. Flere oplysninger i [Oprette brugere ifølge licenser](ui-how-users-permissions.md).

> [!TIP]
> Er du på udkig efter en hurtigere måde at komme i gang på, når du prøver denne funktionssandkasse eller evalueringsvirksomhed? Tildel det **D365 læse**-tilladelsessæt, som giver tilladelse til de fleste objekter.  

Når du arbejder med flere miljøer, skal der tilknyttet licenskonfiguration til hvert miljø, og det kan være forskelligt fra miljø til miljø. 

Du kan finde flere oplysninger om rettigheder i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md) og [Sammensætte tilladelsessæt](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## <a name="turn-on-access-with-microsoft-365-licenses"></a>Aktivere adgang med Microsoft 365-licenser

Adgang med Microsoft 365-licenser er som standard deaktiveret. Adgang skal være aktiveret uafhængigt for hvert miljø, hvilket giver administratorerne mulighed for at styre den midlertidigt inddelte fase i organisationen. Du kan aktivere adgang ved hjælp af Business Central administration: 

1. I øverste højre hjørne vælges **Indstillinger** ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") > **Administration**.  
2. Vælg  **Miljøer** i Administration, og vælg derefter det miljø, hvor du vil ændre licensadgangen. 
3. På siden med **Miljøoplysninger** skal du vælge **Rediger** for at få indstillingen **Adgang med Microsoft 365-licenser**.
4. Aktiver i ruden **Microsoft 365-licenser**. 
5. Vælg **Gem**, når du er færdig, og accepter bekræftelsen. Ændringen træder i kraft med det samme.

## <a name="test-your-setup"></a>Test konfigurationen

Du kan kontrollere, at opsætningen er klar til produktion, ved at benytte følgende fremgangsmåde for at opbygge tilliden for, at alt fungerer, som det skal. 

1. Opret eller identificer to testbrugere (A og B).

   - Testbruger A skal have en Business Central-licens og Microsoft 365-licens, der giver adgang til Teams.
   - Testbruger B må kun have en Microsoft 365-licens til at få adgang til Teams.

2. Log på med Business central-webklienten som testbruger A.

   1. Åbn en post, som testbruger B skal have adgang til, f. eks. et **varekort** i den relevante virksomhed og miljø.
   2. Vælg **Del** ![!Del med andre apps-handlinger på sider.](media/share-icon.png) > **Del med Teams** for at åbne vinduet Del med Teams.
   3. Tilføj i feltet **Del med** testbruger B som modtager. 
   4. Vent på, at linket udvides til et kort, og vælg del. 

3. Log på Microsoft Teams som testbruger B.

   1. Vælg chat, og åbn samtalen med testbruger A. 
   2. I den meddelelse, der er sendt af testbruger A, skal du vælge Detaljer-knappen på kortet. Hvis Business Central-klienten vises og er skrivebeskyttet, er opsætningen lykkedes. 

> [!TIP]
> Gik noget galt? Se [Fejlfinde adgang med Microsoft 365-licenser](admin-access-with-m365-license-troubleshooting.md).

## <a name="see-also"></a>Se også

[Business Central-adgang med Microsoft 365-licenser](admin-access-with-m365-license.md#minimum-requirements)  
[Fejlfinde adgang med Microsoft 365-licenser](admin-access-with-m365-license-troubleshooting.md)  
[Business Central og Microsoft Teams-integration](across-teams-overview.md)  