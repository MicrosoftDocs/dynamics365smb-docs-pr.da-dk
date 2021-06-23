---
title: Opret et sandkassemiljø
description: Oprette et miljø til udforskning, læring, demonstration, udvikling og test fra Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: a76ae33815b8e9368f45b72fd8703bfc47cbd079
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215624"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a><span data-ttu-id="27571-103">Opret et sandkassemiljø i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="27571-103">Creating a Sandbox Environment in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

<span data-ttu-id="27571-104">Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du nemt oprette et sikkert miljø, hvor du kan teste, træne eller foretage fejlfinding uden at forstyrre virksomhedens arbejdsprocesser eller forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="27571-104">With [!INCLUDE[prod_short](includes/prod_short.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="27571-105">Et sådant ikke-produktionsmiljø kaldes en *sandkasse*.</span><span class="sxs-lookup"><span data-stu-id="27571-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="27571-106">Isoleret fra produktion er et sandkassemiljø stedet, hvor du sikkert kan udforske, lære, demonstrere, udvikle og teste tjenesten uden risiko for at påvirke data og indstillinger i dit produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="27571-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="27571-107">Administratoren kan administrere sandkassemiljøer i [Administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), men hvis du hurtigt vil teste noget, kan du oprette et sandkasse-miljø fra [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="27571-107">Your administrator manages sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="27571-108">Når du er færdig, kan du fjerne sandkassen via Administrationscenter.</span><span class="sxs-lookup"><span data-stu-id="27571-108">Once you're done, you can remove the sandbox, using the administration center.</span></span>  

> [!NOTE]
> <span data-ttu-id="27571-109">Teknisk set er sandkassemiljøer meget forskellige fra produktionsmiljøer, selvom administratoren opretter en sandkasse, som inkluderer produktionsdata.</span><span class="sxs-lookup"><span data-stu-id="27571-109">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="27571-110">Du kan ikke bruge en sandkasse til benchmarking, og du kan f.eks. ikke anmode om at eksportere databaser.</span><span class="sxs-lookup"><span data-stu-id="27571-110">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="27571-111">Hvis du vil oprette en sandkasse til benchmarking, kan administratoren oprette et dedikeret miljø i Administrationscenter.</span><span class="sxs-lookup"><span data-stu-id="27571-111">If you want to create a sandbox for benchmarking, your administrator can create a dedicated environment in the administration center.</span></span> <span data-ttu-id="27571-112">Du kan finde flere oplysninger i afsnittet [produktion og sandkassemiljøer](/dynamics365/business-central/dev-itpro/administration/environment-types).</span><span class="sxs-lookup"><span data-stu-id="27571-112">For more information, see [Production and Sandbox Environments](/dynamics365/business-central/dev-itpro/administration/environment-types).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a><span data-ttu-id="27571-113">Sådan opretter du et sandkassemiljø i din [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="27571-113">To create a sandbox environment in your [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

1. <span data-ttu-id="27571-114">Log ind på din produktionsforekomst af [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="27571-114">Sign in to your production instance of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

2. <span data-ttu-id="27571-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sandkassemiljø**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="27571-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="27571-116">Vælg knappen **Opret**.</span><span class="sxs-lookup"><span data-stu-id="27571-116">Choose the **Create** button.</span></span>  

    <span data-ttu-id="27571-117">Der vises endnu en fane i [!INCLUDE[prod_short](includes/prod_short.md)], hvor du kan afslutte opsætningen af dit sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="27571-117">Another tab with [!INCLUDE[prod_short](includes/prod_short.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="27571-118">Hvis blokering af pop op-vinduer er aktiveret i din webbrowser, kan du ændre denne indstilling, så URL-adresser fra \*.businesscentral.dynamics.com-adressen tillades.</span><span class="sxs-lookup"><span data-stu-id="27571-118">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="27571-119">Når sandkassemiljøet er klar, omdirigeres du til miljøet velkomstguide.</span><span class="sxs-lookup"><span data-stu-id="27571-119">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="27571-120">Du kan vælge knappen **Få mere at vide** for at læse om udviklerscenarier, som du kan afprøve i et sandkassemiljø, eller vælg knappen **Luk** for at fortsætte til rollecenteret i din sandkasseforekomst af [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="27571-120">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[prod_short](includes/prod_short.md)] sandbox instance.</span></span>

<span data-ttu-id="27571-121">Der vises en meddelelse om, at dette er et sandkassemiljø, øverst i rollecenteret.</span><span class="sxs-lookup"><span data-stu-id="27571-121">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="27571-122">Du kan også se miljøtypen i titellinjen i klienten.</span><span class="sxs-lookup"><span data-stu-id="27571-122">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="27571-123">Et sandkassemiljø, der oprettes på denne måde, indeholder kun standarddemonstrationsdataene for CRONUS-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="27571-123">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="27571-124">Der kopieres ikke eller på anden måde overføres data fra produktionsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="27571-124">No data is copied or otherwise transferred from the production environment.</span></span>
>
> <span data-ttu-id="27571-125">Du kan også oprette et Sandbox-miljø baseret på produktionsdata.</span><span class="sxs-lookup"><span data-stu-id="27571-125">Alternatively, create a sandbox environment based on production data.</span></span> <span data-ttu-id="27571-126">Dette skal gøres via Administrationscenter.</span><span class="sxs-lookup"><span data-stu-id="27571-126">You must do this through the administration center.</span></span> <span data-ttu-id="27571-127">Du kan finde flere oplysninger i [Administrere miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) i hjælpen til udviklere og administratorer.</span><span class="sxs-lookup"><span data-stu-id="27571-127">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the developer and administration content.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="27571-128">En administrator kan begrænse eller endda blokere adgangen for bestemte brugere til sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="27571-128">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="27571-129">Dette kan gøres ved hjælp af standardsikkerhedsfunktionerne i produktet, f.eks. brugerkort, brugergrupper og rettighedssæt.</span><span class="sxs-lookup"><span data-stu-id="27571-129">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="27571-130">Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="27571-130">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="27571-131">Avancerede funktioner i sandkassemiljøet</span><span class="sxs-lookup"><span data-stu-id="27571-131">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="27571-132">Sandkassemiljøet er ikke mindst anvendelig, fordi det indeholder et par praktiske funktioner:</span><span class="sxs-lookup"><span data-stu-id="27571-132">The sandbox environment is not least useful because it includes a couple of handy features:</span></span>

* [<span data-ttu-id="27571-133">Udvidet brugeroplevelse</span><span class="sxs-lookup"><span data-stu-id="27571-133">Advanced user experience</span></span>](#advanced-user-experience)  
* [<span data-ttu-id="27571-134">Komplette eksempeldata</span><span class="sxs-lookup"><span data-stu-id="27571-134">Complete sample data</span></span>](#complete-sample-data)  
* [<span data-ttu-id="27571-135">Designer</span><span class="sxs-lookup"><span data-stu-id="27571-135">Designer</span></span>](#designer)  

### <a name="advanced-user-experience"></a><span data-ttu-id="27571-136">Udvidet brugeroplevelse</span><span class="sxs-lookup"><span data-stu-id="27571-136">Advanced user experience</span></span>

<span data-ttu-id="27571-137">Du kan aktivere og prøve den fulde funktionalitet af standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] i en sandkasselejer ved at indstille feltet **Oplevelse** på siden **Virksomhedsoplysninger** til *Premium*.</span><span class="sxs-lookup"><span data-stu-id="27571-137">It is possible to enable and try the full functionality of the standard version of [!INCLUDE[prod_short](includes/prod_short.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page to *Premium*.</span></span> Find siden **Virksomhedsoplysninger** i menuen :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Indstillinger":::.  

<span data-ttu-id="27571-139">Når du har aktiveret *Premium*-brugeroplevelsen, får du adgang til alle standardprofilerne (rollerne) og rollecentre i standardversionen.</span><span class="sxs-lookup"><span data-stu-id="27571-139">After you have enabled the *Premium* user experience, you get access to all the standard profiles (roles) and Role Centers in the standard version.</span></span> <span data-ttu-id="27571-140">Du kan også oprette en evalueringsvirksomhed, der er fuldt defineret, herunder med demodata og adgang til avancerede områder af produktet.</span><span class="sxs-lookup"><span data-stu-id="27571-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span> <span data-ttu-id="27571-141">Alternativt kan du kontakte en videresalgspartner for at demonstrere mulighederne.</span><span class="sxs-lookup"><span data-stu-id="27571-141">Alternatively, contact a reselling partner for a demonstration of the capabilities.</span></span> <span data-ttu-id="27571-142">Du kan finde flere oplysninger i [Hvordan finder jeg en videresalgspartner?](/dynamics365/business-central/across-faq.yml#findpartner).</span><span class="sxs-lookup"><span data-stu-id="27571-142">For more information, see [How do I find a reselling partner?](/dynamics365/business-central/across-faq.yml#findpartner).</span></span>  

### <a name="complete-sample-data"></a><span data-ttu-id="27571-143">Komplette eksempeldata</span><span class="sxs-lookup"><span data-stu-id="27571-143">Complete sample data</span></span>

<span data-ttu-id="27571-144">I de situationer, hvor du har brug for yderligere eksempeldata, skal du kontakte din forhandlerpartner.</span><span class="sxs-lookup"><span data-stu-id="27571-144">For situations where you need additional sample data, please talk to your reselling partner.</span></span>
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a><span data-ttu-id="27571-145">Sådan opretter du en virksomhed med komplette eksempeldata i en sandkasse</span><span class="sxs-lookup"><span data-stu-id="27571-145">To create a company with complete sample data in a sandbox</span></span>

1. <span data-ttu-id="27571-146">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomheder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="27571-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="27571-147">Vælg handlingen **Ny**, og vælg derefter **Opret ny virksomhed**.</span><span class="sxs-lookup"><span data-stu-id="27571-147">Choose the **New** action, and then choose **Create New Company**.</span></span>  
3. <span data-ttu-id="27571-148">Vælg **Næste** på siden **Assisteret opsætning af en virksomhed**.</span><span class="sxs-lookup"><span data-stu-id="27571-148">In the **Assisted Setup for Creating a Company** page, choose **Next**.</span></span>  
4. <span data-ttu-id="27571-149">Angiv et navn til den nye virksomhed, og vælg **Avanceret evaluering - komplette eksempeldata** i feltet **Vælg data og konfiguration for at komme i gang**.</span><span class="sxs-lookup"><span data-stu-id="27571-149">Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.</span></span>  
5. <span data-ttu-id="27571-150">Udfør trinnene i resten af guiden til assisteret opsætning.</span><span class="sxs-lookup"><span data-stu-id="27571-150">Complete the rest of the assisted setup guide.</span></span>  

<span data-ttu-id="27571-151">Når den assisterede opsætningsguide afsluttes, kan du begynde at udforske den nye virksomhed med de komplette eksempeldata.</span><span class="sxs-lookup"><span data-stu-id="27571-151">When the assisted setup guide completes, you can start exploring the new company with the complete sample data.</span></span> <span data-ttu-id="27571-152">Du kan finde flere oplysninger om oprettelse af pluk under [Oprettelse af nye virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="27571-152">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>  

### <a name="designer"></a><span data-ttu-id="27571-153">Designer</span><span class="sxs-lookup"><span data-stu-id="27571-153">Designer</span></span>

<span data-ttu-id="27571-154">I et sandkassemiljø er **Designer** aktiveret.</span><span class="sxs-lookup"><span data-stu-id="27571-154">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="27571-155">Du kan aktivere Designer ved at vælge designikon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side eller ved at vælge menupunktet **Design** i menuen ![Indstillinger](media/ui-experience/settings_icon_small.png).</span><span class="sxs-lookup"><span data-stu-id="27571-155">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>  

<span data-ttu-id="27571-156">Du kan finde flere oplysninger i [bruge designer ](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer)i Developer and admin Content (kun på engelsk).</span><span class="sxs-lookup"><span data-stu-id="27571-156">For more information, see [Using Designer](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) in the developer and admin content (in English only).</span></span>  

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a><span data-ttu-id="27571-157">Se også</span><span class="sxs-lookup"><span data-stu-id="27571-157">See Also</span></span>

<span data-ttu-id="27571-158">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="27571-158">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="27571-159">[[!INCLUDE[prod_long](includes/prod_long.md)] Prøveversioner og abonnementer](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="27571-159">[[!INCLUDE[prod_long](includes/prod_long.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="27571-160">Sådan styrer du Miljøer i Business Central Administration</span><span class="sxs-lookup"><span data-stu-id="27571-160">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
