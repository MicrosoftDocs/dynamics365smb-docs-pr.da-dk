---
title: Administration af formål med adgang til databaser i Business Central | Microsoft Docs
description: Ændring af formålet til adgang til databaser for rapporter, API-sider og forespørgsler.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6d79f5b2851df85ea9f19faeeb941eccfd1b397b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752821"
---
# <a name="managing-database-access-intent"></a><span data-ttu-id="79cdc-103">Administration af formål med adgang til database</span><span class="sxs-lookup"><span data-stu-id="79cdc-103">Managing Database Access Intent</span></span> 

<span data-ttu-id="79cdc-104">Som superbruger eller administrator kan du ændre formålet med adgang til databaser for rapporter, sider af typen API og forespørgsler for at forbedre tjenestens ydeevne.</span><span class="sxs-lookup"><span data-stu-id="79cdc-104">As a super user or administrator, you can change the database access intent on reports, pages of the type API, and queries to improve performance of the service.</span></span>

## <a name="overview"></a><span data-ttu-id="79cdc-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="79cdc-105">Overview</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="79cdc-106">kan konfigureres til at bruge skrivebeskyttede kopier af den primære database (læse-skrive).</span><span class="sxs-lookup"><span data-stu-id="79cdc-106">can be set up to use read-only replicas of the primary (read-write) database.</span></span> <span data-ttu-id="79cdc-107">Hvis du bruger kopien af brugerdatabasen, reduceres den primære databases belastning.</span><span class="sxs-lookup"><span data-stu-id="79cdc-107">Using the database replica reduces the load on the primary database.</span></span> <span data-ttu-id="79cdc-108">I nogle tilfælde vil det også forbedre ydeevnen, når data vises i klienten.</span><span class="sxs-lookup"><span data-stu-id="79cdc-108">In some cases, it will also improve the performance when viewing data in the client.</span></span> <span data-ttu-id="79cdc-109">Kopier er nyttige for objekter, f. eks. rapporter, forespørgsler og API-sider, som kun bruges til at se data, ikke til at ændre data.</span><span class="sxs-lookup"><span data-stu-id="79cdc-109">Replicas are beneficial for objects, like reports, queries, and API pages, that are used for viewing data only, not modifying data.</span></span>

