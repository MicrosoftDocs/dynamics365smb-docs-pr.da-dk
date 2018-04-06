---
title: "Periodisere indtægter og udgifter | Microsoft Docs"
description: "For at genkende indtægter og udgifter i perioder ud over den periode, hvor transaktionen blev bogført, kan du automatisk periodisere eller udskyde dem inden for et angivet skema."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7b7b4ce9d2f464d6e2793a21fa5b321846ba9498
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="defer-revenues-and-expenses"></a>Periodisere indtægter og udgifter
For at genkende en indtægt eller udgift i en periode ud over den periode, hvor transaktionen blev bogført, kan du bruge funktionen til automatisk periodisering af indtægter og udgifter inden for et angivet skema.

For at fordele indtægter eller udgifter på de involverede regnskabsperioder, skal du oprette en periodiseringsskabelon for den ressource, vare eller finanskonto, som indtægten eller udgiften skal bogføres til. Når du bogfører det relaterede salgs- eller købsbilag, periodiseres indtægten eller udgiften til de involverede regnskabsperioder i overensstemmelse med en periodiseringsplan, som er omfattet af indstillingerne i periodiseringsskabelonen og bogføringsdatoen.

## <a name="to-set-up-a-gl-account-for-deferral"></a>Sådan konfigureres en finanskonti til periodisering
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov for at oprette en finanskonto til udskudte indtægter. Du kan finde flere oplysninger i [Finans- og kontoplanen](finance-general-ledger.md).
4. Gentag trin 2 og 3 for at oprette en ny finanskonto til udskudte udgifter.

For begge typer periodisering skal du vælge **Balance** i feltet **Type**, og navngiv kontiene efter forholdene som f.eks. "Ikke-indtjent indtægt" for udskudte indtægter og "Ubetalte udgifter" for udskudte udgifter.

## <a name="to-set-up-a-deferral-template"></a>Sådan konfigureres en periodiseringsskabelon
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Periodiseringsskabeloner**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov.
4. I feltet **Bergn.metode** skal du angive, hvordan feltet **Beløb** for hver periode i vinduet **Periodiseringsplan** beregnes. Du kan vælge mellem disse indstillinger:

   * **Lineær**: De periodiserede beløb beregnes i overensstemmelse med antallet af perioder, fordelt efter periodelængde.
   * **Lig med pr. periode**: De periodiserede beløb beregnes i overensstemmelse med antallet af perioder, fordelt jævnt på perioderne.
   * **Dage pr. periode**: De periodiserede beløb beregnes i overensstemmelse med antallet af dage i perioden.
   * **Brugerdefineret**: De periodiserede beløb beregnes ikke. Du skal udfylde feltet **Beløb** manuelt for hver periode i vinduet Periodiseringsplan. Du kan finde flere oplysninger i afsnittet "Sådan ændres en periodiseringsplan fra en salgsfaktura".
5. I feltet **Periodebeskr.** skal du angive en beskrivelse, der vises ved poster for periodiseringsbogføringen. Du kan angive følgende pladsholderkoder for typiske værdier, der indsættes automatisk, når periodebeskrivelsen vises.

   * %1 = Dagens nummer for periodens bogføringsdato
   * %2 = Ugens nummer for periodens bogføringsdato
   * %3 = Månedens nummer for periodens bogføringsdato
   * %4 = Månedens navn for periodens bogføringsdato
   * %5 = Regnskabsperiodens navn for periodens bogføringsdato
   * %6 = Regnskabsåret for periodens bogføringsdato

Eksempel: Bogføringsdatoen er 06-02-2016. Hvis du angiver "Udgifter udskudt for %4 %6", vil den viste beskrivelse være "Udgifter udskudt for februar 2016".

## <a name="to-assign-a-deferral-template-to-an-item"></a>Sådan tildeles en periodiseringsskabelon til en vare
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Periodiseringsskabeloner**, og vælg derefter det relaterede link.
2. Åbn kortet for den vare, for hvilken indtægter eller udgifter skal udskydes til de regnskabsperioder, hvor varen blev solgt eller købt.
3. I feltet **Standardperiodiseringsskabelon** skal du vælge den relevante periodiseringsskabelon.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>Sådan ændres en periodiseringsplan fra en salgsfaktura
> [!NOTE]  
>   Trinnene i denne procedure er de samme, som når du ændrer en periodiseringsplan for udgifter fra en købsfaktura.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.
2. Opret en salgsfaktura for en vare, der er tildelt en periodiseringsskabelon. Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md).

    Bemærk, at så snart du indtaster varen (eller ressourcen eller finanskontoen) på fakturalinjen, udfyldes feltet **Periodiseringskode** med koden for den tildelte periodiseringsskabelon.
3. Vælg handlingen **Periodiseringsplan**.
4. I vinduet **Periodiseringsplan** skal du ændre indstillingerne i hovedet eller værdierne på linjerne, f.eks. for at udskyde beløbet til en supplerende regnskabsperiode.
5. Vælg handlingen **Beregn plan**.
6. Vælg knappen **OK**. Periodiseringsplanen opdateres for salgsfakturaen. Den relaterede periodiseringsskabelon er ændret.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Sådan får du vist, hvordan udskudte indtægter eller udgifter vil blive bogført i finansregnskabet
> [!NOTE]  
>   Trinnene i denne procedure er de samme, som når du får vist, hvordan udgiftsperiodiseringer bogføres.

1. I vinduet **Salgsfaktura** skal du vælge handlingen **Vis bogføring**.
2. I vinduet **Vis bogføring** skal du vælge handlingen **Finanspost** og derefter vælge handlingen **Vis relaterede poster**.

Finansposter, der skal bogføres på den angivne periodiseringskonto, f.eks, Ikke-indtjent indtægt, er angivet med den beskrivelse, som du har angivet i feltet **Periodebeskr.** i periodiseringsskabelonen, f.eks. Udgifter udskudt for februar 2016".

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>Sådan vises bogførte periodiseringer i rapporten Oversigt over salgsperiodisering
> [!NOTE]  
>   Trinnene i denne procedure er de samme, som når du gennemser rapporten Oversigt over købsperiodisering.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Oversigt over salgsperiodisering**, og vælg derefter det relaterede link.
2. I vinduet **Oversigt over salgsperiodisering** i feltet **Balance pr.** skal du angive den dato, indtil hvilken du vil have vist udskudte indtægter.
3. Vælg knappen **Vis eksempel**.

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

