---
title: Administration af Microsoft Teams-integration med Business Central| Microsoft Docs
description: Administration af Microsoft Teams-integration med Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: 7fef0f2ffe23155e840fa89a62b1822fee1efd35
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589078"
---
# <a name="managing-microsoft-teams-integration-with-prod_short"></a>Styring af Microsoft Teams-integration med [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Denne artikel giver en oversigt over, hvad du kan gøre som administrator for at kontrollere Microsoft Teams-integration med [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="in-microsoft-teams"></a>I Microsoft Teams

### <a name="minimum-requirements"></a>Minimumkrav

I dette afsnit beskrives minimumkrav til [!INCLUDE [prod_short](includes/prod_short.md)]-appfunktioner for at arbejde i Teams.

- Krævede licenser

    Denne tabel giver dig et overblik over de licenser, der er nødvendige for at [!INCLUDE [prod_short](includes/prod_short.md)]-appfunktionerne kan bruges i Teams.

    |Hvad|Teams-licens|[!INCLUDE [prod_short](includes/prod_short.md)]-licens|
    |----|---|---|
    |Søg efter kontakter i [!INCLUDE [prod_short](includes/prod_short.md)].|![markering.](media/check.png "check")|![markering](media/check.png "check")|
    |Indsæt et link til en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en samtale, og send den som et kort.|![markering](media/check.png "check")|![markering](media/check.png "check")|
    |Dele et hyperlink fra en side i [!INCLUDE [prod_short](includes/prod_short.md)] til en Teams-samtale.|![markering](media/check.png "check")|![markering](media/check.png "check")|
    |Se et kort over en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en samtale.|![markering](media/check.png "check")||
    |Se flere oplysninger om et kort for en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en samtale.|![markering](media/check.png "check")|![markering](media/check.png "check")|
    |Åbn et sidelink i [!INCLUDE [prod_short](includes/prod_short.md)] fra en samtale.|![markering](media/check.png "check")|![markering](media/check.png "check")|

- Tillad URL-prøveversion

    **Indstillingen Tillad URL-prøveversion** skal være aktiveret. I modsat fald kan der ikke oprettes et kort til [!INCLUDE [prod_short](includes/prod_short.md)]-links, der er indsat i en samtale med Teams. Du kan finde flere oplysninger om denne indstilling under [Administrér meddelelsespolitikker i Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-prod_short-app-optional"></a>Administrerer [!INCLUDE [prod_short](includes/prod_short.md)]-appen (valgfri)

Som Teams-administrator kan du administrere alle apps for din organisation, herunder [!INCLUDE [prod_short](includes/prod_short.md)]-appen. Du kan godkende eller installere [!INCLUDE [prod_short](includes/prod_short.md)]-appen for din organisation, blokere bruger fra installation af appen og meget mere.

Du kan finde flere oplysninger i følgende artikler i Microsoft Teams-dokumentationen:

- [Administrere dine apps i Microsoft Teams Administration](/MicrosoftTeams/manage-apps)
- [Administrere politikker for app-opsætning i Microsoft Teams](/microsoftteams/teams-app-setup-policies)

## <a name="in-prod_short"></a>I [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements"></a>Minimumkrav

- [!INCLUDE [prod_short](includes/prod_short.md)] version:

    [!INCLUDE [prod_short](includes/prod_short.md)] 2021 udgivelsesbølge 1 eller nyere. Teams-integration understøttes kun [!INCLUDE [prod_short](includes/prod_short.md)] online, men ikke lokalt.

- Kode enhed **2718 Page Summary Provider** udgives som en webtjeneste:

    Denne codeunit er som standard udgivet som en webtjeneste. Codeunit er en del af [!INCLUDE [prod_short](includes/prod_short.md)]-systemprogrammet. Den bruges til at hente feltdataene til en [!INCLUDE [prod_short](includes/prod_short.md)]-side, der er føjet til en Teams-samtale. Du kan finde flere oplysninger om udgivelse af webtjenester under [Udgive en webtjeneste](across-how-publish-web-service.md).

- <a name="permissions"></a>Brugerrettigheder:

    De kontaktsøgninger, sider og data, som brugere kan få vist og redigere i en Teams-samtale, kontrolleres oftest af deres tilladelser i [!INCLUDE [prod_short](includes/prod_short.md)].

    - Hvis du vil søge efter kontakter, skal brugere som minimum have læsetilladelse til tabellen **Kontakter**. 
    - Hvis du vil indsætte et [!INCLUDE [prod_short](includes/prod_short.md)]-hyperlink i en Teams-samtale og få den på et kort, skal brugerne som minimum have læsetilladelse til siden og dens data.
    - Når et kort er sendt til en samtale, kan alle brugere i denne samtale se dette kort uden tilladelse til [!INCLUDE [prod_short](includes/prod_short.md)].
    - Hvis du vil have vist flere detaljer om et kort eller åbne posten i [!INCLUDE [prod_short](includes/prod_short.md)], skal brugere have læsetilladelse til siden og dens data.
    - Hvis du vil ændre data, skal brugerens behov redigeres.
    
    Du kan finde flere oplysninger om rettigheder i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).

## <a name="installing-the-business-central-app-by-using-centralized-deployment"></a>Installere Business central-appen ved hjælp af centraliseret installation

