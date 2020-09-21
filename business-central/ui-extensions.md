---
title: Installation af udvidelser til tilpasning af Business Central | Microsoft Docs
description: Få mere at vide om tilføjelse af funktioner og tilpasning af Business Central ved at installere udvidelser.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765917"
---
# <a name="customizing-business-central-using-extensions"></a><span data-ttu-id="5d156-103">Tilpasse Business Central ved brug af udvidelser</span><span class="sxs-lookup"><span data-stu-id="5d156-103">Customizing Business Central Using Extensions</span></span>

<span data-ttu-id="5d156-104">Du kan ændre [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at installere udvidelser, der f.eks. tilføjer funktioner, ændrer funktionsmåder eller giver dig adgang til nye onlinetjenester.</span><span class="sxs-lookup"><span data-stu-id="5d156-104">You can change [!INCLUDE[d365fin](includes/d365fin_md.md)] by installing extensions that add functionality, changes behavior, or gives you access to new online services, for example.</span></span>

> [!NOTE]
> <span data-ttu-id="5d156-105">Hvis du vil installere udvidelser fra AppSource eller tilføje udvidelser pr. lejer, skal du have de rigtige rettigheder.</span><span class="sxs-lookup"><span data-stu-id="5d156-105">To install extensions from AppSource or add per-tenant extensions, you must have the right permissions.</span></span> <span data-ttu-id="5d156-106">Du skal enten være medlem af brugergruppen D365 EXTENSION MGMT, eller du skal have rettighedssættet D365 EXTENSION MGMT.</span><span class="sxs-lookup"><span data-stu-id="5d156-106">You must either be a member of the D365 EXTENSION MGMT user group or you must have the D365 EXTENSION MGMT permission set.</span></span> <span data-ttu-id="5d156-107">Hvis du er administrator, kan du tildele brugergrupper og rettigheder til andre brugere i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="5d156-107">If you are an administrator, you can assign user groups and permissions to other users in your company.</span></span><br /><br />
<span data-ttu-id="5d156-108">Hvis du vil bruge de funktioner, der findes i en udvidelse, f. eks. åbne sider, køre rapporter, vælge handlinger osv., skal du være tildelt de rettighedssæt, der er installeret som en del af udvidelsen.</span><span class="sxs-lookup"><span data-stu-id="5d156-108">To use the functionality that is provided by an extension, such as opening pages, running reports, selecting actions, and so on, you must be assigned the permission sets that are installed as part of the extension.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="5d156-109">Overførsel af udvidelser pr. lejer og installation af AppSource-udvidelser understøttes ikke via siden **Udvidelsesstyring** til lokale installationer.</span><span class="sxs-lookup"><span data-stu-id="5d156-109">The upload of per-tenant extensions and the installation of AppSource extensions is not supported through the **Extension Management** page for on-premise installations.</span></span>

<span data-ttu-id="5d156-110">Når du starter [!INCLUDE[d365fin](includes/d365fin_md.md)] første gang, er der allerede installeret nogle udvidelser for dig.</span><span class="sxs-lookup"><span data-stu-id="5d156-110">When you first launch [!INCLUDE[d365fin](includes/d365fin_md.md)], some extensions are already installed for you.</span></span> <span data-ttu-id="5d156-111">Med tiden gøres flere udvidelser tilgængelige for dig, og du kan derefter vælge, om du vil bruge udvidelsen eller ej.</span><span class="sxs-lookup"><span data-stu-id="5d156-111">Over time, more extensions will be made available to you, and you can then choose if you want to use the extension or not.</span></span>

<span data-ttu-id="5d156-112">Microsoft leverer f.eks. en udvidelse, der giver integration med PayPal Payments Standard.</span><span class="sxs-lookup"><span data-stu-id="5d156-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span> <span data-ttu-id="5d156-113">Denne udvidelse er installeret som standard.</span><span class="sxs-lookup"><span data-stu-id="5d156-113">This extension is installed by default.</span></span>
<span data-ttu-id="5d156-114">Men hvis en anden udvidelse, som tilbyder integration med en anden betalingstjeneste, stilles til rådighed, kan du installere nye udvidelse og derefter vælge, hvilken af to de tjenester du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="5d156-114">But if another extension is made available that offers integration with another payment service, you can install the new extension and then choose which of the two services to use.</span></span>  

<span data-ttu-id="5d156-115">Du kan administrere udvidelserne på siden **Udvidelsesstyring**.</span><span class="sxs-lookup"><span data-stu-id="5d156-115">You manage the extensions on the **Extension Management** page.</span></span> <span data-ttu-id="5d156-116">Du kan åbne siden fra Start.</span><span class="sxs-lookup"><span data-stu-id="5d156-116">You can access this page from Home.</span></span> <span data-ttu-id="5d156-117">Du kan også vælge ikonet **Søg efter side eller rapport** ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), skrive **Udvidelse** i øverste højre hjørne og derefter vælge det relaterede kæde.</span><span class="sxs-lookup"><span data-stu-id="5d156-117">Alternatively, choose the **Search for Page or Report** icon ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") in the top right corner, enter **Extension**, and then choose the related link.</span></span> <span data-ttu-id="5d156-118">Du kan finde flere oplysninger under [Installere og fjerne udvidelser](ui-extensions-install-uninstall.md).</span><span class="sxs-lookup"><span data-stu-id="5d156-118">For more information, see [Installing and Uninstalling Extensions](ui-extensions-install-uninstall.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="5d156-119">Hvis du mener, at du skal have adgang til en udvidelse, men ikke kan finde de relevante funktioner, skal du vælge siden **Udvidelsesstyring** – hvis filtypen ikke er angivet der, kan du installere den som beskrevet i følgende afsnit.</span><span class="sxs-lookup"><span data-stu-id="5d156-119">If you think you should have access to an extension but you cannot find its functionality, check the **Extension Management** page - if the extension is not listed there, you can install it as described in the following section.</span></span>  

