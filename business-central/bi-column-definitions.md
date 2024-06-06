---
title: Kolonnedefinitioner i Financial Reporting
description: 'Beskriver, hvordan kolonnedefinitioner i Financial Reporting fungerer.'
author: kennieNP
ms.author: kepontop
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# <a name="column-definitions-in-financial-reporting"></a>Kolonnedefinitioner i Financial Reporting

Brug kolonnedefinitioner til at angive, hvilke kolonner der skal med i en rapport. Du kan f.eks. udforme en rapport til sammenligning af bevægelse og saldo til dato for den samme periode dette år og sidste år. Du kan have op til 15 kolonner i en kolonnedefinition. Du kan f.eks. bruge flere kolonner til visning af budgetter for 12 måneder med en kolonne, der viser totalen.

## <a name="create-or-edit-a-column-definition"></a>Oprette eller redigere en kolonnedefinition

Opret eller rediger en kolonnedefinition ved at følge disse trin.

> [!NOTE]
> En udskrevet, vist og gemt version af en finansrapport viser højst fem kolonner. Hvis en finansiel rapport kun er beregnet til analyse på siden **Finansiel rapport**, kan du derimod oprette så mange kolonner, du vil.

1. På siden **Finansielle rapporter** skal du vælge den relevante finansielle rapport, du har oprettet, og vælge **Rediger kolonnedefinition**.
1. På siden **Kolonnedefinition** skal du oprette en række til hver kolonne med finansielle data, der vises efter i finansrapporten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Vælg **OK**.
1. Åbn siden **Finansiel rapport** fra tid til anden for at kontrollere, at den nye kolonnedefinition fungerer korrekt.

## <a name="built-in-column-definitions"></a>Indbyggede kolonnedefinitioner

[!INCLUDE[prod_short](includes/prod_short.md)] Indeholder eksempler på kolonnedefinitioner, der kan hjælpe dig med hurtigt at komme i gang med at oprette finansrapporter, der passer til dine behov.

<!-- update this when we release the new templates in 24.1
| Column definition code | Description | How to use this column definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 |
-->

## <a name="example-create-a-column-definition-to-calculate-percentages"></a>Eksempel: Opret en kolonnedefinition for at beregne procenten

Du vil muligvis gerne medtage en kolonne i en finansiel rapport for at beregne procenter af et totalbeløb. Hvis du f.eks. har et antal rækker, som specificerer salg efter dimension, kan du have en kolonne, som angiver procenten af det samlede salg i hver række.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
1. Vælg en finansiel rapport på siden **Finansielle rapporter**.  
1. Vælg handlingen **Rediger finansiel rapport** for at konfigurere en finansiel rapportrække til beregning af den total, som procentdelene baseres på.  
1. Tilføj en linje lige over den første række, som du vil vise en procent for.  
1. Udfyld felterne på linjen som angivet: 
    1. I feltet **Sammentællingstype** skal du angive **Angiv grundlag for procent**. 
    1. I feltet **Sammentælling** skal du indtaste en formel for den total, som procentdelen skal baseres på. Hvis række 11 f.eks. indeholder det samlede salg, indtastes **11**.  
1. Vælg handlingen **Rediger kolonnedefinition** for at oprette en kolonne.  
1. Udfyld felterne på linjen som angivet. 
    1. I feltet **Kolonnetype** skal du vælge **Formel**. 
    1. I feltet **Formel** skal du indtaste en formel for det beløb, som du vil beregne en procentdel for, efterfulgt af procenttegnet (%). Hvis kolonnenummer N f.eks. indeholder nettoændringen, indtastes **N %**.  
1. Gentag trin 4 til 7 for alle de grupper af rækker, du vil specificere efter procent.

## <a name="comparing-accounting-periods-using-period-formulas"></a>Sammenligne regnskabsperioder ved hjælp af periodeformler

Din finansielle rapport kan sammenligne resultaterne af forskellige regnskabsperioder, f.eks. sidste måned sammenlignet med samme måned sidste år. Hvis du vil gøre det, skal du åbne siden **Kolonnedefinition** og tilpasse den ved at tilføje feltet **Sammenligningsperiodeformel** som en kolonne. Flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md). Du kan derefter angive det pågældende felt til en periodeformel.  

En regnskabsperiode behøver ikke at følge kalenderen. En regnskabsperiode skal ikke følge kalenderåret, men hvert regnskabsår skal have det samme antal regnskabsperioder, selvom hver periode kan variere i længde.  

