---
title: Overføre varer mellem lagerlokationer
description: 'Lær, hvordan du flytter lager fra ét sted eller lagersted til et andet enten med omposteringskladden eller overflytningsordrer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
ms.service: dynamics-365-business-central
---

# <a name="transfer-inventory-between-locations"></a>Overflytte lager mellem lokationer

Du kan overføre lagervarer mellem lokationer ved at oprette overflytningsordrer. Du kan også bruge vareomposteringskladden.

> [!NOTE]
> Hvis du vil overflytte varer, skal lokationer og overflytningsruter oprettes. Du kan få mere at vide om konfiguration af lokationer ved at gå til [Konfigurere lokationer](inventory-how-setup-locations.md). Du kan ikke bruge overflytningsordrer på *tomme* lokationer.

## <a name="transfer-orders"></a>Overflytningsordrer

Du kan levere den udgående overflytning fra én placering og modtage en indgående overflytning på destinationen. Du kan:

* Spore et antal i transit.
* Definere kalendere, ruter og indgående og udgående tid til datoberegning og planlægning. Flere oplysninger om planlægning i [Om planlægningsfunktionen](production-about-planning-functionality.md).
* Brug forskellige lagerfunktioner for indgående og udgående lokationer.
* Brug overflytningsordrer til direkte overførsler med nogle begrænsninger.

## <a name="item-reclassification-journals"></a>Vareomposteringskladder

Du kan også bruge siden **Vareomposteringskladden** til at:

* Direkte overførsel af varer mellem lokationer.
* Flytte varer mellem placeringer Du kan få mere at vide om overflytning af varer mellem placeringer ved at gå til [Flyt varer, der ikke er planlagt, i Grundlæggende lagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).
* Ændre et lot-eller serienummer til et nyt lot-eller serienummer. Hvis du vil vide mere om genklassificering af serie-og lotnumre, skal du gå til [Ompostere serie-eller lotnumre](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Ændre udløbsdatoen til en ny dato.
* Ompostere varer fra en tom lokation til en aktuel placering.
* Oprette lagerposter, hvis du ikke administrerer lageraktiviteter.

## <a name="to-transfer-items-with-a-transfer-order"></a>Såden overflyttes varer med en overflytningsordre

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **overflytningsordrer**, og vælg derefter det relaterede link.
2. På siden **Overflytningsordre** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hvis du har udfyldt felterne **Transitkode**, **Speditørkode** og **Speditørservice** på siden **Overflytningsrutespec.**, udfyldes de tilsvarende felter på overflytningsordren automatisk, når du opretter overflytningsruten.

    Når du udfylder feltet **Speditørservice** beregnes modtagelsesdatoen på den lokation, der overflyttes til, ved at lægge speditørens transporttid til afsendelsesdatoen.

3. Der er flere måder at udfylde linjerne på:

    |Indstilling  |Beskrivlse  |
    |---------|---------|
    |Manuelt     | Udfyld en linje for en vare i oversigtspanelet **linjer**, eller brug handlingen **Vælg varer** for at vælge flere varer.        |
    |Automatisk     | * Vælg handlingen **Hent placeringsindhold** for at vælge eksisterende varer fra en bestemt placering på lokationen.<br><br>* Vælg **Hent købsleverancelinjer** for at vælge varer, der lige er ankommet på den lokation, der overflyttes fra.        |

    Du kan nu levere varerne.
4. Vælg handlingen **Bogfør**, vælg indstillingen **Lever**, og vælg derefter knappen **OK**.

    Varerne er nu i transit mellem de angivne lokationer i overensstemmelse til overflytningsruten.

    Fortsæt ved at modtage varerne som lagermedarbejder på den lokation, der overflyttes fra. Overflytningsordrelinjerne er de samme som ved levering og kan ikke redigeres.
5. Vælg handlingen **Bogfør**, vælg indstillingen **Modtag**, og vælg derefter knappen **OK**.

### <a name="undo-a-transfer-shipment"></a>Fortryde en overførselslevering

Hvis du finder en fejl i et antal på en bogført overflytningsordre, så længe leverancen ikke modtages, kan du nemt rette antallet.  **På siden Bogført overflytningsleverance** oprettes der rettelseslinjer ved hjælp af **handlingen Annuller leverance** på følgende måde:

* Værdien i feltet **Antal leveret** faldt med det antal, du har annulleret.
* Værdien i feltet **Antal leveret** steg ifølge det antal, du har annulleret.
* Afkrydsningsfeltet **Rettelse** markeres for linjerne.

Hvis antallet er leveret i en lagerleverance, oprettes der en rettelseslinje i den bogførte lagerleverance.

Hvis du vil fuldføre rettelsen, skal du åbne overflytningsordren igen, angive det korrekte antal og derefter bogføre ordren. Hvis du bruger en lagerleverance til levering af ordren, skal du oprette og bogføre en ny lagerleverance.

### <a name="post-multiple-transfer-orders-in-a-batch"></a>Bogføre flere overflytningsordrer i en batch

Følgende procedure beskriver, hvordan du kan bogføre flere købsordrer samlet.

1. 1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **overflytningsordrer**, og vælg derefter det relaterede link.  
2. Vælg de ordrer, der skal bogføres på, på siden **overførselsordrer**.
3. I feltet **Nummer** Skal du åbne genvejsmenuen og vælge **Vælg flere**.
4. Marker linjerne for de placeringer, du vil slette.
5. Vælg handlingen **Bogfør**, og vælg **derefter Massebogfør**.
6. På siden **Masseoverføre overflytningsordre** skal du udfylde felterne efter behov.

   > [!TIP]
    > I forbindelse med overflytningsordrer kan du enten vælge **Send** eller **Modtag**. Gentag dette trin, hvis du har brug for begge dele. For ordrer, hvor **Direkte bogføring** er aktiveret, fungerer begge indstillinger på samme måde, og ordren bogføres fuldstændigt.

7. Vælg **OK**.
8. Hvis du vil have vist potentielle problemer, skal du åbne siden **Registrering af fejlmeddelelser**.

    > [!NOTE]
    > Det kan tage noget tid at bogføre flere dokumenter, og andre brugere vil blive blokeret. Overvej at aktivere baggrundsbogføring. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](/dynamics365/business-central/admin-job-queues-schedule-tasks).

