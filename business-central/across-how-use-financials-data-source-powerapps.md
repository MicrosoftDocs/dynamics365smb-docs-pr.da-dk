---
title: Bruge dine data til at oprette en app | Microsoft Docs
description: Du kan gøre dine Business Central-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette en forretningsapp ved hjælp af PowerApps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 05/13/2019
ms.author: edupont
ms.openlocfilehash: 67d7129e32ccde3154a02dd12b806d712f470833
ms.sourcegitcommit: 92c7b6c5f0a5d8becbef106ab85258906765bc3e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540265"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Oprette forbindelse til dine Business Central-data for at oprette en forretningsapp ved hjælp af PowerApps
Du kan gøre dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tilgængelige som en datakilde i PowerApps.  

> [!NOTE]  
>   Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til PowerApps.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Sådan tilføjes [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i PowerApps
1. Gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) i din webbrowser, og log på.
2. På startsiden skal du vælge skabelonen **Start fra data** for at oprette en ny lærreds-app. Denne app vil blive udformet til brug på en mobilenhed, men du kan også vælge at bruge en anden skabelon.

    Næste trin til oprettelse af en PowerApp er at vælge dataene. Vælg ikonet med pilen, og vælg derefter indstillingen **Ny forbindelse** øverst til venstre side på siden.
3. Vælg **Business Central**på listen over tilgængelige forbindelser, og vælg derefter knappen **Opret**.

    PowerApps opretter forbindelse til din [!INCLUDE [prodshort](includes/prodshort.md)] ved hjælp af de legitimationsoplysninger, du er logget på med. Hvis du ikke er administrator af din [!INCLUDE [prodshort](includes/prodshort.md)], skal du muligvis logge på med en anden konto.  

4. Hvis du har mere end én virksomhed i din [!INCLUDE [prodshort](includes/prodshort.md)], skal du vælge den virksomhed, du vil oprette forbindelse til. PowerApps viser derefter en liste over *tabeller*, der er tilgængelige fra [!INCLUDE [prodshort](includes/prodshort.md)]. Disse såkaldte tabeller er en del af [!INCLUDE [prodshort](includes/prodshort.md)] API'en. Du behøver ikke selv at konfigurere slutpunkterne - [!INCLUDE [prodshort](includes/prodshort.md)]-connectoren til PowerApps gør det for dig.  

    Hvis du vil medtage data fra andre tabeller i [!INCLUDE [prodshort](includes/prodshort.md)] i din app, skal du samarbejde med en udvikler om at definere en brugerdefineret API i [!INCLUDE [prodshort](includes/prodshort.md)] og derefter bruge denne API via en brugerdefineret connector i PowerApps. Du kan finde flere oplysninger i [Oprette en brugerdefineret connector fra bunden](/connectors/custom-connectors/define-blank).  

Nu har du oprettet forbindelse til dine [!INCLUDE [prodshort](includes/prodshort.md)]-data og er klar til at opbygge din PowerApp. Du kan tilføje yderligere skærmbilleder og oprette forbindelse til flere data fra dit [!INCLUDE [prodshort](includes/prodshort.md)]. Du kan finde flere oplysninger i [Oprette en lærreds-app fra en skabelon i PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Når du har designet og opbygget din app, kan du dele den med dine kolleger. Du kan finde flere oplysninger i [Gemme og udgive en lærreds-app i PowerApps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Hvis du vil oprette forbindelse til [!INCLUDE [prodshort](includes/prodshort.md)] i det lokale miljø, skal du vælge **Business Central til det lokale miljø**-connectoren i trin 3.  

## <a name="see-also"></a>Se også

[Oprette en lærreds-app fra en skabelon i PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Introduktion](product-get-started.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
[Introduktion til udvikling af Connect-apps til Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