[!INCLUDE[prod_short](includes/prod_short.md)] bruger periodeformlen til at beregne varigheden af sammenligningsperioden i relation til den periode, som er defineret af datofiltret i rapportanmodningen. Sammenligningsperioden er baseret på perioden fra startdatoen i datofilteret. Følgende tabel viser forkortelserne for periodespecifikationer.

| Forkortelse | Beskrivelse                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode.                                                                                |
| FP           | Forrige periode i et regnskabsår, halvår eller kvartal.                                   |
| CP           | Nuværende periode i et regnskabsår, halvår eller kvartal. Brug CP i formler til at angive den periode, der starter eller afslutter formlen. F.eks. angiver RÅ \[1.NP\] tiden fra begyndelsen af det aktuelle regnskabsår til den aktuelle periode.|
| RÅ           | Regnskabsår. RÅ\[1..3\] betegner f.eks. det første kvartal i det indeværende regnskabsår. |

Eksempler på formler:

| Formel | Beskrivelse |
|-----|-----|
| \<Blank\>       | Aktuel periode. |
| \-1P            | Forrige periode.            |
| \-1RÅ\[1..FP\]  | Hele forrige regnskabsår.                  |
| \-1RÅ           | Den aktuelle periode i forrige regnskabsår.       |
| \-1RÅ\[1..3\]   | Først kvartal i forrige regnskabsår.        |
| \-1RÅ\[1..NP\]  | Fra starten af forrige regnskabsår til den nuværende periode i forrige regnskabsår, begge perioder inklusive. |
| \-1RÅ\[NP..FP\] | Fra den nuværende periode i forrige regnskabsår til sidste periode i forrige regnskabsår, begge perioder inklusive.   |

Hvis du vil foretage beregninger efter almindelige tidsperioder, skal du angive en formel i feltet **Sammenligningsdatoformel** i stedet. Hvis feltet f.eks. er indstillet til -1Å, sammenligner [!INCLUDE [prod_short](includes/prod_short.md)] med samme periode ét år tidligere.

> [!NOTE]
> Det er ikke altid gennemskueligt, hvilke perioder der sammenlignes, fordi du kan indstille et datofilter i en rapport, der dækker andre datoer end de regnskabsperioder, der afspejles i kontoplanen. Hvis du f.eks. vil oprette en finansiel rapport, hvor du vil sammenligne denne periode med samme periode sidste år, skal du indstille feltet **Sammenligningsdatoformel** til **-1RÅ**. Derefter skal du køre rapporten den **28. februar** og indstille datofilteret til **januar og februar**. Den finansielle rapport sammenligner nu januar og februar i indeværende år med januar sidste år, som er den eneste afsluttede regnskabsperiode af de to for sidste år.  

Du kan finde flere oplysninger i [Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md).

[!INCLUDE [report-best-practices-column-defs](includes/report-best-practices-column-defs.md)]

## <a name="import-or-export-financial-report-column-definitions"></a>Importere eller eksportere kolonnedefinitioner til finansrapport

Fra og med udgivelsesbølge 1 i 2024 (version 24.1) kan du importere og eksportere kolonnedefinitioner af finansrapporter som RapidStart konfigurationspakker. Konfigurationspakker er f. eks. nyttige, når du vil dele oplysninger med andre firmaer. Pakken oprettes i en .rapidstart-fil, som komprimerer indholdet.

> [!NOTE]
> Når du importerer finansielle rapport-/kolonnedefinitioner, erstattes eksisterende poster med samme navn som dem, der importeres, med nye definitioner. Konfigurationspakken til en rapportdefinition overskriver ikke eksisterende række- eller kolonnedefinitioner, der bruges i rapportdefinitionen.

Følg disse trin for at importere eller eksportere kolonnedefinitioner af økonomiske rapporter:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kolonnedefinitioner**, og vælg derefter det relaterede link.
1. Vælg rækkedefinitionen, og vælg derefter **Importer kolonnedefinition** eller **Eksporter kolonnedefinition**, afhængigt af hvad du vil gøre.

## <a name="see-also"></a>Se også

[Rækkedefinitioner i Financial Reporting](bi-row-definitions.md)  
[Klargøre Financial Rapportering](bi-how-work-account-schedule.md)  
[Økonomisk Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
