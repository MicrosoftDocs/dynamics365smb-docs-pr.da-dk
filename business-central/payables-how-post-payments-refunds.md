---
title: "Udligne betalinger til relaterede dokumenter og bogføre dem | Microsoft Docs"
description: "Beskriver, hvordan du registrerer betalinger, du foretager til leverandører, og refusioner, du foretager til kunder."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 3cad699234d95a849bf48f04c8462afa968789f6
ms.contentlocale: da-dk
ms.lasthandoff: 05/15/2018

---
# <a name="record-payments-and-refunds"></a>Registrere betalinger og refusioner
I vinduet **Udbetalingskladde** registrerer du betalinger, du foretager til leverandører, og refusioner, du foretager til kunder. Når du bogfører en udbetalingskladdelinje, registreres det betalte beløb i det angivne banksystem. Du skal derefter sørge for at udføre den faktiske pengeoverførsel fra den relaterede bankkonto.

Hvis du udfylder feltet **Udligningsbilagsnr.** med den faktura eller kreditnota, der skal betales eller refunderes, indstillet det pågældende dokument til betalt, når du bogfører kladden. Det betegnes "udlignet". Som et alternativ til udligning under bogføring af betalingen, kan du bruge vinduerne **Udlign kred.poster** og **Udlign debitorposter**, når du har foretaget bogføringen af betalingen. Du kan finde flere oplysninger i f.eks. [Udligne kreditorbetalinger manuelt](payables-how-apply-purchase-transactions-manually.md).

Funktionen **Lav forslag** kan hjælpe dig med at udfylde betalingskladdelinjer automatisk i overensstemmelse med kreditorprioriteringen og forfaldsdatoer. Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md). Med denne funktion er feltet **Udligningsbilagsnr.** altid udfyldt.

Ud over at registrere, at betalingen er foretaget, kan du også bruge vinduet **Udbetalingskladde** til at sende betalingen til yderligere behandling i banken. Du kan finde flere oplysninger i [Foretage betalinger med check](payables-how-work-checks.md) og [Foretage elektroniske betalinger](payables-how-export-payments-bank-file.md).  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. Åbn det kladdenavn, der er dedikeret til betalinger.
3. Hvis du ved, hvem der skal betales eller refunderes, skal du udfylde felterne manuelt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Du kan også udligne betalingen til den relaterede faktura eller kreditnota, vælge feltet **Udligningsbilagsnr.** i vinduet **Udlign kred.poster**, vælge den relevante faktura eller kreditnota og derefter vælge knappen **OK**.

    Mange felter som f.eks. feltet **Beløb** og **Forfaldsdato** udfyldes nu med oplysninger fra det valgte dokument.
5. Du kan også bruge funktionen **Lav kreditorbetalingsforslag**. Alle udligningsoplysninger og -beløb angives derefter også på kladdelinjerne. Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).

    Meddelelser hjælper dig til at udfylde de obligatoriske felter korrekt.
6.  Når alle betalingskladdelinjer er fuldført, skal du vælge handlingen **Bogfør**.

## <a name="see-also"></a>Se også
[Foretage betalinger med check](payables-how-work-checks.md)  
[Foretage elektroniske betalinger](payables-how-export-payments-bank-file.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Eksportere en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

