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
ms.date: 03/07/2022
ms.author: jswymer
ms.openlocfilehash: e59a57e6cac21f4909088defc42da795e5550562
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9535849"
---
# <a name="setting-the-layout-used-by-a-report"></a>Angive det layout, der bruges af en rapport

> **GÆLDER FOR:** Business Central Online, Business Central lokalt 2022 udgivelsesbølge 1 og nyere. Find tidligere versioner [her](ui-how-change-layout-currently-used-report.md).

Et rapportlayout bestemmer en rapports udseende. Det styrer, hvilke datafelter i et rapport-datasæt der vises, hvordan de er arrangeret, typografierede og mere. En rapport kan konfigureres med flere rapportlayout, som du kan skifte mellem efter behov.

Hvis der findes flere firmaer i programmet, angives layouterne for hvert enkelt regnskab. Så den samme rapport i én virksomhed kan have forskellige layout i et andet regnskab.

## <a name="get-started"></a>Kom i gang

Der er to måder at angive det layout, som en rapport bruges på. En metode er fra siden **Valg af rapportlayout**. Den anden metode er på siden **Rapportlayout**. Hver side har fordele, f. eks.: 

- På siden til **valg af rapportlayout** vises en oversigt over alle rapporter.

  Denne side angiver, hvad rapportens aktuelle layout er. Derudover kan du angive layout i forskellige firmaer, uden at du behøver at skifte det regnskab, du arbejder med.

- På siden **rapportlayout** vises alle tilgængelige layout for hver rapport i det aktuelle regnskab.

  Det er nemt at finde et bestemt layout ved at sortere eller filtrere listen. Når du har fundet layoutet, kan du angive det for en rapport med en enkelt markering.

  > [!NOTE]
  > Du kan ikke bruge siden **Rapportlayout** til Word-og RDLC-layout, der er oprettet med den ældre **brugerdefinerede layout**-funktion. Du kan faktisk ikke se disse brugerdefinerede layout på siden **rapportlayout**. Du kan kun indstille disse layout ved hjælp af siden **Valg af rapportlayout**.

## <a name="set-the-layout-from-the-report-layouts-page"></a>Angiv layoutet fra siden Rapportlayout

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Find layoutet på listen, Marker det, og vælg derefter handlingen **Angiv standard** øverst på siden.

## <a name="set-the-layout-from-report-layout-selection-page"></a>Angiv layoutet fra siden Valg af rapportlayout

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Valg af rapportlayout**, og vælg derefter det relaterede link.
  
   Siden viser en liste over alle de rapporter, der er tilgængelige i det firma, der er angivet i feltet **Virksomhed** øverst på siden. Feltet **Layoutbeskrivelse** angiver det layout, der aktuelt bruges af rapporten.
2. Angiv feltet **Virksomhed** øverst på siden til det firma, der indeholder rapporten.
3. Find og vælg rapporten på listen, og benyt derefter en af følgende fremgangsmåder:

   - Hvis det layout, du vil skifte til, er en anden type end det aktuelle layout, skal du vælge feltet **Layouttype** og derefter vælge den type layout, du vil angive i rapporten. 
   - Hvis det layout, du vil skifte til samme type som det aktuelle layout, skal du vælge handlingen **Vælg layout** øverst.

4. Vælg layoutet på siden **Rapportlayout**, og vælg derefter **OK**.

## <a name="revert-to-the-original-default-layout"></a>Vende tilbage til det oprindelige standardlayout

Rapporter er som standard udformet til at bruge et layout. Du kan skifte tilbage til det oprindelige standardlayout fra siden til **valg af rapportlayout**. Vælg rapporten, og vælg derefter **Gendan standardmarkeringshandlingen** øverst på siden.

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
