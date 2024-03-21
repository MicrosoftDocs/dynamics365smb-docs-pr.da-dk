---
title: 'Modtagelse, placering, plukning og levering i grundlæggende lageropsætning'
description: I Business Central kan de indgående og udgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 02/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Gennemgang af indgående og udgående flow i grundlæggende opsætning af lagersted

Denne gennemgang viser, hvordan indgående og udgående flow kan fuldføres i grundlæggende: ordre-til-ordre-konfiguration. Du kan finde flere oplysninger i [Oversigt over forskellige konfigurationsindstillinger](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## Forudsætninger  
Fuldfør denne gennemgang, og gør dig selv til lagermedarbejder på lokationen *SØLV* ved at følge disse trin:  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
2. Vælg feltet **Bruger-id**, og vælg din egen brugerkonto på siden **Brugere**.  
3. Angiv **SØLV** i feltet *Lokationskode*.  

## Indgående flow: Modtagelse og placering på lager i grundlæggende lageropsætninger

I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.  

|Metode|Indgående proces|Placering|Modtagelser|Læg-på-lager-aktiviteter|Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|T|Bogfør lagermodtagelse og læg-på-lager fra ordrelinjen|X|||2|  
|B|Bogfør lagermodtagelse og læg-på-lager fra et læg-på-lager-dokument|||X|3|  
|L|Bogfør lagermodtagelse og læg-på-lager fra et lagermodtagelsesdokument||X||5-4-6|  
|D|Bogfør modtagelse fra et lagermodtagelsesdokument, og bogfør læg-på-lager fra lagerets læg-på-lager-dokument||X|X|5-4-6|  

Du kan finde flere oplysninger i [Designoplysninger: Indgående lagerflow](../../design-details-inbound-warehouse-flow.md)  

Den følgende gennemgang viser metode B i forrige tabel.  

### Scenarie  
Alicia, indkøbsagenten, opretter en købsordre på forskellige brændte bønner. Når leveringen ankommer til lagerstedet, John, lagermedarbejderen, placerer varerne på lager i egnede placeringer. Når John bogfører læg-på-lager-aktiviteten, bogføres varerne som modtaget på lageret og er tilgængelige til salg eller andet behov.  

### Trin
1. Opsætningen af siden **Lokationskort** definerer indgående flows i virksomheden.  

    1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.  
    2.  Åbn lokationskortet *SØLV*.  
    3.  Markér afkrydsningsfeltet **Kræv læg-på-lager**.  

2. Definere en standardplacering for de to varenumre for at kontrollere, hvor de lægges på lager

    1.  Vælg handlingen **Placeringer** på **lokationskortet**
    2.  Vælg den første række, til placering *S-1-01*, og vælg derefter handlingen **Indhold**.  
    3.  Vælg handlingen **Ny**.  
    4.  Vælg felterne **Fast** og **Standard**.  
    5.  I feltet **Varenr.** skal du skrive *WRB-1000*.  

3. Opret købsordrer, der er den mest almindelige type indgående kildedokument.  

    1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.  
    2.  Vælg handlingen **Ny**.  
    3.  Opret en købsordre for kreditor 10000 med følgende købsordrelinjer. Brug tilpasningsværktøjerne, hvis **Placeringskode** ikke er synligt. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](../../ui-personalization-user.md). 

    |Artikel|Lokationskode|Placeringskode|Antal|  
    |----------|----------|---------|--------------|  
    |WRB-1000|SØLV|S-1-01|20|  
    |WRB-1001|SØLV||30|

    Placeringskoden i den første udfyldes derfor. Placeringskoden for den anden vare er tom, da den ikke har standardværdier. Behold denne metode.  

    4.  Vælg handlingen **Frigiv** for at meddele lageret, at købsordren er klar til lagerekspedition, når leverancen ankommer.  

4. Oprette **Læg-på-lager** for at modtage og lægge de leverede varer på lager  

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Læg-på-lager-aktiviteter**, og vælg derefter det relaterede link.  
    2. Vælg handlingen **Ny**. 
    3. I feltet *Lokationskode* vælges **SØLV**.
    4. Vælg feltet **Kildedokument**, og vælg derefter **Købsordre**.  
    5. Vælg **Kildenr.** skal du vælge linjen for købet hos leverandøren 10000 og derefter vælge knappen **OK** for at udfylde læg-på-lager-linjerne i henhold til det valgte kildedokument.

        Du kan også vælge handlingen **Hent kildedokument** og derefter vælge købsordren.  

