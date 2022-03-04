---
title: Planlægge med eller uden lokationer
description: I dette emne kan du finde oplysninger om produktion og bearbejdning, herunder forsyningsplanlægning, i Business central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/16/2021
ms.author: edupont
ms.openlocfilehash: 27f9b5002d96d55121272f992f58c9cf9748111f
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8137467"
---
# <a name="planning-with-or-without-locations"></a>Planlægge med eller uden lokationer
Med hensyn til planlægning med eller uden lokationskoder på behovslinjer fungerer planlægningssystemet på samme ukomplicerede måde, når:  

-   behovslinjer altid har lokationskoder, og systemet bruger lagervarer i fuld udstrækning, herunder den relevante lokationsopsætning.  
-   behovslinjer aldrig har lokationskoder, og systemet ikke bruger lagervarer eller nogen form for lokationsopsætning (se sidste eksempel nedenfor).  

Hvis behovslinjerne derimod sommetider har lokationskoder og sommetider ikke, vil planlægningssystemet følge visse regler afhængigt af opsætningen.  

> [!TIP]
> Hvis du tit har brug for at planlægge behov på forskellige lokationer, anbefales det at bruge funktionen Lagervarer.

## <a name="demand-at-location"></a>Behov på lokation  

Når planlægningssystemet registrerer behov på en lokation (en linje med en lokationskode), fungerer det forskelligt afhængigt af 3 vigtige opsætningsværdier.  

Under et planlægningsforløb kontrollerer systemet de 3 opsætningsværdier en efter en og planlægger i overensstemmelse med dem:  

1. Er afkrydsningsfeltet **Tvungen lokationskode** på siden **Lageropsætning** markeret?  

    Hvis ja, så:  

2. Er varen registreret som lagervare?  

    Hvis ja, så:  

    Varen planlægges i overensstemmelse med planlægningsparametrene på lagerkortet.  

    Hvis nej, så:  

3. Indeholder feltet **Komponenter på lokation** på siden **Produktionsopsætning** den krævede lokationskode?  

    Hvis ja, så:  

    Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.  

    Hvis nej, så:  

    Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot*, Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme. (Varer, der benytter genbestillingsmetoden  *Ordre*, fortsætter med at bruge  *Ordre* såvel som de andre indstillinger.)  

> [!NOTE]  
> Dette minimale alternativ dækker kun det nøjagtige behov. Eventuelle definerede planlægningsparametre ignoreres.  

Se forskellene i eksemplerne nedenfor.  

> [!TIP]
> Feltet **Tvungen lokationskode** på siden **Lageropsætning** og feltet **Komponenter på lokation** på siden Produktionsopsætning er meget vigtige for, styringen af, hvordan planlægningssystemets håndterer behovslinjer med/uden lokationskoder.
>
> I forbindelse med produktionsbehov, der er købt (når planlægningsmotoren bruges udelukkende til købsplanlægning og ikke til produktionsplanlægning), bruger [!INCLUDE [prod_short](includes/prod_short.md)] den samme lokation for komponenter som den, der er angivet på produktionsordren. Hvis du udfylder dette felt, kan du dog omdirigere komponenterne til en anden lokation.
>
> Du kan også definere dette for en specifik lagervare ved at vælge en anden lokationskode i feltet **Komponenter på lokation** på lagervarekortet. Bemærk, at dette sjældent giver mening, da planlægningslogikken kan blive forvrænget ved planlægning for lagervarekomponenten.

Et andet vigtigt felt er feltet **Maks. ordrestørrelse** på kortet **Vare**. Det angiver det største tilladte vareantal i et ordreforslag og bruges, hvis varen leveres i en fast transportenhed, f.eks. en container, som du vil udnytte fuldt ud. Når behovet for genopfyldning er registreret, og lotstørrelsen er reguleret i forhold til den angivne genbestillingsmetode, reduceres antallet, hvis det er nødvendigt, for at overholde den højeste tilladte ordrestørrelse, du har defineret for varen. Hvis der er flere krav, beregnes der nye ordrer for at overholde dem. Dette felt er beregnet til at blive brugt sammen med produktionsmetoden Fremstil-til-lager.  

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

Hvis du ofte har brug for at planlægge behov på forskellige lokationer, anbefales det derfor at bruge funktionen Lagervarer.  

## <a name="see-also"></a>Se også

[Skabelon](production-planning.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Opsætte lagervarer](inventory-how-to-set-up-stockkeeping-units.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)  
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]