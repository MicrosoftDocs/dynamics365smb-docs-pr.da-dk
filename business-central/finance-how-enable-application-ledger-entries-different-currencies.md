---
title: Udligne poster i forskellige valutaer
description: 'Du kan udligne finansposter i flere valutaer, f.eks. hvis du sælger i én valuta og modtager betaling i en anden.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'multiple currencies, payment, reconcile'
ms.search.form: '148, 460, 25'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="enable-application-of-ledger-entries-in-different-currencies" />Aktivere anvendelsen af finansposter i forskellige valutaer

Hvis du køber varer fra en leverandør i én valuta, men foretager betaling i en anden valuta, kan du udligne betalingen med købet.

Ligeledes, hvis du sælger til en debitor i en valuta og modtager betaling i en anden, kan du knytte betalingen til salgsfakturaen.

Følgende procedure beskriver, hvordan du kan angive dette for kreditorposter på siden **Købsopsætning**. Der er tilsvarende opsætning for debitorposter på siden **Salgsopsætning**.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies" />Sådan aktiveres udligning af kreditorposter i forskellige valutaer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Købsopsætning** og derefter vælge det relaterede link.
2. Vælg en af følgende indstillinger i feltet **Valutaudligning**.

| Indstilling | Beskrivelse |
| --- | --- |
| Ingen |Udligning mellem valutaer er ikke tilladt. |
| ØMU |Udligning mellem ØMU-valutaer er tilladt. |
| Alle |Udligning mellem alle valutaer er tilladt. |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences" />Sådan opsættes finanskonti til afrundingsdifferencer ved valutaudligning

Hvis du anvender poster i forskellige valutaer, skal du oprette finanskonti, hvor du kan bogføre afrundingsdifferencer.  

> [!NOTE]  
> Du skal oprette de pågældende finanskonti, før du kan udføre opgaven. Du kan finde flere oplysninger i [Om finans- og kontoplanen](finance-general-ledger.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Debitorbogføringsgrupper**, og vælg derefter det relaterede link.  
2. I felterne **Valutaudlign.afrnd.kto (deb.)** og **Valutaudlign.afrnd.kto (kre.)** skal du indtaste de relevante finanskonti bogføring af afrundingsdifferencer.  
3. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kreditorbogføringsgrupper**, og vælg derefter det relaterede link.  
4. I felterne **Valutaudlign.afrnd.kto (deb.)** og **Valutaudlign.afrnd.kto (kre.)** skal du indtaste de relevante finanskonti bogføring af afrundingsdifferencer.  

## <a name="see-related-microsoft-trainingtrainingmodulesprocess-foreign-currency-payments-dynamics-365-business-central" />Se relateret [Microsoft-træning](/training/modules/process-foreign-currency-payments-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Administrere skyldige beløb](payables-manage-payables.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
