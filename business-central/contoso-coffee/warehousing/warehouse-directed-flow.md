---
title: 'Modtagelse, læg-på-lager, flytning, pluk og levering i avanceret lageropsætning med styret plukning og læg-på-lager'
description: I Business Central kan de indgående og udgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.
author: andreipanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: andreipa
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-advanced-warehouse-configuration-with-directed-put-away-and-pick" />Gennemgang af indgående og udgående flow i avanceret opsætning af lagersted med Styret læg-på-lager og pluk

Denne gennemgang viser, hvordan indgående og udgående flow kan fuldføres i Avanceret: Styret læg på lager og pluk-konfiguration. Du kan finde flere oplysninger i [Oversigt over forskellige konfigurationsindstillinger](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites" />Forudsætninger
Fuldfør denne gennemgang, og gør dig selv til lagermedarbejder på lokationen *HVID* ved at følge disse trin:  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
2. Vælg feltet **Bruger-id**, og vælg din egen brugerkonto på siden **Brugere**.  
3. Angiv HVID i feltet **Lokationskode**.  
4. Aktiver **Standard** til/fra.


## <a name="scenario" />Scenarie
Ellen, lagerchefen, bruger muligheder for direkte afsendelse og placeringsgenopfyldning for at øge modtagelses- og transporttiden.  

## <a name="steps" />Trin

1. Opret lagerleverance.  

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
    2. Vælg ordre for debitor 10000 for lokationen HVID. Eksternt Ordrenr er *W-1*. Brug tilpasningsværktøjerne, hvis feltet **Eksternt ordrenr.** feltet er ikke synligt. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](../../ui-personalization-user.md).
    3. Vælg **Opret lagerleverance**-handling i kildedokumentet for at oprette en lagerleverance for valgte salgsordrer.
    4.  Vælg **Frigiv** for at meddele lageret, at leverancen er klar til lagerekspedition.  

2. Definere placering for varen for at kontrollere, hvor de lægges på lager 

    1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
    2.  Vælg *WRB-1000*, og vælg derefter handlingen **Placeringsindhold**.  
    3.  Vælg handlingen **Ny**. Tilføj to linjer. Brug tilpasningsværktøjerne, hvis **Placeringskode** ikke er synligt. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](../../ui-personalization-user.md). 
    
    |Artikel|Lokationskode|Placeringskode|Fast|Måleenhed|
    |----------|----------|---------|---|------|  
    |WRB-1000|HVID|V-05-0001|Ja|TASKE|  
    |WRB-1000|HVID|V-05-0002|Ja|TASKE|

3. Opret lagermodtagelse.  

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.  
    2. Vælg ordre for kreditor 10000 for lokationen HVID. Kreditor Ordrenr er *W-2*. Brug tilpasningsværktøjerne, hvis feltet **Kreditor ordrenr.** feltet er ikke synligt. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](../../ui-personalization-user.md).
    3. Vælg **Opret lagerleveranceskvittering**-handling for at oprette lagerstedskvittering for valgte købsordrer.


4. Kontrollere, om der er udgående ordrer, der skal have modtaget varer og bogfør kvittering
    1. Vælg handlingen **Beregn direkte afsendelse**. Derved udfyldes et kolonne **Ant. til dir. afsend.**.
    2. Indtast 0 i feltet **Antal til dir. afsend.** på linjen med varen *WRB-1000*, som du ikke planlægger at omplanlægge i modtagelsesområdet.
    3. Vælg handlingen **Bogfør kvittering**.

5. Registrere læg-på-lager
    1. Brug ![Lightbulb, der åbner funktionen Fortæl mig 5.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Læg-på-lager**, og vælg derefter det relaterede link.
    2. Finde dokumentet Læg-på-lager (logistik), der er oprettet ud fra lagermodtagelse og åben
    3. Gennemgå afsnittet **Linjer** på siden **læg-på-lager**

    På dette stadie vises logikken for placeringskapacitet. Læg-på-lager-linjerne vil indeholde tre linjer for vare *WRB-1000*:
    - Linjen Hent for at flytte det modtagne antal fra modtagelsesplaceringen (W-08-0001)
    - En Placer-linje, der flytter en 1 pose til en af de konfigurerede faste placeringer (W-05-0001)
    - En Placer-linje, der flytter en anden pose til en anden fast placering (W-05-0002). Det skyldes, at enkelt fast placering ikke kan indeholde det fulde tilgangsantal.

    Da denne læg-på-lager-aktivitet indeholder linjer til direkte afsendelse, kan du se tre linjer for vare *WRB-1001*:
    -  Linjen Hent for at flytte det modtagne antal fra modtagelsesplaceringen (W-08-0001)
    -  En Placer-linje for 2 på den direkte afsendelsesplacering
    -  En Placer-linje for det resterende antal på lagerplacering

    4. Vælg handlingen **Registrer læg-på-lager**.


6. Definere en plukplacering for varen for at kontrollere, hvor de plukkes 

    1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig 6.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.  
    2.  Åbn lokationskortet *HVID*.  
    3.  Vælg handlingen **Placeringer** på **lokationskortet**
    4.  Vælg placeringen *W-02-0001*, og vælg derefter handlingen **Indhold**.  
    5.  Vælg handlingen **Ny**.  
    6.  Aktiver **Fast** til/fra.  
    7.  I feltet **Varenr.** skal du skrive *WRB-1000*. 
    8.  Angiv **Min. antal** i feltet *2*. 
    9.  Angiv **Maks. antal** i feltet *10*. 

    Brug tilpasningsværktøjerne, hvis felterne **Min antal** og **Maks antal** ikke er synlige. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](../../ui-personalization-user.md). 

