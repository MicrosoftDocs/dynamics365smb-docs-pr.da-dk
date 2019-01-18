---
title: "Designoplysninger – Genbestillingsmetoder | Microsoft Docs"
description: Dette emne giver et overblik over metoder til varegenbestilling.
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
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 4aaef129da953596632b56716eaff2f0c47736f7
ms.contentlocale: da-dk
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-reordering-policies"></a>Designoplysninger: Genbestillingsmetoder
Genbestillingsmetoder definerer, hvor meget der skal bestilles, når varen skal genbestilles. Der findes fire forskellige genbestillingsmetoder.  

## <a name="fixed-reorder-qty"></a>Fast genbestil.antal
Fast genbestil.antal er relateret til lageret, planlægning af typiske C-varer (lav lageromkostning, lav risiko for forældelse og/eller mange varer). Denne metode bruges normalt i forbindelse med et genbestillingspunkt, hvilket afspejler det forventede behov under leveringstiden for varen.  

### <a name="calculated-per-time-bucket"></a>Beregnet pr. interval  
 Hvis planlægningssystemet har registreret, at genbestillingspunktet er nået eller overskredet i et bestemt interval (genbestillingscyklus) – over eller ved genbestillingspunktet i begyndelsen af perioden og under eller ved genbestillingspunktet sidst i perioden – vil den foreslå at oprette en ny forsyningsordre af det angivne genbestillingsantal og planlægge det fremad fra den første dag efter slutningen af intervallet.  

 Det tidsbegrænsede genbestillingspunkt reducerer antallet af forsyningsforslag. Dette afspejler den manuelle proces, der består i ofte at gå gennem lageret for at kontrollere det faktiske indhold på de forskellige placeringer.  

### <a name="creates-only-necessary-supply"></a>Opretter kun nødvendige forsyninger  
 Før der foreslås, at en ny forsyningsordre opfylder et genbestillingspunkt, kontrollerer planlægningssystemet, om forsyning allerede er bestilt til modtagelse inden for varens leveringstid. Hvis en eksisterende forsyningsordre kan løse problemet ved at bringe den projekterede lagerbeholdning til eller over genbestillingspunktet inden for leveringstiden, vil systemet ikke foreslå en ny forsyningsordre.  

 Forsyningsordrer, der er oprettet specielt med henblik på at opfylde genbestillingspunktet, er udelukket fra almindelig forsyningsafstemning og vil ikke på nogen måde blive ændret bagefter. Hvis en vare, der bruger genbestillingspunktet skal udfases (ikke genbestilt), er det derfor hensigtsmæssigt at gennemgå udestående forsyningsordrer manuelt eller ændre genbestillingsmetoden til lot-for-lot, hvorved systemet vil reducere eller annullere overflødige forsyninger.  

### <a name="combines-with-order-modifiers"></a>Kombineres med ordremodifikatorer  
 Ordremodifikatorerne Min. ordrestørrelse, Maks. ordrestørrelse og Oprundingsfaktor bør ikke spille en stor rolle, når metoden for fast genbestillingsantal bruges. Dog tager planlægningssystemet stadig højde for disse modifikatorer og vil reducere antallet til det angivne maksimale ordreantal (og oprette to eller flere forsyninger for at nå det samlede ordreantal), øge ordren til den angivne minimummængde eller runde ordreantallet op for at opfylde en bestemt oprundingsfaktor.  

### <a name="combines-with-calendars"></a>Kombinerer med kalendere  
 Før der bliver foreslået en ny forsyningsordre for at opfylde et genbestillingspunkt, kontrollerer planlægningssystemet, om ordren er planlagt til en ikkearbejdsdag i overensstemmelse med de kalendere, der er defineret i feltet **Basiskalenderkode** på siderne **Virksomhedsoplysninger** og **Lokationskort**.  

 Hvis den planlagte dato er en ikkearbejdsdag, flytter planlægningssystemet ordren frem til den nærmeste arbejdsdag. Det kan resultere i en ordre, der opfylder et genbestillingspunkt, men ikke opfylder visse specifikke behov. Planlægningssystemet opretter en ekstra levering for sådanne behov.  

