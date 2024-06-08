---
title: Administrere medarbejderfravær
description: 'Beskriver, hvordan medarbejdernes fraværs-og analyse fravær registreres vha. siderne fraværsregistrering og fravær.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '5200, 5201, 5204, 5206, 5208, 5209, 5211, 5212'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Administrere medarbejderfravær
Hvis du vil administrere en medarbejders fravær, skal du registrere fraværet på siden **Fraværsregistrering**. Det kan derefter vises på forskellige måder i forbindelse med analyse og rapportering.

Du kan få vist medarbejderfravær på to forskellige sider:

* På siden **Fraværsregistrering** registreres alt medarbejderfravær med en linje for hvert fravær.
* På siden **Medarbejderfravær** vises kun fravær for én medarbejder. Det er disse oplysninger, du har angivet på siden **Fraværsregistrering**, og de er her filtreret efter den enkelte medarbejder.

For at statistikkerne kan bruges, skal der altid bruges de samme måleenheder (timer eller dage) ved registrering af medarbejderfravær.

## Sådan registreres medarbejderfravær
Du kan registrere medarbejderfravær dagligt eller med andre intervaller, der opfylder virksomhedens behov.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport**, angive **Fraværsregistrering** og derefter vælge det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld en linje for hvert medarbejderfravær, du vil registrere.
4. Luk siden.

    > [!Tip]
    > Du skal sikre dig brugbare statistikker ved altid at bruge samme måleenhed, time eller dag, når du registrerer medarbejderfravær.

## Sådan får du vist en enkelt medarbejders fravær
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport**, angive **Medarbejdere** og derefter vælge det relaterede link.
2. Markér den relevante medarbejder, og vælg derefter handlingen **Fravær**.

    Siden **Medarbejderfravær** åbnes og viser alt fravær med start- og slutdato for fraværet.

## Sådan får du vist en medarbejders fravær pr. kategori
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport**, angive **Medarbejdere** og derefter vælge det relaterede link.
2. Markér den relevante medarbejder, og vælg derefter handlingen **Fravær pr. kategori**.
3. På siden **Medarbejderfravær pr. kategori** skal du udfylde filterfelterne efter behov, og derefter vælg handlingen **Vis Matrix**.

    Siden **Medarbejderfravær pr. kategori** åbnes og viser alle fravær, opdelt efter fraværsårsag.

## Sådan vises alle medarbejderfravær pr. kategori
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport**, angive **Fraværsregistrering** og derefter vælge det relaterede link.
2. På siden **Fraværsregistrering** skal du vælge handlingen **Oversigt pr. kategori**.
3. På siden **Fraværsoversigt pr. kategori** skal du oprette et filter i feltet **Medarbejdernr.filter** for at få vist medarbejderfraværet for en enkelt medarbejder eller en udvalgt gruppe af medarbejdere.
4. Vælg handlingen **Vis matrix**.

    Siden **Fraværsoversigt pr. kategori** åbnes og viser alle medarbejdernes fravær opdelt efter forskellige fraværsårsager.

## Sådan vises alle medarbejderfravær pr. periode
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport**, angive **Fraværsregistrering** og derefter vælge det relaterede link.
   På siden **Fraværsregistrering** skal du vælge handlingen **Oversigt pr. periode**.
2. På siden **Fraværsoversigt pr. periode** skal du vælge et filter i feltet **Fraværsårsagsfilter** for at få vist medarbejderfravær, der har bestemte årsager.
3. Vælg handlingen **Vis matrix**.

    Siden **Fraværsoversigt pr. periode** åbnes og viser alle medarbejdernes fravær opdelt efter periode.

## Se også
[Administrere personale](hr-manage-human-resources.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]