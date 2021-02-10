---
title: Planlægning med eller uden lokationer | Microsoft Docs
description: Det er vigtigt at forstå planlægning med eller uden lokationskoder på behovslinjer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 49448cc56d76846c70471a53a257986b543f11b3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758813"
---
# <a name="planning-with-or-without-locations"></a>Planlægge med eller uden lokationer
Med hensyn til planlægning med eller uden lokationskoder på behovslinjer fungerer planlægningssystemet på samme ukomplicerede måde, når:  

-   behovslinjer altid har lokationskoder, og systemet bruger lagervarer i fuld udstrækning, herunder den relevante lokationsopsætning.  
-   behovslinjer aldrig har lokationskoder, og systemet ikke bruger lagervarer eller nogen form for lokationsopsætning (se sidste eksempel nedenfor).  

Hvis behovslinjerne derimod sommetider har lokationskoder og sommetider ikke, vil planlægningssystemet følge visse regler afhængigt af opsætningen.  

## <a name="demand-at-location"></a>Behov på lokation  
Når planlægningssystemet registrerer behov på en lokation (en linje med en lokationskode), fungerer det forskelligt afhængigt af 3 vigtige opsætningsværdier.  

Under et planlægningsforløb kontrollerer systemet de 3 opsætningsværdier en efter en og planlægger i overensstemmelse med dem:  

1.  Er feltet **Tvungen lokationskode** markeret?  

    Hvis ja, så:  

2.  Er varen registreret som lagervare?  

    Hvis ja, så:  

    Varen planlægges i overensstemmelse med planlægningsparametrene på lagerkortet.  

    Hvis nej, så:  

3.  Indeholder feltet **Komponenter på lokation** den efterspurgte lokationskode?  

    Hvis ja, så:  

    Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.  

    Hvis nej, så:  

    Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot*, Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme. (Varer, der benytter genbestillingsmetoden  *Ordre*, fortsætter med at bruge  *Ordre* såvel som de andre indstillinger.)  

> [!NOTE]  
>  Dette minimale alternativ dækker kun det nøjagtige behov. Eventuelle definerede planlægningsparametre ignoreres.  

Se forskellene i eksemplerne nedenfor.  

## <a name="demand-at-blank-location"></a>Behov på "tom lokation"  
Selv hvis afkrydsningsfeltet **Tvungen lokationskode** er markeret, tillader systemet, at behovslinjer oprettes uden lokationskode – hedder også *TOM* lokation. Dette er en afvigelse for systemet, da det har forskellige opsætningsværdier, der er indstillet til at håndtere lokationer (se ovenfor), og som et resultat opretter planlægningsprogrammet ikke en planlægningslinje for en behovslinje. Hvis feltet **Tvungen lokationskode** ikke er markeret, men alle lokationsopsætningsværdierne findes, skal dette også betragtes en afvigelse, og planlægningssystemet reagerer ved at udføre det "minimale alternativ":   
Varen planlægges i overensstemmelse med Genbestillingsmetode =  *Lot-for-Lot* ( *Ordre* forbliver *Ordre)*, Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.  

Se forskellene i opsætningseksemplerne nedenfor.  

### <a name="setup-1"></a>Opsætning 1:  

-   Tvungen lokationskode = *Ja*  
-   Lagervare er konfigureret for  *RØD*  
-   Komponenter på lokation =  *BLÅ*  

#### <a name="case-11-demand-is-at--red-location"></a>Situation 1.1: Behovet findes på lokationen *RØD*  

Varen planlægges i overensstemmelse med planlægningsparametrene på lagerkortet (herunder mulig overflytning).  

#### <a name="case-12-demand-is-at--blue-location"></a>Situation 1.2: Behovet findes på lokationen *BLÅ*  

Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.  

#### <a name="case-13-demand-is-at--green-location"></a>Situation 1.3: Behovet findes på lokationen  *GRØN*  

Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot* ( *Ordre* forbliver  *Ordre*), Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.  

#### <a name="case-14-demand-is-at--blank-location"></a>Situation 1.4: Behovet findes på lokationen *TOM*  

Varen planlægges ikke, fordi der ikke er defineret en lokation på behovslinjen.  

### <a name="setup-2"></a>Opsætning 2:  

-   Tvungen lokationskode = *Ja*  
-   Ingen lagervare defineret  
-   Komponenter på lokation =  *BLÅ*  

#### <a name="case-21-demand-is-at--red-location"></a>Situation 2.1: Behovet findes på lokationen  *RØD*  

Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot* ( *Ordre* forbliver  *Ordre*), Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.  

#### <a name="case-22-demand-is-at--blue-location"></a>Situation 2.2: Behovet findes på lokationen *BLÅ*  

Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.  

### <a name="setup-3"></a>Opsætning 3:  

-   Tvungen lokationskode = *Nej*  
-   Ingen lagervare defineret  
-   Komponenter på lokation =  *BLÅ*  

#### <a name="case-31-demand-is-at--red-location"></a>Situation 3.1: Behovet findes på lokationen  *RØD*  

Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot* ( *Ordre* forbliver  *Ordre*), Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.  

#### <a name="case-32-demand-is-at--blue-location"></a>Situation 3.2: Behovet findes på lokationen *BLÅ*  

Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.  

#### <a name="case-33-demand-is-at--blank-location"></a>Situation 3.3: Behovet findes på lokationen  *TOM*  

Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot* ( *Ordre* forbliver  *Ordre*), Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.  

### <a name="setup-4"></a>Opsætning 4:  

-   Tvungen lokationskode = *Nej*  
-   Ingen lagervare defineret  
-   Komponenter på lokation =  *TOM*  

#### <a name="case-41-demand-is-at--blue-location"></a>Situation 4.1: Behovet findes på lokationen  *BLÅ*  

Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot* ( *Ordre* forbliver  *Ordre*), Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.  

#### <a name="case-42-demand-is-at--blank-location"></a>Situation 4.2: Behovet findes på lokationen  *TOM*  

Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.  

Som det fremgår af det sidste eksempel, kan man kun få det rigtige resultat for en behovslinje uden en lokationskode ved at deaktivere alle opsætningsværdier, der er knyttet til lokationer. Ligeledes kan man kun få stabile planlægningsresultater for behov på lokationer ved at bruge lagervarer.  

Hvis du ofte planlægger med behov på lokationer, anbefales det derfor kraftigt at benytte lagervarefunktionen.  

## <a name="see-also"></a>Se også
[Planlægning](production-planning.md)    
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
