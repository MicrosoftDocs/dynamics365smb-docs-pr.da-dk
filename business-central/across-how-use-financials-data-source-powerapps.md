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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 718d4378a897b187ba3073449869184fef5cec98
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924824"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="e7153-103">Oprette forbindelse til dine Business Central-data for at oprette en forretningsapp ved hjælp af Power Apps</span><span class="sxs-lookup"><span data-stu-id="e7153-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="e7153-104">Du kan gøre dine [!INCLUDE[prodshort](includes/prodshort.md)]-data tilgængelige som en datakilde i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e7153-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="e7153-105">Du skal have en gyldig konto til [!INCLUDE[prodshort](includes/prodshort.md)] og til Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e7153-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a><span data-ttu-id="e7153-106">Sådan tilføjes [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power Apps</span><span class="sxs-lookup"><span data-stu-id="e7153-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="e7153-107">Gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/) i din webbrowser, og log på.</span><span class="sxs-lookup"><span data-stu-id="e7153-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="e7153-108">Vælg feltet **Andre datakilder** på startsiden i afsnittet **Start fra data**.</span><span class="sxs-lookup"><span data-stu-id="e7153-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="e7153-109">Dette åbner Power Apps Studio.</span><span class="sxs-lookup"><span data-stu-id="e7153-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="e7153-110">Når du logger på første gang, skal du angive land/område.</span><span class="sxs-lookup"><span data-stu-id="e7153-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="e7153-111">Vælg **Business Central**på listen over tilgængelige forbindelser, og vælg derefter knappen **Opret**.</span><span class="sxs-lookup"><span data-stu-id="e7153-111">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="e7153-112">Power Apps opretter forbindelse til din [!INCLUDE[prodshort](includes/prodshort.md)] ved hjælp af de legitimationsoplysninger, du er logget på med.</span><span class="sxs-lookup"><span data-stu-id="e7153-112">Power Apps will connect to your [!INCLUDE[prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="e7153-113">Hvis du ikke er administrator af din [!INCLUDE[prodshort](includes/prodshort.md)], skal du muligvis logge på med en anden konto.</span><span class="sxs-lookup"><span data-stu-id="e7153-113">If you are not an administrator of your [!INCLUDE[prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="e7153-114">Power Apps viser en liste over *Miljøer og regnskaber*, der er tilgængelige fra [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="e7153-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="e7153-115">Vælg det miljø og den virksomhed, der indeholder de data, du vil oprette forbindelse til, f.eks. *PRODUKTION - Min virksomhed*.</span><span class="sxs-lookup"><span data-stu-id="e7153-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company*.</span></span>  

5. <span data-ttu-id="e7153-116">Derefter vises en liste over de tabeller, der eksponeres som en del af API'en for dit miljø.</span><span class="sxs-lookup"><span data-stu-id="e7153-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="e7153-117">Vælg den tabel, du vil oprette forbindelse til, og vælg derefter **Opret forbindelse**.</span><span class="sxs-lookup"><span data-stu-id="e7153-117">Select the table that you want to connect to, and then choose **Connect**.</span></span>

<span data-ttu-id="e7153-118">Disse såkaldte tabeller eksponeres som slutpunkter af [!INCLUDE[prodshort](includes/prodshort.md)]-connectoren til Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e7153-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prodshort](includes/prodshort.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="e7153-119">Hvis du vil medtage data fra andre tabeller i [!INCLUDE[prodshort](includes/prodshort.md)] i din app, skal du samarbejde med en udvikler om at definere en brugerdefineret API i [!INCLUDE[prodshort](includes/prodshort.md)] og derefter bruge denne API via en brugerdefineret connector i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e7153-119">If you want to include data from other tables in [!INCLUDE[prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="e7153-120">Du kan finde flere oplysninger i [Oprette en brugerdefineret connector fra bunden](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="e7153-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="e7153-121">Nu har du oprettet forbindelse til dine [!INCLUDE[prodshort](includes/prodshort.md)]-data og er klar til at opbygge din PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e7153-121">At this point, you have successfully connected to your [!INCLUDE[prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="e7153-122">Du kan tilføje yderligere skærmbilleder og oprette forbindelse til flere data fra dit [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="e7153-122">You can add additional screens and connect to additional data from your [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="e7153-123">Du kan finde flere oplysninger under [Oprette en lærreds-app ud fra et eksempel i Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="e7153-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="e7153-124">Når du har designet og opbygget din app, kan du dele den med dine kolleger.</span><span class="sxs-lookup"><span data-stu-id="e7153-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="e7153-125">Du kan finde flere oplysninger i [Gemme og udgive en lærreds-app i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="e7153-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="e7153-126">Hvis du vil oprette forbindelse til [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø, skal du vælge **Business Central til det lokale miljø**-connectoren i trin 3.</span><span class="sxs-lookup"><span data-stu-id="e7153-126">If you want to connect to [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e7153-127">Se også</span><span class="sxs-lookup"><span data-stu-id="e7153-127">See Also</span></span>

[<span data-ttu-id="e7153-128">Oprette en lærreds-app fra en skabelon i Power Apps</span><span class="sxs-lookup"><span data-stu-id="e7153-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="e7153-129">Importer virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="e7153-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="e7153-130">[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="e7153-130">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="e7153-131">Introduktion til udvikling af Connect-apps til Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="e7153-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
