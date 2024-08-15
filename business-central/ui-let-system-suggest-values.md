---
title: Lad Business Central foreslå værdier
description: 'For at undgå manuelle beregninger og udføre opgaver kan hurtigt og præcist kan du konfigurere automatisk dataindtastning, så Business Central udfylder af udvalgte felter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '39, 251, 981'
ms.date: 07/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="let--suggest-values"></a>Lad [!INCLUDE[prod_short](includes/prod_short.md)] foreslå værdier
[!INCLUDE[prod_short](includes/prod_short.md)] kan hjælpe dig med at udføre opgaver hurtigere og mere korrekt ved at forhåndsudfylde felter eller hele linjer med data, som du normalt selv skal beregne og angive. Selvom sådan automatisk dataindtastning altid er korrekte, kan du ændre oplysningerne bagefter, hvis du vil.

Funktioner, der indsætter feltværdier, tilbydes typisk i opgaver, hvor du skal angive store mængder transaktionsdata og vil undgå fejl og spare tid. Denne artikel indeholder et udvalg af sådanne funktioner. Der bliver tilføjet flere afsnit i fremtidige opdateringer af [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="the-suggest-balancing-amount-check-box-on-the-general-journal-batches-page"></a>Afkrydsningsfeltet **Foreslå modkontobeløb** på siden **Finanskladdenavne**
Hvis du f.eks. angiver finanskladdelinjer for flere udgifter, som alle skal bogføres på samme bankkonto, kan du automatisk få **feltet Beløb** på bankkontolinjen opdateret, så det beløb, der afstemmer udgifterne, hver gang du angiver en ny kladdelinje for en udgift. Du kan finde flere oplysninger om at arbejde med finanskladder i [Arbejde med finanskladder](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Sådan udfyldes feltet **Beløb** til afstemning af finanskladdelinjer automatisk
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Finanskladder**, og vælg derefter det relaterede link.
2. På linjen for dit foretrukne finanskladdenavn skal du markere afkrydsningsfeltet **Foreslå modkontobeløb**.
3. Åbn finanskladden, og fortsæt for at registrere og bogføre transaktioner med den beskrevne funktionen til automatisk indtastning af en feltværdi.       

Du kan finde oplysninger om opsætning af et personligt finanskladdenavn, f.eks. til håndtering af udgifter, i [Arbejde med finanskladder](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-on-the-payment-registration-page"></a>Feltet **Udfyld Dato for modtaget automatisk** på siden **Betalingsregistrering**
Siden **Registrer debitorbetalinger** viser udestående indgående betalinger som linjer, der repræsenterer salgsdokumenter, hvor et beløb er forfaldent til betaling. Du kan finde flere oplysninger om udligning af debitorbetalinger i [Afstemme debitor betalinger på en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

Dine vigtigste handlinger på siden er at udfylde afkrydsningsfeltet **Betaling foretaget** og feltet **Bilag modtaget** den. Du kan indstille [!INCLUDE[prod_short](includes/prod_short.md)] til automatisk at angive arbejdsdato i feltet **Dato for modtaget**, når du markerer feltet **Betaling foretaget**.

### <a name="to-have-the-date-received-field-on-the-payment-registration-page-filled-automatically"></a>Sådan udfyldes feltet **Dato for modtaget** automatisk på siden **Betalingsregistrering**
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af betalingsregistrering**, og vælg derefter det relaterede link.
2. Marker afkrydsningsfeltet **Udfyld Dato for modtaget automatisk**.
3. Åbn siden Registrer debitorbetalinger **,** og fortsæt med at behandle indgående debitorbetalinger ved hjælp af den beskrevne funktion til automatisk indtastning af en feltværdi.

## <a name="see-also"></a>Se også
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Finans](finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
