---
title: Bruge dine data til at oprette en app | Microsoft Docs
description: Du kan gøre dine Business Central-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette en forretningsapp ved hjælp af Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 06/22/2020
ms.author: edupont
ms.openlocfilehash: 8f0eb7a1562a8300bd7181ef6470c70f60934470
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528634"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Oprette forbindelse til dine Business Central-data for at oprette en forretningsapp ved hjælp af Power Apps

Du kan gøre dine [!INCLUDE[prodshort](includes/prodshort.md)]-data tilgængelige som en datakilde i Power Apps.  

> [!NOTE]  
> Du skal have en gyldig konto til [!INCLUDE[prodshort](includes/prodshort.md)] og til Power Apps.  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a>Sådan tilføjes [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power Apps

1. Gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/) i din webbrowser, og log på.
2. Vælg feltet **Andre datakilder** på startsiden i afsnittet **Start fra data**.  

    Dette åbner Power Apps Studio. Når du logger på første gang, skal du angive land/område.  
3. Vælg **Business Central**på listen over tilgængelige forbindelser, og vælg derefter knappen **Opret**.

    Power Apps opretter forbindelse til din [!INCLUDE[prodshort](includes/prodshort.md)] ved hjælp af de legitimationsoplysninger, du er logget på med. Hvis du ikke er administrator af din [!INCLUDE[prodshort](includes/prodshort.md)], skal du muligvis logge på med en anden konto.  

4. Power Apps viser en liste over *Miljøer og regnskaber*, der er tilgængelige fra [!INCLUDE[prodshort](includes/prodshort.md)]. Vælg det miljø og den virksomhed, der indeholder de data, du vil oprette forbindelse til, f.eks. *PRODUKTION - Min virksomhed*.  

5. Derefter vises en liste over de tabeller, der eksponeres som en del af API'en for dit miljø. Vælg den tabel, du vil oprette forbindelse til, og vælg derefter **Opret forbindelse**.

Disse såkaldte tabeller eksponeres som slutpunkter af [!INCLUDE[prodshort](includes/prodshort.md)]-connectoren til Power Apps.  

> [!NOTE]
> Hvis du vil medtage data fra andre tabeller i [!INCLUDE[prodshort](includes/prodshort.md)] i din app, skal du samarbejde med en udvikler om at definere en brugerdefineret API i [!INCLUDE[prodshort](includes/prodshort.md)] og derefter bruge denne API via en brugerdefineret connector i Power Apps. Du kan finde flere oplysninger i [Oprette en brugerdefineret connector fra bunden](/connectors/custom-connectors/define-blank).  

Nu har du oprettet forbindelse til dine [!INCLUDE[prodshort](includes/prodshort.md)]-data og er klar til at opbygge din PowerApp. Du kan tilføje yderligere skærmbilleder og oprette forbindelse til flere data fra dit [!INCLUDE[prodshort](includes/prodshort.md)]. Du kan finde flere oplysninger under [Oprette en lærreds-app ud fra et eksempel i Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Når du har designet og opbygget din app, kan du dele den med dine kolleger. Du kan finde flere oplysninger i [Gemme og udgive en lærreds-app i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Hvis du vil oprette forbindelse til [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø, skal du vælge **Business Central til det lokale miljø**-connectoren i trin 3.  

## <a name="see-also"></a>Se også

[Oprette en lærreds-app fra en skabelon i Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importer virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Introduktion til udvikling af Connect-apps til Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
