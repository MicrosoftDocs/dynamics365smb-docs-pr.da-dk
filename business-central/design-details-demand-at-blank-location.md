---
title: Designoplysninger – Behov og forsyning | Microsoft Docs
description: I dette emne introduceres begrebet behov, der er fællesbetegnelsen for enhver form for bruttobehov, som f.eks. en salgsordre og et komponentbehov fra en produktionsordre.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 3b5f390343f74bc559cce48b2037edd125f829ca
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143630"
---
# <a name="design-details-demand-at-blank-location"></a>Designoplysninger: Behov på lokationen TOM
Når en bruger opretter en behovshændelse, f.eks. en salgsordrelinje, tillader programme sommetider brugeren at angive en lokationskode, og andre gange gør det ikke og bruger dermed en tom lokation.

For behov med eller uden lokationskoder fungerer planlægningssystemet på samme ukomplicerede måde, når:

- Behovslinjer altid har lokationskoder, og systemet bruger lagervarer i fuld udstrækning, herunder den relevante lokationsopsætning.
- Behovslinjer aldrig har lokationskoder, og systemet ikke bruger lagervarer eller nogen form for lokationsopsætning (se sidste eksempel i følgende afsnit).

Men hvis behovshændelser sommetider har lokationskoder og sommetider ikke, vil planlægningssystemet følge visse regler afhængigt af opsætningen.

## <a name="demand-at-location"></a>Behov på lokation
Når planlægningssystemet registrerer behov på en lokation, fungerer det forskelligt afhængigt af tre vigtige opsætningsværdier. Under et planlægningsforløb kontrollerer systemet de tre opsætningsværdier en efter en og planlægger i overensstemmelse med dem.

1. Er feltet **Tvungen lokationskode** markeret?

    Hvis ja, så:

2. Er varen registreret som lagervare?

    Hvis ja, så:

    Varen planlægges i overensstemmelse med planlægningsparametrene på lagerkortet.

    Hvis nej, så:

3. Indeholder feltet Komponenter på lokation den efterspurgte lokationskode?

  Hvis ja, så:

  Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.

  Hvis nej, så:

  Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot, Medtag lager = Ja, alle andre planlægningsparametre = tomme, varer der bruger genbestillingsmetoden Ordre, fortsætter med at bruge Ordre sammen med de andre indstillinger.

> [!NOTE]
> Den ekstraordinære opsætning af planlægningen, der er output som den sidste reaktion i trin 3 ovenfor, omtales i det følgende som det "minimale alternativ". Denne planlægningsopsætning dækker kun det nøjagtige behov, og alle andre planlægningsparametre ignoreres.

Hvis du ønsker oplysninger om variationer af denne planlægningslogik, kan du se afsnittet Scenarier herunder.

## <a name="demand-at-blank-location"></a>Behov på tom lokation
Selv hvis feltet **Tvungen lokationskode** er markeret, tillader systemet, at behovslinjer oprettes uden lokationskode, også kaldet en tom lokation. Dette er en afvigelse for systemet, da det har forskellige opsætningsværdier, der er indstillet til at håndtere lokationer (se ovenfor), og som et resultat opretter planlægningsprogrammet ikke en planlægningslinje for en behovslinje.

Hvis feltet **Tvungen lokationskode** ikke er markeret, men en eller flere af opsætningsværdierne findes, anses det også for en afvigelse, og planlægningssystemet reagerer ved at bruge det "minimale alternativ": Varen planlægges i henhold til: Genbestillingsmetode = Lot-for-Lot (ordre forbliver ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.

## <a name="scenarios"></a>Eksempler
Følgende scenarier beskriver variationer af behov på tom lokation, og hvordan planlægningssystemet oversætter til det "minimale alternativ".

### <a name="setup-1"></a>Opsætning 1:
Tvungen lokationskode = Ja

Lagervare er konfigureret for RØD

Komponenter på lokation = BLÅ

#### <a name="case-11-demand-is-at-red-location"></a>Situation 1.1: Behov findes på lokationen RØD
Varen planlægges i overensstemmelse med planlægningsparametrene på lagerkortet.

#### <a name="case-12-demand-is-at-blue-location"></a>Situation 1.2: Behov findes på lokationen BLÅ
Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot ( Ordre forbliver Ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.

#### <a name="case-13-demand-is-at-green-location"></a>Situation 1.3: Behov findes på lokationen GRØN
Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot ( Ordre forbliver Ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.

#### <a name="case-14-demand-is-at-blank-location"></a>Situation 1.4: Behov findes på lokationen TOM
Varen planlægges ikke, fordi der ikke er defineret en lokation på behovslinjen.

### <a name="setup-2"></a>Opsætning 2:
Tvungen lokationskode = Ja

Ingen lagervare defineret

Komponenter på lokation = BLÅ

#### <a name="case-21-demand-is-at-red-location"></a>Situation 2.1: Behov findes på lokationen RØD
Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot ( Ordre forbliver Ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.

#### <a name="case-22-demand-is-at-blue-location"></a>Situation 2.2: Behov findes på lokationen BLÅ
Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.

### <a name="setup-3"></a>Opsætning 3:
Tvungen lokationskode = Nej

Ingen lagervare defineret

Komponenter på lokation = BLÅ

#### <a name="case-31-demand-is-at-red-location"></a>Situation 3.1: Behov findes på lokationen RØD
Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot ( Ordre forbliver Ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.

#### <a name="case-32-demand-is-at-blue-location"></a>Situation 3.2: Behov findes på lokationen BLÅ
Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.

#### <a name="case-33-demand-is-at-blank-location"></a>Situation 3.3: Behov findes på lokationen TOM
Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot ( Ordre forbliver Ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.

### <a name="setup-4"></a>Opsætning 4:
Tvungen lokationskode = Nej

Ingen lagervare defineret

Komponenter på lokation = TOM

#### <a name="case-41-demand-is-at-blue-location"></a>Situation 4.1: Behov findes på lokationen BLÅ
Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot ( Ordre forbliver Ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.

#### <a name="case-42-demand-is-at-blank-location"></a>Situation 4.2: Behov findes på lokationen TOM
Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.

Som det er illustreret i det sidste eksempel, kan man kun få det rigtige resultat for en behovslinje uden en lokationskode ved at deaktivere alle opsætningsværdier, der er knyttet til lokationer. Ligeledes kan man kun få stabile planlægningsresultater for behov på lokationer ved at bruge lagervarer. Hvis virksomheder ofte planlægger ud fra behov på lokationer, anbefales de derfor kraftigt at benytte begrebet Lagervarer.

## <a name="see-also"></a>Se også  
[Designoplysninger: Afstemning af behov og efterspørgsel](design-details-balancing-demand-and-supply.md)   
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]