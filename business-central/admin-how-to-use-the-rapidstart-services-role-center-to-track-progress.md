---
title: Sådan bruges rollecenteret RapidStart Services-implementering | Microsoft Docs
description: Når du bruger RapidStart Services, anbefales du at registrere dit arbejde og bruge rollecenteret RapidStart Services-implementering, som indeholder den korrekte kontekst til dit konfigurationsarbejde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: /dynamics365/business-central/admin-set-up-company-configuration
ROBOTS: NOINDEX
ms.openlocfilehash: 908e460ae5a3fc8ecb804f27363a1cfad71d997c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307920"
---
# <a name="use-the-rapidstart-services-implementer-role-center"></a><span data-ttu-id="275e7-103">Bruge rollecenteret RapidStart Services-implementering</span><span class="sxs-lookup"><span data-stu-id="275e7-103">Use the RapidStart Services Implementer Role Center</span></span>
<span data-ttu-id="275e7-104">Når du bruger RapidStart Services, anbefales du at bruge rollecenteret RapidStart Services-implementering, som indeholder den korrekte kontekst til dit konfigurationsarbejde.</span><span class="sxs-lookup"><span data-stu-id="275e7-104">When you use RapidStart Services, we recommend that you use the RapidStart Services Implementer Role Center as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="275e7-105">Du kan finde flere oplysninger under [Sådan ændres rollen](ui-change-basic-settings.md#to-change-the-role).</span><span class="sxs-lookup"><span data-stu-id="275e7-105">For more information, see [To change the role](ui-change-basic-settings.md#to-change-the-role).</span></span>

<span data-ttu-id="275e7-106">Når du fortsætter med dit arbejde, kan du tildele hver tabel den status, som afspejler, hvor du befinder dig i processen.</span><span class="sxs-lookup"><span data-stu-id="275e7-106">As you continue with your work, you can assign each table the status that reflects where you are in the process.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="275e7-107">holder derefter styr på status for tabellen i delen **Aktiviteter** i rollecenteret.</span><span class="sxs-lookup"><span data-stu-id="275e7-107">then keeps track of the table status in the **Activities** part on the Role Center.</span></span>  

<span data-ttu-id="275e7-108">Når du føjer en tabel til konfigurationsregnearket, angives dens status til tom.</span><span class="sxs-lookup"><span data-stu-id="275e7-108">By default, when you add a table to the configuration worksheet, its status is set to blank.</span></span> <span data-ttu-id="275e7-109">Det betyder, at konfigurationen af tabellen ikke er startet.</span><span class="sxs-lookup"><span data-stu-id="275e7-109">This means that configuration of the table has not begun.</span></span> <span data-ttu-id="275e7-110">Dette afspejles i tælleren **Ikke startet** i feltet **Aktiviteter**.</span><span class="sxs-lookup"><span data-stu-id="275e7-110">This is reflected in the **Not Started** count in the **Activities** tile.</span></span>  

## <a name="to-update-the-status-of-a-configuration-table"></a><span data-ttu-id="275e7-111">Opdatere status for en konfigurationstabel</span><span class="sxs-lookup"><span data-stu-id="275e7-111">To update the status of a configuration table</span></span>  
1.  <span data-ttu-id="275e7-112">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="275e7-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="275e7-113">Vælg handlingen **Rediger liste**.</span><span class="sxs-lookup"><span data-stu-id="275e7-113">Choose the **Edit List** action.</span></span>  
3.  <span data-ttu-id="275e7-114">Vælg en tabel, og vælg den relevante status i feltet **Status**.</span><span class="sxs-lookup"><span data-stu-id="275e7-114">Select a table, and in the **Status** field, choose the appropriate status.</span></span>  
4.  <span data-ttu-id="275e7-115">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="275e7-115">Choose the **OK** button.</span></span>  

<span data-ttu-id="275e7-116">Når du vender tilbage til rollecenteret, opdateres felterne i delen **Aktiviteter**, så de afspejler dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="275e7-116">When you return to the Role Center, the tiles in the **Activities** part are updated to reflect your changes.</span></span>  

## <a name="to-track-the-status-of-a-configuration-project"></a><span data-ttu-id="275e7-117">Spore status for et konfigurationsprojekt</span><span class="sxs-lookup"><span data-stu-id="275e7-117">To track the status of a configuration project</span></span>  
- <span data-ttu-id="275e7-118">Åbn rollecentret RapidStart Services.</span><span class="sxs-lookup"><span data-stu-id="275e7-118">Open the RapidStart Services Role Center.</span></span>  

<span data-ttu-id="275e7-119">I delen **Konfigurationsområder** vises fuldførelsesstatistikker for de områder og grupper, du har konfigureret.</span><span class="sxs-lookup"><span data-stu-id="275e7-119">In the **Configuration Areas** part, completion statistics are shown for the areas and groups that you have set up.</span></span> <span data-ttu-id="275e7-120">Hvis du ikke har oprettet nogen grupper eller områder, har denne del ingen data.</span><span class="sxs-lookup"><span data-stu-id="275e7-120">If you have not set up any groups or areas, this part has no data.</span></span>  

## <a name="to-see-a-filtered-view-of-table-status"></a><span data-ttu-id="275e7-121">Se en filtreret visning af tabellens status</span><span class="sxs-lookup"><span data-stu-id="275e7-121">To see a filtered view of table status</span></span>  
1. <span data-ttu-id="275e7-122">Vælg handlingen **Tabeller**.</span><span class="sxs-lookup"><span data-stu-id="275e7-122">Choose the **Tables** action.</span></span>  
2. <span data-ttu-id="275e7-123">Vælg den relevante filtrerede visning.</span><span class="sxs-lookup"><span data-stu-id="275e7-123">Select the appropriate filtered view.</span></span>  

## <a name="see-also"></a><span data-ttu-id="275e7-124">Se også</span><span class="sxs-lookup"><span data-stu-id="275e7-124">See Also</span></span>  
[<span data-ttu-id="275e7-125">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="275e7-125">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="275e7-126">Opsætning</span><span class="sxs-lookup"><span data-stu-id="275e7-126">Administration</span></span>](admin-setup-and-administration.md)
