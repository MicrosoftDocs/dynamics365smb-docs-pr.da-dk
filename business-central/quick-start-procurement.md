---
title: 'Indkøb, hurtig start (indeholder video)'
description: 'Få mere at vide om, hvordan du udfylder de første kritiske felter om kreditorer i Business central, så du kan begynde at købe produkter og tjenester.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: quickstart
ms.search.form: '26, 27, 50, 56'
ms.date: 09/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Indkøb, Hurtig start

For at kunne købe produkter og tjenester skal du først oprette kreditorer. Når det er gjort, kan du begynde at registrere købsordrer og modtage fakturaer.  

## Oprette kreditorer

Følgende video viser, hvordan du opretter en kreditor i [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

### Opret en ny kreditor

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

Yderligere oplysninger og andre ting, du kan gøre, når du registrerer kreditorer, finder du i [registrere nye kreditorer](purchasing-how-register-new-vendors.md).  

## Opret nye købsordrer

Når du køber noget fra en leverandør, har du to muligheder. Den første og den enkleste er blot at oprette en købsfaktura. Du skal bruge købsordrer, hvis din købsproces kræver, at du kan registrere delleveringer af et ordreantal, f.eks. fordi hele antallet ikke er tilgængeligt hos leverandøren.

Følgende video viser, hvordan du opretter en købsordre i [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

### Oprette en indkøbsordre  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.  

2. Vælg den **nye handling** på siden **indkøbsordrer** for at oprette en ny købsordre.

3. I feltet **Kreditornavn** skal du indtaste navnet på en eksisterende kreditor.

    Andre felter på siden **Købsoverskrift** er nu udfyldt med standardoplysningerne for den valgte kreditor.  

4. Udfylde de resterende felter efter behov på siden **Købsordre**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Du er nu klar til at udfylde købsordrelinjerne med varer eller ressourcer, som du har købt af kreditoren.

5. I oversigtspanelet **Linjer** skal du i feltet **Varenr.** indsætte nummeret på en vare eller en service.

6. Angiv antal varer, der skal købes, i feltet **Antal**.

    Feltet **Linjebeløb** opdateres, så det viser værdien i feltet **Købspris** ganget med værdien i feltet **Antal**.

7. I feltet **Ordrerabatbeløb** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms** nederst i ordren.

8. Når du modtager de købte varer eller servicer, skal du vælge **Bogfør**.

Du kan finde flere oplysninger og yderligere ting, du kan gøre, når du opretter en købsordre, i afsnittet [Indkøb](purchasing-manage-purchasing.md).  

## Opret en købsfaktura  

Du kan oprette en købsfaktura til at registrere omkostningerne ved køb og til at spore i Kreditor. Oprettelse af en købsfaktura svarer til at oprette en købsordre.

### Sådan opretter og bogfører du en købsfaktura  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** på siden **Indkøbsfaktura** for at oprette en ny købsfaktura.
3. I feltet **Kreditor** skal du indtaste navnet på en eksisterende kreditor.

    Andre felter på siden **Købsfaktura** er nu udfyldt med standardoplysningerne for den valgte kreditor.

4. Udfylde de resterende felter efter behov på siden **Købsfaktura**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Du er nu klar til at udfylde købsfakturalinjerne med varer eller ressourcer, som du har købt af kreditoren.

5. I oversigtspanelet **Linjer** skal du i feltet **Varenr.** indsætte nummeret på en vare eller en service.
6. Angiv antal varer, der skal købes, i feltet **Antal**.

    Feltet **Linjebeløb** opdateres, så det viser værdien i feltet **Købspris** ganget med værdien i feltet **Antal**.

7. I feltet **Fakturarabatbeløb** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms** nederst i fakturaen.

8. Når du modtager de købte varer eller servicer, skal du vælge **Bogfør**.

Købet afspejles nu i lagerposter, ressourceposter og finansposter, og kreditorbetalingen aktiveres. Købsfakturaen fjernes fra listen over købsfakturaer og erstattes med et nyt bilag i oversigten over bogførte købsfakturaer.  

Du kan finde flere oplysninger og yderligere ting, du kan gøre, når du opretter en købsfaktura, i afsnittet [Bogfør køb med købsfakturaer](purchasing-how-record-purchases.md).

## Se også

[Hurtig start af Business Central](quick-start-business-central.md)  
[Købsoversigt](Purchasing-manage-purchasing.md)  
[Registrere køb med købsfakturaer](purchasing-how-record-purchases.md)  
