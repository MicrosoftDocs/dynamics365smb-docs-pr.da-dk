---
title: Bruge ikke-fradragsberettiget moms
description: 'I denne artikel forklares, hvordan du kan bruge og rapportere ikke-fradragsberettiget moms.'
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, return, settlement'
ms.search.form: '50, 51, 52, 161, 187, 317, 403, 6640, 9401'
ms.date: 04/26/2023
ms.custom: bap-template
---

# Bruge ikke-fradragsberettiget moms

I denne artikel forklares, hvordan du kan bruge og rapportere ikke-fradragsberettiget moms.

## Oprette en købsfaktura med ikke-fradragsberettiget moms

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.
2. Vælg **Ny** for at oprette en købsfaktura, og angiv de relevante oplysninger i fakturahovedet.
3. Opret en ny linje af typen i afsnittet **Linjer**, baseret på den momsvirksomhedsbogføringsgruppe og momsproduktbogføringsgruppe, hvor du konfigurerer ikke-fradragsberettiget moms.
4. Angiv de relevante værdier i felterne **Antal** og **Købspris**.

    Hvis du har valgt afkrydsningsfeltet **Vis ikke-fra. moms i linjer** på siden **Momsopsætning**, beregnes beløbene i felterne **Ikke-fradragsberettiget momsgrundlag** og  **Ikke-fradragsberettiget momsbeløb** ud fra feltet **Ikke-fradragsberettiget momsprocent** på siden **Momsbogføringsopsætning**.

5. Bogfør fakturaen.

## Oprette en købsordre med ikke-fradragsberettiget moms

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.
2. Vælg **Ny** for at oprette en købsordre, og angiv de relevante oplysninger i dokumenthovedet.
3. Opret en ny linje af typen i afsnittet **Linjer**, baseret på den momsvirksomhedsbogføringsgruppe og momsproduktbogføringsgruppe, hvor du konfigurerer ikke-fradragsberettiget moms.
4. Angiv de relevante værdier i felterne **Antal** og **Købspris**.

    Hvis du har valgt afkrydsningsfeltet **Vis ikke-fra. moms i linjer** på siden **Momsopsætning**, beregnes beløbene i felterne **Ikke-fradragsberettiget momsgrundlag** og  **Ikke-fradragsberettiget momsbeløb** ud fra feltet **Ikke-fradragsberettiget momsprocent** på siden **Momsbogføringsopsætning**.

5. Bogfør købsordren.

## Reguler momsbeløb før bogføring af bilag

Hvis momsbeløb ikke er afrundet på samme måde i miljøet og i det eksterne regnskabssystem (det oprindelige fakturadokument), kan du justere momsbeløbet, inden du bogfører dokumentet. Hvis du vil foretage denne justering, skal du følge disse trin, inden du bogfører dokumentet.

1. Vælg **Statistik** i handlingsruden.
2. Hvis du arbejder med en købsfaktura, skal du følge disse trin:

    1. I oversigtspanelet **Linjer** skal du vælge momsbeløbet eller det ikke-fradragsberettigede momsbeløb.
    2. Angiv de værdier, du har brug for, fra det oprindelige dokument, og luk derefter siden **Købsfakturastatistik**.

3.  Hvis du arbejder med købsordren, skal du følge disse trin:

    1. Vælg **Antal skattelinjer** i oversigtspanelet **Fakturering** for at åbne siden **Momsbeløbslinjer**.
    2. Vælg det momsbeløb eller ikke-fradragsberettigede momsbeløb, som du vil rette.
    3. Angiv de ønskede værdier fra det oprindelige dokument, luk siden **Momsbeløbslinjer**, og luk derefter siden **Købsordrestatistik**.

Hvis du vil bruge reguleringer af momsbeløb, skal du aktivere reguleringerne. Angiv den maksimalt tilladte moms, der skal rettes, i feltet **Maks. momsdifference tilladt** på siden **Regnskabsopsætning**. På siden **Købsopsætning** skal du vælge afkrydsningsfeltet **Tillad momsdifference**.

Du kan justere værdierne i felterne **Momsbeløb** og **Ikke-fradragsbeløb**. Værdien i feltet **Fradragsberettiget momsbeløb** er resultatet af disse to værdier. Det beløb, du angiver i feltet **Ikke-fradragsberettiget momsbeløb**, må ikke være højere end det beløb, du angiver i feltet **Momsbeløb**. Feltet **Maks. momsdifference tilladt** på siden **Regnskabsopsætning** fungerer uafhængigt for fradragsberettigede og ikke-fradragsberettigede momsbeløb på statistiksider, når du vil justere momsbeløb.

> [!IMPORTANT]
> Du kan ikke bruge ikke-fradragsberettiget moms på forudbetalingsfakturaer.

## Se også

[Økonomistyring](finance.md)

[Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md)  

[Oprette ikke-fradragsberettiget moms](finance-setup-nondeductible-vat.md)

[Designoplysninger om ikke-fradragsberettiget moms](design-details-nondeductible-vat.md)

[Rapportere moms til SKAT](finance-how-report-vat.md)

[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
