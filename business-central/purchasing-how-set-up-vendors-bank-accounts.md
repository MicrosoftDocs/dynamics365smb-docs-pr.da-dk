---
title: Konfigurere kreditorbankkonto
description: Få mere at vide om, hvordan du knytter bankkonti til kreditorkort i Business central, herunder kontaktoplysninger, SWIFT-og IBAN-koder.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 07/04/2022
ms.author: a-reishima
ms.openlocfilehash: 8c6faa8adadb62449d1067f877b40176bc15d034
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529626"
---
# <a name="set-up-vendor-bank-accounts"></a>Konfigurere kreditorbankkonti

På samme måde som du kan bruge bankkontooplysninger på [!INCLUDE [prod_short](includes/prod_short.md)] til at holde styr på virksomhedens banktransaktioner, kan du også angive bankoplysninger for kreditorer. Kreditorbankkonto data kan forenkle betalinger til leverandører, når de kombineres med [AMC Banking 365 Fundamentals-filtypenavn](ui-extensions-amc-banking.md) eller [Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)-funktion, f. eks.

## <a name="add-or-edit-a-vendor-bank-account"></a>Tilføje eller redigere en kreditorbankkonto

[!INCLUDE [purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

> [!TIP]
> Du kan angive flere kreditorbankkonti på siden **Kreditorbankkontoliste**.

## <a name="set-up-a-preferred-vendor-bank-account"></a>Konfigurere en foretrukken kreditorbankkonto

Hvis en kreditor har en eller flere bankkonti, og du vil angive en foretrukken indstilling for Udbetalingskladdelinjer, skal du benytte følgende fremgangsmåde:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link.
2. Åbn kortet for kreditoren.
3. Vælg standard kreditorbankkontoen i feltet **Foretrukken bankkontokode** i oversigtspanelet **Betaling**.

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Konfigurere bankkonti](bank-how-setup-bank-accounts.md)  
[Brug AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md)  
[Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
