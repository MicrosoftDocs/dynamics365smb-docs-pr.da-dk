---
title: Optimere Outlook til Business Central-indbakke
description: Få mere at vide om, hvad du kan gøre for at forbedre oplevelsen med Business-indbakken i Microsoft Outlook.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in
ms.date: 05/12/2021
ms.author: jswymer
ms.openlocfilehash: 2fee1782057d0f45319e4d12d715c2e1e0d3d4a6
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/19/2021
ms.locfileid: "6064852"
---
# <a name="optimizing-outlook-for-your-business-inbox"></a><span data-ttu-id="87074-103">Optimere Outlook til Business Central-indbakke</span><span class="sxs-lookup"><span data-stu-id="87074-103">Optimizing Outlook for Your Business Inbox</span></span> 

<span data-ttu-id="87074-104">Denne artikel beskriver, hvad du kan gøre for at få den bedst mulige oplevelse med Business-indbakken i Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="87074-104">This article discusses things you can do to get the best possible experience with the Business Inbox in Microsoft Outlook.</span></span> 

## <a name="update-outlook"></a><span data-ttu-id="87074-105">Opdatere Outlook</span><span class="sxs-lookup"><span data-stu-id="87074-105">Update Outlook</span></span>

<span data-ttu-id="87074-106">Opdater til Outlook version 2012 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="87074-106">Update to Outlook version 2012 or newer.</span></span>

> [!NOTE]
> <span data-ttu-id="87074-107">Hvis du ikke kan opdatere Outlook til version 2012 eller nyere, skal du kontrollere, at du mindst opdaterer til version 1905.</span><span class="sxs-lookup"><span data-stu-id="87074-107">If you are unable to update Outlook to version 2012 or later, make sure that you at least update to version 1905.</span></span> <span data-ttu-id="87074-108">Dette forhindrer Outlook-tilføjelsesprogrammet i at køre med ældre Internet Explorer-komponenter</span><span class="sxs-lookup"><span data-stu-id="87074-108">This prevents the Outlook Add-in from running using legacy Internet Explorer components</span></span>

### <a name="how-to-check-your-version-of-outlook"></a><span data-ttu-id="87074-109">Sådan kontrolleres din version af Outlook</span><span class="sxs-lookup"><span data-stu-id="87074-109">How to check your version of Outlook</span></span>

<span data-ttu-id="87074-110">Uanset om du bruger Office 2019 eller Microsoft 365, skal du følge denne Microsoft Support vejledning for at kontrollere, hvilken version af Outlook du har:</span><span class="sxs-lookup"><span data-stu-id="87074-110">Whether you use Office 2019 or Microsoft 365, follow this Microsoft Support guide to check which version of Outlook you have:</span></span>  

