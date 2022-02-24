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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: f6b771b0107214702785d2b124983eb369741a84
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187912"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Oprette forbindelse til dine Business Central-data for at oprette en forretningsapp ved hjælp af Power Apps

Du kan gøre dine [!INCLUDE[prodshort](includes/prodshort.md)]-data tilgængelige som en datakilde i Power Apps.  

> [!NOTE]  
> Du skal have en gyldig konto til [!INCLUDE[prodshort](includes/prodshort.md)] og til Power Apps.  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a>Sådan tilføjes [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power Apps

1. Gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/) i din webbrowser, og log på.
2. Vælg **Apps** på startsiden, **Opret en app** og **Lærred** for at oprette en ny lærreds-app. Denne app vil blive udformet til brug på en mobilenhed, men du kan også vælge at bruge en anden skabelon.

    Næste trin til oprettelse af en Power App er at vælge dataene. Vælg ikonet med pilen, og vælg derefter indstillingen **Ny forbindelse** øverst til venstre side på siden.
3. Vælg **Business Central** på listen over tilgængelige forbindelser, og vælg derefter knappen **Opret**.

    Power Apps opretter forbindelse til din [!INCLUDE [prodshort](includes/prodshort.md)] ved hjælp af de legitimationsoplysninger, du er logget på med. Hvis du ikke er administrator af din [!INCLUDE [prodshort](includes/prodshort.md)], skal du muligvis logge på med en anden konto.  

4. Power Apps viser en liste over *Miljøer og regnskaber*, der er tilgængelige fra [!INCLUDE [prodshort](includes/prodshort.md)]. Vælg det miljø og regnskab, der indeholder de data, du vil oprette forbindelse til. Derefter vises en liste over API'er. Vælg den **API**, du vil oprette forbindelse til.

Disse såkaldte tabeller er en del af [!INCLUDE [prodshort](includes/prodshort.md)] API'en. Du behøver ikke selv at konfigurere slutpunkterne – [!INCLUDE [prodshort](includes/prodshort.md)]-connectoren til Power Apps gør det for dig.  

> [!NOTE]
> Hvis du vil medtage data fra andre tabeller i [!INCLUDE [prodshort](includes/prodshort.md)] i din app, skal du samarbejde med en udvikler om at definere en brugerdefineret API i [!INCLUDE [prodshort](includes/prodshort.md)] og derefter bruge denne API via en brugerdefineret connector i Power Apps. Du kan finde flere oplysninger i [Oprette en brugerdefineret connector fra bunden](/connectors/custom-connectors/define-blank).  

Nu har du oprettet forbindelse til dine [!INCLUDE [prodshort](includes/prodshort.md)]-data og er klar til at opbygge din PowerApp. Du kan tilføje yderligere skærmbilleder og oprette forbindelse til flere data fra dit [!INCLUDE [prodshort](includes/prodshort.md)]. Du kan finde flere oplysninger i [Oprette en lærreds-app fra en skabelon i Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Når du har designet og opbygget din app, kan du dele den med dine kolleger. Du kan finde flere oplysninger i [Gemme og udgive en lærreds-app i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Hvis du vil oprette forbindelse til [!INCLUDE [prodshort](includes/prodshort.md)] i det lokale miljø, skal du vælge **Business Central til det lokale miljø**-connectoren i trin 3.  

## <a name="see-also"></a>Se også

[Oprette en lærreds-app fra en skabelon i Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Introduktion](product-get-started.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
[Introduktion til udvikling af Connect-apps til Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
