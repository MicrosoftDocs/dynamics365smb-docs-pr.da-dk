---
title: "Sådan opdeles lageraktivitetslinjer | Microsoft Docs"
description: "I læg-på-lager-aktiviteter, bevægelser eller pluk (logistik) og i læg-på-lager-aktiviteter og pluk (lager) foreslås der automatisk placeringer for varer, der plukkes eller lægges på lager. Den faktiske mængde på den foreslåede placering er muligvis ikke tilstrækkelig, eller at der ikke er nok plads på den foreslåede placering til at lægge den ønskede bestilte mængde på lager. I begge tilfælde skal du opdele linjen, så varerne for én linje enten hentes fra eller anbringes på mere end én placering."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: dfb633ef874b77a3cf6060311f0bcbbf66e05102
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="split-warehouse-activity-lines"></a><span data-ttu-id="2780d-105">Opdele lageraktivitetslinjer</span><span class="sxs-lookup"><span data-stu-id="2780d-105">Split Warehouse Activity Lines</span></span>
<span data-ttu-id="2780d-106">I læg-på-lager-aktiviteter, bevægelser eller pluk (logistik) og i læg-på-lager-aktiviteter og pluk (lager) foreslås der automatisk placeringer for varer, der plukkes eller lægges på lager.</span><span class="sxs-lookup"><span data-stu-id="2780d-106">In warehouse put-aways, movements, or picks, and in inventory put-aways and inventory picks, bins are suggested for the picking or putting away of items.</span></span> <span data-ttu-id="2780d-107">Den faktiske mængde på den foreslåede placering er muligvis ikke tilstrækkelig, eller at der ikke er nok plads på den foreslåede placering til at lægge den ønskede bestilte mængde på lager.</span><span class="sxs-lookup"><span data-stu-id="2780d-107">The actual quantity in the bin suggested may not be sufficient, or there is not enough room in the suggested bin to put away the required quantity.</span></span> <span data-ttu-id="2780d-108">I begge tilfælde skal du opdele linjen, så varerne for én linje enten hentes fra eller anbringes på mere end én placering.</span><span class="sxs-lookup"><span data-stu-id="2780d-108">In these cases, you need to split the line, so that the items for one line are either taken from or placed into more than one bin.</span></span>  

<span data-ttu-id="2780d-109">Følgende fremgangsmåde gælder for lagerdokumenter som f.eks. læg-på-lager (logistik), bevægelse og pluklinjer eller læg-på-lager (lager), bevægelse og pluklinjer.</span><span class="sxs-lookup"><span data-stu-id="2780d-109">The following procedure applies to warehouse documents, such as warehouse put-away, movement, and pick lines, or inventory put-away, movement, and pick lines.</span></span>  

## <a name="to-split-warehouse-activity-lines"></a><span data-ttu-id="2780d-110">Sådan opdeles lageraktivitetslinjer</span><span class="sxs-lookup"><span data-stu-id="2780d-110">To split warehouse activity lines</span></span>  
1.  <span data-ttu-id="2780d-111">Åbn en lageraktivitetslinje, hvor du forsøger at håndtere en utilstrækkelig mængde.</span><span class="sxs-lookup"><span data-stu-id="2780d-111">Open a warehouse activity line where you are trying to handle an insufficient quantity.</span></span>  
2.  <span data-ttu-id="2780d-112">I feltet **Håndteringsantal** skal du angive det reducerede antal, som du er i stand til at håndtere.</span><span class="sxs-lookup"><span data-stu-id="2780d-112">In the **Qty. to Handle** field, enter the reduced quantity that you are able to handle.</span></span>  
3.  <span data-ttu-id="2780d-113">I oversigtspanelet **Linjer** skal du vælge handlingen **Handlinger**, vælge handlingen **Funktioner** og derefter vælge handlingen **Opdel linje**.</span><span class="sxs-lookup"><span data-stu-id="2780d-113">On the **Lines** FastTab, choose the **Actions** action, choose the **Functions** action, and then choose the **Split Line** action.</span></span> <span data-ttu-id="2780d-114">Der vises en ny linje, som er en kopi af den oprindelige linje, bortset fra at feltet **Håndteringsantal** indeholder det antal, du har fjernet fra den oprindelige linje.</span><span class="sxs-lookup"><span data-stu-id="2780d-114">A new line appears, which is a copy of the original line, except that the **Qty. to Handle** field contains the quantity that you removed from the original line.</span></span>  
4.  <span data-ttu-id="2780d-115">Tildel en relevant placering, og hvis der anvendes styret læg-på-lager og pluk, en zone til denne nye linje, eller fortsæt med at opdele linjen efter behov, indtil du finder de rette placeringer for alle antallene.</span><span class="sxs-lookup"><span data-stu-id="2780d-115">Assign an appropriate bin and, if you are using directed put-away and pick, a zone, to this new line, or continue splitting the line as necessary until you find appropriate bins for all of the quantity.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2780d-116">Hvis lokationen bruger styret læg-på-lager og pluk, og du opdeler linjerne, skal du være godt kendt med lagerstedet og i stand til at vælge en placering, som passer med opbevaringskravene til varen og opfylder de generelle krav for lagerdokumentet.</span><span class="sxs-lookup"><span data-stu-id="2780d-116">If the location uses directed put-away and pick and you split the lines, you must be familiar with the warehouse and be able to choose a bin that matches the storage requirements of the item and that fulfills the general requirements of the warehouse document.</span></span> <span data-ttu-id="2780d-117">Det er f.eks. ikke nogen god idé at opdele en linje på et plukdokument og placere nogle af varerne i massevarelageret.</span><span class="sxs-lookup"><span data-stu-id="2780d-117">For example, you would not split a line on a pick document and place some items in the bulk storage.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2780d-118">Se også</span><span class="sxs-lookup"><span data-stu-id="2780d-118">See Also</span></span>  
[<span data-ttu-id="2780d-119">Logistik</span><span class="sxs-lookup"><span data-stu-id="2780d-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="2780d-120">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="2780d-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="2780d-121">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="2780d-121">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="2780d-122">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="2780d-122">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="2780d-123">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="2780d-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="2780d-124">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2780d-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