### <a name="schedule-a-job-queue-entry-to-post-multiple-documents-in-a-batch"></a>Planlægge en opgavekøpost for at bogføre flere dokumenter i en batch

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

### <a name="comparison-of-different-settings-for-transfer-orders"></a>Sammenligning af forskellige indstillinger for overflytningsordrer

Du kan bogføre overflytningsordrer i forskellige transportformer med eller uden en transitlokation. Deaktiver til/fra-knappen Direkte overførsel, og vælg den midlertidige placering i feltet **Transitkode** på siden **Overflytningsordre** . **·**  Når du bogfører leverancen af en overflytningsordre, der bruger transitlokationen, er varerne på linjen ikke længere tilgængelige på en af lokationerne, fordi de er i transit. Direkte bogføring sikrer, at der ikke bruges et transitsted, og at forsendelses- og modtagelsesprocessen behandles samtidigt. Den nøjagtige funktionsmåde for direkte bogføring kan være forskellig baseret på den værdi, der er valgt i **feltet Bogføring** af direkte overførsler på **siden Lageropsætning** .

I følgende tabel beskrives, hvordan kombinationerne adskiller sig.

|Kapacitet|Feltet **Direkte overførsel** er deaktiveret på siden **Overflytningsordre** |**Direkte overførsel** er aktiveret på siden **Overflytningsordre** </br>**Bogføring** af direkte overførsler er angivet til **Direkte overførsel** på **siden Lageropsætning** |**Direkte overførsel** er aktiveret på siden **Overflytningsordre** </br>**Bogføring** af direkte overførsler er angivet til **Modtagelse og levering** på **siden Lageropsætning** |
|---|---|---|---|
|Brug transitlokation|Ja|Nr.|Nr.|
|Kan bogføre modtagelse uden levering.</br>Kan bruge **Annuller modtagelse**.|Ja|Nr.|Nr.|
|Delvis bogføring|Ja|Nr.|Ja|
|Vareposter|4:</br>Overførsel fra fra-placering,</br>Overførsel til transit,</br>Overførsel fra transit,</br>Overfør til Til-Lokation.|2:</br>Overførsel fra fra-placering,</br>Overfør til Til-Lokation.|4:</br>Overførsel fra fra-placering,</br>Overfør til *tom,*</br>Overfør fra *tom,*</br>Overfør til Til-Lokation.|
|Bogførte dokumenter|Bogført overflytningsleverance,</br>Bogført overførselskvittering.|Bogført direkte overførsel|Bogført overflytningsleverance,</br>Bogført overførselskvittering.|
|Reservation: ind- og udgående|Ja|Ja|Ja|
|Varegebyrer - tildeles til bogført overflytningskvittering|Ja|Nr.|Ja|
|Lagerhåndtering|Fuld|Nr.|Begrænset, se nedenfor|

