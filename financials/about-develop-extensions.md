---
title: Tilpasse Dynamics 365 for Financials | Microsoft Docs
description: "Oprette, vise og gøre reklame for dine apps og udvidelser til Dynamics 365 for Financials."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: c50aeb38a13569316f3208c27e5e8dc3d7b6d771
ms.openlocfilehash: fdb60d82c7e8d2215c59d2c087105f42fe37eb84
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="extending-included365finlongincludesd365finlongmdmd"></a><span data-ttu-id="ae011-103">Udvidelse af [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae011-103">Extending [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="ae011-104">Der er mange fordele ved at bruge [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] som platform for appudviklere:</span><span class="sxs-lookup"><span data-stu-id="ae011-104">There are plenty of benefits of using [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] as a platform for App builders:</span></span>

* <span data-ttu-id="ae011-105">Gør [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], en gennemprøvet Microsoft-onlineløsning, endnu bedre med din viden</span><span class="sxs-lookup"><span data-stu-id="ae011-105">Enrich [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], a proven Microsoft online solution, with your expertise</span></span>  
* <span data-ttu-id="ae011-106">Udnyt Dynamics 365-mærket – et mærke, som millioner af brugere kender og har tillid til</span><span class="sxs-lookup"><span data-stu-id="ae011-106">Leverage the Dynamics 365 brand – a brand that millions of users know and trust</span></span>  
* <span data-ttu-id="ae011-107">Nå flere kunder til dine virksomhedsapps med [Microsoft AppSource](https://appsource.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="ae011-107">Reach more customers for your business apps with [Microsoft AppSource](https://appsource.microsoft.com/)</span></span>  
* <span data-ttu-id="ae011-108">Opnå mere ved hjælp af en platform, som giver en moderne oplevelse og skalerbarhed</span><span class="sxs-lookup"><span data-stu-id="ae011-108">Achieve more with a platform that delivers a modern experience and offers scale</span></span>  
* <span data-ttu-id="ae011-109">Bundt med intelligente business-apps som PowerApps, Flow, Power BI, Cortana Intelligence og mange andre</span><span class="sxs-lookup"><span data-stu-id="ae011-109">Bundle with intelligent business apps such as PowerApps, Flow, Power BI, Cortana Intelligence, and many more</span></span>  

## <a name="to-bring-your-included365finincludesd365finmdmd-app-into-appsource"></a><span data-ttu-id="ae011-110">Sådan indlæser du din [!INCLUDE[d365fin](includes/d365fin_md.md)]-app i AppSource:</span><span class="sxs-lookup"><span data-stu-id="ae011-110">To bring your [!INCLUDE[d365fin](includes/d365fin_md.md)] app into AppSource:</span></span>
+ <span data-ttu-id="ae011-111">Opret dine konti</span><span class="sxs-lookup"><span data-stu-id="ae011-111">Create your accounts</span></span>  
<span data-ttu-id="ae011-112">Vi vil gerne give dig adgang til alle de nødvendige værktøjer.</span><span class="sxs-lookup"><span data-stu-id="ae011-112">We want you to have access to all the necessary tools!</span></span> <span data-ttu-id="ae011-113">Du skal have et Microsoft-Partner Network-id, en udviklerkonto og en PSBC-konto.</span><span class="sxs-lookup"><span data-stu-id="ae011-113">You must have a Microsoft Partner Network ID, a Developer account, and a PSBC account.</span></span>
<span data-ttu-id="ae011-114">Du kan finde flere oplysninger om, hvordan du kan få dine konti på plads, i dokumentet [Oprette dine konti.pdf](https://go.microsoft.com/fwlink/?linkid=841514) fra Download Center.</span><span class="sxs-lookup"><span data-stu-id="ae011-114">For more information about how you can get your accounts in place, get the [Create your accounts.pdf](https://go.microsoft.com/fwlink/?linkid=841514) document from the Download Center.</span></span>

+ <span data-ttu-id="ae011-115">Tal med os om din app ide</span><span class="sxs-lookup"><span data-stu-id="ae011-115">Engage with us about your app idea</span></span>  
<span data-ttu-id="ae011-116">Del din [!INCLUDE[d365fin](includes/d365fin_md.md)]-appide med os på Microsoft AppSource!</span><span class="sxs-lookup"><span data-stu-id="ae011-116">Share your [!INCLUDE[d365fin](includes/d365fin_md.md)] app idea with us on Microsoft AppSource!</span></span> <span data-ttu-id="ae011-117">Når du har sendt din ide, tager vi kontakt til dig og giver dig alt det, du behøver for at begynde at arbejde på din app.</span><span class="sxs-lookup"><span data-stu-id="ae011-117">After submitting your idea, we will engage with you and provide you with everything you need to start working on your app.</span></span>
<span data-ttu-id="ae011-118">Du kan finde flere oplysninger om alle trin i dokumentet [Tal med os om din appide.pdf](https://go.microsoft.com/fwlink/?linkid=841515) fra Download Center.</span><span class="sxs-lookup"><span data-stu-id="ae011-118">For more information about all the steps, get the [Engage with us about your app idea document.pdf](https://go.microsoft.com/fwlink/?linkid=841515) document from the Download Center.</span></span>

+ <span data-ttu-id="ae011-119">Udvikl de tekniske aspekter af din app</span><span class="sxs-lookup"><span data-stu-id="ae011-119">Develop the technical aspects of your app</span></span>    
<span data-ttu-id="ae011-120">Når du har oprettet dit eget miljø til udvikling af apps, kan du udvikle din app.</span><span class="sxs-lookup"><span data-stu-id="ae011-120">After you have set up your own app development environment, you can develop your app.</span></span>
<span data-ttu-id="ae011-121">Du kan finde flere oplysninger i forbindelse med udvikling af de tekniske aspekter af din [!INCLUDE[d365fin](includes/d365fin_md.md)] app i dokumentet [Udvikle tekniske aspekter af din app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) fra Download Center.</span><span class="sxs-lookup"><span data-stu-id="ae011-121">For more information about everything you need to know about how to develop the technical aspects of your [!INCLUDE[d365fin](includes/d365fin_md.md)] app, get the [Develop the technical aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) document from the Download Center.</span></span>

+ <span data-ttu-id="ae011-122">Udvikl marketingaspekterne af din app</span><span class="sxs-lookup"><span data-stu-id="ae011-122">Develop the marketing aspects of your app</span></span>  
<span data-ttu-id="ae011-123">Blot at vise dine apps funktioner og funktionalitet konverterer ikke kundeemner til kunder.</span><span class="sxs-lookup"><span data-stu-id="ae011-123">Simply listing your app's features and functionality will not convert prospects to buyers.</span></span> <span data-ttu-id="ae011-124">Du kan finde flere oplysninger om, hvordan du bedst markedsfører din app på AppSource-markedspladsen, ved at hente dokumentet [Udvikle marketingaspekterne af din app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) fra Download Center.</span><span class="sxs-lookup"><span data-stu-id="ae011-124">For more information about how to best market your app in the AppSource marketplace, get the [Develop the marketing aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) from the Download Center.</span></span>

+ <span data-ttu-id="ae011-125">Publicere din app</span><span class="sxs-lookup"><span data-stu-id="ae011-125">Publish your app</span></span>  
<span data-ttu-id="ae011-126">Før vi publicerer appen, vil vi sammen med dig sikre, at din app er iøjnefaldende på Microsoft AppSource og din landingsside.</span><span class="sxs-lookup"><span data-stu-id="ae011-126">Before we publish, we will collaborate with you to ensure that your app stands out on Microsoft AppSource and on your own landing page!</span></span> <span data-ttu-id="ae011-127">Vi skal validere din app for at sikre, at den er markedsført hensigtsmæssigt, er pålidelig og opdateret.</span><span class="sxs-lookup"><span data-stu-id="ae011-127">We need to validate your app to ensure it is marketed well, trustworthy, and up to date.</span></span>
<span data-ttu-id="ae011-128">Du kan finde flere oplysninger om valideringen, og hvordan du publicerer din app, ved at hente dokumentet [Publicere din app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) fra Download Center.</span><span class="sxs-lookup"><span data-stu-id="ae011-128">For more information about the validation process and how to publish your app, get the [Publish your app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) document from the Download Center.</span></span>

## <a name="learn-more-about-extensions-v20"></a><span data-ttu-id="ae011-129">Yderligere oplysninger om udvidelser v2.0</span><span class="sxs-lookup"><span data-stu-id="ae011-129">Learn more about extensions v2.0</span></span>
<span data-ttu-id="ae011-130">De nye udviklingsværktøjer, som gør det muligt for dig at opbygge udvidelser v2.0, er aktuelt i Vis udskrift og aktiveres snart i Dynamics 365 for Financials-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="ae011-130">The new development tools, which enable to you to build extensions v2.0, are currently in preview and will be enabled in the Dynamics 365 for Financials service soon.</span></span> <span data-ttu-id="ae011-131">Hvis du allerede vil blive fortrolig med de nye værktøjer eller læse mere om udvidelser 2.0, kan du se [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).</span><span class="sxs-lookup"><span data-stu-id="ae011-131">If you already want to familiarize yourself with the new tools or learn more about extensions 2.0, have a look at [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).</span></span>  

## <a name="need-help"></a><span data-ttu-id="ae011-132">Har du brug for hjælp?</span><span class="sxs-lookup"><span data-stu-id="ae011-132">Need help?</span></span>
<span data-ttu-id="ae011-133">Hvis du vil have rådgivning, kan du kontakte en appekspert på listen nedenfor:</span><span class="sxs-lookup"><span data-stu-id="ae011-133">If you would like some coaching, you can contact an app subject matter expert from the following list:</span></span>

* <span data-ttu-id="ae011-134">CloudReady-software [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span><span class="sxs-lookup"><span data-stu-id="ae011-134">Cloud Ready Software, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span></span>  
* <span data-ttu-id="ae011-135">Dynamics App Alliance [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span><span class="sxs-lookup"><span data-stu-id="ae011-135">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span></span>

<span data-ttu-id="ae011-136">Partnere på denne liste:</span><span class="sxs-lookup"><span data-stu-id="ae011-136">Partners in this list:</span></span>

* <span data-ttu-id="ae011-137">Vises alfabetisk</span><span class="sxs-lookup"><span data-stu-id="ae011-137">Are listed alphabetically</span></span>  
* <span data-ttu-id="ae011-138">Yder hjælp til eller har bistået mindst tre partnere med at placere apps i Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="ae011-138">Are assisting or have assisted a minimum of three partners with bringing apps into Microsoft AppSource</span></span>  
* <span data-ttu-id="ae011-139">Har en tilgængelig pakket service (som er opført på deres websted) om de appretningslinjer, de leverer</span><span class="sxs-lookup"><span data-stu-id="ae011-139">Have a packaged service available (and listed on their website) about the app guidance that they provide</span></span>  

<span data-ttu-id="ae011-140">Hvis du mener, at du skal stå som appservice-partner, kan du kontakte [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ae011-140">If you believe you should be listed as an app service partner, don't hesitate to reach out to [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="questions"></a><span data-ttu-id="ae011-141">Spørgsmål?</span><span class="sxs-lookup"><span data-stu-id="ae011-141">Questions?</span></span>
<span data-ttu-id="ae011-142">Disse [Ofte stillede spørgsmål](https://go.microsoft.com/fwlink/?linkid=841520) besvarer de mest almindelige spørgsmål om apps til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ae011-142">This [FAQ](https://go.microsoft.com/fwlink/?linkid=841520) responds to the most common questions you might have about apps for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="ae011-143">Hvis du har yderligere spørgsmål, kan du kontakte Microsoft Danmark eller sende en e-mail til [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ae011-143">If you have further questions, don't hesitate to contact your local Microsoft representative or email [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="further-resources"></a><span data-ttu-id="ae011-144">Flere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ae011-144">Further Resources</span></span>
<span data-ttu-id="ae011-145">Du kan finde flere ressourcer til appudvikling på vores [DLP-emneside](https://mbspartner.microsoft.com/BFI/Topic/76) DLP-emneside.</span><span class="sxs-lookup"><span data-stu-id="ae011-145">Please find further resources for app development on our [DLP topic page](https://mbspartner.microsoft.com/BFI/Topic/76) DLP topic page.</span></span> <span data-ttu-id="ae011-146">Du kan vælge imellem dem, der er valgt nedenfor:</span><span class="sxs-lookup"><span data-stu-id="ae011-146">Some selected ones are available below:</span></span>
-   [<span data-ttu-id="ae011-147">Brugerregistrering og efterfølgende fakturering </span><span class="sxs-lookup"><span data-stu-id="ae011-147">User Registration and Subsequent Billing </span></span>](http://download.microsoft.com/download/3/2/0/320D0286-8810-4A8F-B7DD-523ED87D441B/FAQ on apps for Dynamics 365 for Financials.pdf)



## <a name="see-also"></a><span data-ttu-id="ae011-148">Se også</span><span class="sxs-lookup"><span data-stu-id="ae011-148">See Also</span></span>
<span data-ttu-id="ae011-149">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="ae011-149">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="ae011-150">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="ae011-150">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="ae011-151">https://appsource.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="ae011-151">https://appsource.microsoft.com</span></span>](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365-for-financials&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
