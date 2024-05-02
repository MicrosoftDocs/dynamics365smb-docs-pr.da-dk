---
title: Oprette en behovsprognose
description: 'Få mere at vide om behovsprognosefunktioner, og hvordan du kan oprette salgs-og produktionsprognoser.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '9245, 99000919, 99000921, 99000922'
ms.date: 03/11/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-a-demand-forecast"></a>Oprette en behovsprognose

Du kan oprette salgs- og produktionsforecasts vha. siden **Behovsprognoser**. Derefter skal du for hvert forecast angive forskellige indstillinger for budgettet på siden **Oversigt over behovsprognose**.  

Prognosefunktionaliteten anvendes til oprettelse af forventet behov; faktisk behov oprettes fra salgs- og produktionsordrer. I forbindelse med oprettelsen af hovedplanen modregnes et forecast i salgs- og produktionsordrerne. Feltet **Prognosetype** i forecastet afgør, hvilken behovstype der skal tages højde for i forbindelse med modregningen. Hvis forecastet omhandler en *salgsvare*, er det kun salgsordrer, der sammenholdes med forecastantallet. Hvis det er for *komponenter*, sammenfattes forecastet kun fra afhængigt behov fra produktionsordrekomponenter.  

Ved at udnytte forecastfunktionaliteten kan en virksomhed oprette "hvad nu hvis"-scenarier og dermed både effektivt og uden ressourcespild planlægge, tage højde for og imødekomme behov. Et nøjagtigt forecast kan være netop det, der afgør, om virksomheden kan overholde den aftalte leveringstid, levere de bestilte varer til tiden og gøre kunden tilfreds.  

Med 2022 udgivelsesbølge 1 kan du også angive det rigtige detaljeringsniveau i felterne **Forecast efter lokation** og **Forecast efter variant** på siden **Oversigt over behovsprognose**. Filtre og andre indstillinger gemmes i tabellen **Behovsprognosenavn**. Så du nemt kan stoppe og fortsætte arbejdet senere. Hvis organisationen er blevet opdateret til 2022 udgivelsesbølge 1, skal du skifte til den nye oplevelse på siden [Funktionsadministration](admin-feature-management.md).  

## <a name="sales-forecasts-and-production-forecasts"></a>Salgsforecast og produktionsforecast

Du kan oprette kombinerede eller uafhængige salgs- eller produktionsforecasts med programmets forecastfunktion. De fleste virksomheder, der fremstiller varer til ordre, har f.eks. ikke et færdigvarelager, fordi varerne først produceres, når firmaet modtager en ordre. Derfor er det afgørende at kunne forudse ordrer (salgsforecast), så de bestilte varer kan produceres inden for en rimelig tid (produktionsforecast). Det kan f.eks. forsinke produktionen, hvis der er lang leveringstid på en bestemt komponent til en vare, som ikke allerede er i ordre eller på lager.  

- Et salgsforecast er salgsafdelingens kvalificerede bud på, hvad der vil blive solgt fremover, og det er derfor opdelt i varer og perioder. Men et salgsforecast giver ikke altid tilstrækkelige oplysninger til produktionen.  
- Produktionsforecast er produktionsplanlæggerens projektion af, hvor mange færdigvarer og afledte underordnede samlinger der skal fremstilles i bestemte perioder for at dække prognosticeret salg.  

I de fleste tilfælde vil den person, der har ansvaret for produktionsplanlægningen, derfor redigere et salgsforecast, så det passer til de betingelser, der gælder for produktionen, men uden at det betyder, at salgsforecastet ikke længere er nøjagtigt.  

Du kan oprette forecasts manuelt på siden **Behovsprognose**. Der kan være flere forecasts i systemet, som identificeres vha. deres navn og type. Et forecast kan kopieres og redigeres efter behov. 

> [!NOTE]
> På et givet tidspunkt kun er ét forecast, der kan bruges til planlægningsformål.

