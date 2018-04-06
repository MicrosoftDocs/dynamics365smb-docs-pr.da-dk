---
title: "Sådan bruges RapidStart Services-rolleimplementeringscenter | Microsoft Docs"
description: "Når du bruger RapidStart Services, anbefales det, at du sporer dit arbejde og bruger RapidStart Services-rolleimplementeringscenter, som indeholder den korrekte kontekst til dit konfigurationsarbejde."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7d76daf62c46b0b7799ca9dd6be9acf83084b11d
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="use-the-rapidstart-services-implementer-role-center"></a><span data-ttu-id="adb2e-103">Bruge rollecenteret RapidStart Services-implementering</span><span class="sxs-lookup"><span data-stu-id="adb2e-103">Use the RapidStart Services Implementer Role Center</span></span>
<span data-ttu-id="adb2e-104">Når du bruger RapidStart Services, anbefales det, at du bruger rollecenteret RapidStart Services-implementering, som indeholder den korrekte kontekst til dit konfigurationsarbejde.</span><span class="sxs-lookup"><span data-stu-id="adb2e-104">When you use RapidStart Services, we recommend that you use the RapidStart Services Implementer Role Center as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="adb2e-105">Yderligere oplysninger finder du i afsnittet "Sådan ændres et rollecenter" i [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="adb2e-105">For more information, see the "To change Role Center" section in [Changing Basic Settings](ui-change-basic-settings.md).</span></span>

<span data-ttu-id="adb2e-106">Når du fortsætter med dit arbejde, kan du tildele hver tabel den status, som afspejler, hvor du befinder dig i processen.</span><span class="sxs-lookup"><span data-stu-id="adb2e-106">As you continue with your work, you can assign each table the status that reflects where you are in the process.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="adb2e-107"> holder derefter styr på status for tabellen i delen **Aktiviteter** i rollecenteret.</span><span class="sxs-lookup"><span data-stu-id="adb2e-107"> then keeps track of the table status in the **Activities** part on the Role Center.</span></span>  

<span data-ttu-id="adb2e-108">Når du føjer en tabel til konfigurationsregnearket, angives dens status til tom.</span><span class="sxs-lookup"><span data-stu-id="adb2e-108">By default, when you add a table to the configuration worksheet, its status is set to blank.</span></span> <span data-ttu-id="adb2e-109">Det betyder, at konfigurationen af tabellen ikke er startet.</span><span class="sxs-lookup"><span data-stu-id="adb2e-109">This means that configuration of the table has not begun.</span></span> <span data-ttu-id="adb2e-110">Dette afspejles i tælleren **Ikke startet** i feltet **Aktiviteter**.</span><span class="sxs-lookup"><span data-stu-id="adb2e-110">This is reflected in the **Not Started** count in the **Activities** tile.</span></span>  

## <a name="to-update-the-status-of-a-configuration-table"></a><span data-ttu-id="adb2e-111">Opdatere status for en konfigurationstabel</span><span class="sxs-lookup"><span data-stu-id="adb2e-111">To update the status of a configuration table</span></span>  
1.  <span data-ttu-id="adb2e-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Konfigurationsregneark**, og vælg det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="adb2e-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Configuration Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="adb2e-113">Vælg handlingen **Rediger liste**.</span><span class="sxs-lookup"><span data-stu-id="adb2e-113">Choose the **Edit List** action.</span></span>  
3.  <span data-ttu-id="adb2e-114">Vælg en tabel, og vælg den relevante status i feltet **Status**.</span><span class="sxs-lookup"><span data-stu-id="adb2e-114">Select a table, and in the **Status** field, choose the appropriate status.</span></span>  
4.  <span data-ttu-id="adb2e-115">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="adb2e-115">Choose the **OK** button.</span></span>  

<span data-ttu-id="adb2e-116">Når du vender tilbage til rollecenteret, opdateres felterne i delen **Aktiviteter**, så de afspejler dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="adb2e-116">When you return to the Role Center, the tiles in the **Activities** part are updated to reflect your changes.</span></span>  

## <a name="to-track-the-status-of-a-configuration-project"></a><span data-ttu-id="adb2e-117">Spore status for et konfigurationsprojekt</span><span class="sxs-lookup"><span data-stu-id="adb2e-117">To track the status of a configuration project</span></span>  
- <span data-ttu-id="adb2e-118">Åbn RapidStart Services-rollecenter.</span><span class="sxs-lookup"><span data-stu-id="adb2e-118">Open the RapidStart Services Role Center.</span></span>  

<span data-ttu-id="adb2e-119">I delen **Konfigurationsområder** vises fuldførelsesstatistikker for de områder og grupper, du har konfigureret.</span><span class="sxs-lookup"><span data-stu-id="adb2e-119">In the **Configuration Areas** part, completion statistics are shown for the areas and groups that you have set up.</span></span> <span data-ttu-id="adb2e-120">Hvis du ikke har oprettet nogen grupper eller områder, har denne del ingen data.</span><span class="sxs-lookup"><span data-stu-id="adb2e-120">If you have not set up any groups or areas, this part has no data.</span></span>  

## <a name="to-see-a-filtered-view-of-table-status"></a><span data-ttu-id="adb2e-121">Se en filtreret visning af tabellens status</span><span class="sxs-lookup"><span data-stu-id="adb2e-121">To see a filtered view of table status</span></span>  
1. <span data-ttu-id="adb2e-122">Vælg handlingen **Tabeller**.</span><span class="sxs-lookup"><span data-stu-id="adb2e-122">Choose the **Tables** action.</span></span>  
2. <span data-ttu-id="adb2e-123">Vælg den relevante filtrerede visning.</span><span class="sxs-lookup"><span data-stu-id="adb2e-123">Select the appropriate filtered view.</span></span>  

## <a name="see-also"></a><span data-ttu-id="adb2e-124">Se også</span><span class="sxs-lookup"><span data-stu-id="adb2e-124">See Also</span></span>  
[<span data-ttu-id="adb2e-125">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="adb2e-125">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="adb2e-126">Opsætning</span><span class="sxs-lookup"><span data-stu-id="adb2e-126">Administration</span></span>](admin-setup-and-administration.md)