[<span data-ttu-id="87074-111">Om Office: Hvilken version af Office, bruger jeg?</span><span class="sxs-lookup"><span data-stu-id="87074-111">About Office: What version of Office am I using?</span></span>](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### <a name="how-to-update-outlook"></a><span data-ttu-id="87074-112">Sådan opdateres Outlook</span><span class="sxs-lookup"><span data-stu-id="87074-112">How to update Outlook</span></span>

<span data-ttu-id="87074-113">Hvis du vil opdatere Outlook til den seneste version, skal du følge denne Microsoft Support vejledning eller kontakte administratoren:</span><span class="sxs-lookup"><span data-stu-id="87074-113">To update Outlook to the latest version, follow this Microsoft Support guide or contact your administrator:</span></span>

[<span data-ttu-id="87074-114">Installere Office-opdateringer</span><span class="sxs-lookup"><span data-stu-id="87074-114">Install Office updates</span></span>](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## <a name="install-microsoft-edge-webview2"></a><span data-ttu-id="87074-115">Installer Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="87074-115">Install Microsoft Edge WebView2</span></span>

<span data-ttu-id="87074-116">Kontroller, at Microsoft Edge WebView2 er installeret på din enhed.</span><span class="sxs-lookup"><span data-stu-id="87074-116">Ensure that Microsoft Edge WebView2 is installed on your device.</span></span>

### <a name="how-to-check-if-microsoft-edge-webview2-is-installed"></a><span data-ttu-id="87074-117">Sådan kontrollerer du, om Microsoft Edge WebView2 er installeret</span><span class="sxs-lookup"><span data-stu-id="87074-117">How to check if Microsoft Edge WebView2 is installed</span></span> 

<span data-ttu-id="87074-118">Hvis du vil kontrollere, om du har Microsoft Edge WebView2 installeret på en computer, skal du benytte følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="87074-118">To check if you have Microsoft Edge WebView2 installed on a computer, do the following steps:</span></span>

<span data-ttu-id="87074-119">Fra menuen Start:</span><span class="sxs-lookup"><span data-stu-id="87074-119">From Start menu:</span></span>

1. <span data-ttu-id="87074-120">Vælge **Start** ![Windows-Start](media/windows-start-icon.png "Ikonet Windows Start") > **Indstillinger** ![Windows-indstillinger](media/windows-settings-icon.png "Windows-ikonet indstillinger") > **Apps og funktioner**.</span><span class="sxs-lookup"><span data-stu-id="87074-120">Choose **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon") > **Settings** ![Windows Settings](media/windows-settings-icon.png "Windows Settings icon") > **Apps & Features**.</span></span>
2. <span data-ttu-id="87074-121">Skriv **WebView2** i søgefeltet.</span><span class="sxs-lookup"><span data-stu-id="87074-121">In the search box, type **WebView2**.</span></span> <span data-ttu-id="87074-122">Hvis Microsoft Edge WebView2 er installeret, kan du se en post med navnet **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="87074-122">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

<span data-ttu-id="87074-123">Fra kontrolpanel:</span><span class="sxs-lookup"><span data-stu-id="87074-123">From Control Panel:</span></span>

1. <span data-ttu-id="87074-124">I søgefeltet ved siden af **Start** ![Windows Start](media/windows-start-icon.png "Ikonet Windows Start"), skal du skrive **Kontrolpanel** og vælg derefter resultatet.</span><span class="sxs-lookup"><span data-stu-id="87074-124">In the search box next to **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon"), type **Control Panel**, and then select the result.</span></span>
2. <span data-ttu-id="87074-125">Vælg **Programmer** > **Programmer og funktioner**.</span><span class="sxs-lookup"><span data-stu-id="87074-125">Choose **Programs** > **Programs and Features**.</span></span>
3. <span data-ttu-id="87074-126">Skriv **WebView2** i søgefeltet.</span><span class="sxs-lookup"><span data-stu-id="87074-126">In the search box, type **WebView2**.</span></span> <span data-ttu-id="87074-127">Hvis Microsoft Edge WebView2 er installeret, kan du se en post med navnet **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="87074-127">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

### <a name="how-to-install-microsoft-edge-webview2"></a><span data-ttu-id="87074-128">Sådan installeres Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="87074-128">How to install Microsoft Edge WebView2</span></span> 

1. <span data-ttu-id="87074-129">Brug browseren til at gå til [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span><span class="sxs-lookup"><span data-stu-id="87074-129">Using your browser, go to [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span></span>
2. <span data-ttu-id="87074-130">Vælg **Hent**.</span><span class="sxs-lookup"><span data-stu-id="87074-130">Choose **Download**.</span></span>
3. <span data-ttu-id="87074-131">Indstil den **Valgte arkitektur**, så den passer til systemet.</span><span class="sxs-lookup"><span data-stu-id="87074-131">Set **Select Architecture** to match your system.</span></span>
4. <span data-ttu-id="87074-132">Vælg **Hent**.</span><span class="sxs-lookup"><span data-stu-id="87074-132">Choose **Download**.</span></span>

> [!NOTE]
> <span data-ttu-id="87074-133">Organisationen kan have begrænsninger for, hvilke komponenter der kan installeres på din enhed.</span><span class="sxs-lookup"><span data-stu-id="87074-133">Your organization may have restriction on which components can be installed on your device.</span></span> <span data-ttu-id="87074-134">Kontakt din administrator for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="87074-134">Contact your administrator for assistance.</span></span>

## <a name="use-a-supported-browser"></a><span data-ttu-id="87074-135">Brug en understøttet browser</span><span class="sxs-lookup"><span data-stu-id="87074-135">Use a supported browser</span></span>

<span data-ttu-id="87074-136">Overvej at bruge Outlook til World Wide Web i en af de browsere, der understøttes af Business central.</span><span class="sxs-lookup"><span data-stu-id="87074-136">Consider using Outlook for the Web in one of the browsers supported by Business Central.</span></span> <span data-ttu-id="87074-137">Du kan finde en liste over understøttede browsere under [Minimum krav til brug af Business Central](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="87074-137">For a list of supported browsers, see [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>

## <a name="see-also"></a><span data-ttu-id="87074-138">Se også</span><span class="sxs-lookup"><span data-stu-id="87074-138">See Also</span></span>

[<span data-ttu-id="87074-139">Blive køreklar</span><span class="sxs-lookup"><span data-stu-id="87074-139">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
[<span data-ttu-id="87074-140">Få Business Central på min mobilenhed</span><span class="sxs-lookup"><span data-stu-id="87074-140">Getting Business Central on my Mobile Device</span></span>](install-mobile-app.md)  
[<span data-ttu-id="87074-141">Sende dokumenter som mail</span><span class="sxs-lookup"><span data-stu-id="87074-141">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="87074-142">Finans</span><span class="sxs-lookup"><span data-stu-id="87074-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="87074-143">Salg</span><span class="sxs-lookup"><span data-stu-id="87074-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="87074-144">Køb</span><span class="sxs-lookup"><span data-stu-id="87074-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="87074-145">Minimumkrav til Outlook</span><span class="sxs-lookup"><span data-stu-id="87074-145">Minimum Requirements for Outlook</span></span>](product-requirements.md#outlook)  
[<span data-ttu-id="87074-146">Bruge tilføjelsesprogrammer i Outlook på internettet</span><span class="sxs-lookup"><span data-stu-id="87074-146">Using add-ins in Outlook on the web</span></span>](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]