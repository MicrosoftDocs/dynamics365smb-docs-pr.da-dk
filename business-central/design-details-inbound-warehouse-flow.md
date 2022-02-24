---
title: Designoplysninger – Indgående lagerflow | Microsoft Docs
description: Den indgående strøm i et lager begynder, når der ankommer varer på lageret i virksomheden, som enten er modtaget fra eksterne kilder eller fra et andet sted i firmaet. En medarbejder registrerer varerne, typisk ved at scanne en stregkode. Fra modtagelsesområdet udføres lageraktiviteterne på forskellige kompleksitetsniveauer for at bringe varerne ind i lagerområdet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1a20981117fd92751fd9890c8db6feda6120eab8
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185416"
---
# <a name="design-details-inbound-warehouse-flow"></a>Designoplysninger: Indgående lagerflow
Den indgående strøm i et lager begynder, når der ankommer varer på lageret i virksomheden, som enten er modtaget fra eksterne kilder eller fra et andet sted i firmaet. En medarbejder registrerer varerne, typisk ved at scanne en stregkode. Fra modtagelsesområdet udføres lageraktiviteterne på forskellige kompleksitetsniveauer for at bringe varerne ind i lagerområdet.  

 Hvert element identificeres og afstemmes med et tilsvarende indgående kildedokument. Der findes følgende indgående kildedokumenter:  

- Købsordre  
- Indgående overflytningsordre  
- Salgsreturvareordre  

Desuden findes følgende interne kildedokumenter, der fungerer ligesom indgående kilder:  

- Produktionsordre med afgangsbogføring  
- Montageordre med afgangsbogføring  

De sidste to udgør indgående strømme til lageret fra interne operationsområder. Du kan finde flere oplysninger om lagerekspedition for interne indgående og udgående processer i [Designoplysninger: Internt lagerflow](design-details-internal-warehouse-flows.md).  

Processer og brugergrænsefladedokumenter i indgående lagerstrømme er forskellige for grundlæggende og avancerede lageropsætninger. Den væsentligste forskel er, at aktiviteter udføres ordre for ordre i grundlæggende lageropsætninger, og de er fælles for flere ordrer i avancerede lageropsætninger. Du kan finde flere oplysninger om forskellige lagerkompleksitetsniveauer i [Designoplysninger: Oversigt over logistik](design-details-warehouse-setup.md)  

I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner, afhængigt af kompleksitetsniveauet på lageret.  

|Metode|Indgående proces|Placering|Modtagelser|Læg-på-lager-aktiviteter|Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|T|Bogfør lagermodtagelse og læg-på-lager fra ordrelinjen|X|||2|  
|B|Bogfør lagermodtagelse og læg-på-lager fra et læg-på-lager-dokument|||X|3|  
|L|Bogfør lagermodtagelse og læg-på-lager fra et lagermodtagelsesdokument||X||5-4-6|  
|D|Bogfør modtagelse fra et lagermodtagelsesdokument, og bogfør læg-på-lager fra lagerets læg-på-lager-dokument||X|X|5-4-6|  

Valg af metode afhænger af virksomhedens accepterede praksis og graden af organisationens kompleksitet. I et ordre for ordre-lagermiljø, hvor de fleste af lagermedarbejdere arbejder direkte med ordredokumenter, kan en virksomhed beslutte at bruge metode A. Et ordre for ordre-lagersted, der har en mere kompleks læg-på-lager-proces, eller hvor der er særligt lagerpersonale til at udføre lagerfunktioner, kan beslutte at adskille deres læg-på-lager-funktioner fra ordredokumentet, metode B. Desuden vil firmaer, der har brug for at planlægge håndtering af flere ordrer, måske finde det nyttigt at bruge lagermodtagelsesdokumenter, metode C og D.  

Handlinger, der modtager og lægger væk, kombineres i metoderne A, B og C i ét trin, hvor de tilsvarende dokumenter bogføres som modtaget. I D-metoden bogføres modtagelsen først for at genkende forøgelsen af lager, så varerne er tilgængelige til salg. Lagermedarbejderen registrerer derefter læg-på-lager-aktiviteten for at gøre varerne disponible til pluk.  

