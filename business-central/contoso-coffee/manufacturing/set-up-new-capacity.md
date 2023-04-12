---
title: Konfigurere ny kapacitet
description: 'Gennemgang for at få mere at vide om, hvordan du opretter et nyt arbejdscenter med en kapacitets kalender til et enkelt skift i Business central.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Gennemgang: Konfigurere ny kapacitet

I denne artikel kommer vi igennem de trin, du skal benytte, til Contoso Coffee-demodata til administration af kapacitet.  

## Scenarie

Du er produktionsplanlægger hos Contoso Coffee. I forbindelse med ændringer i produktionen skal du oprette et nyt arbejdscenter, en testafdeling. Det nye arbejdscenter har én produktionsressource, tester. De nye centre skal have en kapacitetskalender for et enkelt skift fra 08:00:00 til 16:00:00, mandag til fredag.  

## Trin

1. Konfigurere et arbejdscenter.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **arbejdscentre**, og vælg derefter det relaterede link.  

    2. Vælg handlingen **Ny**, og udfyld derefter felterne som beskrevet i følgende tabel.  

        |Felt  |Værdi  |
        |---------|---------|
        |**Nummer** |700|
        |**Navn** |Testafdeling|
        |**Arbejdscentergruppekode** |1. Produktionsafdeling|
        |**Købspris**|3.25|
        |**Kostprisberegning**|Tidspunkt|
        |**Trækmetode**|Manuelt|
        |**Produktbogføringsgruppe**|FRITAGET</br></br>Bemærk, at valget afhænger af din Regnskabsopsætning og-land.|
        |**Enhedskode** |MINUTTER|
        |**Kapacitet** |1|
        |**Effektivitet** |90|
        |**Produktionskalenderkode** |1|

        I feltet **Produktionskalenderkode** betyder indstilling 1 et skift fra mandag til fredag.

    3. Luk arbejdscenterkortet.

2. Sådan opsættes produktionsressourcer.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **produktionsressource**, og vælg derefter det relaterede link.  

    2. Vælg handlingen **Ny**, og udfyld derefter felterne som beskrevet i følgende tabel.  

        |Felt  |Værdi  |
        |---------|---------|
        |**Nummer** |760|
        |**Navn** |Tester|
        |**Arbejdscenternr.** |700, Testafdeling|
        |**Købspris**|3.25|
        |**Trækmetode**|Manuelt|
        |**Produktbogføringsgruppe**|FRITAGET</br></br>Bemærk, at valget afhænger af din Regnskabsopsætning og-land.|
        |**Kapacitet** |1|
        |**Effektivitet** |90|
    3. Udvid oversigtspanelet **ruteopsætning**, og Skriv **10** i feltet *opstillingstid*.  

3. Beregn kapacitet for produktionsressourcekalender.  

    1. Vælg handlingen **Kalender**.  

    2. På siden **Produktionsressourcekalender** skal du i oversigtspanelet **Matrix-indstillinger** angive **Vis efter** til *måned*.  

    3. Vælg handlingen **Vis matrix**.  

    4. På siden **Produktionsressourcekalendermatrix** skal du vælge handlingen **Beregn**.  

    5. På siden **Beregn produktionsressourcekalender** skal du i oversigtspanelet **Indstillinger** angive **Startdato** til *1. januar*.  

    6. Angiv feltet **Slutdato** til 31. december.  

    7. Udfyld feltet **Nummer** i oversigtspanelet **Produktionsressource**. filterfelt, vælg *760, tester*.  

    8. Vælg knappen **OK**. Når kørslen er afsluttet, vender du tilbage til **produktionsressourcekalendermatrix**-siden.  

    9. Vælg handlingen **Opdater**.  

    10. Specificer i kolonnen januar på linjen til produktionsressource 760.  

På siden **kalenderposter** er felterne for daglig kapacitet i feltet **kapacitet (Total)** i 480 minutter. Dette afspejler et otte-timers skift pr. arbejdsdag. Desuden viser feltet **kapacitet (effektiv)** 432 minutter. Dette afspejler den 90 procent effektivitetsprocent, som du har knyttet til produktionsressourcen.  

## Se også

[Introduktion til demonstrationsdata for Contoso Coffee](../contoso-coffee-intro.md)  
