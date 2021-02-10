---
title: Om planlægningsfunktioner | Microsoft Docs
description: Planlægningssystemet tager højde for alle oplysninger om efterspørgsel og udbud, tæller resultaterne sammen og opretter forslag til, hvordan udbuddet kan afstemmes, så det passer til efterspørgslen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 12ab5bbc374e40d029acaec27c7eb3596fe19d1a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759463"
---
# <a name="about-planning-functionality"></a><span data-ttu-id="c1a69-103">Om planlægningsfunktionen</span><span class="sxs-lookup"><span data-stu-id="c1a69-103">About Planning Functionality</span></span>

<span data-ttu-id="c1a69-104">Planlægningssystemet tager højde for alle oplysninger om efterspørgsel og udbud, tæller resultaterne sammen og opretter forslag til, hvordan udbuddet kan afstemmes, så det passer til efterspørgslen.</span><span class="sxs-lookup"><span data-stu-id="c1a69-104">The planning system takes all demand and supply data into account, nets the results, and creates suggestions for balancing the supply to meet the demand.</span></span>  

<span data-ttu-id="c1a69-105">Du kan finde detaljerede oplysninger i [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)</span><span class="sxs-lookup"><span data-stu-id="c1a69-105">For detailed information, see [Design Details: Supply Planning](design-details-supply-planning.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="c1a69-106">Læs værktøjstippet for alle felter, der er nævnt i dette emne, for at forstå deres funktion.</span><span class="sxs-lookup"><span data-stu-id="c1a69-106">For all the fields that are mentioned in this topic, read the tooltip to understand their function.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a><span data-ttu-id="c1a69-107">Behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="c1a69-107">Demand and Supply</span></span>

<span data-ttu-id="c1a69-108">I planlægningen indgår to elementer, udbud og efterspørgsel, som her kaldes behov og forsyning.</span><span class="sxs-lookup"><span data-stu-id="c1a69-108">Planning has two elements: demand and supply.</span></span> <span data-ttu-id="c1a69-109">Der skal opretholdes en balance mellem disse to elementer, så det kan sikres, at behovet imødekommes rettidigt og på en økonomisk fornuftig måde.</span><span class="sxs-lookup"><span data-stu-id="c1a69-109">These must be held in balance to ensure that the demand is met in a timely and cost-efficient manner.</span></span>  

- <span data-ttu-id="c1a69-110">Behov er fællesbetegnelsen for enhver form for bruttobehov, såsom en salgsordre, serviceordre, komponentbehov fra montage eller produktionsordrer, udgående overflytning, rammeordre eller forecast.</span><span class="sxs-lookup"><span data-stu-id="c1a69-110">Demand is the common term used for any kind of gross requirement such as a sales order, service order, component need from assembly or production orders, outbound transfer, blanket order or forecast.</span></span> <span data-ttu-id="c1a69-111">Herudover kan programmet håndtere andre tekniske behovstyper - som en negativ produktions- eller købsordre, negativ lagerbeholdning og købsreturvarer.</span><span class="sxs-lookup"><span data-stu-id="c1a69-111">In addition to these, application allows some other technical types of demand - such as a negative production or purchase order, negative inventory, and purchase return.</span></span>  
- <span data-ttu-id="c1a69-112">Forsyning er fællesbetegnelsen for enhver form for genanskaffelse som lagerbeholdning, en købsordre, montage eller produktionsordre eller indgående overflytning.</span><span class="sxs-lookup"><span data-stu-id="c1a69-112">Supply is the common word used for any kind of replenishment such as inventory, a purchase order, assembly order, production order, or inbound transfer.</span></span> <span data-ttu-id="c1a69-113">Tilsvarende kan der være en negativ salgs- eller serviceordre, et negativt komponentbehov eller salgsreturvarer – som alle på en eller anden måde repræsenterer forsyning.</span><span class="sxs-lookup"><span data-stu-id="c1a69-113">Correspondingly, there can be a negative sales or service order, negative component need or sales return – all of which in some way also represent supply.</span></span>  

<span data-ttu-id="c1a69-114">Et andet formål med planlægningssystemet er at sikre, at lagerbeholdningen ikke vokser unødvendigt.</span><span class="sxs-lookup"><span data-stu-id="c1a69-114">Another goal of the planning system is to ensure that the inventory does not grow unnecessarily.</span></span> <span data-ttu-id="c1a69-115">Hvis behovet falder, kan planlægningssystemet foreslå, at du udskyder eksisterende genbestillingsordrer, angiver mindre antal til dem eller helt annullerer dem.</span><span class="sxs-lookup"><span data-stu-id="c1a69-115">In the case of decreasing demand, the planning system will suggest that you postpone, decrease in quantity, or cancel existing replenishment orders.</span></span>  

## <a name="planning-calculation"></a><span data-ttu-id="c1a69-116">Planlægningsberegning</span><span class="sxs-lookup"><span data-stu-id="c1a69-116">Planning Calculation</span></span>

<span data-ttu-id="c1a69-117">Udgangspunktet for planlægningssystemet er forventet og faktisk efterspørgsel fra kunderne, dvs. kundebehov og forskellige faktorer i forbindelse med genbestilling af varer til lageret.</span><span class="sxs-lookup"><span data-stu-id="c1a69-117">The planning system is driven by anticipated and actual customer demand, as well as inventory reordering parameters.</span></span> <span data-ttu-id="c1a69-118">Når planlægningsberegningen køres, foreslås det (i form af aktionsmeddelelser), at der tages bestemte forholdsregler, som f.eks. kan være genbestilling fra leverandører, overflytninger mellem lagersteder eller produktion.</span><span class="sxs-lookup"><span data-stu-id="c1a69-118">Running the planning calculation will result in application suggesting specific actions (Action Messages) to take concerning possible replenishment from vendors, transfers between warehouses, or production.</span></span> <span data-ttu-id="c1a69-119">Hvis der allerede findes genbestillingsordrer, kan den foreslåede aktivitet f.eks. være at øge eller fremskynde ordrerne for på den måde at imødekomme det ændrede behov.</span><span class="sxs-lookup"><span data-stu-id="c1a69-119">If replenishment orders already exist, the suggested actions could be to increase or expedite the orders to meet the changes in demand.</span></span>  

<span data-ttu-id="c1a69-120">Udgangspunktet for selve planlægningen er beregningen fra brutto til netto.</span><span class="sxs-lookup"><span data-stu-id="c1a69-120">The basis of the planning routine is in the gross-to-net calculation.</span></span> <span data-ttu-id="c1a69-121">Et nettobehov udløser frigivelse af planlagte ordrer, som planlægges på basis af ruteoplysningerne (producerede varer) eller på basis af fremskaffelsestiden på varekortet (købte varer).</span><span class="sxs-lookup"><span data-stu-id="c1a69-121">Net requirements drive planned order releases, which are scheduled based on the routing information (manufactured items) or the item card lead time (purchased items).</span></span> <span data-ttu-id="c1a69-122">De antal, der frigives i en planlagt ordre, afhænger af planlægningsberegningen og påvirkes af de parametre, der er angivet på de enkelte varekort.</span><span class="sxs-lookup"><span data-stu-id="c1a69-122">Planned order release quantities are based on the planning calculation, and are affected by the parameters set on the individual item cards.</span></span>  

## <a name="planning-with-manual-transfer-orders"></a><span data-ttu-id="c1a69-123">Planlægge med manuelle overflytningsordrer</span><span class="sxs-lookup"><span data-stu-id="c1a69-123">Planning with Manual Transfer Orders</span></span>

<span data-ttu-id="c1a69-124">Som det fremgår af feltet **Genbestillingssystem** på et lagerkort, kan planlægningssystemet indstilles til at oprette overflytningsordrer, der udjævner udbud og efterspørgsel på tværs af lokationer.</span><span class="sxs-lookup"><span data-stu-id="c1a69-124">As you can see from the **Replenishment System** field on a SKU card, the planning system can be set up to create transfer orders to balance supply and demand across locations.</span></span>  

<span data-ttu-id="c1a69-125">Ud over disse automatiske overflytningsordrer kan du undertiden have brug for at udføre en almindelig flytning af lagerbeholdning til en anden lokation, uanset det nuværende behov.</span><span class="sxs-lookup"><span data-stu-id="c1a69-125">In addition to such automatic transfer orders, you may sometimes need to perform a general move of inventory quantities to another location, irrespective of existing demand.</span></span> <span data-ttu-id="c1a69-126">Til det formål skal du manuelt oprette en overflytningsordre på det antal, der skal flyttes.</span><span class="sxs-lookup"><span data-stu-id="c1a69-126">For this purpose you would manually create a transfer order for the quantity to move.</span></span> <span data-ttu-id="c1a69-127">For at sikre, at planlægningssystemet ikke forsøger at justere den manuelle overflytningsordre, skal du indstille **Planlægningsfleksibilitet** på overflytningslinjerne til Ingen.</span><span class="sxs-lookup"><span data-stu-id="c1a69-127">To ensure that the planning system does not try to manipulate this manual transfer order, you must set the **Planning Flexibility** on the transfer line(s) to None.</span></span>  

<span data-ttu-id="c1a69-128">Hvis du derimod ønsker, at planlægningssystemet justerer overflytningsordrens antal og datoer i forhold til det nuværende behov, skal du indstille feltet **Planlægningsfleksibilitet** til standardværdien, Ubegrænset.</span><span class="sxs-lookup"><span data-stu-id="c1a69-128">Contrarily, if you do want the planning system to adjust the transfer order quantities and dates to existing demand, you must set the **Planning Flexibility** field to the default value, Unlimited.</span></span>

## <a name="planning-parameters"></a><span data-ttu-id="c1a69-129">Planlægningsparametre</span><span class="sxs-lookup"><span data-stu-id="c1a69-129">Planning Parameters</span></span>

<span data-ttu-id="c1a69-130">Planlægningsparametrene bestemmer, hvornår, hvor meget og hvordan der genbestilles på basis af de forskellige indstillinger på varekortet (eller lagervare) og produktionsopsætningen.</span><span class="sxs-lookup"><span data-stu-id="c1a69-130">The planning parameters control when, how much, and how to replenish based on the various settings on the item card (or stockkeeping unit - SKU), and the manufacturing setup.</span></span>  

<span data-ttu-id="c1a69-131">Der findes følgende planlægningsparametrene på vare- eller lagerkortet:</span><span class="sxs-lookup"><span data-stu-id="c1a69-131">The following planning parameters exist on the item or SKU card:</span></span>  

- <span data-ttu-id="c1a69-132">Bufferperiode</span><span class="sxs-lookup"><span data-stu-id="c1a69-132">Dampener Period</span></span>  
- <span data-ttu-id="c1a69-133">Buffermængde</span><span class="sxs-lookup"><span data-stu-id="c1a69-133">Dampener Quantity</span></span>  
- <span data-ttu-id="c1a69-134">Genbestillingsmetode</span><span class="sxs-lookup"><span data-stu-id="c1a69-134">Reordering Policy</span></span>  
- <span data-ttu-id="c1a69-135">Genbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="c1a69-135">Reorder Point</span></span>
- <span data-ttu-id="c1a69-136">Maks. lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c1a69-136">Maximum Inventory</span></span>  
- <span data-ttu-id="c1a69-137">Overløbsniveau</span><span class="sxs-lookup"><span data-stu-id="c1a69-137">Overflow Level</span></span>  
- <span data-ttu-id="c1a69-138">Interval</span><span class="sxs-lookup"><span data-stu-id="c1a69-138">Time Bucket</span></span>  
- <span data-ttu-id="c1a69-139">Akkumuleringsperiode for lot</span><span class="sxs-lookup"><span data-stu-id="c1a69-139">Lot Accumulation Period</span></span>  
- <span data-ttu-id="c1a69-140">Ændringsperiode</span><span class="sxs-lookup"><span data-stu-id="c1a69-140">Rescheduling Period</span></span>  
- <span data-ttu-id="c1a69-141">Ordrekvantum</span><span class="sxs-lookup"><span data-stu-id="c1a69-141">Reorder Quantity</span></span>  
- <span data-ttu-id="c1a69-142">Sikkerhedstid</span><span class="sxs-lookup"><span data-stu-id="c1a69-142">Safety Lead Time</span></span>  
- <span data-ttu-id="c1a69-143">Sikkerhedslager</span><span class="sxs-lookup"><span data-stu-id="c1a69-143">Safety Stock Quantity</span></span>  
- <span data-ttu-id="c1a69-144">Montagepolitik</span><span class="sxs-lookup"><span data-stu-id="c1a69-144">Assembly Policy</span></span>  
- <span data-ttu-id="c1a69-145">Produktionsmetode</span><span class="sxs-lookup"><span data-stu-id="c1a69-145">Manufacturing Policy</span></span>  

<span data-ttu-id="c1a69-146">Der findes følgende ordremodifikatorer på vare- eller lagerkortet:</span><span class="sxs-lookup"><span data-stu-id="c1a69-146">The following order modifiers exist on the item or SKU card:</span></span>  

- <span data-ttu-id="c1a69-147">Min. ordrestørrelse</span><span class="sxs-lookup"><span data-stu-id="c1a69-147">Minimum Order Quantity</span></span>  
- <span data-ttu-id="c1a69-148">Maks. ordrestørrelse</span><span class="sxs-lookup"><span data-stu-id="c1a69-148">Maximum Order Quantity</span></span>  
- <span data-ttu-id="c1a69-149">Oprundingsfaktor</span><span class="sxs-lookup"><span data-stu-id="c1a69-149">Order Multiple</span></span>  

<span data-ttu-id="c1a69-150">Globale planlægningsopsætningsfelter på siden **Produktionsopsætning** omfatter:</span><span class="sxs-lookup"><span data-stu-id="c1a69-150">Global planning setup fields on the **Manufacturing Setup** page include:</span></span>  

- <span data-ttu-id="c1a69-151">Dynamisk laveste-niveau-kode</span><span class="sxs-lookup"><span data-stu-id="c1a69-151">Dynamic Low-Level Code</span></span>  
- <span data-ttu-id="c1a69-152">Aktuel behovsprognose</span><span class="sxs-lookup"><span data-stu-id="c1a69-152">Current Demand Forecast</span></span>  
- <span data-ttu-id="c1a69-153">Forecast på lokationer</span><span class="sxs-lookup"><span data-stu-id="c1a69-153">Use Forecast on Locations</span></span>  
- <span data-ttu-id="c1a69-154">Standardsikkerhedstid</span><span class="sxs-lookup"><span data-stu-id="c1a69-154">Default Safety Lead Time</span></span>  
- <span data-ttu-id="c1a69-155">Tomt overløbsniveau</span><span class="sxs-lookup"><span data-stu-id="c1a69-155">Blank Overflow Level</span></span>  
- <span data-ttu-id="c1a69-156">Komb. hovedplan-/MRP-beregning</span><span class="sxs-lookup"><span data-stu-id="c1a69-156">Combined MPS/MRP Calculation</span></span>
- <span data-ttu-id="c1a69-157">Komponenter på lokation</span><span class="sxs-lookup"><span data-stu-id="c1a69-157">Components at Location</span></span>  
- <span data-ttu-id="c1a69-158">Standardbufferperiode</span><span class="sxs-lookup"><span data-stu-id="c1a69-158">Default Dampener Period</span></span>  
- <span data-ttu-id="c1a69-159">Standardbufferantal</span><span class="sxs-lookup"><span data-stu-id="c1a69-159">Default Dampener Quantity</span></span>  

<span data-ttu-id="c1a69-160">Du kan finde flere oplysninger i [Designoplysninger: planlægningsparametre](design-details-planning-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="c1a69-160">For more information, see [Design Details: Planning Parameters](design-details-planning-parameters.md)</span></span>  

## <a name="other-important-planning-fields"></a><span data-ttu-id="c1a69-161">Andre vigtige felter til planlægning</span><span class="sxs-lookup"><span data-stu-id="c1a69-161">Other Important Planning Fields</span></span>

### <a name="planning-flexibility"></a><span data-ttu-id="c1a69-162">Planlægningsfleksibilitet</span><span class="sxs-lookup"><span data-stu-id="c1a69-162">Planning Flexibility</span></span>

<span data-ttu-id="c1a69-163">I de fleste forsyningsordrer, f.eks. produktionsordrer, kan du vælge **Ubegrænset** eller **Ingen** i feltet **Planlægningsfleksibilitet** på linjerne.</span><span class="sxs-lookup"><span data-stu-id="c1a69-163">On most supply orders, such as production orders, you can select **Unlimited** or **None** in the **Planning Flexibility** field on the lines.</span></span>

<span data-ttu-id="c1a69-164">Det angiver, om der tages højde for forsyningen repræsenteret af produktionsordrelinjen i planlægningssystemet, når der beregnes aktionsmeddelelser.</span><span class="sxs-lookup"><span data-stu-id="c1a69-164">This specifies whether the supply represented by the production order line is considered by the planning system when calculating action messages.</span></span>
<span data-ttu-id="c1a69-165">Hvis feltet viser indstillingen **Ubegrænset**, medtager planlægningssystemet linjen, når aktionsmeddelelsen beregnes.</span><span class="sxs-lookup"><span data-stu-id="c1a69-165">If the field contains **Unlimited**, then the planning system includes the line when calculating action messages.</span></span> <span data-ttu-id="c1a69-166">Hvis feltet indeholder indstillingen **Ingen**, er linjen fast og kan ikke ændres, og linjen medtages ikke i beregningen af aktionsmeddelelser.</span><span class="sxs-lookup"><span data-stu-id="c1a69-166">If the field contains **None**, then the line is firm and unchangeable, and the planning system does not include the line when calculating action messages.</span></span>

### <a name="warning"></a><span data-ttu-id="c1a69-167">Advarsel</span><span class="sxs-lookup"><span data-stu-id="c1a69-167">Warning</span></span>

<span data-ttu-id="c1a69-168">Oplysningsfeltet **Advarsel** på siden **Planlægningskladde** viser eventuelle planlægningslinjer, der er oprettet til en usædvanlig situation med en tekst, som brugeren kan vælge for at få yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="c1a69-168">The **Warning** information field on the **Planning Worksheet** page informs you of any planning line created for an unusual situation with a text, which the user can choose to read additional information.</span></span> <span data-ttu-id="c1a69-169">Der findes følgende advarselstyper:</span><span class="sxs-lookup"><span data-stu-id="c1a69-169">The following warning types exist:</span></span>

- <span data-ttu-id="c1a69-170">Nødsituation</span><span class="sxs-lookup"><span data-stu-id="c1a69-170">Emergency</span></span>
- <span data-ttu-id="c1a69-171">Undtagelse</span><span class="sxs-lookup"><span data-stu-id="c1a69-171">Exception</span></span>
- <span data-ttu-id="c1a69-172">Bemærk!</span><span class="sxs-lookup"><span data-stu-id="c1a69-172">Attention</span></span>
- <span data-ttu-id="c1a69-173">Nødsituation</span><span class="sxs-lookup"><span data-stu-id="c1a69-173">Emergency</span></span>

<span data-ttu-id="c1a69-174">Denne advarsel vises i to tilfælde:</span><span class="sxs-lookup"><span data-stu-id="c1a69-174">The emergency warning is displayed in two situations:</span></span>

- <span data-ttu-id="c1a69-175">Når lageret er negativt på den planlagte startdato.</span><span class="sxs-lookup"><span data-stu-id="c1a69-175">The inventory is negative on the planning starting date.</span></span>
- <span data-ttu-id="c1a69-176">Når der er antedaterede udbuds- eller efterspørgselshændelser.</span><span class="sxs-lookup"><span data-stu-id="c1a69-176">Back-dated supply or demand events exist.</span></span>

<span data-ttu-id="c1a69-177">Hvis varens lager er negativt på den planlagte startdato, foreslår planlægningssystemet en nødforsyningsordre for den negative mængde, som skal ankomme på den planlagte startdato.</span><span class="sxs-lookup"><span data-stu-id="c1a69-177">If an item's inventory is negative on the planning starting date, the planning system suggests an emergency supply order for the negative quantity to arrive on the planning starting date.</span></span> <span data-ttu-id="c1a69-178">Advarslen angiver startdatoen og mængden for nødordren.</span><span class="sxs-lookup"><span data-stu-id="c1a69-178">The warning text states the starting date and the quantity of the emergency order.</span></span>

<span data-ttu-id="c1a69-179">Evt. dokumentlinjer med forfaldsdatoer før den planlagte startdato konsolideres i én nødforsyningsordre, så varen kan ankomme på den planlagte startdato.</span><span class="sxs-lookup"><span data-stu-id="c1a69-179">Any document lines with due dates before the planning starting date are consolidated into one emergency supply order for the item to arrive on the planning starting date.</span></span>

### <a name="exception"></a><span data-ttu-id="c1a69-180">Undtagelse</span><span class="sxs-lookup"><span data-stu-id="c1a69-180">Exception</span></span>

<span data-ttu-id="c1a69-181">Advarslen om undtagelsen vises, hvis det forventede disponible lager kommer under sikkerhedslageret.</span><span class="sxs-lookup"><span data-stu-id="c1a69-181">The exception warning is displayed if the projected available inventory drops below the safety stock quantity.</span></span>

<span data-ttu-id="c1a69-182">Planlægningssystemet foreslår en forsyningsordre, der skal opfylde behovet på forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="c1a69-182">The planning system will suggest a supply order to meet the demand on its due date.</span></span> <span data-ttu-id="c1a69-183">Advarslen angiver varemængden på sikkerhedslageret og den dato, hvor den overtrædes.</span><span class="sxs-lookup"><span data-stu-id="c1a69-183">The warning text states the item's safety stock quantity and the date on which it is violated.</span></span>

<span data-ttu-id="c1a69-184">Overskridelse af niveauet for sikkerhedslageret anses for at være en undtagelse, fordi det ikke bør forekomme, hvis genbestillingspunktet er angivet korrekt.</span><span class="sxs-lookup"><span data-stu-id="c1a69-184">Violating the safety stock level is considered an exception because it should not occur if the reorder point has been set correctly.</span></span>

> [!NOTE]
> <span data-ttu-id="c1a69-185">Efterspørgsel på planlægningslinjer med undtagelsesadvarsler modificeres normalt ikke i henhold til planlægningsparametre.</span><span class="sxs-lookup"><span data-stu-id="c1a69-185">Supply on planning lines with Exception warnings is normally not modified according to planning parameters.</span></span> <span data-ttu-id="c1a69-186">Planlægningssystemet foreslår i stedet for kun en forsyning til at dække det nøjagtige behovsantal.</span><span class="sxs-lookup"><span data-stu-id="c1a69-186">Instead, the planning system only suggests a supply to cover the exact demand quantity.</span></span> <span data-ttu-id="c1a69-187">Du kan dog konfigurere planlægningskørslen til at overholde bestemte planlægningsparametre for planlægningslinjer med visse advarsler.</span><span class="sxs-lookup"><span data-stu-id="c1a69-187">However, you can set the planning run up to respect certain planning parameters for planning lines with certain warnings.</span></span> <span data-ttu-id="c1a69-188">Du kan finde flere oplysninger i beskrivelsen af feltet **Respekter advarsler om undtagelser for planlægningsparametre** i artiklen [Kør fuld planlægning, MPS eller MRP](production-how-to-run-mps-and-mrp.md).</span><span class="sxs-lookup"><span data-stu-id="c1a69-188">For more information, see the description for the **Respect Planning Parameters for Exception Warnings** field in the [Run Full Planning, MPS or MRP](production-how-to-run-mps-and-mrp.md) article.</span></span>

### <a name="attention"></a><span data-ttu-id="c1a69-189">Bemærk</span><span class="sxs-lookup"><span data-stu-id="c1a69-189">Attention</span></span>

<span data-ttu-id="c1a69-190">Denne advarsel vises i to tilfælde:</span><span class="sxs-lookup"><span data-stu-id="c1a69-190">The attention warning is displayed in two situations:</span></span>

- <span data-ttu-id="c1a69-191">Når den planlagte startdato ligger før arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="c1a69-191">The planning starting date is earlier than the work date.</span></span>
- <span data-ttu-id="c1a69-192">Når planlægningslinjen foreslår at ændre en frigivet købs- eller produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="c1a69-192">The planning line suggests to change a released purchase or production order.</span></span>

> [!NOTE]
> <span data-ttu-id="c1a69-193">På planlægningslinjer med advarsler er feltet **Accepter aktionsmeddelelse** ikke markeret, fordi planlæggeren forventes at undersøge disse linjer nærmere, før planen udføres.</span><span class="sxs-lookup"><span data-stu-id="c1a69-193">In planning lines with warnings, the **Accept Action Message** field is not selected, because the planner is expected to further investigate these lines before carrying out the plan.</span></span>

## <a name="planning-worksheets-and-requisition-worksheets"></a><span data-ttu-id="c1a69-194">Planlægningskladder og indkøbskladder</span><span class="sxs-lookup"><span data-stu-id="c1a69-194">Planning worksheets and requisition worksheets</span></span>

<span data-ttu-id="c1a69-195">Som beskrevet under [Planlægning](production-planning.md) kan du vælge mellem to kladder til de fleste planlægningsaktiviteter, planlægningskladden og indkøbskladden.</span><span class="sxs-lookup"><span data-stu-id="c1a69-195">As described in [Planning](production-planning.md), you can choose between two worksheets for most planning activities, the planning worksheet and the requisition worksheet.</span></span> <span data-ttu-id="c1a69-196">De fleste processer beskrives på basis af planlægningskladden, men der er et par scenarier, hvor indkøbskladden foretrækkes.</span><span class="sxs-lookup"><span data-stu-id="c1a69-196">Most processes are described based on the planning worksheet, but there are a couple of scenarios where the requisition worksheet is preferred.</span></span>

### <a name="requisition-worksheet"></a><span data-ttu-id="c1a69-197">Indkøbskladde</span><span class="sxs-lookup"><span data-stu-id="c1a69-197">Requisition worksheet</span></span>

<span data-ttu-id="c1a69-198">Siden **Indkøbskladde** viser de varer, du vil bestille.</span><span class="sxs-lookup"><span data-stu-id="c1a69-198">The **Requisition Worksheet** page lists items that you want to order.</span></span> <span data-ttu-id="c1a69-199">Du kan indsætte varer i kladden på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="c1a69-199">You can enter items in the worksheet in the following ways:</span></span>

- <span data-ttu-id="c1a69-200">Indsæt varerne manuelt i kladden, og udfyld de relevante felter.</span><span class="sxs-lookup"><span data-stu-id="c1a69-200">Enter the items manually in the worksheet and fill in the relevant fields.</span></span>

- <span data-ttu-id="c1a69-201">Brug kørslen **Beregn plan**.</span><span class="sxs-lookup"><span data-stu-id="c1a69-201">Use the **Calculate Plan** batch job.</span></span> <span data-ttu-id="c1a69-202">Herved opstilles en genbestillingsplan for varer og enheder, der er oprettet med et genbestillingssystem, der er sat til **Køb** eller **Overførsel**.</span><span class="sxs-lookup"><span data-stu-id="c1a69-202">This calculates a replenishment plan for items and stockkeeping units that have been set up with a replenishment system of **Purchase** or **Transfer**.</span></span> <span data-ttu-id="c1a69-203">Når du udfører denne kørsel, udfyldes feltet **Aktionsmeddelelse** automatisk med en foreslået handling, som du kan udføre for at genbestille varen.</span><span class="sxs-lookup"><span data-stu-id="c1a69-203">When you use this batch job, the program automatically fills in the **Action Message** field with a suggestion for an action you can take to replenish the item.</span></span> <span data-ttu-id="c1a69-204">Det kan f.eks. være at øge vareantallet på en eksisterende ordre eller oprette en ny ordre.</span><span class="sxs-lookup"><span data-stu-id="c1a69-204">This could be increasing the item quantity on an existing order or creating a new order, for example.</span></span>

- <span data-ttu-id="c1a69-205">Hvis du har brugt kørslen **Beregn plan** fra siden **Planlægningskladde** til at opstille en genbestillingsplan, kan du bruge kørslen **Udfør aktionsmeddelelse** til at kopiere forslag til købs- og overflytningsordrer fra planlægningskladden til indkøbskladden.</span><span class="sxs-lookup"><span data-stu-id="c1a69-205">If you have used the **Calculate Plan** batch job from the **Planning Worksheet** page to calculate a replenishment plan, you can use the **Carry Out Action Message** batch job to copy purchase and transfer order proposals from the planning worksheet to the requisition worksheet.</span></span> <span data-ttu-id="c1a69-206">Dette er praktisk, hvis forskellige brugere er ansvarlige for at håndtere produktionsordrer og købs- eller overflytningsordrer.</span><span class="sxs-lookup"><span data-stu-id="c1a69-206">This is practical if separate users are responsible for handling production orders and purchase/transfer orders.</span></span>

- <span data-ttu-id="c1a69-207">Du kan bruge handlingen **Direkte levering** til at udfylde linjerne i indkøbskladden.</span><span class="sxs-lookup"><span data-stu-id="c1a69-207">You can use the **Drop Shipment** action to fill in the requisition worksheet lines.</span></span> <span data-ttu-id="c1a69-208">Denne handling bruger kørslen **Hent salgsordrer** til at finde de salgsordrelinjer, som du vil ekspedere i en direkte levering.</span><span class="sxs-lookup"><span data-stu-id="c1a69-208">This action uses the **Get Sales Orders** batch job to determine the sales order lines that you want to designate for a drop shipment.</span></span>

- <span data-ttu-id="c1a69-209">Du kan bruge handlingen **Specialordre** til at udfylde linjerne i indkøbskladden.</span><span class="sxs-lookup"><span data-stu-id="c1a69-209">You can use the **Special Order** action to fill in the requisition worksheet lines.</span></span> <span data-ttu-id="c1a69-210">Denne handling bruger kørslen **Hent salgsordrer** til at finde de salgsordrelinjer, som du vil ekspedere i en specialordre.</span><span class="sxs-lookup"><span data-stu-id="c1a69-210">This action uses the **Get Sales Orders** batch job to determine the sales order lines that you want to designate for a special order.</span></span>

<span data-ttu-id="c1a69-211">Linjerne i indkøbskladden indeholder detaljerede oplysninger om de varer, der skal genbestilles.</span><span class="sxs-lookup"><span data-stu-id="c1a69-211">Requisition worksheet lines contain detailed information about the items that need to be reordered.</span></span> <span data-ttu-id="c1a69-212">Du kan redigere og slette linjerne for at regulere genbestillingsplanen, og du kan viderebehandle linjerne ved hjælp af kørslen **Udfør aktionsmeddelelse**.</span><span class="sxs-lookup"><span data-stu-id="c1a69-212">You can edit and delete the lines to adjust your replenishment plan, and you can further process the lines by using the **Carry Out Action Message** batch job.</span></span>

<span data-ttu-id="c1a69-213">Du kan finde flere oplysninger om planlægning med lokationer og overflytninger under [Planlægning med eller uden lokationer](production-planning-with-without-locations.md).</span><span class="sxs-lookup"><span data-stu-id="c1a69-213">For details about planning with locations and transfers, see [Planning With or Without Locations](production-planning-with-without-locations.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c1a69-214">Se også</span><span class="sxs-lookup"><span data-stu-id="c1a69-214">See Also</span></span>

[<span data-ttu-id="c1a69-215">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="c1a69-215">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)  
[<span data-ttu-id="c1a69-216">Skabelon</span><span class="sxs-lookup"><span data-stu-id="c1a69-216">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="c1a69-217">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="c1a69-217">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="c1a69-218">Produktion</span><span class="sxs-lookup"><span data-stu-id="c1a69-218">Manufacturing</span></span>](production-manage-manufacturing.md)  
[<span data-ttu-id="c1a69-219">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c1a69-219">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c1a69-220">Køb</span><span class="sxs-lookup"><span data-stu-id="c1a69-220">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="c1a69-221">Konfigurere bedste fremgangsmåder: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="c1a69-221">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="c1a69-222">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c1a69-222">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
