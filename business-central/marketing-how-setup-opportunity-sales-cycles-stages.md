---
title: Konfigurere salgsprocesser og -procesfaser for leads
description: 'Beskriver, hvordan du definerer salgsfaser fra første kontakt til afslutningen for at oprette en salgsproces og tildele den til leads i Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5122, 5121, 5120, 5175, 5119, 5098, 5096'
ms.date: 05/27/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Konfigurere salgsprocesser og -procesfaser for leads

Før du begynder at bruge salgsleads, skal du definere salgsprocesser og salgsprocesfaser. En salgsproces består af en række faser, der går fra den første kontakt til afslutningen af et salg. Hvert trin kan have bestemte krav, der skal opfyldes, f.eks kræve et salgstilbud, før et lead kan gå til næste fase. Du kan også angive, om en fase kan springes over. Du kan oprette et ubegrænset antal salgsprocesser. Du kan oprette så mange Salgsprocesfaser, som det er nødvendigt, i en salgsproces.

Implementering af salgsprocesser for leads kræver, at du konfigurerer salgsprocessen, definerer de forskellige faser i processen og derefter tildeler processen til leads. Tildeling af den pågældende aktivitet eller opgaver til et lead kan være en del af oprettelsen af en salgsproces.

Denne artikel beskriver også opsætning af opgaver og aktiviteter, og hvordan du kan tildele opgaver til aktiviteter. Du kan finde flere oplysninger i afsnittet [Sådan oprettes aktiviteter til opgaver](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

## Sådan oprettes salgsproceskoder for leads

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **salgsprocesser**, og vælg derefter det relaterede link. Siden **Salgsprocesser** åbnes og viser de eksisterende salgsprocesser.
2. Vælg handlingen **Ny**, og udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Gentag disse trin for hver salgsproces, du vil oprette. Når du har defineret salgsprocesser for leads, kan du definere de forskellige faser i hver proces.

## Sådan defineres salgsprocesfaser for leads

1. På siden **Salgsprocesser** skal du vælge den leadsalgsproces, som du vil definere faserne i, og derefter vælge handlingen **Faser**. Siden **Salgsprocesfaser** åbnes.
2. Vælg handlingen **Ny** for at oprette en ny fase i salgsprocessen.

Gentag disse trin for hver fase, du vil definere i salgsproces.

## Sådan tildeles faser i salgsprocesser til leads

Når du har tilføjet fasen i salgsprocessen for leads, kan du begynde at tilføje salgsprocesser og derefter tildele procesfasen til leads ved at angive feltet **Salgsproceskode**. Du kan finde flere oplysninger i [Oprette salgsleads](marketing-how-create-opportunities.md).

## Sådan defineres aktiviteter til opgaver

Du kan samle flere opgaver, for eksempel opgaver, der hver repræsenterer et trin, i aktiviteter. Aktivitetsopgaver er forbundet med hinanden vha. en datoformel. Du kan tildele aktiviteter til leads, sælgere og kontaktpersoner.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Aktiviteter**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. I oversigtspanelet **Linjer** skal du udfylde felterne efter behov for at definere en eller flere opgaver i aktiviteten.

## Sådan tildeles opgaver eller aktiviteter til leads

Når du har oprettet en opgave, kan du tildele den til et salgslead og dermed tildele aktiviteten, som opgaven tilhører.

> [!NOTE]
> Du kan ikke oprette opgaver af typen *møde* i [!INCLUDE [prod_short](includes/prod_short.md)] online. Egenskaben kræver adgang til en lokal installation.

Nedenfor beskrives, hvordan aktivitetsopgaver tildeles til leads. Trinene er de samme, når du tildeler opgaver til sælgere og kontaktpersoner.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leads**, og vælg derefter det relaterede link.
2. Vælg et lead, og vælg derefter handlingen **Opgaver**.
3. Vælg handlingen **Opret opgave** på siden **Opgaveliste**.
4. På siden **Opret opgave** skal du udfylde felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

    > [!TIP]
    > Bemærk, at i feltet **Lead** tildeles det automatisk til det pågældende lead.
5. Vælg knappen **OK**.
6. På siden **Opgaveliste** skal du vælge den nye opgave og derefter vælge handlingen **Tildel aktiviteter**.
7. På siden **Tildel aktivitet** skal du udfylde felterne efter behov, og derefter vælge knappen **OK**.

## Se også

[Behandling af salgsleads](marketing-processing-sales-opportunities.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]