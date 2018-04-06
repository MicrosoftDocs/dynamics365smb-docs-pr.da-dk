---
title: "Designoplysninger – Maks. antal | Microsoft Docs"
description: "Det maksimale antal er en måde at vedligeholde lageret ved hjælp af et genbestillingspunkt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 26bed0b8832d5b12ce5d697df8ec6194ac7ae9b2
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-maximum-qty"></a><span data-ttu-id="3db80-103">Designoplysninger: Maks. antal</span><span class="sxs-lookup"><span data-stu-id="3db80-103">Design Details: Maximum Qty.</span></span>
<span data-ttu-id="3db80-104">Det maksimale antal er en måde at vedligeholde lageret ved hjælp af et genbestillingspunkt.</span><span class="sxs-lookup"><span data-stu-id="3db80-104">The Maximum Quantity policy is a way to maintain inventory using a reorder point.</span></span>  
  
 <span data-ttu-id="3db80-105">Alt om den faste genbestillingsantalmetode gælder også for denne metode.</span><span class="sxs-lookup"><span data-stu-id="3db80-105">Everything regarding the Fixed Reorder Qty. policy also applies to this policy.</span></span> <span data-ttu-id="3db80-106">Den eneste forskel er omfanget af den foreslåede forsyning.</span><span class="sxs-lookup"><span data-stu-id="3db80-106">The only difference is the quantity of the suggested supply.</span></span> <span data-ttu-id="3db80-107">Når metoden med maksimalt antal bruges, defineres genbestillingsantallet dynamisk baseret på det planlagte lagerniveau og varierer derfor normalt fra ordre til ordre.</span><span class="sxs-lookup"><span data-stu-id="3db80-107">When using the maximum quantity policy, the reorder quantity will be defined dynamically based on the projected inventory level and will therefore usually differ from order to order.</span></span>  
  
## <a name="calculated-per-time-bucket"></a><span data-ttu-id="3db80-108">Beregnet pr. interval</span><span class="sxs-lookup"><span data-stu-id="3db80-108">Calculated per Time Bucket</span></span>  
 <span data-ttu-id="3db80-109">Genbestillingsantallet bestemmes på det tidspunkt (slutningen af et interval), hvor planlægningssystemet registrerer, at genbestillingspunktet er passeret.</span><span class="sxs-lookup"><span data-stu-id="3db80-109">The reorder quantity is determined at the point of time (the end of a time bucket) when the planning system detects that the reorder point has been crossed.</span></span> <span data-ttu-id="3db80-110">På dette tidspunkt måler systemet afstanden fra den nuværende forventede lagerbeholdning op til den angivne maksimale lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="3db80-110">At this time, the system measures the gap from the current projected inventory level up to the specified maximum inventory.</span></span> <span data-ttu-id="3db80-111">Dette består af det antal, der skal genbestilles.</span><span class="sxs-lookup"><span data-stu-id="3db80-111">This constitutes the quantity that should be reordered.</span></span> <span data-ttu-id="3db80-112">Derefter kontrollerer systemet, om leveringen allerede er bestilt andre steder med henblik på at blive modtaget inden for leveringstiden, og i så fald reduceres mængden af den nye forsyningsordre med allerede bestilte antal.</span><span class="sxs-lookup"><span data-stu-id="3db80-112">The system then checks if supply has already been ordered elsewhere to be received within the lead time and, if so, reduces the quantity of the new supply order by already ordered quantities.</span></span>  
  
 <span data-ttu-id="3db80-113">Systemet sikrer, at den projekterede lagerbeholdning mindst når genbestillingsniveauet – i tilfælde af at brugeren har glemt at angive et maksimalt lagerantal.</span><span class="sxs-lookup"><span data-stu-id="3db80-113">The system will ensure that the projected inventory at least reaches the reorder point level – in case the user has forgotten to specify a maximum inventory quantity.</span></span>  
  
## <a name="combines-with-order-modifiers"></a><span data-ttu-id="3db80-114">Kombineres med ordremodifikatorer</span><span class="sxs-lookup"><span data-stu-id="3db80-114">Combines with Order Modifiers</span></span>  
 <span data-ttu-id="3db80-115">Afhængigt af opsætningen, kan det være bedst at kombinere metoden Maks. antal med ordremodifikatorer for at sikre et mindste ordreantal eller afrunde til et heltal af købsmåleenheder eller opdele det i flere lotter, som er defineret af det højst tilladte antal.</span><span class="sxs-lookup"><span data-stu-id="3db80-115">Depending on the setup, it may be best to combine the Maximum Quantity policy with order modifiers to ensure a minimum order quantity or round it to an integer number of purchase units of measure, or split it into more lots as defined by the maximum order quantity.</span></span>  
  
## <a name="combines-with-calendars"></a><span data-ttu-id="3db80-116">Kombinerer med kalendere</span><span class="sxs-lookup"><span data-stu-id="3db80-116">Combines with Calendars</span></span>  
 <span data-ttu-id="3db80-117">Før der bliver foreslået en ny forsyningsordre for at opfylde et genbestillingspunkt, kontrollerer planlægningssystemet, om ordren er planlagt til en ikkearbejdsdag i overensstemmelse med de kalendere, der er defineret i feltet **Basiskalenderkode** i vinduerne **Virksomhedsoplysninger** og **Lokationskort**.</span><span class="sxs-lookup"><span data-stu-id="3db80-117">Before suggesting a new supply order to meet a reorder point, the planning system checks if the order is scheduled for a non-working day, according to any calendars that are  defined in the **Base Calendar Code** field in the **Company Information** and **Location Card** windows.</span></span>  
  
 <span data-ttu-id="3db80-118">Hvis den planlagte dato er en ikkearbejdsdag, flytter planlægningssystemet ordren frem til den nærmeste arbejdsdag.</span><span class="sxs-lookup"><span data-stu-id="3db80-118">If the scheduled date is a non-working day, the planning system moves the order forward to the nearest working date.</span></span> <span data-ttu-id="3db80-119">Det kan resultere i en ordre, der opfylder et genbestillingspunkt, men ikke opfylder visse specifikke behov.</span><span class="sxs-lookup"><span data-stu-id="3db80-119">This may result in an order that meets a reorder point but does not meet some specific demand.</span></span> <span data-ttu-id="3db80-120">Planlægningssystemet opretter en ekstra levering for sådanne behov.</span><span class="sxs-lookup"><span data-stu-id="3db80-120">For such unbalanced demand, the planning system creates an extra supply.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3db80-121">Se også</span><span class="sxs-lookup"><span data-stu-id="3db80-121">See Also</span></span>  
 <span data-ttu-id="3db80-122">[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="3db80-122">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="3db80-123">[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="3db80-123">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="3db80-124">[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="3db80-124">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="3db80-125">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="3db80-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