## <a name="basic-warehouse-configurations"></a>Grundlæggende lageropsætninger  
I følgende diagram illustreres de indgående lagerstrømme af dokumenttype i grundlæggende lageropsætninger. Tallene i diagrammet svarer til trinnene i afsnittene efter diagrammet.  

![Indgående flow i grundlæggende lageropsætninger](media/design_details_warehouse_management_inbound_basic_flow.png "Indgående flow i grundlæggende lageropsætninger")  

### <a name="1-release-source-document--create-inventory-put-away"></a>1: Frigiv kildedokument / Opret læg-på-lager  
Når varerne modtages på lageret, frigiver den bruger, der er ansvarlig for modtagelse, kildedokumentet, f.eks. en indkøbsordre eller en indgående overflytningsordre ordre, for at signalere til lagermedarbejdere, at de modtagne varer kan lægges på lager. Alternativt kan brugeren oprette læg-på-lager-dokumenter for de enkelte ordrelinjer på en push-måde, baseret på angivne placeringer og antal, der skal håndteres.  

### <a name="2-create-inbound-request"></a>2: Opret indgående anmodning  
Når det indgående kildedokument frigives, oprettes der automatisk en indgående lageranmodning. Den indeholder referencer til kildebilagstype og -nummer og er ikke synlig for brugeren.  

### <a name="3-create-inventory-put-away"></a>3: Opret læg-på-lager  
På siden **Læg-på-lager** modtager lagermedarbejderen på en pull-måde de ventende kildedokumentlinjer, der er baseret på indgående lageranmodninger. Alternativt er læg-på-lager-linjerne allerede oprettet på en push-måde af den bruger, der er ansvarlig for kildedokumentet.  

### <a name="4-post-inventory-put-away"></a>4: Bogfør læg-på-lager  
På hver linje for varer, der er lagt på lager, helt eller delvist, udfylder lagermedarbejderen feltet **Antal** og bogfører derefter lagt på lager. Kildedokumenter, der er knyttet til læg-på-lager, bogføres som modtaget.  

Der oprettes positive vareposter og lagerposter, og læg-på-lager-anmodningen slettes, hvis den er fuldt håndteret. Feltet **Modtaget \(antal\)** opdateres f.eks. på den indgående kildedokumentlinje. Der oprettes f.eks. et bogført modtagelsesdokument, der afspejler købsordren og de modtagne varer.  

## <a name="advanced-warehouse-configurations"></a>Avancerede lageropsætninger  
I følgende diagram illustreres den indgående lagerstrøm af dokumenttype i avancerede lageropsætninger. Tallene i diagrammet svarer til trinnene i afsnittene efter diagrammet.  

![Indgående flow i avancerede lageropsætninger](media/design_details_warehouse_management_inbound_advanced_flow.png "Indgående flow i avancerede lageropsætninger")  

### <a name="1-release-source-document"></a>1: Frigiv kildedokument  
Når varerne modtages på lageret, frigiver den bruger, der er ansvarlig for modtagelse, kildedokumentet, f.eks. en indkøbsordre eller en indgående overflytningsordre ordre, for at signalere til lagermedarbejdere, at de modtagne varer kan lægges på lager.  

### <a name="2-create-inbound-request"></a>2: Opret indgående anmodning  
Når det indgående kildedokument frigives, oprettes der automatisk en indgående lageranmodning. Den indeholder referencer til kildebilagstype og -nummer og er ikke synlig for brugeren.  

### <a name="3-create-warehouse-receipt"></a>3: Opret lagermodtagelse  
På siden **Lagermodtagelse** modtager den bruger, der er ansvarlig for modtagelse af varer, de ventende kildedokumentlinjer, der er baseret på den indgående lageranmodning. Flere kildedokumentlinjer kan kombineres i et lagermodtagelsesdokument.  

