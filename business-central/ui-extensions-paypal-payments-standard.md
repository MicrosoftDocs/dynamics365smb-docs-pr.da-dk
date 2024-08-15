---
title: Brug af PayPal Payments Standard-udvidelsen
description: 'Denne artikel beskriver, hvordan du bruger standardudvidelsen til at gøre det muligt for kunder at foretage betalinger med PayPal.'
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '1070, 1071, 1073, 1074'
ms.date: 07/09/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Udvidelsen PayPal Payments Standard

Standardudvidelsen PayPal Payments kan hjælpe dig med at øge dit kundeserviceniveau ved at gøre det nemmere for dine kunder at betale deres regninger.

Som et alternativ til at opkræve betalinger via bankoverførsel eller kredit Kort kan kunderne betale via deres PayPal konto. Når du sender en salgsfaktura med mail, er der et PayPal-link i brødteksten i mailen og i det vedhæftede PDF-dokument. Hvis kunden vælger sammenkæde, åbnes servicesiden for deres PayPal konto, hvor betalingsoplysningerne vises. Kunden kan derefter betale fakturaen som andre PayPal-betalinger.

Tjenesten PayPal Payments Standard giver følgende fordele:

* Debitorbetalinger kommer hurtigere ind på bankkontoen.
* Kunder har flere måder at betale fakturaer på.
* PayPal tilbyder en pålidelig betalingstjeneste, som debitorer foretrækker frem for at angive kreditkortoplysninger på websteder.
* PayPal tilbyder flere måder til håndtering af betalinger, herunder kreditkort, PayPal-konti og andre kilder.
* PayPal-linket kan tilføjes automatisk til salgsdokumenter eller manuelt af brugeren.
* Tjenesten PayPal Payments Standard er uden månedlige gebyrer eller opsætningsgebyrer.
* Da PayPal Payments Standard er en udvidelse, kan du nemt aktivere den, når og hvis din virksomhed kræver det.  

Du kan få mere at vide om, hvordan du konfigurerer udvidelsen, ved at gå til [Aktivér debitorbetaling via PayPal](sales-how-enable-payment-service-extensions.md).

## Registrer betalinger automatisk for virksomhedskonti

[!INCLUDE [prod_short](includes/prod_short.md)] kan registrere betalinger automatisk, hvis du har en Business Merchant-konto til PayPal Commerce Platform. Når dine kunder bruger PayPal sammenkæde til at betale en faktura, [!INCLUDE [prod_short](includes/prod_short.md)]  bogfører du posterne og lukker dokumentet.

Hvis du vil bruge denne funktion, **skal du aktivere** Til/fra-knappen Registrer betalinger automatisk [!INCLUDE [prod_short](includes/prod_short.md)] **på siden Opsætning** af betalingsregistrering og bekræfte de konti, du vil bruge til betalingerne. Hvis du beslutter, at du ikke vil registrere betalinger automatisk, kan du slå det fra igen.

> [!TIP]
> Udviklere kan bruge sandkassekonti til at teste opsætningen. For at gøre det skal du ændre PayPal-URL'en til **sandbox.paypal.com**. [!INCLUDE [prod_short](includes/prod_short.md)] bruger PayPals IPN (Instant Payment Notification) via notify_url.

## Se også

[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
