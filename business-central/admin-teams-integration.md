---
title: Administration af Microsoft Teams-integration med Business Central| Microsoft Docs
description: Administration af Microsoft Teams-integration med Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989354"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a><span data-ttu-id="ccab4-103">Administration af Microsoft Teams-integration med Business Central</span><span class="sxs-lookup"><span data-stu-id="ccab4-103">Managing Microsoft Teams Integration with Business Central</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="ccab4-104">Denne artikel giver en oversigt over, hvad du kan gøre som administrator for at kontrollere Microsoft Teams-integration med [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="ccab4-104">This article provides an overview of what you can do as an administrator to control Microsoft Teams integration with [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

## <a name="in-microsoft-teams"></a><span data-ttu-id="ccab4-105">I Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ccab4-105">In Microsoft Teams</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="ccab4-106">Minimumkrav</span><span class="sxs-lookup"><span data-stu-id="ccab4-106">Minimum requirements</span></span>

<span data-ttu-id="ccab4-107">I dette afsnit beskrives minimumkrav til [!INCLUDE [prodshort](includes/prodshort.md)]-appfunktioner for at arbejde i Teams.</span><span class="sxs-lookup"><span data-stu-id="ccab4-107">This section describes the minimum requirements for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

- <span data-ttu-id="ccab4-108">Krævede licenser</span><span class="sxs-lookup"><span data-stu-id="ccab4-108">Required licenses</span></span>

    <span data-ttu-id="ccab4-109">Denne tabel giver dig et overblik over de licenser, der er nødvendige for at [!INCLUDE [prodshort](includes/prodshort.md)]-appfunktionerne kan bruges i Teams.</span><span class="sxs-lookup"><span data-stu-id="ccab4-109">This table gives you an overview of the licenses needed for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

    |<span data-ttu-id="ccab4-110">Hvad</span><span class="sxs-lookup"><span data-stu-id="ccab4-110">What</span></span>|<span data-ttu-id="ccab4-111">Teams-licens</span><span class="sxs-lookup"><span data-stu-id="ccab4-111">Teams license</span></span>|<span data-ttu-id="ccab4-112">Business Central-licens</span><span class="sxs-lookup"><span data-stu-id="ccab4-112">Business Central license</span></span>|
    |----|---|---|
    |<span data-ttu-id="ccab4-113">Indsæt et link til en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en samtale, og send den som et kort.</span><span class="sxs-lookup"><span data-stu-id="ccab4-113">Paste a link to a [!INCLUDE [prodshort](includes/prodshort.md)] record into a conversation, and send it as a card.</span></span>|<span data-ttu-id="ccab4-114">![markering](media/check.png "check")</span><span class="sxs-lookup"><span data-stu-id="ccab4-114">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="ccab4-115">![markering](media/check.png "check")</span><span class="sxs-lookup"><span data-stu-id="ccab4-115">![check mark](media/check.png "check")</span></span>|
    |<span data-ttu-id="ccab4-116">Se et kort over en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en samtale.</span><span class="sxs-lookup"><span data-stu-id="ccab4-116">View a card of a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="ccab4-117">![markering](media/check.png "check")</span><span class="sxs-lookup"><span data-stu-id="ccab4-117">![check mark](media/check.png "check")</span></span>||
    |<span data-ttu-id="ccab4-118">Se flere oplysninger om et kort for en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en samtale.</span><span class="sxs-lookup"><span data-stu-id="ccab4-118">View more details of card for a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="ccab4-119">![markering](media/check.png "check")</span><span class="sxs-lookup"><span data-stu-id="ccab4-119">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="ccab4-120">![markering](media/check.png "check")</span><span class="sxs-lookup"><span data-stu-id="ccab4-120">![check mark](media/check.png "check")</span></span>|

