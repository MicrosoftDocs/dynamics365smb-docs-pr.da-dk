---
title: Bogføre årsafslutningsposten
description: 'Beskriver, hvordan du åbner den kladde, du angav i kørslen Nulstil resultatopgørelse, og derefter gennemser og bogfører årsafslutningsposten.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.search.form: 100
ms.date: 08/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="post-the-year-end-closing-entry"></a>Bogføre årsafslutningsposten

Når du har udført kørslen **Nulstil resultatopgørelse** for at oprette årsafslutningens lukkepost eller -poster, skal du åbne den kladde, du angav i kørslen, og derefter gennemse og bogføre posterne.  

> [!TIP]
> Afhængigt af virksomhedens arbejdsprocesser kan du vælge at lukke eller undlade at lukke regnskabsperioder og regnskabsår i [!INCLUDE [prod_short](includes/prod_short.md)]. I følgende procedure antages det, at du har lukket regnskabsåret ved hjælp af indstillingen *Regnskabsperioder*, genererede en årsafslutningspost ved hjælp af kørslen **Nulstil resultatopgørelse** og er nu klar til at bogføre årsafslutningsposten sammen med modregningskontoposterne for egenkapitalen. Organisationen kan vælge at arbejde forskelligt, f.eks. bogføre årsafslutningsposten som en del af lukningen af regnskabsåret.

## <a name="to-post-the-year-end-closing-entry"></a>Sådan bogføre årsafslutningsposten

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Finanskladder**, og vælg derefter det relaterede link.
2. Vælg det **navn, der indeholder ultimoposterne, i feltet** Kladdenavn **på siden Finanskladder** .
3. Gennemse posterne.
4. Vælg handlingen **Bogfør** for at bogføre kladden.

> [!NOTE]  
> Hvis der opstår en fejl, vises der en fejlmeddelelse. Hvis bogføringen lykkes, fjernes de bogførte poster fra kladden. Når bogføringen er fuldført, bogføres en post til alle resultatopgørelseskonti, så saldoen går i nul, og årsresultatet overføres til balancen.

## <a name="see-also"></a>Se også

[Afslutte regnskabsperioder](year-close-account-periods.md)    
[Lukning af bøger](year-close-books.md)    
[Nulstil resultatopgørelse](year-close-income-statement.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
