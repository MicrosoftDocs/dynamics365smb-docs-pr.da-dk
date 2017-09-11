---
title: "Anvende og ændre gemte indstillinger i rapporter | Microsoft Docs"
description: Beskriver foruddefinerede indstillinger og filtre, der bruges til at tilpasse en rapport og til at generere de korrekte data.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9e5f7417579a5ba0629032cf9fa664e0060b9cbf
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="saved-settings-on-reports"></a><span data-ttu-id="e12b5-103">Gemte indstillinger i rapporter</span><span class="sxs-lookup"><span data-stu-id="e12b5-103">Saved Settings on Reports</span></span>
<span data-ttu-id="e12b5-104">Afhængigt af den rapport, der køres, kan du få vist en side, hvor du kan angive bestemte indstillinger og filtre for at ændre, hvilke data der medtages i den genererede rapport.</span><span class="sxs-lookup"><span data-stu-id="e12b5-104">Depending on the report that is run, you might be presented with a page that lets you to set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="e12b5-105">Denne side kaldes rapportanmodningssiden.</span><span class="sxs-lookup"><span data-stu-id="e12b5-105">This page is known as the report request page.</span></span> <span data-ttu-id="e12b5-106">En rapport kan medtage én eller flere *gemte indstillinger*, som du kan anvende til rapporten fra anmodningssiden.</span><span class="sxs-lookup"><span data-stu-id="e12b5-106">A report can include one or more *saved settings* that you can apply to the report from the request page.</span></span> <span data-ttu-id="e12b5-107">*Gemte indstillinger* er grundlæggende foruddefinerede indstillinger og filtre.</span><span class="sxs-lookup"><span data-stu-id="e12b5-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="e12b5-108">Med gemte indstillinger kan du hurtigt og pålideligt generere ensartede rapporter, der indeholder de korrekte data.</span><span class="sxs-lookup"><span data-stu-id="e12b5-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span>

<span data-ttu-id="e12b5-109">Du kan se de gemte indstillinger, der er tilgængelige for en rapport, i afsnittet **Gemte indstillinger** på rapportanmodningssiden.</span><span class="sxs-lookup"><span data-stu-id="e12b5-109">You can see the saved settings that are available to you for a report in **Saved Settings** section of the report request page.</span></span>  

## <a name="to-apply-saved-settings-to-a-report"></a><span data-ttu-id="e12b5-110">Sådan anvendes gemte indstillinger til en rapport</span><span class="sxs-lookup"><span data-stu-id="e12b5-110">To apply saved settings to a report</span></span>
1. <span data-ttu-id="e12b5-111">Åbn rapporten.</span><span class="sxs-lookup"><span data-stu-id="e12b5-111">Open the report.</span></span>

   <span data-ttu-id="e12b5-112">Rapportanmodningssiden vises.</span><span class="sxs-lookup"><span data-stu-id="e12b5-112">The report request page appears.</span></span>    
2. <span data-ttu-id="e12b5-113">I sektionen **Gemte indstillinger** på siden skal du angive feltet **Navn** til de gemte indstillinger, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="e12b5-113">In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.</span></span>

   <span data-ttu-id="e12b5-114">Afsnittet **Gemte indstillinger** vises kun, hvis rapporten er blevet kørt før, eller hvis der findes poster for gemte indstillinger.</span><span class="sxs-lookup"><span data-stu-id="e12b5-114">The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries.</span></span> <span data-ttu-id="e12b5-115">Posten for gemte indstillinger, som kaldes **Sidst anvendte indstillinger og filtre**, er altid tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="e12b5-115">The saved settings entry called **Last used options and filters** is always available.</span></span> <span data-ttu-id="e12b5-116">Disse indstillinger er de værdier for indstillinger og filtre, som blev brugt, sidste gang du kørte rapporten.</span><span class="sxs-lookup"><span data-stu-id="e12b5-116">These settings are the option and filter values that were used the last time you ran the report.</span></span>

