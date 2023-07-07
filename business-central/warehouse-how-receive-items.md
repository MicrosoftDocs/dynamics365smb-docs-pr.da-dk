---
title: Modtage varer
description: Denne artikel er en oversigt over de forskellige måder at modtage varer på et lagersted med en lagermodtagelse.
author: brentholtorf
ms.author: bholtorf
ms.topic: how-to
ms.date: 09/02/2022
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008'
---
# <a name="receive-items-with-warehouse-receipts"></a>Modtage varer med en lagermodtagelse

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du modtage varer og indsætte dem på en af fire måder som beskrevet i følgende tabel.

|Metode|Indgående proces|Kræv modtagelse|Kræv læg-på-lager|Sværhedsgrad (få mere at vide på [Warehouse Management-oversigt](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bogfør lagermodtagelse og læg-på-lager fra ordrelinjen|||Ingen dedikeret lageraktivitet.|  
|B|Bogfør lagermodtagelse og læg-på-lager fra et læg-på-lager-dokument||Aktiveret|Basis: Ordre for ordre.|  
|U|Bogfør lagermodtagelse og læg-på-lager fra et lagermodtagelsesdokument|Aktiveret||Basis: Konsolideret modtagelse/levering for flere ordrer.|  
|D|Bogfør modtagelse fra et lagermodtagelsesdokument, og bogfør læg-på-lager fra lagerets læg-på-lager-dokument|Aktiveret|Aktiveret|Avanceret|  

Du kan lære mere om, hvordan indgående varer håndteres, ved at gå til [Indgående lagerstedsflow](design-details-inbound-warehouse-flow.md).

Følgende artikel henviser til metode C og D i den foregående tabel.

## <a name="receive-items-with-a-warehouse-receipt"></a>Modtage varer med en lagermodtagelse

Når der ankommer varer til et lagersted, der er sat op til lagermodtagelse, henter du de linjer i kildedokumentet, som har udløst modtagelsen. Hvis du bruger placeringer, kan du enten acceptere standardplaceringen eller angive den placering, varerne skal anbringes i. Dette kan være nødvendigt, når du modtager en vare for første gang. Du skal derefter udfylde det antal af varen, du har modtaget, og bogføre modtagelsen.  

Du kan anvende svar på en af to måder:

* I en push-metode, når der arbejdes på ordre til ordre-grundlag. Vælg **Opret lagerstedsmodtagelse**-handling i kildedokumentet, f. eks. købsordre, Salgsreturvareordre eller overflytningsordre for at oprette lagermodtagelse for ét kildedokument.
*-* På en push-måde, hvor du kan bruge handlingen **Frigiv** i kildedokumentet, f. eks. en købsordre, en salgsreturvareordre eller en overflytningsordre til frigivelse af dokumentet til lagerstedet. En lagerstedsmedarbejder opretter en **Lagerstedsmodtagelse** for en eller flere frigivne kildedokumenter. Følgende fremgangsmåde beskriver, hvordan du opretter en lagermodtagelse på en pull-måde. Følgende fremgangsmåde beskriver, hvordan du opretter en lagermodtagelse på en pull-måde. 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermodtagelse**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  

    Udfyld feltet **Lokationskode** i oversigtspanelet **Generelt**. Når du henter kildedokumentlinjer, kopieres nogle af oplysningerne fra hovedet til hver linje. 

    Udfyld feltet **Placeringskode** for en lokation, der kræver placeringer. Afhængigt af din opsætning kan [!INCLUDE[prod_short](includes/prod_short.md)] tilføje placeringskode for dig. Få mere at vide på [zone-og placeringskoder](warehouse-how-receive-items.md#zone-and-bin-codes).  

3. Du kan hente kildedokument på to måder:

    1. Vælg handlingen **Hent kildedokumenter**. Siden **Kildedokumenter - indgående** åbnes. Her kan du vælge et eller flere kildedokumenter, der er frigivet til lager, som kræver modtagelse.
    2. Vælg handlingen **Brug filtre til at hente kildedok.**. Vinduet **Filtre til at hente kildedok. - indgående** åbnes. Her kan du vælge kildedokument filter og køre det. Alle frigivne kildedokumentlinjer, der overholder filterkriterierne, tilføjes på **lagerstedsmodtagelse**-siden. Flere oplysninger i [Sådan bruges filtre til at hente kildedokumenter](warehouse-how-receive-items.md#how-to-use-filters-to-get-source-documents).

4. Angiv det antal, der skal modtages.

    Feltet **Modtag (antal)** er på forhånd udfyldt med det udestående antal varer for hver linje, men du kan ændre antallet efter behov. 

    Hvis du vil udfylde feltet **Modtag (antal)** på alle linjer med nul, skal du vælge handlingen **Slet Modtag antal**. Du kan f. eks. angive, at mængderne skal være nul, hvis du bruger en stregkodescanner til at opdatere de modtagne antal. Hvis du vil udfylde det igen med det udestående antal, skal du vælge handlingen **Autoudfyld Modtag antal**.  

    På en købsordre eller et lagermodtagelsesdokument, hvor det modtagne antal er højere end det bestilte, skal du angive det faktisk modtagne antal i feltet **Modtag (antal)**. Hvis stigningen ligger inden for den tolerance, der er angivet i overmodtagelseskoden, opdateres feltet **Overmodtagelsesantal**, så det viser det antal, der angiver, hvilken værdi i feltet **Antal**, der overskrides. Hvis forøgelsen er større end den angivne tolerance, er overmodtagelse ikke tilladt.

5. Bogfør lagermodtagelsen. Mængdefelterne opdateres på kildedokumenterne, og varerne tilføjes til lageret.  

    > [!TIP]
    > Hvis du bruger læg-på-lager, som henviser til metode D i tabellen i begyndelsen af denne artikel, modtages varerne, men de kan ikke plukkes, før de er lagt på lager. Du kan lære mere om, hvordan varer lægges på lager, ved at gå til [Lægge varer på lager med læg-på-lager-aktiviteter](warehouse-how-to-put-items-away-with-warehouse-put-aways.md). 
    > 
    > Ellers bør du overveje at bruge handlingen **Bogfør og Udskriv** . Handlingen vil bogføre modtagelsen og udskrive den som en læg-på-lager-instruktion, der viser, hvor varen skal placeres.

> [!NOTE]  
> Hvis lagerstedet bruger direkte afsendelse, kan du kontrollere, om du kan afsende varer direkte uden at lægge dem på lager. Hvis du vil vide mere om direkte afsendelse, skal du gå til [Afsende varer direkte](warehouse-how-to-cross-dock-items.md).

## <a name="how-to-use-filters-to-get-source-documents"></a>Sådan bruges filtre til at hente kildedokumenter

Fra en ny eller en åben lagermodtagelse kan du bruge siden **Filtre til at hente kildedok.** til at hente de frigivne kildedokumentlinjer, der definerer, hvilke varer der skal modtages eller leveres.

1. Vælg handlingen **Brug filtre til at hente kildedok.**.
2. Hvis du vil oprette et nyt filter, skal du indtaste en beskrivende kode i feltet **Kode** og derefter vælge handlingen **Ret**.

    Vinduet **Kildedokumentfilterkort** vises.

3. Brug filtre til at angive, hvilken type kildedokumentlinjer der skal hentes. Du kan f. eks. vælge typer af kildedokumenter, f. eks. købs-eller overflytningsordrer.
4. Vælg **Kør**.  

Alle frigivne kildedokumentlinjer, som opfylder filterkriterierne, indsættes nu på siden **Lagermodtagelse**, hvorfra du har aktiveret filterfunktionen.

Du kan oprette et ubegrænset antal filterkombinationer. De filterkombinationer, du definerer, gemmes på siden **Filtre til at hente kildedok.**, indtil næste gang du skal bruge dem. Du kan til enhver tid ændre kriterierne ved at vælge handlingen **Ret**.

## <a name="zone-and-bin-codes"></a>Zone-og placeringskoder

Hvis du vil modtage varer med en anden lagerklassekode end placeringens klassekode i feltet **Placeringskode** i dokumenthovedet, skal du slette indholdet i feltet **Placeringskode** i hovedet, inden du henter kildedokumentlinjerne for varerne.  
<!-- TBD, table with comparison of various options-->

Hvis placeringer er obligatoriske for en lokation, føjes zone-og placeringskoder til lagermodtagelsesdokumenter på følgende måde:

* I forbindelse med avancerede konfigurationer, der bruger styret læg-på-lager og pluk, bruger [!INCLUDE [prod_short](includes/prod_short.md)] modtagelsesplaceringskoden fra siden **lokationskort** for lokationen. Hvis der ikke er angivet en modtagelsesplaceringskode, er der ikke angivet nogen placering. Hvis varen og kvitterings placeringerne ikke stemmer overens, er modtagelsesplaceringskoden tom.
* I andre konfigurationer bruges placeringskoden fra kildedokumentet, hvis der ikke er angivet [!INCLUDE [prod_short](includes/prod_short.md)], bruges en modtagelsesplaceringskode.

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Se også

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
