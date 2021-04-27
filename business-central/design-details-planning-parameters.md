---
title: Designoplysninger – Planlægningsparametre | Microsoft Docs
description: I dette emne beskrives de forskellige planlægningsparametre, du kan bruge i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, design
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6e7e02cba2648f0791925acc6f0e2c0b9662e345
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779578"
---
# <a name="design-details-planning-parameters"></a>Designoplysninger: Planlægningsparametre
I dette emne beskrives de forskellige planlægningsparametre, du kan bruge i [!INCLUDE[prod_short](includes/prod_short.md)].  

Den måde, som planlægningssystemet styrer vareforsyning på, bestemmes af forskellige indstillinger på varekortet eller lagervaren og indstillinger under produktionsopsætning. Følgende tabel viser, hvordan disse parametre bruges til planlægning.  

|Formål|Parameter|  
|-------------|---------------|  
|Definer, om varen skal planlægges|Genbestillingsmetode = Tom|  
|Definer, hvornår du skal genbestille|Interval<br /><br /> Genbestillingspunkt<br /><br /> Sikkerhedstid|  
|Definer, hvor meget du skal genbestille|Sikkerhedslager<br /><br /> Genbestillingsmetode:<br /><br /> -   Fast genbestil.antal og Ordrekvantum<br />-   Maks. antal plus Maks. lagerbeholdning<br />-   Ordre<br />-   Lot-for-Lot|  
|Optimer, hvornår og hvor meget du skal genbestille|Ændringsperiode<br /><br /> Akkumuleringsperiode for lot<br /><br /> Bufferperiode|  
|Ret forsyningsordrer|Min. ordrestørrelse<br /><br /> Maks. ordrestørrelse<br /><br /> Oprundingsfaktor|  
|Afgræns den planlagte vare|Produktionsmetode:<br /><br /> -   Fremstil-til-lager<br />-   Fremstil-til-ordre|  

## <a name="define-if-the-item-will-be-planned"></a>Definer, om varen bliver planlagt  
Hvis du vil medtage en vare/lagervare i planlægningsprocessen, skal den have en genbestillingsmetode, ellers skal det planlægges manuelt, for eksempel med funktionen Ordreplanlægning.  

## <a name="define-when-to-reorder"></a>Definer, hvornår du skal genbestille  
Genbestillingsforslag frigives normalt kun, når det forventede disponible antal er faldet til eller under et bestemt antal. Dette antal defineres af genbestillingspunktet. Ellers vil det være nul. Nul kan reguleres ved at angive et sikkerhedslager. Hvis brugeren har defineret en sikkerhedstid, medfører det, at forslaget leveres i perioden før den krævede forfaldsdato.  

Feltet **Interval** bruges af genbestillingspunkt metoder (**Fast genbestil.antal** og **Maks. antal**), hvor lagerniveauet kontrolleres efter hvert tidsinterval. Det første interval starter på den planlagte startdato.  

> [!NOTE]  
>  Ved beregning af intervallerne ignorerer planlægningssystemet eventuelle arbejdskalendere, der er defineret i feltet **Basiskalenderkode** på siderne **Virksomhedsoplysninger** og **Lokationskort**.  

Standardsikkerhedstiden på siden **Produktionsopsætning**, skal indstilles til mindst én dag. Forfaldsdatoen for behovet kan være kendt, men ikke forfaldstidspunktet. Der planlægges bagud for at imødekomme bruttobehov, og hvis der ikke er defineret nogen sikkerhedstid, kan varerne ankomme for sent til at opfylde behovet.  

