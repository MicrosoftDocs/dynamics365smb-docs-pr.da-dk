---
title: Bruge fakturering og Business Central | Microsoft Docs
description: Løsning, der giver adgang til Microsoft Invoicing, når du har fået Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: b04da7a7fa6d831646c6af9f0606afa90dc00bd6
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188848"
---
# <a name="using-the-same-office-365-account-in-d365fin-and-microsoft-invoicing"></a><span data-ttu-id="c7117-103">Bruge den samme Office 365-konto i [!INCLUDE[d365fin](includes/d365fin_long_md.md)] og Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="c7117-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="c7117-104">Når du tilmelder dig en prøveversion af [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du gå til en 30-dages evalueringsfase, påbegynde et abonnement eller afslutte din brug af [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c7117-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c7117-105">I alle tilfælde kan du, hvis du logger på Office-portalen, se et felt med navnet **Microsoft Invoicing**, som du skal klikke på.</span><span class="sxs-lookup"><span data-stu-id="c7117-105">In all cases, if you sign in to the Office Portal, you might see a tile called **Microsoft Invoicing** and click it.</span></span> <span data-ttu-id="c7117-106">Dette er en del af Office 365 Business Premium-abonnementet, så ikke alle ser dette felt i Office-portalen.</span><span class="sxs-lookup"><span data-stu-id="c7117-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="c7117-107">Hvis du åbner Microsoft Invoicing, vises en meddelelse om, at du ikke kan få adgang til Microsoft Invoicing, fordi kontoen bruges i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c7117-107">If you access Microsoft Invoicing, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="c7117-108">En lignende meddelelse vises, hvis du installerer mobilappen til Invoicing.</span><span class="sxs-lookup"><span data-stu-id="c7117-108">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="c7117-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="c7117-109">Workaround</span></span>
<span data-ttu-id="c7117-110">Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)] har en fælles platform.</span><span class="sxs-lookup"><span data-stu-id="c7117-110">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="c7117-111">Det betyder, at du genkendes som en eksisterende bruger af [!INCLUDE[d365fin](includes/d365fin_md.md)], når du klikker på Invoicing i Office-portalen.</span><span class="sxs-lookup"><span data-stu-id="c7117-111">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Office Portal.</span></span> <span data-ttu-id="c7117-112">Det skyldes, at Invoicing ikke kan bruge den samme virksomhed som [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c7117-112">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="c7117-113">Så du skal logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] og omdøbe din eksisterende virksomhed og derefter oprette en ny virksomhed, som du kan bruge i Invoicing.</span><span class="sxs-lookup"><span data-stu-id="c7117-113">So you will have to sign in to [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="c7117-114">Ingen data flyttes eller overskrives under denne løsningsprocedure.</span><span class="sxs-lookup"><span data-stu-id="c7117-114">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="c7117-115">Sådan omdøber du din virksomhed</span><span class="sxs-lookup"><span data-stu-id="c7117-115">To rename your company</span></span>
1. <span data-ttu-id="c7117-116">Log på [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c7117-116">Sign in to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
2. <span data-ttu-id="c7117-117">I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") og vælge **Mine indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="c7117-117">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose **My Settings**.</span></span>
3. <span data-ttu-id="c7117-118">I feltet **Virksomhed**, skal du vælge en anden leverandør.</span><span class="sxs-lookup"><span data-stu-id="c7117-118">In the **Company** field, choose a different company.</span></span>
4. <span data-ttu-id="c7117-119">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomheder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c7117-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
5. <span data-ttu-id="c7117-120">På siden **Virksomheder** skal du vælge **Rediger liste**.</span><span class="sxs-lookup"><span data-stu-id="c7117-120">On the **Companies** page, choose **Edit List**.</span></span>  
6. <span data-ttu-id="c7117-121">Giv posten *Min virksomhed* et andet navn.</span><span class="sxs-lookup"><span data-stu-id="c7117-121">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="c7117-122">Vent nogle minutter.</span><span class="sxs-lookup"><span data-stu-id="c7117-122">Wait a number of minutes.</span></span> <span data-ttu-id="c7117-123">Vi foretager en række ændringer i den underliggende database, og det tager et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="c7117-123">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
7.  <span data-ttu-id="c7117-124">Når systemet er klar igen, skal du vælge knappen **Opret ny virksomhed**.</span><span class="sxs-lookup"><span data-stu-id="c7117-124">When the system is ready again, choose the **Create New Company** button.</span></span>  
8.  <span data-ttu-id="c7117-125">I den dialogboks, der vises, skal du angive navnet som *Min virksomhed* og vælge indstillingen **Produktion – Kun konfigurationsdata**.</span><span class="sxs-lookup"><span data-stu-id="c7117-125">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="c7117-126">Der går igen nogle minutter.</span><span class="sxs-lookup"><span data-stu-id="c7117-126">This again takes a number of minutes.</span></span> <span data-ttu-id="c7117-127">Når processen er fuldført, kan du få adgang til Invoicing som en del af din Office 365 Business Premium-oplevelse.</span><span class="sxs-lookup"><span data-stu-id="c7117-127">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="c7117-128">Hvad med mine data?</span><span class="sxs-lookup"><span data-stu-id="c7117-128">What about my data?</span></span>
<span data-ttu-id="c7117-129">Når du omdøber det oprindelige Min virksomhed, omdøbes de tabeller i databasen, der indeholder din eksisterende [!INCLUDE[d365fin](includes/d365fin_md.md)]-data, men selve dataene ændres ikke.</span><span class="sxs-lookup"><span data-stu-id="c7117-129">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="c7117-130">Hvis du bruger både Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)], gemmes dataene i to forskellige beholdere (de to virksomheder).</span><span class="sxs-lookup"><span data-stu-id="c7117-130">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="c7117-131">Intet deles, så du skal administrere kunder og varer i begge virksomheder.</span><span class="sxs-lookup"><span data-stu-id="c7117-131">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c7117-132">Se også</span><span class="sxs-lookup"><span data-stu-id="c7117-132">See Also</span></span>
[<span data-ttu-id="c7117-133">Ofte stillede spørgsmål</span><span class="sxs-lookup"><span data-stu-id="c7117-133">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="c7117-134">Opsætning</span><span class="sxs-lookup"><span data-stu-id="c7117-134">Administration</span></span>](admin-setup-and-administration.md)  
