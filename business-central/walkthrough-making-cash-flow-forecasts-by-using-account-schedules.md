---
title: 'Gennemgang: Udarbejd likviditetsforecast ved hjælp af kontoskemaer'
description: Denne gennemgang beskriver, hvordan du kan bruge kontoskemaer til at foretage likviditetsforecasts i Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 242c3e65401f188068c6e1fbea20212d4a3a7653
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076145"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Gennemgang: Udarbejd likviditetsforecast ved hjælp af kontoskemaer

Denne gennemgang beskriver, hvordan du kan bruge kontoskemaer til at foretage likviditetsforecasts. Kontoskemaer udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti. I kontoskemaerne kan du oprette subtotaler for likviditetsindbetalinger og -udbetalinger. Disse subtotaler kan medtages i nye totaler, der kan bruges i forbindelse med udarbejdelse af likviditetsforecasts.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang

Denne gennemgang beskriver følgende opgaver:  

- Opsætning af et nyt kassekontoskemanavn.  
- Opsætning af kontoskemalinjer.  
- Opsætning af et nyt kolonneformat.  
- Tildeling et kolonneformat til et kontoskema.  
- Visning og udskrift af likviditetsforecastet.  

### <a name="prerequisites"></a>Forudsætninger

For at gennemføre denne gennemgang skal du bruge:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Likviditetskladdelinjerne registreres  

## <a name="roles"></a>Roller

Denne gennemgang viser de opgaver, der udføres af følgende brugerrolle:  

- Controller  

## <a name="story"></a>Historie

Ken er controller hos CRONUS, der udarbejder månedlige likviditetsforecasts. Han medtager økonomi, salg, køb og anlæg i budgettet, og derefter præsenterer han det for Økonomichefen Sara med henblik på brancheindsigt.  

## <a name="setting-up-a-new-account-schedule-name"></a>Opsætning af et nyt kontoskemanavn.

Et kontoskema består af et kassekontoskemanavn med en række linjer og et kolonneformat.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Sådan opsættes et nyt kontoskemanavn  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoskemaer**, og vælg derefter det relaterede link.  
2. På siden **Kontoskemanavne** i skal du vælge handlingen **Ny** for at oprette et nyt kassekontoskemanavn.  
3. I feltet **Navn** skal du skrive **Forecast**.  
4. I feltet **Beskrivelse** skal du angive **Pengestrømsprognose**.  
5. Lad felterne **Standard kolonneformat** og **Analysenavn** være tomme.  

## <a name="setting-up-account-schedule-lines"></a>Opsætning af kontoskemalinjer

Efter opsætning af et kontoskemanavn, definerer Ken hver linje, der vises i kassekontoskemaet. Ken definerer linjer, der kan vises i rapporter, foruden de linjer, der kun er til beregning.  

### <a name="to-set-up-account-schedule-lines"></a>Opsætning af kontoskemalinjer  

1. Vælg det nye **Forecast**-kontoskemanavn, du har oprettet, på siden **Kontoskemanavne**, og vælg derefter handlingen **Rediger kontoskema**.  
2. På siden **Kontoskema** skal du angive hver linje som vist i følgende tabel.  

    > [!TIP]  
    >  Ved hjælp af funktionen **Indsæt CF-konti** kan du hurtigt markere pengestrømskonti fra diagrammet for pengestrømkonti og kopiere dem til linjer i kontoskemaet.  

    | Rækkenr. | Description              | Sammentællingstype            | Sammentælling | Rækketype   | Beløbstype | Vis |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Åbne salgsordrer        | Konti for pengestrømspost | 20       |Bevægelse | Nettobeløb  | Ja  |
    | R10     | Udlejning                  | Konti for pengestrømspost | 30       |Bevægelse | Nettobeløb  | Ja  |
    | R10     | Finansielle anlæg         | Konti for pengestrømspost | 40       |Bevægelse | Nettobeløb  | Ja  |
    | R10     | Afhændelse af faste anlægsaktiver    | Konti for pengestrømspost | 50       |Bevægelse | Nettobeløb  | Ja  |
    | R10     | Private investeringer      | Konti for pengestrømspost | 60       |Bevægelse | Nettobeløb  | Ja  |
    | R10     | Diverse kladder   | Konti for pengestrømspost | 70       |Bevægelse | Nettobeløb  | Ja  |
    | R10     | Åbne serviceordrer      | Konti for pengestrømspost | 80       |Bevægelse | Nettobeløb  | Ja  |
    | R20     | Indbetaling kladde i alt      | Formel                  | R10      |Bevægelse | Nettobeløb  | Ja  |
    | R20     | Indbetaling kladde i alt      | Formel                  | R10      |Bevægelse | Nettobeløb  | Ja  |
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
    | R50     | Overskud                  | Formel                  | R20+R40  |Bevægelse | Nettobeløb  | Ja  |
    | R60     | Likvide midler          | Konti for pengestrømspost | 2100     |Bevægelse | Nettobeløb  | Ja  |
    | R70     | Likviditet i alt          | Formel                  | R50+R60  |Bevægelse | Nettobeløb  | Ja  |

    > [!NOTE]
    > Rækkenummer R10 bruges til at registrere kontototaler for tilgodehavender. Rækkenummer R20 bruges til at beregne summen af alle indbetalinger. Rækkenummer R30 bruges til at registrere kontototaler for skyldige beløb. Rækkenummer R40 bruges til at beregne summen af alle kontante udbetalinger. Rækkenummer R50 bruges til at registrere summen af alle kontante overskud. Rækkenummer R60 bruges til at registrere de likvide midler. Rækkenummer R70 bruges til at beregne den budgetterede pengestrøm.

