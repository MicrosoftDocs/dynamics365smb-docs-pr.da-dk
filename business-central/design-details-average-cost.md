---
title: Designoplysninger - Gennemsnitlig kostpris
description: Den gennemsnitlige kostpris for en vare beregnes med et periodisk vejet gennemsnit.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '8645,'
ms.date: 06/06/2023
ms.author: bholtorf
---
# <a name="design-details-average-cost" />Designoplysninger: Gennemsnitlig omkostning

Den gennemsnitlige kostpris for en vare beregnes med et periodisk vejet gennemsnit. Gennemsnittet er baseret på den gennemsnitlige omkostningsperiode, der er konfigureret i [!INCLUDE[prod_short](includes/prod_short.md)].  

Værdiansættelsesdatoen angives automatisk.  

## <a name="setting-up-average-cost-calculation" />Opsætning af beregning af gennemsnitsomkostninger

I følgende tabel beskrives de to felter på siden **Opsætning af Lager**, der skal angives for at aktivere beregningen af gennemsnitlig kostpris.  

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Gennemsnitlig omkostningsperiode**|Angiver, hvilken periode den gennemsnitlige kostpris beregnes i. Der findes følgende indstillinger:<br /><br /> - **DAG**<br />- **Uge**<br />- **Måned**<br />- **Regnskabsperiode**<br /><br /> Reduceringer i lageret, der er bogført i den gennemsnitlige omkostningsperiode, modtager den gennemsnitlige kostpris, der er beregnet for den pågældende periode.|  
|**Beregn.type for gnsn. kostpris**|Angiver, hvordan den gennemsnitlige omkostning beregnes. Der findes følgende indstillinger:<br /><br /> - **Vare**<br />- **Vare, variant og lokation**<br /> Med denne indstilling beregnes gennemsnitsomkostningen for hver vare, for hver lokation og for hver variant af varen. Det betyder, at den pågældende vares gennemsnitlige kostpris afhænger af, hvor den opbevares, og hvilken variant af varen du har valgt, f.eks. farve.|  

> [!NOTE]  
> Du kan kun bruge én gennemsnitlig omkostningsperiode og én beregningstype for gennemsnitlig kostpris i et regnskabsår.  
>
> Siden **Regnskabsperioder** viser, hvilken gennemsnitlig omkostningsperiode og hvilken beregningstypen for gennemsnitskostprisen er gældende i den pågældende periode for hver regnskabsperiode.  

## <a name="calculating-average-cost" />Beregning af gennemsnitlig kostpris

 Når du bogfører en transaktion for en vare, der bruger kostmetoden Gennemsnit, oprettes en post i tabellen **Indf.st., regl. gnsn. kostpr.**. Denne post indeholder transaktionens varenummer, variantkode og lokationskode. Posten indeholder også feltet **Værdiansættelsesdato**, som angiver den sidste dato i den gennemsnitlige omkostningsperiode, hvor transaktionen blev bogført.  

> [!NOTE]  
> Dette felt må ikke forveksles med feltet **Værdiansættelsesdato** i tabellen **Værdipost**, som viser den dato, hvor værdien træder i kraft, og bruges til at bestemme den gennemsnitlige omkostningsperiode, som værdiposten tilhører.  

 Den gennemsnitlige kostpris for en postering beregnes, når varens kostpris er reguleret. Du kan finde flere oplysninger i [Designoplysninger: Omkostningsregulering](design-details-cost-adjustment.md). En omkostningsregulering benytter posterne i tabellen **Indf.st., regl. gnsn. kostpr.** til at identificere de varer (eller varer, lokationer og varianter), den gennemsnitlige kostpris skal beregnes for. For hver post, hvor kostprisen endnu ikke er blevet reguleret, bruger kostregulering følgende for at bestemme den gennemsnitlige kostpris:  

- Bestemmer varens kostpris i starten af den gennemsnitlige omkostningsperiode.  
- Tilføjer summen af indgående omkostninger, som blev bogført under den gennemsnitlige omkostningsperiode. Disse omfatter køb, salgsreturvarer, opreguleringer og produktions- og montageafgange.  
- Fratrækker summen af kostprisen for alle udgående transaktioner, der blev fast udlignet med modtagelser i den gennemsnitlige omkostningsperiode. Disse omfatter sædvanligvis købsreturvarer og negative afgange.  
- Deler det samlede lagerantal pr. ultimo i den gennemsnitlige omkostningsperiode. Udelukker lagerreduktioner, der værdiansættes.  

 Den beregnede gennemsnitlige kostpris udligner derefter lagerreduktionen for varen (eller vare, lokation og variant) med bogføringsdatoer inden for den gennemsnitlige omkostningsperiode. Hvis der er nogen lagerforøgelser, som blev fast udlignet til lagerreduceringer i den gennemsnitlige omkostningsperiode, videresender [!INCLUDE [prod_short](includes/prod_short.md)] den beregnede gennemsnitlige kostpris fra forøgelsen til reduceringen.  

