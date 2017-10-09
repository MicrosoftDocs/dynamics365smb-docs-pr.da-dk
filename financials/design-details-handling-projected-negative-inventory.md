---
title: "Designoplysninger – Håndtering af forventet negativt lager | Microsoft Docs"
description: "Genbestillingspunktet udtrykker det forventede behov under leveringstiden for varen. Når genbestillingspunktet er overskredet, er det tid til at bestille mere. Men den forventede lagerbeholdning skal være stor nok til at dække behovet, indtil den nye ordre er modtaget. I mellemtiden bør sikkerhedslageret tage højde for udsving i behov op til et målrettet serviceniveau."
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
ms.openlocfilehash: 3436e2a00858a1dbfcbb0a44cb9db32bd7665593
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-handling-projected-negative-inventory"></a><span data-ttu-id="98450-106">Designoplysninger: Håndtering af forventet negativt lager</span><span class="sxs-lookup"><span data-stu-id="98450-106">Design Details: Handling Projected Negative Inventory</span></span>
<span data-ttu-id="98450-107">Genbestillingspunktet udtrykker det forventede behov under leveringstiden for varen.</span><span class="sxs-lookup"><span data-stu-id="98450-107">The reorder point expresses the anticipated demand during the lead time of the item.</span></span> <span data-ttu-id="98450-108">Når genbestillingspunktet er overskredet, er det tid til at bestille mere.</span><span class="sxs-lookup"><span data-stu-id="98450-108">When the reorder point is passed, it is time to order more.</span></span> <span data-ttu-id="98450-109">Men den forventede lagerbeholdning skal være stor nok til at dække behovet, indtil den nye ordre er modtaget.</span><span class="sxs-lookup"><span data-stu-id="98450-109">But the projected inventory must be large enough to cover the demand until the new order is received.</span></span> <span data-ttu-id="98450-110">I mellemtiden bør sikkerhedslageret tage højde for udsving i behov op til et målrettet serviceniveau.</span><span class="sxs-lookup"><span data-stu-id="98450-110">Meanwhile, the safety stock should take care of fluctuations in demand up to a targeted service level.</span></span>  

 <span data-ttu-id="98450-111">Derfor anser planlægningssystemet det for en nødsituation, hvis et fremtidigt behov ikke kan dækkes fra den forventede lagerbeholdning, eller udtrykt på en anden måde, hvis den forventede lagerbeholdning bliver negativ.</span><span class="sxs-lookup"><span data-stu-id="98450-111">Consequently, the planning system considers it an emergency if a future demand cannot be served from the projected inventory, or expressed in another way, that the projected inventory goes negative.</span></span> <span data-ttu-id="98450-112">Systemet håndterer en sådan undtagelse ved at foreslå en ny forsyningsordre for at imødekomme en del af det behov, som ikke kan opfyldes af lagerbeholdningen eller andre forsyninger.</span><span class="sxs-lookup"><span data-stu-id="98450-112">The system deals with such an exception by suggesting a new supply order to meet the part of the demand that cannot be met by inventory or other supply.</span></span> <span data-ttu-id="98450-113">Ordrestørrelsen på den nye forsyningsordre vil ikke tage det maksimale lager eller genbestillingsantal i betragtning og vil heller ikke tage ordremodifikatorerne Maks. ordrestørrelse, Min. ordrestørrelse og Oprundingsfaktor i betragtning.</span><span class="sxs-lookup"><span data-stu-id="98450-113">The order size of the new supply order will not take the maximum inventory or the reorder quantity into consideration, nor will it take into consideration the order modifiers Maximum Order Quantity, Minimum Order Quantity, and Order Multiple.</span></span> <span data-ttu-id="98450-114">I stedet afspejler den nøjagtig mangel.</span><span class="sxs-lookup"><span data-stu-id="98450-114">Instead, it will reflect the exact deficiency.</span></span>  

 <span data-ttu-id="98450-115">Planlægningslinjen for denne type forsyningsordre viser et Nødsituation-advarselsikon, og yderligere oplysninger kan findes ved opslag for at informere brugeren om situationen.</span><span class="sxs-lookup"><span data-stu-id="98450-115">The planning line for this type of supply order will display an Emergency warning icon, and additional information will be provided upon lookup to inform the user of the situation.</span></span>  

 <span data-ttu-id="98450-116">I følgende illustration repræsenterer forsynings-id en akutordre for at justere for negativt lager.</span><span class="sxs-lookup"><span data-stu-id="98450-116">In the following illustration, supply D represents an emergency order to adjust for negative inventory.</span></span>  

 ![](media/nav_app_supply_planning_2_negative_inventory.png "NAV_APP_supply_planning_2_negative_inventory")  

