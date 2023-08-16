---
title: Bruge dine data til at oprette en app | Microsoft Docs
description: Du kan gøre dine Business Central-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette en forretningsapp ved hjælp af Power Apps.
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 05/15/2023
ms.author: jswymer
---
# Oprette forbindelse til dine Business Central-data for at oprette en forretningsapp ved hjælp af Power Apps

Du kan gøre dine [!INCLUDE[prod_short](includes/prod_short.md)]-data tilgængelige som en datakilde i Power Apps.  

> [!TIP]  
> Business Central tilbyder nu understøttelse til udvikling og drift til Power Platform i AL-Go og eksempler, så du kan komme i gang med at oprette dine egne apps med Power Apps. Disse funktioner findes i øjeblikket som forhåndsversion. Hvis du vil vide mere, kan du gå videre til [Business Central og Power Apps](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-overview) i Hjælp til it-fagfolk.

## Forudsætninger

Du skal have en gyldig konto til [!INCLUDE[prod_short](includes/prod_short.md)] og til Power Apps.  

## Tilføje [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power Apps

Denne fremgangsmåde tilføjer en Business Central-tabel, f. eks. kunder eller varer, som datakilde til en Power Apps-app.

1. Gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/) i din webbrowser, og log på.
2. Marker **+ Opret** i navigationsruden til venstre, og vælg derefter **Flere datakilder** på siden **Opret app**.
  
   <!-- This step opens Power Apps canavs. On first sign-in, you must specify the country/region.  -->
3. De **forbindelser**, der vises på listen, viser eksisterende dataforbindelser.

   - Hvis der allerede er en **Business Central**-forbindelse, skal du markere den og derefter vælge **Opret**.

   - Hvis du ikke kan se en Business Central-forbindelse, skal du vælge **+ ny forbindelse**, søge efter og vælge **Business Central** og derefter vælge **Opret**.

   > [!NOTE]
   > Hvis du vil oprette forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø, skal du vælge **Business Central til det lokale miljø**-connectoren.  
  
4. Power Apps opretter forbindelse til din [!INCLUDE[prod_short](includes/prod_short.md)]. Log på med Business central-kontoens kontonavn og adgangskode. Hvis du ikke er administrator af din [!INCLUDE[prod_short](includes/prod_short.md)], skal du muligvis logge på med en anden konto.  
5. Når du er logget ind, viser Power Apps en liste over *Miljøer og regnskaber*, der er tilgængelige fra [!INCLUDE[prod_short](includes/prod_short.md)]. Vælg det miljø og den virksomhed, der indeholder de data, du vil oprette forbindelse til, f.eks. *PRODUKTION - Min virksomhed*.  
6. Derefter vises en liste over de tabeller, der eksponeres som en del af API'en for dit miljø. Vælg den tabel, du vil oprette forbindelse til, og vælg derefter **Opret forbindelse**.

Disse såkaldte tabeller eksponeres som slutpunkter af [!INCLUDE[prod_short](includes/prod_short.md)]-connectoren til Power Apps.  

> [!NOTE]
> Hvis du vil medtage data fra andre tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] i din app, skal du samarbejde med en udvikler om at definere en brugerdefineret API i [!INCLUDE[prod_short](includes/prod_short.md)].  

Nu har du oprettet forbindelse til dine [!INCLUDE[prod_short](includes/prod_short.md)]-data og er klar til at opbygge din Power App. Du kan altid tilføje flere skærmbilleder og oprette forbindelse til flere data. Du kan få mere at vide på [Oprette en lærredsapp ud fra et eksempel i Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Når du har designet og opbygget din app, kan du dele den med dine kolleger. Du kan finde flere oplysninger i [Gemme og udgive en lærreds-app i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

<!--
## Sample apps to get started

As a preview version, Business Central offers several sample apps that you can use as a starting point for building your own apps that use Business Central data. These sample apps are available in the [Business Central Demos](https://github.com/BusinessCentralDemos) repo on GitHub. For a quick overview on the apps, go to [Power Apps samples for Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-samples).

## Develop and maintain apps application lifecycle management

As an app developer, you may already be familiar with Business Central AL-Go. AL-Go is set of tools on GiHub that enables you to maintain professional DevOps processes for your Business Central AL projects. AL-Go supports source control and activities, like building, testing, and deploying. As a preview, Business Central now offers an Al-Go version that supports for Power Platform solutions. The preview, for example, includes workflows that let you push and pull Power Platfrom changes to and from enviroments. You can access the tools at [https://github.com/BusinessCentralDemos/AL-Go-PTE](https://github.com/BusinessCentralDemos/AL-Go-PTE). For more information, see [Application lifecycle management for Power Apps in Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-alm).-->

## Se relateret [Microsoft-træning](/training/paths/power-apps-power-automate-business-central/)

## Se også

[Oprette en lærreds-app fra en skabelon i Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Import af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Introduktion til udvikling af Connect-apps til Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
