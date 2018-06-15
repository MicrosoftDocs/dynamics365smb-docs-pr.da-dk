---
title: Konfiguration af API-skabeloner | Microsoft Docs
description: "Beskriver de trin, du skal udføre for at konfigurere API-skabeloner til Dynamics 365 Business Central."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 05/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 1695a6950dabc1b2f0a2f85ad9e0c565012c92e1
ms.contentlocale: da-dk
ms.lasthandoff: 05/17/2018

---

# <a name="configuring-api-templates"></a><span data-ttu-id="d5b10-103">Konfiguration af API-skabeloner</span><span class="sxs-lookup"><span data-stu-id="d5b10-103">Configuring API Templates</span></span>
<span data-ttu-id="d5b10-104">API-biblioteket til [!INCLUDE[d365fin_md](includes/d365fin_md.md)] giver en forenklet fremstilling af de underliggende objekter.</span><span class="sxs-lookup"><span data-stu-id="d5b10-104">The API library for [!INCLUDE[d365fin_md](includes/d365fin_md.md)] provides a simplified representation of the underlying entities.</span></span> <span data-ttu-id="d5b10-105">Det er ikke alle egenskaber i programmet, der vises ved hjælp af den tilknyttede API.</span><span class="sxs-lookup"><span data-stu-id="d5b10-105">All the properties in the application are not exposed through the associated API.</span></span> <span data-ttu-id="d5b10-106">I vinduet **API-opsætning** kan du definere skabeloner, der bruges til at angive tomme egenskaber for en enhed, når du opretter en BOGF-handling via API'et.</span><span class="sxs-lookup"><span data-stu-id="d5b10-106">The **API Setup** window allows you to define templates that are used to populate empty properties on an entity when you create a POST action through the API.</span></span> 

<span data-ttu-id="d5b10-107">Hvis en konfigurationsskabelon defineres for vareobjektet, når der oprettes en ny post ved hjælp af varer-API'et, bliver egenskaber for den nye vare, der ikke er defineret i API-kaldet, f.eks. udfyldt med oplysninger fra den valgte skabelon.</span><span class="sxs-lookup"><span data-stu-id="d5b10-107">For example, if a configuration template is defined for the item entity, when a new item record is created through the items API, any properties for the new item that are not defined in the API call will be populated from the selected template.</span></span> <span data-ttu-id="d5b10-108">Hvis der f.eks. ikke er angivet en værdi i feltet **Produktbogføringsgruppe** ved hjælp af API'et, men der er angivet en værdi i den valgte skabelon, bliver værdien for bogføringsgruppen i skabelonen anvendt på den nye vare.</span><span class="sxs-lookup"><span data-stu-id="d5b10-108">If, for example, no value is defined for the **Gen. Prod. Posting Group** field through the API, but a value is defined in the selected template, then the posting group value defined in the template will be applied to the new item.</span></span> 

## <a name="setting-up-the-entity-template"></a><span data-ttu-id="d5b10-109">Opsætning af enhedsskabelonen</span><span class="sxs-lookup"><span data-stu-id="d5b10-109">Setting up the Entity Template</span></span>
<span data-ttu-id="d5b10-110">Hvis du vil bruge skabeloner med API-biblioteket, skal du først oprette og definere egenskaber for skabelonerne.</span><span class="sxs-lookup"><span data-stu-id="d5b10-110">To use templates with the API library, you must first set up and define properties for the templates.</span></span> <span data-ttu-id="d5b10-111">Du kan oprette skabelonerne i vinduet **Konfigurationsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="d5b10-111">You can set up these templates in the **Configuration Templates** window.</span></span> <span data-ttu-id="d5b10-112">Du kan finde flere oplysninger i [Forberede overflytning af debitordata](admin-use-templates-to-prepare-customer-data-for-migration.md).</span><span class="sxs-lookup"><span data-stu-id="d5b10-112">For more information, see [Prepare to Migrate Customer Data](admin-use-templates-to-prepare-customer-data-for-migration.md).</span></span> 

## <a name="assign-the-template-to-an-api"></a><span data-ttu-id="d5b10-113">Tildele skabelonen til et API</span><span class="sxs-lookup"><span data-stu-id="d5b10-113">Assign the template to an API</span></span>

<span data-ttu-id="d5b10-114">Hvis du vil tildele en skabelon til en API, skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="d5b10-114">To assign a template to an API, you must go through the following steps.</span></span>