### <a name="example-average-cost-period--day" />Eksempel: Gennemsnitlig omkostningsperiode = dag

Følgende eksempler viser effekten af beregning af den gennemsnitlige kostpris ud fra en gennemsnitlig omkostningsperiode på én dag. Feltet **Beregn.type for gnsn. kostpris** på siden **Opsætning af Lager** er angivet til **Vare**.  

Følgende tabel viser vareposter for eksemplet med den gennemsnitlige omkostningsvare, VARE1, før kørslen **Juster kostpris - vareposter** er udført.  

| **Bogføringsdato** | **Vareposttype** | **Antal** | **Kostbeløb (faktisk)** | **Løbenummer** |
|--|--|--|--|--|
| 01-01-23 |   Køb | 1 | 20.00 | 1 |
| 01-01-23 |   Køb | 1 | 40.00 | 2 |
| 01-01-23 |   Salg | -1 | -20,00 | 3 |
| 02-01-23 |   Salg | -1 | -40,00 | 4 |
| 02-02-23 |   Køb | 1 | 100.00 | 5 |
| 02-03-23 |   Salg | -1 | -100,00 | 6 |

> [!NOTE]  
> Da omkostningsreguleringer ikke er sket endnu, falder værdierne i feltet **Kostbeløb (faktisk)** for lagerbeholdningen svarende til de lagerforøgelser, de er anvendt til.  

 I følgende tabel vises posterne i tabellen **Indf.sted, regl. gnsn. kostpr.**, der gælder for de værdiposter, der stammer fra vareposterne i ovenstående tabel.  

| **Varenr.** | **Variantkode** | **Lokationskode** | **Værdiansættelsesdato** | **Kostværdien er reguleret** |
|--|--|--|--|--|
| VARE1 |  | BLÅ | 01-01-23 |   Nr. |
| VARE1 |  | BLÅ | 02-01-23 |   Nr. |
| VARE1 |  | BLÅ | 02-02-23 |   Nr. |
| VARE1 |  | BLÅ | 02-03-23 |   Nr. |

 Følgende tabel viser de samme vareposter, efter at kørslen **Juster kostpris - vareposter** er udført. Den gennemsnitlige kostpris pr. dag beregnes og anvendes til lagerreduktionen.  

| **Bogføringsdato** | **Vareposttype** | **Antal** | **Kostbeløb (faktisk)** | **Løbenummer** |
|--|--|--|--|--|--|
| 01-01-23 |   Køb | 1 | 20.00 | 1 |
| 01-01-23 |   Køb | 1 | 40.00 | 2 |
| 01-01-23 |   Salg | -1 | -30,00 | 3 |
| 02-01-23 |   Salg | -1 | -30,00 | 4 |
| 02-02-23 |   Køb | 1 | 100.00 | 5 |
| 02-03-23 |   Salg | -1 | -100,00 | 6 |

### <a name="example-average-cost-period--month" />Eksempel: Gennemsnitlig omkostningsperiode = måned

 Følgende eksempel viser effekten af beregning af den gennemsnitlige kostpris ud fra en gennemsnitlig omkostningsperiode på én måned. Feltet **Beregn.type for gnsn. kostpris** på siden **Opsætning af Lager** er indstillet til **Vare**.  

 Hvis den gennemsnitlige omkostningsperiode er en måned, opretter [!INCLUDE [prod_short](includes/prod_short.md)] kun én post for hver kombination af varenummer, variantkode, lokationskode og værdiansættelsesdato.  

 Følgende tabel viser vareposter for eksemplet med den gennemsnitlige omkostningsvare, VARE1, før kørslen **Juster kostpris - vareposter** er udført.  

| **Bogføringsdato** | **Vareposttype** | **Antal** | **Kostbeløb (faktisk)** | **Løbenummer** |
|--|--|--|--|--|
| 01-01-23 |   Køb | 1 | 20.00 | 1 |
| 01-01-23 |   Køb | 1 | 40.00 | 2 |
| 01-01-23 |   Salg | -1 | -20,00 | 3 |
| 02-01-23 |   Salg | -1 | -40,00 | 4 |
| 02-02-23 |   Køb | 1 | 100.00 | 5 |
| 02-03-23 |   Salg | -1 | -100,00 | 6 |

> [!NOTE]  
> Da omkostningsreguleringer ikke er sket endnu, falder værdierne i feltet **Kostbeløb (faktisk)** for lagerbeholdningen svarende til de lagerforøgelser, de er anvendt til.  

