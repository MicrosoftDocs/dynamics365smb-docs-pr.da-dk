---
title: Opret en ny fastlagt produktionsordre og ændre den
description: 'Gennemgang af en produktionsplanlægger hos contoso Coffee, som vil oprette en fastlagt produktionsordre og derefter redigere den.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-create-a-firm-planned-production-order-and-change-it"></a>Gennemgang: Opret en ny fastlagt produktionsordre og ændre den

I denne artikel kommer vi igennem de trin, du skal benytte, når du skal arbejde med produktionsordrer fra Contoso Coffee.  

## <a name="scenario"></a>Scenarie

Eduardo, der er produktionsplanlægger hos Contoso Coffee, skal oprette en ny produktionsordre på 10 enheder af varen **SP-SCM1009, Airpot**, der skal betales den 28. april. Eduardo bagudretter planlægningen og bekræfter, at de kan starte ordren den 27. april.  

Kort efter at han har afsluttet opgaven, bliver Eduardo bedt om at øge ordren til 50 enheder. Hvis det er tilfældet, skubber den bagudrettede planlægningsfunktion den første rækkefølge. Så Eduardo videresender ordren fra den 23. april for at fastlægge en mere realistisk slutdato.  

## <a name="steps"></a>Trin

1. Opret den første produktionsordre på 10 enheder af varen **SP-SCM1009, Airpot**.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Fastlagte produktionsordrer**, og vælg derefter det relaterede link.  

    2. Vælg handlingen **Ny**, og udfyld derefter felterne som beskrevet i følgende tabel.  

        |Felt  |Værdi  |
        |---------|---------|
        |**Kildetype** |Vare|
        |**Kildenr.** |SP-SCM1009|
        |**Antal** |10|
        |**Forfaldsdato**|April 28  |

    3. Vælg handlingen **Opdater produktionsordre**.  

    4. På siden **Opdater produktionsordre** accepteres alle standardindstillinger på siden , og klik derefter på knappen **OK** for at starte processen.  

        I den aktuelle opsætning anvendes baglæns planlægning. I den nye linje på produktionsordren er startdatoen 26. april.  

2. Skift produktionsordrens antal til 50 enheder, og Planlæg ordren.  

    1. I oversigtspanelet **Linjer** til **produktionsstyklisten** vælges den linje, du lige har tilføjet, og angiv derefter **50** i feltet *Antal*.  

3. Vælg handlingen **Opdater produktionsordre**.  

    Startdatoen er nu blevet skubbet tilbage til 20. april. Dette er ikke en acceptabel dato for Eduardo.

4. Udløs en forlæns planlægning af produktionsordren.

    1. I oversigtspanelet **Planlæg** skal du angive feltet **Startdato** til *23. april*.

    Starten af ordren er nu 25. april, og slutdatoen er 2. maj. Ordrens forfaldsdato angives én dag senere, 3. maj. Eduardo ved nu, at den vil tage indtil den 3. maj at levere den øgede ordre.

> [!NOTE]
> Planlægning af en ordre ved at ændre dens start-eller slutdato, kræver ikke **opdatering af produktionsordren**, fordi alle datoer genberegnes automatisk.

Den nye produktionsordre er nu oprettet, og Eduardos anmodning imødekommes.  

## <a name="see-also"></a>Se også

[Introduktion til demonstrationsdata for Contoso Coffee](../contoso-coffee-intro.md)  
