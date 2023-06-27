---
title: Bruge Ordreplanlægning til at oprette og reservere levering
description: 'Gennemgang for at lære, hvordan du bruger Ordreplanlægning til at oprette den krævede produktionsordre til levering i Business central.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-use-order-planning-to-create-and-reserve-supply"></a>Gennemgang: Bruge Ordreplanlægning til at oprette og reservere levering

I denne artikel kommer vi igennem de trin, du skal benytte, når du skal bruge Contoso Coffee-demodataene i ordreplanlægning.

## <a name="scenario"></a>Scenarie

Du er produktionsplanlægger hos Contoso Coffee. Du har oprettet en produktionsordre på 100 enheder af varen **SP-SCM1009, Airpot**, og du vil planlægge underordnede samlinger for denne ordre. Du kan bruge Ordreplanlægning til at oprette den krævede produktionsordre til levering. Da du opretter produktionsordren for at opfylde kravene i en bestemt ordre, bestemmer du dig for at reservere produktionsordrens afgang.  

## <a name="steps"></a>Trin

1. Opret den nye frigivne produktionsordre på 100 enheder af varen **SP-SCM1009, Airpot**.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Frigivet produktionsordre**, og vælg derefter det relaterede link.  

    2. Vælg handlingen **Ny**, og udfyld derefter felterne som beskrevet i følgende tabel.  

        |Felt  |Værdi  |
        |---------|---------|
        |**Kildetype** |Vare|
        |**Kildenr.** |SP-SCM1009|
        |**Antal** |100|
    3. Vælg handlingen **Opdater produktionsordre**.  

    Angiver nummeret på den frigivne produktionsordre.

2. Åbn siden **Ordreplanlægning** og beregn en ny plan.

    1. Vælg handlingen **Planlægning**.  

    2. Vælg handlingen **Beregn plan** på siden **Ordreplanlægning**.  

    3. Rul ned til den behovslinje, der repræsenterer den frigivne produktionsordre, du har oprettet tidligere.  

    4. Udvid linjerne for at se detaljerne til behovslinjen. Bekræft, at det er et forslag til en produktionsordre på 100 enheder af vare 1001.  

3. Opret en ny produktionsordre på 100 enheder af vare **SP-BOM2000, Reservoirsaml.**, og reserver afgangen for produktionsordren på vegne af den relaterede overordnede ordre.  

    1. Marker afkrydsningsfeltet **Reserver** på behovslinjen for 100 enheder af vare SP-BOM2000.

    2. Vælg handlingen **Lav ordrer**.  

    3. Angiv feltet **Lav ordrer for** til den *Aktive linje*.  

    4. Indstil feltet **Opret produktionsordre** til *fastlagt*.

    5. Vælg knappen **OK** for at oprette en produktionsordre.

    6. På siden **Ordreplanlægning** skal du bekræfte, at behovslinjen for 100 enheder af vare 1001 er blevet fjernet.

Det var ordreplanlægning i [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## <a name="see-also"></a>Se også

[Introduktion til demonstrationsdata for Contoso Coffee](../contoso-coffee-intro.md)  
[Om produktionsordrer](../../production-about-production-orders.md)  
