---
title: Registrere indbetalinger og refusioner i udbetalingskladden
description: 'Læs om, hvordan du kan registrere på siden Udbetalingskladde de betalinger, du foretager til debitorer, på udbetalingskladdesiden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP'
ms.search.form: '256, 233, 624, 1228'
ms.date: 07/17/2024
ms.service: dynamics-365-business-central
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Registrere indbetalinger og refusioner i udbetalingskladden

 **På siden Udbetalingskladder** registrerer du betalinger, som du foretager til kreditorer, og refusioner, som du foretager til debitorer. Når du bogfører en udbetalingskladdelinje, registreres det betalte beløb i den angivne bankkonto. Du skal derefter sørge for at udføre den faktiske pengeoverførsel fra den relaterede bankkonto.  

Betalingskladder er en kassekladde, der er optimeret til betalinger. Du kan hurtigt tilføje linjerne manuelt, du kan lade [!INCLUDE[prod_short](includes/prod_short.md)] foreslå kreditorbetalinger, og du kan udligne betalingen på bogførte dokumenter. Selvom du foretager betalinger, skal du angive et positivt beløb i feltet **Dokumentbeløb**. Afhængigt af dokumenttypen for kladdelinjen konverteres beløbet derefter til et negativt beløb i de underliggende transaktioner. På denne måde kan du hurtigere tilføje linjerne manuelt. Hvis du vil angive negative beløb, kan du tilpasse udbetalingskladden for at få vist feltet **Beløb** i stedet. Hvis du vil vide mere om at tilpasse sider, skal du gå til [Start tilpasning ved hjælp af tilpasningstilstand](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).  

- Udligne betalinger til fakturaer eller kreditnotaer

    Hvis du udfylder feltet **Udligningsbilagsnr.** med den faktura eller kreditnota, der skal betales eller refunderes, indstillet det pågældende dokument til **Betalt**, når du bogfører kladden. Indstillingen betegnes som "udlignet." Som et alternativ til udligning, når du bogfører en betaling, kan du bruge siderne **Udlign kred.poster** og **Udlign debitorposter**, når du har foretaget bogføringen af betalingen. Du kan få mere at vide i f.eks. [Afstemme kreditorbetalinger med udbetalingskladden eller fra kreditorposter](payables-how-apply-purchase-transactions-manually.md).  

- Få foreslåede betalinger til leverandører eller medarbejdere

    Handlingerne **Lav forslag** og **Foreslå medarbejderbetalinger** kan hjælpe dig med at udfylde betalingskladdelinjer automatisk i overensstemmelse med kreditorprioriteringen og forfaldsdatoer. Du kan få mere at vide ved at gå til [Lav kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md). Med denne funktion er feltet **Udligningsbilagsnr.** altid udfyldt.  

- Udskrive checks og sende betalinger elektronisk til din bank

    Ud over at registrere, at betalingen er foretaget, kan du også bruge siden **Udbetalingskladde** til at sende betalingen til yderligere behandling i banken. Du kan få mere at vide i [Foretage betalinger med check](payables-how-work-checks.md) og [Foretage elektroniske betalinger](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal"></a>Foretage betalinger i udbetalingskladden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. Åbn det kladdenavn, du bruger til betalinger.
3. Hvis du ved, hvem der skal betales, skal du udfylde felterne manuelt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Hvis du også vil udligne betalingen med den relaterede faktura eller kreditnota, skal du vælge feltet **Udligningsbilagsnr.**  **på siden Udlign kreditorposter**, skal du vælge den relevante faktura eller kreditnota og derefter vælge knappen **OK** .

    Mange felter som f.eks. feltet **Dokumentbeløb** og **Forfaldsdato** udfyldes nu med oplysninger fra det valgte dokument.
5. Du kan også bruge handlingen **Lav kreditorbetalingsforslag**. Alle udligningsoplysninger og -beløb angives derefter også på kladdelinjerne. Du kan få mere at vide ved at gå til [Lav kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).
6. Når du har fuldført alle betalingskladdelinjer, skal du vælge handlingen **Bogfør**.

## <a name="to-issue-a-refund-check"></a>Sådan udstedes en refusionscheck

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. I feltet **Dokumenttype** skal du vælge **Refusion**.  
3. I feltet **Eksternt bilagsnr.** bruges denne som reference til refusionschecken (f.eks. returordrenummer).  
4. I feltet **Kontotype** skal du vælge **Debitor**.  
5. Vælg det debitorkontonummer, som refusions kontrollen udstedes til, i feltet **Kontonr.**.  
6. Angiv det beløb, der skal tilbagebetales, i feltet **Beløb**.  
7. I feltet **Modkontotype** skal du vælge **Bankkonto**.  
8. I Modkonto **skal** du vælge den bankkonto, checken kommer fra.  
9. I feltet **Udligningsbilagsnr.** til at vælge de dokumenter, der kræver refusion.  
10. Når du afslutter alle linjer i betalingskladden, skal du vælge handlingen **Bogfør/Udskriv**, derefter vælge handlingen **Bogfør og Udskriv** og derefter vælge **Ja**.  
  
## <a name="see-also"></a>Se også

[Foretage checkbetalinger](payables-how-work-checks.md)  
[Foretage elektroniske betalinger](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Eksportere en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
