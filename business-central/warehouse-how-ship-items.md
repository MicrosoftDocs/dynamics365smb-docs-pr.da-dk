---
title: Afsende varer
description: 'Denne artikel beskriver, hvordan du leverer varer fra lagerstedet.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---

# <a name="ship-items-with-a-warehouse-shipment" />Levere varer med en lagerleverance

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du modtage varer og indsætte dem på en af fire måder som beskrevet i følgende tabel.

|Metode|Udgående proces|Kræv pluk|Kræv leverance|Sværhedsgrad (få mere at vide på [Warehouse Management-oversigt](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bogfør pluk og leverance fra ordrelinjen|||Ingen dedikeret lageraktivitet.|  
|B|Bogfør pluk og leverance fra et lagerplukdokument|Aktiveret||Basis: Ordre for ordre.|  
|U|Bogfør pluk og leverance fra et lagerstedsleverancedokument||Aktiveret|Basis: Konsolideret modtagelse/levering for flere ordrer.|  
|D|Bogfør pluk fra et lagerstedsplukdokument, og bogfør leverance fra et lagerstedsleverancedokument|Aktiveret|Aktiveret|Avanceret|  

Hvis du vil vide mere om forsendelse af varer, skal du gå til [Udgående lagerflow](design-details-outbound-warehouse-flow.md).

Denne artikel henviser til metode C og D i den foregående tabel. I begge metoder skal du starte med at oprette et leverancedokument fra et virksomhedskildedokument. Derefter skal du vælge de angivne varer til leverancen.

Når en lokation kræver lagerleverancer, kan du levere varer på baggrund af kildedokumenter, der er frigivet til lagerstedet. Frigivelse af kildedokumenter gør varerne på dem klar til at blive ekspederet på lagerstedet. Der findes følgende eksempler på kildedokumenter:

* Salgsordrer
* Købsreturordrer
* Overflytningsordrer
* Serviceordrer

Du kan oprette en lagerleverance på en af to måder:

* I en push-metode, når der arbejdes på ordre til ordre-grundlag. Vælg **Opret lagerleverance**-handling i kildedokumentet for at oprette en lagerleverance for dokumentet.
* Når du bruger funktionen **Frigiv** i kildedokumentet til at frigive den til lageret. En lagerstedsmedarbejder opretter en **Lagerstedsmodtagelse** for en eller flere frigivne kildedokumenter. Følgende fremgangsmåde beskriver, hvordan du opretter en lagermodtagelse på en pull-måde.

## <a name="to-ship-items-using-a-warehouse-shipment-document" />Sådan leveres varer med et lagerleverancedokument

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerleverancer**, og vælg derefter det relaterede link.  
2. Vælg **Ny**.  
3. I feltet **Nummer** Skal du vælge den nummerserie, der skal bruges til at oprette et ID for forsendelsen.  
4. I feltet **Lokationskode** skal du vælge den lokation, du er ved at sende fra. 

    Når du henter kildedokumentlinjer, kopieres nogle af oplysningerne fra lokationen til hver linje.  
5. Udfyld feltet **Placeringskode** for en lokation, der kræver placeringer. Afhængigt af din opsætning kan [!INCLUDE[prod_short](includes/prod_short.md)]] tilføje placeringskode for dig. Få mere at vide på [zone-og placeringskoder](warehouse-how-ship-items.md#zone-and-bin-codes).  
6. Du kan hente kildedokument på to måder:

    * Vælg handlingen **Hent kildedokumenter**. Siden **Kildedokumenter - udgående** åbnes. Her kan du vælge et eller flere kildedokumenter, der er frigivet til lager, som kræver leverance.
    * Vælg handlingen **Brug filtre til at hente kildedok.**. Vinduet **Filtre til at hente kildedok.** åbnes. Her kan du vælge kildedokumentfilter og køre det. Alle frigivne kildedokumentlinjer, der overholder filterkriterierne, tilføjes på **lagerstedsmodtagelse**-siden. Flere oplysninger i [Sådan bruges filtre til at hente kildedokumenter](warehouse-how-ship-items.md#how-to-use-filters-to-get-source-documents).

    > [!NOTE]
    > Hvis der benyttes direkte afsendelse og placeringer på lageret, kan du for hver linje få vist, hvor mange varer der er blevet placeret på de direkte afsendelsesplaceringer. [!INCLUDE [prod_short](includes/prod_short.md)] beregner varemængder , hver gang felterne på leverancen opdateres. Hvis de pågældende varer også er dem, som er relevante for den leverance, som du er i gang med, kan du oprette et pluk til alle linjerne og derefter færdiggøre leverancen. Flere oplysninger i [Afsende varer direkte](warehouse-how-to-cross-dock-items.md).

7. Opret lagerstedspluk. Hvis lokationen kræver pluk, kan du oprette plukaktiviteter for lagerleverancer på en af to følgende måder:

    * På en push-måde, hvor du kan bruge handlingen **Opret pluk**. Marker de linjer, der skal plukkes, og angiv oplysninger om plukningerne. F.eks. hvilke placeringer, der skal tages fra, og hvor mange enheder der skal håndteres. Placeringerne kan være foruddefineret ved opsætning af lagerstedslokationen eller ressourcen.
    * På en push-måde, hvor du kan bruge handlingen **Frigiv**. På siden **Plukkladde** kan lagerstedsmedarbejderne bruge handlingen **Hent lagerstedsdokumenter** til at få tildelt de tildelte pluk. Når lagerstedspluk er fuldt tildelt, slettes linjerne i **Plukkladde**. Flere oplysninger i [Plukke varer til lagerleverance](warehouse-how-to-pick-items-for-warehouse-shipment.md).

    > [!TIP]
    > Du kan udskrive lagerleverancen og bruge den som en plukliste, hvis du vil have en lokation, der ikke kræver plukning.

8. Angiv det antal, der skal leveres.  

    For en lokation, der kræver plukning, opdateres feltet **Lever (antal)** automatisk, når plukket registreres. Feltet **Lever (antal)** er på forhånd udfyldt med det udestående antal varer for hver linje, men du kan ændre antallet efter behov.

    Du kan ændre antallet, men du kan ikke levere flere varer end antallet i feltet **Antal udestående** på kildedokumentlinjen eller i feltet **Antal plukket**, hvis der kræves plukning.

    Hvis du vil udfylde feltet **Lever (antal)** på alle linjer med nul, skal du vælge handlingen **Annuller Lever (antal)**. Du kan f. eks. angive, at mængderne skal være nul, hvis du bruger en stregkodescanner til at opdatere de leverede mængder. Hvis du vil tilføje det disponible antal til levering, skal du vælge handlingen **Autofyld Lever (antal)**.

9. Bogfør leverancen.

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

## <a name="how-to-use-filters-to-get-source-documents" />Sådan bruges filtre til at hente kildedokumenter

Fra en ny eller en åben lagerleverance kan du bruge siden **Filtre til at hente kildedok.** til at hente de frigivne kildedokumentlinjer, der definerer, hvilke varer der skal leveres.

1. Vælg handlingen **Brug filtre til at hente kildedok.**. 
2. Hvis du vil oprette et nyt filter, skal du indtaste en beskrivende kode i feltet **Kode** og derefter vælge handlingen **Ret**.

    Vinduet **Kildedokumentfilterkort - udgående** vises.

3. Brug filtre til at angive, hvilken type kildedokumentlinjer der skal hentes. Du kan f. eks. vælge typer af kildedokumenter, f. eks. salg- eller overflytningsordrer.
4. Vælg **Kør**.  

Alle frigivne kildedokumentlinjer, som opfylder filterkriterierne, indsættes nu på siden **Lagerleverance**, hvorfra du har aktiveret filterfunktionen.

Du kan oprette et ubegrænset antal filterkombinationer. De filterkombinationer, du definerer, gemmes på siden **Filtre til at hente kildedok.**, indtil næste gang du skal bruge dem. Du kan til enhver tid ændre kriterierne ved at vælge handlingen **Ret**.

## <a name="zone-and-bin-codes" />Zone-og placeringskoder

Hvis der er obligatoriske placeringer på lokationen, foreslår [!INCLUDE [prod_short](includes/prod_short.md)] en zone og Placeringskode i lagerleverancedokumentet.

* I forbindelse med avancerede konfigurationer, hvor en lokation bruger styret læg-på-lager og pluk, bruger [!INCLUDE [prod_short](includes/prod_short.md)] den placering, der er angivet i feltet **Lev. placeringskode** på **lokationskortet**. Hvis der ikke er angivet en **leveringsplaceringskode**, er feltet tomt. Hvis varen og leverancens placering ikke stemmer overens, bevarer [!INCLUDE [prod_short](includes/prod_short.md)] leveranceplaceringen.
* I andre tilfælde bruger [!INCLUDE [prod_short](includes/prod_short.md)] altid den placering, der er angivet i feltet **Overførselsplaceringskode** på **lokationskortet** først. I andre konfigurationer bruger [!INCLUDE [prod_short](includes/prod_short.md)] placeringskoden fra kildedokumentet.

## <a name="handling-assemble-to-order-items-in-warehouse-shipments" />Håndtering af montageordrevarer i lagerleverancer

I montageordrescenarier bruges feltet **Lever (antal)** på lagerleverancelinjerne til at registrere, hvor mange enheder der monteres. Den angivne mængde bogføres derefter som montageoutput, når er bogført lagerleverance. For andre lagerleverancelinjer er værdien i feltet **Lever (antal)** nul fra start.

Når medarbejdere, der er ansvarlige for montering, afslutter monteringsdele eller montage til ordre-mængde, registrerer de det i feltet **Levér antal** på lagerleverancelinjen. Vælg **Bogfør leverance**-handling. Montageoutput bogføres, herunder forbrug af komponent. En salgsleverance for mængden, bogføres for salgsordre.

Fra montageordren kan du vælge **Ordremont.lagerleverancelinje** for at gå til lagerleverancelinjen.

Når lagerleverance bogføres, opdateres forskellige felter på salgsordrelinjen for at vise fremskridt på lageret. Følgende felter opdateres også for at vise, hvor mange montageordrer der mangler at blive monteret og leveret:

* **Udes. lagerantal for MTO**
* **Udes. lagerantal for MTO (basis)**

> [!NOTE]
> I kombinationsscenarier, hvor en del af mængden først skal samles, og en anden skal leveres fra lageret, oprettes minimum to lagerleverancelinjer. En er til montage efter ordre-antal, og den anden er til beholdningsantal.
>
> Montage efter ordre-antallet håndteres som beskrevet i denne artikel. Lagerantal håndteres som en almindelig lagerleverancelinje. Du kan finde flere oplysninger om kombinationsscenarier i [Om Montage til ordre og Montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-related-microsoft-training" />Se relateret [Microsoft-træning](/training/modules/ship-invoice-items-dynamics-365-business-central/).

## <a name="see-also" />Se også

[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
