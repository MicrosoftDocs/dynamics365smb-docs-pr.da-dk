---
title: Bruge fakturering og Business Central | Microsoft Docs
description: Løsning, der giver adgang til Microsoft Invoicing, når du har fået Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Microsoft 365
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 0c6b739faf2d531505bde4ad2dc7eb85c39ed223
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385020"
---
# <a name="using-the-same-microsoft-365-account-in-prod_short-and-microsoft-invoicing"></a><span data-ttu-id="d85bb-103">Bruge den samme MIcrosoft 365-konto i [!INCLUDE[prod_short](includes/prod_long.md)] og Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="d85bb-103">Using the same Microsoft 365 Account in [!INCLUDE[prod_short](includes/prod_long.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="d85bb-104">Når du tilmelder dig en prøveversion af [!INCLUDE[prod_short](includes/prod_short.md)], kan du gå til en 30-dages evalueringsfase, påbegynde et abonnement eller afslutte din brug af [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d85bb-104">When you sign up for a trial with [!INCLUDE[prod_short](includes/prod_short.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d85bb-105">I alle tilfælde har du måske på et tidspunkt set noget, der hedder **Microsoft Invoicing** og klikket på det.</span><span class="sxs-lookup"><span data-stu-id="d85bb-105">In all cases, you may at some point have seen something called **Microsoft Invoicing** and clicked it.</span></span> <span data-ttu-id="d85bb-106">Dette var en app, som var en del af det, der nu hedder Microsoft 365 Business Standard. Dette hed tidligere et Microsoft 365 Business Premium-abonnement. Derfor er det ikke alle, der har set feltet i Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d85bb-106">This was an app that was part of what is now Microsoft 365 Business Standard and was formerly known as Microsoft 365 Business Premium subscription, so not everyone will have seen that tile in their Microsoft 365 experience.</span></span>  

