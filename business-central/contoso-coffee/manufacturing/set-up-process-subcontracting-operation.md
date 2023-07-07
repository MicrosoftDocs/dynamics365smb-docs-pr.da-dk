---
title: Konfigurere og behandle en underleverandørhandling
description: 'Gennemgang for at lære, hvordan du opretter og behandler en underleverandøroperation i Business central.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="set-up-and-process-a-subcontracting-operation"></a>Konfigurere og behandle en underleverandørhandling

I denne artikel kommer vi igennem de trin, du skal benytte, når du skal bruge Contoso Coffee-demodataene i underleverandør.

## <a name="scenario"></a>Scenarie

Du er produktionsplanlægger hos Contoso Coffee. På grund af kapacitetsbegrænsninger skal du planlægge at bruge en underleverandør til at producere varen **SP-SCM1009, Airpot**.

Her kan du oprette en ny frigivet produktionsordre på 12 enheder af vare SP-SCM1009, Airpot, ved hjælp af routing-SP-SCM1009-SUB-2. Du kan bruge underleverandørkladden til at oprette en købsordre for produktionen og afslutte operationen ved at modtage og fakturere købsordren.

## <a name="steps"></a>Trin

1. Opret den nye frigivne produktionsordre på 12 enheder af varen SP-SCM1009, Airpot.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Frigivet produktionsordre**, og vælg derefter det relaterede link.  

    2. Vælg handlingen **Ny**, og udfyld derefter felterne som beskrevet i følgende tabel.  

        |Felt  |Værdi  |
        |---------|---------|
        |**Kildetype** |Vare|
        |**Kildenr.** |SP-SCM1009|
        |**Antal** |100|
    3. Vælg handlingen **Opdater produktionsordre**.  

2. Udskift ruten til SP-SCM1009-SUB-2 i produktionsordrelinjen, og opdater derefter produktionsordren, men kun for rute.  

    1. Føj feltet Produktionsstyklistenr. til linjerne i den frigivne produktionsordre.<!--in code, this is marked as visible=false-->

    2. Ændre feltet **Rutenr.** fra *SP-SCM1009-SERIAL* til *SP-SCM1009-SUB-2*.  

    3. Vælg handlingen **Opdater produktionsordre**.  

    4. På anmodningssiden **Opdater produktionsordre** skal du fjerne markeringen af felterne **linjer** og **komponentbehov**, så opgaven kun køres for ruten, og derefter skal du vælge knappen **OK**.

3. Du kan bruge underleverandørkladden til at oprette en købsordre for underleverandøroperationen på den produktionsordre, du oprettede i trin 2.  

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Underleverandørkladde**, og vælg derefter det relaterede link.  

    2. Vælg handlingen **Beregn underleverandør**.

    3. Vælg feltet **Accepter handlingsmeddelelse** for den nye linje.

    4. Vælg handlingen **Udfør aktionsmeddelelse**.  

    5. Accepter alle standardværdier på anmodningssiden **Udfør aktionsmeddl. - Indk.**, og klik derefter på knappen **OK**.

    6. Når kørslen er færdig, skal du klikke på **OK** for at lukke underleverandørkladden.  

4. Modtag og bogfør indkøbsordren.  

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.  

    2. Find købsordren fra leverandøren 82000 underleverandøren på listen **Købsordrer**.

    3. Udfyld feltet **Kreditors fakturanr.** med *542349*.

    4. Marker linjen i oversigtspanelet **linjer**, og angiv derefter feltet **Købspris** til *18*.

    5. Vælg handlingen **Bogfør**.  

    6. Vælg indstillingen **Modtag og Fakturer** i anmodningsmeddelelsen.  

Resultatet af vare SP-SCM1009 Airpot er nu registreret.

## <a name="see-also"></a>Se også

[Introduktion til demonstrationsdata for Contoso Coffee](../contoso-coffee-intro.md)  
