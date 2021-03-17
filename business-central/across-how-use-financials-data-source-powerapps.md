---
title: Bruge dine data til at oprette en app | Microsoft Docs
description: Du kan gøre dine Business Central-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette en forretningsapp ved hjælp af Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0bfa7a36a7655b4b26dfbfd11688fe42eeb19cfe
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379319"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="48d10-103">Oprette forbindelse til dine Business Central-data for at oprette en forretningsapp ved hjælp af Power Apps</span><span class="sxs-lookup"><span data-stu-id="48d10-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="48d10-104">Du kan gøre dine [!INCLUDE[prod_short](includes/prod_short.md)]-data tilgængelige som en datakilde i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="48d10-104">You can make your [!INCLUDE[prod_short](includes/prod_short.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="48d10-105">Du skal have en gyldig konto til [!INCLUDE[prod_short](includes/prod_short.md)] og til Power Apps.</span><span class="sxs-lookup"><span data-stu-id="48d10-105">You must have a valid account with [!INCLUDE[prod_short](includes/prod_short.md)] and with Power Apps.</span></span>  

## <a name="to-add-prod_short-as-a-data-source-in-power-apps"></a><span data-ttu-id="48d10-106">Sådan tilføjes [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power Apps</span><span class="sxs-lookup"><span data-stu-id="48d10-106">To add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="48d10-107">Gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/) i din webbrowser, og log på.</span><span class="sxs-lookup"><span data-stu-id="48d10-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="48d10-108">Vælg feltet **Andre datakilder** på startsiden i afsnittet **Start fra data**.</span><span class="sxs-lookup"><span data-stu-id="48d10-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="48d10-109">Dette åbner Power Apps Studio.</span><span class="sxs-lookup"><span data-stu-id="48d10-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="48d10-110">Når du logger på første gang, skal du angive land/område.</span><span class="sxs-lookup"><span data-stu-id="48d10-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="48d10-111">Vælg **Business Central** på listen over tilgængelige forbindelser, og vælg derefter knappen **Opret**.</span><span class="sxs-lookup"><span data-stu-id="48d10-111">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="48d10-112">Power Apps opretter forbindelse til din [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af de legitimationsoplysninger, du er logget på med.</span><span class="sxs-lookup"><span data-stu-id="48d10-112">Power Apps will connect to your [!INCLUDE[prod_short](includes/prod_short.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="48d10-113">Hvis du ikke er administrator af din [!INCLUDE[prod_short](includes/prod_short.md)], skal du muligvis logge på med en anden konto.</span><span class="sxs-lookup"><span data-stu-id="48d10-113">If you are not an administrator of your [!INCLUDE[prod_short](includes/prod_short.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="48d10-114">Power Apps viser en liste over *Miljøer og regnskaber*, der er tilgængelige fra [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="48d10-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="48d10-115">Vælg det miljø og den virksomhed, der indeholder de data, du vil oprette forbindelse til, f.eks. *PRODUKTION - Min virksomhed*.</span><span class="sxs-lookup"><span data-stu-id="48d10-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company*.</span></span>  

5. <span data-ttu-id="48d10-116">Derefter vises en liste over de tabeller, der eksponeres som en del af API'en for dit miljø.</span><span class="sxs-lookup"><span data-stu-id="48d10-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="48d10-117">Vælg den tabel, du vil oprette forbindelse til, og vælg derefter **Opret forbindelse**.</span><span class="sxs-lookup"><span data-stu-id="48d10-117">Select the table that you want to connect to, and then choose **Connect**.</span></span>

<span data-ttu-id="48d10-118">Disse såkaldte tabeller eksponeres som slutpunkter af [!INCLUDE[prod_short](includes/prod_short.md)]-connectoren til Power Apps.</span><span class="sxs-lookup"><span data-stu-id="48d10-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prod_short](includes/prod_short.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="48d10-119">Hvis du vil medtage data fra andre tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] i din app, skal du samarbejde med en udvikler om at definere en brugerdefineret API i [!INCLUDE[prod_short](includes/prod_short.md)] og derefter bruge denne API via en brugerdefineret connector i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="48d10-119">If you want to include data from other tables in [!INCLUDE[prod_short](includes/prod_short.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prod_short](includes/prod_short.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="48d10-120">Du kan finde flere oplysninger i [Oprette en brugerdefineret connector fra bunden](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="48d10-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="48d10-121">Nu har du oprettet forbindelse til dine [!INCLUDE[prod_short](includes/prod_short.md)]-data og er klar til at opbygge din PowerApp.</span><span class="sxs-lookup"><span data-stu-id="48d10-121">At this point, you have successfully connected to your [!INCLUDE[prod_short](includes/prod_short.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="48d10-122">Du kan tilføje yderligere skærmbilleder og oprette forbindelse til flere data fra dit [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="48d10-122">You can add additional screens and connect to additional data from your [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="48d10-123">Du kan finde flere oplysninger under [Oprette en lærreds-app ud fra et eksempel i Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="48d10-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="48d10-124">Når du har designet og opbygget din app, kan du dele den med dine kolleger.</span><span class="sxs-lookup"><span data-stu-id="48d10-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="48d10-125">Du kan finde flere oplysninger i [Gemme og udgive en lærreds-app i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="48d10-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="48d10-126">Hvis du vil oprette forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø, skal du vælge **Business Central til det lokale miljø**-connectoren i trin 3.</span><span class="sxs-lookup"><span data-stu-id="48d10-126">If you want to connect to [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="48d10-127">Se også</span><span class="sxs-lookup"><span data-stu-id="48d10-127">See Also</span></span>

[<span data-ttu-id="48d10-128">Oprette en lærreds-app fra en skabelon i Power Apps</span><span class="sxs-lookup"><span data-stu-id="48d10-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="48d10-129">Importer virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="48d10-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="48d10-130">[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="48d10-130">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="48d10-131">Introduktion til udvikling af Connect-apps til Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="48d10-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]