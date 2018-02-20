---
title: "Sådan oprettes et produktionsforecast | Microsoft Docs"
description: Du kan oprette salgs- og produktionsforecasts vha. vinduet **Produktionsforecast**.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fea8af85518d608f051be154e551c4c8645ed42a
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="create-a-production-forecast"></a>Oprette et produktionsforecast
Du kan oprette salgs- og produktionsforecasts vha. vinduet **Produktionsforecast**.  

Prognosefunktionaliteten anvendes til oprettelse af forventet behov; faktisk behov oprettes fra salgs- og produktionsordrer. I forbindelse med oprettelsen af hovedplanen modregnes et forecast i salgs- og produktionsordrerne. Indstillingen *Komponent* i forecastet afgør, hvilken behovstype der skal tages højde for i forbindelse med modregningen. Hvis forecastet omhandler en salgsvare, er det kun salgsordrer, der sammenholdes med forecastantallet. Hvis det er for komponenter, sammenfattes forecastet kun fra afhængigt behov fra produktionsordrekomponenter.  

Ved at udnytte forecastfunktionaliteten kan en virksomhed oprette "hvad nu hvis"-scenarier og dermed både effektivt og uden ressourcespild planlægge, tage højde for og imødekomme behov. Et nøjagtigt forecast kan være netop det, der afgør, om virksomheden kan overholde den aftalte leveringstid, levere de bestilte varer til tiden og gøre kunden tilfreds.  

## <a name="sales-forecasts-and-production-forecasts"></a>Salgsforecast og produktionsforecast  
Du kan oprette kombinerede eller uafhængige salgs- eller produktionsforecasts med programmets forecastfunktion. De fleste virksomheder, der fremstiller varer til ordre, har f.eks. ikke et færdigvarelager, fordi varerne først produceres, når firmaet modtager en ordre. Derfor er det afgørende at kunne forudse ordrer (salgsforecast), så de bestilte varer kan produceres inden for en rimelig tid (produktionsforecast). Det kan f.eks. forsinke produktionen, hvis der er lang leveringstid på en bestemt komponent til en vare, som ikke allerede er i ordre eller på lager.  

-   Et salgsforecast er salgsafdelingens kvalificerede bud på, hvad der vil blive solgt fremover, og det er derfor opdelt i varer og perioder. Men et salgsforecast giver ikke altid tilstrækkelige oplysninger til produktionen.  
-   Produktionsforecast er produktionsplanlæggerens projektion af, hvor mange færdigvarer og afledte underordnede samlinger der skal fremstilles i bestemte perioder for at dække prognosticeret salg.  

I de fleste tilfælde vil den person, der har ansvaret for produktionsplanlægningen, derfor redigere et salgsforecast, så det passer til de betingelser, der gælder for produktionen, men uden at det betyder, at salgsforecastet ikke længere er nøjagtigt.  

Du kan oprette forecasts manuelt i vinduet **Produktionsforecast**. Der kan være flere forecasts i systemet, som identificeres vha. deres navn og type. Et forecast kan kopieres og redigeres efter behov. Bemærk, at der på et givet tidspunkt kun er ét forecast, der kan bruges til planlægningsformål.  

Et forecast består af en række oplysninger som varenummer, forecastdato og forecastantal. Et forecast for en vare dækker en periode, der afgrænses af den angivne forecastdato og forecastdatoen for den næste (eller forrige) forecastpost. Set fra et planlægningssynspunkt bør forecastantallet være til rådighed fra starten på behovsperioden.  

Du skal angive, om et forecast omhandler en *Salgsvare*, *Komponent* eller *Begge*. Forecasttypen *Salgsvare* bruges til salgsprognoser. Når du opretter et produktionsforecast, skal du bruge typen *Komponent*. Formålet med forecasttypen *Begge* er udelukkende at give planlæggeren en oversigt over både salgsforecastet og produktionsforecastet. Hvis du har valgt denne indstilling, kan oplysningerne i forecastet ikke redigeres. Når du angiver disse forecasttyper her, kan du angive et salgsforecast i den samme kladde, som du bruger til et produktionsforecast, og du kan se begge forecasts samtidig i én og samme kladde. Bemærk, at systemet behandler de forskellige oplysninger (salg og produktion) forskelligt, når planlægningen beregnes afhængigt af den opsætning, der er valgt til varer og produktion.  