> [!NOTE]  
> <span data-ttu-id="5d156-120">Der findes ingen nye udvidelser i AppSource umiddelbart efter, at vi har oplyst om en opdatering.</span><span class="sxs-lookup"><span data-stu-id="5d156-120">New extensions are not available in AppSource immediately after we announce an update.</span></span> <span data-ttu-id="5d156-121">Du kan holde øje med udvidelser på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span><span class="sxs-lookup"><span data-stu-id="5d156-121">You can keep an eye out for the extensions at  [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span></span>

## <a name="see-also"></a><span data-ttu-id="5d156-122">Se også</span><span class="sxs-lookup"><span data-stu-id="5d156-122">See Also</span></span>

[<span data-ttu-id="5d156-123">Udvidelse af Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="5d156-123">Extending Dynamics 365 Business Central</span></span>](about-develop-extensions.md)  
[<span data-ttu-id="5d156-124">Business Central-udvidelser fra andre leverandører</span><span class="sxs-lookup"><span data-stu-id="5d156-124">Business Central Extensions by Other Providers</span></span>](ui-extensions-other.md)  
[<span data-ttu-id="5d156-125">Konfigurere tjenesten Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="5d156-125">Set Up the Envestnet Yodlee Bank Feeds Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="5d156-126">Aktivere debitorbetaling via PayPal</span><span class="sxs-lookup"><span data-stu-id="5d156-126">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md)  
[<span data-ttu-id="5d156-127">Overførsel af virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="5d156-127">Migrating Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="5d156-128">Konfiguration af den britiske GetAddress.io-postnummerudvidelse</span><span class="sxs-lookup"><span data-stu-id="5d156-128">Setting Up the GetAddress.io UK Postal Code extension</span></span>](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
<span data-ttu-id="5d156-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)]-udvidelser fra andre leverandører](ui-extensions-other.md)</span><span class="sxs-lookup"><span data-stu-id="5d156-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensions by Other Providers](ui-extensions-other.md)</span></span>  
[<span data-ttu-id="5d156-130">Introduktion</span><span class="sxs-lookup"><span data-stu-id="5d156-130">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