I følgende tabel vises posterne i tabellen **Indf.sted, regl. gnsn. kostpr.**, der gælder for de værdiposter, der stammer fra vareposterne i ovenstående tabel.  

| **Varenr.** | **Variantkode** | **Lokationskode** | **Værdiansættelsesdato** | **Kostværdien er reguleret** |
|--|--|--|--|--|
| VARE1 |  | BLÅ | 01-31-23 |   Nr. |
| VARE1 |  | BLÅ | 02-28-23 |   Nr. |

> [!NOTE]  
> Værdiansættelsesdatoen angives til den sidste dag i den gennemsnitlige omkostningsperiode, som i dette tilfælde er den sidste dag i måneden.  

Følgende tabel viser de samme vareposter, efter at kørslen **Juster kostpris - vareposter** er udført. Den gennemsnitlige kostpris pr. måned beregnes og anvendes til lagerreduktionen.  

|**Bogføringsdato** | **Vareposttype** | **Antal** | **Kostbeløb (faktisk)** | **Løbenummer** |
|--|--|--|--|--|
| 01-01-23 | Køb | 1 | 20.00 | 1 |
| 01-01-23 | Køb | 1 | 40.00 | 2 |
| 01-01-23 | Salg | -1 | -30,00 | 3 |
| 02-01-23 | Salg | -1 | -65,00 | 4 |
| 02-02-23 | Køb | 1 | 100.00 | 5 |
| 02-03-23 | Salg | -1 | -65,00 | 6 |

Den gennemsnitlige kostpris for løbenummer 3 beregnes i den gennemsnitlige omkostningsperiode for januar. Den gennemsnitlige kostpris for løbenummer 4 og 6 beregnes i den gennemsnitlige omkostningsperiode for februar.  

For at få den gennemsnitlige kostpris for februar lægger [!INCLUDE [prod_short](includes/prod_short.md)] den gennemsnitlige kostpris for varen, der er modtaget på lageret (100,00) til den gennemsnitlige kostpris i begyndelsen af perioden (30,00). Summen (130,00) divideres derefter med det samlede antal på lagerbeholdningen (2). Denne beregning giver varens gennemsnitlige kostpris i perioden pr. februar (65,00). Den gennemsnitlige kostpris anvendes derefter til lagerreduktionerne i perioden (post 4 og 6).  

## <a name="setting-the-valuation-date" />Angivelse af værdiansættelsesdatoen

 Feltet **Værdiansættelsesdato** i tabellen **Værdipost** bruges til at bestemme, hvilken gennemsnitlige omkostningsperiode en lagerreduktionspost tilhører. Denne indstilling gælder også for igangværende lagerarbejde (WIP).  

 Følgende tabel viser de kriterier, der bruges til at angive værdiansættelsesdatoen.  

| Scenarie | Bogføringsdato | Værdiansat antal | Værdiregulering | Værdiansættelsesdato |
|--|--|--|--|--|
| 1 |  | Positiv | Nej | Bogføringsdato for varepost |
| 2 | Senere end den seneste værdiansættelsesdato for anvendte værdiposter | Negativ | Nej | Bogføringsdato for varepost |
| 3 | Tidligere end den seneste værdiansættelsesdato for anvendte værdiposter | Positiv | Nej | Seneste værdiansættelsesdato for anvendte værdiposter |
| 4 |  | Negativ | Ja | Bogføringsdato for værdireguleringspost |

### <a name="example" />Eksempel

Følgende tabel med værdiposter illustrerer de forskellige scenarier.  

| Scenarie | Bogføringsdato | Vareposttype | Værdiansættelsesdato | Værdiansat antal | Kostbeløb (faktisk) | Varepostløbenr. | Løbenummer |
|--|--|--|--|--|--|--|--|
| 1 | 01-01-20 | Køb | 01-01-20 | 2 | 20.00 | 1 | 1 |
| 2 | 01-15-20 | (Varegebyr) | 01-01-20 | 2 | 8.00 | 1 | 2 |
| 3 | 02-01-20 | Salg | 02-01-20 | -1 | -14,00 | 2 | 3 |
| 4 | 03-01-20 | (Regulering) | 03-01-20 | 1 | -,4,00 | 1 | 4 |
| 5 | 02-01-20 | Salg | 03-01-20 | -1 | -10,00 | 3 | 5 |

