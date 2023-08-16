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

3. Der er flere måder at udfylde linjerne på:

    |Indstilling  |Beskrivlse  |
    |---------|---------|
    |Manuelt     | Udfyld en linje for en vare i oversigtspanelet **linjer**, eller brug handlingen **Vælg varer** for at vælge flere varer.        |
    |Automatisk     | * Vælg handlingen **Hent placeringsindhold** for at vælge eksisterende varer fra en bestemt placering på lokationen.<br><br>* Vælg **Hent købsleverancelinjer** for at vælge varer, der lige er ankommet på den lokation, der overflyttes fra.        |

    Du kan nu levere varerne.
4. Vælg handlingen **Bogfør**, vælg indstillingen **Lever**, og vælg derefter knappen **OK**.

    Varerne er nu i transit mellem de angivne lokationer i overensstemmelse med den angivne overflytningsrute.

    Fortsæt ved at modtage varerne som lagermedarbejder på den lokation, der overflyttes fra. Overflytningsordrelinjerne er de samme som ved levering og kan ikke redigeres.
5. Vælg handlingen **Bogfør**, vælg indstillingen **Modtag**, og vælg derefter knappen **OK**.

### Bogføre flere overflytningsordrer i en batch

Følgende procedure beskriver, hvordan du kan bogføre flere købsordrer samlet.

1. 1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **overflytningsordrer**, og vælg derefter det relaterede link.  
2. Vælg de ordrer, der skal bogføres på, på siden **overførselsordrer**.
3. I feltet **Nummer** Skal du åbne genvejsmenuen og vælge **Vælg flere**.
4. Marker linjerne for de placeringer, du vil slette.
5. Vælg handlingen **Bogføring**, og vælg derefter handlingen **Massebogfør**.
6. På siden **Masseoverføre overflytningsordre** skal du udfylde felterne efter behov.

   > [!TIP]
    > I forbindelse med overflytningsordrer kan du enten vælge **Send** eller **Modtag**. Gentag dette trin, hvis du har brug for begge dele. For ordrer, hvor **Direkte bogføring** er aktiveret, fungerer begge indstillinger på samme måde, og ordren bogføres fuldstændigt.

7. Vælg **OK**.
8. Hvis du vil have vist potentielle problemer, skal du åbne siden **Registrering af fejlmeddelelser**.

    > [!NOTE]
    > Det kan tage noget tid at bogføre flere dokumenter, og andre brugere vil blive blokeret. Overvej at aktivere baggrundsbogføring. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](/dynamics365/business-central/admin-job-queues-schedule-tasks).

### Planlægge en opgavekøpost for at bogføre flere dokumenter i en batch

Alternativt kan du bruge opgavekøen til at planlægge bogføringen til at finde sted på et tidspunkt, der passer til din organisation. F.eks. giver det måske mening i din virksomhed at køre visse rutiner, når de fleste af dataindtastningerne for den pågældende dag er afsluttede.

Følgende procedure viser, hvordan du kan indstille rapporten **Massebogfør salgsordrer** til automatisk bogføring af direkte overførselsordrer kl. 16 på hverdage. Dette klokkeslæt er blot et eksempel. Fremgangsmåden er den samme for de andre dokumenter.  

1. Søg efter siden **Opgavekøposter**, og vælg det relevante link.  
2. Vælg handlingen **Ny**.  
3. I feltet **Objekttype, der skal aktiveres** skal du vælge **Rapport**.  
4. I feltet **Objekt-id, der skal køres** skal du vælge **5707, Massebogfør overførselsordrer**.
5. Marker **Siden Rapportanmodning**-afkrydsningsfeltet.
6. På anmodningssiden **Massebogfør overflytningsordrer** skal du vælge **leverings**-indstillingen, filtrere på **Direkte overførsel** og derefter vælge **OK**.

   > [!IMPORTANT]
   > Det er vigtigt at angive filtre. Ellers vil [!INCLUDE [prod_short](includes/prod_short.md)] bogføre alle dokumenterne, selvom de ikke er klar. Overvej at angive et filter på feltet **Status** for værdien **Frigivet** og et filter på feltet **Bogføringsdato** for værdien **..i dag**. Hvis du vil vide mere om filtre, skal du gå til [Sortering, søgning og filtrering](/dynamics365/business-central/ui-enter-criteria-filters).

7. Marker alle afkrydsningsfelter fra **Aktiver hver mandag** til **Aktiver hver fredag**.
8. I feltet **Starttidspunkt** skal du angive **kl. 16**.
9. Vælg handlingen **Angiv status til Klar**.

## Sådan overflyttes varer i vareomposteringskladden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vareomposteringskladder**, og vælg derefter det relaterede link.
2. På siden **Vareomposteringskladder** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I feltet **Lokationskode** skal du indtaste den lokation, hvor varerne opbevares i øjeblikket.

    > [!NOTE]  
    > For at overflytte varer, der ikke har en lokationskode, skal du lade feltet **Lokationskode** stå tomt.
4. I feltet **Ny lokationskode** skal du angive den lokation, som du vil overflytte varerne til.
5. Vælg handlingen **Bogfør**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Fortryde en overførselslevering

Hvis du finder en fejl i et antal på en bogført overflytningsordre, så længe leverancen ikke modtages, kan du nemt rette antallet. På siden **Bogføre overførselsleverance** opretter handlingen **Fortryde leverance** korrigerende linjer på følgende måde:

* Værdien i feltet **Antal leveret** faldt med det antal, du har annulleret.
* Værdien i feltet **Antal leveret** steg ifølge det antal, du har annulleret.
* Afkrydsningsfeltet **Rettelse** markeres for linjerne.

Hvis mængden blev leveret i en lagerleverance, oprettes en korrektionslinje i den bogførte lagerleverance.

Hvis du vil fuldføre rettelsen, skal du åbne overflytningsordren igen, angive det korrekte antal og derefter bogføre ordren. Hvis du bruger en lagerleverance til levering af ordren, skal du oprette og bogføre en ny lagerleverance.

## Se relateret [Microsoft-træning](/training/modules/transfer-items/)

## Se også

[Administrere lager](inventory-manage-inventory.md)  
[Opsætte lokationer](inventory-how-setup-locations.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
