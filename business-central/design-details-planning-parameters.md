---
title: Designoplysninger - Planlægningsparametre
description: 'I denne artikel beskrives de forskellige planlægningsparametre, du kan bruge, og hvordan de påvirker planlægningssystemet.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 04/26/2023
ms.custom: bap-template
---
# <a name="design-details-planning-parameters" />Designoplysninger: Planlægningsparametre

I denne artikel beskrives de forskellige planlægningsparametre, du kan bruge i [!INCLUDE[prod_short](includes/prod_short.md)].  

Den måde, som planlægningssystemet styrer vareforsyning på, bestemmes af forskellige indstillinger på siderne **Varekort**, **SKU** og **Produktionsopsætning**. I følgende tabel forklares det, hvordan planlægningen bruger disse indstillinger.  

|Formål|Indstillinger|
|-------------|---------------|
|Definer, om varen skal planlægges|Genbestillingsmetode = Tom|
|Definer, hvornår du skal genbestille|Tidsinterval<br /><br /> Genbestillingspunkt<br /><br /> Sikkerhedstid|
|Definer, hvor meget du skal genbestille|Sikkerhedslager<br /><br /> Genbestillingsmetode:<br /><br /> -   Fast genbestil.antal og Ordrekvantum<br />-   Maks. antal plus Maks. lagerbeholdning<br />-   Ordre<br />-   Lot-for-Lot|
|Optimer, hvornår og hvor meget du skal genbestille|Ændringsperiode<br /><br /> Akkumuleringsperiode for lot<br /><br /> Bufferperiode|
|Ret forsyningsordrer|Min. ordrestørrelse<br /><br /> Maks. ordrestørrelse<br /><br /> Oprundingsfaktor|
|Afgræns den planlagte vare|Produktionsmetode:<br /><br /> -  Fremstil-til-lager<br />- Fremstil-til-ordre|

## <a name="define-whether-the-item-is-planned" />Definer, om varen skal planlægges

Hvis du vil medtage en vare eller lagervare i planlægningsprocessen, skal du tildele det en genbestillingsmetode. Ellers skal det planlægges manuelt, f.eks. ved hjælp af funktionen Ordreplanlægning.  

## <a name="define-when-to-reorder" />Definer, hvornår du skal genbestille

Genbestillingsforslag frigives normalt kun, når det forventede disponible antal er faldet til eller under et bestemt antal. Dette antal defineres af genbestillingspunktet. Ellers vil det være nul. Nul kan reguleres ved at angive et sikkerhedslager. Hvis du definerer en sikkerhedstid, medfører det, at forslaget leveres i perioden før den krævede forfaldsdato.  

Feltet **Interval** bruges af genbestillingspunktsmetoderne (**Fast genbestillingsantal** og **Maks. antal**). Lagerniveauet kontrolleres efter hvert tidsinterval. Det første interval starter på den planlagte startdato.  

> [!NOTE]  
> Ved beregning af intervallerne ignorerer planlægningssystemet eventuelle arbejdskalendere, der er defineret i feltet **Basiskalenderkode** på siderne **Virksomhedsoplysninger** og **Lokationskort**.  

På siden **Produktionsopsætning**, skal du indstille standardsikkerhedstiden til mindst én dag. Forfaldsdatoen for behovet kan være kendt, men ikke forfaldstidspunktet. Planlægningen planlægger baglæns for at opfylde bruttobehovet. Hvis du ikke definerer en sikkerhedstid, kan varerne blive afleveret for sent for at overholde efterspørgslen.  

