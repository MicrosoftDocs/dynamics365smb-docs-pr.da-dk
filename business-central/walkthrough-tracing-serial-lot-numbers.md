---
title: Gennemgang - Sporing af serie-lotnumre | Microsoft Docs
description: Når der forekommer fejlbehæftede produkter, skal fejlene identificeres, og de relevante varer må ikke kunne forlade virksomheden. Hvis de fejlbehæftede varer allerede er afsendt, skal du finde ud af, hvem der har modtaget dem, for om nødvendigt at kunne tilbagekalde varerne.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 23bbed9e19fa2a3fd99f45cfde24d6d16f31e795
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876819"
---
# <a name="walkthrough-tracing-seriallot-numbers"></a>Gennemgang: Sporing af serie-/lotnumre

**Bemærk**: Denne gennemgang skal udføres på et demoregnskab med indstillingen **Fuld evaluering - Komplette eksempeldata**, der findes i sandkassemiljøet. Du kan finde flere oplysninger i [Oprette et sandkassemiljø](across-how-create-sandbox-environment.md).

Når der forekommer fejlbehæftede produkter, skal fejlene identificeres, og de relevante varer må ikke kunne forlade virksomheden. Hvis de fejlbehæftede varer allerede er afsendt, skal du finde ud af, hvem der har modtaget dem, for om nødvendigt at kunne tilbagekalde varerne.  

Den første opgave i forbindelse med administrationen af fejlbehæftede varer er at finde ud af, hvor de fejlbehæftede varer kom fra, og hvor de bruges. Denne undersøgelse er baseret på historiske data og gøres lettere ved at søge på varesporingsposterne ved hjælp af siden **Varesporing**.  

Den første opgave i forbindelse med administrationen af fejlbehæftede varer er at finde ud af, om der er foretaget planlægning for de sporede varer i åbne dokumenter, som f.eks. ikke-bogførte salgsordrer eller forbrugskladder. Dette arbejde udføres på siden **Naviger**. Du kan bruge funktionen Naviger til at søge efter alle typer databaseposter.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
Denne gennemgang viser, hvordan fejlbehæftede varer identificeres, hvilken leverandør der leverede dem, og hvor de bruges, så de pågældende ordrer kan stoppes eller tilbagekaldes.  

Denne gennemgang illustrerer følgende opgaver:  

-   Sporing af brug til oprindelsen.  
-   Sporing af oprindelse til brug.  
-   Søgning efter aktuelle poster, der indeholder det sporede serie-/lotnummer.  

## <a name="roles"></a>Roller  
Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:  

-   Ansvarlig for kvalitetssikring  
-   Lagerchef  
-   Ordrebehandler  
-   Indkøbsagent  

## <a name="prerequisites"></a>Forudsætninger  
For at gennemføre denne gennemgang skal du bruge:  

