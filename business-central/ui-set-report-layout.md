---
title: Indstille rapportlayoutet
description: Få mere at vide om, hvordan du indstiller det layout, der bruges i en rapport, til at få vist udskrift og udskrive.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9652, 9650
ms.date: 08/12/2022
ms.author: jswymer
ms.openlocfilehash: d63bfb699932261e0e9b74ef3aebcbd52bc53604
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606879"
---
# <a name="setting-the-layout-used-by-a-report" /><a name="setting-the-layout-used-by-a-report"></a>Angive det layout, der bruges af en rapport

> **GÆLDER FOR:** Business Central Online, Business Central lokalt 2022 udgivelsesbølge 1 og nyere. Find tidligere versioner [her](ui-how-change-layout-currently-used-report.md).

Et rapportlayout bestemmer en rapports udseende. Det styrer, hvilke datafelter i et rapport-datasæt der vises, hvordan de er arrangeret, typografierede og mere. En rapport kan konfigureres med flere rapportlayout, som du kan skifte mellem efter behov.

Hvis der findes flere firmaer i programmet, angives layouterne for hvert enkelt regnskab. Så den samme rapport i én virksomhed kan have forskellige layout i et andet regnskab.

## <a name="get-started" /><a name="get-started"></a>Kom i gang

Der er et par måder at angive det layout, som en rapport bruges på. Der er fordele ved hver måde, afhængigt af hvad du leder efter: 

- Fra rapportanmodningssiden

  Når du konfigurerer en rapport til kørsel, indeholder rapportanmodningssiden **rapportlayout**, som viser det aktuelle standardlayout, som bruges af rapporten. Du kan bruge dette felt til midlertidigt at skifte til et andet tilgængeligt layout, som er den rapport, du kører. Når du har kørt rapporten, gendannes standardlayoutet igen. Du kan få flere oplysninger [Køre og udskrive en rapport](ui-work-report.md#switching-the-report-layout).

- Fra siden **Valg af rapportlayout**

  På siden til **valg af rapportlayout** vises en oversigt over alle rapporter. Denne side angiver, hvad rapportens standardlayout er. Den lader dig angive layout i forskellige firmaer, uden at du behøver at skifte det regnskab, du arbejder med.

- Fra siden **rapportlayout** vises **Rapportlayouts** for hver rapport i det aktuelle regnskab. Den bruges også til at angive standardlayoutet for rapporter. Det er nemt at finde et bestemt layout ved at sortere eller filtrere listen. Når du har fundet layoutet, kan du angive det for en rapport med en enkelt markering.

  > [!NOTE]
  > Du kan ikke bruge siden **Rapportlayout** til Word-og RDLC-layout, der er oprettet med den ældre **brugerdefinerede layout**-funktion. Du kan faktisk ikke se disse brugerdefinerede layout på siden **rapportlayout**. Du kan kun indstille disse layout ved hjælp af siden **Valg af rapportlayout**.

## <a name="set-the-layout-from-the-report-layouts-page" /><a name="set-the-layout-from-the-report-layouts-page"></a>Angiv layoutet fra siden Rapportlayout

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Find layoutet på listen, Marker det, og vælg derefter handlingen **Angiv standard** øverst på siden.

## <a name="set-the-layout-from-report-layout-selection-page" /><a name="set-the-layout-from-report-layout-selection-page"></a>Angiv layoutet fra siden Valg af rapportlayout

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Valg af rapportlayout**, og vælg derefter det relaterede link.
  
   Siden viser en liste over alle de rapporter, der er tilgængelige i det firma, der er angivet i feltet **Virksomhed** øverst på siden. Feltet **Layoutbeskrivelse** angiver det layout, der aktuelt bruges af rapporten.
2. Angiv feltet **Virksomhed** øverst på siden til det firma, der indeholder rapporten.
3. Find og vælg rapporten på listen, og benyt derefter en af følgende fremgangsmåder:

   - Hvis det layout, du vil skifte til, er en anden type end det aktuelle layout, skal du vælge feltet **Layouttype** og derefter vælge den type layout, du vil angive i rapporten. 
   - Hvis det layout, du vil skifte til samme type som det aktuelle layout, skal du vælge handlingen **Vælg layout** øverst.

4. Vælg layoutet på siden **Rapportlayout**, og vælg derefter **OK**.

## <a name="revert-to-the-original-default-layout" /><a name="revert-to-the-original-default-layout"></a>Vende tilbage til det oprindelige standardlayout

Rapporter er som standard udformet til at bruge et layout. Du kan skifte tilbage til det oprindelige standardlayout fra siden til **valg af rapportlayout**. Vælg rapporten, og vælg derefter **Gendan standardmarkeringshandlingen** øverst på siden.

## <a name="see-related-microsoft-trainingtrainingmoduleschange-documents-dynamics--business-centralindex" /><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also" /><a name="see-also"></a>Se også

[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