Lagerhåndteringsmatrix til konfiguration:Direkte overførsel **er aktiveret på siden Overflytningsordre**  **,**  og **Direkte overflytningsbogføring er angivet til** Direkte **overførsel** på **siden Lageropsætning** .

|Fra \ Til|Til: Ingen lagerhåndtering|Til: Lagermodtagelse|Til: Læg-på-lager (lager)|Til: Styret læg-på-lager og pluk|
|-|-|-|-|-|
|**Fra: Ingen lagerhåndtering**|1|Ikke understøttet|1, 4|Ikke understøttet|
|**Fra: Lagerleverance**|1, 2|Ikke understøttet|1,2,4|Ikke understøttet|
|**Fra: Læg-på-lager (lager)**|1, 3|Ikke understøttet|1,3,4|Ikke understøttet|
|**Fra: Styret læg-på-lager og pluk**|2|Ikke understøttet|2|Ikke understøttet|

Tallene i cellerne viser de bogføringsindstillinger, der understøttes.

1. Bogfør fra overflytningsordre. For nogle kombinationer skal du muligvis udfylde feltet **Lever** (antal).
2. Oprette og bogføre en lagerleverance.
3. Opret og bogfør et lagerpluk.
4. Oprette og bogføre en læg-på-lager-aktivitet. For nogle kombinationer skal du muligvis udfylde feltet **Lever** (antal).

Uanset metoden udføres forsendelses- og modtagelsestransaktionerne. Du kan f.eks. oprette en overflytningsordre fra en lokation, der kræver pluk fra lager, til en lokation, der kræver læg-på-lager. Du kan oprette og bogføre læg-på-lager, og både leverance- og modtagelsestransaktioner oprettes. Du kan også bogføre sådanne dokumenter fra en overflytningsordre eller fra et lagerpluk.  

Du kan finde flere oplysninger om lagerstedshåndtering i [Oversigt](design-details-warehouse-management.md) over lagerstedsstyring.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Sådan overflyttes varer i vareomposteringskladden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vareomposteringskladder**, og vælg derefter det relaterede link.
2. På siden **Vareomposteringskladder** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I feltet **Lokationskode** skal du indtaste den lokation, hvor varerne opbevares i øjeblikket.

    > [!NOTE]  
    > For at overflytte varer, der ikke har en lokationskode, skal du lade feltet **Lokationskode** stå tomt.
4. I feltet **Ny lokationskode** skal du angive den lokation, som du vil overflytte varerne til.
5. Vælg handlingen **Bogfør**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]


## <a name="see-also"></a>Se også

[Administrere lager](inventory-manage-inventory.md)  
[Konfigurere lokationer](inventory-how-setup-locations.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
