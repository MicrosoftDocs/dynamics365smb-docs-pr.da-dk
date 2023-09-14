---
title: Registrere indbetalinger og refusioner i udbetalingskladden
description: 'Læs om, hvordan du kan registrere på siden Udbetalingskladde de betalinger, du foretager til debitorer, på udbetalingskladdesiden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP'
ms.search.form: '256, 233, 624, 1228'
ms.date: 07/09/2021
ms.author: bholtorf
---
# Registrere indbetalinger og refusioner i udbetalingskladden

På siden **Udbetalingskladde** registrerer du betalinger, du foretager til leverandører, og refusioner, du foretager til kunder. Når du bogfører en udbetalingskladdelinje, registreres det betalte beløb i det angivne banksystem. Du skal derefter sørge for at udføre den faktiske pengeoverførsel fra den relaterede bankkonto.  

Betalingskladden er en kassekladde, der er optimeret til betalinger. Du kan hurtigt tilføje linjerne manuelt, du kan lade [!INCLUDE[prod_short](includes/prod_short.md)] foreslå kreditorbetalinger, og du kan udligne betalingen på bogførte dokumenter. Selvom du foretager betalinger, skal du angive et positivt beløb i feltet **Dokumentbeløb**. Afhængigt af dokumenttypen for kladdelinjen konverteres beløbet derefter til et negativt beløb i de underliggende transaktioner. På denne måde kan du hurtigere tilføje linjerne manuelt. Hvis du vil angive negative beløb, kan du tilpasse udbetalingskladden for at få vist feltet **Beløb** i stedet.  

- Udligne betalinger til fakturaer eller kreditnotaer

    Hvis du udfylder feltet **Udligningsbilagsnr.** med den faktura eller kreditnota, der skal betales eller refunderes, indstillet det pågældende dokument til betalt, når du bogfører kladden. Det betegnes "udlignet". Som et alternativ til udligning under bogføring af betalingen, kan du bruge siderne **Udlign kred.poster** og **Udlign debitorposter**, når du har foretaget bogføringen af betalingen. Du kan finde flere oplysninger i f.eks. [Afstemme kreditorbetalinger med udbetalingskladden eller fra kreditorposter](payables-how-apply-purchase-transactions-manually.md).  

- Få foreslåede betalinger til leverandører eller medarbejdere

    Funktionerne **Lav forslag** og **Foreslå medarbejderbetalinger** kan hjælpe dig med at udfylde betalingskladdelinjer automatisk i overensstemmelse med kreditorprioriteringen og forfaldsdatoer. Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md). Med denne funktion er feltet **Udligningsbilagsnr.** altid udfyldt.  

- Udskrive checks og sende betalinger elektronisk til din bank

    Ud over at registrere, at betalingen er foretaget, kan du også bruge siden **Udbetalingskladde** til at sende betalingen til yderligere behandling i banken. Du kan finde flere oplysninger i [Foretage betalinger med check](payables-how-work-checks.md) og [Foretage elektroniske betalinger](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## Foretage betalinger i udbetalingskladden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. Åbn det kladdenavn, der er dedikeret til betalinger.
3. Hvis du ved, hvem der skal betales, skal du udfylde felterne manuelt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Du kan også udligne betalingen til den relaterede faktura eller kreditnota, vælge feltet **Udligningsbilagsnr.** på siden **Udlign kred.poster**, vælge den relevante faktura eller kreditnota og derefter vælge knappen **OK**.

    Mange felter som f.eks. feltet **Dokumentbeløb** og **Forfaldsdato** udfyldes nu med oplysninger fra det valgte dokument.
5. Du kan også bruge funktionen **Lav kreditorbetalingsforslag**. Alle udligningsoplysninger og -beløb angives derefter også på kladdelinjerne. Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).

    Meddelelser hjælper dig til at udfylde de obligatoriske felter korrekt.
6. Når alle betalingskladdelinjer er fuldført, skal du vælge handlingen **Bogfør**.


## Sådan udstedes en refusionscheck

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. I feltet **Dokumenttype** skal du vælge **Refusion**.  
3. I feltet **Eksternt bilagsnr.** bruges denne som reference til refusionschecken (f.eks. returordre nummer).  
4. I feltet **Kontotype** skal du vælge **Debitor**.  
5. Vælg det debitorkontonummer, som refusions kontrollen udstedes til, i feltet **Kontonr.**.  
6. Angiv det beløb, der skal tilbagebetales, i feltet **Beløb**.  
7. I feltet **Modkontotype** skal du vælge **Bankkonto**.  
8. Vælg den bankkonto, som checken skal komme fra, i feltet **Modkonto**.  
9. I feltet **Udligningsbilagsnr.** til at vælge de dokumenter, der kræver refusion.  
10. Når alle linjer i betalingskladden er færdige, skal du vælge handlingen **Bogfør/Udskriv**, derefter vælge handlingen **Bogfør og Udskriv** og derefter vælge **Ja**.  
  

## Se også
[Foretage betalinger med check](payables-how-work-checks.md)  
[Foretage elektroniske betalinger](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Eksportere en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