### <a name="should-not-be-used-with-forecast"></a>Bør ikke bruges med forecast  
 Det er ikke nødvendigt at medtage en prognose i planlægningen af en vare ved hjælp af et genbestillingspunktet, fordi det forventede behov allerede er angivet i genbestillingspunktet. Hvis det er relevant at basere planen på et forecast, kan du bruge politikken lot-for-lot.  

### <a name="must-not-be-used-with-reservations"></a>Må ikke anvendes med reservationer  
 Hvis brugeren har reserveret en mængde, for eksempel et antal på lageret, til nogle fremtidige behov, bliver grundlaget for planlægningen forstyrret. Selvom det planlagte beholdningsniveau er acceptabelt i relation til genbestillingspunktet, er mængderne muligvis ikke tilgængelige. Systemet kan forsøge at kompensere for dette ved at oprette undtagelsesordrer. Det anbefales dog, at feltet Reserver angives til Aldrig på varer, der er planlagt ved hjælp af et genbestillingspunkt.

## <a name="maximum-qty"></a>Maks. antal
Det maksimale antal er en måde at vedligeholde lageret ved hjælp af et genbestillingspunkt.  

Alt om den faste genbestillingsantalmetode gælder også for denne metode. Den eneste forskel er omfanget af den foreslåede forsyning. Når metoden med maksimalt antal bruges, defineres genbestillingsantallet dynamisk baseret på det planlagte lagerniveau og varierer derfor normalt fra ordre til ordre.  

### <a name="calculated-per-time-bucket"></a>Beregnet pr. interval  
Genbestillingsantallet bestemmes på det tidspunkt (slutningen af et interval), hvor planlægningssystemet registrerer, at genbestillingspunktet er passeret. På dette tidspunkt måler systemet afstanden fra den nuværende forventede lagerbeholdning op til den angivne maksimale lagerbeholdning. Dette består af det antal, der skal genbestilles. Derefter kontrollerer systemet, om leveringen allerede er bestilt andre steder med henblik på at blive modtaget inden for leveringstiden, og i så fald reduceres mængden af den nye forsyningsordre med allerede bestilte antal.  

Systemet sikrer, at den projekterede lagerbeholdning mindst når genbestillingsniveauet – i tilfælde af at brugeren har glemt at angive et maksimalt lagerantal.  

### <a name="combines-with-order-modifiers"></a>Kombineres med ordremodifikatorer  
Afhængigt af opsætningen, kan det være bedst at kombinere metoden Maks. antal med ordremodifikatorer for at sikre et mindste ordreantal eller afrunde til et heltal af købsmåleenheder eller opdele det i flere lotter, som er defineret af det højst tilladte antal.  

### <a name="combines-with-calendars"></a>Kombinerer med kalendere  
Før der bliver foreslået en ny forsyningsordre for at opfylde et genbestillingspunkt, kontrollerer planlægningssystemet, om ordren er planlagt til en ikkearbejdsdag i overensstemmelse med de kalendere, der er defineret i feltet **Basiskalenderkode** på siderne **Virksomhedsoplysninger** og **Lokationskort**.  

Hvis den planlagte dato er en ikkearbejdsdag, flytter planlægningssystemet ordren frem til den nærmeste arbejdsdag. Det kan resultere i en ordre, der opfylder et genbestillingspunkt, men ikke opfylder visse specifikke behov. Planlægningssystemet opretter en ekstra levering for sådanne behov.

## <a name="order"></a>Sorteringsrækkefølge
I et Fremstil-til-ordre-miljø bliver en vare købt eller produceret udelukkende til at dække et bestemt behov. Normalt relateres det til A-varer, og motivationen for at vælge denne ordregenbestillingsmetode kan være, at behovet er sjældent, leveringstiden er ubetydelig, eller de påkrævede attributter varierer.  

