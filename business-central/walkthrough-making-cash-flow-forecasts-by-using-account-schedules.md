---
title: Foretage Likviditetsforecasts ved hjælp af regnskabsrapporter
description: 'Denne gennemgang beskriver, hvordan du kan bruge kontoskemaer til at foretage likviditetsforecasts i Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/18/2022
ms.author: bholtorf
---
# <a name="walkthrough-making-cash-flow-forecasts-using-financial-reports"></a>Gennemgang: Udarbejd likviditetsforecast ved hjælp af finansrapporter

Denne gennemgang beskriver, hvordan du kan bruge kontoskemaer til at foretage likviditetsforecasts i Business Central. Finansrapporter udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti. I kontoskemaerne kan du oprette subtotaler for likviditetsindbetalinger og -udbetalinger. Disse subtotaler kan medtages i nye totaler, der kan bruges i forbindelse med udarbejdelse af likviditetsforecasts.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang

Denne gennemgang beskriver følgende opgaver:  

- Opsætning af et nyt finansrapportnavn.  
- Oprette finansrapportlinjer.  
- Opsætning af et nyt kolonneformat.  
- Tildele en kolonnedefinition til en finansrapport.  
- Visning og udskrift af likviditetsforecastet.  

### <a name="prerequisites"></a>Forudsætninger

For at gennemføre denne gennemgang skal du:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Likviditetskladde med registrerede linjer  

## <a name="roles"></a>Roller

Denne gennemgang viser de opgaver, der udføres af følgende brugerrolle:  

- Controller  

## <a name="story"></a>Historie

Ken er controller hos CRONUS, der udarbejder månedlige likviditetsforecasts. Ken medtager økonomi, salg, køb og anlæg i budgettet, og derefter præsenterer han det for Økonomichefen Sara med henblik på brancheindsigt.  

## <a name="setting-up-a-new-financial-report-name"></a>Opsætning af et nyt finansrapportnavn

Finansrapportnavnet er det navn, som du giver det likviditetsforecast, der indeholder en række definerede linjer og en kolonnedefinition.  

### <a name="set-up-a-new-financial-report-name"></a>Opsætning af et nyt finansrapportnavn

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansrapporter**, og vælg derefter det relaterede link.  
2. På siden **Finansrapporter** skal du vælge **Ny** for at oprette et nyt navn til Finansrapport for likviditet.  
3. I feltet **Navn** skal du skrive **Forecast**.  
4. I feltet **Beskrivelse** skal du angive **Pengestrømsprognose**.  
5. Lad felterne **rækkedefinition** og **kolonnedefinition** være tomme.

## <a name="setting-up-row-definition-lines"></a>Opsætte rækkedefinitionslinjer

Når der er oprettet et økonomisk rapportnavn, definerer Ken hver linje i den finansielle likviditetsrapport. Ken definerer linjer, der kan vises i rapporter, foruden de linjer, der kun er til beregning.  

### <a name="set-up-row-definition-lines"></a>Opsætte rækkedefinitionslinjer

1. På siden **Finansrapporter** skal du vælge den nye **Prognose**-finansrapport, du har oprettet, og vælg **Rediger rækkedefinition**.  
2. På siden **Rækkedefinition** skal du angive hver linje som vist i følgende tabel.  

    > [!TIP]  
    > Ved hjælp af funktionen **Indsæt CF-konti** kan du hurtigt markere pengestrømskonti fra diagrammet for pengestrømkonti og kopiere dem til linjer i kontoskemaet.  

    | Rubriknr. | Beskrivelse              | Sammentællingstype            | Sammentælling | Rækketype   | Beløbstype | Vis |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Tilgodehavender              | Konti for pengestrømspost | 10       |Nettoændring | Nettobeløb  | Ja  |
    | R10     | Åbne salgsordrer        | Konti for pengestrømspost | 20       |Nettoændring | Nettobeløb  | Ja  |
    | R10     | Udlejning                  | Konti for pengestrømspost | 30       |Bevægelse | Nettobeløb  | Ja  |
    | R10     | Finansielle anlæg         | Konti for pengestrømspost | 40       |Bevægelse | Nettobeløb  | Ja  |
    | R10     | Afhændelse af faste anlægsaktiver    | Konti for pengestrømspost | 50       |Bevægelse | Nettobeløb  | Ja  |
    | R10     | Private investeringer      | Konti for pengestrømspost | 60       |Bevægelse | Nettobeløb  | Ja  |
    | R10     | Diverse kladder   | Konti for pengestrømspost | 70       |Bevægelse | Nettobeløb  | Ja  |
    | R10     | Åbne serviceordrer      | Konti for pengestrømspost | 80       |Nettoændring | Nettobeløb  | Ja  |
    | R20     | Samlede indbetalinger      | Formel                  | R10      |Nettoændring | Nettobeløb  | Ja  |
    | R30     | Gæld                 | Konti for pengestrømspost | 1010     |Bevægelse | Nettobeløb  | Ja  |
    | R30     | Åbne købsordrer     | Konti for pengestrømspost | 1020     |Bevægelse | Nettobeløb  | Ja  |
    | R30     | Personaleomkostninger          | Konti for pengestrømspost | 1030     |Bevægelse | Nettobeløb  | Ja  |
    | R30     | Driftsomkostninger            | Konti for pengestrømspost | 1040     |Bevægelse | Nettobeløb  | Ja  |
    | R30     | Finansomkostninger            | Konti for pengestrømspost | 1050     |Bevægelse | Nettobeløb  | Ja  |
    | R30     | Investeringer              | Konti for pengestrømspost | 1070     |Bevægelse | Nettobeløb  | Ja  |
    | R30     | Privatforbrug     | Konti for pengestrømspost | 1090     |Bevægelse | Nettobeløb  | Ja  |
    | R30     | Forfalden MOMS                  | Konti for pengestrømspost | 1100     |Bevægelse | Nettobeløb  | Ja  |
    | R30     | Andre udgifter           | Konti for pengestrømspost | 1110     |Bevægelse | Nettobeløb  | Ja  |
    | R40     | Kontante udbetalinger i alt | Formel                  | R30      |Bevægelse | Nettobeløb  | Ja  |
    | R50     | Overskud                  | Formel                  | R20+R40  |Nettoændring | Nettobeløb  | Ja  |
    | R60     | Likvide midler          | Konti for pengestrømspost | 2100     |Nettoændring | Nettobeløb  | Ja  |
    | R70     | Likviditet i alt          | Formel                  | R50+R60  |Nettoændring | Nettobeløb  | Ja  |

    > [!NOTE]
    > Rækkenummer R10 bruges til at registrere kontototaler for tilgodehavender. Rækkenummer R20 bruges til at beregne summen af alle indbetalinger. Rækkenummer R30 bruges til at registrere kontototaler for skyldige beløb. Rækkenummer R40 bruges til at beregne summen af alle kontante udbetalinger. Rækkenummer R50 bruges til at registrere summen af alle kontante overskud. Rækkenummer R60 bruges til at registrere de likvide midler. Rækkenummer R70 bruges til at beregne den budgetterede pengestrøm.

