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
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 5fc5957695145ad3bbc4225c7c7e18dd7ca0c728
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386295"
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
    |Indsæt et link til en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en samtale, og send den som et kort.|![markering](media/check.png "check")|![markering](media/check.png "check")|
    |Se et kort over en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en samtale.|![markering](media/check.png "check")||
    |Se flere oplysninger om et kort for en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en samtale.|![markering](media/check.png "check")|![markering](media/check.png "check")|

- Tillad URL-prøveversion

    **Indstillingen Tillad URL-prøveversion** skal være aktiveret. I modsat fald kan der ikke oprettes et kort til [!INCLUDE [prod_short](includes/prod_short.md)]-links, der er indsat i en samtale med Teams. Du kan finde flere oplysninger om denne indstilling under [Administrér meddelelsespolitikker i Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-prod_short-app-optional"></a>Administrerer [!INCLUDE [prod_short](includes/prod_short.md)]-appen (valgfri)

Som Teams-administrator kan du administrere alle apps for din organisation, herunder [!INCLUDE [prod_short](includes/prod_short.md)]-appen. Du kan godkende eller installere [!INCLUDE [prod_short](includes/prod_short.md)]-appen for din organisation, blokere bruger fra installation af appen og meget mere.

Du kan finde flere oplysninger i følgende artikler i Microsoft Teams-dokumentationen:

- [Administrer dine apps i Microsoft Teams Administration](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Administrer politikker for app-opsætning i Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prod_short"></a>I [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements"></a>Minimumkrav

- [!INCLUDE [prod_short](includes/prod_short.md)] version:

    [!INCLUDE [prod_short](includes/prod_short.md)] 2020 release Wave 2, opdatering 17.3 eller nyere. Teams-integration understøttes kun [!INCLUDE [prod_short](includes/prod_short.md)] online, men ikke lokalt.

- Kode enhed **2718 Page Summary Provider** udgives som en webtjeneste:

    Denne codeunit er som standard udgivet som en webtjeneste. Codeunit er en del af [!INCLUDE [prod_short](includes/prod_short.md)]-systemprogrammet. Den bruges til at hente feltdataene til en [!INCLUDE [prod_short](includes/prod_short.md)]-side, der er føjet til en Teams-samtale. Du kan finde flere oplysninger om udgivelse af webtjenester under [Udgive en webtjeneste](across-how-publish-web-service.md).

- <a name="permissions"></a>Brugerrettigheder:

    De sider og data, som brugerne kan få vist og redigere i en Teams-samtale, kontrolleres oftest af deres tilladelser i [!INCLUDE [prod_short](includes/prod_short.md)].
    
    - Hvis du vil indsætte et [!INCLUDE [prod_short](includes/prod_short.md)]-hyperlink i en Teams-samtale og få den på et kort, skal brugerne som minimum have læsetilladelse til siden og dens data.
    - Når et kort er sendt til en samtale, kan alle brugere i denne samtale se dette kort uden tilladelse til [!INCLUDE [prod_short](includes/prod_short.md)].
    - Hvis du vil have vist flere detaljer om et kort eller åbne posten i [!INCLUDE [prod_short](includes/prod_short.md)], skal brugere have læsetilladelse til siden og dens data.
    - Hvis du vil ændre data, skal brugerens behov redigeres.
    
    Du kan finde flere oplysninger om rettigheder i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).

## <a name="managing-privacy-and-compliance"></a>Administrere beskyttelse af personlige oplysninger og overholdelse 

Microsoft Teams indeholder omfattende styring af overholdelse og håndtering af følsomme eller personlige data&mdash;herunder data, som er føjet til chats og kanaler fra [!INCLUDE [prod_short](includes/prod_short.md)]-appen.

### <a name="understanding-where-prod_short-cards-are-stored"></a>Om, hvor [!INCLUDE [prod_short](includes/prod_short.md)]-kort gemmes 

Når et kort er sendt til en chat, kopieres kortet og de felter, der vises på kortet, til team. Disse oplysninger er underlagt team politikkerne for organisationen, f. eks. politikker for opbevaring af data. Når der vises kort detaljer, er ingen af dataene i vinduet detaljer gemt i grupper. Dataene gemmes stadig i [!INCLUDE [prod_short](includes/prod_short.md)] og bliver kun hentet af Teams, når brugeren vælger at få vist detaljerne. 

- Du kan finde flere oplysninger om, hvor grupper lagrer disse data, i [Placering af data i Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Du kan få mere at vide om opbevaringspolitikker i grupper under [Opbevaringspolitikker i Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Begrænse deling af kort 

Du kan forhindre, at bestemte brugere eller grupper sender kort til chatrum eller kanaler ved at oprette meddelelses politikker, der deaktiverer indstilling af **URL-eksempler**. Du kan finde flere oplysninger om denne indstilling under [Administrér meddelelsespolitikker i Teams](/microsoftteams/messaging-policies-in-teams). 

Du kan også bruge informations hinder til at forhindre, at personer eller grupper kommunikerer med hinanden. Du kan finde flere oplysninger i [Informationsbarrierer i Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Funktionerne til forebyggelse af datatab i Microsoft 365 Security & Compliance Center kan ikke anvendes specifikt på kort. Men de kan anvendes på de chatmeddelelser, der indeholder kortene. Du kan spore kommende avancerede funktioner, der omfatter aktivering af DLP til kort, i [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).

### <a name="responding-to-data-requests"></a>Reagere på anmodninger om data

Du kan give teammedlemmer og team ejere mulighed for at slette meddelelser, der indeholder følsomme kort, ved at oprette meddelelses politikker, f. eks **Ejere kan slette sendte meddelelser** og **Brugere kan slette sendte meddelelser**. Du kan finde flere oplysninger om denne indstilling under [Administrér meddelelsespolitikker i Teams](/microsoftteams/messaging-policies-in-teams).

Indholdssøgning og opdagelse af overholdelsesfunktioner i i Microsoft 365 Security & Compliance Center kan ikke anvendes specifikt på kort. Men de kan anvendes på de chatmeddelelser, der indeholder kort. Du kan spore kommende kompatibilitetsfunktioner for kort i [https://www.microsoft.com/microsoft-365/roadmap?featureid=68875](https://www.microsoft.com/microsoft-365/roadmap?featureid=68875).

Da kortdata i grupper er en kopi af data i [!INCLUDE [prod_short](includes/prod_short.md)], kan du også bruge [!INCLUDE [prod_short](includes/prod_short.md)]-funktioner til at eksportere en kundes data, hvis der er anmodet om det. Du kan finde flere oplysninger om beskyttelse af personlige oplysninger i [!INCLUDE [prod_short](includes/prod_short.md)] under [Ofte stillede spørgsmål om beskyttelse Business Central-kunder](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="see-also"></a>Se også
[[!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams Oversigt over integration](across-teams-overview.md)  
[Installér appen [!INCLUDE [prod_short](includes/prod_short.md)] til Microsoft Teams](across-install-app-for-teams.md)  
[Teams, ofte stillede spørgsmål](teams-faq.md)  
[Fejlfinding i Teams](admin-teams-troubleshooting.md)  
[Udvikling af Teams-integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]