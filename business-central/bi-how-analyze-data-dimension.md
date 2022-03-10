---
title: Analysere data efter dimensioner
description: Dette emne beskriver, hvordan du analyserer forskellige forretningsdata efter dimensioner. Med dimensioner får du større indsigt i din virksomhed, så du kan evaluere oplysninger.
author: edupont
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 555, 556, 557, 558, 9372, 9370, 9371
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: ca377898f9dd49a55ec9113fc020054288c33910
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/23/2022
ms.locfileid: "8335054"
---
#  <a name="analyze-data-by-dimensions"></a>Analysere data efter dimensioner
I finansielle analyser er en dimension data, som du kan føje til en post som en slags markør. Disse data bruges til at gruppere poster med ens karakteristika, f.eks. debitorer, regioner, produkter og sælger, og disse grupper kan nemt hentes frem til analyse. Dimensioner kan bruges til poster i kladder, dokumenter og budgetter. Selve udtrykket dimension beskriver, hvordan analysen opstår. En todimensional analyse kan f.eks. være pr. område. Men når der bruges mere end to dimensioner ved oprettelsen af en post, kan du udføre mere komplekse analyser, f.eks. salg pr. salgskampagne pr. kundegruppe pr. område. Du kan finde flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

Når du analyserer data efter dimensioner, får du større indsigt i din forretning, så du kan evaluere oplysningerne, f.eks. om hvor godt din forretning kører, hvor den blomster og hvor det ikke gør det, og hvor der bør allokeres flere ressourcer.

> [!TIP]
> For hurtigt at analysere transaktionsdata efter dimensioner kan du filtrere totaler i kontoplanen og poster på alle sider af typen **Poster** efter dimensioner. Kig efter handlingen **Angiv dimensionsfilter**.

> [!NOTE]
> Hvis du opdager, at der er anvendt en ukorrekt dimension på bogførte finansposter, kan du rette dimensionsværdierne og opdatere dine analysevisninger. Du kan finde flere oplysninger i [Fejlfinding og udbedring af dimensioner](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="to-set-up-an-analysis-view"></a>Sådan defineres en analyse  
En dimensionsanalyse viser en valgt kombination af dimensioner. Du kan gemme og få vist de analyser, du har oprettet. Opsætningsoplysningerne til en analyse gemmes på et **Analysevisning**-kort, så det fremtidige analysearbejde bliver så nemt som muligt.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Analysevisninger**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** på siden **Analysevisningsoversigt**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Du kan tilføje andre dimensionskoder til de fire i oversigtspanelet **Dimensioner** ved at vælger handlingen **Filter**, udfylde felterne og derefter vælge knappen **OK**.  
5. Hvis du vil opdatere visningen, skal du vælge handlingen **Opdater**.

## <a name="to-analyze-by-dimensions"></a>Sådan analyseres dimensioner
I matrixen **Dimensionsanalyse** kan du få vist beløbene i finansposter vha. de analyser, du har oprettet. Udfyld siden **Dimensionsanalyse** for at angive, hvad der skal vises i matrixen og vælg derefter handlingen **Vis matrix** for at se matrixen.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Analysevisninger**, og vælg derefter det relaterede link.  
2. Vælg den relevante analysevisning, og vælg derefter handlingen **Dimensionsanalyse**.
3. Øverst på siden **Dimensionsanalyse** skal du udfylde felterne for at definere, hvilke data der vises og hvordan.
4. Vælg handlingen **Vis Matrix** for at åbne den respektive matrixside for den definerede analysevisning.
5. Hvis du vil se en specifikation af et beløb på matrixsiden, skal du vælge beløbet for at gå ned i detaljerne.  

- Kolonnen længst til venstre indeholder oplysninger, der er baseret på, hvad du har valgt i feltet **Vis som linjer** i hovedet.  
- Kolonnen længst til højre indeholder oplysninger, der er baseret på, hvad du har valgt i feltet **Vis som kolonner** i hovedet.

> [!IMPORTANT]  
>   Du kan ikke vælge en periodelængde som er kortere en den periode, som er angivet på kortet **Analysevisning**. Kommandoerne **Næste sæt** og **Forrige sæt** er deaktiveret, hvis du har valgt **Periode** i feltet **Vis som linjer** eller feltet **Vis som kolonner**.  

> [!NOTE]  
>   Du kan bruge rapporten **Dimensioner - detaljer** til at se en detaljeret klassifikation af, hvordan dimensioner er blevet brugt på poster over en udvalgt periode. Du kan bruge rapporten **Dimensioner - i alt** til kun at få vist de totale beløb.  

> [!TIP]  
>   Du kan også ændre visningen ved at ændre oplysningerne i felterne **Vis som linjer** og **Vis som kolonner**. For at tilbageføre en indstilling for visningen skal du vælge handlingen **Byt om på linjer og kolonner**.

## <a name="to-update-an-analysis-view"></a>Sådan opdateres en analysevisning  
Beløbet, der vises på siden **Dimensionsanalyse** viser et billede af virksomhedens tilstand på tidspunktet for den sidste opdatering. Hvis du vil have et billede af den aktuelle tilstand, skal du opdatere analysen ved at bruge opdateringsfunktionen.

Du kan opdatere en analyse vha. følgende fremgangsmåde, som startes på siden **Dimensionsanalyse** . Trinene er de samme fra siderne **Analysevisningskort** og **Analysevisningsoversigt**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Analysevisninger**, og vælg derefter det relaterede link.
2. Vælg den relevante analysevisning, og vælg derefter handlingen **Dimensionsanalyse**.
2. På siden **Dimensionsanalyse** skal du markere feltet **Analysekode**.  
3. Vælg linjen med den relevante analysevisning.  
4. På siden **Analysevisninger** skal du vælge analysevisningen og derefter vælge handlingen **Opdater**.  

> [!TIP]  
>   Hvis du markerer afkrydsningsfeltet **Opdater ved bogføring** på et analysekort, opdateres visningen automatisk, når en involveret transaktion bogføres.

> [!NOTE]  
>   Du kan opdatere nogle eller alle analyser samtidig ved at bruge kørslen **Opdater analysevisninger**.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/dimensions-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]