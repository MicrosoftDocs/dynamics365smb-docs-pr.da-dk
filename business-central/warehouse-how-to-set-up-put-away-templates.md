---
title: Sådan oprettes læg-på-lager-skabeloner | Microsoft Docs
description: Hvis du benytter styret læg-på-lager og pluk, foreslås den til enhver tid mest velegnede placering til varer ifølge den læg-på-lager-skabelon, du har defineret til lagerstedet, de placeringsniveauer, du har tildelt placeringerne, og de minimum- og maksimumantal, du har angivet for faste placeringer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 168a330bdb85c8d5ed18a9ce2b65339c82b4055e
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196135"
---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="f3989-103">Oprette læg-på-lager-skabeloner</span><span class="sxs-lookup"><span data-stu-id="f3989-103">Set Up Put-away Templates</span></span>
<span data-ttu-id="f3989-104">Hvis du benytter styret læg-på-lager og pluk, foreslås den til enhver tid mest velegnede placering til varer ifølge den læg-på-lager-skabelon, du har defineret til lagerstedet, de placeringsniveauer, du har tildelt placeringerne, og de minimum- og maksimumantal, du har angivet for faste placeringer.</span><span class="sxs-lookup"><span data-stu-id="f3989-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="f3989-105">Du kan oprette en række læg-på-lager-skabeloner og vælge en af som standardskabelon for læg-på-lager-aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="f3989-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="f3989-106">Du kan også vælge en bestemt skabelon til en vare eller lagervare, som der er specielle krav til i forbindelse med læg-på-lager-aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="f3989-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="f3989-107">Sådan oprettes læg-på-lager-skabeloner</span><span class="sxs-lookup"><span data-stu-id="f3989-107">To set up put-away templates</span></span>  
1.  <span data-ttu-id="f3989-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Læg-på-lager-skabeloner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f3989-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f3989-109">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f3989-109">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="f3989-110">Indtast en kode som entydig id for skabelonen.</span><span class="sxs-lookup"><span data-stu-id="f3989-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4.  <span data-ttu-id="f3989-111">Indtast evt. en kort beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f3989-111">Enter a short description, if you wish.</span></span>  
5.  <span data-ttu-id="f3989-112">Brug den første linje til at angive de krav til placeringer, som du ønsker, først og fremmest skal være overholdt, når der foreslås en læg-på-lager-aktivitet.</span><span class="sxs-lookup"><span data-stu-id="f3989-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>  
6.  <span data-ttu-id="f3989-113">Brug den anden linje til at angive de sekundære krav til placeringer, som skal overholdes, når der skal findes en placering for en læg-på-lager-aktivitet.</span><span class="sxs-lookup"><span data-stu-id="f3989-113">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="f3989-114">Den anden linje bruges kun, hvis en placering, der overholder kravene på den første linje, ikke kan findes.</span><span class="sxs-lookup"><span data-stu-id="f3989-114">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7.  <span data-ttu-id="f3989-115">Fortsæt med at udfylde linjerne, indtil du har beskrevet alle de acceptable placeringer, som du vil bruge til læg-på-lager-aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="f3989-115">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8.  <span data-ttu-id="f3989-116">Marker afkrydsningsfeltet **Find løs placering** på den nederste linje i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="f3989-116">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="f3989-117">Du kan oprette en række læg-på-lager-skabeloner og bruge dem efter behov.</span><span class="sxs-lookup"><span data-stu-id="f3989-117">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="f3989-118">Den læg-på-lager-skabelon, som du har valgt til varen eller lagervaren, hvis en sådan er oprettet, benyttes først.</span><span class="sxs-lookup"><span data-stu-id="f3989-118">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="f3989-119">Hvis felterne her ikke er udfyldt, anvendes den læg-på-lager-skabelon, du har valgt til lagerstedet i oversigtspanelet **Placeringsmetode** på lokationskortet.</span><span class="sxs-lookup"><span data-stu-id="f3989-119">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f3989-120">Se også</span><span class="sxs-lookup"><span data-stu-id="f3989-120">See Also</span></span>  
[<span data-ttu-id="f3989-121">Logistik</span><span class="sxs-lookup"><span data-stu-id="f3989-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="f3989-122">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="f3989-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f3989-123">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="f3989-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="f3989-124">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="f3989-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="f3989-125">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="f3989-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="f3989-126">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f3989-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