## <a name="component-forecast"></a>Komponentforecast  
Et komponentforecast kan betragtes som et forecast for en model eller variant i forhold til en overordnet eller samlet vare. Det kan f.eks. være en fordel, at planlæggeren kan give et bud på komponentbehovet.  

Eftersom formålet med et komponentforecast er at angive flere muligheder for en overordnet vare, kan komponentforecastet være lig med eller mindre end antallet i salgsforecastet. Hvis komponentforecastet er større end salgsforecastet, behandler systemet forskellen mellem de to forecasttyper som et uafhængigt behov.  

## <a name="forecasting-periods"></a>Forecastperioder  
 Forecastperioden træder i kraft på den angivne startdato og er gældende, indtil det næste forecast træder i kraft. I tidsintervalvinduet har du flere muligheder for at indsætte behovet på en bestemt dato i en periode. Derfor anbefales det, at du undlader at ændre forecastperioden, medmindre du vil flytte alle forecastoplysninger til periodens startdato.  

## <a name="forecast-by-locations"></a>Forecast opdelt efter lokationer  
Det kan angives under produktionsopsætningen, hvis. Hvis du får vist lokationsbaserede forecasts enkeltvis, skal du være opmærksom på, at det ikke er sikkert, at den overordnede forecast i så fald giver et korrekt billede.

## <a name="to-create-a-production-forecast"></a>Sådan oprette et produktionsforecast

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Produktionsforecast**, og vælg derefter det relaterede link.  
2.  På oversigtspanelet **Generelt**, vælges et forecast i feltet **Produktionsforecastnavn**. Hvis der er flere forecasts i systemet, kan du skelne imellem dem vha. navnet og forecasttypen.  
3.  Vælg i feltet **Lokationsfilter** den lokation, som dette forecast skal gælde for.  
4.  I feltet **Forecasttype** skal du vælge **Salgsvare**, **Komponent** eller **Begge**. Hvis du vælger **Salgsvare** eller **Komponent**, kan du redigere antallet efter periode. Hvis du vælger **Begge**, kan du ikke redigere antallet, men du kan vælge pilen til rullelisten og få vist produktionsforecastposter.  
5.  Angiv et **Datofilter**, hvis du vil begrænse den mængde data, der skal vises.  
6.  I oversigtspanelet **Matrix for produktionsforecast** skal du angive det prognosticerede antal for forecasts for **salgsvarer** eller **Komponenter** for de forskellige perioder.  
7.  På oversigtspanelet **Matrixindstillinger** kan du angive tidsintervallet i feltet **Vis efter** for at ændre den periode, der er vist i den enkelte kolonne. Du kan vælge mellem følgende intervaller: **Dag**, **Uge**, **Måned**, **Kvartal**, **År** eller **Regnskabsperiode**, som opsætning i finansstyringen.  

    > [!NOTE]  
    >  Du bør overveje, hvilket tidsinterval du vil bruge til fremtidige forecasts, så tidsintervallet er konsistent hele vejen igennem. Når du angiver et forecastantal, gælder det kun den første dag i det tidsinterval, du vælger. Hvis du f.eks. vælger en måned, skal du angive forecastantallet på den første dag i måneden. Hvis du vælger et kvartal, skal du angive forecastantallet på den første dag i den første måned i kvartalet.  

8.  Vælg i feltet **Vis som**, hvordan forecastantal vises for tidsintervallet. Hvis du vælger **Bevægelse**, vises bevægelsen i saldoen for tidsintervallet. Hvis du vælger **Saldo til dato**, viser vinduet saldoen pr. den sidste dag i tidsintervallet.  

> [!NOTE]  
>  Du kan også redigere et eksisterende forecast. Klik i vinduet **Matrix for produktionsforecast**, vælg handlingen **Kopier produktionsforecast**, og udfyld vinduet **Produktionsforecast** med et eksisterende forecast. Antal kan redigeres efter behov.  

## <a name="see-also"></a>Se også  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