1.  <span data-ttu-id="98450-117">Forsyning **A**, oprindeligt planlagte lagerbeholdning, er under genbestillingspunkt.</span><span class="sxs-lookup"><span data-stu-id="98450-117">Supply **A**, initial projected inventory, is below reorder point.</span></span>  

2.  <span data-ttu-id="98450-118">En ny ordre, der er planlagt fremad, oprettes (**C**).</span><span class="sxs-lookup"><span data-stu-id="98450-118">A new forward-scheduled supply is created (**C**).</span></span>  

     <span data-ttu-id="98450-119">(Antal = Maks. lagerbeholdning – Forventet lagerbeholdning)</span><span class="sxs-lookup"><span data-stu-id="98450-119">(Quantity = Maximum Inventory – Projected Inventory Level)</span></span>  

3.  <span data-ttu-id="98450-120">Forsyning **A** er lukket af behov **B**, som ikke fuldt ud dækkes.</span><span class="sxs-lookup"><span data-stu-id="98450-120">Supply **A** is closed by demand **B**, which is not fully covered.</span></span>  

     <span data-ttu-id="98450-121">(Behov **B** kunne forsøge at planlægge forsyning C, men det vil ikke ske i overensstemmelse med intervalkonceptet).</span><span class="sxs-lookup"><span data-stu-id="98450-121">(Demand **B** could try to schedule Supply C in but that will not happen according to the time-bucket concept.)</span></span>  

4.  <span data-ttu-id="98450-122">Ny forsyning (**D**) er oprettet for at dække det resterende antal efter behov **B**.</span><span class="sxs-lookup"><span data-stu-id="98450-122">New supply (**D**) is created to cover the remaining quantity on Demand **B**.</span></span>  

5.  <span data-ttu-id="98450-123">Behov **B** er lukket (oprettelse af en påmindelse til den forventede lagerbeholdning).</span><span class="sxs-lookup"><span data-stu-id="98450-123">Demand **B** is closed (creating a reminder to the projected inventory).</span></span>  

6.  <span data-ttu-id="98450-124">Den nye forsyning **D** er lukket.</span><span class="sxs-lookup"><span data-stu-id="98450-124">The new supply **D** is closed.</span></span>  

7.  <span data-ttu-id="98450-125">Planlagt lagerbeholdning kontrolleres, og genbestillingspunkt er ikke krydset.</span><span class="sxs-lookup"><span data-stu-id="98450-125">Projected Inventory is checked; reorder point has not been crossed.</span></span>  

8.  <span data-ttu-id="98450-126">Forsyning **C** er lukket (der findes ingen yderligere behov).</span><span class="sxs-lookup"><span data-stu-id="98450-126">Supply **C** is closed (no more demand exists).</span></span>  

9. <span data-ttu-id="98450-127">Sidste kontrol: Der findes ingen udestående påmindelser om lagerniveau.</span><span class="sxs-lookup"><span data-stu-id="98450-127">Final check: No outstanding inventory level reminders exist.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="98450-128">Trin 4 afspejler, hvordan systemet reagerer i versioner tidligere end Microsoft Dynamics NAV 2009 SP1.</span><span class="sxs-lookup"><span data-stu-id="98450-128">Step 4 reflects how the system reacts in versions earlier than Microsoft Dynamics NAV 2009 SP1.</span></span>  

 <span data-ttu-id="98450-129">Dette afslutter beskrivelsen af de centrale principper vedrørende lagerplanlægning baseret på genbestillingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="98450-129">This concludes the description of central principles relating to inventory planning based on reordering policies.</span></span> <span data-ttu-id="98450-130">I følgende afsnit beskrives karakteristika for de fire understøttede genbestillingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="98450-130">The following section describes the characteristics of the four supported reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="98450-131">Se også</span><span class="sxs-lookup"><span data-stu-id="98450-131">See Also</span></span>  
 <span data-ttu-id="98450-132">[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="98450-132">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="98450-133">[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="98450-133">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="98450-134">[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="98450-134">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="98450-135">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="98450-135">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