5. Rediger læg-på-lager-aktiviteten baseret på faktisk placering af varer, og bogfør bilag

    Når der lægges varer på placeringer, har John bemærket, at standardplaceringen allerede indeholder nogle varer, så han har besluttet at bruge en anden placering. John anbringer også andre varer på de næste placeringer, da det modtagne antal ikke passer til kapaciteten.

    1. På første linje ændres **Placeringskoden** fra *S-1-01*, der blev kopieret fra købsordren, til *S-1-02*. 
    2.  Indtast 20 i feltet **Mgd. at håndtere** i læg-på-lager-linjen med varen WRB-1000.  
    3. På den anden linje skal du angive 20 i feltet **Mgd. at håndtere** og vælge **Opdel linje**-handlingen. Der vises en ny linje, som er en kopi af den oprindelige linje, bortset fra at feltet **Håndteringsantal** indeholder det antal, du har fjernet fra den oprindelige linje. 
    4. Udfyld placeringskoderne for vare WRB-1001:

    |Artikel|Placeringskode|Antal|  
    |----------|-------------------|--------------|  
    |WRB-1001|S-1-03|20|  
    |WRB-1001|S-1-04|10|

    5.  Vælg handlingen **Bogfør**, vælg handlingen **Modtag**, og vælg derefter knappen **OK**.  

### Resultater 
 - De brændte bønner registreres nu som lagt på lager på bestemte placeringer
 - **Bogf. læg-på-lager** oprettes
 - **Bogført købsmodtagelse** oprettes
 - købsordren har modtaget **Antal, der er modtaget** opdateret for de modtagne linjer
 - varen **Lageret** øges med det valgte antal
    

## Udgående flow: Pluk og forsendelse i grundlæggende lageropsætninger

I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan de udgående processer for pluk og levering udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.  

|Metode|Indgående proces|Placering|Pluk|Leverancer|Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|T|Bogfør pluk og leverance fra ordrelinjen|X|||2|  
|B|Bogfør pluk og leverance fra et lagerplukdokument||X||3|  
|L|Bogfør pluk og leverance fra et lagerleverancedokument|||X|5-4-6|  
|D|Bogfør pluk fra et lagerplukdokument, og bogfør leverance fra et lagerleverancedokument||X|X|5-4-6|  

Du kan finde flere oplysninger i [Designoplysninger: Udgående lagerflow](../../design-details-outbound-warehouse-flow.md)  

Den følgende gennemgang viser metode B i forrige tabel.

### Scenarie  
Susan, ordrebehandleren, opretter en salgsordre for forskellige brændte bønner og overfører den til lagerstedet. John, som arbejder på lageret, skal sørge for, at forsendelsen klargøres og leveres til debitoren. John administrerer alle involverede opgaver på siden **Pluk (lager)**, som automatisk peger på de placeringer, hvor brændte bønner opbevares.

### Trin
Dette er en fortsættelse af [Indgående flow: Modtagelse og placering på lager i grundlæggende lageropsætninger](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Opsætningen af siden **Lokationskort** definerer indgående flows i virksomheden.  

    1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig 5.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.  
    2.  Åbn lokationskortet *SØLV*.  
    3.  Markér afkrydsningsfeltet **Kræv pluk**.  

2. Opret salgsordrer, der er den mest almindelige type udgående kildedokument.  

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 6.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
    2. Vælg handlingen **Ny**.  
    3. Opret en salgsordre for debitor 10000 med følgende salgsordrelinje.  

    |Artikel|Lokationskode|Antal|  
    |----|-------------|--------|  
    |WRB-1000|SØLV|20|  
    |WRB-1001|SØLV|30|  

    Placeringskoderne udfyldes automatisk med standardplaceringer.

    4. Vælg handlingen **Opret læg-på-lager/pluk**.
    5. Markér afkrydsningsfeltet **Opret pluk (lager)**.  
    6. Vælg knappen **OK**. Der oprettes et nyt lagerpluk.

3. Plukke og levere varer

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 7.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk fra lager**, og vælg derefter det relaterede link.  
    2. Vælge lagerpluk for salg til debitor 10000
    
    Det oprettede pluk ignorerede den placering, der er defineret for varen *WRB-1000*, da den ikke indeholder lager og brugte en anden placering. De næste linjer med vare *WRB-1001* blev automatisk opdelt, så de kan plukkes fra flere forskellige placeringer.
    
4. Vælg handlingen **Autofyld håndteringsantal**.  

5. Vælg handlingen **Bogfør**, vælg **Lever**, og vælg derefter knappen **OK**.  

### Resultater
 - De brændte bønner registreres nu som plukket fra bestemte placeringer
 - **Bogført lagerpluk** oprettes
 - den **bogførte salgsleverance** oprettes
 - salgsordren har modtaget **Antal, der er leveret** opdateret for de afsendte linjer
 - varen **Lageret** reduceres med det valgte antal


## Se også
[Læg-på-lager-varer med læg-på-lager-aktiviteter](../../warehouse-how-to-put-items-away-with-inventory-put-aways.md) 
[Konfigurere basislagersteder med operationsområder](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) 
[Designdetaljer: Indgående lagerstedsflow](../../design-details-inbound-warehouse-flow.md) 
[Pluk varer med lagerstedspluk](../../warehouse-how-to-pick-items-with-inventory-picks.md) 
[Designdetaljer: Udgående lagerstedsflow](../../design-details-outbound-warehouse-flow.md) 
[Vis tilgængelighed for varer](../../inventory-how-availability-overview.md) 
