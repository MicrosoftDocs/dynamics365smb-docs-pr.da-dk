---
title: "Designoplysninger – Fast genbestil.antal | Microsoft Docs"
description: "Fast genbestil.antal er relateret til lageret, planlægning af typiske C-varer (lav lageromkostning, lav risiko for forældelse og/eller mange varer). Denne metode bruges normalt i forbindelse med et genbestillingspunkt, hvilket afspejler det forventede behov under leveringstiden for varen."
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
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5084c8a49972ea51600867d90acedc2698609732
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-fixed-reorder-qty"></a>Designoplysninger: Fast genbestil.antal
Fast genbestil.antal er relateret til lageret, planlægning af typiske C-varer (lav lageromkostning, lav risiko for forældelse og/eller mange varer). Denne metode bruges normalt i forbindelse med et genbestillingspunkt, hvilket afspejler det forventede behov under leveringstiden for varen.  

## <a name="calculated-per-time-bucket"></a>Beregnet pr. interval  
 Hvis planlægningssystemet har registreret, at genbestillingspunktet er nået eller overskredet i et bestemt interval (genbestillingscyklus) – over eller ved genbestillingspunktet i begyndelsen af perioden og under eller ved genbestillingspunktet sidst i perioden – vil den foreslå at oprette en ny forsyningsordre af det angivne genbestillingsantal og planlægge det fremad fra den første dag efter slutningen af intervallet.  

 Det tidsbegrænsede genbestillingspunkt reducerer antallet af forsyningsforslag. Dette afspejler den manuelle proces, der består i ofte at gå gennem lageret for at kontrollere det faktiske indhold på de forskellige placeringer.  

## <a name="creates-only-necessary-supply"></a>Opretter kun nødvendige forsyninger  
 Før der foreslås, at en ny forsyningsordre opfylder et genbestillingspunkt, kontrollerer planlægningssystemet, om forsyning allerede er bestilt til modtagelse inden for varens leveringstid. Hvis en eksisterende forsyningsordre kan løse problemet ved at bringe den projekterede lagerbeholdning til eller over genbestillingspunktet inden for leveringstiden, vil systemet ikke foreslå en ny forsyningsordre.  

 Forsyningsordrer, der er oprettet specielt med henblik på at opfylde genbestillingspunktet, er udelukket fra almindelig forsyningsafstemning og vil ikke på nogen måde blive ændret bagefter. Hvis en vare, der bruger genbestillingspunktet skal udfases (ikke genbestilt), er det derfor hensigtsmæssigt at gennemgå udestående forsyningsordrer manuelt eller ændre genbestillingsmetoden til lot-for-lot, hvorved systemet vil reducere eller annullere overflødige forsyninger.  

## <a name="combines-with-order-modifiers"></a>Kombineres med ordremodifikatorer  
 Ordremodifikatorerne Min. ordrestørrelse, Maks. ordrestørrelse og Oprundingsfaktor bør ikke spille en stor rolle, når metoden for fast genbestillingsantal bruges. Dog tager planlægningssystemet stadig højde for disse modifikatorer og vil reducere antallet til det angivne maksimale ordreantal (og oprette to eller flere forsyninger for at nå det samlede ordreantal), øge ordren til den angivne minimummængde eller runde ordreantallet op for at opfylde en bestemt oprundingsfaktor.  

## <a name="combines-with-calendars"></a>Kombinerer med kalendere  
 Før der bliver foreslået en ny forsyningsordre for at opfylde et genbestillingspunkt, kontrollerer planlægningssystemet, om ordren er planlagt til en ikkearbejdsdag i overensstemmelse med de kalendere, der er defineret i feltet **Basiskalenderkode** i vinduerne **Virksomhedsoplysninger** og **Lokationskort**.  

 Hvis den planlagte dato er en ikkearbejdsdag, flytter planlægningssystemet ordren frem til den nærmeste arbejdsdag. Det kan resultere i en ordre, der opfylder et genbestillingspunkt, men ikke opfylder visse specifikke behov. Planlægningssystemet opretter en ekstra levering for sådanne behov.  

## <a name="should-not-be-used-with-forecast"></a>Bør ikke bruges med forecast  
 Det er ikke nødvendigt at medtage en prognose i planlægningen af en vare ved hjælp af et genbestillingspunktet, fordi det forventede behov allerede er angivet i genbestillingspunktet. Hvis det er relevant at basere planen på et forecast, kan du bruge politikken lot-for-lot.  

## <a name="must-not-be-used-with-reservations"></a>Må ikke anvendes med reservationer  
 Hvis brugeren har reserveret en mængde, for eksempel et antal på lageret, til nogle fremtidige behov, bliver grundlaget for planlægningen forstyrret. Selvom det planlagte beholdningsniveau er acceptabelt i relation til genbestillingspunktet, er mængderne muligvis ikke tilgængelige. Systemet kan forsøge at kompensere for dette ved at oprette undtagelsesordrer. Det anbefales dog, at feltet Reserver angives til Aldrig på varer, der er planlagt ved hjælp af et genbestillingspunkt.  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md)   
 [Designoplysninger: Maks. antal](design-details-maximum-qty.md)   
 [Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
 [Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
 [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)

