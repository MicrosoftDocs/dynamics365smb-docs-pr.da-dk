---
title: Anvende og ændre gemte indstillinger i rapporter | Microsoft Docs
description: Beskriver foruddefinerede indstillinger og filtre, der bruges til at tilpasse en rapport og til at generere de korrekte data.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 3e7b00d54a9c655a77b7b7f4854e59993866427e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251212"
---
# <a name="managing-saved-settings-on-reports"></a><span data-ttu-id="f0e59-103">Administrere gemte indstillinger i rapporter</span><span class="sxs-lookup"><span data-stu-id="f0e59-103">Managing Saved Settings on Reports</span></span>
<span data-ttu-id="f0e59-104">Når brugerne kører en rapport, får de normalt vist en side, hvor de kan angive bestemte indstillinger og filtre for at ændre, hvilke data der skal medtages i den genererede rapport.</span><span class="sxs-lookup"><span data-stu-id="f0e59-104">When running a reports, users are typically presented with a page that lets them set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="f0e59-105">Denne side kaldes rapportanmodningssiden.</span><span class="sxs-lookup"><span data-stu-id="f0e59-105">This page is called the report request page.</span></span> <span data-ttu-id="f0e59-106">En rapport kan medtage én eller flere *gemte indstillinger*, som brugerne kan anvende til rapporten fra anmodningssiden.</span><span class="sxs-lookup"><span data-stu-id="f0e59-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="f0e59-107">*Gemte indstillinger* er grundlæggende foruddefinerede indstillinger og filtre.</span><span class="sxs-lookup"><span data-stu-id="f0e59-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="f0e59-108">Med gemte indstillinger kan du hurtigt og pålideligt generere ensartede rapporter, der indeholder de korrekte data.</span><span class="sxs-lookup"><span data-stu-id="f0e59-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="f0e59-109">Du kan finde flere oplysninger om, hvordan gemte indstillinger bruges, under [Bruge gemte indstillinger](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="f0e59-109">For more information about how saved settings are used, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="f0e59-110">Hvis du har de nødvendige tilladelser, kan du få vist, oprette og redigere de gemte indstillinger for alle rapporter for alle brugere i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="f0e59-110">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="f0e59-111">Du kan tildele gemte indstillinger for en rapport til enkelte brugere eller alle brugere i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="f0e59-111">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="f0e59-112">Oprette og redigere gemte indstillinger for alle brugere</span><span class="sxs-lookup"><span data-stu-id="f0e59-112">Create and modify saved settings for all users</span></span>
<span data-ttu-id="f0e59-113">Du administrerer gemte indstillinger fra siden **1560 Rapportindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="f0e59-113">You manage saved settings from page **1560 Reports Settings**.</span></span> <span data-ttu-id="f0e59-114">Du kan åbne siden på to måder:</span><span class="sxs-lookup"><span data-stu-id="f0e59-114">There are two ways to open this page:</span></span>
-   <span data-ttu-id="f0e59-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rapportindstillinger**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f0e59-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="f0e59-116">Åbn en rapport, vælg opslaget ud for feltet **Brug standardværdier fra:** og vælg **Vælg fra komplet liste**.</span><span class="sxs-lookup"><span data-stu-id="f0e59-116">Open a report, choose the lookup next to the **Used default values from:** box, choose **Select from full list**.</span></span>

<span data-ttu-id="f0e59-117">Siden viser alle eksisterende Gem indstillinger-poster for alle brugere.</span><span class="sxs-lookup"><span data-stu-id="f0e59-117">The page displays all the existing save settings entries for all users.</span></span> <span data-ttu-id="f0e59-118">Hvis der er et brugernavn i kolonnen **Tildelt til**, er det kun denne bruger, der kan bruge de gemte indstillinger for den tilknyttede rapport.</span><span class="sxs-lookup"><span data-stu-id="f0e59-118">If there is a user name in the **Assigned to** column, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="f0e59-119">Hvis der er en markering i kolonnen **Del med alle brugere**, kan alle brugere anvende de gemte indstillinger for rapporten.</span><span class="sxs-lookup"><span data-stu-id="f0e59-119">If there is a check mark in the **Share with all users** column, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="f0e59-120">Fra siden **Rapportindstillinger** kan du:</span><span class="sxs-lookup"><span data-stu-id="f0e59-120">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="f0e59-121">Vælge **Ny** for at oprette en ny post for gemte indstillinger fra bunden.</span><span class="sxs-lookup"><span data-stu-id="f0e59-121">Choose **New** to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="f0e59-122">Vælg en post for gemte indstillinger på listen, og vælg **Kopier** for at oprette en kopi.</span><span class="sxs-lookup"><span data-stu-id="f0e59-122">Select a saved settings entry from the list, and choose **Copy** to create a copy.</span></span>
-   <span data-ttu-id="f0e59-123">Vælg en post for gemte indstillinger på listen, og vælg **Rediger** for at ændre en post for gemte indstillinger.</span><span class="sxs-lookup"><span data-stu-id="f0e59-123">Select a saved settings entry from the list, and choose **Edit** to modify a saved settings entry.</span></span>


> [!Important]
> <span data-ttu-id="f0e59-124">Overvej, hvilket navn du giver en post for gemte indstillinger.</span><span class="sxs-lookup"><span data-stu-id="f0e59-124">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="f0e59-125">Hvis du opretter en post for gemte indstillinger for alle brugere, og du giver den samme navn som en eksisterende post for gemte indstillinger, som er tildelt til en bestemt bruger, kan den pågældende bruger ikke anvende den post for gemte indstillinger, der er tildelt til alle.</span><span class="sxs-lookup"><span data-stu-id="f0e59-125">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="f0e59-126">Under **Gemte indstillinger** på rapportanmodningssiden får brugeren vist to poster for gemte indstillinger med det samme navn.</span><span class="sxs-lookup"><span data-stu-id="f0e59-126">Under **Saved Settings** on the report request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="f0e59-127">Men uanset hvilken indstilling brugeren vælger, anvendes den brugerspecifikke post for gemte indstillinger.</span><span class="sxs-lookup"><span data-stu-id="f0e59-127">However, no matter which option he chooses, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="f0e59-128">Funktionen for gemte indstillinger for rapporter er kun tilgængelig, når [egenskaben SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) for rapportens anmodningsside er indstillet til `Yes`.</span><span class="sxs-lookup"><span data-stu-id="f0e59-128">The saved settings feature is available only on reports where the [SaveValues property](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) of the report's request page is set to `Yes`.</span></span> <span data-ttu-id="f0e59-129">Egenskaben **SaveValues** indstilles i udviklingsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="f0e59-129">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f0e59-130">Se også</span><span class="sxs-lookup"><span data-stu-id="f0e59-130">See Also</span></span>
[<span data-ttu-id="f0e59-131">Arbejde med rapporter og kørsler</span><span class="sxs-lookup"><span data-stu-id="f0e59-131">Working with Reports and Batch Jobs</span></span>](ui-work-report.md)  
