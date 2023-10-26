---
title: Om beregning af standardomkostning
description: Et system til standardkostpriser bestemmer lagerkostprisen på basis af rimelige historiske eller forventede omkostninger.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.author: bholtorf
ms.date: 10/10/2023
---
# <a name="about-calculating-standard-cost"></a>Om beregning af standardomkostning

Mange produktionsvirksomheder vælger en værdiansættelse for standardkostpriser. Dette gælder også for virksomheder, der udfører let produktion som montage og kitting. Et system til standardkostpriser bestemmer lagerkostprisen på basis af nogle rimelige historiske eller forventede omkostninger. Undersøgelser af tidligere og fremtidige omkostningsdata kan derefter danne grundlag for standardkostpriser. Standardkostpriserne er fastfrosne, indtil der træffes en beslutning om, at de skal ændres. De faktiske omkostninger til at fremstille et produkt kan afvige fra de forventede standardomkostninger. Af hensyn til styringen sammenlignes den faktiske kostpris med standardkostprisen for en bestemt vare, og forskellene, eller *afvigelser*, identificeres og analyseres.  

Standardkostpriserne kan opretholdes for varer, der genopfyldes via indkøb, montage og produktion. For hver genbestillingsmetode kan standardkostpriserne bestå af følgende elementer.  

|Genbestillingssystem|Standardkostpriselementer|  
|--------------------------|----------------------------|  
|**Køb**|Direkte materialeomkostninger og faste materialeomkostninger efter behov.|  
|**Montage**|Direkte materialeomkostninger, direkte eller faste arbejdsomkostninger og faste omkostninger.|  
|**Prod.ordre**|Direkte materialeomkostninger, arbejdsomkostninger, underleverandøromkostninger og faste omkostninger.|  

## <a name="setting-up-standard-costs"></a>Oprette standardkostpriser

Da standardkostprisen for en fremstillet vare eller en montagevare kan bestå af flere kostelementer, herunder materialeomkostninger, kapacitetsomkostninger (arbejdskraft) og direkte og faste underleverandøromkostninger, skal der oprettes standardkostpriser for hvert af disse elementer.  

Opgaven for en fremstillingsvirksomhed, der bruger standardkostpriser, består af:  

- At anslå en standardkostpris for den færdig vare og at oprette den på varekortet.  
- At registrere og allokere de faktiske omkostninger til de vigtigste omkostningselementer og tage højde for afvigelser.  

Alle komponentomkostninger skal lægges sammen for at bestemme den direkte kostpris for en færdig vare. En samlet eller produceret vare kan omfatte underordnede samlinger, som også består af flere komponenter.  

Følgende vigtigste omkostningselementer udgør den samlede direkte omkostning for en færdig produktionsvare:  

- Materialekostpriser.  
- Kapacitetskostpris.  
- Underleverandøromkostninger for kun producerede varer.  

### <a name="material-costs"></a>Materialekostpriser

Materialekostpriser, der er forbundet med underordnede samlinger og indkøbte råvarer. Materialekostprisen kan bestå af direkte og indirekte kostelementer.  

- Direkte materialeomkostninger repræsenterer et faktureret beløb for købte råmaterialer eller omkostningen til fremstilling af en underordnet samling.  
- Indirekte materialeomkostninger, eller *faste omkostninger* kan være elementer som f.eks. lageromkostninger for den færdige vare, efter at den er fremstillet.  

Opsætningen af materialeomkostninger for købte varer, der påvirker direkte og indirekte omkostninger, afhænger af den kostmetode, der er valgt for den pågældende vare. Du kan oprette omkostningsoplysninger for hver kostmetode på varekortet. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).

Omkostningen til spild (kun produktion) er en anden faktor, du skal overveje, når du beregner den samlede materialeomkostning. Når en bestemt mængde råmateriale går til spilde under montage eller fremstilling af en vare, medfører det generelt en forøgelse af de komponenter, der skal bruges til fremstilling af varen. Dette medfører desuden en stigning i materialeomkostningerne for de komponenter, der bruges under fremstilling af den overordnede vare. Du opretter spildomkostninger for materialer på enten produktionsstyklisten eller produktionsruten.  

