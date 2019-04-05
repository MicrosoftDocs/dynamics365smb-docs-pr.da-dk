---
title: Automatisk nedbrydning med styret læg-på-lager og pluk | Microsoft Docs
description: På lokationer, hvor der bruges styret læg-på-lager og pluk, kan du nedbryde større enheder til mindre enheder, når der oprettes lagerinstruktioner, som opfylder behovet for kildedokumenter, produktionsordrer eller interne pluk og læg-på-lager.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: c328df334d1bb1be33ced814677c3ef3ea634799
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792807"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><span data-ttu-id="2210f-103">Aktivere automatisk nedbrydning med styret læg-på-lager og pluk</span><span class="sxs-lookup"><span data-stu-id="2210f-103">Enable Automatic Breaking Bulk with Directed Put-away and Pick</span></span>
<span data-ttu-id="2210f-104">På lokationer, hvor der bruges styret læg-på-lager og pluk, kan [!INCLUDE[d365fin](includes/d365fin_md.md)] i visse tilfælde foretage automatisk nedbrydning. Dermed nedbrydes større enheder til mindre enheder, når der oprettes lagerinstruktioner, som opfylder behovet for kildedokumenter, produktionsordrer eller interne pluk og læg-på-lager.</span><span class="sxs-lookup"><span data-stu-id="2210f-104">For locations that use directed put-away and pick, [!INCLUDE[d365fin](includes/d365fin_md.md)] can, in various situations, automatically breakbulk, that is, break a larger unit of measure into smaller units of measure, when it creates warehouse instructions that fulfill the needs of source documents, production orders, or internal picks and put-aways.</span></span> <span data-ttu-id="2210f-105">Nedbrydning kan også betyde indsamling af mindre enheder, hvis det er nødvendigt for at efterkomme udgående anmodninger, ved at nedbryde den største enhed i kildedokumentet eller produktionsordren i mindre enheder, der er tilgængelig på lageret. -nedbrydninger som følger.</span><span class="sxs-lookup"><span data-stu-id="2210f-105">To breakbulk sometimes also means gathering smaller units of measure, if necessary, to meet outbound requests by breaking the larger unit of measure on the source document or production order into the smaller units of measure that are available in the warehouse.</span></span>   

## <a name="breakbulking-in-picks"></a><span data-ttu-id="2210f-106">Nedbrydning under pluk</span><span class="sxs-lookup"><span data-stu-id="2210f-106">Breakbulking in Picks</span></span>  
<span data-ttu-id="2210f-107">Hvis du vil lagre varer i flere forskellige enheder og lader dem blive automatisk kombineret efter behov i plukprocessen, skal du markere feltet **Tillad nedbrydning** på lokationskortet.</span><span class="sxs-lookup"><span data-stu-id="2210f-107">If you want to store items in several different units of measure and allow them to be automatically combined as needed in the picking process, select the **Allow Breakbulk** field on the location card.</span></span>  

<span data-ttu-id="2210f-108">Når programmet skal fuldføre en opgave, leder det automatisk efter en vare fra samme enhed.</span><span class="sxs-lookup"><span data-stu-id="2210f-108">To fulfill a task, the program automatically looks for an item in the same unit of measure.</span></span> <span data-ttu-id="2210f-109">Men hvis programmet ikke kan finde denne type vare, og du har markeret dette felt, foreslår programmet, at du nedbryder en stor enhed til den størrelse enhed, der er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="2210f-109">But if it cannot find this form of the item, and this field is selected, the program will suggest that you break a larger unit of measure into the unit of measure that is needed.</span></span>  

<span data-ttu-id="2210f-110">Hvis systemet kun kan finde mindre enheder, foreslår det, at du samler varerne for at opfylde antallet på leverance- eller produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="2210f-110">If the system can only find smaller units of measure, it will suggest that you gather items to fulfill the quantity on the shipment or production order.</span></span> <span data-ttu-id="2210f-111">I praksis nedbryder det større enheder på kildedokumentet til mindre enheder, der kan plukkes.</span><span class="sxs-lookup"><span data-stu-id="2210f-111">In effect, it breaks the larger unit of measure on the source document into smaller units for picking.</span></span>  

