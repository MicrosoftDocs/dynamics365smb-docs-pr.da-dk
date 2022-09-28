---
title: Afsende varer
description: Denne artikel beskriver, hvordan du leverer varer fra lagerstedet afhængigt af lager konfigurationen af leverancen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7335, 7337, 7339, 7340, 7341, 7362, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: b66a0a0a4cad12c4f41c53569b0007c51e846de7
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531211"
---
# <a name="ship-items"></a>Afsende varer

Når du leverer varer fra et lagersted, der ikke er konfigureret til lagerleverancebehandling, skal du blot registrere leverancen på det relaterede forretningsbilag f.eks. en salgsordre, serviceordre, købsordre, returvareordre eller udgående overflytningsordre.

Når du leverer varer fra et lagersted, der er konfigureret til lagerleverance, kan du kun levere varer på baggrund af kildedokumenter, som andre virksomheder har frigivet til lagerstedet.

> [!NOTE]
> Hvis der benyttes direkte afsendelse og placeringer på lageret, kan du for hver linje få vist, hvor mange varer der er blevet placeret på de direkte afsendelsesplaceringer. Disse varemængder beregnes automatisk, hver gang felterne på leverancen opdateres. Hvis de pågældende varer også er dem, som er relevante for den leverance, som du er i gang med, kan du oprette et pluk til alle linjerne og derefter færdiggøre leverancen. Flere oplysninger i [Afsende varer direkte](warehouse-how-to-cross-dock-items.md).

## <a name="ship-items-with-a-sales-order"></a>Levere varer med en salgsordre

Følgende vejledning beskriver, hvordan du leverer varer fra en salgsordre. Der er tilsvarende fremgangsmåde for købsreturvareordrer, serviceordrer og udgående overflytningsordrer.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.
2. Åbn en eksisterende salgsordre eller opret en ny. Flere oplysninger i [Salg-produkter](sales-how-sell-products.md).
3. Angiv det leverede antal i feltet **Lever (antal)**.

    Værdien i feltet **Leveret antal** opdateres. Hvis det er en delvis leverance, er værdien lavere end værdien i feltet **Antal**. Flere oplysninger i [Behandle delleverancer](sales-how-send-partial-shipments.md).
4. Vælg handlingen **Bogfør**.

> [!NOTE]
> Hvis din organisation ikke bruger salgsordrer, antager [!INCLUDE [prod_short](includes/prod_short.md)], at du har leveret det fulde antal, når du bogfører salgsfakturaen. Hvis dette strider mod den måde, din organisation arbejder på, anbefales du at bruge salgsordrer og bogføre leverancer som forklaret i denne artikel.

## <a name="ship-items-with-a-warehouse-shipment"></a>Levere varer med en lagerleverance

Først skal du oprette et leverancedokument fra et virksomhedskildedokument. Derefter skal du vælge de angivne varer til leverancen.

### <a name="create-a-warehouse-shipment"></a>Oprette en lagerleverance

Medarbejderen, der er ansvarlig for leverancen, opretter typisk en lagerleverance. Følgende fremgangsmåde beskriver, hvordan du opretter forsendelsen manuelt i standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)]. Organisationen kan imidlertid have en automatiseret del af processen, f. eks. via brug af håndholdte eller tilsluttede scannere, der understøttes af eksterne providere.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerleverancer**, og vælg derefter det relaterede link.  
2. Vælg **Ny**.  

    Udfyld felterne i oversigtspanelet **Generelt**. Når du henter kildedokumentlinjer, kopieres nogle af oplysningerne fra hovedet til hver linje.  

    I forbindelse med lager konfigureret med styret læg-på-lager og pluk: Hvis der på lokationen er en standardzone og -placering til leverancer, udfyldes felterne **Zonekode** og **Placeringskode** automatisk, men du kan ændre dem efter behov.  

    > [!NOTE]  
    > Hvis du vil levere varer med en anden lagerklassekode end placeringens klassekode i feltet **Placeringskode** i dokumenthovedet, skal du slette indholdet i feltet **Placeringskode** i hovedet, inden du henter kildedokumentlinjerne for varerne.  
