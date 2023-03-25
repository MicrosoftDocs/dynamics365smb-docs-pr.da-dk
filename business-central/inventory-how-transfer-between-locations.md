---
title: Overføre varer mellem lagerlokationer
description: 'Lær, hvordan du flytter lager fra ét sted eller lagersted til et andet enten med omposteringskladden eller overflytningsordrer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
---
# Overflytte lagerbeholdning mellem lokationer

Du kan overføre lagervarer mellem lokationer ved at oprette overflytningsordrer. Du kan også bruge vareomposteringskladden.

> [!NOTE]
> Hvis du vil overflytte varer, skal lokationer og overflytningsruter oprettes. Du kan få mere at vide om opsætning af lokationer ved at gå til  [Lokationsopsætning](inventory-how-setup-locations.md). Du kan ikke bruge overflytningsordrer på *tomme* lokationer.

## Overflytningsordrer

Du kan levere den udgående overflytning fra én placering og modtage en indgående overflytning på destinationen. Du kan:

* Spore et antal i transit
* Definere kalendere, ruter og indgående og udgående tid til datoberegning og planlægning. Flere oplysninger om planlægning i [Om planlægningsfunktionen](production-about-planning-functionality.md).
* Brug forskellige lagerfunktioner for indgående og udgående lokationer.
* Du kan med nogle begrænsninger bruge overflytningsordrer til direkte overførsler.

## Vareomposteringskladder

* Enkel, direkte overførsel af varer mellem lokationer.
* Flytte varer mellem placeringer. Hvis du vil vide mere om overflytning af varer mellem placeringer, skal du gå til [Flyt varer, der ikke er planlagt i basislagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Ændre et lot-eller serienummer til et nyt lot-eller serienummer. Hvis du vil vide mere om genklassificering af serie-og lotnumre, skal du gå til [Ompostere serie-eller lotnumre](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Ændre udløbsdatoen til en ny dato.
* Ompostere varer fra en *tom* lokation til en aktuel placering.
* Lageraktiviteter administreres ikke. Lagerposterne bliver oprettet.

## Såden overflyttes varer med en overflytningsordre

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **overflytningsordrer**, og vælg derefter det relaterede link.
2. På siden **Overflytningsordre** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Hvis du har udfyldt felterne **Transitkode**, **Speditørkode** og **Speditørservice** på siden **Overflytningsrutespec.**, udfyldes de tilsvarende felter på overflytningsordren automatisk, når du opretter overflytningsruten.

    Når du udfylder feltet **Speditørservice** beregnes modtagelsesdatoen på den lokation, der overflyttes til, ved at lægge speditørens transporttid til afsendelsesdatoen.

3. Du udfylder linjerne ved enten at angive dem manuelt eller ved at vælge en af følgende indstillinger under handlingen **Funktioner**:

    * Vælg handlingen **Hent placeringsindhold** for at vælge eksisterende varer fra en bestemt placering på lokationen.
    * Vælg **Hent købsleverancelinjer** for at vælge varer, der lige er ankommet på den lokation, der overflyttes fra.

    Fortsæt med at levere varerne som lagermedarbejder på den lokation, der overflyttes fra.
4. Vælg handlingen **Bogfør**, vælg indstillingen **Lever**, og vælg derefter knappen **OK**.

    Varerne er nu i transit mellem de angivne lokationer i overensstemmelse med den angivne overflytningsrute.

    Fortsæt ved at modtage varerne som lagermedarbejder på den lokation, der overflyttes fra. Overflytningsordrelinjerne er de samme som ved levering og kan ikke redigeres.
5. Vælg handlingen **Bogfør**, vælg indstillingen **Modtag**, og vælg derefter knappen **OK**.

## Sådan overflyttes varer i vareomposteringskladden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vareomposteringskladder**, og vælg derefter det relaterede link.
2. På siden **Vareomposteringskladder** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I feltet **Lokationskode** skal du indtaste den lokation, hvor varerne opbevares i øjeblikket.

    > [!NOTE]  
    > For at overflytte varer, der ikke har en lokationskode, skal du lade feltet **Lokationskode** stå tomt.
4. I feltet **Ny lokationskode** skal du angive den lokation, som du vil overflytte varerne til.
5. Vælg handlingen **Bogfør**.

## Se relateret [Microsoft-træning](/training/modules/transfer-items/)

## Se også

[Administrere lager](inventory-manage-inventory.md)  
[Opsætte lokationer](inventory-how-setup-locations.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