Brugeren udfylder feltet **Håndteringsantal** og vælger den modtagende zone og placering, hvis det er nødvendigt.  

### <a name="4-post-warehouse-receipt"></a>4: Bogfør lagermodtagelse  
Brugeren bogfører lagermodtagelsen. Der oprettes positive vareposter. Feltet **Modtaget \(antal\)** opdateres f.eks. på den indgående kildedokumentlinje.  

### <a name="5-create-warehouse-internal-put-away"></a>5: Opret intern læg-på-lager  
Den bruger, der er ansvarlig for læg-på-lager fra interne operationer, opretter et lagersted for internt læg-på-lager for varer, der skal lægges på lager, f.eks. produktions- eller montageoutput. Brugeren angiver antal, zone og placering fra, hvor varerne skal lægges på lager, eventuelt med funktionen **Hent placeringsindh.**. Brugeren frigiver lagerstedets interne læg-på-lager, hvilket opretter en indgående lageranmodning, så opgaven kan hentes i læg-på-lager-dokumenter eller i læg-på-lager-kladden.  

### <a name="6-create-put-away-request"></a>6: Opret læg-på-lager-anmod.  
Når det indgående kildedokument bogføres, oprettes der automatisk en læg-på-lager-lageranmodning. Den indeholder referencer til kildebilagstype og -nummer og er ikke synlig for brugeren. Afhængigt af opsætningen opretter afgang fra en produktionsordre også en læg-på-lager-anmodning om at lægge de færdige varer på lager.  

### <a name="7-generate-put-away-worksheet-lines-optional"></a>7: Generér læg-på-lager-kladdelinjer (valgfrit)  
Den bruger, der er ansvarlig for at koordinere læg-på-lager-aktiviteterne, henter læg-på-lager-linjer i den **Læg-på-lager-kladde**, der er baseret på bogførte lagermodtagelser eller interne operationer med afgang. Brugeren vælger de linjer med læg-på-lager-aktiviteter og forbereder disse læg-på-lager-aktiviteter ved at angive, hvilke placeringer der skal tages fra, hvilke placeringer der skal placeres i, og hvor mange enheder der skal håndteres. Placeringerne kan være foruddefineret ved opsætning af lagerlokationen eller operationsressourcen.  

Når alle læg-på-lager-aktiviteter er planlagt og tildelt til lagermedarbejdere, opretter brugeren læg-på-lager-dokumenter. Fuldt tildelte læg-på-lager-linjer slettes fra **Læg-på-lager-kladden**.  

> [!NOTE]  
>  Hvis feltet **Brug Læg-på-lager-kladde** ikke er markeret på lokationskortet, bliver læg-på-lager-dokumenter oprettet direkte ud fra bogførte lagermodtagelser. I så fald udelades trin 7.  

### <a name="8-create-warehouse-put-away-document"></a>8: Opret læg-på-lager-dokument  
Den lagermedarbejder, der udfører læg-på-lager-aktiviteter, opretter et læg-på-lager-lager-dokument på en pull-måde baseret på den bogførte lagermodtagelse. Alternativt er læg-på-lager-dokumentet oprettet og tildelt en lagermedarbejder på en push-måde.  

### <a name="9-register-warehouse-put-away"></a>9: Registrer læg-på-lager  
På hver linje for varer, der er lagt på lager, helt eller delvist, udfylder lagermedarbejderen feltet **Antal** på siden **Læg-på-lager (logistik)** og registrerer derefter læg-på-lager-aktiviteten.  

Lagerposter oprettes og læg-på-lager-linjerne slettes, hvis de er fuldt håndteret. Læg-på-lager-dokumentet forbliver åbent, indtil det fulde antal af den relaterede bogførte lagermodtagelse er registreret. Feltet **Antal lagt\-på\-lager** på lagermodtagelsens ordrelinjer opdateres.  

## <a name="see-also"></a>Se også  
[Designoplysninger: Logistik](design-details-warehouse-management.md)
