---
title: Kombinere automatisk og manuel træk
description: 'Gennemgang af en produktionsplanlægger hos Contoso Coffee, som vil kombinere automatisk og manuel træk.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Gennemgang: Kombinere automatisk og manuel træk

I denne artikel kommer vi igennem de trin, du skal benytte, når du skal bruge demonstrationsdataene fra Contoso Coffee.  

## Scenarie

Du er produktionsplanlægger hos Contoso Coffee. Du skal oprette en ny produktionsordre på ti enheder af vare SP-SCM1004, AutoDrip. Nogle komponenter og operationer vil blive tømt, andre tilbage træk baseret på forskellige betingelser.

## Trin

> [Bemærk!] Husk at regulere lagerbeholdningen ved at bogføre varekladder med primosaldi.

1. Opret en fast planlagt produktionsordre på fem enheder af vare **SP-SCM1004, AutoDrip** på lokationen *MAIN*. Du kan finde en vejledning under [Gennemgang: Oprette en fastlagt produktionsordre og ændre den](create-firm-planned-production-order-change.md).  

2. Frigive produktionsordre.

    1. Vælg handlingen **Skift status**.  

    2. Indstil feltet **Ny status** til *Frigivet* på den side, der vises, og klik derefter på knappen **Ja**.  

        Der vises en meddelelse med en statuslinje og en reference til automatisk forbrug. Dette efterfølges af en bekræftelsesmeddelelse om, at ordren er ændret, så den har status *Frigivet*.  

    3. Vælg knappen **OK** for at gemme og lukke bekræftelsesmeddelelsen.

3. Gennemgå vare-og kapacitetsposterne for produktionsordren.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Frigivet produktionsordre**, og vælg derefter det relaterede link.  

    2. Åbn produktionsordren med 5 enheder af AutoDrip kaffemaskine.  

    3. Vælg handlingen **Vareposter**.  

        Elementet **SP-BOM1305 Screw Hex M3 Zink** justeres øjeblikkeligt med det fulde forventede antal. Luk siden **Vareposter**.  

    4. Alternativt kan du vælge handlingen **Kapacitetsposter**.  Bemærk, at en post med centrale samlingshandlinger også blev afsluttet på det øjeblik, da ordren blev frigivet. Luk vinduet **Kapacitetsposter**.

    Du kan manuelt rydde komponentvarer ved hjælp af forbrugs- eller produktionskladden. Ved manuel træk får du mulighed for at justere antal inden bogføring. Hvis du f. eks. har brug for yderligere mængde til at dække råmaterialer i det lave kvalitets materiale.
4. Rydde komponenter manuelt.  
    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forbrugskladde**, og vælg derefter det relaterede link.  

    2. Vælg handlingen **Beregn forbrug**.  

    3. På anmodningssiden **Beregn forbrug** i oversigtspanelet **Produktionsordre** skal du definere et filter for den specifikke ordre i feltet **Ordrenr.** felt, og vælg derefter knappen **OK**. Når kørselssiden lukkes, skal du bemærke, at siden **Forbrugskladde** bliver udfyldt med de komponenter, der kræver manuel forbrug.

    4. Vælg handlingen **Bogfør**. Luk forbrugskladden.

5. Registrere afgang for elektriske kabler manuelt.  

    Udfyld felterne manuelt i **Opstillingstid** og **Operationstid**. Du kan også angive det faktisk producerede antal og spild. Angiv *3* som afgangsantal, og Bogfør afgangen.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afgangskladde**, og vælg derefter det relaterede link.  

    2. På siden **Afgangskladde** skal du oprette en ny kladdelinje.  

    3. I feltet **Ordrenr.** felt, angiv rækkefølgen.  

    4. Vælg **Udfold rute**-handlingen.  

        På siden **afgangskladde** indsættes kun operationslinjen for elektrisk ledning.

    5. Angiv **Kørselstid** til *10*.  

    6. Ret feltet **Mængde** fra *5* til *3*.

    7. Vælg **Bogfør**.  
    8. Luk afgangskladde.

6. Gennemgå vare- og kapacitetsposterne for produktionsordren.

    1. Vælg handlingen **Vareposter** på siden til produktionsordren.  

    Elementet **SP-BOM1302, Kontrolpanelvisning** bogføres med en mængde på *3*, der er baseret på den aktuelle afgang, mens **SP-BOM1303, knap** er markeret med det fulde forventede antal. Luk siden **Vareposter**.

7. Afslut produktionsordre.  

    1. Vælg handlingen **Skift status**.
    2. Indstil feltet **Ny status** til *Afsluttet* på den side, der vises, og klik derefter på knappen **Ja**.  

        Der vises en meddelelse med en statuslinje, der afspejler det automatiske forbrug. Dette efterfølges af en bekræftelsesmeddelelse om, at ordren er ændret, så den har status *Afsluttet*. Den færdige produktionsordre har samme nummer, som det havde med status *Frigivet*.
    3. Vælg knappen **OK** for at gemme og lukke bekræftelsesmeddelelsen.

8. Gennemgå vare- og kapacitetsposterne for produktionsordren igen.

    1. Alternativt kan du vælge handlingen **Kapacitetsposter**.  

        Følge operationsposten er fuldført på det tidspunkt, hvor ordren blev frigivet. Det producerede (afgangsantal) er *5*, uanset output fra det foregående trin. Luk siden **Kapacitetsposter**.

    2. Vælg handlingen **Vareposter**.  

        Mængden i vareposten af typen *Afgang* svarer til afgangsantallet i kapacitetsposten. Det forbrugte antal af **SP-BOM1301, Housing AutoDrip** og **SP-BOM1304, Stainless still thermal carafe** er 5 for begge, fordi den forventede afgang og det faktiske output er det samme. 

    3. Luk siden **Vareposter**.  

Det er den til manuel og automatisk træk af komponenter.

## Se også

[Udtrække komponenter i henhold til operationsafgang](../../production-how-to-flush-components-according-to-operation-output.md)  
[Introduktion til demonstrationsdata for Contoso Coffee](contoso-coffee-manufacturing-intro.md)  
