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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305015"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a><span data-ttu-id="4a1b3-103">Oprette forbindelse til dine Business Central-data for at oprette en forretningsapp ved hjælp af PowerApps</span><span class="sxs-lookup"><span data-stu-id="4a1b3-103">Connecting to Your Business Central Data to Build a Business App Using PowerApps</span></span>
<span data-ttu-id="4a1b3-104">Du kan gøre dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tilgængelige som en datakilde i PowerApps.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-104">You can make your [!INCLUDE[d365fin](includes/d365fin_md.md)] data available as a data source in PowerApps.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="4a1b3-105">Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til PowerApps.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with PowerApps.</span></span>  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a><span data-ttu-id="4a1b3-106">Sådan tilføjes [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i PowerApps</span><span class="sxs-lookup"><span data-stu-id="4a1b3-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in PowerApps</span></span>
1. <span data-ttu-id="4a1b3-107">Gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) i din webbrowser, og log på.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="4a1b3-108">Vælg **Apps** på startsiden, **Opret en app** og **Lærred** for at oprette en ny lærreds-app.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="4a1b3-109">Denne app vil blive udformet til brug på en mobilenhed, men du kan også vælge at bruge en anden skabelon.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="4a1b3-110">Næste trin til oprettelse af en PowerApp er at vælge dataene.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-110">The next step to create a PowerApp is to select your data.</span></span> <span data-ttu-id="4a1b3-111">Vælg ikonet med pilen, og vælg derefter indstillingen **Ny forbindelse** øverst til venstre side på siden.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="4a1b3-112">Vælg **Business Central**på listen over tilgængelige forbindelser, og vælg derefter knappen **Opret**.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="4a1b3-113">PowerApps opretter forbindelse til din [!INCLUDE [prodshort](includes/prodshort.md)] ved hjælp af de legitimationsoplysninger, du er logget på med.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-113">PowerApps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="4a1b3-114">Hvis du ikke er administrator af din [!INCLUDE [prodshort](includes/prodshort.md)], skal du muligvis logge på med en anden konto.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4.  <span data-ttu-id="4a1b3-115">PowerApps viser en liste over *Miljøer og regnskaber*, der er tilgængelige fra [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="4a1b3-115">PowerApps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="4a1b3-116">Vælg det miljø og regnskab, der indeholder de data, du vil oprette forbindelse til.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="4a1b3-117">Derefter vises en liste over API'er.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="4a1b3-118">Vælg den **API**, du vil oprette forbindelse til.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="4a1b3-119">Disse såkaldte tabeller er en del af [!INCLUDE [prodshort](includes/prodshort.md)] API'en.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="4a1b3-120">Du behøver ikke selv at konfigurere slutpunkterne – [!INCLUDE [prodshort](includes/prodshort.md)]-connectoren til PowerApps gør det for dig.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for PowerApps does it for you.</span></span>  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

<span data-ttu-id="4a1b3-121">Nu har du oprettet forbindelse til dine [!INCLUDE [prodshort](includes/prodshort.md)]-data og er klar til at opbygge din PowerApp.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-121">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="4a1b3-122">Du kan tilføje yderligere skærmbilleder og oprette forbindelse til flere data fra dit [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="4a1b3-122">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="4a1b3-123">Du kan finde flere oplysninger i [Oprette en lærreds-app fra en skabelon i PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="4a1b3-123">For more information, see [Create a canvas app from a template in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="4a1b3-124">Når du har designet og opbygget din app, kan du dele den med dine kolleger.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="4a1b3-125">Du kan finde flere oplysninger i [Gemme og udgive en lærreds-app i PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="4a1b3-125">For more information, see [Save and publish a canvas app in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="4a1b3-126">Hvis du vil oprette forbindelse til [!INCLUDE [prodshort](includes/prodshort.md)] i det lokale miljø, skal du vælge **Business Central til det lokale miljø**-connectoren i trin 3.</span><span class="sxs-lookup"><span data-stu-id="4a1b3-126">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4a1b3-127">Se også</span><span class="sxs-lookup"><span data-stu-id="4a1b3-127">See Also</span></span>

[<span data-ttu-id="4a1b3-128">Oprette en lærreds-app fra en skabelon i PowerApps</span><span class="sxs-lookup"><span data-stu-id="4a1b3-128">Create a canvas app from a template in PowerApps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="4a1b3-129">Introduktion</span><span class="sxs-lookup"><span data-stu-id="4a1b3-129">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="4a1b3-130">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="4a1b3-130">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="4a1b3-131">[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="4a1b3-131">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="4a1b3-132">Finans</span><span class="sxs-lookup"><span data-stu-id="4a1b3-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="4a1b3-133">Introduktion til udvikling af Connect-apps til Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="4a1b3-133">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
