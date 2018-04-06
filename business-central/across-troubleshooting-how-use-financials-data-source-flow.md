---
title: Fejlfinding af integration med Microsoft Flow | Microsoft Docs
description: "Du kan bruge fejlfinding til at gøre dine Financials-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette et automatiseret workflow."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 60ce05760251da39280eb8a4884cb80586c2ab62
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="40031-103">Fejlfinding af integration med Microsoft Flow - URL-adresse til anmodning er for lang</span><span class="sxs-lookup"><span data-stu-id="40031-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="40031-104">Du kan bruge dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del af en arbejdsproces i Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="40031-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="40031-105">Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Flow.</span><span class="sxs-lookup"><span data-stu-id="40031-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="40031-106">Hvis du opretter et Microsoft Flow ved hjælp af [!INCLUDE[d365fin](includes/d365fin_md.md)]-konnektoren, får du vist en fejlmeddelelse om, at den anmodede URL-adresse er for lang, når du har oprettet flowet, f.eks. som følgende: **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="40031-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="40031-107">Årsag</span><span class="sxs-lookup"><span data-stu-id="40031-107">Cause</span></span>
<span data-ttu-id="40031-108">For at et flow kan udløses, søges der efter ændringer i dine data.</span><span class="sxs-lookup"><span data-stu-id="40031-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="40031-109">Når det afgøres, om dataene er blevet ændret, sammenligner konnektorerne de cachede data med de nye data, der anmodes om fra kilden.</span><span class="sxs-lookup"><span data-stu-id="40031-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="40031-110">Hvis dataanmodningen opretter en URL-adresse, der er for lang, mislykkes anmodningen.</span><span class="sxs-lookup"><span data-stu-id="40031-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="40031-111">Almindelige årsager kan omfatte:</span><span class="sxs-lookup"><span data-stu-id="40031-111">Common causes may include:</span></span>
- <span data-ttu-id="40031-112">Som regel enhver kildetabel med mere end 250 rækker</span><span class="sxs-lookup"><span data-stu-id="40031-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="40031-113">Kildetabeller, der indeholder flere tusinde poster</span><span class="sxs-lookup"><span data-stu-id="40031-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="40031-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="40031-114">Workaround</span></span>
<span data-ttu-id="40031-115">Følg disse trin for at løse problemet.</span><span class="sxs-lookup"><span data-stu-id="40031-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="40031-116">Vælg at redigere det flow, der er problemer med.</span><span class="sxs-lookup"><span data-stu-id="40031-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="40031-117">Udvid **Vis avancerede indstillinger** på udløseren til flowet.</span><span class="sxs-lookup"><span data-stu-id="40031-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="40031-118">Angiv antallet af poster, der skal springes over, i feltet **Antal, der skal springes over**.</span><span class="sxs-lookup"><span data-stu-id="40031-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="40031-119">Hvis den tabel, der bruges som datakilde har 4.000 poster, skal du f.eks. angive 4.000 som det antal poster, der skal springes over.</span><span class="sxs-lookup"><span data-stu-id="40031-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="40031-120">Opdater dit flow.</span><span class="sxs-lookup"><span data-stu-id="40031-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="40031-121">Konnektoren er i øjeblikket i Beta.</span><span class="sxs-lookup"><span data-stu-id="40031-121">The connector is currently in Beta.</span></span> <span data-ttu-id="40031-122">Opdateringer til hvordan dataændringer beregnes i en senere version.</span><span class="sxs-lookup"><span data-stu-id="40031-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="40031-123">Se også</span><span class="sxs-lookup"><span data-stu-id="40031-123">See Also</span></span>
<span data-ttu-id="40031-124">[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i et automatisk workflow](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="40031-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
<span data-ttu-id="40031-125">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="40031-125">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="40031-126">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="40031-126">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="40031-127">[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="40031-127">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="40031-128">[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="40031-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="40031-129">Finans</span><span class="sxs-lookup"><span data-stu-id="40031-129">Finance</span></span>](finance.md)  

