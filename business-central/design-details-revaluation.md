---
title: Designoplysninger - Regulering
description: 'Du kan regulere lagerbeholdningen baseret på det værdigrundlag, der mest præcist afspejler værdien af lageret.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 07/07/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Designoplysninger: Regulering

Du kan regulere lagerbeholdningen baseret på det værdigrundlag, der mest præcist afspejler værdien af lageret. Du kan også tilbagedatere en værdiregulering, så omkostningerne for vareforbruget opdateres korrekt for varer, der allerede er solgt. Varer, der benytter kostmetoden Standard, der ikke er blevet fuldt faktureret, kan også revalueres.  

I [!INCLUDE[prod_short](includes/prod_short.md)] understøttes følgende fleksibilitet med hensyn til værdiregulering:  

- Antallet, der skal reguleres, kan være beregnet for en given dato, også tilbage i tiden.  
- For varer, der benytter kostmetoden Standard, medtages forventede omkostningsposter i reguleringen.  
- Lagerreduceringer, der påvirkes af værdiregulering, registreres.  

## Beregning af det antal, der kan reguleres

Antallet, der skal reguleres, er det resterende antal på lager, der er tilgængeligt for værdiregulering på en given dato. Antallet er den samlede værdi af vareposter, der er fuldt faktureret, og som du bogfører på eller før værdi reguleringsdatoen.  

> [!NOTE]  
>  Varer, der benytter kostmetoden Standard, behandles forskelligt ved beregning af den revaluerbare mængde pr. vare, lokation og variant. Antallet og værdien af vareposter, der ikke er fuldt faktureret, medtages i det antal, der skal reguleres.  

Når en regulering er blevet bogført, kan du bogføre en lagerforøgelse eller reducering med en bogføringsdato, der kommer før bogføringsdatoen for reguleringen. Dette antal påvirkes dog ikke af reguleringen. Med henblik på at afstemme lageret er det kun det oprindelige regulerbare antal, der tages i betragtning.  

Da regulering kan foretages på en hvilken som helst dato, skal der være konventioner for, hvornår en vare betragtes som en del af lageret fra et økonomisk synspunkt. Når varen f.eks. er på lager, og når varen er igangværende arbejde (VIA).  

### Eksempel  

I følgende eksempel illustreres, når en vareoverflytning for igangværende arbejde bliver en del af lageret. Eksemplet er baseret på produktion af en kæde med 150 links.  

![Lageret og værdiregulering for igangværende arbejde.](media/design_details_inventory_costing_10_revaluation_wip.png "Lageret og værdiregulering for igangværende arbejde")  

**1K**: Brugeren bogfører de købte led som modtaget. Følgende tabel viser de resulterende vareposter.  

|Bogføringsdato|Vare|Postens type|Antal|Løbenr.|  
|------------------|----------|----------------|--------------|---------------|  
|01-01-20|LINK|Køb|150|1|  

> [!NOTE]  
>  En vare, der benytter kostmetoden Standard, er nu tilgængelig for værdiregulering.  

**1V**: Brugeren bogfører de købte led som faktureret, og ledene bliver en del af lageret fra et økonomisk synspunkt. Følgende tabel viser de resulterende værdiposter.  

|Bogføringsdato|Postens type|Værdiansættelsesdato|Kostbeløb (faktisk)|Varepostløbenr.|Løbenr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Købspris|01-01-20|150,00|1|1|  

 **2K + 2V**: Brugeren bogfører de købte led som forbrugt til fremstillingen af jernkæden. Fra et økonomisk synspunkt bliver linkene en del af VIA-lagerbeholdningen.  Følgende tabel viser de resulterende vareposter.  

|Bogføringsdato|Vare|Postens type|Antal|Løbenr.|  
|------------------|----------|----------------|--------------|---------------|  
|02-01-20|LINK|Forbrug|-150|1|  

Følgende tabel viser den resulterende værdipost.  

