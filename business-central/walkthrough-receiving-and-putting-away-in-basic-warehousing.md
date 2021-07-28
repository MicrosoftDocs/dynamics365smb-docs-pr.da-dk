---
title: Gennemgang - Modtagelse og placering på lager i grundlæggende lageropsætninger
description: I Business Central kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c5d3ce9b7bb02c12da8d62413c6c5722c59ee1d8
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439306"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Gennemgang: Modtagelse og placering på lager i grundlæggende lageropsætninger

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

I [!INCLUDE[prod_short](includes/prod_short.md)] kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.  

|Metode|Indgående proces|Placering|Modtagelser|Læg-på-lager-aktiviteter|Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|T|Bogfør lagermodtagelse og læg-på-lager fra ordrelinjen|X|||2|  
|B|Bogfør lagermodtagelse og læg-på-lager fra et læg-på-lager-dokument|||X|3|  
|L|Bogfør lagermodtagelse og læg-på-lager fra et lagermodtagelsesdokument||X||5-4-6|  
|D|Bogfør modtagelse fra et lagermodtagelsesdokument, og bogfør læg-på-lager fra lagerets læg-på-lager-dokument||X|X|5-4-6|  

Du kan finde flere oplysninger i [Designoplysninger: Indgående lagerflow](design-details-inbound-warehouse-flow.md)  

Den følgende gennemgang viser metode B i forrige tabel.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
I grundlæggende lageropsætninger, hvor lokationen, du vil plukke fra, er sat op til at kræve læg-på-lager men ikke modtagelse, bruges siden **Læg-på-lager** til at registrere og bogføre læg-på-lager- og modtagelsesoplysninger for de indgående kildedokumenterne. Det indgående kildedokument kan være en købsordre, en salgsreturvareordre, en indgående overflytningsordre eller en produktionsordre med afgang, der er klar til at blive lagt på lager.

> [!NOTE]
> Selv om indstillingerne kaldes **Kræv pluk** og **Kræv læg-på-lager**, kan du bogføre modtagelser og leverancer direkte fra kildeforretningsdokumenterne på lokationer, hvor du kan markerer disse afkrydsningsfelter.  

Denne gennemgang viser følgende opgaver.  

-   Indstilling af SØLV-lokation til læg-på-lager-aktiviteter.  
-   Indstilling af SØLV-lokation til placeringshåndtering.  
-   Definition af en standardplacering for varen LS-81. (LS-75 er allerede oprettet i CRONUS).  
-   Oprettelse af en købsordre for kreditor 10000 til 40 højttalere.  
-   Kontrol af, at lagerplaceringerne er forudindstillet af opsætningen.  
-   Frigivelse af købsordren til lagerekspedition.  
-   Oprettelse af en læg-på-lager-aktivitet baseret på et frigivet kildedokumentet.  
-   Kontrol af, at lagerplaceringerne er overført fra købsordren.  
-   Registrering af lagerbevægelsen til lageret og på samme tid bogføring af købsmodtagelsen til kildekøbsordren.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a>Roller  
Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:  

-   Lagerchef  
-   Indkøbsagent  
-   Lagermedarbejder  

## <a name="prerequisites"></a>Forudsætninger  
For at gennemføre denne gennemgang skal du:  

-   CRONUS Danmark A/S være installeret.  
-   Du kan oprette dig selv som lagermedarbejder på lokationen SØLV ved at følge disse trin:  

    1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
    2.  Vælg feltet **Bruger-id**, og vælg din egen brugerkonto på siden **Brugere**.  
    3.  Angiv SØLV i feltet **Lokationskode**.  
    4.  Markér feltet **Standard**.  

