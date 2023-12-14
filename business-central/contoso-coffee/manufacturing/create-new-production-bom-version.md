---
title: Opret en ny produktionsstykliste og styklisteversion
description: 'Gennemgang for at lære, hvordan du føjer endnu en kaffemaskine til contoso Coffes produktlinje i Business central.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---
# Gennemgang: Opret en ny produktionsstykliste og styklisteversion

I denne artikel kommer vi igennem de trin, du skal benytte, når du skal arbejde Contoso Coffee-demodata til at arbejde med produktionsstyklister i produktionsprocesser.  

## Scenarie

Contoso Coffee har besluttet at føje en anden kaffemaskine til deres produktserie: **SP-SCM1008 Airpot Lite**. Kaffemaskine er identisk med den eksisterende vare **SP-SCM1009 Airpot**, bortset fra at den ikke inkluderer varme pladen, **SP-BOM1104**. I et separat trin, fjernes til/fra-lys **SP-BOM1106**, som er fjernet for en version af Airpot Lite-styklisten.

Oscar, procesteknikeren hos Contoso Coffee skal oprette en ny produktionsstykliste for at definere de oprindelige komponentkrav til Airpot Lite. Oscar skal derefter oprette en ny styklisteversion med startdato for d. 01, for at kunne justere med yderligere planer om frigivelse af en anden udgave.

## Trin

1. Opret en ny produktionsstykliste til Airpot Lite.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Produktionsstykliste**, og vælg derefter det relaterede link.  

    2. Vælg handlingen **Ny**, og udfyld derefter felterne som beskrevet i følgende tabel.  

        |Felt  |Værdi  |
        |---------|---------|
        |**Nummer** |SP-SCM1008|
        |**Beskrivelse** |Airpot Lite|
        |**Enhedskode**|STK  |

2. Kopier styklistekomponenterne fra produktionsstykliste **SP-SCM1009**.

    1. Vælg handlingen **Kopier stykliste**.

    2. På siden **Produktionsstyklister** vælges linjen til **SP-SCM1009, Airpot**, og derefter vælges knappen **OK**.

3. Rediger komponenterne til den nye produktionsstykliste som beskrevet i scenariet.

    1. I oversigtspanelet **Linjer** skal du vælge linjen for elementet **SP-BOM1104** pog derefter vælge handlingen **Slet linje**.  

4. Godkend ny stykliste.  

    1. Vælg **Godkendt** i feltet *Status*.  

5. Opret en ny produktionsstyklisteversion til Airpot Lite.

    1. Vælg handlingen **Versioner**.

    2. Vælg handlingen **Ny**, og udfyld derefter kontofelterne som beskrevet i følgende tabel på siden **Prod.stykl.versionsoversigt** .  

        |Felt  |Værdi  |
        |---------|---------|
        |**Versionskode** |02|
        |**Beskrivelse** |Airpot Lite, v2|
        |**Enhedskode**|STK  |  
        |**Startdato**|Juli 01  |  

6. Kopier komponentlinjerne fra produktionsstyklisten til den nye styklisteversion.

    1. Vælg **Kopier stykliste**-handlingen, og klik derefter på knappen **Ja** for at kopiere komponenterne fra den oprindelige produktionsstykliste.

7. Fjern varen **SP-BOM1106, lys til/fra** fra versionskomponenterne.

8. Godkend ny styklisteversion.

    1. Vælg **Godkendt** i feltet *Status*.  

    2. Luk styklisteversion

Den nye kaffemaskine er nu sat op som en produktionsstykliste med én version.  

## Se også

[Introduktion til demonstrationsdata for Contoso Coffee](../contoso-coffee-intro.md)  
