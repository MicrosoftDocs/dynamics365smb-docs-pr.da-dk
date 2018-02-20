---
title: "Designoplysninger – Indlæsning af lagerprofiler | Microsoft Docs"
description: "Planlægningssystemet organiserer de mange kilder for behov og forsyning på to tidslinjer, der kaldes lagerprofiler, for at få dem sorteret."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: d2a2ee196be4562f62604afd4faed608ff07411f
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-loading-the-inventory-profiles"></a>Designoplysninger: Indlæsning af lagerprofiler
Planlægningssystemet organiserer de mange kilder for behov og forsyning på to tidslinjer, der kaldes lagerprofiler, for at få dem sorteret.  

 Normale typer af behov og forsyning med forfaldsdatoer på eller efter den planlagte startdato indlæses i hver lagerprofil. Når de er indlæst, sorteres de forskellige behovs- og forsyningstyper i henhold til overordnede prioriteter, f.eks. forfaldsdato, laveste-niveau-koder, lokation og variant. Desuden anvendes ordreprioriteter på de forskellige typer for at sikre, at de vigtigste behov opfyldes først. Du kan finde flere oplysninger i [Designoplysninger: Prioritering af ordrer](design-details-prioritizing-orders.md).  

 Som tidligere nævnt kan behov også være negativt. Det betyder, at det bør behandles som forsyning. I modsætning til de normale typer forsyning anses negative behov dog som fast forsyning. Planlægningssystemet kan tage det i betragtning, men ikke vil foreslå ændringer.  

 Generelt tager planlægningssystemet højde for alle forsyningsordrer efter den planlagte startdato i forbindelse med ændringer for at opfylde behovet. Så snart et antal er bogført fra en forsyningsordre, kan det dog ikke længere ændres af planlægningssystemet. Derfor kan følgende forskellige ordrer ikke planlægges om:  

-   Frigivne produktionsordrer, hvor der er bogført forbrug eller afgang.  

-   Montageordrer, hvor der er bogført forbrug eller afgang.  

-   Overflytningsordrer, hvor leverancen er blevet bogført.  

-   Indkøbsordrer, hvor modtagelsen er blevet bogført.  

 Bortset fra indlæsning af behovs- og forsyningstyper, indlæses visse typer med opmærksomhed på særlige regler og afhængigheder, der er beskrevet i det følgende.  

## <a name="item-dimensions-are-separated"></a>Varedimensioner er adskilt  
 Forsyningsplanen skal beregnes pr. kombination af varedimensioner, f.eks. variant og lokation. Der er ingen grund til at beregne nogen teoretisk kombination. Kun de kombinationer, der bærer behov og/eller forsyning, skal beregnes.  

 Planlægningssystemet kontrollerer dette ved at køre gennem lagerprofilen. Når der findes en ny kombination, opretter programmet en automatisk kontrolpost, der indeholder den faktiske kombinationsoplysninger. Programmet indsætter lagervaren som kontrolpost eller ydre løkke. Derfor angives de korrekte planlægningsparametre i overensstemmelse med en kombination af variant og placering, og programmet kan gå videre til den indre løkke.  

> [!NOTE]  
>  Programmet kræver ikke, at brugeren angiver en lagervarepost ved angivelse af behov og/eller forsyning for en bestemt kombination af variant og lokation. Hvis der ikke findes en lagervare for en given kombination, opretter programmet derfor sin egen midlertidige lagervare baseret på varekortdata. Hvis Tvungen lokationskode er angivet til Ja i vinduet Lageropsætning, skal der oprettes en Lagervare, eller komponenter på lokation skal angives til Ja. Du kan finde flere oplysninger i [Designoplysninger: Behov på lokationen TOM](design-details-demand-at-blank-location.md).  

## <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Serienumre/lotnumre indlæses efter specifikationsniveau  
 Attributter i form af serie-/lotnumre indlæses i lagerprofilerne sammen med det behov og den forsyning, de er tildelt.  

 Behov- og forsyningsattributter arrangeres efter ordreprioritet og efter deres specifikationsniveau. Da afstemte serienumre/lotnumre afspejler specifikationsniveauet, vil de mere specifikke behov, som f.eks. et lotnummer, der er valgt specifikt til en salgslinje, søge efter en overensstemmelse, før mindre specifikke behov, f.eks. et salg fra et valgt lotnummer.  

> [!NOTE]  
>  Der er ingen dedikerede prioriteringsregler for serie-/lotnummereret behov og forsyning udover niveauet af specifikation, der er defineret af deres kombinationer af serie- og lotnumre og varesporingsopsætningen for de involverede varer.  

 Under justering anser planlægningssystemet forsyning, der har serienumre/lotnumre, for ufleksible og forsøger ikke at forøge eller omplanlægge sådanne forsyningsordre (medmindre de bruges i en ordre-til-ordre-relation). Se Ordre-til-ordre-links er aldrig brudt). Dette sikrer, at forsyningen ikke modtager flere, eventuelt modstridende aktionsmeddelelser, når en forsyning har forskellige attributter, f.eks. en samling af forskellige serienumre.  

 En anden grund til, at serie-/lotnummereret forsyning er ufleksibel er, at serie-/lotnumre generelt tildeles så sent i processen, at det ville være forvirrende, hvis der foreslås ændringer.  

 Afstemning af serienumre/lotnumre overholder ikke den [frosne Zone](design-details-dealing-with-orders-before-the-planning-starting-date.md). Hvis behov og forsyning ikke er synkroniseret, kan planlægningssystemet foreslå ændringer eller foreslå nye ordrer, uanset den planlagte startdato.  