- <span data-ttu-id="ccab4-121">Tillad URL-prøveversion</span><span class="sxs-lookup"><span data-stu-id="ccab4-121">Allow URL previews</span></span>

    <span data-ttu-id="ccab4-122">**Indstillingen Tillad URL-prøveversion** skal være aktiveret.</span><span class="sxs-lookup"><span data-stu-id="ccab4-122">**Allow URL previews** policy setting must be turned on.</span></span> <span data-ttu-id="ccab4-123">I modsat fald kan der ikke oprettes et kort til Business Central-links, der er indsat i en samtale med Teams.</span><span class="sxs-lookup"><span data-stu-id="ccab4-123">Otherwise, a card can't be generated for Business Central links pasted into a Teams conversation.</span></span> <span data-ttu-id="ccab4-124">Du kan finde flere oplysninger om denne indstilling under [Administrér meddelelsespolitikker i Teams](/microsoftteams/messaging-policies-in-teams).</span><span class="sxs-lookup"><span data-stu-id="ccab4-124">For more information about this setting, see [Manage messaging policies in Teams](/microsoftteams/messaging-policies-in-teams).</span></span>

### <a name="managing-the-business-central-app-optional"></a><span data-ttu-id="ccab4-125">Administration af Business Central-app (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="ccab4-125">Managing the Business Central app (optional)</span></span>

<span data-ttu-id="ccab4-126">Som Teams-administrator kan du administrere alle apps for din organisation, herunder [!INCLUDE [prodshort](includes/prodshort.md)]-appen.</span><span class="sxs-lookup"><span data-stu-id="ccab4-126">As a Teams administrator, you can manage all apps for your organization, including the [!INCLUDE [prodshort](includes/prodshort.md)] app.</span></span> <span data-ttu-id="ccab4-127">Du kan godkende eller installere [!INCLUDE [prodshort](includes/prodshort.md)]-appen for din organisation, blokere bruger fra installation af appen og meget mere.</span><span class="sxs-lookup"><span data-stu-id="ccab4-127">You can approve or install the [!INCLUDE [prodshort](includes/prodshort.md)] app for your organization, block user's from installing the app, and more.</span></span>

<span data-ttu-id="ccab4-128">Du kan finde flere oplysninger i følgende artikler i Microsoft Teams-dokumentationen:</span><span class="sxs-lookup"><span data-stu-id="ccab4-128">For more information, see the following articles in the Microsoft Teams documentation:</span></span>

