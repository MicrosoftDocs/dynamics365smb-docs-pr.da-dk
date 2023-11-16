---
title: Pluk og forsendelse i grundlæggende lageropsætninger
description: I denne artikel beskrives forskellige niveauer af kompleksitet i pluk-og leveringsprocesser.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Gennemgang: Pluk og forsendelse i grundlæggende lageropsætninger

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du modtage varer og indsætte dem på en af fire måder som beskrevet i følgende tabel.

|Metode|Udgående proces|Kræv pluk|Kræv leverance|Sværhedsgrad (få mere at vide på [Warehouse Management-oversigt](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bogfør pluk og leverance fra ordrelinjen|||Ingen dedikeret lageraktivitet.|  
|B|Bogfør pluk og leverance fra et lagerplukdokument|Aktiveret||Basis: Ordre for ordre.|  
|U|Bogfør pluk og leverance fra et lagerstedsleverancedokument||Aktiveret|Basis: Konsolideret modtagelse/levering for flere ordrer.|  
|D|Bogfør pluk fra et lagerstedsplukdokument, og bogfør leverance fra et lagerstedsleverancedokument|Aktiveret|Aktiveret|Avanceret|  

Få mere at vide på [Udgående lagerstedsflow](design-details-outbound-warehouse-flow.md).

Den følgende gennemgang viser metode B i forrige tabel.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang

I grundlæggende lageropsætninger, hvor lokationen, du vil plukke fra, er sat op til at kræve pluk, men ikke leverance, bruges siden **Pluk (lager)** til at registrere og bogføre pluk- og leveranceoplysninger for de udgående kildedokumenterne. Det udgående kildedokumentet kan være en salgsordre, en købsreturvareordre, en udgående overflytning eller en produktionsordre med komponentbehov.  

Denne gennemgang viser følgende opgaver:  

- Indstilling af SYD-lokation til pluk fra lager.  
- Oprettelse af en salgsordre for debitor 10000 til 30 Amsterdam Lamps.  
- Frigivelse af salgsordren til lagerekspedition.  
- Oprette et pluk baseret på et frigivet kildedokumentet.  
- Registrering af lagerbevægelsen fra lageret og på samme tid bogføring af salgsleverancen til kildesalgsordren.  

## <a name="roles"></a>Roller

Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:  

- Lagerchef  
- Ordrebehandler  
- Lagermedarbejder  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a>Historie

Ellen, lagerlederen hos CRONUS, konfigurerer lagerstedet SYD til grundlæggende håndtering af pluk, hvor lagermedarbejdere kan behandle udgående ordrer enkeltvis. Susan, ordrebehandleren, opretter en salgsordre for 30 enheder af varen LS-1928-S, der skal sendes til debitor 10000 på lagerstedet SYD. John, som arbejder på lageret, skal sørge for, at forsendelsen klargøres og leveres til debitoren. John administrerer alle involverede opgaver på siden **Pluk (lager)**, som automatisk peger på de placeringer, hvor 1928-S opbevares.

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a>Indstilling af placeringskoder

Når du har oprettet lokationen, skal du tilføje to placeringer.

#### <a name="to-setup-the-bin-codes"></a>Indstilling af placeringskoder

1. Vælg handlingen **Placeringer**.
2. Opret to placeringer med koderne *S-01-0001* og *S-01-0002*.

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a>Selv oprette en lagermedarbejder på lokationen SYD

Hvis du vil bruge denne funktion, skal du føje dig selv til lokationen som en lagermedarbejder. 

#### <a name="to-make-yourself-a-warehouse-employee"></a>Sådan oprettes en lagermedarbejder som en lagermedarbejder

  1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig første.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
  2. Vælg feltet **Bruger-id**, og vælg din egen brugerkonto på siden **Lagerstedsansatte**.
  3. Angiv SYD i feltet **Lokationskode**.  
  4. Vælg handlingen **Bogfør**, og vælg derefter knappen **Ja**.  

### <a name="making-item-1928-s-available"></a>Gør vare 1928-S tilgængelig

Gør varen 1928-S tilgængelig på SYD-lokationen ved at følge disse trin:  

  1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig anden.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varekladder**, og vælg derefter det relaterede link.  
  2. Åbn standardkladden, og opret derefter to varekladdelinjer med de følgende oplysninger om arbejdsdatoen (23. januar).  

        |Postens type|Varenummer|Lokationskode|Placeringskode|Antal|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Opregulering|1928-S|SYD|S-01-0001|20|  
        |Opregulering|1928-S|SYD|S-01-0002|20|  

        Feltet **Placeringskode** på salgslinjerne er som standard skjult, så de skal vises. Hvis du vil gøre dette, skal du tilpasse siden. Du kan finde flere oplysninger i [Start af tilpasning af en side gennem det personlige banner](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

  3. Vælg **Bogfør** i gruppen **Bogføring** under fanen **Handlinger**.  
  4. Vælg knappen **Ja**.  

## <a name="creating-the-sales-order"></a>Oprettelse af salgsordren

Salgsordrer er den mest almindelige type udgående kildedokument.  

### <a name="to-create-the-sales-order"></a>Sådan oprettes salgsordren

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig tredje.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Opret en salgsordre for debitor 10000 på arbejdsdatoen (23. januar) med følgende salgsordrelinje.  

    |Vare|Lokationskode|Antal|  
    |----|-------------|--------|  
    |1928-S|SYD|30|  

     Fortsæt ved at meddele lageret, at salgsordren er klar til lagerekspedition.  

4. Vælg handlingen **Frigivelse**.  

    John fortsætter ved at vælge og sende de solgte varer.  

## <a name="picking-and-shipping-items"></a>Sådan plukkes og leveres varer

På siden **Pluk (lager)** kan du administrere alle udgående lageraktiviteter til et specifikt kildedokument såsom en salgsordre. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a>Sådan foretages pluk og levering af varer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig fjerde.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk fra lager**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  

    Sørg for, at feltet **Nr.** er udfyldt i oversigtspanelet **Generelt**.
3. Vælg feltet **Kildedokument**, og vælg derefter **Salgsordre**.  
4. Vælg feltet **Kildenr.**, vælg linjen for salget til debitor 10000, og vælg knappen **OK**.  

    Du kan også vælge handlingen **Hent kildedokument** og derefter vælge salgsordren.  
5. Vælg handlingen **Autofyld håndteringsantal**.  

    Du kan også indtaste henholdsvis 10 og 20 på de to lagerpluklinjer i feltet **Håndteringsantal**.  
6. Vælg handlingen **Bogfør**, vælg **Lever**, og vælg derefter knappen **OK**.  

    De 30 Amsterdam Lamps er nu registreret som plukket fra placeringerne S-01-0001 og S-01-0002, og der oprettes en negativ varepost, der afspejler den bogførte salgsleverance.  

## <a name="see-also"></a>Se også

[Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Plukke varer til lagerstedsleverance](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Oprette grundlæggende lagersteder med handlingsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md)  
[Flytte varer ad hoc i grundlæggende lageropsætninger](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Designoplysninger: Udgående lagerflow](design-details-outbound-warehouse-flow.md)  
[Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