I Microsoft Teams Administration kan du konfigurere Teams App-installation for organisationen. I administrationscenter for Teams kan du bruge funktionen centraliseret installation til automatisk at installere Business Central-app i Teams for alle brugere i din organisation, bestemte grupper eller enkelte brugere.

> [!NOTE]
> Hvis du vil konfigurere centraliseret installation, skal Teams have rollen **Teams service administrator** eller **Global administrator**.

1. I Business Central kan du vælge den ![Forstørrelsesglas, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikonet, skal du skrive **Teams App Centraliseret installation** og derefter vælge det relaterede link. Du kan desuden vælge [her](https://businesscentral.dynamics.com/?page=1833) for at åbne siden direkte.
2. Læs oplysningerne om **Konfigurere Business central-appen til Teams**, og vælg derefter **Næste**.
3. Åbn [Teams Administration](https://go.microsoft.com/fwlink/?linkid=2163970), og gennemfør følgende trin.
    1. Gå til **Teams-apps** > **Opsætningspolitikker**.
    2. Opret en ny politik, eller Vælg den politik, du vil bruge til at installere Business central-app'en, og vælg derefter **Tilføj apps**.
    3. Søg efter og vælg **Business central** på siden **Tilføj installerede apps**.
    4. Vælg **Tilføj**.

       Business central skal nu vises under **installerede apps** til politikken.
    5. Konfigurer eventuelle yderligere indstillinger, og vælg **Gem**.

    Du kan finde flere oplysninger om opsætnings politikker i grupper i [Administrer politikker for app-opsætning i Microsoft Teams](/MicrosoftTeams/teams-app-setup-policies) i dokumentationen til Teams.
4. Gå tilbage til **Teams appen centraliseret installation** i Business central, og vælg **udført**.

> [!IMPORTANT]
> Det kan være op til 24 timer, før appen Konfigurer politikken skal anvendes, og appen installeres på brugerne.

## <a name="managing-privacy-and-compliance"></a>Administrere beskyttelse af personlige oplysninger og overholdelse 

Microsoft Teams indeholder omfattende styring af overholdelse og håndtering af følsomme eller personlige data&mdash;herunder data, som er føjet til chats og kanaler fra [!INCLUDE [prod_short](includes/prod_short.md)]-appen.

### <a name="understanding-where-prod_short-cards-are-stored"></a>Om, hvor [!INCLUDE [prod_short](includes/prod_short.md)]-kort gemmes

Når et kort er sendt til en chat, kopieres kortet og de felter, der vises på kortet, til team. Disse oplysninger er underlagt team politikkerne for organisationen, f.eks. politikker for opbevaring af data. Når der vises kort detaljer, er ingen af dataene i vinduet detaljer gemt i grupper. Dataene gemmes stadig i [!INCLUDE [prod_short](includes/prod_short.md)] og bliver kun hentet af Teams, når brugeren vælger at få vist detaljerne. 

- Du kan finde flere oplysninger om, hvor grupper lagrer disse data, i [Placering af data i Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Du kan få mere at vide om opbevaringspolitikker i grupper under [Opbevaringspolitikker i Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Begrænse deling af kort 

Du kan forhindre, at bestemte brugere eller grupper sender kort til chatrum eller kanaler ved at oprette meddelelses politikker, der deaktiverer indstilling af **URL-eksempler**. Du kan finde flere oplysninger om denne indstilling under [Administrér meddelelsespolitikker i Teams](/microsoftteams/messaging-policies-in-teams). 

Du kan også bruge informations hinder til at forhindre, at personer eller grupper kommunikerer med hinanden. Du kan finde flere oplysninger i [Informationsbarrierer i Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Funktionerne til forebyggelse af datatab i Microsoft 365 Security & Compliance Center kan ikke anvendes specifikt på kort. Men de kan anvendes på de chatmeddelelser, der indeholder kortene. <!-- To track upcoming advanced features that include enabling DLP for cards, see [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).-->

### <a name="responding-to-data-requests"></a>Reagere på anmodninger om data

Du kan give teammedlemmer og team ejere mulighed for at slette meddelelser, der indeholder følsomme kort, ved at oprette meddelelses politikker, f. eks **Ejere kan slette sendte meddelelser** og **Brugere kan slette sendte meddelelser**. Du kan finde flere oplysninger om denne indstilling under [Administrér meddelelsespolitikker i Teams](/microsoftteams/messaging-policies-in-teams).

Indholdssøgning og overholdelsesfunktioner i eDiscovery i Microsoft 365 Security & Compliance Center kan også anvendes til kort.

Da kortdata i grupper er en kopi af data i [!INCLUDE [prod_short](includes/prod_short.md)], kan du også bruge [!INCLUDE [prod_short](includes/prod_short.md)]-funktioner til at eksportere en kundes data, hvis der er anmodet om det. Du kan finde flere oplysninger om beskyttelse af personlige oplysninger i [!INCLUDE [prod_short](includes/prod_short.md)] under [Ofte stillede spørgsmål om beskyttelse Business Central-kunder](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="see-also"></a>Se også
[[!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams Oversigt over integration](across-teams-overview.md)  
[Installér appen [!INCLUDE [prod_short](includes/prod_short.md)] til Microsoft Teams](across-install-app-for-teams.md)  
[Teams, ofte stillede spørgsmål](teams-faq.md)  
[Fejlfinding i Teams](admin-teams-troubleshooting.md)  
[Udvikling af Teams-integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]