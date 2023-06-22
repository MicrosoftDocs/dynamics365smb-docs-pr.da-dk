---
title: Analysere data efter dimensioner
description: 'Denne artikel beskriver, hvordan du kan analysere forretningsdata efter dimensioner for at få større viden om din virksomhed.'
author: edupont
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: edupont
---
# <a name="analyze-data-by-dimensions" />Analysere data efter dimensioner

I finansielle analyser er en dimension data, som du kan føje til en post som en slags markør. Disse data bruges til at gruppere poster med ens karakteristika, f.eks. debitorer, regioner, produkter og sælger, og disse grupper kan nemt hentes frem til analyse. Dimensioner kan bruges til poster i kladder, dokumenter og budgetter. 

Hver "dimension" beskriver analysens fokus. En todimensional analyse kan f.eks. være pr. område. Når der bruges mere end to dimensioner ved oprettelsen af en post, kan du udføre mere komplekse analyser, f.eks. salg pr. salgskampagne pr. kundegruppe pr. område. Så får du større indsigt i din forretning, så du kan evaluere oplysningerne, f.eks. om hvor godt din forretning kører, hvor den blomster og hvor det ikke gør det, og hvor der bør allokeres flere ressourcer, så du kan tage bedre beslutninger undervejs. Flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

> [!TIP]
> For hurtigt at analysere transaktionsdata efter dimensioner kan du filtrere totaler i kontoplanen og poster på alle sider af typen **Poster** efter dimensioner. Kig efter handlingen **Angiv dimensionsfilter**.

> [!NOTE]
> Hvis du opdager, at der er anvendt en forkert dimensionsværdi på bogførte finansposter, kan du rette den og opdatere dine analysevisninger. Du kan finde flere oplysninger i [Fejlfinding og udbedring af dimensioner](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="set-up-an-analysis-view" />Konfigurere en analysevisning

En dimensionsanalyse bruger en valgt kombination af dimensioner. Du lagrer, henter og opdaterer dimensionsgruppen ved at oprette et **Analysevisning**-kort. 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Analysevisninger**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** på siden **Analysevisningsoversigt**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Du kan tilføje andre dimensionskoder til de fire i oversigtspanelet **Dimensioner** ved at vælger handlingen **Filter**, udfylde felterne og derefter vælge knappen **OK**.  
5. Hvis du vil opdatere visningen, skal du vælge handlingen **Opdater**.

## <a name="analyze-by-dimensions" />Analysere efter dimensioner

Brug de analysevisninger, du allerede har oprettet med matrixen **Dimensionsanalyse**, til at få vist beløbene i finans.   

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Analysevisninger**, og vælg derefter det relaterede link.  
2. Vælg den relevante analysevisning, og vælg derefter handlingen **Dimensionsanalyse**.
3. Øverst på siden **Dimensionsanalyse** skal du udfylde felterne for at definere, hvilke data der vises og hvordan.
4. Vælg handlingen **Vis Matrix** for at åbne den respektive matrixside for den definerede analysevisning.
5. Hvis du vil se en specifikation af et beløb på matrixsiden, skal du vælge beløbet for at gå ned i detaljerne.  

- Kolonnen længst til venstre indeholder oplysninger, der er baseret på, hvad du har valgt i feltet **Vis som linjer** i hovedet.  
- Kolonnen længst til højre indeholder oplysninger, der er baseret på, hvad du har valgt i feltet **Vis som kolonner** i hovedet.

> [!IMPORTANT]  
> Du kan ikke vælge en periodelængde som er kortere en den periode, som er angivet på kortet **Analysevisning**. Kommandoerne **Næste sæt** og **Forrige sæt** er inaktive, hvis du har valgt **Periode** i feltet **Vis som linjer** eller **Vis som kolonner**.  

> [!NOTE]  
> Du kan bruge rapporten **Dimensioner - detaljer** til at se en detaljeret klassifikation af, hvordan dimensioner er blevet brugt på poster over en udvalgt periode. Du kan bruge rapporten **Dimensioner - i alt** til kun at få vist de totale beløb.  

> [!TIP]  
> Du kan også ændre visningen ved at ændre indholdet i felterne **Vis som linjer** og **Vis som kolonner**. For at tilbageføre en indstilling for visningen skal du vælge handlingen **Byt om på linjer og kolonner**.

## <a name="update-an-analysis-view" />Opdatere en analysevisning

Beløbene, der vises på siden **Dimensionsanalyse**, viser et billede af virksomhedens tilstand på tidspunktet for den sidste opdatering. Hvis du vil have et billede af den aktuelle tilstand, skal du opdatere analysen ved at bruge opdateringsfunktionen.

Du kan opdatere en analysevisning vha. følgende fremgangsmåde, som startes på siden **Dimensionsanalyse**. Trinnene ligner dem til opdatering af siderne **Analysevisningskort** og **Analysevisningsoversigt**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Analysevisninger**, og vælg derefter det relaterede link.
2. Vælg den relevante analysevisning, og vælg derefter handlingen **Dimensionsanalyse**.
3. På siden **Dimensionsanalyse** skal du markere feltet **Analysekode**.  
4. Vælg linjen med den relevante analysevisning.  
5. På siden **Analysevisninger** skal du vælge analysevisningen og derefter vælge handlingen **Opdater**.  

> [!TIP]  
> Hvis du markerer afkrydsningsfeltet **Opdater ved bogføring** på et analysevisningskort, opdateres visningen automatisk, når en tilknyttet transaktion bogføres.

> [!NOTE]  
> Du kan opdatere nogle eller alle analyser samtidig ved at bruge kørslen **Opdater analysevisninger**.  

## <a name="see-related-training-at-microsoft-learnlearnmodulesdimensions-financial-reports-dynamics--business-centralindex" />Se relateret træning på [Microsoft Learn](/learn/modules/dimensions-financial-reports-dynamics-365-business-central/index).

## <a name="see-also" />Se også

[Financial Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
