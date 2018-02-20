---
title: Analysere data efter dimensioner | Microsoft Docs
description: Beskriver, hvordan du analyserer forskellige forretningsdata efter dimensioner.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ec3210e019da3369971d3aef6a4e38f4dcf1f530
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
#  <a name="analyze-data-by-dimensions"></a>Analysere data efter dimensioner
I finansielle analyser er en dimension data, som du kan føje til en post som en slags markør. Disse data bruges til at gruppere poster med ens karakteristika, f.eks. debitorer, regioner, produkter og sælger, og disse grupper kan nemt hentes frem til analyse. Dimensioner kan bruges til poster i kladder, dokumenter og budgetter. Selve udtrykket dimension beskriver, hvordan analysen opstår. En todimensional analyse kan f.eks. være pr. område. Men når der bruges mere end to dimensioner ved oprettelsen af en post, kan du udføre mere komplekse analyser, f.eks. salg pr. salgskampagne pr. kundegruppe pr. område. Du kan finde flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

Når du analyserer data efter dimensioner, får du større indsigt i din forretning, så du kan evaluere oplysningerne, f.eks. om hvor godt din forretning kører, hvor den blomster og hvor det ikke gør det, og hvor der bør allokeres flere ressourcer.

> [!TIP]
> For hurtigt at analysere transaktionsdata efter dimensioner kan du filtrere totaler i kontoplanen og poster i alle vinduer af typen **Poster** efter dimensioner. Kig efter handlingen **Angiv dimensionsfilter**.

## <a name="to-set-up-an-analysis-view"></a>Sådan defineres en analyse  
En dimensionsanalyse viser en valgt kombination af dimensioner. Du kan gemme og få vist de analyser, du har oprettet. Opsætningsoplysningerne til en analyse gemmes på et **Analysevisning**-kort, så det fremtidige analysearbejde bliver så nemt som muligt.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Analysevisninger**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** i vinduet **Analysevisningsoversigt**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Du kan tilføje andre dimensionskoder til de fire i oversigtspanelet **Dimensioner** ved at vælger handlingen **Filter**, udfylde felterne og derefter vælge knappen **OK**.  
5. Hvis du vil opdatere visningen, skal du vælge handlingen **Opdater**.

## <a name="to-analyze-by-dimensions"></a>Sådan analyseres dimensioner
I matrixen **Dimensionsanalyse** kan du få vist beløbene i finansposter vha. de analyser, du har oprettet. Udfyld vinduet **Dimensionsanalyse** for at angive, hvad der skal vises i matrixen og vælg derefter handlingen **Vis matrix** for at se matrixen.  

- Kolonnen længst til venstre indeholder oplysninger, der er baseret på, hvad du har valgt i feltet **Vis som linjer** i hovedet.  
- Kolonnen længst til højre indeholder oplysninger, der er baseret på, hvad du har valgt i feltet **Vis som kolonner** i hovedet.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Dimensionsanalyse**, og vælg derefter det relaterede link.  
2. Vælg den relevante analysevisning, og vælg derefter handlingen **Rediger analysevisning**.
3. Øverst i vinduet **Dimensionsanalyse - Salg** skal du udfylde felterne for at definere, hvad der vises.
4. 5. Hvis du vil se en specifikation af et beløb i matrixvinduet, skal du vælge beløbet.  

> [!IMPORTANT]  
>   Du kan ikke vælge en periodelængde som er kortere en den periode, som er angivet på kortet **Analysevisning**. Kommandoerne **Næste sæt** og **Forrige sæt** er deaktiveret, hvis du har valgt **Periode** i feltet **Vis som linjer** eller feltet **Vis som kolonner**.  

> [!NOTE]  
>   Du kan bruge rapporten **Dimensioner - detaljer** til at se en detaljeret klassifikation af, hvordan dimensioner er blevet brugt på poster over en udvalgt periode. Du kan bruge rapporten **Dimensioner - i alt** til kun at få vist de totale beløb.  

> [!TIP]  
>   Du kan også ændre visningen ved at ændre oplysningerne i felterne **Vis som linjer** og **Vis som kolonner**. For at tilbageføre en indstilling for visningen skal du vælge handlingen **Byt om på linjer og kolonner**.

## <a name="to-update-an-analysis-view"></a>Sådan opdateres en analysevisning  
Beløbet, der vises i vinduet **Dimensionsanalyse** viser et billede af virksomhedens tilstand på tidspunktet for den sidste opdatering. Hvis du vil have et billede af den aktuelle tilstand, skal du opdatere analysen ved at bruge opdateringsfunktionen.

Du kan opdatere en analyse vha. følgende fremgangsmåde, som startes i vinduet **Dimensionsanalyse** . Trinene er de samme fra vinduerne **Analysevisningskort** og **Analysevisningsoversigt**.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Dimensionsanalyse**, og vælg derefter det relaterede link.  
2. I vinduet **Dimensionsanalyse** skal du markere feltet **Analysekode**.  
3. Vælg linjen med den relevante analysevisning.  
4. Vælg handlingen **Opdater**.  

> [!TIP]  
>   Hvis du markerer afkrydsningsfeltet **Opdater ved bogføring** på et analysekort, opdateres visningen automatisk, når en involveret transaktion bogføres.

> [!NOTE]  
>   Du kan opdatere nogle eller alle analyser samtidig ved at bruge kørslen **Opdater analysevisninger**.  

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

