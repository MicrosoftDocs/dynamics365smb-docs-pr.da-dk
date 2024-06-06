---
title: Designoplysninger - Indgående lagerflow
description: 'Vide, hvordan du modtager varer på lagerstedet og registrerer og matcher dem med indgående kildedokumenter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: warehouse
ms.date: 09/18/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-inbound-warehouse-flow"></a>Designoplysninger: Indgående lagerflow

Den indgående strøm i et lager begynder, når der ankommer varer på lageret i virksomheden, som enten er modtaget fra eksterne kilder eller fra et andet sted i firmaet. Du kan modtage fysiske og ikke-lagerførte varer. Du kan få mere at vide om modtagelse af ikke-lagerførte varer ved at gå til [Bogføre ikke-lagervarer](#post-non-inventory-items).

Processen med at modtage indgående ordrer består principielt af to aktiviteter:

* Modtage varer ved modtagelse, hvor du kan identificere dem, sammenligne dem med et kildedokument og registrere det modtagne antal.
* Lægge varer på lager og registrere, hvor de er placeret.

Kildedokumenterne for indgående lagerflows er:

* Købsordrer  
* Indgående overflytningsordrer  
* Salgsreturordrer  

> [!NOTE]
> Produktions- og montage-output repræsenterer også indgående kildedokumenter. Du kan finde flere oplysninger om lagerekspedition for interne indgående og udgående processer i [Designoplysninger: Internt lagerflow](design-details-internal-warehouse-flows.md).  

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du modtage varer og indsætte dem på en af fire måder som beskrevet i følgende tabel.

|Metode|Indgående proces|Kræv modtagelse|Kræv læg-på-lager|Sværhedsgrad (få mere at vide på [Warehouse Management-oversigt](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bogfør lagermodtagelse og læg-på-lager fra ordrelinjen|||Ingen dedikeret lageraktivitet.|  
|B|Bogfør lagermodtagelse og læg-på-lager fra et læg-på-lager-dokument||Aktiveret|Basis: Ordre for ordre.|  
|U|Bogfør lagermodtagelse og læg-på-lager fra et lagermodtagelsesdokument|Aktiveret||Basis: Konsolideret modtagelse/levering for flere ordrer.|  
|D|Bogfør modtagelse fra et lagermodtagelsesdokument, og bogfør læg-på-lager fra lagerets læg-på-lager-dokument|Aktiveret|Aktiveret|Avanceret|  

Valg af metode afhænger af virksomhedens accepterede praksis og graden af organisationens kompleksitet. Nedenfor er vist nogle eksempler, som kan være en hjælp.

* I lagermiljøet ordre for ordre, hvor de fleste lagermedarbejdere arbejder direkte med ordredokumenter, kan du vælge at bruge metode A. 
* Et ordre for ordre-lagersted, der har en mere kompleks læg-på-lager-proces, eller hvor lagerpersonalet adskiller deres læg-på-lager-aktiviteter fra ordredokumentet, kan bruge metode B.
* Virksomheder, der har brug for at planlægge håndteringen af flere ordrer, kan være nyttig i stedet for at bruge lagermodtagelsesdokumenter, metode C og D.  

I metoderne A, B og C kombineres i metoderne i ét trin, hvor de tilsvarende dokumenter bogføres som modtaget. I D-metoden bogføres modtagelsen først for at registrere forøgelsen af lager, så varerne er tilgængelige til salg. Lagermedarbejderen registrerer derefter læg-på-lager-aktiviteten for at gøre varerne disponible til pluk for udgående ordrer. 

> [!NOTE]
> Mens læg-på-lager-aktiviteter og læg-på-lager-aktiviteter i det samme lyder som forskellige dokumenter og bruges i forskellige processer.
> * Den læg-på-lager-aktivitet, der anvendes i metode B sammen med registreringen af oplysninger om læg-på-lager-aktiviteter, bogfører også modtagelsen af kildedokumentet.
> * Den læg-på-lager-aktivitet, der bruges i metode D, kan ikke bogføres og registrerer kun læg-på-lager. Registreringen gør varerne tilgængelige for viderebehandlingen, men bogfører ikke modtagelsen. I den indgående flow kræver læg-på-lager-aktiviteten en lagermodtagelse.

## <a name="no-dedicated-warehouse-activity"></a>Ingen dedikeret lageraktivitet

Følgende artikler indeholder oplysninger om, hvordan du behandler modtagelser af kildedokumenter, hvis du ikke har dedikerede lageraktiviteter.

* [Registrere køb](purchasing-how-record-purchases.md)
* [Overflytningsordrer](inventory-how-transfer-between-locations.md)
* [Gennemgå salgsreturvareordrer](sales-how-process-sales-returns-orders.md)

## <a name="basic-warehouse-configurations"></a>Grundlæggende lageropsætninger

I en grundlæggende lageropsætning er funktionen **Kræv læg-på-lagerR** slået til, men indstillingen **Kræv modtagelse** er slået fra på **lokationskortet** for lokationen.

I følgende diagram illustreres de indgående lagerstrømme af dokumenttype i grundlæggende lageropsætninger. Tallene i diagrammet svarer til trinnene i afsnittene efter diagrammet.  

:::image type="content" source="media/design_details_warehouse_management_inbound_basic_flow.png" alt-text="Indgående flow i grundlæggende lageropsætninger":::

### <a name="1-release-a-source-document-to-create-a-request-for-an-inventory-put-away"></a>1: Frigiv et kildedokument for at oprette en anmodning om en læg-på-lager-aktivitet

Når du modtager varer, skal du frigive kildedokumentet, f. eks. en købsordre eller en indgående overflytningsordre. Når du frigiver dokumentet, bliver varerne klar til at blive lagt på lager. Du kan også oprette læg-på-lager-dokumenter for de enkelte ordrelinjer på en push-måde, baseret på placeringer og antal, der skal håndteres.  

### <a name="2-create-an-inventory-put-away"></a>2: Opret et læg-på-lager

På siden **Læg-på-lager** modtager lagermedarbejderen på en pull-måde de ventende kildedokumentlinjer, der er baseret på indgående lageranmodninger. Når du opretter kildedokumentet, kan du også oprette læg-på-lager-linjer.  

### <a name="3-post-an-inventory-put-away"></a>3: Bogfør læg-på-lager

På hver linje for varer, der er lagt på lager, helt eller delvist, udfylder lagermedarbejderen feltet **Antal** og bogfører derefter lagt på lager. Kildedokumenter, der er knyttet til læg-på-lager, bogføres som modtaget.  

* Der oprettes positive vareposter.
* Lagerposter oprettes til lokationer, der kræver placeringskode på alle varetransaktioner.
* Læg-på-lager-anmodningen slettes, hvis den håndteres fuldt ud. Feltet **Modtaget \(antal\)** opdateres f.eks. på den indgående kildedokumentlinje.
* Der oprettes f.eks. et bogført modtagelsesdokument, der afspejler købsordren og de modtagne varer.  

## <a name="advanced-warehouse-configurations"></a>Avancerede lageropsætninger

I en avanceret Lageropsætning skal **Kræv modtagelse**-til/fra være aktiveret på lokationskort siden for lokationen. Funktionen **Kræv læg-på-lager** er valgfrit.

I følgende diagram illustreres den indgående lagerstrøm af dokumenttype. Tallene i diagrammet svarer til trinnene i afsnittene efter diagrammet.  

:::image type="content" source="media/design_details_warehouse_management_inbound_advanced_flow.png" alt-text="Indgående flow i avancerede lageropsætninger.":::

### <a name="1-release-the-source-document"></a>1: Frigiv kildedokument

Når du modtager varer, skal du frigive kildedokumentet, f. eks. en købsordre eller en indgående overflytningsordre. Når du frigiver dokumentet, bliver varerne klar til at blive lagt på lager. Funktionen til at lægge væk indeholder referencer til kildebilagstype og -nummer.

### <a name="2-create-a-warehouse-receipt"></a>2: Opret lagermodtagelse

Linjerne fra kildedokumentet vises på siden **Lagermodtagelse**. Du kan kombinere flere kildedokumentlinjer i et lagermodtagelsesdokument. Brugeren udfylder feltet **Håndteringsantal** og vælger den modtagende zone og placering, hvis det er nødvendigt.  

### <a name="3-post-the-warehouse-receipt"></a>3: Bogfør lagermodtagelsen

Bogfør lagerstedsmodtagelse for at oprette positive poster for varen. Feltet **Modtaget antal** opdateres f.eks. på den indgående kildedokumentlinje.  

Hvis indstillingen **Kræv læg-på-lager** ikke er aktiveret på lokationskortet, er det her, hvor processen stopper. Når du frigiver dokumentet, bliver varerne klar til at blive lagt på lager. Funktionen til at lægge væk indeholder referencer til kildebilagstype og -nummer.  

### <a name="4-optional-generate-put-away-worksheet-lines"></a>4: (Valgfrit) Generér læg-på-lager-kladdelinjer

Hent læg-på-lager-linjer i **Læg-på-lager-kladden** baseret på bogførte lagermodtagelser eller operationer, der genererer afgang. Vælg de linjer, der skal lægges på lager, og angiv følgende oplysninger:

* De placeringer, som varerne skal hentes fra.
* Sådan lægges varerne på lager.
* Hvor mange enheder, der skal håndteres.

Placeringerne kan være foruddefineret ved opsætning af lagerlokationen eller operationsressourcen.  

Når alle læg-på-lager-aktiviteter er planlagt og tildelt til lagermedarbejdere, opretter brugeren læg-på-lager-dokumenter. Fuldt tildelte læg-på-lager-linjer slettes fra **Læg-på-lager-kladden**.  

> [!NOTE]  
> Hvis feltet **Brug Læg-på-lager-kladde** ikke er markeret på lokationskortet, bliver læg-på-lager-dokumenter oprettet direkte ud fra bogførte lagermodtagelser. I dette tilfælde er dette trin ikke nødvendigt.  

### <a name="5-create-a-warehouse-put-away-document"></a>5: Opret et læg-på-lager-bilag

Oprette et læg-på-lager-dokument på en pull-måde baseret på den bogførte lagermodtagelse. Alternativt er læg-på-lager-dokumentet oprettet og tildelt en lagermedarbejder på en push-måde.  

### <a name="6-register-a-warehouse-put-away"></a>6: Registrer et læg-på-lager

På hver linje for varer, der er lagt på lager, helt eller delvist, udfylder lagermedarbejderen feltet **Antal** på siden **Læg-på-lager** og registrerer derefter læg-på-lager-aktiviteten.  

* Lagerposter oprettes til lokationer, der kræver placeringskode på alle varetransaktioner.
* Læg-på-lager-linjerne slettes, hvis den håndteres fuldt ud.
* Læg-på-lager-dokumentet forbliver åbent, indtil du registrerer det fulde antal af den relaterede bogførte lagermodtagelse.
* Feltet **Antal lagt-på-lager** på lagermodtagelsens ordrelinjer opdateres.

## <a name="related-tasks"></a>Relaterede emner

Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.

|**For at**|**Skal du se**|  
|------------|-------------|  
|Modtag varer på lagerlokationer med en lagerkvittering i tilfælde af halvt eller fuldt automatiseret lagerbehandling på lokationen.|[Modtage varer](warehouse-how-receive-items.md)|
|Lægge varer på lager en ordre ad gangen og bogføre tilgangen i samme aktivitet i en grundlæggende lageropsætning.|[Lægge varer på lager med Læg-på-lager (lager)](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Lægge varer på lager, der er modtaget fra flere køb, salgsreturvarer, overflytningsordrer i henhold til den konfigurerede lagerproces.|[Lægge varer på lager med Læg-på-lager (lagersted)](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  

## <a name="post-non-inventory-items"></a>Varer, der ikke er lagervarer

[!INCLUDE [post-non-inventory-items](includes/post-non-inventory-items.md)]

## <a name="see-also"></a>Se også

[!INCLUDE[footer-include](includes/footer-banner.md)]