-   [!INCLUDE[d365fin](includes/d365fin_md.md)]-virksomhed.  
-   Oprette nye varer og forskellige forretningstransaktioner ved at følge trinnene i [Klargøre eksempeldata](walkthrough-tracing-serial-lot-numbers.md#prepare-sample-data).  

## <a name="story"></a>Historie  
Ricardo, der er ansvarlig for kvalitetssikring, handler ud fra returnering af salgsvaren 1002, Racercykel. Kunden, Ravel Møbler, klagede over, at stellet var gået i stykker ved svejsningerne. Kvalitetskontrolteknikeren har bekræftet, at racerstellet på den returnerede cykel er fejlbehæftet. Den ansvarlige for kvalitetssikring skal nu finde ud af:  

-   Hvilket racerstellet, der er fejlbehæftet.  
-   Hvilken indkøbsordre det fejlbehæftede lot blev modtaget via.  

Salgsafdelingen har fortalt den ansvarlige for kvalitetssikring, at den returnerede racercykel, vare 1002, havde serienummeret SN1. Ved at bruge denne grundlæggende oplysning skal han finde ud af, hvor racercyklen sidst blev brugt, og derefter skal han spore den tilbage til den tidligste oprindelse for at finde ud af, hvilket lotnummer den fejlbehæftede komponent, racerstellet, kom fra.  

Resultaterne af denne første varesporingsopgave kan identificere, hvilke racerstel der var defekte, og hvilken leverandør der leverede dem. Bagefter, men i det samme overordnede opfølgningsproces, skal den ansvarlige for kvalitetssikring finde alle solgte racercykler, der indeholder racerstel fra det fejlbehæftede parti, så disse ordrer kan stoppes eller tilbagekaldes. Endelig skal den ansvarlige for kvalitetssikring finde alle åbne dokumenter, hvor det fejlbehæftede parti bruges, så der ikke oprettes tilsvarende transaktioner.  

De første to opgaver i forbindelse med administrationen af fejlbehæftede varer udføres på siden **Varesporing**. Den sidste opgave udføres på siden **Naviger** i sammen med siden **Varesporing**.  

## <a name="prepare-sample-data"></a>Klargøre eksempeldata  
Du skal oprette følgende nye punkter:  

-   2000, Racerstel: lotspecifik sporing, komponent af 1002  
-   1002, Racercykel: serienummerspecifik sporing  

Du skal derefter oprette forskellige indkøbs-, produktions- og salgstransaktioner med de to varer.  

### <a name="to-create-the-items"></a>Sådan oprettes varerne  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  I feltet **Nummer** skal du skrive **2000**, og derefter udfylde de følgende felter.  

    |Beskrivelse|Basisenhed|Finans- Produktbogføringsgruppe|Momsproduktbogf.gruppe|Varebogføringsgruppe|Varesporingskode|  
    |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|------------------------|  
    |Racerstel|STK|RÅVARE|MOMS25|RÅVARE|LOTALLE|  

    > [!NOTE]  
    >  Hvis du vil angive basisenheden, skal du vælge knappen **Ny** og derefter vælge **PSC** på siden **Vareenheder**.  

4.  Alle andre felter indeholder godkendte standarddata eller behøver ikke blive udfyldt.  
5.  Klik på knappen **OK** for at oprette det første nye varekort, 2000.  
6.  Vælg **Ny**.  
7.  I feltet **Nummer** skal du skrive **1002**, og derefter udfylde de følgende felter.  

    |Beskrivelse|Basisenhed|Finans- Produktbogføringsgruppe|Momsproduktbogf.gruppe|Varebogføringsgruppe|Genbestillingssystem|Varesporingskode|  
    |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|--------------------------|------------------------|  
    |Racercykel|STK|DETAIL|MOMS25|FÆRDIG|Prod.ordre|SNALLE|  

    > [!NOTE]  
    >  Hvis du vil angive basisenheden, skal du vælge knappen **Ny** og derefter vælge **PSC** på siden **Vareenheder**.  

    Du skal derefter definere produktionsopsætningen for varen.

9. Gå til oversigtspanelet **Genbestilling**, og indtast **1000** i feltet **Rutenr.**.  
10. Vælg feltet **Produktionsstkl.nr.**, og vælg derefter **Avanceret**.  
11. På siden **Prod.styklisteoversigt** skal du vælge den første linje, **1000**, og derefter vælge handlingen **Rediger**.  
12. På siden **Produktionsstykliste** skal du ændre værdi til **Under udvikling** i feltet **Status**.  
13. Gå til en tom linje, indtast **2000** i feltet **Nummer**, og indtast derefter **1** i feltet **Antal pr.**.  
14. Skift værdien i **Status** tilbage til **Godkendt**.  
15. Vælg knappen **OK** for at indsætte produktionsstyklisten på varekortet og lukke siden **Produktionsstykliste**.  

    Derefter skal du købe racerstel fra Custom Metals Incorporated.  

### <a name="to-purchase-components"></a>Købe komponenter  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsordre**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Opret en købsordre for kreditoren Custom Metals Incorporated ved at udfylde følgende linjefelter.  

    |Vare|Antal|Lotnr.|  
    |----------|--------------|-------------|  
    |2000|10|LOT1|  

4.  Hvis du vil angive lotnummeret, skal du vælg handlingen **Varesporingslinjer**.  
5.  På siden **Varesporingslinjer** skal du udfylde felterne **Lotnr.** og **Antal (basis)** og derefter lukke siden.  
6.  Angiv en værdi i feltet **Kreditors fakturanr.**.  
7.  Vælg handlingen **Bogfør**, vælg indstillingen **Modtag og fakturer**, og vælg derefter knappen **OK**.  

    Dernæst skal du købe racerstel fra Schmeichel Møbler A/S.  
8.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsordre**, og vælg derefter det relaterede link.  
9. Vælg handlingen **Ny**.
10. Opret en købsordre for kreditoren, Schmeichel Møbler A/S, ved at udfylde følgende linjefelter.  

    |Vare|Antal|Lotnr.|  
    |----------|--------------|-------------|  
    |2000|11|LOT2|  

11. Hvis du vil angive lotnummeret, skal du på oversigtspanelet **Linjer** i gruppen **Linje** vælge handlingen **Varesporingslinjer**.  
12. På siden **Varesporingslinjer** skal du udfylde felterne **Lotnr.** og **Antal (basis)** og derefter lukke siden.  
13. Angiv en værdi i feltet **Kreditors fakturanr.**.  
14. Vælg handlingen **Bogfør**, vælg indstillingen **Modtag og fakturer**, og vælg derefter knappen **OK**.  

    Dernæst skal producere to racercykler, SN1 og SN2.  

### <a name="to-produce-end-items"></a>Fremstille færdigvarer  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Frigivne produktionsordrer**, og vælg derefter det relaterede link.  
2.  Vælg gruppen **Ny**.  
3.  Opret en ny frigivet produktionsordre ved at udfylde følgende felter.  

    |-|-|-|  
    |Kildenr.|Antal| Serienr.|  
    |1002|2|SN1|  
    |1002|2|SN2|  

4.  Vælg handlingen **Opdater produktionsordre**, og vælg derefter knappen **OK** for at udfylde linjen.  
5.  Hvis du vil angive serienumre, skal du vælg handlingen **Varesporingslinjer**.  
6.  På siden **Varesporingslinjer** skal du udfylde felterne **Serienr.** og **Antal (basis)** og derefter lukke siden.  

    Derefter skal du bogføre forbruget af racerstel fra LOT1.  
7.  På siden **Frigivet produktionsordre** skal du vælge handlingen **Produktionskladde**.  
8.  Vælg forbrugslinjen for vare 2000 på siden **Produktionskladde**, og vælg handlingen **Varesporingslinjer**.
9. På siden **Varesporingslinjer** skal du vælge feltet **Lotnr.**, vælge **LOT1** og derefter vælge knappen **OK**.  
10. Lad alle andre standardindstillinger stå på siden **Produktionskladde**, og vælg derefter handlingen **Bogfør**.  

    Dernæst skal producere to yderligere racercykler, SN3 og SN4.  

11. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Frigivne produktionsordrer**, og vælg derefter det relaterede link.  
12. Vælg handlingen **Ny**.  
13. Opret en ny frigivet produktionsordre ved at udfylde følgende felter i hovedet.  

    |Kildenr.|Antal|Serienr.|  
    |----------------|--------------|----------------|  
    |1002|2|SN3|  
    |1002|2|SN4|  

14. Vælg handlingen **Opdater produktionsordre** for at udfylde linjen.  
15. Hvis du vil angive serienumre, skal du vælge handlingen **Varesporingslinjer** og derefter numrene på to linjer i feltet **Serienr.** på siden **Varesporingslinjer**.  

    Derefter skal du bogføre flere forbrug af racerstel fra LOT1.  
16. På siden **Frigivet produktionsordre** skal du vælge handlingen **Produktionskladde**.  
17. Vælg forbrugslinjen for vare 2000 på siden **Produktionskladde**, og vælg handlingen **Varesporingslinjer**.
18. På siden **Varesporingslinjer** skal du vælge feltet **Lotnr.**, vælge **LOT1** og derefter vælge knappen **OK**.  
19. Lad alle andre standardindstillinger stå på siden **Produktionskladde**, og vælg derefter handlingen **Bogfør**.  

    Du har produceret fire racercykler, SN1 til SN4, og forbrugt fire af ti racerstel fra LOT1, to stel i hver produktionsordre.  

20. Luk produktionskladden og produktionsordrer.  

    Dernæst skal sælge racercykler. Først skal du sælge racercykler med SN1 til Ravel Møbler A/S.  

### <a name="to-sell-the-end-items"></a>Sælge færdigvarer  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**, og opret derefter en salgsordre ved at udfylde følgende felter.  

    |Debitor|Vare|Antal|Serienr.|  
    |--------------|----------|----------|----------------|  
    |Ravel Møbler|1002|1|SN1|  

3.  Hvis du vil angive serienummeret, skal du vælge handlingen **Varesporingslinjer** og derefter nummeret i feltet **Serienr.** på siden **Varesporingslinjer**.  
4.  Vælg handlingen **Bogfør**, vælg indstillingen **Lever og fakturer**, og vælg derefter knappen **OK**.  

    Derefter skal du sælge racercyklen med SN2 til Kontorcentralen A/S.  

5.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.  
6.  Vælg handlingen **Ny**, og opret derefter en salgsordre ved at udfylde følgende felter.  

    |Debitor|Vare|Antal|Serienr.|  
    |--------------|----------|----------|----------------|  
    |Kontorcentralen A/S|1002|1|SN2|  

7.  Hvis du vil angive serienummeret, skal du vælge handlingen **Varesporingslinjer** og derefter nummeret i feltet **Serienr.** på siden **Varesporingslinjer**.  
8.  Vælg handlingen **Bogfør**, vælg indstillingen **Lever og fakturer**, og vælg derefter knappen **OK**.  

    Til sidst skal du sælge nogle racerstel separat. Kontorcentralen A/S bestiller også fire separate racerstel til deres egen montagelinje.  

9. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.  
10. Vælg handlingen **Ny**, og opret derefter en salgsordre ved at udfylde følgende felter.  

    |Debitor|Vare|Antal|Serienr.|  
    |--------------|----------|----------|----------------|  
    |Kontorcentralen A/S|2000|5|LOT1|  

11. Hvis du vil angive serienummeret, skal du i oversigtspanelet **Linjer** i gruppen **Linje** vælge handlingen **Varesporingslinjer** og derefter nummeret i feltet **Serienr.** på siden **Varesporingslinjer**.  

    > [!NOTE]  
    >  Bogfør ikke den sidste salgsordre på fem racerstel.  

    Dermed er klargøringen af data til demonstrationen af varesporings- og navigationsfunktionerne færdig.  

## <a name="tracing-from-usage-to-origin"></a>Sporing fra brug til oprindelse  
 Salgsafdelingen har fortalt den ansvarlige for kvalitetssikring, at den returnerede racercykel, vare 1002, har serienummeret SN1. Ved at anvende denne grundlæggende oplysning kan han finde ud af, hvor racercyklen sidst blev brugt, i dette tilfælde som salgsleverance til Ravel Møbler. Den ansvarlige for kvalitetssikringen skal derefter foretage en sporing tilbage til den tidligste oprindelse for at finde ud af, hvilket lotnummer det fejlbehæftede racerstel kom fra, og hvilken leverandør der leverede det.  

### <a name="to-determine-which-lot-included-the-faulty-frame-and-who-supplied-it"></a>Sådan finder du ud af, hvilket lot det fejlbehæftede stel kommer fra, og hvem der leverede det  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varesporing**, og vælg derefter det relaterede link.  
2.  På siden **Varesporing** skal du indtaste **SN1** i feltet **Serienr.filter** og derefter indtaste **1002** i feltet **Varefilter**.  
3.  Behold standardindstillingen **Kun varesporing** i feltet **Vis komponenter**, og behold standardsporingsmetoden **Brug - Oprindelse** i **Sporingsmetode**.  
4.  Vælg handlingen **Sporing**.  

    Bemærk, at ét af salgsleverancehovederne svarer til søgekriterierne. Før du fortsætter sporingen, skal du kontrollere, at leverancen er den samme som den med leverancen af den fejlbehæftede racercykel til Ravel Møbler.  

5.  Vælg sporingslinjen, og vælg derefter handlingen **Vis bilag**.  

    Forsæt nu til sporingen af oprindelsen af salgsleverancen af racercyklen med nummeret SN1.  
6.  Vælg ikonet + på sporingslinjerne for at udvide og foretage sporingen gradvist tilbage i den transaktionskæde, som salgsleverancen kommer fra.  

    Du kan spore følgende transaktionsoversigt:  

    -   Det første bogførte bilag tilbage i kæden af transaktioner er udleveringsbogføringen af SN1 fra den første frigivne produktionsordre.  
    -   Det næste bogførte bilag tilbage efter dette er forbrugsbogføringen fra den første frigivne produktionsordre. Her kan den ansvarlige for kvalitetssikring se, at det er racerstellet fra LOT1, der blev anvendt.  
    -   Det laveste bogførte bilag i denne kæde er den bogførte købsleverance, som racerstellene med LOT1 blev modtaget på lageret med.  

    Den ansvarlige for kvalitetssikringen har nu fastlagt, hvilket lot de fejlbehæftede racerstel kommer fra, og kan se, hvilken kreditor der leverede dem, nemlig Custom Metals Incorporated.  

    > [!NOTE]  
    >  Du skal ikke foretage yderligere ændringer i sporingsresultatet, da du skal bruge det i næste sektion.  

     Dermed er den første opgave med administration af fejlbehæftede varer ved hjælp af siden **Varesporing** udført. Den ansvarlige for kvalitetssikring skal nu finde ud af, om der er andre bogførte bilag, hvor der indgår racerstel fra LOT1.  

## <a name="tracing-from-origin-to-usage"></a>Sporing fra oprindelse til brug  
 Den ansvarlige for kvalitetssikring har fastlagt, at de fejlbehæftede racerstel kom fra LOT1. Han skal nu finde eventuelt andre racercykler, der bruger racerstel fra det fejlbehæftede lot, således at disse cykler kan stoppes eller tilbagekaldes.  

 En måde, du kan forberede denne sporingsopgave på siden **Varesporing** på, er manuelt at indtaste LOT1 i feltet **Lotnr.filter** og 2000 i feltet **Varefilter**. I denne gennemgang vil vi dog bruge funktionen **Spor modsat - fra linje**.  

### <a name="to-find-all-usage-of-the-faulty-lot"></a>Sådan findes alle anvendelser af det fejlbehæftede lot  

1.  Vælg linjen med købsleverancen, den sidste sporingslinje, på siden **Varesporing**, og vælg derefter **Spor modsat - fra linje**.  

    Sporingsresultatet er nu baseret på filtrene på sporingslinjen for købsleverancen, LOT1 og vare 2000, og resultatet er baseret på sporingsmetoden **Oprindelse - Brug**.  

    Hvis du vil have vist en oversigt over alle anvendelser af vare 2000 med LOT1, skal du fortsætte med at udvide alle sporingslinjer.  

2.  Vælg handlingen **Udvid alle**.  

    De første fire sporingslinjer refererer til salgsleverancen til Ravel Møbler, der allerede er afklaret. Den sidste linje indikerer, at der er produceret én til racercykel, SN2, i samme frigivne produktionsordre, og at den derefter er solgt og leveret med en anden salgsleverance.  

    Den ansvarlige for kvalitetssikring informerer straks salgsafdelingen, så de kan foretage en tilbagekaldelse af den fejlbehæftede racercykel fra kunden Kontorcentralen A/S.  

    Han kan samtidig se ud af de tre sidste sporingslinjer, at der er fremstillet to andre varer, SN3 og SN4, med racerstel fra LOT1. Han tager handling for at blokere disse slutvarer på lageret.  

    Dermed er den anden opgave med administration af fejlbehæftede varer ved hjælp af siden **Varesporing** udført. Da siden **Varesporing** kun er baseret på de bogførte poster, skal den ansvarlige for kvalitetssikringen fortsætte til siden **Naviger** for at sikre, at LOT1 ikke er brugt i ikke-bogførte bilag.  

## <a name="finding-all-records-of-a-seriallot-number"></a>Find alle poster for et serie-/lotnummer  
 Den ansvarlige for kvalitetssikringen brugte siden **Varesporing** til at finde ud af, at LOT1 indeholdt fejlbehæftede racerstel, hvem leverandøren var, og i hvilken bogførte transaktion de er brugt. Han skal nu finde ud af, om LOT1 findes i eventuelle andre åbne bilag, ved integrering af sporingsresultatet til siden **Naviger**, hvor han kan foretage en søgning i alle databaseposter.  

### <a name="to-find-all-occurrences-of-lot1-in-non-posted-records-such-as-open-orders"></a>Sådan findes alle forekomster af LOT1 i ikke-bogførte poster, som f.eks. åbne ordrer  

1.  Vælg markøren i første sporingslinje på siden **Varesporing**, dvs. købsleverancen for LOT1.  
2.  Vælg handlingen **Naviger**.  

    Siden **Naviger** er forudindstillet med søgefiltre, der er baseret på sporingsresultatet for LOT1. Den ansvarlige for kvalitetssikring kan genkende de fleste poster som tilhørende bilag, der allerede er identificeret på siden **Varesporing**. Den sidste navigationslinje af typen Produktionsordre refererer til to frigivne produktionsordrer, der har brugt racerstellene fra LOT1.  

    Den anden navigeringslinje af typen **Salgslinje** er en ikke-bogført dokumentlinje, så den undersøger den ansvarlige for kvalitetssikring.  

3.  Vælg den anden navigationslinje for at åbne salgslinjeposten, og vælg handlingen **Vis**. Du kan også vælge værdien i feltet **Antal poster**.  

    Her kan den ansvarlige for kvalitetssikringen se, at der er en åben salgslinje for de fejlbehæftede racerstel. Han foreslår straks salgsafdelingen, at denne ordre annulleres, og at der startes en ny produktionsordre, der er baseret op fejlfrie racerstel.  

 Dermed er denne gennemgang i, hvordan siden **Naviger** bruges til administration af fejlbehæftede varer sammen med siden **Varesporing**, færdig.  

## <a name="see-also"></a>Se også
[Arbejde med serienumre og lotnumre](inventory-how-work-item-tracking.md)  
[Spore vare via varesporing](inventory-how-to-trace-item-tracked-items.md)  
[Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
