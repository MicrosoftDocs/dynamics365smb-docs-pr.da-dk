---
title: 'Modtagelse, placering, plukning og levering i blandet lageropsætning'
description: I Business Central kan de indgående og udgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# Gennemgang af indgående og udgående flow i blandet opsætning af lagersted

Denne gennemgang viser, hvordan indgående og udgående flow skal udfyldes i blandet konfiguration, hvor for indgående lagersteder er konfigureret som basis: ordre-til-ordre og for udgående flow Avanceret konfiguration bruges. Du kan finde flere oplysninger i [Oversigt over forskellige konfigurationsindstillinger](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## Forudsætninger  
Fuldfør denne gennemgang, og gør dig selv til lagermedarbejder på lokationen *GUL* ved at følge disse trin:  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
2. Vælg feltet **Bruger-id**, og vælg din egen brugerkonto på siden **Brugere**.  
3. Angiv **GUL** i feltet *Lokationskode*.  

## Indgående flow: Modtagelse og placering på lager i grundlæggende lageropsætninger

I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.  

|Metode|Indgående proces|Placering|Modtagelser|Læg-på-lager-aktiviteter|Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|T|Bogfør lagermodtagelse og læg-på-lager fra ordrelinjen|X|||2|  
|B|Bogfør lagermodtagelse og læg-på-lager fra et læg-på-lager-dokument|||X|3|  
|L|Bogfør lagermodtagelse og læg-på-lager fra et lagermodtagelsesdokument||X||5-4-6|  
|D|Bogfør modtagelse fra et lagermodtagelsesdokument, og bogfør læg-på-lager fra lagerets læg-på-lager-dokument||X|X|5-4-6|  

Du kan finde flere oplysninger i [Designoplysninger: Indgående lagerflow](../../design-details-inbound-warehouse-flow.md)  

Den følgende gennemgang viser metode C i forrige tabel.  

### Scenarie  
Alicia, indkøbsagenten, opretter købsordrer på forskellige brændte bønner, når efterspørgslen vises. Når leveringen ankommer på lagerstedet, sætter John, som er lagerarbejder, varerne på lager på standardplaceringer, der er defineret for varerne. Når John bogfører modtagelsen, bogføres varerne som modtaget på lageret og tilgængelige til salg eller andre behov.  

### Trin
1. Opsætningen af siden **Lokationskort** definerer indgående flows i virksomheden.  

    1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.  
    2.  Åbn lokationskortet *GUL*.  
    3.  Deaktiver **Kræv læg-på-lager** til/fra.  

2. Frigiv Købsordrer til lagersted.  

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.  
    2. Vælg ordrer fra kreditor 10000 til lokationen GUL. Ingen leverandørordrenr. er *Y-1* og *Y-2*. Brug tilpasningsværktøjerne, hvis feltet **Kreditor ordrenr.** feltet er ikke synligt. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](../../ui-personalization-user.md).
    3. Vælg handlingen **Frigiv** for at meddele lageret, at købsordren er klar til lagerekspedition, når leverancen ankommer.  

3. Oprette Lagermodtagelse for at modtage og lægge de leverede varer på lager
    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermodtagelser**, og vælg derefter det relaterede link.
    2. Vælg handlingen **Ny**
    3. På siden lagermodtagelse skal du trykke på Enter for automatisk at få valgt et lagermodtagelsesnummer
    4. Angiv **GUL** i feltet *Lokationskode*.
    5. Vælg handlingen **Hent kildedokumenter...**
    6. Vælg tidligere frigivne købsordrer fra kreditor 10000, og klik på knappen **OK**.
        Linjerne vil indeholde en ny post for hver købsordrelinje.

4. Reguler antal til modtagelse baseret på modtaget antal, og bogfør bilag
    1. Vælg linje med vare *WRB-1000*.
    2. Marker *OVERRCPT10* i feltet **Overmodtagelseskode**, og skift værdien i feltet **Modtag antal** fra *100* til *110*.
    3. Vælg linje med vare *WRB-1001* og 
    4. På den anden linje skal du ændre værdien i feltet **Antal til modtagelse** fra *200* til *190*.
    5. Vælg handlingen **Bogfør kvittering**.

### Resultater 
 - De brændte bønner registreres nu som lagt på lager
 - **Bogført lagerstedsmodtagelse** oprettes
 - **Bogført købsmodtagelse** oprettes
 - købsordren har modtaget **Antal, der er modtaget** opdateret for de modtagne linjer
 - varen **Lageret** øges med det valgte antal
    

## Udgående flow: Pluk og forsendelse i avancerede lageropsætninger

I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan de udgående processer for pluk og levering udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.  