<span data-ttu-id="d85bb-107">Microsoft Invoicing er ikke længere tilgængelig, men hvis du skal logge på Invoicing for at hente dine data, vil du muligvis se en besked om, at du ikke kan få adgang til Microsoft Invoicing, fordi din konto bruges i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d85bb-107">Microsoft Invoicing is no longer available, but if you need to sign into Invoicing to retrieve your data, you might see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="d85bb-108">En lignende meddelelse vises, hvis du installerer mobilappen til Invoicing.</span><span class="sxs-lookup"><span data-stu-id="d85bb-108">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="d85bb-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="d85bb-109">Workaround</span></span>
<span data-ttu-id="d85bb-110">Invoicing og [!INCLUDE[prod_short](includes/prod_short.md)] har en fælles platform.</span><span class="sxs-lookup"><span data-stu-id="d85bb-110">Invoicing and [!INCLUDE[prod_short](includes/prod_short.md)] have a shared platform.</span></span> <span data-ttu-id="d85bb-111">Det betyder, at du genkendes som en eksisterende bruger af [!INCLUDE[prod_short](includes/prod_short.md)], når du klikker på Invoicing i Microsoft 365 Administration.</span><span class="sxs-lookup"><span data-stu-id="d85bb-111">That means that you are recognized as an existing user of [!INCLUDE[prod_short](includes/prod_short.md)] when you click Invoicing in the Microsoft 365 admin center.</span></span> <span data-ttu-id="d85bb-112">Det skyldes, at Invoicing ikke kan bruge den samme virksomhed som [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d85bb-112">The reason is that Invoicing cannot use the same company as [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="d85bb-113">Så du skal logge på [!INCLUDE[prod_short](includes/prod_short.md)] og omdøbe din eksisterende virksomhed og derefter oprette en ny virksomhed, som du kan bruge i Invoicing.</span><span class="sxs-lookup"><span data-stu-id="d85bb-113">So you will have to sign in to [!INCLUDE[prod_short](includes/prod_short.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="d85bb-114">Ingen data flyttes eller overskrives under denne løsningsprocedure.</span><span class="sxs-lookup"><span data-stu-id="d85bb-114">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="d85bb-115">Sådan omdøber du din virksomhed</span><span class="sxs-lookup"><span data-stu-id="d85bb-115">To rename your company</span></span>
1. <span data-ttu-id="d85bb-116">Log på [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d85bb-116">Sign in to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
2. <span data-ttu-id="d85bb-117">I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") og vælge **Mine indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="d85bb-117">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose **My Settings**.</span></span>
3. <span data-ttu-id="d85bb-118">I feltet **Virksomhed**, skal du vælge en anden leverandør.</span><span class="sxs-lookup"><span data-stu-id="d85bb-118">In the **Company** field, choose a different company.</span></span>
4. <span data-ttu-id="d85bb-119">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomheder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d85bb-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
5. <span data-ttu-id="d85bb-120">På siden **Virksomheder** skal du vælge **Rediger liste**.</span><span class="sxs-lookup"><span data-stu-id="d85bb-120">On the **Companies** page, choose **Edit List**.</span></span>  
6. <span data-ttu-id="d85bb-121">Giv posten *Min virksomhed* et andet navn.</span><span class="sxs-lookup"><span data-stu-id="d85bb-121">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="d85bb-122">Vent nogle minutter.</span><span class="sxs-lookup"><span data-stu-id="d85bb-122">Wait a number of minutes.</span></span> <span data-ttu-id="d85bb-123">Vi foretager en række ændringer i den underliggende database, og det tager et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="d85bb-123">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
7.  <span data-ttu-id="d85bb-124">Når systemet er klar igen, skal du vælge knappen **Opret ny virksomhed**.</span><span class="sxs-lookup"><span data-stu-id="d85bb-124">When the system is ready again, choose the **Create New Company** button.</span></span>  
8.  <span data-ttu-id="d85bb-125">I den dialogboks, der vises, skal du angive navnet som *Min virksomhed* og vælge indstillingen **Produktion – Kun konfigurationsdata**.</span><span class="sxs-lookup"><span data-stu-id="d85bb-125">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="d85bb-126">Der går igen nogle minutter.</span><span class="sxs-lookup"><span data-stu-id="d85bb-126">This again takes a number of minutes.</span></span> <span data-ttu-id="d85bb-127">Når processen er fuldført, kan du få adgang til Invoicing som en del af din Microsoft 365 Business Standard-oplevelse.</span><span class="sxs-lookup"><span data-stu-id="d85bb-127">When the process completes, you will be able to access Invoicing as part of your Microsoft 365 Business Standard experience.</span></span> <span data-ttu-id="d85bb-128">men kun for at eksportere data, da Invoicing-programmet er udfaset.</span><span class="sxs-lookup"><span data-stu-id="d85bb-128">but only to export data since the Invoicing app is deprecated.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="d85bb-129">Hvad med mine data?</span><span class="sxs-lookup"><span data-stu-id="d85bb-129">What about my data?</span></span>
<span data-ttu-id="d85bb-130">Når du omdøber det oprindelige Min virksomhed, omdøbes de tabeller i databasen, der indeholder din eksisterende [!INCLUDE[prod_short](includes/prod_short.md)]-data, men selve dataene ændres ikke.</span><span class="sxs-lookup"><span data-stu-id="d85bb-130">When you rename the original My Company, the database tables that store your existing [!INCLUDE[prod_short](includes/prod_short.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="d85bb-131">Hvis du bruger både Invoicing og [!INCLUDE[prod_short](includes/prod_short.md)], gemmes dataene i to forskellige beholdere (de to virksomheder).</span><span class="sxs-lookup"><span data-stu-id="d85bb-131">If you use both Invoicing and [!INCLUDE[prod_short](includes/prod_short.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="d85bb-132">Intet deles, så du skal administrere kunder og varer i begge virksomheder.</span><span class="sxs-lookup"><span data-stu-id="d85bb-132">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d85bb-133">Se også</span><span class="sxs-lookup"><span data-stu-id="d85bb-133">See Also</span></span>
[<span data-ttu-id="d85bb-134">Ofte stillede spørgsmål</span><span class="sxs-lookup"><span data-stu-id="d85bb-134">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="d85bb-135">Opsætning</span><span class="sxs-lookup"><span data-stu-id="d85bb-135">Administration</span></span>](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]