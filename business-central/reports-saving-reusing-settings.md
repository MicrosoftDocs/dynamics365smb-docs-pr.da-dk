---
title: Anvende og ændre gemte indstillinger i rapporter | Microsoft Docs
description: Beskriver foruddefinerede indstillinger og filtre, der bruges til at tilpasse en rapport og til at generere de korrekte data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 70b3f391c141aa53dcef258a131d6395782a4488
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392545"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><span data-ttu-id="710c6-103">Administrere gemte indstillinger for rapporter og kørsler</span><span class="sxs-lookup"><span data-stu-id="710c6-103">Manage Saved Settings for Reports and Batch jobs</span></span>
<span data-ttu-id="710c6-104">Når brugerne kører rapporter, får de normalt vist en side, hvor de kan vælge indstillinger og angive filtre for at ændre, hvilke data der skal medtages i den genererede rapport.</span><span class="sxs-lookup"><span data-stu-id="710c6-104">When running reports, users are typically presented with a page that lets them select options and set filters to change the data that is included in the generated report.</span></span> <span data-ttu-id="710c6-105">Denne side kaldes anmodningssiden.</span><span class="sxs-lookup"><span data-stu-id="710c6-105">This page is called the request page.</span></span> <span data-ttu-id="710c6-106">En rapport kan medtage én eller flere *gemte indstillinger*, som brugerne kan anvende til rapporten fra anmodningssiden.</span><span class="sxs-lookup"><span data-stu-id="710c6-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="710c6-107">*Gemte indstillinger* er grundlæggende foruddefinerede indstillinger og filtre.</span><span class="sxs-lookup"><span data-stu-id="710c6-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="710c6-108">Med gemte indstillinger kan du hurtigt og pålideligt generere ensartede rapporter, der indeholder de korrekte data.</span><span class="sxs-lookup"><span data-stu-id="710c6-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="710c6-109">Du kan finde flere oplysninger under [Bruge gemte indstillinger](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="710c6-109">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

> [!NOTE]
> <span data-ttu-id="710c6-110">I dette emne omtales hovedsageligt "rapport", men lignende oplysninger gælder for kørsler.</span><span class="sxs-lookup"><span data-stu-id="710c6-110">This topic refers mainly to "report", but similar information applies to batch jobs.</span></span>

<span data-ttu-id="710c6-111">Hvis du har de nødvendige tilladelser, kan du få vist, oprette og redigere de gemte indstillinger for alle rapporter for alle brugere i en virksomhed.</span><span class="sxs-lookup"><span data-stu-id="710c6-111">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in a company.</span></span> <span data-ttu-id="710c6-112">Du kan tildele gemte indstillinger for en rapport til enkelte brugere eller til alle brugere i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="710c6-112">You can assign saved settings for a report to individual users or to all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="710c6-113">Sådan oprettes og redigeres gemte indstillinger for alle brugere</span><span class="sxs-lookup"><span data-stu-id="710c6-113">To create and modify saved settings for all users</span></span>
<span data-ttu-id="710c6-114">Du administrerer gemte indstillinger på siden **Rapportindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="710c6-114">You manage saved settings on the **Reports Settings** page.</span></span> <span data-ttu-id="710c6-115">Du kan åbne siden på to måder:</span><span class="sxs-lookup"><span data-stu-id="710c6-115">There are two ways to open this page:</span></span>
-   <span data-ttu-id="710c6-116">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rapportindstillinger**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="710c6-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="710c6-117">Åbn en rapport, vælg opslaget i feltet **Brug standardværdier fra**, og vælg derefter handlingen **Vælg fra komplet liste**.</span><span class="sxs-lookup"><span data-stu-id="710c6-117">Open a report, choose the lookup in the **Use default values from** field, and then choose the **Select from full list** action.</span></span>

<span data-ttu-id="710c6-118">Siden viser alle eksisterende poster for gemte indstillinger for alle brugere.</span><span class="sxs-lookup"><span data-stu-id="710c6-118">The page displays all the existing saved settings entries for all users.</span></span> <span data-ttu-id="710c6-119">Hvis der er et brugernavn i feltet **Tildelt til**, er det kun denne bruger, der kan bruge de gemte indstillinger for den tilknyttede rapport.</span><span class="sxs-lookup"><span data-stu-id="710c6-119">If there is a user name in the **Assigned to** field, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="710c6-120">Hvis der er en markering i feltet **Del med alle brugere**, kan alle brugere anvende de gemte indstillinger for rapporten.</span><span class="sxs-lookup"><span data-stu-id="710c6-120">If there is a check mark in the **Share with all users** field, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="710c6-121">Fra siden **Rapportindstillinger** kan du:</span><span class="sxs-lookup"><span data-stu-id="710c6-121">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="710c6-122">Vælge handlingen **Ny** for at oprette en ny post for gemte indstillinger fra bunden.</span><span class="sxs-lookup"><span data-stu-id="710c6-122">Choose the **New** action to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="710c6-123">Vælg en post for gemte indstillinger på listen, og vælg handlingen **Kopiér** for at oprette en kopi.</span><span class="sxs-lookup"><span data-stu-id="710c6-123">Select a saved settings entry from the list, and choose the **Copy** action to create a copy.</span></span>
-   <span data-ttu-id="710c6-124">Vælg en post for gemte indstillinger på listen, og vælg handlingen **Rediger** for at ændre en post for gemte indstillinger.</span><span class="sxs-lookup"><span data-stu-id="710c6-124">Select a saved settings entry from the list, and choose the **Edit** action to modify a saved settings entry.</span></span>

> [!Important]
> <span data-ttu-id="710c6-125">Overvej, hvilket navn du giver en post for gemte indstillinger.</span><span class="sxs-lookup"><span data-stu-id="710c6-125">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="710c6-126">Hvis du opretter en post for gemte indstillinger for alle brugere, og du giver den samme navn som en eksisterende post for gemte indstillinger, som er tildelt til en bestemt bruger, kan den pågældende bruger ikke anvende den post for gemte indstillinger, der er tildelt til alle.</span><span class="sxs-lookup"><span data-stu-id="710c6-126">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="710c6-127">I sektionen **Gemte indstillinger** på rapportanmodningssiden får brugeren vist to poster for gemte indstillinger med det samme navn.</span><span class="sxs-lookup"><span data-stu-id="710c6-127">In the **Saved Settings** section on the request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="710c6-128">Men uanset hvilken indstilling brugeren vælger, anvendes den brugerspecifikke post for gemte indstillinger.</span><span class="sxs-lookup"><span data-stu-id="710c6-128">However, no matter which option they choose, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="710c6-129">Funktionen Gemte indstillinger for rapporter er kun tilgængelig, når egenskaben [SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) for rapportens anmodningsside er indstillet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="710c6-129">The Saved Settings feature is available only on reports where the [SaveValues property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) of the report's request page is set to **Yes**.</span></span> <span data-ttu-id="710c6-130">Egenskaben **SaveValues** indstilles i udviklingsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="710c6-130">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="710c6-131">Se også</span><span class="sxs-lookup"><span data-stu-id="710c6-131">See Also</span></span>
[<span data-ttu-id="710c6-132">Arbejde med rapporter, kørsler og XMLporte</span><span class="sxs-lookup"><span data-stu-id="710c6-132">Working with Reports, Batch Jobs, and XMLports</span></span>](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]