Felterne **Ændringsperiode**, **Akkumuleringsperiode for lot** og **Bufferperiode** spiller også en rolle, når det skal defineres, hvornår der skal genbestilles. Du kan finde flere oplysninger i [Optimere, hvornår og hvor meget der genbestilles](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

## <a name="define-how-much-to-reorder" />Definer, hvor meget du skal genbestille

Hvis planlægningssystemet registrerer behovet for genbestilling, bruges genbestillingsmetoden til at bestemme, hvornår og hvor meget der skal bestilles.  

Uafhængigt af genbestillingsmetoden følger planlægningssystemet sædvanligvis denne logik:  

1. Beregn antallet af ordreforslag, så det opfylder det angivne minimumslagerniveau for varen, normalt sikkerhedslageret. Hvis der ikke er angivet noget, er det minimale lagerniveau nul.  
2. Hvis den forventede disponible beholdning er under mængden på sikkerhedslageret, foreslås en forsyningsordre, der er planlagt bagud. Ordreantallet udfylder mindst sikkerhedslagermængden og kan forøges af bruttobehov inden for intervallet, af genbestillingsmetoden og af ordremodifikatorer.  
3. Hvis den forventede beholdning ligger på eller under genbestillingspunktet (beregnet fra aggregerede ændringer inden for intervallet) og over sikkerhedslageret, foreslås en undtagelsesordre, der er planlagt fremad. Både bruttobehovet, der skal opfyldes, og genbestillingsmetoden bestemmer ordreantallet. Ordreantallet skal som minimum opfylde genbestillingspunktet.  
4. Hvis der er flere bruttobehov før slutdatoen for ordreforslag, der er planlagt fremad, og dette behov bringer den aktuelt beregnede forventede disponible beholdning under sikkerhedslageret, øges ordremængden for at opveje underskuddet. Den foreslåede forsyningsordre planlægges derefter baglæns fra bruttobehovets forfaldsdato, der ville have overtrådt sikkerhedslageret.  
5. Hvis feltet **Interval** ikke er udfyldt, er det kun bruttobehovet på samme forfaldsdato, der vil blive tilføjet.  

### <a name="reordering-policies" />Genbestillingsmetoder

Følgende genbestillingsmetoder påvirker den mængde, der genbestilles. Du kan lære mere om genbestillingsmetode ved at gå til [Designdetaljer: Håndtere genbestillingsmetoder](design-details-handling-reordering-policies.md).  

|Genbestillingsmetode|Beskrivelse|  
|-----------------------|---------------------------------------|  
|**Fast genbestil.antal **|Som et minimum vil ordremængden være lig genbestillingsantallet. Du kan øge antallet for at imødekomme behovet eller det ønskede lagerniveau. Denne genbestillingsmetode bruges normalt med et genbestillingspunkt.|  
|**Maks. antal **|Ordreantallet vil blive beregnet til at opfylde det maksimale lager. Hvis antal modifikatorer anvendes, kan maksimumlageret blive overtrådt. Vi anbefaler ikke, at du bruger intervallet sammen med maksimalt antal. Intervallet tilsidesættes sædvanligvis. Denne genbestillingsmetode bruges normalt med et genbestillingspunkt.|  
|**Ordre**|Ordreantallet vil blive beregnet til at opfylde hver enkelt behovshændelse, og behov-forsyningssættet forbliver sammenkædet indtil udførelse. Ingen planlægningsparametre overvejes.|  
|**Lot-for-Lot**|Antallet beregnes for at opfylde summen for det behov, der bliver forfaldent i intervallet.|  

## <a name="optimize-when-and-how-much-to-reorder" />Optimer, hvornår og hvor meget du skal genbestille

En planlægger kan finjustere planlægningsparametre for at begrænse ændringsforslag, akkumulere behov (dynamisk genbestillingsantal) eller for at undgå ubetydelige planlægningshandlinger. Følgende felter hjælper med at optimere, hvornår og hvor meget der skal genbestilles.  

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Ændringsperiode**|Dette felt bestemmer, om aktionsmeddelelsen skal omplanlægge en eksisterende ordre eller annullere den og oprette en ny ordre. Den eksisterende ordre bliver ændret i én ændringsperiode før den aktuelle forsyning og indtil én ændringsperiode efter den aktuelle forsyning.<br><br>**Bemærk!** Denne parameter fungerer kun med **Lot-for-Lot**-genbestillingsmetoden.|  
|**Akkumuleringsperiode for lot**|Dette felt bruges sammen med genbestillingsmetoden Lot-for-Lot, til at akkumulere flere forsyningsbehov i én forsyningsordre. Fra datoen for den første planlagte forsyning akkumulerer systemet alle forsyninger i den følgende akkumuleringsperiode for lot i én forsyning, der placeres på datoen for den første forsyning. Behov, som er uden for akkumuleringsperioden for lot, er ikke omfattet af denne forsyning.|  
|**Bufferperiode**|Dette felt bruges til at undgå mindre omlægning af eksisterende forsyningsordrer i fremtiden. Ændringer fra forsyningsdatoen til en bufferperiode fra forsyningsdatoen genererer ikke nogen aktionsmeddelelser.<br /><br /> Bufferperioden angiver en tidsperiode, hvor planlægningsprogrammet ikke skal foreslå at omplanlægge eksisterende forsyningsordrer fremad. Dette begrænser antallet af ubetydelige forsalg til ny planlægning for eksisterende forsyning til en senere dato, hvis ændringsdatoen er inden for bufferperioden.<br /><br /> Derfor vil et positivt delta mellem den foreslåede nye forsyningsdato og den oprindelige forsyningsdato altid være større end bufferperioden.|  

> [!NOTE]
> Med genbestillingsmetoden Lot-for-Lot skal værdien i feltet **Akkumuleringsperiode for lot** være lig med eller større end værdien i feltet **Bufferperiode**. I modsat fald reduceres bufferperioden under planlægningsrutinen, så den svarer til akkumuleringsperioden for lot.  

Tidspunktet for ændringsperiode, bufferperiode og akkumuleringsperiode for lot er baseret på en forsyningsdato. Intervallet er baseret på planlægningens startdato, som vist i følgende illustration.  

:::image type="content" source="media/supply_planning_5_time_bucket_elements.png" alt-text="Intervalelementer.":::

I nedenstående eksempler repræsenterer sorte pile eksisterende forsyning (op) og behov (ned). Rød, grøn og orange pil er planlægningsforslag.  

**Eksempel 1**: Den ændrede dato er uden for ændringsperioden, hvilket forårsager, at den eksisterende forsyning bliver annulleret. Der foreslås en ny forsyning til at dække behovet i akkumuleringsperioden for lot.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accumulation_period.png" alt-text="Ændringsperiode og akkumuleringsperioder for lot":::

**Eksempel 2**: Den ændrede dato er inden for ændringsperioden, hvilket forårsager, at den eksisterende forsyning skal omplanlægges. Der foreslås en ny forsyning til at dække behovet uden for akkumuleringsperioden for lot.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png" alt-text="Ændringsperiode, akkumuleringsperiode for lot og ændring":::

**Eksempel 3**: Der er et behov i bufferperioden, og forsyningsantallet i akkumuleringsperioden for lot svarer til forsyningsantallet. Næste behov er uafdækket, og der foreslås en ny forsyning.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accumulation_period.png" alt-text="Bufferperiode og akkumuleringsperiode for lot.":::

**Eksempel 4**: Der er et behov i bufferperioden, og forsyningen forbliver på samme dato. Men den aktuelle leveringsmængde dækker ikke behovet i akkumuleringsperioden for lot. Der foreslås en ændring i mængdehandlingen for den eksisterende forsyningsordre.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png" alt-text="Bufferperiode, akkumuleringsperiode for lot og rediger antal.":::

**Standardværdier:** Standardværdien for feltet **Interval** og de tre felter for genbestillingsperioden er tomme. For alle felter, undtagen feltet **Bufferperiode**, betyder det 0D (nul dage). Hvis feltet **Bufferperiode** er tomt, bruges den globale værdi i feltet **Standardbufferperiode** på siden **Produktionsopsætning**.  

## <a name="modify-the-supply-orders" />Ret forsyningsordrer

Når antallet af ordreforslaget er beregnet, kan en eller flere af ordremodifikatorerne justere den. Det maksimale ordreantal er f.eks. større end eller lig med det mindst tilladte ordreantal, som er større end eller lig med oprundingsfaktoren.  

Antallet reduceres, hvis det overskrider det maksimale ordreantal. Derefter forøges det, hvis det er under det mindst tilladte ordreantal. Endelig skal det rundes op, så det passer til en bestemt oprundingsfaktor. Eventuelle restmængder bruger de samme justeringer, indtil det samlede behov er blevet konverteret til ordreforslag.  

## <a name="delimit-the-item" />Afgræns varen

Feltet **Produktionsmetode** på **Varekortet** definerer, hvilke andre ordrer MRP beregningen foreslår.  

Hvis indstillingen **Fremstil-til-lager** bruges, vedrører ordrerne kun varen.  

Hvis indstillingen **Fremstil-til-ordre** bruges, vil planlægningssystemet analysere produktionsstyklisten for varen og oprette yderligere tilknyttede ordreforslag for disse elementer på lavere niveauer, der også er defineret som Fremstil-til-ordre. Dette fortsætter, så længe der er fremstil-til-ordre-varer i de faldende styklistestrukturer.

## <a name="use-low-level-codes-to-manage-derived-demand" />Brug laveste-niveau-koder til at administrere afledt behov

Brug laveste-niveau-koder for at føre det afledte behov for komponenter frem til de lavere niveauer i styklisten. Du kan få mere at vide om laveste-niveau-koder ved at gå til [Vareprioritet/laveste-niveau-kode](design-details-central-concepts-of-the-planning-system.md#item-priority--low-level-code).

Du kan tildele en laveste-niveau-kode til hver del i produktstrukturen eller til den niveaudelte stykliste. Det højeste niveau for montageelementer betegnes som niveau 0 – færdigvaren. Jo højere nummeret for laveste-niveau-kode er, desto lavere er varen i hierarkiet. Færdigvarer har f.eks. laveste-niveau-kode 0, og komponenter, som indgår i færdigvaren, har laveste-niveau-kode 1, 2, 3 osv. Resultatet er, at komponenter planlægges i henhold til behovet på alle højere niveauer. Når du beregner en plan, udfoldes styklisten i planlægningskladden, og bruttobehovet på niveau 0 overføres til de lavere planlægningsniveauer som bruttobehov for det næste niveau.

Brug til/fra-feltet **Dynamisk laveste-niveau-kode** på siden **Produktionsopsætning** for at angive, om der med det samme skal tildeles og beregnes laveste-niveau-koder for hver komponent i produktstrukturen. Hvis du har store mængder data, kan denne funktion have negativ indvirkning på programmets ydeevne, f.eks. under automatisk kostregulering. Bemærk, at det ikke er en funktion med tilbagevirkende kraft, så det er en god ide at overveje, om du vil bruge faciliteten, inden du går i gang.

Som et alternativ til automatisk beregning, som udføres dynamisk, hvis feltet et markeret, kan du køre **Beregn laveste-niveau-kode** fra menuen **Produktion** ved at klikke på **Produktdesign**, **Beregn laveste-niveau-kode**.

> [!IMPORTANT]
> Hvis du ikke markerer til/fra-feltet **Dynamisk laveste-niveau-kode**, skal du køre **Beregn laveste-niveau-kode**, før du beregner en forsyningsplan (kørslen **Beregn plan**).  

> [!NOTE]
> Selv hvis feltet **Dynamisk laveste-niveau-kode** er markeret, ændres laveste-niveau-koderne for komponentvarer ikke dynamisk, hvis en overordnet stykliste er slettet eller angivet til ikke-godkendt. Det kan medføre, at det er svært at tilføje nye varer i slutningen af produktstrukturen, da det kan overstige det maksimalt tilladte antal laveste-niveau-koder. Hvis du har omfattende produktstrukturer, der når grænsen for laveste-niveau-kode, anbefales det derfor, at du ofte kører **Beregn laveste-niveau-kode** for at vedligeholde strukturen.  

## <a name="see-also" />Se også

[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)  
[Designoplysninger: Afstemning mellem udbud og efterspørgsel](design-details-balancing-demand-and-supply.md)  
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
