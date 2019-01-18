---
title: "Opsætning af foreslåede feltværdier | Microsoft Docs"
description: "For at undgå manuelle beregninger og udføre opgaver kan hurtigt og præcist kan du konfigurere automatisk dataindtastning, så Business Central udfylder af udvalgte felter."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 74a88d3e81413b4ecf849f500b5b670feea948bf
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="letting-included365finincludesd365finmdmd-suggest-values"></a>Lade [!INCLUDE[d365fin](includes/d365fin_md.md)] foreslå værdier
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan hjælpe dig med at udføre opgaver hurtigere og mere korrekt ved at forhåndsudfylde felter eller hele linjer med data, som du normalt selv skal beregne og angive. Selvom sådan automatisk dataindtastning altid er korrekte, kan du ændre oplysningerne bagefter, hvis du vil.

Funktioner, der indsætter feltværdier, tilbydes typisk i opgaver, hvor du skal angive store mængder transaktionsdata og vil undgå fejl og spare tid. Dette emne indeholder et udvalg af disse funktioner. Der bliver tilføjet flere afsnit i fremtidige opdateringer af [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="the-suggest-balancing-amount-check-box-on-the-general-journal-batches-page"></a>Afkrydsningsfeltet **Foreslå modkontobeløb** på siden **Finanskladdenavne**
Når f.eks. du angiver finanskladdelinjer for flere udgifter, der skal alle bogføres til samme bankkonto, kan du derefter, hver gang du indtaster en ny kladdelinje for en udgift, få feltet **Beløb** på bankkontolinjen opdateret automatisk med det beløb, der modsvarer udgifterne. Du kan finde flere oplysninger om at arbejde med finanskladder i [Arbejde med finanskladder](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Sådan udfyldes feltet **Beløb** til afstemning af finanskladdelinjer automatisk
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladder**, og vælg derefter det relaterede link.
2. På linjen for dit foretrukne finanskladdenavn skal du markere afkrydsningsfeltet **Foreslå modkontobeløb**.
3. Åbn finanskladden, og fortsæt for at registrere og bogføre transaktioner med den beskrevne funktionen til automatisk indtastning af en feltværdi.       

Du kan finde oplysninger om opsætning af et personligt finanskladdenavn, f.eks. til håndtering af udgifter, i [Arbejde med finanskladder](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-on-the-payment-registration-page"></a>Feltet **Udfyld Dato for modtaget automatisk** på siden **Betalingsregistrering**
Siden **Betalingsregistrering** viser udestående indgående betalinger som linjer, der repræsenterer bogførte salgsdokumenter, hvor et beløb er forfaldent til betaling. Du kan finde flere oplysninger om udligning af debitorbetalinger i [Afstemme debitor betalinger manuelt på en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

På siden skal du først og fremmest udfylde afkrydsningsfeltet **Betaling foretaget** og feltet **Dato for modtaget**. Du kan indstille [!INCLUDE[d365fin](includes/d365fin_md.md)] til automatisk at angive arbejdsdato i feltet **Dato for modtaget**, når du markerer feltet **Betaling foretaget**.

### <a name="to-have-the-date-received-field-on-the-payment-registration-page-filled-automatically"></a>Sådan udfyldes feltet **Dato for modtaget** automatisk på siden **Betalingsregistrering**
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af betalingsregistrering**, og vælg derefter det relaterede link.
2. Marker afkrydsningsfeltet **Udfyld Dato for modtaget automatisk**.
3. Åbn siden **Betalingsregistrering**, og fortsæt for at behandle indgående betalinger fra kunder ved hjælp af den beskrevne funktionen for automatisk angivelse af en feltværdi.

## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Finans](finance.md)