|Metode|Indgående proces|Placering|Pluk|Leverancer|Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|T|Bogfør pluk og leverance fra ordrelinjen|X|||2|  
|B|Bogfør pluk og leverance fra et lagerplukdokument||X||3|  
|L|Bogfør pluk og leverance fra et lagerleverancedokument|||X|5-4-6|  
|D|Bogfør pluk fra et lagerplukdokument, og bogfør leverance fra et lagerleverancedokument||X|X|5-4-6|  

Du kan finde flere oplysninger i [Designoplysninger: Udgående lagerflow](../../design-details-outbound-warehouse-flow.md)  

Den følgende gennemgang viser metode D i forrige tabel.

### Scenarie  
Susan, ordrebehandleren, opretter salgsordrer for forskellige brændte bønner og overfører den til lagerstedet. Da alle ordrer kommer fra den samme kunde, beslutter Ellen, lagerchefen, at levere dem sammen. John, som arbejder på lageret, skal sørge for, at forsendelsen klargøres og leveres til debitoren.

### Trin
Dette er en fortsættelse af [Indgående flow: Modtagelse og placering på lager i grundlæggende lageropsætninger](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Frigiv salgsordrer til lagersted.  

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 5.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
    2. Vælg ordrer til debitor 10000 til lokationen GUL. Eksterne ordrenr. er *Y-3*, *Y-4* og *Y-5*. Brug tilpasningsværktøjerne, hvis feltet **Eksternt ordrenr.** feltet er ikke synligt. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](../../ui-personalization-user.md).
    3. Vælg **Frigiv** for at meddele lageret, at de valgte salgsordrer er klar til lagerekspedition.  

2. Afsende varer  
    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 6.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerleverancer**, og vælg derefter det relaterede link.  
    2. Vælg handlingen **Ny**.  
    3. Angiv **GUL** i feltet *Lokationskode*.  
    4. Vælg handlingen **Brug filtre til at hente kildedok.**.  
    5. Skriv **CUST10000** i feltet **Kode**.  
    6. Angiv **Debitor 10000** i feltet **Beskrivelse**.  
    7. Vælg handlingen **Ret**.  
    8. I oversigtspanelet **Salg** skal du i feltet **Kundenummerfilter** angive *10000*.  
    9. Vælg handlingen **Kør**. 
    
    Lagermodtagelsen udfyldes med fire linjer, der repræsenterer salgsordrelinjer for de angivne debitorer. Feltet **Lever (antal)** er tomt, da varer først skal plukkes.

3. Oprette lagerpluk fra lagerleverance
    1. Vælg handlingen **Opret pluk** på siden lagerleverance.
    2. Bekræft alle de plukindstillinger, du skal bruge, f.eks. vælg *Vare* i feltet **Sorteringsmetode for aktivitetslinje** for at gruppere de samme varer sammen. Vælg knappen **OK**.
    3. Du modtager en bekræftelsesmeddelelse med pluknummer. 

4. Åbne lagerplukket
    1. Brug ![Lightbulb, der åbner funktionen Fortæl mig 7.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerstedspluk**, og vælg derefter det relaterede link.
    2. Find de pluk, du har oprettet, og åbn det.
    3. Opdatere **Mgd. at håndtere**, hvis det er nødvendigt.
    4. Vælg handlingen **Registrer pluk**.
    5. Lagerplukket lukkes og fjernes, hvis alle antal håndteres.

5. Bogfør lagerstedsleverance
   1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 8.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerleverancer**, og vælg derefter det relaterede link.  
   2. Find den leverance, du har oprettet tidligere, og åbn den.
    Bemærk, at **Lever (antal)** er udfyldt.
    3. Du kan opdatere **Bogføringsdato**, **Eksternt bilagsnr.**, **Speditørkode**, **Leveringsmåde**, hvis det er nødvendigt. Ikke-tomme værdier overføres til kildedokumenter.
    4. Vælg **Bogfør leverance**-handling.
    5. Bekræft indstillingen **Levering**.

### Resultater
 - De brændte bønner registreres nu som plukket 
 - **Registreret lagerpluk** oprettes
 - **Bogført lagerstedslevering** oprettes
 - de tre **bogførte salgsleverance** oprettes
 - salgsordren har modtaget **Antal, der er leveret** opdateret for de afsendte linjer
 - varen **Lageret** reduceres med det valgte antal


## Se også
[Modtag varer](../../warehouse-how-receive-items.md)
[Konfigurer basislagersteder med operationsområder](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)
[Designdetaljer: Indgående lagerstedsflow](../../design-details-inbound-warehouse-flow.md)
[Lever varer](../../warehouse-how-ship-items.md)
[Pluk varer til lagerleverance](../../warehouse-how-to-pick-items-for-warehouse-shipment.md)
[Designdetaljer: udgående lagerstedsflow](../../design-details-outbound-warehouse-flow.md)
[Vis tilgængelighed for varer](../../inventory-how-availability-overview.md)
