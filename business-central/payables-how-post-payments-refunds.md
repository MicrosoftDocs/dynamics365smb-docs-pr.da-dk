---
title: Udligne betalinger til relaterede dokumenter og bogføre dem | Microsoft Docs
description: Beskriver, hvordan du registrerer betalinger, du foretager til leverandører, og refusioner, du foretager til kunder.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b45b4c109d33773ead4e920d5692a615faa7a366
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759588"
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Registrere indbetalinger og refusioner i udbetalingskladden

På siden **Udbetalingskladde** registrerer du betalinger, du foretager til leverandører, og refusioner, du foretager til kunder. Når du bogfører en udbetalingskladdelinje, registreres det betalte beløb i det angivne banksystem. Du skal derefter sørge for at udføre den faktiske pengeoverførsel fra den relaterede bankkonto.  

Betalingskladden er en kassekladde, der er optimeret til betalinger. Du kan hurtigt tilføje linjerne manuelt, du kan lade [!INCLUDE[prod_short](includes/prod_short.md)] foreslå kreditorbetalinger, og du kan udligne betalingen på bogførte dokumenter. Selvom du foretager betalinger, skal du angive et positivt beløb i feltet **Dokumentbeløb**. Afhængigt af dokumenttypen for kladdelinjen konverteres beløbet derefter til et negativt beløb i de underliggende transaktioner. På denne måde kan du hurtigere tilføje linjerne manuelt. Hvis du vil angive negative beløb, kan du tilpasse udbetalingskladden for at få vist feltet **Beløb** i stedet.  

- Udligne betalinger til fakturaer eller kreditnotaer

    Hvis du udfylder feltet **Udligningsbilagsnr.** med den faktura eller kreditnota, der skal betales eller refunderes, indstillet det pågældende dokument til betalt, når du bogfører kladden. Det betegnes "udlignet". Som et alternativ til udligning under bogføring af betalingen, kan du bruge siderne **Udlign kred.poster** og **Udlign debitorposter**, når du har foretaget bogføringen af betalingen. Du kan finde flere oplysninger i f.eks. [Afstemme kreditorbetalinger med udbetalingskladden eller fra kreditorposter](payables-how-apply-purchase-transactions-manually.md).  

- Få foreslåede betalinger til leverandører eller medarbejdere

    Funktionerne **Lav forslag** og **Foreslå medarbejderbetalinger** kan hjælpe dig med at udfylde betalingskladdelinjer automatisk i overensstemmelse med kreditorprioriteringen og forfaldsdatoer. Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md). Med denne funktion er feltet **Udligningsbilagsnr.** altid udfyldt.  

- Udskrive checks og sende betalinger elektronisk til din bank

    Ud over at registrere, at betalingen er foretaget, kan du også bruge siden **Udbetalingskladde** til at sende betalingen til yderligere behandling i banken. Du kan finde flere oplysninger i [Foretage betalinger med check](payables-how-work-checks.md) og [Foretage elektroniske betalinger](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal"></a>Foretage betalinger i udbetalingskladden

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. Åbn det kladdenavn, der er dedikeret til betalinger.
3. Hvis du ved, hvem der skal betales eller refunderes, skal du udfylde felterne manuelt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Du kan også udligne betalingen til den relaterede faktura eller kreditnota, vælge feltet **Udligningsbilagsnr.** på siden **Udlign kred.poster**, vælge den relevante faktura eller kreditnota og derefter vælge knappen **OK**.

    Mange felter som f.eks. feltet **Dokumentbeløb** og **Forfaldsdato** udfyldes nu med oplysninger fra det valgte dokument.
5. Du kan også bruge funktionen **Lav kreditorbetalingsforslag**. Alle udligningsoplysninger og -beløb angives derefter også på kladdelinjerne. Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).

    Meddelelser hjælper dig til at udfylde de obligatoriske felter korrekt.
6.  Når alle betalingskladdelinjer er fuldført, skal du vælge handlingen **Bogfør**.

## <a name="see-also"></a>Se også
[Foretage betalinger med check](payables-how-work-checks.md)  
[Foretage elektroniske betalinger](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Eksportere en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]