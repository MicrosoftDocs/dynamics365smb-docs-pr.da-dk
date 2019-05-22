---
title: Oprette et sandkassemiljø | Microsoft Docs
description: Oprette et miljø til udforskning, læring, demonstration, udvikling og test.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 113c081e60b825c48cfb85ae3475a713a1a1e215
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241656"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a><span data-ttu-id="520ca-103">Oprette et sandkassemiljø</span><span class="sxs-lookup"><span data-stu-id="520ca-103">Creating a Sandbox Environment</span></span>
<span data-ttu-id="520ca-104">Et sandkassemiljø (eksempelvisning) er en ikke-produktiv forekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="520ca-104">A sandbox environment (Preview) is a non-production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="520ca-105">Isoleret fra produktion er et sandkassemiljø stedet, hvor du sikkert kan udforske, lære, demonstrere, udvikle og teste tjenesten uden risiko for at påvirke data og indstillinger i dit produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="520ca-105">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>

## <a name="to-create-a-sandbox-environment"></a><span data-ttu-id="520ca-106">Sådan opretter du et sandkassemiljø</span><span class="sxs-lookup"><span data-stu-id="520ca-106">To create a sandbox environment</span></span>
<span data-ttu-id="520ca-107">Du skal have abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)] for at kunne oprette et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="520ca-107">You must have a subscription to [!INCLUDE[d365fin](includes/d365fin_md.md)] to be able to create a sandbox environment.</span></span> <span data-ttu-id="520ca-108">Der kan kun være ét sandkassemiljø pr. abonnement.</span><span class="sxs-lookup"><span data-stu-id="520ca-108">There can only be one sandbox environment per subscription.</span></span>

1. <span data-ttu-id="520ca-109">Log ind på din produktionsforekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)]-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="520ca-109">Sign in to your production instance of the [!INCLUDE[d365fin](includes/d365fin_md.md)] service.</span></span>
2. <span data-ttu-id="520ca-110">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sandkassemiljø**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="520ca-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="520ca-111">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="520ca-111">Select **Create**.</span></span>  
  <span data-ttu-id="520ca-112">Der åbnes en anden fane i din webbrowser, hvor du kan afslutte opsætningen af sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="520ca-112">Another tab in your browser will open for finishing the setup of your sandbox environment.</span></span>
> [!NOTE]  
>  <span data-ttu-id="520ca-113">Hvis blokering af pop op-vinduer er aktiveret i din webbrowser, kan du ændre denne indstilling, så URL-adresser fra \*.businesscentral.dynamics.com-adressen tillades.</span><span class="sxs-lookup"><span data-stu-id="520ca-113">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>   

4. <span data-ttu-id="520ca-114">Når sandkassemiljøet er klar, omdirigeres du til miljøet velkomstguide.</span><span class="sxs-lookup"><span data-stu-id="520ca-114">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. <span data-ttu-id="520ca-115">Vælg **Lær mere** for at læse om scenarier, som du kan prøve i et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="520ca-115">Choose **Learn more** to read about scenarios that you can try in a sandbox environment.</span></span> <span data-ttu-id="520ca-116">Eller du kan vælge **Luk** for at fortsætte til rollecenteret for din [!INCLUDE[d365fin](includes/d365fin_md.md)]-sandkasseforekomst.</span><span class="sxs-lookup"><span data-stu-id="520ca-116">Or, choose **Close** to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>
6. <span data-ttu-id="520ca-117">Der vises en meddelelse om, at dette er et sandkassemiljø, øverst i rollecenteret.</span><span class="sxs-lookup"><span data-stu-id="520ca-117">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="520ca-118">Du kan også se miljøtypen i titellinjen i klienten.</span><span class="sxs-lookup"><span data-stu-id="520ca-118">You can also see the type of the environment in the title bar of the client.</span></span>
<!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) --> <span data-ttu-id="520ca-119">I sandkassemiljøet er der blevet oprettet en ny lejer.</span><span class="sxs-lookup"><span data-stu-id="520ca-119">In the sandbox environment, a new tenant has been created.</span></span> <span data-ttu-id="520ca-120">Denne lejer er indlæst med standarddemodata for virksomheden CRONUS.</span><span class="sxs-lookup"><span data-stu-id="520ca-120">This tenant is loaded with default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="520ca-121">Ingen data kopieres eller på anden måde overføres fra produktionsmiljøet under oprettelsen af sandkassen.</span><span class="sxs-lookup"><span data-stu-id="520ca-121">No data is copied or otherwise transferred from the production environment during the sandbox creation.</span></span>

