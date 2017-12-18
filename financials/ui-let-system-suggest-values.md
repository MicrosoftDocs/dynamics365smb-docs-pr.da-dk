---
title: "Opsætning af foreslåede feltværdier | Microsoft Docs"
description: "For at undgå manuelle beregninger og udføre opgaver kan hurtigt og præcist kan du konfigurere automatisk dataindtastning, så Dynamics 365 udfylder udvalgte felter."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 26a66f87f85cac1ff6f6ba6eb4cb90527565f236
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="letting-included365finlongincludesd365finlongmdmd-suggest-values"></a>Lade [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] foreslå værdier
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan hjælpe dig med at udføre opgaver hurtigere og mere korrekt ved at forhåndsudfylde felter eller hele linjer med data, som du normalt selv skal beregne og angive. Selvom sådan automatisk dataindtastning altid er korrekte, kan du ændre oplysningerne bagefter, hvis du vil.

Funktioner, der indsætter feltværdier, tilbydes typisk i opgaver, hvor du skal angive store mængder transaktionsdata og vil undgå fejl og spare tid. Dette emne indeholder et udvalg af disse funktioner. Der bliver tilføjet flere afsnit i fremtidige opdateringer af [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="the-suggest-balancing-amount-check-box-in-the-general-journal-batches-window"></a>Afkrydsningsfeltet **Foreslå modkontobeløb** i vinduet **Finanskladdenavne**
Når f.eks. du angiver finanskladdelinjer for flere udgifter, der skal alle bogføres til samme bankkonto, kan du derefter, hver gang du indtaster en ny kladdelinje for en udgift, få feltet **Beløb** på bankkontolinjen opdateret automatisk med det beløb, der modsvarer udgifterne. Du kan finde flere oplysninger om at arbejde med finanskladder i [Arbejde med finanskladder](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Sådan udfyldes feltet **Beløb** til afstemning af finanskladdelinjer automatisk
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladder**, og vælg derefter det relaterede link.
2. På linjen for dit foretrukne finanskladdenavn skal du markere afkrydsningsfeltet **Foreslå modkontobeløb**.
3. Åbn finanskladden, og fortsæt for at registrere og bogføre transaktioner med den beskrevne funktionen til automatisk indtastning af en feltværdi.       

Du kan finde oplysninger om opsætning af et personligt finanskladdenavn, f.eks. til håndtering af udgifter, i [Arbejde med finanskladder](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-in-the-payment-registration-window"></a>Feltet **Udfyld Dato for modtaget automatisk** i vinduet **Betalingsregistrering**
Vinduet **Betalingsregistrering** viser udestående indgående betalinger som linjer, der repræsenterer bogførte salgsdokumenter, hvor et beløb er forfaldent til betaling. Du kan finde flere oplysninger om udligning af debitorbetalinger i [Fremgangsmåde: afstemme debitor betalinger manuelt på en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

De vigtigste handlinger i vinduet består i at udfylde afkrydsningsfeltet **Betaling foretaget** og feltet **Dato for modtaget**. Du kan indstille [!INCLUDE[d365fin](includes/d365fin_md.md)] til automatisk at angive arbejdsdato i feltet **Dato for modtaget**, når du markerer feltet **Betaling foretaget**.

### <a name="to-have-the-date-received-field-in-the-payment-registration-window-filled-automatically"></a>Sådan udfyldes feltet **Dato for modtaget** automatisk i vinduet **Betalingsregistrering**
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af betalingsregistrering**, vælg og derefter det relaterede link.
2. Marker afkrydsningsfeltet **Udfyld Dato for modtaget automatisk**.
3. Åbn vinduet **Betalingsregistrering**, og fortsæt for at behandle indgående betalinger fra kunder ved hjælp af den beskrevne funktionen for automatisk angivelse af en feltværdi.

## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Finans](finance.md)