## <a name="administer-saved-report-settings-for-users"></a><span data-ttu-id="e12b5-117">Administrere gemte rapportindstillinger for brugere</span><span class="sxs-lookup"><span data-stu-id="e12b5-117">Administer saved report settings for users</span></span>
<span data-ttu-id="e12b5-118">Hvis du har de nødvendige tilladelser, kan du få vist, oprette og redigere de gemte indstillinger for alle rapporter for alle brugere i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="e12b5-118">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="e12b5-119">Du kan tildele gemte indstillinger for en rapport til enkelte brugere eller alle brugere i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="e12b5-119">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<span data-ttu-id="e12b5-120">Du administrerer gemte indstillinger fra side 1506 **Rapportindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="e12b5-120">You manage saved settings from page 1506 **Reports Settings**.</span></span> <span data-ttu-id="e12b5-121">Du åbner denne side ved at vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Rapportindstillinger** og derefter vælge det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e12b5-121">To open this page, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Settings**, and then choose the related link.</span></span>

<span data-ttu-id="e12b5-122">Fra siden **Rapportindstillinger** kan du oprette nye indstillinger fra bunden, eller du kan kopiere og redigere eksisterende indstillinger.</span><span class="sxs-lookup"><span data-stu-id="e12b5-122">From the **Report Settings** page, you can create a new settings from scratch or you can make a copy and modify existing settings.</span></span> <span data-ttu-id="e12b5-123">Hvis du vil ændre indstillinger og filtre for en indstilling, skal du vælge handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="e12b5-123">To modify the options and filters for a settings, choose the **Edit** action.</span></span>

<span data-ttu-id="e12b5-124">**Bemærk!**</span><span class="sxs-lookup"><span data-stu-id="e12b5-124">**Notes:**</span></span>

* <span data-ttu-id="e12b5-125">Funktionen for gemte indstillinger for rapporter er kun relevant, hvis egenskaben SaveValues for anmodningssiden er angivet til Ja.</span><span class="sxs-lookup"><span data-stu-id="e12b5-125">The saved settings feature on reports is only relevant when the SaveValues property of the request page is set to Yes.</span></span> <span data-ttu-id="e12b5-126">Egenskaben SaveValues angives i udviklingsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="e12b5-126">The SaveValues property property is set in the development environment.</span></span>
* <span data-ttu-id="e12b5-127">Hvis du opretter et element for gemte indstillinger for alle brugere, og det hedder det samme som en eksisterende gemt indstilling for en bestemt bruger, kan den pågældende bruger ikke anvende de gemte indstillinger, der er tildelt til alle.</span><span class="sxs-lookup"><span data-stu-id="e12b5-127">If you create a saved settings item for all users, and it has the same name as an existing saved settings for a specific user, then that user will not be able to use the saved settings that is assigned to everyone.</span></span>  <span data-ttu-id="e12b5-128">I feltet Gemte indstillinger på rapportanmodningssiden får brugeren vist to valgmuligheder for gemte indstillinger med det samme navn.</span><span class="sxs-lookup"><span data-stu-id="e12b5-128">In the Saved Settings field on the report request page, the user will see two saved settings options with the same name.</span></span> <span data-ttu-id="e12b5-129">Men uanset hvilken indstilling brugeren vælger, anvendes de brugerspecifikke gemte indstillinger.</span><span class="sxs-lookup"><span data-stu-id="e12b5-129">However, no matter which option he chooses, the user-specific saved settings will be used.</span></span>

## <a name="see-also"></a><span data-ttu-id="e12b5-130">Se også</span><span class="sxs-lookup"><span data-stu-id="e12b5-130">See Also</span></span>
[<span data-ttu-id="e12b5-131">Planlægge kørsel af en rapport</span><span class="sxs-lookup"><span data-stu-id="e12b5-131">Schedule a Rpeort to Run</span></span>](ui-schedule-report.md)  

