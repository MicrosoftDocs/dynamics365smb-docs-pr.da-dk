---
title: "Sådan konfigureres nye virksomheder ved brug af en cmdlet | Microsoft Docs"
description: "I en række scenarier kan du indlæse og importere en konfigurationspakke uden at involvere brugerne eller ved hjælp af RapidStart Services-brugergrænsefladen. Du kan gøre det ved hjælp af en Windows PowerShell-cmdlet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8b91c3b91e07f5ad96dcfc65152062054fc13c01
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a><span data-ttu-id="2b35c-104">Konfigurere nye virksomheder ved brug af en cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b35c-104">Configure New Companies using a Cmdlet</span></span>
<span data-ttu-id="2b35c-105">I en række scenarier kan du indlæse og importere en konfigurationspakke uden at involvere brugerne eller ved hjælp af RapidStart Services-brugergrænsefladen.</span><span class="sxs-lookup"><span data-stu-id="2b35c-105">In a number of scenarios, you may want to load and import a configuration package without involving your users or using the RapidStart Services user interface.</span></span> <span data-ttu-id="2b35c-106">Du kan gøre det ved hjælp af en Windows PowerShell-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b35c-106">You can do so by using a Windows PowerShell cmdlet.</span></span> <span data-ttu-id="2b35c-107">Scenarier, hvor dette kan være nyttigt, omfatter:</span><span class="sxs-lookup"><span data-stu-id="2b35c-107">Scenarios where this may be useful include:</span></span>  

- <span data-ttu-id="2b35c-108">Udføre import af data på tværs af flere [!INCLUDE[d365fin](includes/d365fin_md.md)]-installationer.</span><span class="sxs-lookup"><span data-stu-id="2b35c-108">Performing data import across multiple [!INCLUDE[d365fin](includes/d365fin_md.md)] installations.</span></span>
- <span data-ttu-id="2b35c-109">Konfiguration af yderligere moduler til flere kunder.</span><span class="sxs-lookup"><span data-stu-id="2b35c-109">Configuring additional application areas for multiple customers.</span></span>  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a><span data-ttu-id="2b35c-110">Sådan implementeres en konfigurationspakke ved brug af cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b35c-110">To deploy a configuration package using a cmdlet</span></span>  

1. <span data-ttu-id="2b35c-111">Forberede en RapidStart Services-pakke.</span><span class="sxs-lookup"><span data-stu-id="2b35c-111">Prepare a RapidStart Services package.</span></span> <span data-ttu-id="2b35c-112">Du kan for eksempel oprette en pakke for at importere bestemte værdier og navnene på tabellen og felterne, som disse værdier skal indsættes i.</span><span class="sxs-lookup"><span data-stu-id="2b35c-112">For example, you can create a package to import certain values and the names of the table and the fields to insert these values into.</span></span>  
2. <span data-ttu-id="2b35c-113">Placer pakken på en computer, hvor du kører cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b35c-113">Place the package on a computer where you will run the cmdlet.</span></span>  
3. <span data-ttu-id="2b35c-114">Åbn [!INCLUDE[d365fin](includes/d365fin_md.md)] Administration Shell.</span><span class="sxs-lookup"><span data-stu-id="2b35c-114">Open the [!INCLUDE[d365fin](includes/d365fin_md.md)] administration shell.</span></span>  
4. <span data-ttu-id="2b35c-115">Angiv **Invoke-NAVCodeUnit**, og angiv oplysninger, der svarer til følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="2b35c-115">Enter **Invoke-NAVCodeUnit**, and specify information similar to the following example.</span></span>  
    ```  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
<span data-ttu-id="2b35c-116">Denne cmdlet importerer pakken til hvert firma.</span><span class="sxs-lookup"><span data-stu-id="2b35c-116">The cmdlet imports the package into each company.</span></span> <span data-ttu-id="2b35c-117">Brugere kan begynde at bruge de nye funktioner med det samme.</span><span class="sxs-lookup"><span data-stu-id="2b35c-117">Users can start to use the new functionality immediately.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2b35c-118">Se også</span><span class="sxs-lookup"><span data-stu-id="2b35c-118">See Also</span></span>  
[<span data-ttu-id="2b35c-119">Konfigurere nye virksomheder</span><span class="sxs-lookup"><span data-stu-id="2b35c-119">Configure New Companies</span></span>](admin-how-to-configure-new-companies.md)  
[<span data-ttu-id="2b35c-120">Anvende konfigurationer på nye virksomheder</span><span class="sxs-lookup"><span data-stu-id="2b35c-120">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="2b35c-121">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="2b35c-121">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="2b35c-122">Opsætning</span><span class="sxs-lookup"><span data-stu-id="2b35c-122">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="2b35c-123">Microsoft Dynamics NAV Windows PowerShell-cmdletter</span><span class="sxs-lookup"><span data-stu-id="2b35c-123">Microsoft Dynamics NAV Windows PowerShell Cmdlets</span></span>](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

