---
title: "Forsyningsplanlægning | Microsoft Docs"
description: Opret en detaljeret, eksekverbar plan og produktionsplanen med endelig montage til salgs- og produktionsbehov.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 85b5583d18042b05aea264d59ed9484dddeb4d12
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="planning"></a>Planlægning
De produktionsoperationer, der kræves for at omdanne tilgange til færdigvarer, skal planlægges dagligt eller ugentligt afhængigt af produkternes omfang og egenskaber. [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder funktioner til levering af forventet og faktisk behov fra salg, montage og produktion samt funktioner til distributionsplanlægning ved hjælp af lagervarer og overflytning af lokationer.

> [!NOTE]
> I dette emne beskrives primært planlægning for virksomheder, der er involveret i produktion eller montagestyring, hvor de resulterende forsyningsordrer kan være enten produktion, montage, overflytning eller købsordrer. Den primære brugergrænseflade for dette planlægningsarbejde er vinduet **Planlægningskladde**.

> [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter også forsyningsplanlægning for engrosvirksomheder, hvor de oprettede forsyningsordrer kun være overførsels- og købsordrer. Den primære brugergrænseflade for dette planlægningsarbejde er vinduet **Indkøbskladde**, som beskrives indirekte i dette emne, da de fleste planlægningsfunktioner gælder for begge kladder.

Før du planlægger og udfører produktionsordrer, skal du konfigurere produktionskapaciteter, f.eks. oprette produktionskalendere, ruter, produktionsstyklister og produktionsprocesser. Du kan finde flere oplysninger i [Konfigurere produktion](production-configure-production-processes.md).

Planlægning kan betragtes som forberedelsen af forsyningsordrer i montage- eller produktionsafdelinger til at imødekomme behov. Du kan finde flere oplysninger i [Montagestyring](assembly-assemble-items.md) og [Produktion](production-manage-manufacturing.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Få er kort introduktion til, hvordan planlægningssystemet kan bruges til at registrere og prioritere behov og foreslå en afstemt forsyningsplan.|[Om planlægningsfunktionen](production-about-planning-functionality.md)|
|Forstå, hvordan alle aspekter af planlægningssystemet fungerer, og hvordan du justerer algoritmer for at opfylde planlægningsbehov i forskellige miljøer.|[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)|
|Vide, hvordan planlægningslogikken differentierer mellem behov på lokationer i henhold til lagervareopsætningen og behov uden lokationskoder.|[Planlægge med eller uden lokationer](production-planning-with-without-locations.md)|
|Lave et forecast over produktionsbehov afledt af de forventede salgs- og produktionsordrer.|[Oprette et produktionsforecast](production-how-to-create-a-forecast.md)|  
|Oprette en-til-en-produktionsordrer automatisk fra en salgsordre for at dække det nøjagtige behov for denne salgsordreline.|[Oprette produktionsordrer fra salgsordrer](production-how-to-create-production-orders-from-sales-orders.md)|
|Oprette en projektproduktionsordre direkte fra en salgsordre med flere linjer, som udgør et produktionsprojekt.|[Planlægge projektordrer](production-how-to-plan-project-orders.md)|
|Bruge vinduet **Ordreplanlægning** til manuel planlægning af salgs- eller produktionsbehov for et styklisteniveau ad gangen.|[Planlægge efter nyt behov ordre for ordre](production-how-to-plan-for-new-demand.md)|
|Brug vinduet **Planlægningskladde** til at køre både MPS- og MRP-funktionerne for automatisk at oprette enten en overordnet eller en detaljeret forsyningsplan på alle vareniveauer.|[Køre fuld planlægning, MPS eller MRP](production-how-to-run-mps-and-mrp.md)|
|Køre indkøbskladden for automatisk at oprette en detaljeret forsyningsplan for at dække behovet for varer, der kun kan opfyldes med et et køb eller ene overførsel.|Siden **Indkøbskladde**|  
|Starte eller opdatere en produktionsordre som grovplanlagte operationer i masterproduktionsskemaet.|[Omplanlægge eller forny produktionsordrer direkte](production-how-to-replan-refresh-production-orders.md)|
|Genberegne arbejdscenter- eller produktionsressourcekalendere på grund af planlægningsændringer.|Afsnittet "Sådan beregnes en arbejdscenterkalender" i [Opsætte produktionskalendere](production-how-to-create-work-center-calendars.md)|
|Spore ordrebehov (sporet antal), forecast, rammesalgsordre eller planlægningsparameter (ikkesporet antal), der er årsag til den pågældende planlægningslinje.|[Spore relationer mellem behov og forsyning](production-how-track-demand-supply.md)|
|Få vist en vares planlagte disponible lager ved forskellige visninger og se, hvilke bruttobehov, planlagte ordretilgange og andre hændelser, der påvirker over tid.|[Vise varedisponering](inventory-how-availability-overview.md)|  
|Udfør udvalgte planlægningsaktiviteter, f.eks. ændring eller tilføjelse af planlægningskladdelinjer, i en grafisk oversigt over forsyningsplanen.|[Ændre planlægningsforslag i en grafisk visning](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## <a name="see-also"></a>Se også
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

