---
title: Oversigt over udgående lagerstedsprocesser
description: Denne artikel beskriver den udgående lagerarbejdsgang.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 02/05/2024
ms.custom: bap-template
---
# <a name="outbound-warehouse-processes"></a>Udgående lagerprocesser

Udgående processer i lagersteder starter, når du frigiver et kildedokument for at hente varer fra en lagerlokation. F.eks. for at sende varerne et sted eller til at flytte dem til en anden virksomhedsplacering. Du kan afsende fysiske og ikke-lagerførte varer. Du kan få mere at vide om modtagelse af ikke-lagerførte varer ved at gå til [Bogføre ikke-lagervarer](#post-non-inventory-items). 

Processen med at afsende udgående ordrer består principielt af to aktiviteter:

* Plukke varer fra hylderne.
* Afsendelse af varer fra lagerstedet.

Kildedokumenterne for udgående lagerflows er:  

* Salgsordre  
* Udgående overflytningsordre  
* Købsreturvareordre  
* Serviceordre  

> [!NOTE]
> Produktions-og montageordrer med komponentbehov repræsenterer også udgående kildedokumenter. Produktions-og montageordrer er lidt forskellige, fordi de typisk er interne processer, der ikke involverer levering. I stedet bruges de til læg-på-lager-aktiviteter, eller du kan flytte de komponenter, der skal bruges til at samle en vare til et montageområde. Få mere at vide om disse processer i forbindelse med [Designdetaljer: interne lagerflows](design-details-internal-warehouse-flows.md).  

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du modtage varer og indsætte dem på en af fire måder som beskrevet i følgende tabel.

|Metode|Udgående proces|Kræv pluk|Kræv leverance|Sværhedsgrad (få mere at vide på [Warehouse Management-oversigt](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bogfør pluk og leverance fra ordrelinjen|||Ingen dedikeret lageraktivitet.|  
|B|Bogfør pluk og leverance fra et lagerplukdokument|Aktiveret||Basis: Ordre for ordre.|  
|U|Bogfør pluk og leverance fra et lagerstedsleverancedokument||Aktiveret|Basis: Konsolideret modtagelse/levering for flere ordrer.|  
|D|Bogfør pluk fra et lagerstedsplukdokument, og bogfør leverance fra et lagerstedsleverancedokument|Aktiveret|Aktiveret|Avanceret|  

Valg af metode afhænger af virksomhedens accepterede praksis og graden af organisationens kompleksitet. Nedenfor er vist nogle eksempler, som kan være en hjælp.

* I et ordre for ordre-miljø med enkle processer og simpel placeringsstruktur, metode A, er pluk og levering fra ordrelinjen passende.
* Hvis varer for en ordrelinje stammer fra mere end én placering, eller hvis lagermedarbejdere ikke kan arbejde med ordredokumenter, er brug af separate plukdokumenter relevant, metode B.
* Hvis pluk- og leveringsprocesserne omfatter flere ordrer og kræver bedre kontrol og oversigt, kan du vælge at bruge et lagerstedsleverancedokument og lagerstedsplukdokument til at adskille pluk-og leveringsopgaverne, metode C og D.  

Handlinger af pluk og levering kombineres i metoderne A, B og C i ét trin, hvor et tilsvarende dokument bogføres som leveret. Plukket er registreret første gang i metode D, og derefter bogføres leverancen på et senere tidspunkt fra et andet dokument.

> [!NOTE]
> Mens lagerstedspluk og lagerpluk lyder ens, anvendes forskellige dokumenter og de bruges i forskellige processer.
> * Den lagerpluk-aktivitet, der anvendes i metode B sammen med registreringen af oplysninger om plukaktiviteter, bogfører også afsendelse af kildedokumentet.
> * Det lagerstedspluk, der bruges i metode D, kan ikke bogføres og registrerer kun plukket. Registreringen medfører, at elementer er tilgængelige for lagerstedsforsendelse, men bogfører ikke leveringen. I det udgående flow kræver lagerstedspluk en lagerstedsforsendelse.

## <a name="no-dedicated-warehouse-activity"></a>Ingen dedikeret lageraktivitet

Følgende artikler indeholder oplysninger om, hvordan du behandler modtagelser af kildedokumenter, hvis du ikke har dedikerede lageraktiviteter.

* [Sælge produkter](sales-how-sell-products.md)
* [Overflytningsordrer](inventory-how-transfer-between-locations.md)
* [Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md)
* [Oprette serviceordrer](service-how-to-create-service-orders.md)

## <a name="basic-warehouse-configurations"></a>Grundlæggende lageropsætninger

I følgende diagram illustreres de udgående lagerstedsprocesser for forskellige dokumenttyper i grundlæggende lagerstedsopsætninger. Tallene i diagrammet svarer til trinnene i afsnittene efter diagrammet.  

:::image type="content" source="media/design-details-warehouse-management-outbound-basic-flow.png" alt-text="Viser trinene i en grundlæggende udgående flow på et lagersted.":::

### <a name="1-release-a-source-document"></a>1: Frigiv et kildedokument

Når du bruger handlingen **Frigiv** på et kildedokument, f. eks. en salgs-eller overflytningsordre, er varerne i dokumentet klar til at blive ekspederet på lagerstedet. Plukkes og lægges f. eks. på den placering, der er angivet i dokumentet. Alternativt kan du oprette lagerplukdokumenter for de enkelte ordrelinjer på ordrer, baseret på angivne placeringer og antal, der skal håndteres.  

### <a name="2-create-an-inventory-pick"></a>2: Opret lagerpluk

På siden **lagerpluk** henter lagermedarbejderen på en pull-måde kildedokumentlinjerne. Alternativt er pluklinjerne for lageret allerede oprettet på en push-måde af den bruger, der er ansvarlig for kildedokumentet.  

### <a name="3-post-an-inventory-pick"></a>3: Bogfør lagerpluk

På hver linje for varer, der er lagt på lager, helt eller delvist, udfylder feltet **Antal** og bogfører derefter lagerplukket. Kildedokumenter, der er knyttet til lagerplukningen, bogføres som leveret eller forbrugt.  

Ved lagerpluk oprettes der negative vareposter, lagerposter oprettes, og plukanmodningen slettes, hvis fuldt håndteret. Feltet **Leveret (antal)** opdateres f.eks. på den udgående kildedokumentlinje. Der oprettes f.eks. et bogført leverancedokument, der afspejler salgsordren og de leverede varer.  

## <a name="advanced-warehouse-configurations"></a>Avancerede lageropsætninger

I følgende diagram illustreres de udgående lagerstedsprocesser for forskellige dokumenttyper i avancerede lagerstedsopsætninger. Tallene i diagrammet svarer til trinnene i afsnittene efter diagrammet.  

:::image type="content" source="media/design_details_warehouse_management_outbound_advanced_flow.png" alt-text="Viser trinene i et avanceret udgående lagerstedsflow.":::

### <a name="1-release-a-source-document-1"></a>1: Frigiv et kildedokument

Frigivelse af kildedokumenter i avancerede konfigurationer gør det samme som for grundlæggende konfigurationer. Varerne bliver disponible til håndtering på lagerstedet. F.eks. kan de medtages i en forsendelse.  

### <a name="2-create-a-warehouse-shipment"></a>2: Opret en lagerleverance

Linjerne fra kildedokumentet vises på siden **Lagerstedsleverance**. Flere kildedokumentlinjer kan kombineres i et lagerleverancedokument.  

### <a name="3-create-a-warehouse-pick"></a>3: Opret lagerstedspluk

På siden **Lagerstedsleverance** kan du oprette lagerstedsplukaktiviteter for lagerstedsleverancer på to måder:

- På en push-måde, hvor du kan bruge handlingen **Opret pluk**. Vælg de linjer, der skal plukkes, og forbered plukkene ved at angive, hvilke placeringer der skal tages fra, hvilke placeringer der skal placeres i, og hvor mange enheder der skal håndteres. Placeringerne kan være foruddefineret ved opsætning af lagerstedslokationen eller ressourcen.
- På en push-måde, hvor du kan bruge handlingen **Frigiv**. På siden **Plukkladde** kan lagerstedsmedarbejderne bruge handlingen **Hent lagerstedsdokumenter** til at få tildelt de tildelte pluk. Når lagerstedspluk er fuldt tildelt, slettes linjerne i **Plukkladde**.

### <a name="4-register-a-warehouse-pick"></a>4: Registrer et lagerstedspluk

På hver linje for varer, der er plukket eller flyttet helt eller delvist, udfylder lagermedarbejderen feltet **Antal** på siden **Lagerstedspluk** og registrerer derefter lagerplukningen.

Lagerstedsposter oprettes og lagerstedspluklinjerne slettes, hvis plukningen er fuldført. Lagerstedsplukdokumentet forbliver åbent, indtil det fulde antal af den relaterede lagerstedsleverance er registreret. Feltet **Plukket antal** på lagerleverancelinjerne opdateres i overensstemmelse hermed.  

### <a name="5-post-the-warehouse-shipment"></a>5: Bogfør lagerstedsleverance

Når alle varer på lagerstedsleverancedokumentet er registreret som plukket, bogfører den lagermedarbejderen leverancen. Bogføring opdaterer vareposterne, så de afspejler reduktionen af lagerbeholdningen. Feltet **Leveret (antal)** opdateres f.eks. på den udgående kildedokumentlinje.  

## <a name="post-non-inventory-items"></a>Varer, der ikke er lagervarer

[!INCLUDE [post-non-inventory-items](includes/post-non-inventory-items.md)]

## <a name="see-also"></a>Se også

[Warehouse Management](design-details-warehouse-management.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
