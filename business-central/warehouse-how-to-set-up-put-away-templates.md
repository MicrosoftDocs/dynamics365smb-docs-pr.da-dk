---
title: "Sådan oprettes læg-på-lager-skabeloner | Microsoft Docs"
description: "Hvis du benytter styret læg-på-lager og pluk, foreslås den til enhver tid mest velegnede placering til varer ifølge den læg-på-lager-skabelon, du har defineret til lagerstedet, de placeringsniveauer, du har tildelt placeringerne, og de minimum- og maksimumantal, du har angivet for faste placeringer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 83ae54e61c5881cce9a58c6684bbf82c4b3ad750
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="cefea-103">Oprette læg-på-lager-skabeloner</span><span class="sxs-lookup"><span data-stu-id="cefea-103">Set Up Put-away Templates</span></span>
<span data-ttu-id="cefea-104">Hvis du benytter styret læg-på-lager og pluk, foreslås den til enhver tid mest velegnede placering til varer ifølge den læg-på-lager-skabelon, du har defineret til lagerstedet, de placeringsniveauer, du har tildelt placeringerne, og de minimum- og maksimumantal, du har angivet for faste placeringer.</span><span class="sxs-lookup"><span data-stu-id="cefea-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="cefea-105">Du kan oprette en række læg-på-lager-skabeloner og vælge en af som standardskabelon for læg-på-lager-aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="cefea-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="cefea-106">Du kan også vælge en bestemt skabelon til en vare eller lagervare, som der er specielle krav til i forbindelse med læg-på-lager-aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="cefea-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="cefea-107">Sådan oprettes læg-på-lager-skabeloner</span><span class="sxs-lookup"><span data-stu-id="cefea-107">To set up put-away templates</span></span>  
1.  <span data-ttu-id="cefea-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Læg-på-lager-skabeloner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="cefea-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cefea-109">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cefea-109">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="cefea-110">Indtast en kode som entydig id for skabelonen.</span><span class="sxs-lookup"><span data-stu-id="cefea-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4.  <span data-ttu-id="cefea-111">Indtast evt. en kort beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="cefea-111">Enter a short description, if you wish.</span></span>  
5.  <span data-ttu-id="cefea-112">Brug den første linje til at angive de krav til placeringer, som du ønsker, først og fremmest skal være overholdt, når der foreslås en læg-på-lager-aktivitet.</span><span class="sxs-lookup"><span data-stu-id="cefea-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>  
6.  <span data-ttu-id="cefea-113">Brug den anden linje til at angive de sekundære krav til placeringer, som skal overholdes, når der skal findes en placering for en læg-på-lager-aktivitet.</span><span class="sxs-lookup"><span data-stu-id="cefea-113">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="cefea-114">Den anden linje bruges kun, hvis en placering, der overholder kravene på den første linje, ikke kan findes.</span><span class="sxs-lookup"><span data-stu-id="cefea-114">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7.  <span data-ttu-id="cefea-115">Fortsæt med at udfylde linjerne, indtil du har beskrevet alle de acceptable placeringer, som du vil bruge til læg-på-lager-aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="cefea-115">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8.  <span data-ttu-id="cefea-116">Marker afkrydsningsfeltet **Find løs placering** på den nederste linje i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="cefea-116">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="cefea-117">Du kan oprette en række læg-på-lager-skabeloner og bruge dem efter behov.</span><span class="sxs-lookup"><span data-stu-id="cefea-117">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="cefea-118">Den læg-på-lager-skabelon, som du har valgt til varen eller lagervaren, hvis en sådan er oprettet, benyttes først.</span><span class="sxs-lookup"><span data-stu-id="cefea-118">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="cefea-119">Hvis felterne her ikke er udfyldt, anvendes den læg-på-lager-skabelon, du har valgt til lagerstedet i oversigtspanelet **Placeringsmetode** på lokationskortet.</span><span class="sxs-lookup"><span data-stu-id="cefea-119">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cefea-120">Se også</span><span class="sxs-lookup"><span data-stu-id="cefea-120">See Also</span></span>  
[<span data-ttu-id="cefea-121">Logistik</span><span class="sxs-lookup"><span data-stu-id="cefea-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="cefea-122">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="cefea-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="cefea-123">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="cefea-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="cefea-124">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="cefea-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="cefea-125">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="cefea-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="cefea-126">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cefea-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

