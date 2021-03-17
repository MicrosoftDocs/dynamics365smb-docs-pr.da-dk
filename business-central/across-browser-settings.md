---
title: Konfigurerer din browser
description: Beskriver, hvordan du konfigurerer browsere til at arbejde med Business Central og produkter, der er integreret med den.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 01/08/2021
ms.author: jswymer
ms.openlocfilehash: b5083735be31b635cb3fc3ce404e7f182d04640f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384970"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><span data-ttu-id="1f5d6-103">Konfigurere og foretage fejlfinding i browseren om, hvordan du arbejder med webklienten Business Central</span><span class="sxs-lookup"><span data-stu-id="1f5d6-103">Setting Up and Troubleshooting Your Browser to Work With Business Central Web Client</span></span>

<span data-ttu-id="1f5d6-104">I denne artikel forklares det, hvordan du konfigurerer din webbrowser, så [!INCLUDE[web_client](includes/web_client.md)] og alle funktionerne fungerer korrekt.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-104">This article explains how to set up your browser so that the [!INCLUDE[web_client](includes/web_client.md)] and all its features work properly.</span></span> <span data-ttu-id="1f5d6-105">Læs denne artikel, hvis du har problemer med at åbne [!INCLUDE[web_client](includes/web_client.md)], fordi nogle problemer kan være forårsaget af browserens indstillinger.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-105">Read this article if you're having problems opening the [!INCLUDE[web_client](includes/web_client.md)], because some problems may be caused by your browser's settings.</span></span>

<span data-ttu-id="1f5d6-106">Artiklen indeholder oplysninger om, hvordan du kan konfigurere Microsoft Edge, men kravene til JavaScript, cookies og pop op-vinduer er de samme for alle understøttede browsere.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-106">The article provides details for setting up Microsoft Edge, but the requirements for JavaScript, cookies, and pop-ups are the same for all supported browsers.</span></span> <span data-ttu-id="1f5d6-107">Hvis du har andre browsere, skal du se vejledningen fra producenten.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-107">For other browsers, refer to the instructions provided by the manufacturer.</span></span>  

## <a name="use-a-supported-browser"></a><span data-ttu-id="1f5d6-108">Brug en understøttet browser</span><span class="sxs-lookup"><span data-stu-id="1f5d6-108">Use a supported browser</span></span>

<span data-ttu-id="1f5d6-109">Sørg for at bruge en af de understøttede browsere.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-109">Make sure to use a one of the supported browsers.</span></span> <span data-ttu-id="1f5d6-110">Se [Minimumkrav til brug af Business Central](product-requirements.md#recommended-browsers).</span><span class="sxs-lookup"><span data-stu-id="1f5d6-110">See [Minimum Requirements for Using Business Central](product-requirements.md#recommended-browsers).</span></span>  

## <a name="allow-javascript-from-business-central"></a><span data-ttu-id="1f5d6-111">Tillad JavaScript fra Business Central</span><span class="sxs-lookup"><span data-stu-id="1f5d6-111">Allow JavaScript from Business Central</span></span>

<span data-ttu-id="1f5d6-112">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="1f5d6-112">*Problem:*</span></span>

<span data-ttu-id="1f5d6-113">Hvis browseren ikke tillader JavaScript, kan du se **NotSupported/DisabledJavaScript** på adresselinjen og en **HTTP-fejl 404,0-ikke fundet**-meddelelse, når du forsøger at åbne [!INCLUDE[prod_short](includes/prod_short.md)], og den</span><span class="sxs-lookup"><span data-stu-id="1f5d6-113">If the browser doesn't allow JavaScript, you'll see **NotSupported/DisabledJavaScript** in the address bar and an **HTTP Error 404.0 - Not Found** message when you try to open [!INCLUDE[prod_short](includes/prod_short.md)], and the</span></span> 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

<span data-ttu-id="1f5d6-114">*Ret:*</span><span class="sxs-lookup"><span data-stu-id="1f5d6-114">*Fix:*</span></span>

1. <span data-ttu-id="1f5d6-115">I Microsoft Edge skal du gå til **Indstillinger** > **Cookies og websteds tilladelser** > **JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-115">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **JavaScript**.</span></span>
2. <span data-ttu-id="1f5d6-116">Gør ét af følgende:</span><span class="sxs-lookup"><span data-stu-id="1f5d6-116">Do one of the following steps.</span></span> <span data-ttu-id="1f5d6-117">Vælg det trin, der anbefales af organisationen:</span><span class="sxs-lookup"><span data-stu-id="1f5d6-117">Choose the step that is recommended by your organization:</span></span>

    - <span data-ttu-id="1f5d6-118">Flytte **Tilladt** til venstre mod venstre (Off).</span><span class="sxs-lookup"><span data-stu-id="1f5d6-118">Move the **Allowed** toggle to the left (Off).</span></span> <span data-ttu-id="1f5d6-119">Derefter skal du vælge **Tilføj** og skrive adressen (URL-adressen) til [!INCLUDE[prod_short](includes/prod_short.md)] i feltet **Websted**.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-119">Then, select **Add** and type the address (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] in the **Site** box.</span></span> <span data-ttu-id="1f5d6-120">Vælg **Tilføj**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-120">Select **Add** when done.</span></span>
    - <span data-ttu-id="1f5d6-121">Flytte **Tilladt** til venstre mod højre (On).</span><span class="sxs-lookup"><span data-stu-id="1f5d6-121">Move the **Allowed** toggle to the right (On).</span></span>