|Bogføringsdato|Postens type|Værdiansættelsesdato|Kostbeløb (faktisk)|Varepostløbenr.|Løbenr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|02-01-20|Købspris|02-01-20|-150,00|2|2|  

Værdiansættelsesdatoen angives til datoen for forbrugsbogføring (01-02-20) som en almindelig lagerreduktion.  

**3Q**: Brugeren bogfører kæden som output, og produktionsordren afsluttes. Følgende tabel viser de resulterende vareposter.  

|Bogføringsdato|Vare|Postens type|Antal|Løbenummer|  
|------------------|----------|----------------|--------------|---------------|  
|02-15-20|KÆDE|Afgang|1|3|  

**3V**: Brugeren udfører kørslen **Juster kostpris - vareposter**, som bogfører kæden som faktureret for at angive, at alt materialeforbrug er fuldt faktureret. Fra et økonomisk synspunkt er linkene ikke længere en del af VIA-lagerbeholdningen, når afgangen er fuldt faktureret og reguleret. Følgende tabel viser de resulterende værdiposter.  

|Bogføringsdato|Postens type|Værdiansættelsesdato|Kostbeløb (faktisk)|Varepostløbenr.|Løbenr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Købspris|01-01-20|150,00|2|2|  
|02-01-20|Købspris|02-01-20|-150,00|2|2|  
|02-15-20|Købspris|02-15-20|150.00|3|3|  

## Forventet kostpris i værdiregulering

Antallet, der skal reguleres, beregnes som det samlede antal af fuldt fakturerede vareposter med en bogføringsdato, der er lig med eller tidligere end reguleringsdatoen. Det betyder, at når nogle varer er modtaget/leveret, men ikke faktureret, så kan deres lagerværdi ikke beregnes. Varer, der benytter kostmetoden Standard, er ikke begrænset i denne henseende.  