> [!NOTE]  
> I post nummer 5 i den foregående tabel har som brugeren angivet en salgsordre med en bogføringsdato (02-01-20), der kommer før den seneste værdiansættelsesdato af anvendte værdiposter (03-01-20). Hvis den tilsvarende værdi i feltet **Kostbeløb (faktisk)** for denne dato 010220 blev brugt til denne post, ville den være 14,00. Dette vil give en situation, hvor antallet på lager er nul, men lagerværdien er -4,00.  
>
> For at undgå en sådan antal-værdi-uoverensstemmelse, angives værdiansættelsesdatoen til at være lig med den seneste værdiansættelsesdato for de anvendte værdiposter (01-03-20). Værdien i feltet **Kostbeløb (faktisk)** bliver 10,00 (efter værdiregulering), hvilket betyder, at antallet på lager er nul, og lagerværdien er også nul.  

> [!CAUTION]  
> Da rapporten **Lagerværdi** er baseret på bogføringsdato, vil rapporten afspejle en hvilken som helst uoverensstemmelse mellem antal-værdi i scenarier som i eksemplet ovenfor. Du kan finde flere oplysninger i [Designoplysninger: Lagerværdi](design-details-inventory-valuation.md).  

Hvis antallet på lager er mindre end nul efter bogføring af en reducering i lagerbeholdningen, indstilles værdiansættelsesdatoen først til bogføringsdatoen for lagerreduceringen. Du kan ændre denne dato, når lagerforøgelsen aktiveres, i henhold til de regler, der er beskrevet i noten tidligere i dette afsnit.  

## <a name="recalculating-average-cost" />Genberegning af gennemsnitlig kostpris

Værdiansættelse af lagerreduktioner som et vejet gennemsnit er ligetil i flere forskellige scenarier:

- Køb faktureres altid før salg.
- Bogføringer tilbagedateres aldrig.
- Du har aldrig lavet fejl.

Virkeligheden er dog anderledes.  

Som vist i eksemplerne i denne artikel defineres værdiansættelsesdatoen som den dato, hvorfra værdiposten medtages i den gennemsnitlige beregning af kostprisen. Denne indstilling gør det muligt at udføre flere ting for varer med den gennemsnitlige Kostmetode:  

- Faktura salget af en vare, inden købet af varen er blevet faktureret.  
- Tilbagedatering af en bogføring.  
- Gendanne en forkert postering.  

> [!NOTE]  
> En anden grund til denne fleksibilitet er fast udligning. Du kan finde flere oplysninger om fast udligning i [Designoplysninger: Vareudligning](design-details-item-application.md).  

På grund af denne fleksibilitet kan det være nødvendigt at genberegne den gennemsnitlige kostpris, efter bogføring. Hvis du f.eks. bogfører en lagerforøgelse eller -reducering med en værdiansættelsesdato, der kommer før en eller flere lagerreduceringer. Genberegning af den gennemsnitlige kostpris sker automatisk, når du udfører kørslen **Juster kostpris - vareposter** manuelt eller automatisk.  

Du kan ændre grundlaget for lagerværdi inden for en regnskabsperiode ved at ændre felterne **Gennemsnitlig omkostningsperiode** og **Beregn.type for gnsn. kostpris**. Det anbefales dog, at du er forsigtig og får hjælp hos din revisor.  

### <a name="example-of-recalculated-average-cost" />Eksempel på genberegnet gennemsnitlig kostpris

Dette eksempel viser, hvordan [!INCLUDE [prod_short](includes/prod_short.md)] genberegner den gennemsnitlige kostpris, når du bogfører på en dato, der ligger før en lagerreduktion. Eksemplet er baseret på den gennemsnitlige omkostningsperiode **Dag**.  

Følgende tabel viser de værdiposter, der findes for varen, før bogføringen introduceres.  

| Værdiansættelsesdato | Antal | Kostbeløb (faktisk) | Løbenummer |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 02-15-20 | -1 | -15,00 | 3 |
| 02-16-20 | -1 | -15,00 | 4 |

Brugeren bogfører en lagerforøgelse (løbenummer 5) med en værdiansættelsesdato (01-03-20), før en lagerreduktion. Med henblik på at afstemme lageret skal den gennemsnitlige kostpris genberegnes og reguleres til 17,00.  

Følgende tabel viser de værdiposter, der findes for varen, når løbenummer 5 introduceres.  

| Værdiansættelsesdato | Antal | Kostbeløb (faktisk) | Løbenummer |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 01-03-20 | 1 | 21.00 | 5 |
| 02-15-20 | -1 | -17,00 | 3 |
| 02-16-20 | -1 | -17,00 | 4 |

## <a name="see-also" />Se også

[Designoplysninger: Lagerberegning](design-details-inventory-costing.md)  
[Designoplysninger: Beregningsmetoder](design-details-costing-methods.md)  
[Designoplysninger: Beregningsregulering](design-details-cost-adjustment.md)  
[Designoplysninger: Vareudligning](design-details-item-application.md)  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ordliste med termer i Dynamics 365 business processes](/dynamics365/guidance/business-processes/glossary)  
[Definere oversigt over produkt-og serviceomkostninger](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