## <a name="order-to-order-links-are-never-broken"></a>Ordre-til-ordre-links er aldrig brudt  
 Ved planlægning af en ordre-til-ordre-vare må den tilknyttede forsyning ikke bruges til andre behov end det, den oprindeligt var tiltænkt. Sammenkædede behov bør ikke være dækket af andre tilfældige forsyninger, selv om den aktuelt er tilgængelig i tid og antal. En montageordre, der er knyttet til en salgsordre i et montage-til-ordre-scenarie, kan f.eks. ikke bruges til at dække andre behov.  

 Ordre-til-ordre efterspørgsel og udbud skal afstemmes nøjagtigt. Planlægningssystemet sikrer forsyningen under alle omstændigheder uden hensyntagen til ordrestørrelsesparametre, modifikatorer og antal på lager (bortset fra antal, der er relateret til linkede ordrer). Af samme grund foreslår systemet at reducere overskydende forsyninger, hvis det tilknyttede behov reduceres.  

 Denne udligning påvirker også timingen. Den begrænsede horisont, der er givet af intervallet, tages ikke i betragtning. Forsyning flyttes, hvis timingen af behovet er blevet ændret. Aktionsgrænsen for tid vil dog blive overholdt og vil forhindre, at ordre-til-ordre-forsyninger planlægges, bortset fra de interne forsyninger af en produktionsordre med flere niveauer (projektordre).  

> [!NOTE]  
>  Serienumre/lotnumre kan også angives på ordre-til-ordre efter behov. I så fald betragtes forsyning ikke som fleksibel som standard, hvilket normalt er tilfældet for serienumre/lotnumre. I så fald vil systemet øge/reducere efter ændringer i behovet. Hvis ét behov desuden har forskellige serie-/lotnumre, som f.eks. mere end ét lotnummer, vil der blive foreslået en forsyningsordre pr. lot.  

> [!NOTE]  
>  Forecasts bør ikke føre til at oprettelse af forsyningsordrer, der er bundet af et ordre-til-ordre-link. Hvis forecast bruges, skal det kun bruges som en generator af afhængigt behov i et produktionsmiljø.  

## <a name="component-need-is-loaded-according-to-production-order-changes"></a>Komponentbehov er indlæst i overensstemmelse med ændringer af produktionsordrer  
 Ved håndtering af produktionsordrer skal planlægningssystemet overvåge de nødvendige komponenter, før de indlæses i behovsprofilen. Komponentlinjer, der skyldes en ændret produktionsordre, erstatter dem fra den oprindelige ordre. Dette sikrer, at planlægningssystemet definerer, at planlægningslinjer for komponentbehov aldrig kopieres.  

##  <a name="BKMK_SafetyStockMayBeConsumed"></a> Sikkerhedslager kan forbruges  
 Sikkerhedslageret er primært en behovstype og indlæses derfor i lagerprofilen på planlægningens startdato.  

 Sikkerhedslager er et lagerantal, der er lagt til side for at kompensere for usikkerheden i behov under leveringstiden for genopfyldning. Det kan dog forbruges, hvis det er nødvendigt at tage fra det for at opfylde et behov. I dette tilfælde, vil planlægningssystemet sikre, at sikkerhedslageret hurtigt fyldes igen ved at foreslå en forsyningsordre den dag, hvor sikkerhedslageret opbruges. Denne planlægningslinje vil vise ikonet Undtagelsesadvarsel, som forklarer planlæggeren, at sikkerhedslageret er blevet helt eller delvist opbrugt ved brug af en undtagelsesordre for det manglende antal.  

## <a name="forecast-demand-is-reduced-by-sales-orders"></a>Forecastbehov reduceres af salgsordrer  
 Produktionsprognosen udtrykker det forventede fremtidige behov. Mens faktisk behov angives, normalt som salgsordrer for producerede varer, bruger den prognosen.  

 Selve forecastet er ikke reelt reduceret af salgsordrer; det forbliver det samme. Dog reduceres forecastantal i beregningen af planlægning (med salgsordremængder) før det eventuelle resterende antal i behovet for lagerprofilen. Når planlægningssystemet undersøger faktiske salgstal i en periode, medtages både åbne salgsordrer og vareposter fra leverede salg, medmindre de stammer fra en rammeordre.  

 En bruger skal angive en gyldig prognoseperiode. Datoen på det planlagte antal angiver starten af perioden, og datoen på det næste forecast angiver slutningen af perioden.  

 Forecast for perioder før planlægningsperioden bruges ikke, uanset om det er forbrugt eller ej. Det første budgetterede tal af interesse er enten datoen eller den nærmeste dato før planlægningens startdato.  

 Forecast kan være for uafhængige behov som salgsordrer eller afhængige behov som produktionsordrekomponenter (modul-forecast). En vare kan have begge typer forecast. Under planlægningen sker forbruget separat, først for uafhængige behov og derefter for afhængige behov.  

## <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Rammeordrebehov reduceres af salgsordrer  
 Forecastfunktionaliteten suppleres af rammesalgsordren som en måde til at angive fremtidige behov fra en bestemt kunde. Som med (uspecificerede) prognoser bør faktiske salg forbruge det forventede behov, og det resterende antal bør indgå i behovslagerprofilen. Igen, forbruget reducerer ikke rammeordren.  

 Planlægningsberegningen finder åbne salgsordrer, der er knyttet til den bestemte rammeordrelinje, men den tager ikke hensyn til en gyldig periode. Der tages heller ikke højde for bogførte ordrer, da bogføringsproceduren allerede har reduceret udestående rammeordreantal.  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)   
 [Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)   
 [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
 [Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)