Materialeomkostningerne for en fremstillet vare kan repræsenteres på to måder, der svarer til følgende kostprisberegninger.  

|Kostprisberegningsgrundlag|Materialekostprisberegning|  
|----------------------------|-------------------------------|  
|Enkelt niveau|Produceret vare er lig med det samlede kostbeløb af alle varer, der er indkøbte eller underordnede samlinger, på denne vares produktionsstykliste.|  
|Akkumuleret niveau eller flere niveauer|Den fremstillede vare er summen af materialeomkostningerne for alle underordnede samlinger på varens stykliste og omkostningerne for alle købte varer på varens produktionsstykliste.|  

### <a name="capacity-costs"></a>Kapacitetsomkostninger

Kapacitetsomkostninger er omkostninger, der er knyttet til intern arbejdskraft og maskinomkostninger. Du skal angive disse omkostninger for hver ressource (i montagestyring) og arbejds- eller produktionscenter på ruten (i produktion). Som med materialer kan du identificere både direkte og indirekte elementer af kapacitetsomkostninger. Den direkte omkostning for et arbejdscenter kan f.eks. være den fastsatte produktionstakst for udførelse af en bestemt funktion. Den indirekte omkostning for et arbejdscenter kan repræsentere nogle generelle fremstillingsomkostninger, f.eks. lys, varme osv. Som med materialeomkostninger kan indirekte kapacitetsomkostninger udtrykkes som en indirekte omkostningsprocent eller en fast sats.  

Oprettelsen af kapacitetsomkostningerne for montagevarer består af følgende elementer:  

- Direkte og indirekte kostpris for ressourcen.  
- Type af fast eller direkte ressourceforbrug.  

Oprettelsen af kapacitetsomkostningerne for fremstillede varer består af følgende elementer:  

- Direkte og indirekte kostpris for produktions- eller arbejdscentret.  
- Oprettelse af tid og lotstørrelsen.  

Hvis du vil beregne standardkapacitetsomkostningerne, skal du etablere de standardtimesatser, der kræves for at foretage opgaver i maskin- og arbejdscentre. Den samlede tid til at færdiggøre en operation består som regel af tid til opstilling og kørsel samt vente- og flyttetid.  

Du opretter satserne for hver tidstype for hver maskine eller hvert arbejdscenter på en individuel rute.  

> [!NOTE]  
>  Mens timesatserne for kørsel gælder pr. fremstillet vare, gælder timesatserne for opstilling pr. lot. Derfor skal rutens opstillingstid for hver operation fordeles over lotstørrelsen. Du skal angive lotstørrelsen i det tilsvarende felt i oversigtspanelet **Genbestilling** på siden **Varekort**.  

Hvis du vil angive opstillingstiden på ruten af hensyn til planlægningen, men ikke vil medtage denne omkostning i standardkostprisberegningen, skal du fjerne markeringen i feltet **Kostpris inkl. opstilling** på siden **Produktionsopsætning**.  

På enkeltniveaubasis er det den arbejdsomkostning, der kræves til fremstilling af den færdige vare, og den angives på fremstillingsvarens rute. På akkumuleret niveau er dette den kapacitetsomkostning, der er angivet for hver enkelt fremstillet vare, der er medtaget på den overordnede vares stykliste.  

### <a name="subcontractor-costs"></a>Underleverandøromkostninger

Underleverandøromkostningerne er de omkostninger, der er knyttet til serviceydelser, der leveres af en virksomheds eksterne leverandører eller underleverandører. Ligesom for materiale- og kapacitetsomkostninger kan underleverandøromkostninger bestå af både direkte og indirekte omkostninger. Direkte underleverandøromkostninger repræsenterer det faktiske beløb for hver serviceenhed, der leveres. Faste underleverandøromkostninger kan f.eks. repræsentere fragtomkostninger og håndteringsomkostninger i forbindelse med en ordre til en underleverandør.  

Da underleverandøropgaver er en udliciteret kapacitet, skal du oprette omkostningerne for både direkte og indirekte underleverandørtjenester på det arbejdscenterkort, der repræsenterer underleverandøroperationen.  