## <a name="allow-cookies-from-business-central"></a><span data-ttu-id="1f5d6-122">Tillad cookies fra Business Central</span><span class="sxs-lookup"><span data-stu-id="1f5d6-122">Allow cookies from Business Central</span></span>

<span data-ttu-id="1f5d6-123">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="1f5d6-123">*Problem:*</span></span>

<span data-ttu-id="1f5d6-124">Hvis browseren ikke tillader cookies, får du vist følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="1f5d6-124">If the browser doesn't allow cookies, you'll get the following error:</span></span>

<span data-ttu-id="1f5d6-125">**Beklager, men siden blev ikke fundet. Kontroller adressen, og prøv igen.**</span><span class="sxs-lookup"><span data-stu-id="1f5d6-125">**Sorry, the page could not be found. Please check the address and try again.**</span></span> 

<span data-ttu-id="1f5d6-126">*Ret:*</span><span class="sxs-lookup"><span data-stu-id="1f5d6-126">*Fix:*</span></span>

1. <span data-ttu-id="1f5d6-127">I Microsoft Edge skal du gå til **Indstillinger** > **Cookies og webstedstilladelser** > **Cookies og webstedsdata**.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-127">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.</span></span>
2. <span data-ttu-id="1f5d6-128">Flyt **Tillad websteder gemmer og læser cookiedata** til højre (On).</span><span class="sxs-lookup"><span data-stu-id="1f5d6-128">Move the **Allow sites to save and read cookie data** toggle to the right (On).</span></span>  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a><span data-ttu-id="1f5d6-129">Tillad pop-ops fra Business Central</span><span class="sxs-lookup"><span data-stu-id="1f5d6-129">Allow pop-ups from Business Central</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="1f5d6-130">integreres med flere produkter.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-130">integrates with several products.</span></span> <span data-ttu-id="1f5d6-131">I nogle tilfælde, som f.eks. med Microsoft Teams [!INCLUDE[prod_short](includes/prod_short.md)] åbnes, eller "pop op-vinduer", i produktet.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-131">In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product.</span></span> <span data-ttu-id="1f5d6-132">Denne egenskab kræver, at browseren tillader pop op-vinduer [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1f5d6-132">This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="1f5d6-133">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="1f5d6-133">*Problem:*</span></span>

<span data-ttu-id="1f5d6-134">Hvis pop op-vinduer i [!INCLUDE[prod_short](includes/prod_short.md)] er blokeret, vises der en meddelelse, der ligner følgende meddelelse:</span><span class="sxs-lookup"><span data-stu-id="1f5d6-134">If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:</span></span>

<span data-ttu-id="1f5d6-135">**Noget gik galt. Måske blokerer browseren pop op-vinduer, der kræves af Business Central.**</span><span class="sxs-lookup"><span data-stu-id="1f5d6-135">**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**</span></span>

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
<span data-ttu-id="1f5d6-136">*Ret:*</span><span class="sxs-lookup"><span data-stu-id="1f5d6-136">*Fix:*</span></span>

1. <span data-ttu-id="1f5d6-137">I Microsoft Edge skal du gå til **Indstillinger** > **Cookies og webstedstilladelser** > **Pop op-vinduer og omdirigere**.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-137">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.</span></span>
2. <span data-ttu-id="1f5d6-138">Flytte **Blokeret** til mod højre (On).</span><span class="sxs-lookup"><span data-stu-id="1f5d6-138">Move the **Blocked** toggle to the right (On).</span></span>
3. <span data-ttu-id="1f5d6-139">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-139">Select **Add**.</span></span> <span data-ttu-id="1f5d6-140">Skriv i feltet **Websted** `https://businesscentral.dynamics.com`, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-140">In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f5d6-141">Se også</span><span class="sxs-lookup"><span data-stu-id="1f5d6-141">See Also</span></span>

[<span data-ttu-id="1f5d6-142">Fejlfinding i Teams</span><span class="sxs-lookup"><span data-stu-id="1f5d6-142">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]