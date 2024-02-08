---
title: Beregne ordrebekræftelsesdatoer
description: 'Beregning af leveringstid er et værktøj, du kan bruge til at beregne den tidligst mulige dato, en vare er disponibel til afsendelse eller levering.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="calculate-order-promising-dates"></a>Beregne ordrebekræftelsesdatoer

En virksomhed skal være i stand til at informere deres kunder om leveringsdatoer for ordren. Med siden **Beregning af lev.tid - linjer** kan du gøre dette fra en salgsordre.  

[!INCLUDE[prod_short](includes/prod_short.md)] beregner leverance- og leveringsdatoer baseret på en vares kendte og forventede rådighedsdatoer , som derefter kan stilles i udsigt for debitor.  

Hvis der står en ønsket leveringsdato på en salgsordrelinje, bruges denne dato som udgangspunkt for følgende beregninger:  

- ønsket leveringsdato– transporttid = planlagt afsendelsesdato  
- planlagt afsendelsesdato – udgående lagerekspeditionstid = planlagt afsendelsesdato  

Hvis varen er disponibel til pluk på afsendelsesdatoen, kan salgsprocessen fortsættes. Hvis varen ikke er disponibel til pluk på afsendelsesdatoen, vises en advarsel om, at varen ikke er på lager.  

Hvis du ikke angiver en ønsket leveringsdato på en salgsordrelinje, eller hvis ikke den ønskede leveringsdato kan imødekommes, vil den tidligste dato for varernes tilgængelighed blive beregnet. Datoen kan derefter indtastes i feltet **Afsendelsesdato** på linjen, og den dato, som du planlægger at levere varer samt den dato, hvor de leveres til debitor beregnes ved hjælp af følgende beregninger:  

- afsendelsesdato + udgående lagerekspeditionstid = planlagt afsendelses dato  
- planlagt afsendelsesdato + transporttid = planlagt leveringsdato  

## <a name="about-order-promising"></a>Om beregning af leveringstid

Vha. funktionen Beregning af leveringstid kan du oprette en ordrebekræftelse med en bestemt afsendelses- eller leveringsdato. Den dato, hvor en vare er disponibel til levering eller den første mulige afsendelsesdato for en vare og opretter ordrelinjer for de datoer, som du godkender. Funktionen beregner den tidligst mulige dato, en vare er disponibel til afsendelse eller levering. Funktionen opretter også rekvisitionslinjer, hvis varerne først skal købes eller produceres, for de datoer, du godkender.

[!INCLUDE[prod_short](includes/prod_short.md)] bruger to grundlæggende begreber:  

- Disp.-til-levering  
- Første m. afs.dato  

### <a name="available-to-promise"></a>Disp.-til-levering

Disp.-til-levering (ATP) beregner datoer baseret på reservationssystemet. Der udføres en tilgængelighedskontrol af de ikke-reserverede mængder på lageret med henblik på planlagt produktion, indkøb, overførsler og salgsreturvarer. Baseret på disse oplysninger beregner [!INCLUDE[prod_short](includes/prod_short.md)] leveringsdato for kundens ordre, da varerne er tilgængelige på lageret eller på fastlagte tilgange.  

### <a name="capable-to-promise"></a>Første m. afs.dato

Første m. afs.dato (CTP) forudsætter et "hvad nu hvis"-scenarie, som kun gælder for vareantal, der ikke findes på lageret eller i planlagte ordrer. Baseret på dette scenarie vil [!INCLUDE[prod_short](includes/prod_short.md)] beregne den tidligste dato, varen kan være tilgængelig, hvis den skal produceres, købes eller overføres.

#### <a name="example"></a>Eksempel

Hvis der er en ordre på henholdsvis 10 stk. og 6 stk. er tilgængelige på lageret eller i planlagte ordrer, så skal den første m. afs.dato-beregning baseres på 4 stykker.

### <a name="calculations"></a>Beregninger

Når [!INCLUDE[prod_short](includes/prod_short.md)] beregner kundens leveringsdato, udfører den to opgaver:  

