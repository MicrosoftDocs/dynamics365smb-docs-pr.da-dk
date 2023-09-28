---
title: Planlægge med eller uden lokationer
description: 'I dette emne kan du finde oplysninger om produktion og bearbejdning, herunder forsyningsplanlægning, i Business central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/15/2022
ms.author: bholtorf
---
# <a name="planning-with-or-without-locations"></a>Planlægge med eller uden lokationer

Før du begynder at bruge planlægningsprogrammet, anbefaler vi, at du beslutter, om du vil bruge lokationer. Der er to enkle, enkle muligheder:

* behovslinjer altid har lokationskoder, og systemet bruger lagervarer i fuld udstrækning, herunder den relevante lokationsopsætning. Flere oplysninger [Behov på lokation](#demand-at-location).  
* behovslinjer har aldrig lokationskoder, og systemet bruger varekortet. Se [Behov på en "tom lokation"](#demand-at-blank-location) nedenfor.

## <a name="demand-at-location"></a>Behov på lokation

Når planlægningssystemet registrerer behov på en lokation (en linje med en lokationskode), fungerer det forskelligt afhængigt af 2 vigtige opsætningsværdier.  

Under et planlægningsforløb kontrollerer systemet de 2 opsætningsværdier en efter en og planlægger i overensstemmelse med dem:  

1. Findes der en SKU for varen på den efterspurgte lokation?  

    Hvis ja, så:  

    Varen planlægges i overensstemmelse med planlægningsparametrene på lagerkortet.  

    Hvis nej, så:  

2. Indeholder feltet **Komponenter på lokation** på siden **Produktionsopsætning** den krævede lokationskode?  

    Hvis ja, så:  

    Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.  

    Hvis nej, så:  

    Varen planlægges i overensstemmelse med det "minimale alternativ", der dækker det nøjagtige behov. Varen planlægges i overensstemmelse med: Genbestillingsmetode = *Lot-for-Lot*, Medtag lager = *Ja*, alle andre planlægningsparametre = tomme. (Varer, der benytter genbestillingsmetoden *Ordre*, fortsætter med at bruge *Ordre* såvel som de andre indstillinger.)

> [!TIP]
> Hvis du tit har brug for at planlægge behov på forskellige lokationer, anbefales det at bruge funktionen Lagervarer pr. lokation og undgår behov på tomme lokationer. Flere oplysninger i [Konfigurere Lagervarer pr. lokation](inventory-how-to-set-up-stockkeeping-units.md)

Se forskellene i [scenarierne nedenfor](#scenarios).

> [!NOTE]
> Feltet **Komponenter på Lokation** på siden **Produktionsopsætning** er meget vigtigt, når du skal styre planlægningssystemets håndtering af produktionsbehovslinjer.
>
> I forbindelse med produktionsbehov bruger [!INCLUDE [prod_short](includes/prod_short.md)] den samme lokation til halvfabrikata og komponenter som den, der er angivet på produktionsordren. Hvis du udfylder dette felt, kan du dog omdirigere halvfabrikata og komponenter til en anden lokation.
>
> Du kan også definere dette for en specifik lagervare ved at vælge en anden lokationskode i feltet **Komponenter på lokation** på lagervarekortet. Bemærk, at dette sjældent giver mening, da planlægningslogikken kan blive forvrænget ved planlægning for lagervarekomponenten.

## <a name="demand-at-blank-location"></a>Behov på "tom lokation"

Når planlægningssystemet finder behov på en tom lokation (en linje uden en lokationskode), planlægges varen generelt i overensstemmelse med planlægningsparametrene på varekortet.

Feltet **Tvungen lokationskode** på siden **Lageropsætning**, feltet **Komponenter på lokation** på siden **Produktionsopsætning** eller lagervareenheder styrer, hvordan planlægningssystemets håndterer behovslinjer med/uden lokationskoder. Hvis et af følgende udsagn er sandt, anses efterspørgsel på tom lokation også for en afvigelse, og planlægningssystemet reagerer ved at bruge det udskrive det "minimale alternativ": Varen planlægges i henhold til: Genbestillingsmetode = *Lot-for-Lot* (*Ordre* forbliver *Ordre*), Medtag lager = *Ja*, alle andre planlægningsparametre = Tomme.

* På siden **Produktionsopsætning** er feltet **Komponenter på lokation** har en værdi.
* Der findes en lagervare for den planlagte vare.
* Feltet **obligatorisk lokation** er markeret.

## <a name="scenarios"></a>Eksempler

Se forskellene i opsætningseksemplerne nedenfor.

### <a name="setup-1"></a>Opsætning 1

* Tvungen lokationskode = *Ja*  
* SKU er konfigureret for *VEST*  
* Komponenter på lokation = *ØST*  

#### <a name="case-11-demand-is-at-west-location"></a>Situation 1.1: Behov findes på lokationen *VEST*

Varen planlægges i overensstemmelse med planlægningsparametrene på lagerkortet (herunder mulig overflytning).

#### <a name="case-12-demand-is-at-east-location"></a>Situation 1.2: Behov findes på lokationen *ØST*

Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.

#### <a name="case-13-demand-is-at-north-location"></a>Situation 1.3: Behovet findes på lokationen *NORD*

Varen planlægges i overensstemmelse med: Genbestillingsmetode = *Lot-for-Lot* (*Ordre* forbliver *Ordre*), Medtag lager = *Ja*, alle andre planlægningsparametre = tomme.

#### <a name="case-14-demand-is-at-blank-location"></a>Situation 1.4: Behovet findes på lokationen *TOM*

Varen planlægges i overensstemmelse med: Genbestillingsmetode = *Lot-for-Lot* (*Ordre* forbliver *Ordre*), Medtag lager = *Ja*, alle andre planlægningsparametre = tomme.

### <a name="setup-2"></a>Opsætning 2

* Tvungen lokationskode = *Ja*  
* Ingen lagervare defineret  
* Komponenter på lokation = *ØST*  

#### <a name="case-21-demand-is-at-west-location"></a>Situation 2.1: Behov findes på lokationen *VEST*

Varen planlægges i overensstemmelse med: Genbestillingsmetode = *Lot-for-Lot* (*Ordre* forbliver *Ordre*), Medtag lager = *Ja*, alle andre planlægningsparametre = tomme.

#### <a name="case-22-demand-is-at-east-location"></a>Situation 2.2: Behov findes på lokationen *ØST*

Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.  

### <a name="setup-3"></a>Opsætning 3

* Tvungen lokationskode = *Nej*  
* Ingen lagervare defineret  
* Komponenter på lokation = *ØST*  

#### <a name="case-31-demand-is-at-west-location"></a>Situation 3.1: Behov findes på lokationen *VEST*

Varen planlægges i overensstemmelse med: Genbestillingsmetode = *Lot-for-Lot* (*Ordre* forbliver *Ordre*), Medtag lager = *Ja*, alle andre planlægningsparametre = tomme.

#### <a name="case-32-demand-is-at-east-location"></a>Situation 3.2: Behov findes på lokationen *ØST*

Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.  

#### <a name="case-33-demand-is-at-blank-location"></a>Situation 3.3: Behovet findes på lokationen *TOM*

Varen planlægges i overensstemmelse med: Genbestillingsmetode = *Lot-for-Lot* (*Ordre* forbliver *Ordre*), Medtag lager = *Ja*, alle andre planlægningsparametre = tomme.

### <a name="setup-4"></a>Opsætning 4

* Tvungen lokationskode = *Nej*  
* Ingen lagervare defineret  
* Komponenter på lokation = *TOM*  

#### <a name="case-41-demand-is-at-east-location"></a>Situation 4.1: Behov findes på lokationen *ØST*

Varen planlægges i overensstemmelse med: Genbestillingsmetode = *Lot-for-Lot* (*Ordre* forbliver *Ordre*), Medtag lager = *Ja*, alle andre planlægningsparametre = tomme.

#### <a name="case-42-demand-is-at-blank-location"></a>Situation 4.2: Behovet findes på lokationen *TOM*

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
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