Programmet opretter et ordre-til-ordre-link, der fungerer som en indledende forbindelse mellem forsyningen, en forsyningsordre eller lager og det behov, som den eller det skal opfylde.  

Bortset fra brug af prdrepolitikken, kan ordre-til-ordre-linket anvendes under planlægningen på følgende måder:  

* Når produktionsmetoden Fremstil-til-ordre bruges til at oprette produktionsordrer med flere niveauer eller produktionsordrer af projekttype (fremstilling af nødvendige komponenter på den samme produktionsordre).  
* Når funktionen Salgsordreplanlægning bruges til at oprette en produktionsordre fra en salgsordre.  

Selvom en produktionsvirksomhed anser sig selv som værende et Fremstil-til-ordre-miljø, kan det være bedst at bruge en genbestillingsmetode med lot-for-lot, hvis varerne er ren standard uden variation i attributter. Som resultat vil systemet bruge ikke-planlagt lagerbeholdning og akkumulerer kun salgsordrer med samme afsendelsesdato eller inden for et defineret interval.  

### <a name="order-to-order-links-and-past-due-dates"></a>Ordre-til-ordre-links og overskredne datoer  
I modsætning til de fleste forsyning-behov-sæt, planlægges tilknyttede ordrer med forfaldsdatoer, før planlægningsstartdatoen er fuldt planlagt af systemet. Forretningsårsagen til denne undtagelse er, at bestemte behov-forsyningssæt skal synkroniseres til kørsel. Du kan finde flere oplysninger om den fastlåste zone, der gælder for de fleste behovsforsyningstyper i [Designoplysninger: Håndtering af ordrer før planlægningsstartdatoen](design-details-dealing-with-orders-before-the-planning-starting-date.md).

## <a name="lot-for-lot"></a>Lot-for-Lot
Lot-for-lot-politik er den mest fleksible, fordi systemet kun reagerer på det faktiske behov, plus det fungerer på forventet behov fra prognose og rammeordrer og udligner derefter ordreantallet på baggrund af behovet. Lot-for-lot-politik tager sigte på A - og B-varer, hvor lageret kan accepteres, men bør undgås.  

På nogle måder ser lot-for-lot politik ud som ordrepolitikken, men der er en generisk tilgang til varer: Den kan acceptere antal på lager, og den kombinerer behov og tilsvarende forsyning i intervaller, der er defineret af brugeren.  

Intervallet er defineret i feltet **Interval**. Systemet fungerer med et mindste interval på én dag, da det er den mindste tidsenhed på behovs- og forsyningshændelser i systemet (selvom tidsenheden på produktionsordrer og komponentbehov i praksis kan være sekunder).  

Intervallet angiver også grænser for, hvornår en eksisterende forsyningsordre bør omplanlægges for at opfylde et bestemt behov. Hvis forsyningen ligger i intervallet, bliver den flyttet ind eller ud for at opfylde behovet. Hvis den ligger tidligere, vil det medføre unødvendig ophobning af lageret og skal annulleres. Hvis den ligger senere, oprettes en ny forsyningsordre i stedet.  

Med denne politik er det også muligt at definere et sikkerhedslager for at kompensere for mulige udsving i udbud eller for at imødekomme pludselige behov.  

Da forsyningsordreantallet er baseret på det faktiske behov, kan det være smart at bruge ordremodifikatorer: Rund ordreantallet op, så det passer med en specifik oprundingsfaktor (eller købsenhedskoden), forøg ordren til et fastsat minimumsordreantal, eller reducer antallet til det angivne maksimale antal (og opret derefter to eller flere forsyninger for at nå det nødvendige samlede antal).

## <a name="see-also"></a>Se også  
[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)