- Den beregner den tidligste leveringsdato, når kunden ikke har anmodet om en bestemt leveringsdato.  
- Kontrollerer, om den leveringsdato, som kunden havde ønsket, eller som var blevet lovet kunden, er realistisk.  

Hvis kunden ikke anmoder om en bestemt leveringsdato, bliver afsendelsesdato sat til at være lig med arbejdsdato, og tilgængeligheden er derefter baseret på denne dato. Hvis varen er på lager, beregner [!INCLUDE[prod_short](includes/prod_short.md)] fremad i tiden for at bestemme, hvornår ordren kan leveres. Dette opnås ved hjælp af følgende formler:  

- Afsendelsesdato - Udgående lagerekspeditionstid = Planlagt afsendelsesdato  
- Planlagt afsendelsesdato + Transporttid = Planlagt leveringsdato  

[!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer derefter, om den beregnede leveringsdato er realistisk ved at regne bagud i tid og afgøre, hvornår varen skal være tilgængelig for at kunne opfylde den lovede dato. Dette opnås ved hjælp af følgende formler:  

- Planlagt leveringsdato + Transporttid = Planlagt afsendelsesdato  
- Planlagt afsendelsesdato - Udgående lagerekspeditionstid = Afsendelsesdato  

Afsendelsesdatoen bruges til udførelse af tilgængelighedskontrollen. Hvis varen er tilgængelig på denne dato, vil [!INCLUDE[prod_short](includes/prod_short.md)] bekræfte, at den ønskede/bekræftede leveringsdato kan overholdes ved at angive den planlagte leveringsdato skal være lig med den ønskede/bekræftede leveringsdato. Hvis varen ikke er tilgængelig, returneres en tom dato og ordrebehandler kan derefter bruge funktionen LE.  

Baseret på nye datoer og klokkeslæt, beregnes alle relaterede datoer ifølge de formler, der er angivet tidligere i dette afsnit. LE-beregningen tager længere tid, men den giver en nøjagtig dato, når kunden kan forvente at have varen leveret. De datoer, som beregnes ud fra CTP, vises i felterne **Planlagt leveringsdato** og **Tidligste afsendelsesdato** på siden **Beregning af lev.tid - linjer**.  

Ordrebehandler afslutter LE-processen ved at acceptere datoerne. Det betyder, at en planlægningslinje og en reservationspost oprettes for varen, inden de datoer, der er beregnet til at sikre, at ordren opfyldes.  

Foruden den eksterne beregning af leveringstid, som du kan udføre på siden **Beregning af lev.tid - linjer**, kan du også love interne eller eksterne leveringsdatoer for stykliste-elementer. Du kan finde flere oplysninger i [Vise tilgængeligheden af varer](inventory-how-availability-overview.md).

## <a name="to-set-up-order-promising"></a>Sådan defineres beregning af leveringstid

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætn. af beregn. af lev.tid**, og vælg derefter det relaterede link.  
2. Angiv et nummer og en tidsenhedskode i feltet **Responstid**. Marker én af følgende koder.  

    |Kode|Beskrivelse|  
    |----------|-----------------|  
    |**d**|Kalenderdag|  
    |**a**|Uge|  
    |**m**|Måned|  
    |**q**|Kvartal|  
    |**y**|År|  

    ”3u” angiver f.eks., at responstiden er 3 uger. Brug ”c” som præfiks til koderne for at angive den aktuelle tidsenhed. Hvis responstiden f.eks. skal være den aktuelle måned, skal du angive **cm**.  
3. Angiv en nummerserie i feltet **Nr. for beregn. af lev.tid** ved at vælge en linje fra oversigten på siden **Nummerserier**.  
4. Angiv en skabelon til beregning af leveringstid i feltet **Skabl. til beregn. af lev.tid** ved at vælge en linje fra oversigten på siden **Indkøbskld.typeover**.  
5. Angiv en indkøbskladdetype i feltet **Kld. til beregn. af lev.tid** ved at vælge en linje i oversigten på siden **Indkøbskladdenavne**.

### <a name="inbound-and-outbound-warehouse-handling-times-in-order-promising"></a>Indgående og Udgående lagerekspeditionstid i beregning af leveringstid

Hvis du automatisk vil inkludere lagerekspeditionstiden i beregningen af leveringstiden på købslinjen, kan du på siden **Opsætning af Lager** angive en standardindstilling for ekspeditionstid til salgs- og købsdokumenter. Du kan også angive bestemte tidspunkter for hver af lokationerne på siden **Lokationskort**. 

#### <a name="to-enter-default-inbound-and-outbound-warehouse-handling-times-for-sales-and-purchase-documents"></a>Angive standard-indgående og -udgående lagerekspeditionstid for salgs-og købsdokumenter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af Lager**, og vælg derefter det relaterede link.  
2. På oversigtspanelet **Generelt** i felterne **Indgående lagerekspeditionstid** og **Udgående lagerekspeditionstid** skal du angive det antal dage, du vil inkludere i beregningerne af leveringstiden.  

#### <a name="to-enter-inbound-and-outbound-warehouse-handling-times-on-locations"></a>Angive ind- og udgående lagerekspeditionstider på lokationer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokation**, og vælg derefter det relaterede link.  
2.  Åbn det relevante lokationskort.  
3.  På oversigtspanelet **Lagersted** i felterne **Indgående lagerekspeditionstid** og **Udgående lagerekspeditionstid** skal du angive det antal dage, du ønsker at inkludere i beregningerne af leveringstiden.  

> [!NOTE]  
>  Hvis du opretter en købsordre, og du vælger **lokation** i feltet **Leveringsadresse** i oversigtspanelet **Levering og betaling**, og du derefter vælger en lokation i feltet **Lokationskode**, udfyldes bruger felterne **Udgående lagerekspeditionstid** og **Indgående lagerekspeditionstid** det ekspeditionstidstidspunkt, der er angivet for lokationen. Det samme gælder for salgsordrer, hvis du vælger en lokation i feltet **Lokationskode**. Hvis der ikke er angivet nogen ekspeditionstid for lokationen, er felterne **Udgående lagerekspeditionstid** og **Indgående lagerekspeditionstid** tomme. Hvis du lader feltet **Lokationskode** stå tomt på salgs- og købsdokumenterne, bruger beregningen den ekspeditionstid, der er angivet på siden **Lageropsætning**.

## <a name="to-make-an-item-critical"></a>Sådan gør du en vare kritisk

Før en vare kan indgå i beregningen af ordrebekræftelsen, skal den markeres som kritisk. Denne opsætning sikrer, at ikke-kritiske varer ikke medfører irrelevante beregnede leveringstider.   
1.  Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2.  Åbn det relevante varekort.  
3.  Vælg feltet **Kritisk** i oversigtspanel **Planlægning**.  

## <a name="to-calculate-an-order-promising-date"></a>Sådan beregnes en ordrebekræftelsesdato

1.  Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordre**, og vælg derefter det relaterede link.  
2.  Åbn den relevante salgsordre, og vælg de salgsordrelinjer, du vil have programmet til at beregne.  
3.  Vælg handlingen **Beregning af leveringstid**, og vælg derefter handlingen **Beregning af lev.tid - linjer**.  
4.  Vælg en linje, og vælg derefter en af følgende indstillinger:  

    - Marker **Disp.-til-bekræftelse**, hvis du vil beregne den tidligste dato, en vare er disponibel med hensyntagen til lager, fastlagt tilgang og bruttobehov.  
    - Marker **Første m. afs.dato**, hvis du ved, at varen er udgået af lageret og du vil beregne den tidligste dato, varen kan være disponibel ved at afsende en genbestillingsordre.  
5.  Vælg knappen **Accepter** for at godkende den tidligst tilgængelige afsendelsesdato.  

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Beregne dato for køb](purchasing-date-calculation-for-purchases.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