1. <span data-ttu-id="d5b10-115">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **API-opsætning**, og vælg det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d5b10-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **API Setup**, and choose the related link.</span></span>
2. <span data-ttu-id="d5b10-116">Vælg **Ny**, og vælg derefter **Rækkefølge**-værdien for posten.</span><span class="sxs-lookup"><span data-stu-id="d5b10-116">Choose **New**, and then choose the **Order** value for the record.</span></span>  
<span data-ttu-id="d5b10-117">Hvis der er valgt mere end én skabelon for et API (side-id), anvendes skabelonerne i den rækkefølge, der er defineret i kolonnen **Rækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="d5b10-117">If there is more than one template selected for an API (Page ID), the templates are applied in the order defined in the **Order** column.</span></span>   
<span data-ttu-id="d5b10-118">Når hver skabelon anvendes, anvendes feltværdier, der er defineret i skabelonen, kun til felter, der ikke allerede har en defineret værdi, enten direkte i API'et eller i en tidligere anvendt skabelon i rækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="d5b10-118">When each template is applied, field values defined in the template are only applied to fields that have not already had a value defined, either explicitly in the API, or in a previously applied template in the order.</span></span> 
3. <span data-ttu-id="d5b10-119">Vælg en værdi for **Side-id**:</span><span class="sxs-lookup"><span data-stu-id="d5b10-119">Select a **Page ID** value.</span></span>  
<span data-ttu-id="d5b10-120">Dette er siden for det API, som skabelonen skal anvendes på.</span><span class="sxs-lookup"><span data-stu-id="d5b10-120">This is the page for the API to which the template will be applied.</span></span> <span data-ttu-id="d5b10-121">**Side-ID**-opslaget indeholder en oversigt over alle API'er, der er tilgængelige i biblioteket.</span><span class="sxs-lookup"><span data-stu-id="d5b10-121">The **Page ID** lookup provides a list of all APIs available in the library.</span></span>
4. <span data-ttu-id="d5b10-122">Vælg en værdi i feltet **Skabelonkode**.</span><span class="sxs-lookup"><span data-stu-id="d5b10-122">Select a value in the **Template Code** field.</span></span>  
<span data-ttu-id="d5b10-123">Skabelonkoden er koden for den skabelon, der blev defineret i vinduet **Konfigurationsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="d5b10-123">The template code is the code for the template that was defined in the **Configuration Templates** window.</span></span> <span data-ttu-id="d5b10-124">De definerede skabelonværdier anvendes på API'et.</span><span class="sxs-lookup"><span data-stu-id="d5b10-124">The template values defined are applied to the API.</span></span> 
5. <span data-ttu-id="d5b10-125">I feltet **Betingelser** skal du angive, hvilken skabelon der skal anvendes.</span><span class="sxs-lookup"><span data-stu-id="d5b10-125">In the **Conditions** field, specify which template should be applied.</span></span>  
<span data-ttu-id="d5b10-126">Den definerede skabelon anvendes på en ny post, der oprettes via API'et, hvis og kun hvis de betingelser, der er defineret i feltet **Betingelser**, opfyldes af de værdier, der allerede er defineret for den nye forekomst af enheden.</span><span class="sxs-lookup"><span data-stu-id="d5b10-126">The defined template is applied to a new record created through the API if, and only if, the conditions defined in the **Conditions** field are met by the values already defined for the new instance of the entity.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5b10-127">Se også</span><span class="sxs-lookup"><span data-stu-id="d5b10-127">See Also</span></span>
[<span data-ttu-id="d5b10-128">API-dokumentation</span><span class="sxs-lookup"><span data-stu-id="d5b10-128">API Documentation</span></span>](/dynamics-nav/fin-graph)  
<span data-ttu-id="d5b10-129">[Udvikle Connect-apps til [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span><span class="sxs-lookup"><span data-stu-id="d5b10-129">[Developing Connect Apps for [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span></span>  
[<span data-ttu-id="d5b10-130">Aktivere API'erne</span><span class="sxs-lookup"><span data-stu-id="d5b10-130">Enabling the APIs</span></span>](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[<span data-ttu-id="d5b10-131">Slutpunkter for API'erne</span><span class="sxs-lookup"><span data-stu-id="d5b10-131">Endpoints for the APIs</span></span>](/dynamics-nav/endpoints-apis-for-dynamics)  
[<span data-ttu-id="d5b10-132">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="d5b10-132">Setting Up a Company with RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="d5b10-133">Opsætning</span><span class="sxs-lookup"><span data-stu-id="d5b10-133">Administration</span></span>](admin-setup-and-administration.md)