> [!NOTE]  
>  En anden type af forventede omkostninger, der kan reguleres, er lagerbeholdningen for det igangværende arbejde, inden for visse regler. Du kan finde flere oplysninger i [WIP-lagerregulering](design-details-revaluation.md#wip-inventory-revaluation).  

Ved beregning af det revaluable antal for varer ved brug af kostmetoden Standard medtages vareposter, der endnu ikke er fuldt faktureret i beregningen. Disse poster reguleres så, når du bogfører reguleringen. Når du fakturerer den regulerede post, oprettes der følgende værdiposter:  

- Den normale fakturerede værdipost med posttypen **Direkte omkostning**. Kostbeløbet for denne post er den direkte omkostning fra kildelinjen.  
- En værdipost med posttypen **Afvigelse**. Denne post registrerer forskellen mellem fakturerede omkostninger og den regulerede standardkostpris.  
- En værdipost med posttypen **Værdiregulering af**. Denne post registrerer tilbageførsel af værdireguleringen af de forventede omkostninger.

### Eksempel  

Følgende eksempel er baseret på produktionen af kæden i det forrige eksempel. Dette eksempel viser, hvordan de tre typer poster oprettes, baseret på følgende scenario:  

1.  Du bogfører købte links som modtaget med en kostpris på LV 2,00.  
2.  Du bogfører derefter en regulering af linkene med en ny kostpris på LV 3,00 og opdaterer standardkostprisen til LV 3,00.  
3.  Du bogfører det oprindelige køb af led som faktureret, så der oprettes følgende:  

    1.  En faktureret værdipost med posttypen **Direkte omkostning**.  
    2.  En værdipost med posttypen **Værdiregulering** til at registrere tilbageførsel af værdiregulering for de forventede omkostninger.  
    3.  En værdipost med posttypen Afvigelse, der registrerer forskellen mellem fakturerede omkostninger og de regulerede standardomkostninger.  

Den følgende tabel viser resultaterne.  

|Trin|Bogføringsdato|Postens type|Værdiansættelsesdato|Kostbeløb (forventet)|Kostbeløb (faktisk)|Varepostløbenr.|Løbenr.|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|01-15-20|Købspris|01-15-20|300,00|0.00|1|1|  
|2.|01-20-20|Regulering|01-20-20|150,00|0.00|1|2|  
|3.a.|01-15-20|Købspris|01-15-20|-300,00|0.00|1|3|  
|3.b.|01-15-20|Regulering|01-20-20|-150,00|0.00|1|4|  
|3.c.|01-15-20|Varians|01-15-20|0.00|450.00|1|5|  

## Bestemmelse af om en lagerreducering påvirkes af værdiregulering  

Datoen for bogføringen eller reguleringen bruges til at bestemme, om en lagerreduktion er berørt af en værdiregulering.  

Følgende tabel viser de kriterier, der bruges til en vare, der ikke bruger kostmetoden Gennemsnit.  

|Scenarie|Løbenummer|Timing|Påvirket af regulering|  
|--------------|---------------|------------|-----------------------------|  
|A|Tidligere end reguleringsløbenummeret.|Tidligere end bogføringsdatoen for reguleringen|Nej|  
|B|Tidligere end reguleringspostnummeret.|Lig med bogføringsdatoen for reguleringen|Nej|  
|L|Tidligere end reguleringspostnummeret.|Senere end bogføringsdatoen for reguleringen|Ja|  
|D|Senere end reguleringspostnummeret.|Tidligere end bogføringsdatoen for reguleringen|Ja|  
|E|Senere end reguleringspostnummeret.|Lig med bogføringsdatoen for reguleringen|Ja|  
|F|Senere end reguleringspostnummeret.|Senere end bogføringsdatoen for reguleringen|Ja|  

### Eksempel  

Følgende eksempel, som illustrerer værdiregulering af en vare, der bruger kostmetoden FIFO. Eksemplet bygger på følgende scenario:  

1.  Den 01-01-20 bogfører brugeren et køb på 6 enheder.  
2.  Den 02-01-20 bogfører du et salg på 1 enhed.  
3.  Den 03-01-20 bogfører du et salg på 1 enhed.  
4.  Den 04-01-20 bogfører du et salg på 1 enhed.  
5.  Den 01-03-20 beregner brugeren lagerværdien for varen og bogfører en værdiregulering af varens kostpris i LV 10,00 til LV 8,00.  
6.  Den 02-01-20 bogfører du et salg på 1 enhed.  
7.  Den 03-01-20 bogfører du et salg på 1 enhed.  
8.  Den 04-01-20 bogfører du et salg på 1 enhed.  
9. Kør batchjobbet **Juster kostpris - vareposter**.  

Følgende tabel viser de resulterende værdiposter.  

|Scenarie|Bogføringsdato|Postens type|Værdiansættelsesdato|Værdiansat antal|Kostbeløb (faktisk)|Varepostløbenr.|Løbenr.|  
|--------------|------------------|----------------|--------------------|---------------------|----------------------------|---------------------------|---------------|  
||01-01-20|Køb|01-01-20|6|60.00|1|1|  
||03-01-20|Regulering|03-01-20|4|-8,00|1|5|  
|A|02-01-20|Salg|02-01-20|-1|-10,00|2|2|  
|B|03-01-20|Salg|03-01-20|-1|-10,00|3|3|  
|L|04-01-20|Salg|04-01-20|-1|-10,00|4|4|  
||04-01-20|Salg|04-01-20|-1|2.00|4|9|  
|D|02-01-20|Salg|03-01-20|-1|-10,00|5|6|  
||02-01-20|Salg|03-01-20|-1|2.00|5|10|  
|E|03-01-20|Salg|03-01-20|-1|-10,00|6|7|  
||03-01-20|Salg|03-01-20|-1|2.00|6|11|  
|F|04-01-20|Salg|04-01-20|-1|-10,00|7|8|  
||04-01-20|Salg|04-01-20|-1|2.00|7|12|  

## Igangværende arbejde - Regulering af lagerværdi  

Revaluating igangværende arbejde i lager angiver, at du regulerer komponenter, der er registreret som igangværende arbejde-lager.  

Det er vigtigt at have konventioner, der styrer, hvornår en vare er igangværende arbejde-lagervare fra et økonomisk synspunkt. I [!INCLUDE[prod_short](includes/prod_short.md)] findes følgende konventioner:  

- En købt komponent bliver en del af lageret for råmaterialer fra det tidspunkt, hvor et køb bogføres som faktureret.  
- En købt/delmonteret komponent bliver en del af lagerbeholdningen for det igangværende arbejde fra det tidspunkt, hvor forbruget bogføres i forbindelse med en produktionsordre.  
- En købt/delmonteret komponent forbliver en del af lagerbeholdningen for det igangværende arbejde indtil det tidspunkt, hvor en produktionsordre (en fremstillet vare) faktureres.  

Den måde, hvorpå værdiansættelsesdatoen for værdiposten af forbrug angives, følger de samme regler som for ikke-igangværende arbejde-lagerbeholdningen. Du kan lære mere i [Bestemmelse af om en lagerreducering påvirkes af værdiregulering](#determine-whether-revaluation-affects-an-inventory-decrease).  

Du kan revaluere igangværende arbejde-lageret under følgende betingelser:

- Værdireguleringsdatoen ligger før bogføringsdatoerne for de tilsvarende vareposter af typen forbrug.
- Du har ikke faktureret produktionsordren.  

> [!CAUTION]  
> Rapporten **Lagerværdi - igangværende arb.** viser værdien af bogførte produktionsordreposter og kan derfor være lidt forvirrende for igangværende arbejders varer, der er blevet reguleret.  

## Revaluate varer, der har kostmetoden gennemsnit

Du kan kun revaluate varer, der bruger kostmetoden gennemsnit, hvis **Beregn pr.** er *vare*.

Du kan kun foretage værdiregulering ved slutningen af den periode, der er valgt i feltet **gennemsnitlig omkostningsperiode** på **lageropsætningssiden**.

Værdiregulering påvirker ikke negative transaktioner i den aktuelle måned, hvilket vil sige, at fuldstændig udlignede indgående poster ikke medtages.

### Eksempel

Dette eksempel viser, hvad der sker, når du beregner lagerværdien på siden **vareværdireguleringskladde**. På siden **Lageropsætning** vælges **vare** i feltet **Beregn. type for gnsn. kostpris** og derefter vælges **måned** i feltet **gennemsnitlig omkostningsperiode**.

Følgende tabel indeholder de vareposter, som prøveeksemplet er baseret på, ITEM1.

|Bogføringsdato|Vareposttype|Antal|Kostbeløb (faktisk)|Løbenummer|
|----|----|----|----|----|
25-04-23|Køb|5|5.00|1
26-04-23|Køb|3|3.00|2
27-04-23|Salg|-5|-5,00|3
28-04-23|Salg|-1|-1,00|4
13-05-23|Køb|2|20.00|5
17-06-23|Salg|-6|-22,00|6

I følgende tabel vises resultatet af kørselsrapporten **Beregn lagerværdi** med forskellige tilgangsdatoer.

|Bogføringsdato|Antal|Kommentar|
|---|---|-------------|
30-04-23|2|Inkluderer kun Restantal fra post 2. Post 1 er helt udlignet før bogføringsdatoen, og post 5 er efter bogføringsdato.
31-05-23|4|Inkluderer restmængder fra post 2 og 13.
30-06-23|0|Restantal på bogføringsdatoen er ikke angivet.

Resultatet af følgende poster vil være 0, uanset bogføringsdatoen.

|Bogføringsdato|Vareposttype|Antal|Kostbeløb (faktisk)|Løbenummer|
|----|----|----|----|----|
13-05-23|Køb|5|5.00|1
26-04-23|Salg|-5|5.00|2

## Se også  

[Designoplysninger: Lagerberegning](design-details-inventory-costing.md)   
[Designoplysninger: Kostmetoder](design-details-costing-methods.md)   
[Designdetaljer: Lagervurdering](design-details-inventory-valuation.md)
[Administration af lageromkostninger](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