7. <span data-ttu-id="520ca-122">Du kan når som helst vende tilbage til siden **Sandkassemiljø** og nulstille sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="520ca-122">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>
> [!NOTE]  
>  <span data-ttu-id="520ca-123">Nulstilling af sandkassemiljøet vil fjerne miljøet helt, og derefter oprettes det igen med standarddemodata.</span><span class="sxs-lookup"><span data-stu-id="520ca-123">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

8. <span data-ttu-id="520ca-124">Hvis du vil skifte mellem produktions- og sandkassemiljøerne, kan du bruge Business Central-appstarter.</span><span class="sxs-lookup"><span data-stu-id="520ca-124">To switch between your production and sandbox environments, you can use the Business Central app launcher.</span></span>
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

9. <span data-ttu-id="520ca-125">Det er muligt for en administrator eller en anden bruger at begrænse eller endda blokere adgangen for bestemte brugere til sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="520ca-125">It is possible for an administrator or another user to limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="520ca-126">Dette kan gøres ved hjælp af standardsikkerhedsfunktionerne i produktet, f.eks. brugerkort, brugergrupper og rettighedssæt.</span><span class="sxs-lookup"><span data-stu-id="520ca-126">This can be done by using the standard security features of the product, such as the User card, User Groups, and Permission Sets.</span></span>

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="520ca-127">Avancerede funktioner i sandkassemiljøet</span><span class="sxs-lookup"><span data-stu-id="520ca-127">Advanced functionality in the sandbox environment</span></span>
### <a name="designer"></a><span data-ttu-id="520ca-128">Designer</span><span class="sxs-lookup"><span data-stu-id="520ca-128">Designer</span></span>
<span data-ttu-id="520ca-129">I et sandkassemiljø er **Designer** aktiveret. Du kan aktivere funktionen ved at vælge designikonet ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side.</span><span class="sxs-lookup"><span data-stu-id="520ca-129">In a sandbox environment, you will find the **Designer** enabled, which you can activate by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="enable-the-advanced-user-experience"></a><span data-ttu-id="520ca-130">Aktivere den avancerede brugeroplevelse</span><span class="sxs-lookup"><span data-stu-id="520ca-130">Enable the advanced user experience</span></span>
<span data-ttu-id="520ca-131">Du kan aktivere og prøve alle de avancerede funktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] i en sandkasselejer ved at indstille feltet **Oplevelse** på siden **Virksomhedsoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="520ca-131">It is possible to enable and try the advanced (full) functionality of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="520ca-132">Når du har aktiveret de avancerede funktioner i en sandkasselejer, kan du få adgang til alle standardprofiler og rollecentre.</span><span class="sxs-lookup"><span data-stu-id="520ca-132">After you’ve enabled the advanced functionality in a sandbox tenant, you get access to all the standard Profiles and Role Centers.</span></span> <span data-ttu-id="520ca-133">Du kan også oprette en evalueringsvirksomhed, der er fuldt defineret, herunder med demodata og adgang til avancerede områder af produktet.</span><span class="sxs-lookup"><span data-stu-id="520ca-133">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span>

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a><span data-ttu-id="520ca-134">Se også</span><span class="sxs-lookup"><span data-stu-id="520ca-134">See Also</span></span>
<span data-ttu-id="520ca-135">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="520ca-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