- [<span data-ttu-id="ccab4-129">Administrer dine apps i Microsoft Teams Administration</span><span class="sxs-lookup"><span data-stu-id="ccab4-129">Manage your apps in the Microsoft Teams admin center</span></span>](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [<span data-ttu-id="ccab4-130">Administrer politikker for app-opsætning i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ccab4-130">Manage app setup policies in Microsoft Teams</span></span>](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a><span data-ttu-id="ccab4-131">I [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="ccab4-131">In [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="ccab4-132">Minimumkrav</span><span class="sxs-lookup"><span data-stu-id="ccab4-132">Minimum requirements</span></span>

- <span data-ttu-id="ccab4-133">[!INCLUDE [prodshort](includes/prodshort.md)] version:</span><span class="sxs-lookup"><span data-stu-id="ccab4-133">[!INCLUDE [prodshort](includes/prodshort.md)] version:</span></span>

    <span data-ttu-id="ccab4-134">[!INCLUDE [prodshort](includes/prodshort.md)] 2020 release Wave 2 (version 17) eller nyere.</span><span class="sxs-lookup"><span data-stu-id="ccab4-134">[!INCLUDE [prodshort](includes/prodshort.md)] 2020 release wave 2 (version 17) or later.</span></span> <span data-ttu-id="ccab4-135">Teams-integration understøttes kun [!INCLUDE [prodshort](includes/prodshort.md)] online, men ikke lokalt.</span><span class="sxs-lookup"><span data-stu-id="ccab4-135">Teams integration is only supported for [!INCLUDE [prodshort](includes/prodshort.md)] online; not on-premises.</span></span>

- <span data-ttu-id="ccab4-136">Kode enhed **2718 Page Summary Provider** udgives som en webtjeneste:</span><span class="sxs-lookup"><span data-stu-id="ccab4-136">Codeunit **2718 Page Summary Provider** is published as a web service:</span></span>

    <span data-ttu-id="ccab4-137">Denne codeunit er som standard udgivet som en webtjeneste.</span><span class="sxs-lookup"><span data-stu-id="ccab4-137">This codeunit is published as a web service by default.</span></span> <span data-ttu-id="ccab4-138">Codeunit er en del af [!INCLUDE [prodshort](includes/prodshort.md)]-systemprogrammet.</span><span class="sxs-lookup"><span data-stu-id="ccab4-138">The codeunit is part of the [!INCLUDE [prodshort](includes/prodshort.md)] system application.</span></span> <span data-ttu-id="ccab4-139">Den bruges til at hente feltdataene til en [!INCLUDE [prodshort](includes/prodshort.md)]-side, der er føjet til en Teams-samtale.</span><span class="sxs-lookup"><span data-stu-id="ccab4-139">It's used to get the field data for a [!INCLUDE [prodshort](includes/prodshort.md)] page added to a Teams conversation.</span></span> 

- <span data-ttu-id="ccab4-140">Brugerrettigheder:</span><span class="sxs-lookup"><span data-stu-id="ccab4-140">User permissions:</span></span>

    <span data-ttu-id="ccab4-141">De sider og data, som brugerne kan få vist og redigere i en Teams-samtale, kontrolleres oftest af deres tilladelser i [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="ccab4-141">For the most part, the pages and data that users can view and edit in a Teams conversation is controlled by their permissions in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>
    
    - <span data-ttu-id="ccab4-142">Hvis du vil indsætte et [!INCLUDE [prodshort](includes/prodshort.md)]-hyperlink i en Teams-samtale og få den på et kort, skal brugerne som minimum have læsetilladelse til siden og dens data.</span><span class="sxs-lookup"><span data-stu-id="ccab4-142">To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, users must have at least read permission on the page and its data.</span></span>
    - <span data-ttu-id="ccab4-143">Når et kort er sendt til en samtale, kan alle brugere i denne samtale se dette kort uden tilladelse til Business Central.</span><span class="sxs-lookup"><span data-stu-id="ccab4-143">Once a card is submitted into a conversation, any user in that conversation can view that card without permission to Business Central.</span></span>
    - <span data-ttu-id="ccab4-144">Hvis du vil have vist flere detaljer om et kort eller åbne posten i [!INCLUDE [prodshort](includes/prodshort.md)], skal brugere have læsetilladelse til siden og dens data.</span><span class="sxs-lookup"><span data-stu-id="ccab4-144">To view more details for a card or open the record in [!INCLUDE [prodshort](includes/prodshort.md)], users must have read permission on the page and its data.</span></span>
    - <span data-ttu-id="ccab4-145">Hvis du vil ændre data, skal brugerens behov redigeres.</span><span class="sxs-lookup"><span data-stu-id="ccab4-145">To change data, user's need modify permissions.</span></span>
    
    <span data-ttu-id="ccab4-146">Du kan finde flere oplysninger om rettigheder i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="ccab4-146">For information about permissions, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ccab4-147">Se også</span><span class="sxs-lookup"><span data-stu-id="ccab4-147">See Also</span></span>
[<span data-ttu-id="ccab4-148">Business Central og Microsoft Teams Oversigt over integration</span><span class="sxs-lookup"><span data-stu-id="ccab4-148">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="ccab4-149">[Installér appen [!INCLUDE [prodshort](includes/prodshort.md)] til Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="ccab4-149">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="ccab4-150">Udvikling af Teams-integration</span><span class="sxs-lookup"><span data-stu-id="ccab4-150">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="ccab4-151">Introduktion</span><span class="sxs-lookup"><span data-stu-id="ccab4-151">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