## <a name="breakbulking-in-put-aways"></a><span data-ttu-id="2210f-112">Nedbrydning i læg-på-lager</span><span class="sxs-lookup"><span data-stu-id="2210f-112">Breakbulking in Put-aways</span></span>  
<span data-ttu-id="2210f-113">I lagerstedets læg-på-lager foreslår programmet automatisk at placere handlingslinjer i læg-på-lager-enheder, for eksempel stykker, selvom varerne leveres i en anden form for enhed.</span><span class="sxs-lookup"><span data-stu-id="2210f-113">In the warehouse put-away, the program automatically suggests Place action lines in the put-away unit of measure, for example, pieces, even though the items arrive in a different unit of measure.</span></span>  

## <a name="breakbulking-in-movements"></a><span data-ttu-id="2210f-114">Nedbrydning i bevægelse</span><span class="sxs-lookup"><span data-stu-id="2210f-114">Breakbulking in Movements</span></span>  
<span data-ttu-id="2210f-115">Programmet foretager også automatisk nedbrydning i genopfyldningsbevægelser, hvis feltet **Tillad nedbrydning** er markeret i oversigtspanelet **Indstillinger** på siden **Beregn placeringsgenopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="2210f-115">The program also breakbulks automatically in replenishment movements, if the **Allow Breakbulk** field is selected on the **Option** FastTab on the **Calculate Bin Replenishment** page.</span></span>  

<span data-ttu-id="2210f-116">Du kan få vist resultaterne af konverteringsprocessen fra en enhed til en anden som midlertidige nedbrydningslinjer i læg-på-lager-, pluk- eller bevægelsesinstruktionerne.</span><span class="sxs-lookup"><span data-stu-id="2210f-116">You can view the results of the conversion process from one unit of measure to another as intermediate breakbulk lines in the put-away, pick, or movement instructions.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2210f-117">Hvis du markerer feltet **Angiv nedbrydningsfilter** i lagerinstruktionshovedet, skjuler programmet nedbrydningslinjer, hver gang en større enhed vil blive brugt fuldstændig.</span><span class="sxs-lookup"><span data-stu-id="2210f-117">If you select the **Set Breakbulk Filter** field on the warehouse instruction header, the program will hide the breakbulk lines whenever the larger unit of measure is going to be completely used.</span></span> <span data-ttu-id="2210f-118">Hvis en palle f.eks. består af 12 stykker, og du skal bruge alle 12, anmoder plukket dig om at tage en palle og placere 12 stykker der.</span><span class="sxs-lookup"><span data-stu-id="2210f-118">For example, if a pallet is 12 pieces and you are going to use all 12 pieces, the pick will then direct you to take 1 pallet and place 12 pieces.</span></span> <span data-ttu-id="2210f-119">Hvis du på den anden side kun plukker ni stykker, skjules nedbrydningslinjerne ikke, selvom du har markeret feltet **Nedbrydningsfilter**, da de resterende tre stykker stadig skal placeres et sted på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="2210f-119">However, if you have to pick only 9 pieces, then the breakbulk lines will not be hidden, even if you have selected the **Breakbulk Filter** field, because you have to place the remaining three pieces somewhere in the warehouse.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2210f-120">Hvis enhederne skal fungere optimalt på lagerstedet – også i forbindelse med nedbrydningsfunktionen – bør du altid tilstræbe at:</span><span class="sxs-lookup"><span data-stu-id="2210f-120">If you want your units of measure to perform optimally in the warehouse, also in connection with the breakbulk functionality, you should wherever possible try to:</span></span>  
>   
> - <span data-ttu-id="2210f-121">indstille basisenheden for en vare til at være den mindste enhed, som du forventer at skulle håndtere under lagerprocessen.</span><span class="sxs-lookup"><span data-stu-id="2210f-121">Set up the base unit of measure for an item as the smallest unit of measure that you expect to handle in your warehouse processes.</span></span>  
> - <span data-ttu-id="2210f-122">Indstil alternative enheder for varen som flere forekomster af basisenheden.</span><span class="sxs-lookup"><span data-stu-id="2210f-122">Set up your alternative units of measure for the item as multiples of the base unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2210f-123">Se også</span><span class="sxs-lookup"><span data-stu-id="2210f-123">See Also</span></span>  
[<span data-ttu-id="2210f-124">Logistik</span><span class="sxs-lookup"><span data-stu-id="2210f-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="2210f-125">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="2210f-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="2210f-126">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="2210f-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="2210f-127">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="2210f-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="2210f-128">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="2210f-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="2210f-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2210f-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
