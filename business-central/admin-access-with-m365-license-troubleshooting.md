---
title: Fejlfinde adgang med Microsoft 365-licenser
description: 'Få mere at vide om, hvordan du kan løse problemer med at få adgang til Business central med en Microsoft 365-licens.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.date: 02/07/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# <a name="troubleshoot-access-with-microsoft-365-licenses" />Fejlfinde adgang med Microsoft 365-licenser

## <a name="this-page-uses-data-from-related-tables-that-you-do-not-have-access-to-error-message" />Fejlmeddelelse "Denne side bruger data fra relaterede tabeller, som du ikke har adgang til"

### <a name="symptoms" />Symptomer

Når du åbner en post i Teams, vises der en fejlmeddelelse i en eller flere af de kortdetaljer, der ligner:

"Denne side bruger data fra relaterede tabeller, som du ikke har adgang til. Hvis du vil arbejde med alle funktioner på denne side, skal du kontakte din administrator."

### <a name="cause" />Årsag

Du mangler sandsynligvis objekttilladelser til tabeller, som den aktuelle side eller post er knyttet til.

## <a name="microsoft-365-access-has-been-enabled-but-users-get-a-permission-error" />Microsoft 365-adgang er aktiveret, men brugerne får en tilladelsesfejl

### <a name="symptoms" />Symptomer

Adgang med Microsoft 365 er aktiveret i Business Central Administration, men brugerne får en tilladelsesfejl, når de får adgang til en post.

### <a name="cause" />Årsag

Hvis du aktiverer adgang i Business central-administration, men ikke tildeler tilladelser på siden **Licenskonfiguration**, er alle, der forsøger at få adgang til Business Central-poster i Teams, klargjort uden tilladelse til objekter. Business Central er sikret af design: Administratorer skal først konfigurere, hvilke data der kan opnås adgang til i Teams. 

### <a name="resolution" />Løsning

Hvis du tilpasser tilladelserne på siden med licenskonfiguration, påvirker det kun de senest oprettede brugere. Du skal også tildele de manglende tilladelser til de brugere, der allerede er oprettet, via siden med brugerliste. 

## <a name="you-shared-a-link-in-teams-but-users-get-a-message-that-they-can-only-view-data" />Du har delt et link i grupper, men brugerne får en meddelelse om, at de kun kan få vist data

### <a name="symptoms" />Symptomer

Når jeg deler et hyperlink i Teams som Business Central-bruger, får andre fejlmeddelelsen "Når du får adgang til Business central med en Microsoft 365-licens, kan du kun få vist data i Microsoft Teams" .

### <a name="cause" />Årsag

Når du deler et Business Central-link til en Teams-chat eller kanaler, navigerer et hyperlink altid ud af Microsoft Teams, hvor dataene ikke længere bliver tilgængelige for en person med Microsoft 365-licens.

### <a name="resolution" />Løsning

Når du deler sider eller poster, skal du enten medtage linkforhåndsversionen som et kort, eller du kan dele data som en fane i chatten eller kanalen.

## <a name="card-from-shared-link-is-minimal-and-doesnt-include-details-button" />Kort fra delt link er minimalt og indeholder ikke oplysninger om knappen detaljer

### <a name="symptoms" />Symptomer

Når en Microsoft 365-licensindehaver uden en Business Central-licens deler et Business Central-link i Teams, udvides den automatisk til et kort, der ikke har nogen brugbare oplysninger, og viser kun Business central uden knappen **Detaljer**.

### <a name="cause" />Årsag

Brugere, der har en Microsoft 365-licens, men ingen Business central-licens, har tilladelse til at dele links som kort. Hvis brugeren har Business central-app til Teams installeret og indsætter et link i meddelelsesområdet, vises der kun et minimalt kort. 

## <a name="see-also" />Se også

[Business Central-adgang med Microsoft 365-licenser](admin-access-with-m365-license.md#minimum-requirements)  
[Konfigurere adgang til Microsoft 365-licenser](admin-access-with-m365-license-setup.md)  
[Business central og Microsoft Teams-integration](across-teams-overview.md)
[Dele Business Central-poster og sidelinks i Microsoft Teams](across-working-with-teams.md)  
[Foretage fejlfinding af integration af Teams](admin-teams-troubleshooting.md)  
