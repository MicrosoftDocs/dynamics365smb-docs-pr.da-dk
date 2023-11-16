---
title: Periodisere indtægter og udgifter
description: 'For at genkende indtægter og udgifter i perioder, hvor transaktionen ikke blev bogført, kan du automatisk periodisere eller udskyde dem inden for et angivet skema.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: '1700, 1701, 1702, 1703, 1704, 1705, 1706, 1707'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="defer-revenues-and-expenses"></a>Periodisere indtægter og udgifter

For at genkende en indtægt eller udgift i en periode ud over den periode, hvor transaktionen blev bogført, kan du bruge funktionen til automatisk periodisering af indtægter og udgifter inden for et angivet skema.

For at fordele indtægter eller udgifter på de involverede regnskabsperioder, skal du oprette en periodiseringsskabelon for den ressource, vare eller finanskonto, som indtægten eller udgiften skal bogføres til. Når du bogfører det relaterede salgs- eller købsbilag, periodiseres indtægten eller udgiften til de involverede regnskabsperioder i overensstemmelse med en periodiseringsplan, som er omfattet af indstillingerne i periodiseringsskabelonen og bogføringsdatoen.

## <a name="to-set-up-a-gl-account-for-deferral"></a>Sådan konfigureres en finanskonti til periodisering

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov for at oprette en finanskonto til udskudte indtægter. Du kan finde flere oplysninger i [Finans- og kontoplanen](finance-general-ledger.md).
4. Gentag trin 2 og 3 for at oprette en ny finanskonto til udskudte udgifter.

For begge typer periodisering skal du vælge **Balance** i feltet **Type**, og navngiv kontiene efter forholdene som f.eks. "Ikke-indtjent indtægt" for udskudte indtægter og "Ubetalte udgifter" for udskudte udgifter.

## <a name="to-set-up-a-deferral-template"></a>Sådan konfigureres en periodiseringsskabelon

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Periodiseringsskabeloner**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov.
4. I feltet **Bergn.metode** skal du angive, hvordan feltet **Beløb** for hver periode på siden **Periodiseringsplan** beregnes. Du kan vælge mellem disse indstillinger:

   * **Lineær**: De periodiserede beløb beregnes i overensstemmelse med antallet af perioder, fordelt efter periodelængde.
   * **Lig med pr. periode**: De periodiserede beløb beregnes i overensstemmelse med antallet af perioder, fordelt jævnt på perioderne.
   * **Dage pr. periode**: De periodiserede beløb beregnes i overensstemmelse med antallet af dage i perioden.
   * **Brugerdefineret**: De periodiserede beløb beregnes ikke. Du skal udfylde feltet **Beløb** manuelt for hver periode på siden Periodiseringsplan. Du kan finde flere oplysninger i afsnittet "Sådan ændres en periodiseringsplan fra en salgsfaktura".
5. I feltet **Periodebeskr.** skal du angive en beskrivelse, der vises ved poster for periodiseringsbogføringen. Du kan angive følgende pladsholderkoder for typiske værdier, der indsættes automatisk, når periodebeskrivelsen vises.

   * %1 = Dagens nummer for periodens bogføringsdato
   * %2 = Ugens nummer for periodens bogføringsdato
   * %3 = Månedens nummer for periodens bogføringsdato
   * %4 = Månedens navn for periodens bogføringsdato
   * %5 = Regnskabsperiodens navn for periodens bogføringsdato
   * %6 = Regnskabsåret for periodens bogføringsdato

Eksempel: Bogføringsdatoen er 06-02-2016. Hvis du angiver "Udgifter udskudt for %4 %6", vil den viste beskrivelse være "Udgifter udskudt for februar 2016".

## <a name="to-assign-a-deferral-template-to-an-item"></a>Sådan tildeles en periodiseringsskabelon til en vare

> [!NOTE]  
> Trinnene i denne procedure er de samme, som når du knytter en periodiseringsskabelon til en finanskonto eller en ressource.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vare**, og vælg derefter det relaterede link.
2. Åbn kortet for den vare, for hvilken indtægter eller udgifter skal udskydes til de regnskabsperioder, hvor varen blev solgt eller købt.
3. I feltet **Standardperiodiseringsskabelon** skal du vælge den relevante periodiseringsskabelon.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>Sådan ændres en periodiseringsplan fra en salgsfaktura

> [!NOTE]  
> Trinnene i denne procedure er de samme, som når du ændrer en periodiseringsplan for udgifter fra en købsfaktura.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.
2. Opret en salgsfaktura for en vare, der er tildelt en periodiseringsskabelon. Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md).

    Bemærk, at så snart du indtaster varen (eller ressourcen eller finanskontoen) på fakturalinjen, udfyldes feltet **Periodiseringskode** med koden for den tildelte periodiseringsskabelon.
3. Vælg handlingen **Periodiseringsplan**.
4. På siden **Periodiseringsplan** skal du ændre indstillingerne i hovedet eller værdierne på linjerne, f.eks. for at udskyde beløbet til en supplerende regnskabsperiode.
5. Vælg handlingen **Beregn plan**.
6. Vælg knappen **OK**. Periodiseringsplanen opdateres for salgsfakturaen. Den relaterede periodiseringsskabelon er ændret.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Sådan får du vist, hvordan udskudte indtægter eller udgifter vil blive bogført i finansregnskabet

> [!NOTE]  
> Trinnene i denne procedure er de samme, som når du får vist, hvordan udgiftsperiodiseringer bogføres.

1. På siden **Salgsfaktura** skal du vælge handlingen **Vis bogføring**.
2. På siden **Vis bogføring** skal du vælge handlingen **Finanspost** og derefter vælge handlingen **Vis relaterede poster**.

Finansposter, der skal bogføres på den angivne periodiseringskonto, f.eks. Ikke-indtjent indtægt, angives med den beskrivelse, som du har angivet i feltet **Periodebeskr.** i periodiseringsskabelonen, f.eks. "Udgifter udskudt for februar 2016".

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>Sådan vises bogførte periodiseringer i rapporten Oversigt over salgsperiodisering

> [!NOTE]  
> Trinnene i denne procedure er de samme, som når du gennemser rapporten Oversigt over købsperiodisering.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Oversigt over salgsperiodisering**, og vælg derefter det relaterede link.
2. På siden **Oversigt over salgsperiodisering** i feltet **Balance pr.** skal du angive den dato, indtil hvilken du vil have vist udskudte indtægter.
3. Vælg knappen **Vis eksempel**.

## <a name="to-specify-a-period-in-which-to-allow-deferral-posting"></a>Sådan angives en periode, hvor der kan tillades periodiseringsbogføring

Du kan angive en periode, hvor der kan bogføres transaktioner ved at angive datoer i felterne **Tillad bogføring fra** og **Tillad bogføring til** på følgende måde:

* På siden **Finansopsætning** for alle brugere
* Til bestemte brugere på siden **Brugeropsætning**

Hvis du har gjort det, skal du angive en undtagelse for periodiseringer, så de kan bogføres uden for perioden. Hvis du vil definere perioden, skal du gøre følgende.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af Finans** eller **Brugeropsætning**, og vælg derefter det relaterede link.
2. Angiv en start-og slutdato for perioden i feltet **Tillad udsættelsens bogføring fra** og **Tillad udsættelsens bogføring til**.

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
