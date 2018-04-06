---
title: "Om planlægningsfunktioner | Microsoft Docs"
description: "Planlægningssystemet tager højde for alle oplysninger om efterspørgsel og udbud, tæller resultaterne sammen og opretter forslag til, hvordan udbuddet kan afstemmes, så det passer til efterspørgslen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e00df5ac20c9fcd692919c622deb237999171fbc
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="about-planning-functionality"></a><span data-ttu-id="c9132-103">Om planlægningsfunktionen</span><span class="sxs-lookup"><span data-stu-id="c9132-103">About Planning Functionality</span></span>
<span data-ttu-id="c9132-104">Planlægningssystemet tager højde for alle oplysninger om efterspørgsel og udbud, tæller resultaterne sammen og opretter forslag til, hvordan udbuddet kan afstemmes, så det passer til efterspørgslen.</span><span class="sxs-lookup"><span data-stu-id="c9132-104">The planning system takes all demand and supply data into account, nets the results, and creates suggestions for balancing the supply to meet the demand.</span></span>  

<span data-ttu-id="c9132-105">Du kan finde detaljerede oplysninger i [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)</span><span class="sxs-lookup"><span data-stu-id="c9132-105">For detailed information, see [Design Details: Supply Planning](design-details-supply-planning.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="c9132-106">Læs værktøjstippet for alle felter, der er nævnt i dette emne, for at forstå deres funktion.</span><span class="sxs-lookup"><span data-stu-id="c9132-106">For all the fields that are mentioned in this topic, read the tooltip to understand their function.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a><span data-ttu-id="c9132-107">Behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="c9132-107">Demand and Supply</span></span>  
<span data-ttu-id="c9132-108">I planlægningen indgår to elementer, udbud og efterspørgsel, som her kaldes behov og forsyning.</span><span class="sxs-lookup"><span data-stu-id="c9132-108">Planning has two elements: demand and supply.</span></span> <span data-ttu-id="c9132-109">Der skal opretholdes en balance mellem disse to elementer, så det kan sikres, at behovet imødekommes rettidigt og på en økonomisk fornuftig måde.</span><span class="sxs-lookup"><span data-stu-id="c9132-109">These must be held in balance to ensure that the demand is met in a timely and cost-efficient manner.</span></span>  

- <span data-ttu-id="c9132-110">Behov er fællesbetegnelsen for enhver form for bruttobehov, såsom en salgsordre, serviceordre, komponentbehov fra montage eller produktionsordrer, udgående overflytning, rammeordre eller forecast.</span><span class="sxs-lookup"><span data-stu-id="c9132-110">Demand is the common term used for any kind of gross requirement such as a sales order, service order, component need from assembly or production orders, outbound transfer, blanket order or forecast.</span></span> <span data-ttu-id="c9132-111">Herudover kan programmet håndtere andre tekniske behovstyper - som en negativ produktions- eller købsordre, negativ lagerbeholdning og købsreturvarer.</span><span class="sxs-lookup"><span data-stu-id="c9132-111">In addition to these, the program allows some other technical types of demand - such as a negative production or purchase order, negative inventory, and purchase return.</span></span>  
- <span data-ttu-id="c9132-112">Forsyning er fællesbetegnelsen for enhver form for genanskaffelse som lagerbeholdning, en købsordre, montage eller produktionsordre eller indgående overflytning.</span><span class="sxs-lookup"><span data-stu-id="c9132-112">Supply is the common word used for any kind of replenishment such as inventory, a purchase order, assembly order, production order, or inbound transfer.</span></span> <span data-ttu-id="c9132-113">Tilsvarende kan der være en negativ salgs- eller serviceordre, et negativt komponentbehov eller salgsreturvarer – som alle på en eller anden måde repræsenterer forsyning.</span><span class="sxs-lookup"><span data-stu-id="c9132-113">Correspondingly, there can be a negative sales or service order, negative component need or sales return – all of which in some way also represent supply.</span></span>  

<span data-ttu-id="c9132-114">Et andet formål med planlægningssystemet er at sikre, at lagerbeholdningen ikke vokser unødvendigt.</span><span class="sxs-lookup"><span data-stu-id="c9132-114">Another goal of the planning system is to ensure that the inventory does not grow unnecessarily.</span></span> <span data-ttu-id="c9132-115">Hvis behovet falder, kan planlægningssystemet foreslå, at du udskyder eksisterende genbestillingsordrer, angiver mindre antal til dem eller helt annullerer dem.</span><span class="sxs-lookup"><span data-stu-id="c9132-115">In the case of decreasing demand, the planning system will suggest that you postpone, decrease in quantity, or cancel existing replenishment orders.</span></span>  

## <a name="planning-calculation"></a><span data-ttu-id="c9132-116">Planlægningsberegning</span><span class="sxs-lookup"><span data-stu-id="c9132-116">Planning Calculation</span></span>  
<span data-ttu-id="c9132-117">Udgangspunktet for planlægningssystemet er forventet og faktisk efterspørgsel fra kunderne, dvs. kundebehov og forskellige faktorer i forbindelse med genbestilling af varer til lageret.</span><span class="sxs-lookup"><span data-stu-id="c9132-117">The planning system is driven by anticipated and actual customer demand, as well as inventory reordering parameters.</span></span> <span data-ttu-id="c9132-118">Når planlægningsberegningen køres, foreslås det (i form af aktionsmeddelelser), at der tages bestemte forholdsregler, som f.eks. kan være genbestilling fra leverandører, overflytninger mellem lagersteder eller produktion.</span><span class="sxs-lookup"><span data-stu-id="c9132-118">Running the planning calculation will result in the program suggesting specific actions (Action Messages) to take concerning possible replenishment from vendors, transfers between warehouses, or production.</span></span> <span data-ttu-id="c9132-119">Hvis der allerede findes genbestillingsordrer, kan den foreslåede aktivitet f.eks. være at øge eller fremskynde ordrerne for på den måde at imødekomme det ændrede behov.</span><span class="sxs-lookup"><span data-stu-id="c9132-119">If replenishment orders already exist, the suggested actions could be to increase or expedite the orders to meet the changes in demand.</span></span>  

<span data-ttu-id="c9132-120">Udgangspunktet for selve planlægningen er beregningen fra brutto til netto.</span><span class="sxs-lookup"><span data-stu-id="c9132-120">The basis of the planning routine is in the gross-to-net calculation.</span></span> <span data-ttu-id="c9132-121">Et nettobehov udløser frigivelse af planlagte ordrer, som planlægges på basis af ruteoplysningerne (producerede varer) eller på basis af fremskaffelsestiden på varekortet (købte varer).</span><span class="sxs-lookup"><span data-stu-id="c9132-121">Net requirements drive planned order releases, which are scheduled based on the routing information (manufactured items) or the item card lead time (purchased items).</span></span> <span data-ttu-id="c9132-122">De antal, der frigives i en planlagt ordre, afhænger af planlægningsberegningen og påvirkes af de parametre, der er angivet på de enkelte varekort.</span><span class="sxs-lookup"><span data-stu-id="c9132-122">Planned order release quantities are based on the planning calculation, and are affected by the parameters set on the individual item cards.</span></span>  

## <a name="planning-with-manual-transfer-orders"></a><span data-ttu-id="c9132-123">Planlægge med manuelle overflytningsordrer</span><span class="sxs-lookup"><span data-stu-id="c9132-123">Planning with Manual Transfer Orders</span></span>
<span data-ttu-id="c9132-124">Som det fremgår af feltet **Genbestillingssystem** på et lagerkort, kan planlægningssystemet indstilles til at oprette overflytningsordrer, der udjævner udbud og efterspørgsel på tværs af lokationer.</span><span class="sxs-lookup"><span data-stu-id="c9132-124">As you can see from the **Replenishment System** field on a SKU card, the planning system can be set up to create transfer orders to balance supply and demand across locations.</span></span>  

<span data-ttu-id="c9132-125">Ud over disse automatiske overflytningsordrer kan du undertiden have brug for at udføre en almindelig flytning af lagerbeholdning til en anden lokation, uanset det nuværende behov.</span><span class="sxs-lookup"><span data-stu-id="c9132-125">In addition to such automatic transfer orders, you may sometimes need to perform a general move of inventory quantities to another location, irrespective of existing demand.</span></span> <span data-ttu-id="c9132-126">Til det formål skal du manuelt oprette en overflytningsordre på det antal, der skal flyttes.</span><span class="sxs-lookup"><span data-stu-id="c9132-126">For this purpose you would manually create a transfer order for the quantity to move.</span></span> <span data-ttu-id="c9132-127">For at sikre, at planlægningssystemet ikke forsøger at justere den manuelle overflytningsordre, skal du indstille **Planlægningsfleksibilitet** på overflytningslinjerne til Ingen.</span><span class="sxs-lookup"><span data-stu-id="c9132-127">To ensure that the planning system does not try to manipulate this manual transfer order, you must set the **Planning Flexibility** on the transfer line(s) to None.</span></span>  

<span data-ttu-id="c9132-128">Hvis du derimod ønsker, at planlægningssystemet justerer overflytningsordrens antal og datoer i forhold til det nuværende behov, skal du indstille feltet **Planlægningsfleksibilitet** til standardværdien, Ubegrænset.</span><span class="sxs-lookup"><span data-stu-id="c9132-128">Contrarily, if you do want the planning system to adjust the transfer order quantities and dates to existing demand, you must set the **Planning Flexibility** field to the default value, Unlimited.</span></span>

## <a name="planning-parameters"></a><span data-ttu-id="c9132-129">Planlægningsparametre</span><span class="sxs-lookup"><span data-stu-id="c9132-129">Planning Parameters</span></span>  
<span data-ttu-id="c9132-130">Planlægningsparametrene bestemmer, hvornår, hvor meget og hvordan der genbestilles på basis af de forskellige indstillinger på varekortet (eller lagervare) og produktionsopsætningen.</span><span class="sxs-lookup"><span data-stu-id="c9132-130">The planning parameters control when, how much, and how to replenish based on the various settings on the item card (or stockkeeping unit - SKU), and the manufacturing setup.</span></span>  

<span data-ttu-id="c9132-131">Der findes følgende planlægningsparametrene på vare- eller lagerkortet:</span><span class="sxs-lookup"><span data-stu-id="c9132-131">The following planning parameters exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="c9132-132">Bufferperiode</span><span class="sxs-lookup"><span data-stu-id="c9132-132">Dampener Period</span></span>  
-   <span data-ttu-id="c9132-133">Buffermængde</span><span class="sxs-lookup"><span data-stu-id="c9132-133">Dampener Quantity</span></span>  
-   <span data-ttu-id="c9132-134">Genbestillingsmetode</span><span class="sxs-lookup"><span data-stu-id="c9132-134">Reordering Policy</span></span>  
-   <span data-ttu-id="c9132-135">Genbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="c9132-135">Reorder Point</span></span>
-   <span data-ttu-id="c9132-136">Maks. lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c9132-136">Maximum Inventory</span></span>  
-   <span data-ttu-id="c9132-137">Overløbsniveau</span><span class="sxs-lookup"><span data-stu-id="c9132-137">Overflow Level</span></span>  
-   <span data-ttu-id="c9132-138">Interval</span><span class="sxs-lookup"><span data-stu-id="c9132-138">Time Bucket</span></span>  
-   <span data-ttu-id="c9132-139">Akkumuleringsperiode for lot</span><span class="sxs-lookup"><span data-stu-id="c9132-139">Lot Accumulation Period</span></span>  
-   <span data-ttu-id="c9132-140">Ændringsperiode</span><span class="sxs-lookup"><span data-stu-id="c9132-140">Rescheduling Period</span></span>  
-   <span data-ttu-id="c9132-141">Ordrekvantum</span><span class="sxs-lookup"><span data-stu-id="c9132-141">Reorder Quantity</span></span>  
-   <span data-ttu-id="c9132-142">Sikkerhedstid</span><span class="sxs-lookup"><span data-stu-id="c9132-142">Safety Lead Time</span></span>  
-   <span data-ttu-id="c9132-143">Sikkerhedslager</span><span class="sxs-lookup"><span data-stu-id="c9132-143">Safety Stock Quantity</span></span>  
-   <span data-ttu-id="c9132-144">Montagepolitik</span><span class="sxs-lookup"><span data-stu-id="c9132-144">Assembly Policy</span></span>  
-   <span data-ttu-id="c9132-145">Produktionsmetode</span><span class="sxs-lookup"><span data-stu-id="c9132-145">Manufacturing Policy</span></span>  

<span data-ttu-id="c9132-146">Der findes følgende ordremodifikatorer på vare- eller lagerkortet:</span><span class="sxs-lookup"><span data-stu-id="c9132-146">The following order modifiers exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="c9132-147">Min. ordrestørrelse</span><span class="sxs-lookup"><span data-stu-id="c9132-147">Minimum Order Quantity</span></span>  
-   <span data-ttu-id="c9132-148">Maks. ordrestørrelse</span><span class="sxs-lookup"><span data-stu-id="c9132-148">Maximum Order Quantity</span></span>  
-   <span data-ttu-id="c9132-149">Oprundingsfaktor</span><span class="sxs-lookup"><span data-stu-id="c9132-149">Order Multiple</span></span>  

<span data-ttu-id="c9132-150">Globale planlægningsopsætningsfelter i vinduet **Produktionsopsætning** omfatter:</span><span class="sxs-lookup"><span data-stu-id="c9132-150">Global planning setup fields on the **Manufacturing Setup** window include:</span></span>  

-   <span data-ttu-id="c9132-151">Dynamisk laveste-niveau-kode</span><span class="sxs-lookup"><span data-stu-id="c9132-151">Dynamic Low-Level Code</span></span>  
-   <span data-ttu-id="c9132-152">Aktuel produktionsforecast</span><span class="sxs-lookup"><span data-stu-id="c9132-152">Current Production Forecast</span></span>  
-   <span data-ttu-id="c9132-153">Forecast på lokationer</span><span class="sxs-lookup"><span data-stu-id="c9132-153">Use Forecast on Locations</span></span>  
-   <span data-ttu-id="c9132-154">Standardsikkerhedstid</span><span class="sxs-lookup"><span data-stu-id="c9132-154">Default Safety Lead Time</span></span>  
-   <span data-ttu-id="c9132-155">Tomt overløbsniveau</span><span class="sxs-lookup"><span data-stu-id="c9132-155">Blank Overflow Level</span></span>  
-   <span data-ttu-id="c9132-156">Komb. hovedplan-/MRP-beregning</span><span class="sxs-lookup"><span data-stu-id="c9132-156">Combined MPS/MRP Calculation</span></span>   
-   <span data-ttu-id="c9132-157">Komponenter på lokation</span><span class="sxs-lookup"><span data-stu-id="c9132-157">Components at Location</span></span>  
-   <span data-ttu-id="c9132-158">Standardbufferperiode</span><span class="sxs-lookup"><span data-stu-id="c9132-158">Default Dampener Period</span></span>  
-   <span data-ttu-id="c9132-159">Standardbufferantal</span><span class="sxs-lookup"><span data-stu-id="c9132-159">Default Dampener Quantity</span></span>  

<span data-ttu-id="c9132-160">Du kan finde flere oplysninger i [Designoplysninger: planlægningsparametre](design-details-planning-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="c9132-160">For more information, see [Design Details: Planning Parameters](design-details-planning-parameters.md)</span></span>  

## <a name="other-important-planning-fields"></a><span data-ttu-id="c9132-161">Andre vigtige felter til planlægning</span><span class="sxs-lookup"><span data-stu-id="c9132-161">Other Important Planning Fields</span></span>
### <a name="planning-flexibility"></a><span data-ttu-id="c9132-162">Planlægningsfleksibilitet</span><span class="sxs-lookup"><span data-stu-id="c9132-162">Planning Flexibility</span></span>
<span data-ttu-id="c9132-163">I de fleste forsyningsordrer, f.eks. produktionsordrer, kan du vælge **Ubegrænset** eller **Ingen** i feltet **Planlægningsfleksibilitet** på linjerne.</span><span class="sxs-lookup"><span data-stu-id="c9132-163">On most supply orders, such as production orders, you can select **Unlimited** or **None** in the **Planning Flexibility** field on the lines.</span></span>

<span data-ttu-id="c9132-164">Det angiver, om der tages højde for forsyningen repræsenteret af produktionsordrelinjen i planlægningssystemet, når der beregnes aktionsmeddelelser.</span><span class="sxs-lookup"><span data-stu-id="c9132-164">This specifies whether the supply represented by the production order line is considered by the planning system when calculating action messages.</span></span>
<span data-ttu-id="c9132-165">Hvis feltet viser indstillingen **Ubegrænset**, medtager planlægningssystemet linjen, når aktionsmeddelelsen beregnes.</span><span class="sxs-lookup"><span data-stu-id="c9132-165">If the field contains **Unlimited**, then the planning system includes the line when calculating action messages.</span></span> <span data-ttu-id="c9132-166">Hvis feltet indeholder indstillingen **Ingen**, er linjen fast og kan ikke ændres, og linjen medtages ikke i beregningen af aktionsmeddelelser.</span><span class="sxs-lookup"><span data-stu-id="c9132-166">If the field contains **None**, then the line is firm and unchangeable, and the planning system does not include the line when calculating action messages.</span></span>

### <a name="warning"></a><span data-ttu-id="c9132-167">Advarsel</span><span class="sxs-lookup"><span data-stu-id="c9132-167">Warning</span></span>
<span data-ttu-id="c9132-168">Oplysningsfeltet **Advarsel** i vinduet **Planlægningskladde** viser eventuelle planlægningslinjer, der er oprettet til en usædvanlig situation med en tekst, som brugeren kan vælge for at få yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="c9132-168">The **Warning** information field in the **Planning Worksheet** window informs you of any planning line created for an unusual situation with a text, which the user can choose to read additional information.</span></span> <span data-ttu-id="c9132-169">Der findes følgende advarselstyper:</span><span class="sxs-lookup"><span data-stu-id="c9132-169">The following warning types exist:</span></span>

- <span data-ttu-id="c9132-170">Nødsituation</span><span class="sxs-lookup"><span data-stu-id="c9132-170">Emergency</span></span>
- <span data-ttu-id="c9132-171">Undtagelse</span><span class="sxs-lookup"><span data-stu-id="c9132-171">Exception</span></span>
- <span data-ttu-id="c9132-172">Bemærk!</span><span class="sxs-lookup"><span data-stu-id="c9132-172">Attention</span></span>
- <span data-ttu-id="c9132-173">Nødsituation</span><span class="sxs-lookup"><span data-stu-id="c9132-173">Emergency</span></span>

<span data-ttu-id="c9132-174">Denne advarsel vises i to tilfælde:</span><span class="sxs-lookup"><span data-stu-id="c9132-174">The emergency warning is displayed in two situations:</span></span>

- <span data-ttu-id="c9132-175">Når lageret er negativt på den planlagte startdato.</span><span class="sxs-lookup"><span data-stu-id="c9132-175">The inventory is negative on the planning starting date.</span></span>
- <span data-ttu-id="c9132-176">Når der er antedaterede udbuds- eller efterspørgselshændelser.</span><span class="sxs-lookup"><span data-stu-id="c9132-176">Back-dated supply or demand events exist.</span></span>

<span data-ttu-id="c9132-177">Hvis varens lager er negativt på den planlagte startdato, foreslås der en nødforsyningsordre for den negative mængde, som skal ankomme på den planlagte startdato.</span><span class="sxs-lookup"><span data-stu-id="c9132-177">If an item’s inventory is negative on the planning starting date, the planning system suggests an emergency supply order for the negative quantity to arrive on the planning starting date.</span></span> <span data-ttu-id="c9132-178">Advarslen angiver startdatoen og mængden for nødordren.</span><span class="sxs-lookup"><span data-stu-id="c9132-178">The warning text states the starting date and the quantity of the emergency order.</span></span>

<span data-ttu-id="c9132-179">Evt. dokumentlinjer med forfaldsdatoer før den planlagte startdato konsolideres i én nødforsyningsordre, så varen kan ankomme på den planlagte startdato.</span><span class="sxs-lookup"><span data-stu-id="c9132-179">Any document lines with due dates before the planning starting date are consolidated into one emergency supply order for the item to arrive on the planning starting date.</span></span>

### <a name="exception"></a><span data-ttu-id="c9132-180">Undtagelse</span><span class="sxs-lookup"><span data-stu-id="c9132-180">Exception</span></span>
<span data-ttu-id="c9132-181">Advarslen om undtagelsen vises, hvis det forventede disponible lager kommer under sikkerhedslageret.</span><span class="sxs-lookup"><span data-stu-id="c9132-181">The exception warning is displayed if the projected available inventory drops below the safety stock quantity.</span></span>

<span data-ttu-id="c9132-182">Planlægningssystemet foreslår en forsyningsordre, der skal opfylde behovet på forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="c9132-182">The planning system will suggest a supply order to meet the demand on its due date.</span></span> <span data-ttu-id="c9132-183">Advarslen angiver varens sikkerhedslager og den dato, hvor det overtrædes.</span><span class="sxs-lookup"><span data-stu-id="c9132-183">The warning text states the item’s safety stock quantity and the date on which it is violated.</span></span>

<span data-ttu-id="c9132-184">Overskridelse af niveauet for sikkerhedslageret anses for at være en undtagelse, fordi det ikke bør forekomme, hvis genbestillingspunktet er angivet korrekt.</span><span class="sxs-lookup"><span data-stu-id="c9132-184">Violating the safety stock level is considered an exception because it should not occur if the reorder point has been set correctly.</span></span>

> [!NOTE]
> <span data-ttu-id="c9132-185">Efterspørgsel på planlægningslinjer med undtagelsesadvarsler modificeres normalt ikke i henhold til planlægningsparametre.</span><span class="sxs-lookup"><span data-stu-id="c9132-185">Supply on planning lines with Exception warnings is normally not modified according to planning parameters.</span></span> <span data-ttu-id="c9132-186">Planlægningssystemet foreslår i stedet for kun en forsyning til at dække det nøjagtige behovsantal.</span><span class="sxs-lookup"><span data-stu-id="c9132-186">Instead, the planning system only suggests a supply to cover the exact demand quantity.</span></span> <span data-ttu-id="c9132-187">Du kan dog konfigurere planlægningskørslen til at overholde bestemte planlægningsparametre for planlægningslinjer med visse advarsler.</span><span class="sxs-lookup"><span data-stu-id="c9132-187">However, you can set the planning run up to respect certain planning parameters for planning lines with certain warnings.</span></span> <span data-ttu-id="c9132-188">Du kan se flere oplysninger i "Respekter planlægningsparametre for undtagelsesadvarsler" i Beregn plan - planlægnings.</span><span class="sxs-lookup"><span data-stu-id="c9132-188">For more information, see “Respect Planning Parameters for Exception Warnings” in Calculate Plan - Plan.</span></span> <span data-ttu-id="c9132-189">kld.</span><span class="sxs-lookup"><span data-stu-id="c9132-189">Wksh.</span></span>

### <a name="attention"></a><span data-ttu-id="c9132-190">Bemærk!</span><span class="sxs-lookup"><span data-stu-id="c9132-190">Attention</span></span>
<span data-ttu-id="c9132-191">Denne advarsel vises i to tilfælde:</span><span class="sxs-lookup"><span data-stu-id="c9132-191">The attention warning is displayed in two situations:</span></span>

- <span data-ttu-id="c9132-192">Når den planlagte startdato ligger før arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="c9132-192">The planning starting date is earlier than the work date.</span></span>
- <span data-ttu-id="c9132-193">Når planlægningslinjen foreslår at ændre en frigivet købs- eller produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="c9132-193">The planning line suggests to change a released purchase or production order.</span></span>

> [!NOTE]
> <span data-ttu-id="c9132-194">På planlægningslinjer med advarsler er feltet **Accepter aktionsmeddelelse** ikke markeret, fordi planlæggeren forventes at undersøge disse linjer nærmere, før planen udføres.</span><span class="sxs-lookup"><span data-stu-id="c9132-194">In planning lines with warnings, the **Accept Action Message** field is not selected, because the planner is expected to further investigate these lines before carrying out the plan.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9132-195">Se også</span><span class="sxs-lookup"><span data-stu-id="c9132-195">See Also</span></span>  
[<span data-ttu-id="c9132-196">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="c9132-196">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)  
<span data-ttu-id="c9132-197">[Planlægning](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="c9132-197">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="c9132-198">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="c9132-198">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="c9132-199">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="c9132-199">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="c9132-200">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c9132-200">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c9132-201">Køb</span><span class="sxs-lookup"><span data-stu-id="c9132-201">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="c9132-202">Konfigurere bedste fremgangsmåder: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="c9132-202">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="c9132-203">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c9132-203">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