<span data-ttu-id="79cdc-110">Når objekter køres, bestemmer formålet med adgang til databasen, om der skal bruges en skrivebeskyttet kopi, hvis den er tilgængelig, eller den primære database.</span><span class="sxs-lookup"><span data-stu-id="79cdc-110">When objects run, the database access intent determines whether to use a read-only replica, if one is available, or the primary database.</span></span> <span data-ttu-id="79cdc-111">Rapporter, API-sider og forespørgsler udvikles med et foruddefineret formål med adgang til databasen (få flere oplysninger i [egenskaben DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span><span class="sxs-lookup"><span data-stu-id="79cdc-111">Reports, API pages, and queries are developed with a predefined database access intent (see [DatabaseAccessIntent property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span></span>

<span data-ttu-id="79cdc-112">På siden **Liste over formål med adgang til database** kan du tilsidesætte det foruddefinerede formål med adgang til database for objekter, når de køres.</span><span class="sxs-lookup"><span data-stu-id="79cdc-112">The **Database Access Intent List** page lets you override the predefined database access intent for objects when they're run.</span></span>

<span data-ttu-id="79cdc-113">I databaseterminologi kaldes denne funktion ofte for *read scale-out*. Du kan få flere oplysninger om read-scale out og formål med adgang til databaser i [!INCLUDE[prod_short](includes/prod_short.md)] i [Sådan bruger du read scale-out til at forbedre ydeevnen](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) i [!INCLUDE[prod_short](includes/prod_short.md)] Hjælp til udviklere og administratorer.</span><span class="sxs-lookup"><span data-stu-id="79cdc-113">In database terms, this feature is commonly known as *read scale-out*. For more information about read-scale out and data access intent in [!INCLUDE[prod_short](includes/prod_short.md)], see [Utilizing Read Scale-Out for Better Performance](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in the [!INCLUDE[prod_short](includes/prod_short.md)] Developer and Administration help.</span></span>

## <a name="to-change-the-database-access-intent"></a><span data-ttu-id="79cdc-114">Sådan ændrer du formålet med adgang til databaser</span><span class="sxs-lookup"><span data-stu-id="79cdc-114">To change the database access intent</span></span>

1. <span data-ttu-id="79cdc-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Liste over formål med adgang til database**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="79cdc-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Database Access Intent List**, and then choose the related link.</span></span>

    <span data-ttu-id="79cdc-116">Siden viser alle rapporter, sider og forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="79cdc-116">The page lists all reports, pages, and queries.</span></span> <span data-ttu-id="79cdc-117">Kolonnen **Formål med adgang** indeholder en af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="79cdc-117">The **Access Intent** column includes one of the following values:</span></span>

    |<span data-ttu-id="79cdc-118">**Indstilling**</span><span class="sxs-lookup"><span data-stu-id="79cdc-118">**Setting**</span></span>|<span data-ttu-id="79cdc-119">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="79cdc-119">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="79cdc-120">**Standard**</span><span class="sxs-lookup"><span data-stu-id="79cdc-120">**Default**</span></span>|<span data-ttu-id="79cdc-121">Angiver, at objektet bruger det foruddefinerede formål med adgang til database.</span><span class="sxs-lookup"><span data-stu-id="79cdc-121">Indicates that the object uses the predefined database access intent.</span></span>|
    |<span data-ttu-id="79cdc-122">**Tillad skrivning**</span><span class="sxs-lookup"><span data-stu-id="79cdc-122">**Allow Write**</span></span>|<span data-ttu-id="79cdc-123">Indstiller objektet til at bruge den primære database, så brugeren kan ændre data.</span><span class="sxs-lookup"><span data-stu-id="79cdc-123">Sets the object to use the primary database, allowing the user to modify data.</span></span>|
    |<span data-ttu-id="79cdc-124">**Skrivebeskyttet**</span><span class="sxs-lookup"><span data-stu-id="79cdc-124">**Read Only**</span></span>|<span data-ttu-id="79cdc-125">Angiver, at objektet skal bruge kopien af databasen, hvilket betyder, at brugeren kun kan se data, ikke ændre data.</span><span class="sxs-lookup"><span data-stu-id="79cdc-125">Sets the object to use the database replica, which means that the user can only view data, not change data.</span></span>|

2. <span data-ttu-id="79cdc-126">Vælg handlingen **Rediger liste**.</span><span class="sxs-lookup"><span data-stu-id="79cdc-126">Choose the **Edit List** action.</span></span>

3. <span data-ttu-id="79cdc-127">På siden **Rediger – liste over formål med adgang til database** skal du redigere feltet **Formål med adgang** for objekterne.</span><span class="sxs-lookup"><span data-stu-id="79cdc-127">On the **Edit - Database Access Intent List** page, change the **Access Intent** field for the objects.</span></span>

    > [!NOTE]
    > <span data-ttu-id="79cdc-128">Hvis et objekt, der kan redigeres (f.eks. Kundekort) er **Skrivebeskyttet**, vil den primære database stadig blive brugt, uanset adgangsformålet, så brugerne kan foretage ændringer som normalt.</span><span class="sxs-lookup"><span data-stu-id="79cdc-128">If an object that is editable, like the Customer Card, is set to **Read Only**, the primary database will still be used, regardless of the access intent, allowing users to make changes as normal.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="79cdc-129">Se relateret oplæring på [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="79cdc-129">See Related Training at [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="79cdc-130">Se også</span><span class="sxs-lookup"><span data-stu-id="79cdc-130">See Also</span></span>
[<span data-ttu-id="79cdc-131">Forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="79cdc-131">Business Functionality</span></span>](across-business-functionality.md)  
[<span data-ttu-id="79cdc-132">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="79cdc-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="79cdc-133">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="79cdc-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="79cdc-134">Introduktion</span><span class="sxs-lookup"><span data-stu-id="79cdc-134">Getting Started</span></span>](product-get-started.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
