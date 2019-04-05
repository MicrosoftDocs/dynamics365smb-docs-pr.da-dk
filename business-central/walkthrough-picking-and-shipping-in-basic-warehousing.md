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
ms.date: 01/31/2019
ms.author: sgroespe
ms.openlocfilehash: 1b07a3b064f1bc45a183d0a2d27b810312007a22
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792242"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Gennemgang: Pluk og forsendelse i grundlæggende lageropsætninger

**Bemærk**: Denne gennemgang skal udføres på et demoregnskab med indstillingen **Fuld evaluering - Komplette eksempeldata**, der findes i sandkassemiljøet. Du kan finde flere oplysninger i [Oprette et sandkassemiljø](across-how-create-sandbox-environment.md).

I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de udgående processer for pluk og levering udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.  

|Metode|Indgående proces|Placering|Pluk|Leverancer|Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|T|Bogfør pluk og leverance fra ordrelinjen|X|||2|  
|B|Bogfør pluk og leverance fra et lagerplukdokument||X||3|  
|L|Bogfør pluk og leverance fra et lagerleverancedokument|||X|5-4-6|  
|D|Bogfør pluk fra et lagerplukdokument, og bogfør leverance fra et lagerleverancedokument||X|X|5-4-6|  

Du kan finde flere oplysninger i [Designoplysninger: Udgående lagerflow](design-details-outbound-warehouse-flow.md)  

Den følgende gennemgang viser metode B i forrige tabel.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
I grundlæggende lageropsætninger, hvor lokationen, du vil plukke fra, er sat op til at kræve pluk, men ikke leverance, bruges siden **Pluk (lager)** til at registrere og bogføre pluk- og leveranceoplysninger for de udgående kildedokumenterne. Det udgående kildedokumentet kan være en salgsordre, en købsreturvareordre, en udgående overflytning eller en produktionsordre med komponentbehov.  

Denne gennemgang viser følgende opgaver:  

-   Indstilling af SØLV-lokation til pluk fra lager.  
-   Oprettelse af en salgsordre for debitor 10000 til 30 højttalere.  
-   Frigivelse af salgsordren til lagerekspedition.  
-   Oprette et pluk baseret på et frigivet kildedokumentet.  
-   Registrering af lagerbevægelsen fra lageret og på samme tid bogføring af salgsleverancen til kildesalgsordren.  

## <a name="roles"></a>Roller  
Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:  

-   Lagerchef  
-   Ordrebehandler  
-   Lagermedarbejder  

## <a name="prerequisites"></a>Forudsætninger  
For at gennemføre denne gennemgang skal:  

-   CRONUS Danmark A/S være installeret.  
-   Du kan oprette dig selv som lagermedarbejder på lokationen SØLV ved at følge disse trin:  

    1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
    2.  Vælg feltet **Bruger-id**, og vælg din egen brugerkonto på siden **Brugere**.  
    3.  Angiv SØLV i feltet **Lokationskode**.  
    4.  Markér feltet **Standard**.  

-   Gør varen LS-81 tilgængelig på SØLV-lokationen ved at følge disse trin:  

    1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varekladder**, og vælg derefter det relaterede link.  
    2.  Åbn standardkladden, og opret derefter to varekladdelinjer med de følgende oplysninger om arbejdsdatoen (23. januar).  

        |Postens type|Varenummer|Lokationskode|Placeringskode|Antal|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Opregulering|LS-81|SØLV|S-01-0001 **Bemærk:** Varens standardplacering i CRONUS|20|  
        |Opregulering|LS-81|SØLV|S-01-0002|20|  

    3.  Vælg handlingen **Bogfør**, og vælg derefter knappen **Ja**.  

## <a name="story"></a>Historie  
Ellen, lagerlederen hos CRONUS, konfigurerer lagerstedet SØLV til grundlæggende håndtering af pluk, hvor lagermedarbejdere kan behandle udgående ordrer enkeltvis. Susan, ordrebehandleren, opretter en salgsordre for 30 enheder af varen LS-81, der skal sendes til debitor 10000 på lagerstedet SØLV. John, som arbejder på lageret, skal sørge for, at forsendelsen klargøres og leveres til debitoren. John administrerer alle involverede opgaver på siden **Pluk (lager)**, som automatisk peger på de placeringer, hvor LS-81 opbevares.  

## <a name="setting-up-the-location"></a>Indstilling af lokation  
Opsætningen af siden **Lokationskort** definerer flows i virksomheden.  

### <a name="to-set-up-the-location"></a>Sådan oprettes lokationen  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lokationer**, og vælg derefter det relaterede link.  
2.  Åbn lokationskortet SØLV.  
3.  Markér afkrydsningsfeltet **Kræv pluk**.  

## <a name="creating-the-sales-order"></a>Oprettelse af salgsordren  
Salgsordrer er den mest almindelige type udgående kildedokument.  

### <a name="to-create-the-sales-order"></a>Sådan oprettes salgsordren  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordrer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Opret en salgsordre for debitor 10000 på arbejdsdatoen (23. januar) med følgende salgsordrelinje.  

    |Vare|Lokationskode|Antal|  
    |----------|-------------------|--------------|  
    |LS_81|SØLV|30|  

     Fortsæt ved at meddele lageret, at salgsordren er klar til lagerekspedition.  

4.  Vælg handlingen **Frigivelse**.  

    John fortsætter ved at vælge og sende de solgte varer.  

## <a name="picking-and-shipping-items"></a>Sådan plukkes og leveres varer  
På siden **Pluk (lager)** kan du administrere alle udgående lageraktiviteter til et specifikt kildedokument såsom en salgsordre.  

### <a name="to-pick-and-ship-items"></a>Sådan foretages pluk og levering af varer  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Pluk (lager)**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Vælg feltet **Kildedokument**, og vælg derefter **Salgsordre**.  
4.  Vælg feltet **Kildenr.**, vælg linjen for salget til debitor 10000, og vælg knappen **OK**.  

    Du kan også vælge handlingen **Hent kildedokument** og derefter vælge salgsordren.  
5.  Vælg handlingen **Autofyld håndteringsantal**.  

    Du kan også indtaste henholdsvis 10 og 30 på de to lagerpluklinjer i feltet **Håndteringsantal**.  
6.  Vælg handlingen **Bogfør**, vælg **Lever**, og vælg derefter knappen **OK**.  

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
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