3. Vælg handlingen **Hent kildedokumenter**. Siden **Kildedokumenter** åbnes.

    Fra en ny eller en åben lagerleverance kan du bruge siden **Filtre til at hente kildedok.** til at hente de frigivne kildedokumentlinjer, der definerer, hvilke varer der skal leveres.

    1. Vælg handlingen **Brug filtre til at hente kildedok.**.  
    2. Hvis du vil oprette et nyt filter, skal du indtaste en beskrivende kode i feltet **Kode** og derefter vælge handlingen **Ret**.  
    3. Definer den type kildedokumentlinjer, som du ønsker at hente, ved at udfylde de relevante filterfelter.  
    4. Vælg handlingen **Kør**.  

    Alle frigivne kildedokumentlinjer, som opfylder filterkriterierne, indsættes nu på siden **Lagerleverance**, hvorfra du har aktiveret filterfunktionen.  

    De filterkombinationer, du definerer, gemmes på siden **Filtre til at hente kildedok.**, indtil næste gang du skal bruge dem. Du kan oprette et ubegrænset antal filterkombinationer. Du kan til enhver tid ændre kriterierne ved at vælge handlingen **Ret**.

4. Vælg de kildedokumenter, som du vil levere varer fra, og vælg derefter knappen **OK**.  

Linjerne fra kildedokumentet vises på siden **Lagerleverance**. Feltet **Lever (antal)** er på forhånd udfyldt med det udestående antal varer for hver linje, men du kan ændre antallet efter behov. Hvis du slettede indholdet i feltet **Placeringskode** i oversigtspanelet **Generelt**, inden du hentede linjerne, skal du udfylde alle modtagelseslinjer med den rette leverancekode.  

> [!NOTE]  
> Du kan ikke levere flere varer end antallet i feltet **Antal udestående** på kildedokumentlinjen. Hvis du vil levere flere varer, skal du hente et andet kildedokument, der indeholder en linje for varen ved hjælp af filterfunktionen.  

Når du har de linjer, som du vil levere, kan du starte den proces, som fører til, at linjerne sendes til de lagermedarbejdere, der skal plukkes.

### <a name="pick-and-ship"></a>Pluk og levering

Typisk opretter en lagermedarbejder, der er ansvarlig for pluk, et plukdokument og åbner et allerede oprettet plukdokument.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerleverancer**, og vælg derefter det relaterede link.
2. Vælg den lagerleverance, som du vil plukke til, og vælg derefter handlingen **Opret pluk**.
3. Udfyld felterne på anmodningssiden, og vælg derefter den knappen **OK**. Det angivne lagerplukdokument oprettes.

    Du kan også åbne et eksisterende lagerpluk-dokument.
4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk**, og vælg derefter det relaterede link. Vælg det lagerpluk, du vil arbejde på.

    Hvis lagerstedet kræver brug af placeringer, er pluklinjerne ændret til Hent og Placer-handlingslinjer.

    Du kan sortere linjerne, tildele plukket til en medarbejder, angive et nedbrydningsfilter, hvis du benytter styret læg-på-lager og pluk og udskrive plukinstruktionerne.

5. Foretag det faktiske pluk af varerne, og placer dem på den angivne leveranceplacering eller i leveranceområdet, hvis der ikke benyttes placeringer.
6. Vælg handlingen **Registrer pluk**.

    Felterne **Lever (antal)** og **Bilagsstatus** på leverancedokumentets hoved er opdateret. De varer, som du har plukket, er ikke længere disponible til pluk til andre leverancer eller til interne operationer.
7. Udskriv leverancedokumenterne, foretag indpakningen, og bogfør derefter leverancen.

Flere oplysninger om plukning til lagerleverancer i [Plukke varer til lagerleverance](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Du kan også bruge plukkladden til at samle flere forskellige plukinstruktioner i en enkelt instruktion (til flere leverancer) og på den måde foretage plukkene på lagerstedet mere effektivt. Flere oplysninger i [Planlægning af pluk i kladder](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Hvis du venter på, at bestemte varer skal ankomme på lagerstedet, og du bruger direkte afsendelsesfunktioner, beregner [!INCLUDE[prod_short](includes/prod_short.md)] mængden af varer i den direkte afsendelsesplacering på hver leverance eller kladdelinje det antal af varen. Feltet opdateres, hver gang du lukker eller åbner leverancedokumentet eller kladden. Flere oplysninger i [Afsende varer direkte](warehouse-how-to-cross-dock-items.md).

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/ship-invoice-items-dynamics-365-business-central/).

## <a name="see-also"></a>Se også

[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
