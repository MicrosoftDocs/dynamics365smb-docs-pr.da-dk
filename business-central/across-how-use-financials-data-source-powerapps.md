---
title: Bruge dine data til at oprette en app | Microsoft Docs
description: Du kan gøre dine Business Central-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette en forretningsapp ved hjælp af Power Apps.
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 04/01/2023
ms.author: jswymer
---
# Oprette forbindelse til dine Business Central-data for at oprette en forretningsapp ved hjælp af Power Apps

Du kan gøre dine [!INCLUDE[prod_short](includes/prod_short.md)]-data tilgængelige som en datakilde i Power Apps.  

> [!TIP]  
> Den ekstra Power Apps-dokumentation og vores Power app-eksempler, der vises under [!INCLUDE[prod_short](includes/prod_short.md)]-lanceringen, udgives her senere i 2023 bølge 1. Læs mere på [Introduktion til flere Power Automate-skabelonprøver og Power Apps](/dynamics365/release-plan/2023wave1/smb/dynamics365-business-central/get-started-more-sample-power-automate-templates-power-apps).

## Forudsætninger

Du skal have en gyldig konto til [!INCLUDE[prod_short](includes/prod_short.md)] og til Power Apps.  

## Tilføje [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power Apps

1. Gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/) i din webbrowser, og log på.
2. Vælg feltet **Andre datakilder** på startsiden i afsnittet **Start fra data**.  

    Dette trin åbner Power Apps Studio. Når du logger på første gang, skal du angive land/område.  
3. Vælg **Business Central**på listen over tilgængelige forbindelser, og vælg derefter knappen **Opret**.

    Power Apps opretter forbindelse til din [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af de legitimationsoplysninger, du er logget på med. Hvis du ikke er administrator af din [!INCLUDE[prod_short](includes/prod_short.md)], skal du muligvis logge på med en anden konto.  

4. Power Apps viser en liste over *Miljøer og regnskaber*, der er tilgængelige fra [!INCLUDE[prod_short](includes/prod_short.md)]. Vælg det miljø og den virksomhed, der indeholder de data, du vil oprette forbindelse til, f.eks. *PRODUKTION - Min virksomhed*.  

5. Derefter vises en liste over de tabeller, der eksponeres som en del af API'en for dit miljø. Vælg den tabel, du vil oprette forbindelse til, og vælg derefter **Opret forbindelse**.

Disse såkaldte tabeller eksponeres som slutpunkter af [!INCLUDE[prod_short](includes/prod_short.md)]-connectoren til Power Apps.  

> [!NOTE]
> Hvis du vil medtage data fra andre tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] i din app, skal du samarbejde med en udvikler om at definere en brugerdefineret API i [!INCLUDE[prod_short](includes/prod_short.md)].  

Nu har du oprettet forbindelse til dine [!INCLUDE[prod_short](includes/prod_short.md)]-data og er klar til at opbygge din Power App. Du kan tilføje flere skærmbilleder og oprette flere data fra dit [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Oprette en lærreds-app ud fra et eksempel i Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Når du har designet og opbygget din app, kan du dele den med dine kolleger. Du kan finde flere oplysninger i [Gemme og udgive en lærreds-app i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Hvis du vil oprette forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø, skal du vælge **Business Central til det lokale miljø**-connectoren i trin 3.  

## Se relateret [Microsoft-træning](/training/paths/power-apps-power-automate-business-central/)

## Se også

[Oprette en lærreds-app fra en skabelon i Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Import af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Introduktion til udvikling af Connect-apps til Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
