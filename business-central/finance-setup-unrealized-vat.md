---
title: Konfigurere ikke-realiseret moms
description: 'Hvis du bruger bogføring, der er baseret på kontanter, kan du angive, hvordan urealiseret moms for salg og køb skal håndteres.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'cash, VAT, unrealized, cash-based'
ms.search.form: '118, 472, 473'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a>Konfigurere urealiseret moms i forbindelse med bogføring baseret på kontanter

Hvis du bruger bogføringsmetoder, der er baseret på kontanter, kan du konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til at håndtere urealiseret moms.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Sådan bruges finanskonti for urealiseret moms

Du kan vælge, at momsbeløb beregnes og bogføres til en midlertidig finanskonto, når en faktura bogføres. Når den faktiske betaling af fakturaen bogføres, kan momsbeløbet så bogføres til den korrekte finanskonto og medtages i momsangivelsen. Du skal først [færdiggøre momsbogføringsopsætning](finance-setup-vat.md).

Når du vil bruge konti for urealiseret moms, skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, og skriv **Opsætning af Finans**.
2. I oversigtspanelet **Opsætning af Finans** skal du markere afkrydsningsfeltet **Urealiseret moms**.
3. Vælg ikonet **Søg efter side eller rapport** ![Elpære, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), og angiv **Opsætning af momsbogføring**.
4. På siden **Opsætning af momsbogføring** skal du vælge momsbogføringsgruppen og derefter vælge handlingen **Rediger**.
5. I feltet **Urealiseret moms - type** skal du vælge en indstilling for at angive, hvordan betalinger skal tildeles til fakturabeløbet (uden moms) og selve momsbeløbet, og hvordan momsbeløb skal overføres fra den urealiserede momskonto til den realiserede momskonto. Følgende tabel beskriver indstillingerne.

| Indstilling | Beskrivelse |
| --- | --- |
| Tom | Vælg denne indstilling, hvis du ikke vil bruge funktionen for urealiseret moms. |
| Procent | Betalinger dækker både moms og fakturabeløbet i forhold til den procentmæssige andel af det samlede fakturabeløb. Det betalte momsbeløb overføres fra den urealiserede momskonto til den realiserede momskonto. |
| Første | Betalingerne dækker først moms og derefter fakturabeløb. I dette tilfælde svarer beløbet, der overføres fra kontoen for urealiseret moms til momskontoen, til betalingsbeløbet, indtil hele momsbeløbet er betalt. |
| Sidste | Betalingerne dækker fakturabeløbet først moms og derefter moms. I dette tilfælde overføres intet beløb fra kontoen for urealiseret moms til momskontoen, før hele fakturabeløbet eksklusive moms er betalt. |
| Først (betalt) | Betalingerne skal først dække momsbeløbet (som ved indstillingen _Først_), men der overføres ikke noget beløb til momskontoen, før det fulde momsbeløb er betalt. |
| Sidst (betalt) | Betalingerne skal først dække fakturabeløbet (som ved indstillingen _Sidst_), men der overføres ikke noget beløb til momskontoen, før det fulde momsbeløb er betalt. |

6. I feltet **Urealiseret salgsmomskonto** skal du vælge finanskontoen for urealiseret salgsmoms.

    > [!NOTE]  
    > Momsbeløbet bogføres på denne konto og bliver stående der, indtil debitors indbetaling er bogført. Derefter overføres beløbet til finanskontoen for salgsmoms.
7. Angiv finanskontoen for urealiseret købsmoms i feltet **Urealiseret købsmomskonto**.

> [!NOTE]  
> Momsbeløbet bogføres på denne konto og bliver stående der, indtil debitors indbetaling er bogført. Derefter overføres beløbet til finanskontoen for købsmoms.

## <a name="see-also"></a>Se også
[Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