## <a name="setting-up-a-new-column-layout"></a>Opsætning af et nyt kolonneformat

Før Ken kan udskrive likviditetsforecastet, skal han oprette kolonneformat for de numeriske oplysninger. I kolonnerne skal han definere de oplysninger, han ønsker at bruge fra linjerne.

- Den første kolonne er nummeret *C10* med titlen **Beløb**, og den indeholder bevægelsen.  
- Den anden kolonne er nummereret *C20* med titlen **Saldo til dato** og indeholder transaktionerne i perioden.  
- Den tredje kolonne er nummeret *C30* med titlen **Hele året** og indeholder bevægelsen i saldiene for hele regnskabsåret.  
- Endelig angiver han kolonneformatet som standardkolonneformat for kontoskemaet **Forecast**.  

## <a name="to-set-up-a-new-column-layout"></a>Opsætning af et nyt kolonneformat

1. I vinduet **Kontoskemanavne** skal du vælge det nye **forecast**-kontoskemanavn, du har oprettet. Under fanen **Startside** i gruppen **Proces** skal du vælge **Rediger opsætning af kolonneformat**.

    > [!TIP]
    > Du kan finde den samme handling på siden **Kontoskema**, hvis du stadig redigerer **Forecast**-kontoskemaet her.

2. Opret et nyt kolonneformat med navnet **Pengestrøm**.

3. Vælg knappen OK.

4. Angiv hver linje nøjagtigt som vist i følgende tabel.

    |Kolonnenr.|Kolonnehoved|Kolonnetype|Posteringstype|Beløbstype|Vis|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Beløb|Bevægelse|Poster|Nettobeløb|Altid|  
    |C20|Beløb til dato|Saldo til dato|Poster|Nettobeløb|Altid|  
    |C30|Hele regnskabsåret|Hele regnskabsåret|Poster|Nettobeløb|Altid|

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Tildele kolonneformatet til navnet på kontoskemaet

Ken er nu klar til at tildele kolonneformatet til kontoskemanavnet.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Sådan tildeles kolonneformatet til navnet på kontoskemaet  

1. På siden **Kontoskema**, hvor du arbejder med prognose for **Forecast**-kontoskemaet, skal du vælge handlingen **Rediger kolonneformat opsætning**.  
2. I feltet **Kolonneformatnavn** skal du vælge kolonneformatet **Pengestrøm** for at angive det som standardkolonneformat.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Visning og udskrift af likviditetsforecastet

1. På siden **Kontoskemanavne** skal du vælge handlingen **Oversigt** for at få vist pengestrømsprognosen.  
2. På siden **Kontoskemaoversigt** kan du vælge et beløb og derefter få vist pengestrømsprognoseposterne, der udgør beløbet. Derudover kan du få vist den formel, der bruges til at beregne beløbet. Du kan også filtrere beløbene efter dato og dimension.  
3. Vælg handlingen **Udskriv** for at udskrive pengestrømsprognosen.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Arbejde med kontoskemaer](bi-how-work-account-schedule.md)  
[Analysere pengestrømme i din virksomhed](finance-analyze-cash-flow.md)  
[Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]