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
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989354"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a>Administration af Microsoft Teams-integration med Business Central

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

Denne artikel giver en oversigt over, hvad du kan gøre som administrator for at kontrollere Microsoft Teams-integration med [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="in-microsoft-teams"></a>I Microsoft Teams

### <a name="minimum-requirements"></a>Minimumkrav

I dette afsnit beskrives minimumkrav til [!INCLUDE [prodshort](includes/prodshort.md)]-appfunktioner for at arbejde i Teams.

- Krævede licenser

    Denne tabel giver dig et overblik over de licenser, der er nødvendige for at [!INCLUDE [prodshort](includes/prodshort.md)]-appfunktionerne kan bruges i Teams.

    |Hvad|Teams-licens|Business Central-licens|
    |----|---|---|
    |Indsæt et link til en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en samtale, og send den som et kort.|![markering](media/check.png "check")|![markering](media/check.png "check")|
    |Se et kort over en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en samtale.|![markering](media/check.png "check")||
    |Se flere oplysninger om et kort for en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en samtale.|![markering](media/check.png "check")|![markering](media/check.png "check")|

- Tillad URL-prøveversion

    **Indstillingen Tillad URL-prøveversion** skal være aktiveret. I modsat fald kan der ikke oprettes et kort til Business Central-links, der er indsat i en samtale med Teams. Du kan finde flere oplysninger om denne indstilling under [Administrér meddelelsespolitikker i Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-business-central-app-optional"></a>Administration af Business Central-app (prøveversion)

Som Teams-administrator kan du administrere alle apps for din organisation, herunder [!INCLUDE [prodshort](includes/prodshort.md)]-appen. Du kan godkende eller installere [!INCLUDE [prodshort](includes/prodshort.md)]-appen for din organisation, blokere bruger fra installation af appen og meget mere.

Du kan finde flere oplysninger i følgende artikler i Microsoft Teams-dokumentationen:

- [Administrer dine apps i Microsoft Teams Administration](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Administrer politikker for app-opsætning i Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a>I [!INCLUDE [prodshort](includes/prodshort.md)]

### <a name="minimum-requirements"></a>Minimumkrav

- [!INCLUDE [prodshort](includes/prodshort.md)] version:

    [!INCLUDE [prodshort](includes/prodshort.md)] 2020 release Wave 2 (version 17) eller nyere. Teams-integration understøttes kun [!INCLUDE [prodshort](includes/prodshort.md)] online, men ikke lokalt.

- Kode enhed **2718 Page Summary Provider** udgives som en webtjeneste:

    Denne codeunit er som standard udgivet som en webtjeneste. Codeunit er en del af [!INCLUDE [prodshort](includes/prodshort.md)]-systemprogrammet. Den bruges til at hente feltdataene til en [!INCLUDE [prodshort](includes/prodshort.md)]-side, der er føjet til en Teams-samtale. 

- Brugerrettigheder:

    De sider og data, som brugerne kan få vist og redigere i en Teams-samtale, kontrolleres oftest af deres tilladelser i [!INCLUDE [prodshort](includes/prodshort.md)].
    
    - Hvis du vil indsætte et [!INCLUDE [prodshort](includes/prodshort.md)]-hyperlink i en Teams-samtale og få den på et kort, skal brugerne som minimum have læsetilladelse til siden og dens data.
    - Når et kort er sendt til en samtale, kan alle brugere i denne samtale se dette kort uden tilladelse til Business Central.
    - Hvis du vil have vist flere detaljer om et kort eller åbne posten i [!INCLUDE [prodshort](includes/prodshort.md)], skal brugere have læsetilladelse til siden og dens data.
    - Hvis du vil ændre data, skal brugerens behov redigeres.
    
    Du kan finde flere oplysninger om rettigheder i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).

## <a name="see-also"></a>Se også
[Business Central og Microsoft Teams Oversigt over integration](across-teams-overview.md)  
[Installér appen [!INCLUDE [prodshort](includes/prodshort.md)] til Microsoft Teams](across-install-app-for-teams.md)  
[Udvikling af Teams-integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Introduktion](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