7. Reorganiser lagersted ved at flytte varer fra masselagerområdet til plukområdet for at optimere pluktiden.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 7.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bevægelseskladder**, og vælg derefter det relaterede link
    2. Vælg handlingen **Beregn genopfyldning**. 

    Lagerkladden med forslag om flytning af vare *WRB-1000* fra masselager til plukområde oprettes.

    3. Vælg handlingen **Opret bevægelse**, og bekræft for at oprette dokumentet.
    4.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig 8.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerbevægelser**, og vælg derefter det relaterede link
    5.  Åbn den lagerbevægelse, du har oprettet, gennemgå afsnittet **Linjer**

     På dette trin vises nedbrydningsfunktionen. Der kommer fire linjer:
    - En linje til at overføre den ene pose med masse lagerplacering
    - En linje til at placere 48-PCS på lager igen på samme placering. 
    - En linje til at tage de 10 PCS med masse lagerplacering
    - En linje, som de 10 PCS skal placeres i plukplaceringen

    6.  Vælg handlingen **Registrer bevægelse**.

8. Opret lagerstedspluk

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 9.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Plukkladder**, og vælg derefter det relaterede link
    2. Vælg funktionen **Hent lagerdokumenter**, marker linjen for salgsordren for debitor 10000, og klik derefter på knappen **OK** for at udfylde kladdelinjerne i henhold til det valgte dokument.

    3. Undersøg feltet **Antal i feltet dir. afs. placering**. 

    4. Vælg handlingen **Opret pluk**.
    5. Bekræft alle de plukindstillinger, du skal bruge, f. eks. aktivér **pr. fra-zone til/fra-område**. Vælg knappen **OK**.
    
    Du modtager en bekræftelsesmeddelelse med pluknumrene. Der er to pluk, da nogle varer er placeret i zonen direkte afsendelse, tæt på forsendelsesområde, og det vil give mening at behandle dem separat.

9.  Registrere lagerplukninger
    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 10.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerstedspluk**, og vælg derefter det relaterede link.
    2. Find de pluk, du har oprettet, og åbn den.
    3. Vælg handlingen **Registrer pluk**.
    4. Gentag for det andet pluk

10. Bogfør lagerstedsleverance
    
    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 11.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerleverancestatus**, og vælg derefter det relaterede link.
    2. Gennemgå afsnittet **Linjer** på siden Lagerstedslevering. Når plukket fra lager er registreret, opdateres lagerleverancen med feltet **antal til levering** angivet.
    3. Vælg **Bogfør leverance**-handling.
    4. Bekræft indstillingen **Levering**.


## <a name="results" />Resultater
- **Bogført lagerstedsmodtagelse** oprettes
- **Bogf. læg-på-lager** oprettes    
- **Bogført købsmodtagelse** oprettes    
- **Købsordren** har opdateret **Modtaget antal** for de modtagne linjer
- **Registreret lagerbevægelse** oprettes
- **Registreret lagerpluk** oprettes
- **Bogført lagerstedslevering** oprettes
- den **bogførte salgsleverance** oprettes
- **Salgsordren** har modtaget **Antal, der er leveret** opdateret for de afsendte linjer
- varen **Lagerbeholdning** øges med enhver rest, der ikke udlever



## <a name="see-also" />Se også
[Modtag varer](../../warehouse-how-receive-items.md) 
[Designdetaljer: Indgående lagerstedsflow](../../design-details-inbound-warehouse-flow.md) 
[Lever varer](../../warehouse-how-ship-items.md) 
[Pluk varer til lagerstedsleverancer](../../warehouse-how-to-pick-items-for-warehouse-shipment.md) 
[Designdetaljer: Udgående lagerstedsflow](../../design-details-outbound-warehouse-flow.md) 
[Vis tilgængelighed for varer](../../inventory-how-availability-overview.md) 