## <a name="story"></a>Historie  
Ellen, som er indkøbschef hos CRONUS Danmark A/S, opretter en købsordre til 10 enheder af varen LS-75 og 30 enheder af varen LS-81 fra kreditoren 10000 til afsendelse til lagerstedet SØLV. Når leveringen ankommer på lagerstedet, sætter John, som er lagerarbejder, varerne på lager på standardplaceringer, der er defineret for varerne. Når John bogfører placeringen på lager, bogføres varerne som modtaget på lageret og tilgængelige til salg eller andre behov.  

## <a name="setting-up-the-location"></a>Indstilling af lokation  
 Opsætningen af siden **Lokationskort** definerer flows i virksomheden.  

### <a name="to-set-up-the-location"></a>Sådan oprettes lokationen  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.  
2.  Åbn lokationskortet SØLV.  
3.  Markér afkrydsningsfeltet **Kræv læg-på-lager**.  

    Fortsæt ved at oprette en standardplacering for de to varenumre for at kontrollere, hvor de lægges på lager.  

4.  Vælg handlingen **Placeringer**.  
5.  Vælg den første række, til placering S-01-0001, og vælg derefter handlingen **Indhold**.  

    Bemærk på siden **Placeringsindhold**, at vare LS-75 allerede er oprettet som indhold på placering S-01-0001.  

6.  Vælg handlingen **Ny**.  
7.  Vælg felterne **Fast** og **Standard**.  
8.  Skriv LS-81 i feltet **Bilagsnr.**.  

## <a name="creating-the-purchase-order"></a>Oprettelse af købsordren  
Købsordrer er den mest almindelige type indgående kildedokument.  

### <a name="to-create-the-purchase-order"></a>Hvis du vil oprette købsordren  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Opret en købsordre for kreditor 10000 på arbejdsdatoen (23. januar) med følgende købsordrelinjer.  

    |Vare|Lokationskode|Placeringskode|Antal|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|SØLV|S-01-0001|10|  
    |LS-81|SØLV|S-01-0001|30|  

    > [!NOTE]  
    >  Placeringskoden angives automatisk i overensstemmelse med opsætningen, som du har foretaget i afsnittet "Indstilling af lokation".  

    Fortsæt ved at meddele lageret, at købsordren er klar til lagerekspedition, når leverancen ankommer.  

4.  Vælg handlingen **Frigivelse**.  

    Leverancen af højttalere fra kreditor 10000 er modtaget på SØLV-lageret, og John fortsætter med at lægge dem på plads.  

## <a name="receiving-and-putting-the-items-away"></a>Modtagelse og placering af varer på lager  
På siden **Læg-på-lager** kan du administrere alle indgående lageraktiviteter til et specifikt kildedokument, f.eks. en købsordre.  

### <a name="to-receive-and-put-the-items-away"></a>Sådan modtager du varerne og lægger dem på lager  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Læg-på-lager-aktiviteter**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Vælg feltet **Kildedokument**, og vælg derefter **Købsordre**.  
4.  Vælg feltet **Kildenr.**, vælg linjen til købet fra kreditor 10000, og vælg knappen **OK**.  

    Du kan også vælge handlingen **Hent kildedokument** og derefter vælge købsordren.  

5.  Vælg handlingen **Autofyld håndteringsantal**.  

    Du kan også indtaste henholdsvis 10 og 30 på de to læg-på-lager-linjer i feltet **Håndteringsantal**.  

6.  Vælg handlingen **Bogfør**, vælg handlingen **Modtag**, og vælg derefter knappen **OK**.  

    De 40 højttalere er nu registreret som lagt på lager på placering S-01-0001, og der oprettes en positiv varepost, der afspejler den bogførte købsmodtagelse.  

## <a name="see-also"></a>Se også  
 [Lægge varer på lager med Læg-på-lager (lager)](warehouse-how-to-put-items-away-with-inventory-put-aways.md)   
 [Oprette grundlæggende lagersteder med handlingsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md)   
 [Flytte varer ad hoc i grundlæggende lageropsætninger](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Designoplysninger: Indgående lagerflow](design-details-inbound-warehouse-flow.md)   
 [Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]