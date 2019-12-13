---
title: Sådan defineres lagermedarbejdere | Microsoft Docs
description: Hver bruger, som udfører lageraktiviteter, skal være defineret som en lagermedarbejder, der er tildelt én standardlokation og evt. flere ikke-standardlokationer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 624603a2610ca07388c0b84d13b0707e06e92a18
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881530"
---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="ca961-103">Definere lagermedarbejdere</span><span class="sxs-lookup"><span data-stu-id="ca961-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="ca961-104">Hver bruger, som udfører lageraktiviteter, skal være defineret som en lagermedarbejder, der er tildelt én standardlokation og evt. flere ikke-standardlokationer.</span><span class="sxs-lookup"><span data-stu-id="ca961-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="ca961-105">Denne brugeropsætning filtrerer alle lageraktiviteter på tværs af databasen til medarbejderens lokation, så medarbejderen kun kan udføre lageraktiviteterne på standardlokationen.</span><span class="sxs-lookup"><span data-stu-id="ca961-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="ca961-106">En bruger kan være tildelt yderligere ikke-standard-lokationer, som medarbejderen kan få vist aktivitetslinjer for men ikke udføre aktiviteterne.</span><span class="sxs-lookup"><span data-stu-id="ca961-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="ca961-107">Sådan defineres lagermedarbejdere</span><span class="sxs-lookup"><span data-stu-id="ca961-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="ca961-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagermedarbejdere**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ca961-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ca961-109">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ca961-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="ca961-110">Vælg feltet **Bruger-ID**, og vælg derefter brugeren, der skal tilføjes som lagermedarbejder.</span><span class="sxs-lookup"><span data-stu-id="ca961-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="ca961-111">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca961-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="ca961-112">Angiv i feltet **Lokationskode** koden for den lokation, hvor brugeren skal arbejde.</span><span class="sxs-lookup"><span data-stu-id="ca961-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="ca961-113">Marker afkrydsningsfeltet **Standard** for at definere lokationen som den eneste lokation, hvor medarbejderen kan udføre lageraktiviteter.</span><span class="sxs-lookup"><span data-stu-id="ca961-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="ca961-114">Gentag disse trin for at tildele andre medarbejdere til lokationer eller for at tildele ikke-standardlokationer til eksisterende lagermedarbejdere.</span><span class="sxs-lookup"><span data-stu-id="ca961-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ca961-115">Se også</span><span class="sxs-lookup"><span data-stu-id="ca961-115">See Also</span></span>  
[<span data-ttu-id="ca961-116">Logistik</span><span class="sxs-lookup"><span data-stu-id="ca961-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="ca961-117">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="ca961-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ca961-118">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="ca961-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="ca961-119">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="ca961-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="ca961-120">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="ca961-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ca961-121">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ca961-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
