---
title: Fejlfinde adgang med Microsoft 365-licenser
description: 'Få mere at vide om, hvordan du kan løse problemer med at få adgang til Business central med en Microsoft 365-licens.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: troubleshooting
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# Fejlfinde adgang med Microsoft 365-licenser

## Symptomer

Når du åbner en post i Teams, vises der en fejlmeddelelse i en eller flere af de kortdetaljer, der ligner:

"Denne side bruger data fra relaterede tabeller, som du ikke har adgang til. Hvis du vil arbejde med alle funktioner på denne side, skal du kontakte din administrator."

## Årsag

Du mangler sandsynligvis objekttilladelser til tabeller, som den aktuelle side eller post er knyttet til.

## Symptomer

Adgang er aktiveret, men brugerne får en tilladelsesfejl, når de får adgang til en post.

## Årsag

Hvis du aktiverer adgang i Business central-administration, men ikke tildeler tilladelser på siden licens konfiguration, er alle, der forsøger at få adgang til Business Central-poster i Teams, klargjort uden tilladelse til objekter. Business Central er sikret af design: Administratorer skal først konfigurere, hvilke data der kan opnås adgang til i Teams. 

## Løsning

Hvis du tilpasser tilladelserne på siden med licenskonfiguration, påvirker det kun de senest oprettede brugere. Du skal også tildele de manglende tilladelser til de brugere, der allerede er oprettet, via siden med brugerliste. 

## Symptomer

Når jeg deler et hyperlink i Teams, får andre fejlmeddelelsen "Når du får adgang til Business central med en Microsoft 365-licens, kan du kun få vist data i Microsoft Teams" .

## Årsag

Når du deler et Business Central-link til en Teams-chat eller kanaler, navigerer et hyperlink altid ud af Microsoft Teams, hvor dataene ikke længere bliver tilgængelige for en person med Microsoft 365-licens.

## Løsning

Når du deler sider eller poster, skal du enten medtage linkforhåndsversionen som et kort, eller du kan dele data som en fane i chatten eller kanalen.

## Se også

[Business Central-adgang med Microsoft 365-licenser](admin-access-with-m365-license.md#minimum-requirements)  
[Konfigurere adgang til Microsoft 365-licenser](admin-access-with-m365-license-setup.md)  
[Business central og Microsoft Teams-integration](across-teams-overview.md)
[Dele Business Central-poster og sidelinks i Microsoft Teams](across-working-with-teams.md)  
[Foretage fejlfinding af integration af Teams](admin-teams-troubleshooting.md)  