Et forecast består af en række oplysninger som varenummer, forecastdato og forecastantal. Et forecast for en vare dækker en periode, der afgrænses af den angivne forecastdato og forecastdatoen for den næste (eller forrige) forecastpost. Set fra et planlægningssynspunkt bør forecastantallet være til rådighed fra starten på behovsperioden.  

Du skal angive, om et forecast omhandler en *Salgsvare*, *Komponent* eller *Begge*. Forecasttypen *Salgsvare* bruges til salgsprognoser. Når du opretter et produktionsforecast, skal du bruge typen *Komponent*. Formålet med forecasttypen *Begge* er udelukkende at give planlæggeren en oversigt over både salgsforecastet og produktionsforecastet. Hvis du har valgt denne indstilling, kan oplysningerne i forecastet ikke redigeres. Når du angiver disse forecasttyper her, kan du angive et salgsforecast i den samme kladde, som du bruger til et produktionsforecast, og du kan se begge forecasts samtidig i én og samme kladde. Bemærk, at systemet behandler de forskellige oplysninger (salg og produktion) forskelligt, når planlægningen beregnes afhængigt af den opsætning, der er valgt til varer og produktion.  

## <a name="component-forecast"></a>Komponentforecast

Et komponentforecast kan betragtes som et forecast for en model eller variant i forhold til en overordnet eller samlet vare. Det kan f.eks. være en fordel, at planlæggeren kan give et bud på komponentbehovet.  

Eftersom formålet med et komponentforecast er at angive flere muligheder for en overordnet vare, kan komponentforecastet mindre end eller lig med antallet i salgsforecastet. Hvis komponentforecastet er større end salgsforecastet, behandler systemet forskellen mellem de to prognosetyper som et uafhængigt behov.  

## <a name="forecasting-periods"></a>Forecastperioder

Forecastperioden træder i kraft på den angivne startdato og er gældende, indtil det næste forecast træder i kraft. I tidsintervalsiden har du flere muligheder for at indsætte behovet på en bestemt dato i en periode. Derfor anbefales det, at du undlader at ændre forecastperioden, medmindre du vil flytte alle forecastoplysninger til periodens startdato.  

## <a name="forecast-by-locations"></a>Forecast opdelt efter lokationer

På siden **Produktionsopsætning** kan du angiv, hvordan du vil håndtere lokationer, der er defineret på estimater, når du beregner planer. 

### <a name="use-forecast-by-locations"></a>Brug forecast på lokationer

Hvis du slår til/fra-feltet **Brug forecast pr. lokation** til, skal [!INCLUDE[prod_short](includes/prod_short.md)] respektere de lokationskoder, der er angivet for hver efterspørgselsprognosepost, og beregne restbudgettet for hver lokation.  

Overvej dette eksempel: Virksomheden køber og sælger varer på to lokationer: EAST og WEST. For begge lokationer har du konfigureret en metode til at genbestille lot-til-Lot. Du opretter forecast for de to lokationer:

- 10 stykker af lokation EAST
- 4 stykker af lokation WEST

Derefter skal du oprette en salgsordre med et antal på 12 på lokationen WEST. Planlægningssystemet vil foreslå, at du gør følgende:

- Genopfyld 10 enheder for lokation EAST, baseret på data fra din forecast.  
- Genopfyld 12 enheder for lokationen WEST baseret på salgsordren. De fire stk., der blev angivet i din forecast, forbruges fuldt ud af det faktiske behov fra salgsordren. Hvis du ønsker yderligere oplysninger, kan du se [Forecastbehov reduceres af salgsordrer](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

> [!NOTE]  
> Hvis du får vist lokationsbaserede forecasts enkeltvis, skal du være opmærksom på, at det ikke er sikkert, at den overordnede forecast i så fald giver et korrekt billede.

### <a name="if-you-dont-use-forecast-by-locations"></a>Brug ikke forecast på lokationer

Hvis du slå til/fra-feltet **Brug forecast pr. lokation** fra, vil [!INCLUDE[prod_short](includes/prod_short.md)] ignorere de lokationskoder, der er angivet for hver efterspørgselsprognosepost, og beregne prognoser for tomme lokationer.  

Overvej dette eksempel: Virksomheden køber og sælger varer på to lokationer: EAST og WEST. For begge lokationer har du konfigureret en metode til at genbestille lot-til-Lot. Du opretter forecast for de to lokationer:

- 10 stykker af lokation EAST
- 4 stykker af lokation WEST

Derefter skal du oprette en salgsordre med et antal på 12 på lokationen WEST. Planlægningssystemet vil foreslå, at du gør følgende:

- Genopfyld 12 enheder for lokationen WEST baseret på salgsordren.  
- Genbestille 2 enheder for den tomme lokation. De 10 og 4 stk., der blev angivet i din forecast, forbruges delvis ud af det faktiske behov fra salgsordren. [!INCLUDE[prod_short](includes/prod_short.md)] ignorerede de lokationskoder, der er angivet af brugeren og anvender i stedet en tom lokation.  

> [!NOTE]  
> Du kan angive et filter på lokationer, men placeringsbaserede resultater passer muligvis ikke til planlægningsresultaterne uden filtre.

## <a name="to-create-a-demand-forecast"></a>Sådan oprettes en behovsprognose

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Behovsprognose**, og vælg derefter det relaterede link.  
2. Vælg på oversigtspanelet **Generelt** en prognose i feltet **Navn på behovsprognose**. Hvis der er flere forecasts i systemet, kan du skelne imellem dem vha. navnet og forecasttypen.  
3. Vælg i feltet **Lokationsfilter** den lokation, som dette forecast skal gælde for.
4. I feltet **Vis efter** for at ændre den periode, der vises i hver kolonne. Du kan vælge mellem følgende intervaller: **Dag**, **Uge**, **Måned**, **Kvartal**, **År** eller **Regnskabsperiode**, som opsætning i finansområde.

> [!NOTE]  
> Du bør overveje, hvilket tidsinterval du vil bruge til fremtidige forecasts, så tidsintervallet er konsistent hele vejen igennem. Når du angiver et forecastantal, gælder det kun den første dag i det tidsinterval, du vælger. Hvis du f.eks. vælger en måned, skal du angive forecastantallet på den første dag i måneden. Hvis du vælger et kvartal, skal du angive forecastantallet på den første dag i den første måned i kvartalet.

5. Vælg i feltet **Vis som**, hvordan forecastantal vises for tidsintervallet. Hvis du vælger **Bevægelse**, vises bevægelsen i saldoen for tidsintervallet. Hvis du vælger **Saldo til dato**, viser siden saldoen pr. den sidste dag i tidsintervallet.  
6. I feltet **Forecasttype** skal du vælge **Salgsvare**, **Komponent** eller **Begge**. Hvis du vælger **Salgsvare** eller **Komponent**, kan du redigere antallet efter periode. Hvis du vælger **Begge**, kan du ikke redigere antallet, men du kan vælge pilen til rullelisten og få vist behovsprognoseposter.  
7. Angiv et **Datofilter**, hvis du vil begrænse den mængde data, der skal vises.  
8. I oversigtspanelet **Matrix for efterspørgselsprognose** skal du angive de budgetterede antal ved at indtaste et antal i den celle, der repræsenterer en vare på en bestemt dato eller i en bestemt periode. Bemærk, at opslagsknappen i tomme celler åbner en tom side, der angiver, at du skal angive en værdi manuelt.   

> [!NOTE]  
> Du kan også redigere et eksisterende forecast. Klik på siden **Matrix for efterspørgselsprognose**, vælg handlingen **Kopiér behovsprognose**, og udfyld siden **Behovsprognose** med en eksisterende pronose. Antal kan redigeres efter behov.  

## <a name="see-also"></a>Se også

[Konfigurere produktion](production-configure-production-processes.md)  
[Produktions-](production-manage-manufacturing.md)
[lager](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