## <a name="updating-standard-costs"></a>Opdatere standardkostpriser

Hvis du vil opdatere eller beregne standardkostprisen for montageelementer, skal du bruge funktionen fra varekortet.  

Processen med at opdatere eller beregne standardkostpriser består typisk af følgende opgaver:  

1.  Opdatering af omkostninger på komponent- og kapacitetsniveau. Du kan finde flere oplysninger i kørslerne **Foreslå kostpris (standard)** og **Foreslå kapacitetskostpris (standard)**.  
2.  Konsolidering og akkumulering af komponent- og kapacitetsomkostninger til beregning af den samlede montage eller de samlede fremstillingsomkostninger for varerne. Du kan finde flere oplysninger i [Sådan beregnes standardkostprisen for et montageelement](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  Implementering af de standardkostpriser, der angives, når du kører de tidligere kørsler. Standardkostpriserne træder ikke i kraft, før de er implementeret. Med **Implementer std.kostprisændringer**-kørslen, der opdaterer ændringerne i standardkostprisen for varer med ændringerne i tabellen Standardkostpriskladde.  
4.  Implementering af ændringer for at opdatere feltet **Kostpris** på varekortet og udførsel af lagerværdiregulering. Du kan finde flere oplysninger i [Regulere lagerbeholdningen](inventory-how-revalue-inventory.md).

## <a name="use-batch-jobs-to-update-standard-costs"></a>Bruge kørsler til at opdatere standardkostpriser
I følgende afsnit beskrives de kørsler, du kan bruge til at opdatere standardkostpriser.
### <a name="suggest-item-standard-cost"></a>Foreslå kostpris (standard)

 Opretter forslag til ændring af kostpriser og kostprisfordelinger af kostpris (standard) på varekortene. Når kørslen er afsluttet, kan du se resultatet i vinduet Standardkostpriskladde.

> [!NOTE]  
> Denne kørsel bruges kun til indkøbte varer. Hvis du vil opdatere en vare med en produktionsstykliste eller en montagestykliste, skal du først udfylde kladden med alle komponenterne og derefter udføre kørslen Akkum. standardkostpris.

Med denne kørsel oprettes der kun forslag. De foreslåede ændringer implementeres ikke. Hvis du er tilfreds med forslagene og vil implementere dem, dvs. opdatere dem på varekortene og indføje dem i Værdireguleringskladde, så skal du klikke på Implementer std.kostprisændringer i vinduet Standardkostpriskladde.
#### <a name="options"></a>Indstillinger

**Kostpris (standard)**: Angiv den justeringsfaktor, du vil bruge til at opdatere standardkostprisen. Du kan også vælge en afrundingsmetode for den nye standardkostpris. Du skal udfylde feltet med en decimal for den procentvise stigning, f.eks. 1.1.

**Indir. omkost.pct**: Angiv den justeringsfaktor, du vil bruge til at opdatere den indirekte omkostningsprocent. Du kan også vælge en afrundingsmetode for den nye indirekte omkostningsprocent. Du skal udfylde feltet med en decimal for den procentvise stigning, f.eks. 1.1.

**IPO-bidrag**: Angiv den justeringsfaktor, du vil bruge til at opdatere IPO-bidraget. Du kan også vælge en afrundingsmetode for det nye IPO-bidrag. Du skal udfylde feltet med en decimal for den procentvise stigning, f.eks. 1.1.

### <a name="suggest-workmach-ctr-std-cost"></a>Foreslå arb.ctr./prd.res.kostp

Opretter forslag til ændring af kostpriser og kostprisfordelinger af kostpris på arbejdscenter, produktionsressource eller ressourcekort. Når kørslen er afsluttet, kan du se resultatet i vinduet **Standardkostpriskladde**.

Med denne kørsel oprettes der kun forslag. De foreslåede ændringer implementeres ikke. Hvis du er tilfreds med forslagene og vil implementere dem, dvs. opdatere dem på arbejdscenteret/produktionsressource og ressourcekortene og indføje dem i Værdireguleringskladde, så skal du klikke på **Implementer std.kostprisændringer** i vinduet **Standardkostpriskladde**.

Når du har udført kørslen og ønsker at se, hvilken virkning den har på produktionen eller samleafdelinger, kan du udføre kørslen **Akkum. standardkostpris** for at opdatere kostpriserne (standard) på arbejdscentre, produktionsressourcer, montageressourcer, produktionsstyklister og montagestyklister.
#### <a name="options-1"></a>Indstillinger
**Kostpris (standard)**: Angiv den justeringsfaktor, du vil bruge til at opdatere standardkostprisen. Du kan også vælge en **afrundingsmetode** for den nye standardkostpris. Du skal udfylde feltet med en decimal for den procentvise stigning, f.eks. 1.1.

**Indir. omkost.pct**: Angiv den justeringsfaktor, du vil bruge til at opdatere den indirekte omkostningsprocent. Du kan også vælge en afrundingsmetode for den nye indirekte omkostningsprocent. Du skal udfylde feltet med en decimal for den procentvise stigning, f.eks. 1.1.

**IPO-bidrag**: Angiv den justeringsfaktor, du vil bruge til at opdatere IPO-bidraget. Du kan også vælge en afrundingsmetode for det nye IPO-bidrag. Du skal udfylde feltet med en decimal for den procentvise stigning, f.eks. 1.1.

### <a name="post-inventory-cost-to-gl"></a>Bogfør lagerregulering til Finans

 Registrerer ændringen i antal og værdi for lageret i vareposterne og værdiposterne, når du bogfører lagertransaktioner som f.eks. salgsleverancer eller købsmodtagelser.

Medmindre du har markeret afkrydsningsfeltet **Aut.lagerværdibogføring** i vinduet **Opsætning af lager**, registreres kostpriser ikke dynamisk i regnskabet, og vareforbrug beregnes ikke i forbindelse med et salg. Derfor skal du bogføre manuelt ved at udføre kørslen **Bogfør lagerregulering** for at opdatere regnskabet og eventuelt udskrive en rapport over de værdiposter, der er bogført.

Kørslen bruger værdiposterne som udgangspunkt. For at beregne værdien til bogføring bruger den differencen mellem feltet **Kostbeløb (faktisk)** og feltet **Bogført kostværdi** i værdiposterne. Hvis du har markeret afkrydsningsfeltet **Bogf. af forventet kostpris** i vinduet **Opsætning af lager**, posterer kørslen også forskellen mellem feltet **Kostbeløb (forventet)** og feltet **Bogført forv. kostpris (EV)** til melllemregningskonti i regnskabet.

> [!NOTE]
> Hvis du ikke har markeret afkrydsningsfeltet **Bogf. af forventet kostpris** i vinduet **Opsætning af Lager**, viser den sidste sektion i rapporten de værdiposter, der er sprunget over, fordi de repræsenterer forventede omkostninger.

> [!NOTE] 
> Hvis der opstår en fejl, som omfatter dimensioner eller opsætning af dimensioner, tilsidesætter batchjobbet fejlen og bogfører værdien i finansregnskabet med dimensionerne af værdiposten.

Hvis du vil sikre, at der ikke opstår fejl under en kørsel, kan du køre rapporten **Bogfør lagerregulering - Test** for at se alle de fejl, der kan opstå. Du kan derefter rette fejlene og udføre kørslen **Bogfør lagerregulering**, som derefter behandler alle poster.
 
> [!IMPORTANT]  
> Inden du bruger kørslen, skal du udføre kørslen **Juster kostpris - vareposter**. Dette sikrer, at de kostpriser, der bogføres i finansregnskabet, er opdateret, når du har udført kørslen.
#### <a name="options-2"></a>Indstillinger

|Indstilling  |Beskrivelse  |
|--------------|---------|
|**Bogføringsmetode**|Ved kørslen kan lagerværdien bogføres i finansregnskabet pr. varebogføringsgruppe eller pr. bogført post. Hvis du bogfører pr. post, får du en detaljeret specifikation af lagerets indflydelse på finansregnskabet, men du får også et stort antal finansposter. Hvis du bogfører pr. bogføringsgruppe, opretter kørslen en post i finansregnskabet pr. bogføringsdato pr. bogføringsgruppekombination. Det betyder, at der oprettes en finanspost for hver kombination af bogføringsdato, generel virksomhedsbogføringsgruppe, generel produktbogføringsgruppe, varebogføringsgruppe og lokationskode. Desuden opretter kørslen separate finansposter for omkostninger med forskellige fortegn.|
|**Bilagsnr.**|I dette felt kan du angive et bilagsnummer, hvis du har markeret indstillingen Pr. varebogføringsgruppe. Bilagsnummeret vil fremgå af de bogførte poster.|
|**Bogfør**|Markér dette felt, hvis batchjobbet skal bogføre til finanskontiene automatisk. Hvis du vælger ikke at bogføre lagerreguleringen, udskrives der kun en kontrolrapport, som viser de værdier, der kan bogføres i finansregnskabet, og rapporten indeholder teksten: **Kontroludskrift (er ikke bogført)**.|

### <a name="roll-up-standard-cost"></a>Akkum. standardkostpris

Akkumulerer standardkostpriser over samlede og fremstillede varer. Disse påvirkes af ændringen i standardkostprisen for komponenter, der foreslås af kørslen **Foreslå kostpris (standard)**. Desuden påvirkes de af ændringen i standardkostprisen for produktionskapacitets- og montageressourcer, der foreslås af kørslen **Foreslå arb.ctr./prd.res.kostp**.

Når du har udført en eller begge kørsler, og du foretager akkumuleringen, implementeres alle ændringerne af standardkostpriserne i kladden i de tilknyttede produktions- eller montagestyklister, og kostpriserne anvendes på alle styklisteniveauer.

> [!NOTE] 
> Med denne funktion akkumuleres standardkostprisen kun på varekortene, ikke på lagerkortene.

Med denne kørsel oprettes der kun forslag. De foreslåede ændringer implementeres ikke. Hvis du er tilfreds med forslagene og vil implementere dem, dvs. opdatere dem på varekortene og sætte dem ind i **værdireguleringskladden**, kan du udføre kørslen **Implementer standardkostprisændring**. Du har adgang til denne kørsel fra vinduet **Standardkostpriskladde**.
#### <a name="options-3"></a>Indstillinger

**Beregningsdato**: Angiv den dato, der gælder for den version af produktionsstyklisten, du vil foretage akkumuleringen for.
 
### <a name="implement-standard-cost-change"></a>Implementer standardkostprisændring

Opdaterer ændringerne i standardkostprisen i tabellen **Vare** med ændringerne i tabellen **Standardkostpriskladde**. Du kan oprette forslagene til standardkostprisændringer med kørslen **Foreslå kostpris (standard)** og/eller kørslen **Foreslå arb.ctr./prd.res.kostp**, og de kan også ændres. Indholdet i alle felterne i forslagene til standardkostprisændringer overføres. Når du implementerer forslag til standardkostprisændringer, kan du se dem på varekortet og/eller på arbejdscenter- og produktionsressourcekortene. Der oprettes også en værdireguleringskladde, som du bruger til at opdatere værdien af det eksisterende lager.
#### <a name="options-4"></a>Indstillinger

**Bogføringsdato**: Angiv den dato, hvor værdireguleringen skal finde sted.

**Dokumentnr.**: Angiv nummeret på værdireguleringskladdelinjerne. Hvis der er angivet en nummerserie på varekladdenavnet, følger dokumentnummeret de poster, der oprettes, når værdireguleringskladden bogføres. Ellers kan du indtaste et nummer manuelt.

**Varekladdetype**: Angiv navnet på værdireguleringskladden.

**Varekladdenavn**: Angiv navnet på den faktiske værdireguleringskladde

Vælg **OK** for at starte kørslen. Hvis du ikke vil starte kørslen nu, skal du vælge **Annuller** for at lukke vinduet.

## <a name="see-also"></a>Se også

[Designoplysninger: Beregningsmetoder](design-details-costing-methods.md)  
[Opdatere kostpris (standard)](finance-how-to-update-standard-costs.md)  
[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  
[Arbejde med montagestyklister](assembly-how-work-assembly-boms.md)  
[Oprette produktionsstyklister](production-how-to-create-production-boms.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