## <a name="setting-up-a-new-column-definition"></a>Opsætning af et nyt kolonneformat

Før Ken kan udskrive likviditetsforecastet, skal han oprette kolonneformat for de numeriske oplysninger. I kolonnerne skal Ken definere de oplysninger, han ønsker at bruge fra linjerne.

- Den første kolonne er nummeret *C10* med titlen **Beløb**, og den indeholder bevægelsen.  
- Den anden kolonne er nummereret *C20* med titlen **Saldo til dato** og indeholder transaktionerne i perioden.  
- Den tredje kolonne er nummeret *C30* med titlen **Hele året** og indeholder bevægelsen i saldiene for hele regnskabsåret.  
- Endelig angiver Ken kolonnedefinitionen som standardindstillingen for finansrapporten **Prognose**.  

### <a name="set-up-a-new-column-definition"></a>Opsætning af ny kolonnedefinition

1. På siden **Finansrapporter** skal du vælge den nye **Prognose**-finansrapport, du har oprettet. Under fanen **Startside** i gruppen **Proces** skal du vælge **Rediger kolonnedefinition**.

2. Opret en ny kolonnedefinition med navnet **Pengestrøm**.

3. Vælg knappen **OK**.

4. Angiv hver linje nøjagtigt som vist i følgende tabel.

    |Kolonnenr.|Kolonnehoved|Kolonnetype|Posteringstype|Beløbstype|Vis|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |D10|Beløb|Nettoændring|Poster|Nettobeløb|Altid|  
    |C20|Beløb til dato|Saldo til dato|Poster|Nettobeløb|Altid|  
    |C30|Hele regnskabsåret|Hele regnskabsåret|Poster|Nettobeløb|Altid|

## <a name="assigning-the-column-definition-to-the-financial-report-name"></a>Tildele en kolonnedefinition til en finansrapport

Ken er nu klar til at tildele kolonnedefinition til finansrapportnavnet.  

### <a name="assign-the-column-definition-to-the-financial-report-name"></a>Tildele en kolonnedefinition til en finansrapport

1. På siden **Finansrapporter** skal du vælge den nye **Prognose**-finansrapport, du har oprettet, og vælg **Rediger kolonnedefinition**.  
2. I feltet **Navn** skal du vælge kolonnedefinitionen **Pengestrøm** for at angive det som standardkolonnedefinition.  

## <a name="view-and-print-the-cash-flow-forecast"></a>Visning og udskrift af likviditetsforecastet

1. På siden **Finansrapporter** skal du vælge **Prognose**-finansrapport for at vise likviditetsforecast.  
2. På siden **Finansrapport** kan du vælge et beløb og derefter få vist pengestrømsprognoseposterne, der udgør beløbet. Derudover kan du få vist den formel, der bruges til at beregne beløbet. Du kan også filtrere beløbene efter dato og dimension.  
3. Vælg handlingen **Udskriv** for at udskrive pengestrømsprognosen.  

## <a name="see-also"></a>Se også

[Arbejde med finansielle rapporter](bi-how-work-account-schedule.md)  
[Analysere pengestrømme i din virksomhed](finance-analyze-cash-flow.md)  
[Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
