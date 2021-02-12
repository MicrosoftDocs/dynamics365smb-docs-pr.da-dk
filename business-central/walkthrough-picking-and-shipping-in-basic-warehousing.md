---
title: Pluk og forsendelse i grundlæggende lageropsætninger | Microsoft Docs
description: I Business Central kan de udgående processer for pluk og levering udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f3815e0e928041ca9fcef09b1c7410e45ebb57a1
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035752"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Gennemgang: Pluk og forsendelse i grundlæggende lageropsætninger

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

I [!INCLUDE[prod_short](includes/prod_short.md)] kan de udgående processer for pluk og levering udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.  

|Metode|Indgående proces|Placering|Pluk|Leverancer|Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|T|Bogfør pluk og leverance fra ordrelinjen|X|||2|  
|B|Bogfør pluk og leverance fra et lagerplukdokument||X||3|  
|L|Bogfør pluk og leverance fra et lagerleverancedokument|||X|5-4-6|  
|D|Bogfør pluk fra et lagerplukdokument, og bogfør leverance fra et lagerleverancedokument||X|X|5-4-6|  

Du kan finde flere oplysninger i [Designoplysninger: Udgående lagerflow](design-details-outbound-warehouse-flow.md)  

Den følgende gennemgang viser metode B i forrige tabel.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="about-this-walkthrough"></a>Om denne gennemgang

I grundlæggende lageropsætninger, hvor lokationen, du vil plukke fra, er sat op til at kræve pluk, men ikke leverance, bruges siden **Pluk (lager)** til at registrere og bogføre pluk- og leveranceoplysninger for de udgående kildedokumenterne. Det udgående kildedokumentet kan være en salgsordre, en købsreturvareordre, en udgående overflytning eller en produktionsordre med komponentbehov.  

Denne gennemgang viser følgende opgaver:  

- Indstilling af SØLV-lokation til pluk fra lager.  
- Oprettelse af en salgsordre for debitor 10000 til 30 højttalere.  
- Frigivelse af salgsordren til lagerekspedition.  
- Oprette et pluk baseret på et frigivet kildedokumentet.  
- Registrering af lagerbevægelsen fra lageret og på samme tid bogføring af salgsleverancen til kildesalgsordren.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a>Roller

Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:  

- Lagerchef  
- Ordrebehandler  
- Lagermedarbejder  

## <a name="prerequisites"></a>Forudsætninger

For at gennemføre denne gennemgang skal du bruge:  

- Til [!INCLUDE[prod_short](includes/prod_short.md)] online en virksomhed, der er baseret på indstillingen **Avanceret evaluering - komplette eksempeldata** i et sandkassemiljø. Til [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø installeret CRONUS International Ltd.  
- Du kan oprette dig selv som lagermedarbejder på lokationen SØLV ved at følge disse trin:  

  1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
  2. Vælg feltet **Bruger-id**, og vælg din egen brugerkonto på siden **Brugere**.  
  3. Angiv SØLV i feltet **Lokationskode**.  
  4. Markér feltet **Standard**.  

- Gør varen LS-81 tilgængelig på SØLV-lokationen ved at følge disse trin:  

  1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varekladder**, og vælg derefter det relaterede link.  
  2. Åbn standardkladden, og opret derefter to varekladdelinjer med de følgende oplysninger om arbejdsdatoen (23. januar).  

        |Postens type|Varenummer|Lokationskode|Placeringskode|Antal|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Opregulering|LS-81|SØLV|S-01-0001|20|  
        |Opregulering|LS-81|SØLV|S-01-0002|20|  

  3. Vælg handlingen **Bogfør**, og vælg derefter knappen **Ja**.  

## <a name="story"></a>Historie

Ellen, lagerlederen hos CRONUS, konfigurerer lagerstedet SØLV til grundlæggende håndtering af pluk, hvor lagermedarbejdere kan behandle udgående ordrer enkeltvis. Susan, ordrebehandleren, opretter en salgsordre for 30 enheder af varen LS-81, der skal sendes til debitor 10000 på lagerstedet SØLV. John, som arbejder på lageret, skal sørge for, at forsendelsen klargøres og leveres til debitoren. John administrerer alle involverede opgaver på siden **Pluk (lager)**, som automatisk peger på de placeringer, hvor LS-81 opbevares.  

## <a name="setting-up-the-location"></a>Indstilling af lokation

Opsætningen af siden **Lokationskort** definerer flows i virksomheden.  

### <a name="to-set-up-the-location"></a>Sådan oprettes lokationen

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lokationer**, og vælg dernæst det relaterede link.  
2. Åbn lokationskortet SØLV.  
3. Markér afkrydsningsfeltet **Kræv pluk** i oversigtspanelet **Lagersted**.  

## <a name="creating-the-sales-order"></a>Oprettelse af salgsordren

Salgsordrer er den mest almindelige type udgående kildedokument.  

### <a name="to-create-the-sales-order"></a>Sådan oprettes salgsordren

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Opret en salgsordre for debitor 10000 på arbejdsdatoen (23. januar) med følgende salgsordrelinje.  

    |Vare|Lokationskode|Antal|  
    |----|-------------|--------|  
    |LS_81|SØLV|30|  

     Fortsæt ved at meddele lageret, at salgsordren er klar til lagerekspedition.  

4. Vælg handlingen **Frigivelse**.  

    John fortsætter ved at vælge og sende de solgte varer.  

## <a name="picking-and-shipping-items"></a>Sådan plukkes og leveres varer

På siden **Pluk (lager)** kan du administrere alle udgående lageraktiviteter til et specifikt kildedokument såsom en salgsordre. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a>Sådan foretages pluk og levering af varer

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagerpluk**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  

    Sørg for, at feltet **Nr.** er udfyldt i oversigtspanelet **Generelt**.
3. Vælg feltet **Kildedokument**, og vælg derefter **Salgsordre**.  
4. Vælg feltet **Kildenr.**, vælg linjen for salget til debitor 10000, og vælg knappen **OK**.  

    Du kan også vælge handlingen **Hent kildedokument** og derefter vælge salgsordren.  
5. Vælg handlingen **Autofyld håndteringsantal**.  

    Du kan også indtaste henholdsvis 10 og 20 på de to lagerpluklinjer i feltet **Håndteringsantal**.  
6. Vælg handlingen **Bogfør**, vælg **Lever**, og vælg derefter knappen **OK**.  

    De 30 højttalere er nu registreret som plukket fra placeringerne S-01-0001 og S-01-0002, og der oprettes en negativ varepost, der afspejler den bogførte salgsleverance.  

## <a name="see-also"></a>Se også

[Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Plukke varer til lagerleverance](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Oprette grundlæggende lagersteder med handlingsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md)  
[Flytte varer ad hoc i grundlæggende lageropsætninger](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Designoplysninger: Udgående lagerflow](design-details-outbound-warehouse-flow.md)  
[Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
