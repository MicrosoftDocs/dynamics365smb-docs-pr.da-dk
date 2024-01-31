---
title: 'Fejlfinding: Adgang til kamera og placering'
description: 'Denne artikel beskriver, hvordan du retter fejl i forbindelse med adgang til kamera- og placeringsoplysninger i Business central.'
author: brentholtorf
ms.author: bholtorf
ms.date: 04/01/2021
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
ms.service: dynamics-365-business-central
---

# Fejlfinding: Adgang til kamera og placering

Der kan opstå fejl, når du forsøger at få adgang til en enheds kamera- og placeringsoplysninger via [!INCLUDE[prod_short](includes/prod_short.md)]. På listen nedenfor kan du se de mulige årsager til disse fejl, og hvordan du retter dem.

## Enhed skal have kamera- og placeringsfunktioner

For at du kan få adgang til kameraet eller brugerens placering på en enhed, skal enheden have et fysisk kamera eller muligheden for at hente oplysninger om placeringen.

Hvis din enhed har kamera- og placeringsfunktioner, men der stadig opstår fejl, skal nogle af driverne muligvis opdateres eller geninstalleres. Selvom du ikke er sikker, anbefaler vi altid, at du opdaterer enhedens operativsystem, drivere og browser til den seneste version, så du får den bedste oplevelse.

## Adgangstilladelser er ikke aktiveret

Du skal aktivere generel adgang til kamera og placering i enhedens indstillinger for beskyttelse af personlige oplysninger og give [!INCLUDE[prod_short](includes/prod_short.md)] udtrykkelig tilladelse til at få adgang til dem. Hvis du f.eks. vil se eller ændre tilladelser for en enhed, der kører i Windows, skal du gå til **Indstillinger**, vælge **Beskyttelse af personlige oplysninger** og derefter gå til **App-tilladelser**. 

I forbindelse med mobilenheder skal du give kamera- og placeringsadgangstilladelserne til [!INCLUDE[prod_short](includes/prod_short.md)]-mobilappen. Hvis du vil gøre det for en iOS-enhed, skal du gå til **Indstillinger**, vælge **Beskyttelse af personlige oplysninger** og derefter vælge **Kamera** eller **Lokation**. Hvis du bruger en Android-enhed, skal du vælge **Indstillinger**, vælge **Apps og meddelelser**, **Avanceret**, **Rettighedsadministrator** og derefter **Kamera** eller **Placering**.

Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] i en browser, skal du desuden give [!INCLUDE[prod_short](includes/prod_short.md)]-webstedet tilladelse til at få adgang til oplysninger om kamera eller placering. Hvis du vil se eller ændre tilladelserne for et websted i Microsoft Edge-browseren, skal du gå til **Indstillinger**, vælge **Webstedstilladelser** og derefter vælge **Kamera** eller **Placering**. Bemærk, at dette kan være anderledes for andre browsere.

Som standard viser enheden eller browseren en anmodning om at få adgang til disse egenskaber, når brugeren aktiverer dem første gang.

> [!NOTE]  
> Nogle ældre browsere giver ikke adgang til kamera og placering. Kameraet er f.eks. ikke tilgængeligt i Internet Explorer eller den ældre Microsoft Edge-browser.

## Webklientens forbindelse er ikke sikker

Kamera- og placeringsfunktionerne er kun tilgængelige, når du får adgang til webklienten via SSL-sikrede HTTP-forbindelser ved hjælp af `https://` URI-skemaet. 

Den eneste undtagelse er at oprette forbindelse til `http://localhost`, der bruges til udviklings- og testformål.


## Arbejde med virtualiseringsteknologier

Når der oprettes forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)] med fjernskrivebordet eller en anden virtualisering, er der muligvis ikke adgang til kameraet eller placeringen. Hvis det er tilfældet, skal du bruge det fysiske system i stedet for.

## Antivirusprogram
Nogle antivirusprogrammer blokerer som standard for kamera og placering. Husk at kontrollere indstillingerne for dit antivirusprogram.

## Se også
[Implementering af kameraet i AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[Implementering af placeringen i AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)


[!INCLUDE[footer-include](includes/footer-banner.md)]