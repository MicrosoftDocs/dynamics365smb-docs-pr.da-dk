---
title: "Gennemgang - Udarbejd likviditetsforecast ved hjælp af kontoskemaer | Microsoft Docs"
description: "Denne gennemgang beskriver, hvordan du kan bruge kontoskemaer til at foretage likviditetsforecasts. Kontoskemaer udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti. I kontoskemaerne kan du oprette subtotaler for likviditetsindbetalinger og -udbetalinger. Disse subtotaler kan medtages i nye totaler, der kan bruges i forbindelse med udarbejdelse af likviditetsforecasts."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c66fc5da322ddb1d217b61da0b563faab27b344e
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

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

- [!INCLUDE[d365fin](includes/d365fin_md.md)] være installeret  
- Likviditetskladdelinjerne registreres.  

## <a name="roles"></a>Roller  
Denne gennemgang viser de opgaver, der udføres af følgende brugerrolle:  

- Controller  

## <a name="story"></a>Historie  
Ken er controller hos CRONUS, der udarbejder månedlige likviditetsforecasts. Han medtager økonomi, salg, køb og anlæg i budgettet, og derefter præsenterer han det for Økonomichefen Sara med henblik på brancheindsigt.  

## <a name="setting-up-a-new-account-schedule-name"></a>Opsætning af et nyt kontoskemanavn.  
Et kontoskema består af et kassekontoskemanavn med en række linjer og et kolonneformat.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Sådan opsættes et nyt kontoskemanavn  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.  
2.  I vinduet **Kontoskemanavne** i skal du vælge handlingen **Ny** for at oprette et nyt kassekontoskemanavn.  
3.  I feltet **Navn** skal du skrive **Forecast**.  
4.  I feltet **Beskrivelse** skal du angive **Pengestrømsprognose**.  
5.  Lad felterne **Standard kolonneformat** og **Analysenavn** være tomme.  

## <a name="setting-up-account-schedule-lines"></a>Opsætning af kontoskemalinjer  
Efter opsætning af et kontoskemanavn, definerer Ken hver linje, der vises i kassekontoskemaet. Ken definerer linjer, der kan vises i rapporter, foruden de linjer, der kun er til beregning.  

### <a name="to-set-up-account-schedule-lines"></a>Opsætning af kontoskemalinjer  

1.  I vinduet **Kontoskemanavne** skal du vælge det nye **forecast**-kontoskemanavn, du har oprettet. Under fanen **Startside** i gruppen **Proces** skal du vælge **Rediger kontoskema**.  
2.  I vinduet **Kontoskema** skal du angive hver linje nøjagtigt som vist i følgende tabel.  

    > [!NOTE]  
    >  Ved hjælp af funktionen **Indsæt CF-konti** kan du hurtigt markere pengestrømskonti fra diagrammet for pengestrømkonti og kopiere dem til linjer i kontoskemaet.  

    |Rækkenr.|Beskrivelsen|Sammentællingstype|Sammentælling|Rækketypen|Beløbstype|Vis|  
    |-------|-----------|-------------|--------|--------|---  ------|----| |C10|Beløb|Bevægelse|Poster|Nettobeløb|Altid|  
    |C20|Beløb til dato|Saldo til dato|Poster|Nettobeløb|Altid|  
    |C30|Helt regnskabsår|Helt regnskabsår|Poster|Nettobeløb|Altid|  

4.  Vælg knappen **OK**.  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Tildele kolonneformatet til navnet på kontoskemaet  
Ken er nu klar til at tildele kolonneformatet til kontoskemanavnet.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Sådan tildeles kolonneformatet til navnet på kontoskemaet  

1.  I vinduet **Kontoskemanavne** skal du vælge **Forecast** i feltet **Navn**.  
2.  I feltet **Standard kolonneformat** skal du vælge kolonneformatet **Pengestrøm** for at angive det som standardkolonneformat.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Visning og udskrift af likviditetsforecastet  
1.  I vinduet **Kontoskemanavne** skal du vælge handlingen **Oversigt** for at få vist pengestrømsprognosen.  
2.  I vinduet **Kontoskemaoversigt** kan du vælge et beløb og derefter få vist pengestrømsprognoseposterne, der udgør beløbet. Derudover kan du få vist den formel, der bruges til at beregne beløbet. Du kan også filtrere beløbene efter dato og dimension.  
3.  Vælg handlingen **Udskriv** for at udskrive pengestrømsprognosen.  

## <a name="see-also"></a>Se også  
 [Fremgangsmåde: Arbejde med kontoskemaer](bi-how-work-account-schedule.md)   
 [Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

