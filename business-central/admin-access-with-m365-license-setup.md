---
title: Konfigurere adgang til Microsoft 365-licenser
description: 'En vejledning til, hvordan administratorer kan konfigurere adgang til Business Central med Microsoft 365-licenser.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 09/28/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.search.form: '9061,'
---
# Konfigurere Business Central-adgang i Teams med Microsoft 365-licenser

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Administratorer skal udføre flere aktiviteter, før brugere kan få adgang til [!INCLUDE [prod_short](includes/prod_short.md)] med deres Microsoft 365-licens. Nedenstående trin repræsenterer den opsætning, der som minimum kræves for at komme i gang. Hvis du vil vide mere om adgang med Microsoft 365-licenser, skal du gå til [Business Central-adgang med Microsoft 365-licenser](admin-access-with-m365-license.md).

## Retningslinjer

Opsætning af adgang til Microsoft 365-licenser omfatter følgende opgaver:

|Trin|Opgave|Påkrævet|
|-|-|-|
|1|[Konfigurere de Business Central-data, som Microsoft 365-licensbrugere har tilladelse til at få vist](#configure-permissions)|![markering](media/check.png "check")|
|2|[Aktivér adgang med Microsoft 365-licenser til Business Central-miljø](#enable-access-with-microsoft-365-licenses)|![markering](media/check.png "check")|
|3|[Tildele sikkerhedsgruppe til miljøet](#choose-who-gets-access-by-using-security-group)|
|4|[Udrulle Business Central-appen til Teams til brugere](#deploy-the-business-central-app-for-teams)|![markering](media/check.png "check")|
|5|[Teste konfigurationen](#test-your-setup)||

> [!TIP]
> Bortset fra den sidste opgave, kan du udføre opgaverne i vilkårlig rækkefølge. Du kan udføre opgaver separat, som beskrevet i de følgende afsnit, der følger efter eller bruger assisteret opsætningsvejledning **Adgang med Microsoft 365-licenser**, som vejledning.
>
> Hvis du vil køre den assisterede opsætningsvejledning, skal du gøre følgende:
>
> 1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Assisteret opsætning** og vælg derefter det relaterede link.
> 2. Gå til afsnittet **Gør mere med Business Central**, og vælg **Adgang med Microsoft 365-licenser** på siden **Assisteret opsætning**.
> 3. Følg anvisningerne.  

## Konfigurer tilladelser

[!INCLUDE [prod_short](includes/prod_short.md)] har et sikkert design og minimerer risikoen ved at give adgang til Microsoft 365-brugere som standard. Administratorer skal konfigurere objekttilladelser, der bestemmer, hvilke tabeller, sider og rapporter der er adgang til i Teams, der kun har en Microsoft 365-licens. Disse tilladelser er de starttilladelser, der tildeles, når en bruger logger på første gang med Microsoft 365-licensen. 

Konfigurere starttilladelser:

1. I [!INCLUDE [prod_short](includes/prod_short.md)] skal du søge efter **Licenskonfiguration**.
2. Vælg Microsoft 365-licensen.
3. Klik på redigeringsikonet ![Rediger ikon](media/edit-pencil.png), øverst på siden **Microsoft 365**-licens, og aktiver **Tilpas tilladelser**. 
4. Tilføj de relevante tilladelsessæt i sektionen **brugerdefineret tilladelsessæt**, og vælg, om de gælder for en enkelt virksomhed eller alle virksomheder i miljøet.

Med denne konfiguration bliver brugere, der kun har en Microsoft 365-licens, føjet til listen **Brugere**, når de åbner [!INCLUDE [prod_short](includes/prod_short.md)] første gang. Du kan finde flere oplysninger om brugere i [Oprette brugere i henhold til licenser](ui-how-users-permissions.md).

> [!NOTE]
> Når listen med brugere i [!INCLUDE [prod_short](includes/prod_short.md)] synkroniseres med brugere i Microsoft 365, tilføjes kun brugere, der har en [!INCLUDE [prod_short](includes/prod_short.md)]-licens, til [!INCLUDE [prod_short](includes/prod_short.md)]-brugerliste. Hvis du vil have mere administrativ kontrol over tilladelser og profiler, kan du tildele en sikkerhedsgruppe til miljøet. Når miljøer er sikret ved hjælp af en sikkerhedsgruppe og giver adgang med Microsoft 365-licenser, omfatter funktionen **Opdater brugere fra Microsoft 365** en handling på siden **Brugere** også brugere, der kun har en Microsoft 365-licens. Du kan få mere at vide om sikring af miljøer i afsnittet [Administrere adgang med Microsoft Entra-grupper](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) i hjælp til udviklere og it-fagfolk.

> [!TIP]
> Er du på udkig efter en hurtigere måde at komme i gang på, når du prøver denne funktion i en sandkasse eller evalueringsvirksomhed? Tildel det **D365 læse**-tilladelsessæt, som giver tilladelse til de fleste objekter.  

Når du arbejder med flere miljøer, skal der tilknyttet licenskonfiguration til hvert miljø, og det kan være forskelligt fra miljø til miljø.

Du kan finde flere oplysninger om rettigheder i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md) og [Sammensætte tilladelsessæt](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## Aktivere adgang med Microsoft 365-licenser

Adgang med Microsoft 365-licenser er som standard deaktiveret. Adgang skal være aktiveret uafhængigt for hvert miljø, hvilket giver administratorerne mulighed for at styre den midlertidigt inddelte fase i organisationen. Du kan aktivere adgang ved hjælp af [!INCLUDE [prod_short](includes/prod_short.md)] Administration: 

1. I øverste højre hjørne vælges **Indstillinger** ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") > **Administration**.  
2. Vælg  **Miljøer** i Administration, og vælg derefter det miljø, hvor du vil ændre licensadgangen. 
3. På siden med **Miljøoplysninger** skal du vælge **Rediger** for at få indstillingen **Adgang med Microsoft 365-licenser**.
4. Aktiver i ruden **Microsoft 365-licenser**. 
5. Vælg **Gem**, når du er færdig, og accepter bekræftelsen. Ændringen træder i kraft med det samme.

## Vælge, hvem der får adgang ved hjælp af sikkerhedsgruppen

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

I Business Center administration kan et miljø tildeles til en eller flere sikkerhedsgrupper for at kontrollere adgangen. Du kan tildele en Microsoft Entra-gruppe til miljøet. Ved at tildele en Microsoft Entra-gruppe til et miljø giver gruppen kun direkte og indirekte medlemmer af gruppen adgang til miljøet. Indirekte medlemmer er brugere i en anden gruppe, som selv er medlem af den gruppe, der er tildelt miljøet. Selvom alle brugere med licens i Microsoft Entra ID bliver føjet til miljøet, når det synkroniseres med Microsoft 365, kan kun gruppemedlemmer logge på. Du kan få mere at vide i afsnittet [Administrere adgang med Microsoft Entra-grupper](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) i hjælp til udviklere og it-fagfolk.

## Implementer Business Central-appen til Teams

Hvis du vil have, at [!INCLUDE [prod_short](includes/prod_short.md)]-licensindehavere skal dele data i Teams, og hvis Microsoft 365-licensindehavere skal have adgang til disse data, skal hver enkelt have installeret [!INCLUDE [prod_short](includes/prod_short.md)]-app til teams. Selvom brugerne kan installere appen alene, anbefales det, at administratorer bruger centraliseret udrulning. Centraliseret installation giver dig mulighed for at samle en app til et bredere publikum i hele organisationen og minimere den enkelte bruger indsats. 

Du kan få mere at vide om, hvordan du installerer [!INCLUDE [prod_short](includes/prod_short.md)]-appen til Teams i [Installation af Business central-appen ved hjælp af centraliseret installation](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Hvis du har kørt centraliseret installation, før og kun implementerer appen på en sikkerhedsgruppe af licenserede [!INCLUDE [prod_short](includes/prod_short.md)]-brugere, skal du køre den igen for at implementere den i flere grupper eller hele organisationen, afhængigt af hvordan du konfigurerer adgangen.

> [!TIP]
> Er du på udkig efter en hurtigere måde at komme i gang på, når du prøver denne funktion? Test brugere kan installere appen på [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## Test konfigurationen

Du kan kontrollere, at opsætningen er klar til produktion, ved at benytte følgende fremgangsmåde for at opbygge tilliden for, at alt fungerer, som det skal.

1. Opret eller identificer to testbrugere (A og B).

   - Testbruger A skal have en [!INCLUDE [prod_short](includes/prod_short.md)]-licens og Microsoft 365-licens, der giver adgang til Teams.
   - Testbruger B må kun have en Microsoft 365-licens til at få adgang til Teams.

2. Log på med [!INCLUDE [prod_short](includes/prod_short.md)]-webklienten som testbruger A.

   1. Åbn en post, som testbruger B skal have adgang til, f. eks. et **varekort** i den relevante virksomhed og miljø.
   2. Vælg **Del** ![!Del med andre apps-handlinger på sider.](media/share-icon.png) > **Del med Teams** for at åbne vinduet Del med Teams.
   3. Tilføj i feltet **Del med** testbruger B som modtager.
   4. Vent på, at linket udvides til et kort, og vælg del.

3. Log på Microsoft Teams som testbruger B.

   1. Vælg chat, og åbn samtalen med testbruger A.
   2. I den meddelelse, der er sendt af testbruger A, skal du vælge Detaljer-knappen på kortet. Hvis [!INCLUDE [prod_short](includes/prod_short.md)]-klienten vises og er skrivebeskyttet, er opsætningen lykkedes.

> [!TIP]
> Gik noget galt? Se [Fejlfinde adgang med Microsoft 365-licenser](admin-access-with-m365-license-troubleshooting.md).

## Se også

[Oversigt over Business Central-adgang med Microsoft 365-licenser](admin-access-with-m365-license.md#minimum-requirements)  
[Fejlfinde adgang med Microsoft 365-licenser](admin-access-with-m365-license-troubleshooting.md)  
[Business Central og Microsoft Teams-integration](across-teams-overview.md)  
