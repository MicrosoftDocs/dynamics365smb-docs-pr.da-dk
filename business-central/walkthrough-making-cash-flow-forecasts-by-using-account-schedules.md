---
title: Gennemgang - Udarbejd likviditetsforecast ved hjælp af kontoskemaer | Microsoft Docs
description: Denne gennemgang beskriver, hvordan du kan bruge kontoskemaer til at foretage likviditetsforecasts. Kontoskemaer udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti. I kontoskemaerne kan du oprette subtotaler for likviditetsindbetalinger og -udbetalinger. Disse subtotaler kan medtages i nye totaler, der kan bruges i forbindelse med udarbejdelse af likviditetsforecasts.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a210792a187bde0217917659f118c58a6a135df2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756529"
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
For at gennemføre denne gennemgang skal:  

- [!INCLUDE[prod_short](includes/prod_short.md)] være installeret  
- Likviditetskladdelinjerne registreres.  

## <a name="roles"></a>Roller  
Denne gennemgang viser de opgaver, der udføres af følgende brugerrolle:  

- Controller  

## <a name="story"></a>Historie  
Ken er controller hos CRONUS, der udarbejder månedlige likviditetsforecasts. Han medtager økonomi, salg, køb og anlæg i budgettet, og derefter præsenterer han det for Økonomichefen Sara med henblik på brancheindsigt.  

## <a name="setting-up-a-new-account-schedule-name"></a>Opsætning af et nyt kontoskemanavn.  
Et kontoskema består af et kassekontoskemanavn med en række linjer og et kolonneformat.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Sådan opsættes et nyt kontoskemanavn  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.  
2.  På siden **Kontoskemanavne** i skal du vælge handlingen **Ny** for at oprette et nyt kassekontoskemanavn.  
3.  I feltet **Navn** skal du skrive **Forecast**.  
4.  I feltet **Beskrivelse** skal du angive **Pengestrømsprognose**.  
5.  Lad felterne **Standard kolonneformat** og **Analysenavn** være tomme.  

## <a name="setting-up-account-schedule-lines"></a>Opsætning af kontoskemalinjer  
Efter opsætning af et kontoskemanavn, definerer Ken hver linje, der vises i kassekontoskemaet. Ken definerer linjer, der kan vises i rapporter, foruden de linjer, der kun er til beregning.  

### <a name="to-set-up-account-schedule-lines"></a>Opsætning af kontoskemalinjer  

1.  Vælg det nye **Forecast**-kontoskemanavn, du har oprettet, på siden **Kontoskemanavne**, og vælg derefter handlingen **Rediger kontoskema**.  
2.  På siden **Kontoskema** skal du angive hver linje nøjagtigt som vist i følgende tabel.  

    > [!NOTE]  
    >  Ved hjælp af funktionen **Indsæt CF-konti** kan du hurtigt markere pengestrømskonti fra diagrammet for pengestrømkonti og kopiere dem til linjer i kontoskemaet.  

    |Rækkenr.|Beskrivelse|Sammentællingstype|Sammentælling|Rækketype|Beløbstype|Vis|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |C10|Beløb|Bevægelse|Poster|Nettobeløb|Altid|  
    |C20|Beløb til dato|Saldo til dato|Poster|Nettobeløb|Altid|  
    |C30|Hele regnskabsåret|Hele regnskabsåret|Poster|Nettobeløb|Altid|  

4.  Vælg knappen **OK**.  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Tildele kolonneformatet til navnet på kontoskemaet  
Ken er nu klar til at tildele kolonneformatet til kontoskemanavnet.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Sådan tildeles kolonneformatet til navnet på kontoskemaet  

1.  På siden **Kontoskemanavne** skal du vælge **Forecast** i feltet **Navn**.  
2.  I feltet **Standard kolonneformat** skal du vælge kolonneformatet **Pengestrøm** for at angive det som standardkolonneformat.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Visning og udskrift af likviditetsforecastet  
1.  På siden **Kontoskemanavne** skal du vælge handlingen **Oversigt** for at få vist pengestrømsprognosen.  
2.  På siden **Kontoskemaoversigt** kan du vælge et beløb og derefter få vist pengestrømsprognoseposterne, der udgør beløbet. Derudover kan du få vist den formel, der bruges til at beregne beløbet. Du kan også filtrere beløbene efter dato og dimension.  
3.  Vælg handlingen **Udskriv** for at udskrive pengestrømsprognosen.  

## <a name="see-also"></a>Se også  
 [Arbejde med kontoskemaer](bi-how-work-account-schedule.md)   
 [Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]