Tre ekstra felter for genbestillingsperiode **Ændringsperiode**, **Akkumuleringsperiode for lot**, og **Bufferperiode** spiller også en rolle, når det skal defineres, hvornår der skal genbestilles. Du kan finde flere oplysninger i [Optimere, hvornår og hvor meget der genbestilles](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

## <a name="define-how-much-to-reorder"></a>Definer, hvor meget du skal genbestille  
Hvis planlægningssystemet registrerer behovet for genbestilling, bruges den valgte genbestillingsmetode til at bestemme, hvornår og hvor meget der skal bestilles.  

Uafhængigt af genbestillingsmetoden følger planlægningssystemet sædvanligvis denne logik:  

1. Antallet af ordreforslag beregnes, så det opfylder det angivne minimumslagerniveau for varen, normalt sikkerhedslageret. Hvis der ikke er angivet noget, er det minimale lagerniveau nul.  
2. Hvis den forventede disponible beholdning er under mængden på sikkerhedslageret, foreslås en forsyningsordre, der er planlagt bagud. Ordreantallet udfylder mindst sikkerhedslagermængden og kan forøges af bruttobehov inden for intervallet, af genbestillingsmetoden og af ordremodifikatorer.  
3. Hvis den forventede beholdning ligger på eller under genbestillingspunktet (beregnet fra aggregerede ændringer inden for intervallet) og over sikkerhedslageret, foreslås en undtagelsesordre, der er planlagt fremad. Både bruttobehovet, der skal opfyldes, og genbestillingsmetoden bestemmer ordreantallet. Ordreantallet skal som minimum opfylde genbestillingspunktet.  
4. Hvis der er flere bruttobehov før slutdatoen for ordreforslag, der er planlagt fremad, og dette behov bringer den aktuelt beregnede forventede disponible beholdning under sikkerhedslageret, øges ordremængden for at opveje underskuddet. Den foreslåede forsyningsordre planlægges derefter baglæns fra bruttobehovets forfaldsdato, der ville have overtrådt sikkerhedslageret.  
5. Hvis feltet **Interval** ikke er udfyldt, er det kun bruttobehovet på samme forfaldsdato, der vil blive tilføjet.  

     De tre følgende felter for genbestillingsperiode spiller også en rolle, når det skal defineres, hvor meget der skal genbestilles: **Ændringsperiode**, **Akkumuleringsperiode for lot**, og **Bufferperiode**. Du kan finde flere oplysninger i [Optimere, hvornår og hvor meget der genbestilles](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

### <a name="reordering-policies"></a>Genbestillingsmetoder  
Følgende genbestillingsmetoder påvirker den mængde, der genbestilles.  

|Genbestillingsmetode|Beskrivelse|  
|-----------------------|---------------------------------------|  
|**Fast genbestil.antal**|Som et minimum vil ordremængden være lig genbestillingsantallet. Det kan forhøjes for at imødekomme behovet eller det ønskede lagerniveau. Denne genbestillingsmetode bruges normalt med et genbestillingspunkt.|  
|**Maks. antal**|Ordreantallet vil blive beregnet til at opfylde det maksimale lager. Hvis antal modifikatorer anvendes, kan maksimumlageret blive overtrådt. Vi anbefaler ikke, at du bruger intervallet sammen med maksimalt antal. Intervallet tilsidesættes sædvanligvis. Denne genbestillingsmetode bruges normalt med et genbestillingspunkt.|  
|**Ordre**|Ordreantallet vil blive beregnet til at opfylde hver enkelt behovshændelse, og behov-forsyningssættet forbliver sammenkædet indtil udførelse. Ingen planlægningsparametre overvejes.|  
|**Lot-for-Lot**|Antallet beregnes for at opfylde summen for det behov, der bliver forfaldent i intervallet.|  

##  <a name="optimize-when-and-how-much-to-reorder"></a>Optimer, hvornår og hvor meget du skal genbestille  
En planlægger vil, for at få en rationel forsyningsplan, finjustere planlægningsparametre for at begrænse ændringsforslag, akkumulere behov (dynamisk genbestillingsantal) eller for at undgå ubetydelige planlægningshandlinger. Følgende genbestillingsperiodefelter optimerer, hvornår og hvor meget der skal genbestilles.  

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Ændringsperiode**|Dette felt bruges til at afgøre, om aktionsmeddelelsen skal omplanlægge en eksisterende ordre eller annullere den og oprette en ny ordre. Den eksisterende ordre bliver ændret i én ændringsperiode før den aktuelle forsyning og indtil én ændringsperiode efter den aktuelle forsyning.|  
|**Akkumuleringsperiode for lot**|Dette felt bruges sammen med genbestillingsmetoden Lot-for-Lot, til at akkumulere flere forsyningsbehov i én forsyningsordre. Fra datoen for den første planlagte forsyning akkumulerer systemet alle forsyninger i den følgende akkumuleringsperiode for lot i én forsyning, der placeres på datoen for den første forsyning. Behov, som er uden for akkumuleringsperioden for lot, er ikke omfattet af denne forsyning.|  
|**Bufferperiode**|Dette felt bruges til at undgå mindre omlægning af eksisterende forsyningsordrer i fremtiden. Ændringer fra forsyningsdatoen til en bufferperiode fra forsyningsdatoen genererer ikke nogen aktionsmeddelelser.<br /><br /> Bufferperioden angiver en tidsperiode, hvor planlægningsprogrammet ikke skal foreslå at omplanlægge eksisterende forsyningsordrer fremad. Dette begrænser antallet af ubetydelige forsalg til ny planlægning for eksisterende forsyning til en senere dato, hvis ændringsdatoen er inden for bufferperioden.<br /><br /> Derfor vil et positivt delta mellem den foreslåede nye forsyningsdato og den oprindelige forsyningsdato altid være større end bufferperioden.|  
> [!NOTE]
> Med genbestillingsmetoden Lot-for-Lot skal værdien i feltet **Akkumuleringsperiode for lot** være lig med eller større end værdien i feltet **Bufferperiode**. I modsat fald reduceres bufferperioden automatisk under planlægningsrutinen, så den svarer til akkumuleringsperioden for lot.  

Tidspunktet for ændringsperiode, bufferperiode og akkumuleringsperiode for lot er baseret på en forsyningsdato. Intervallet er baseret på planlægningens startdato, som vist i følgende illustration.  

![Intervalelementer](media/supply_planning_5_time_bucket_elements.png "Intervalelementer")  

I nedenstående eksempler repræsenterer sorte pile eksisterende forsyning (op) og behov (ned). Rød, grøn og orange pil er planlægningsforslag.  

**Eksempel 1**: Den ændrede dato er uden for ændringsperioden, hvilket forårsager, at den eksisterende forsyning bliver annulleret. Der foreslås en ny forsyning til at dække behovet i akkumuleringsperioden for lot.  

![Ændringsperiode og Akkumuleringsperiode for lot](media/supply_planning_5_recheduling_period_lot_accumulation_period.png "Ændringsperiode og Akkumuleringsperiode for lot")  

**Eksempel 2**: Den ændrede dato er inden for ændringsperioden, hvilket forårsager, at den eksisterende forsyning skal omplanlægges. Der foreslås en ny forsyning til at dække behovet uden for akkumuleringsperioden for lot.  

![Ændringsperiode, Akkumuleringsperiode for lot og ændring](media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png "Ændringsperiode, Akkumuleringsperiode for lot og ændring")  

**Eksempel 3**: Der er et behov i bufferperioden, og forsyningsantallet i akkumuleringsperioden for lot svarer til forsyningsantallet. Næste behov er uafdækket, og der foreslås en ny forsyning.  

![Bufferperiode og Akkumuleringsperiode for lot](media/supply_planning_5_dampener_period_lot_accumulation_period.png "Bufferperiode og Akkumuleringsperiode for lot")  

**Eksempel 4**: Der er et behov i bufferperioden, og forsyningen forbliver på samme dato. Den aktuelle forsyningsmængde er dog ikke nok til at dække efterspørgslen i akkumuleringsperioden for lot, så en handling, der skifter mængde af den eksisterende forsyningsordre, foreslås.  

![Bufferperiode, Akkumuleringsperiode for lot og Rediger antal](media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png "Bufferperiode, Akkumuleringsperiode for lot og Rediger antal")  

**Standardværdier:** Standardværdien for feltet **Interval** og de tre felter for genbestillingsperioden er tomme. For alle felter, undtagen feltet **Bufferperiode**, betyder det 0D (nul dage). Hvis feltet **Bufferperiode** er tomt, bruges den globale værdi i feltet **Standardbufferperiode** på siden **Produktionsopsætning**.  

## <a name="modify-the-supply-orders"></a>Ret forsyningsordrerne  
Når antallet af ordreforslaget er beregnet, kan en eller flere af ordremodifikatorerne justere den. Det maksimale ordreantal er f.eks. større end eller lig med det mindst tilladte ordreantal, som er større end eller lig med oprundingsfaktoren.  

Antallet reduceres, hvis det overskrider det maksimale ordreantal. Derefter forøges det, hvis det er under det mindst tilladte ordreantal. Endelig skal det rundes op, så det passer til en bestemt oprundingsfaktor. Eventuelle restmængder bruger de samme justeringer, indtil det samlede behov er blevet konverteret til ordreforslag.  

## <a name="delimit-the-item"></a>Afgræns varen  
Indstillingen **Produktionsmetode** definerer, hvilke yderligere ordrer MPS-beregningen foreslår.  

Hvis indstillingen **Fremstil-til-lager** bruges, vedrører ordrerne kun varen.  

Hvis indstillingen **Fremstil-til-ordre** bruges, vil planlægningssystemet analysere produktionsstyklisten for varen og oprette yderligere tilknyttede ordreforslag for disse elementer på lavere niveauer, der også er defineret som Fremstil-til-ordre. Dette fortsætter, så længe der er fremstil-til-ordre-varer i de faldende styklistestrukturer.  

## <a name="see-also"></a>Se også  
[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
[Designoplysninger: Afstemning af behov og efterspørgsel](design-details-balancing-demand-and-supply.md)   
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]