---
title: Betalingsudligning med Envestnet Yodlee Bank Feeds-udvidelsen
description: 'Beskriver udvidelsen Envestnet Yodlee Bank Feeds, der sammenkæder med bankkonti, så du hurtigt kan afstemme betalinger.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'app, add-in, manifest, customize, stream, bank account link'
ms.search.form: '1450, 1451, 1452, 1453, 1454, 1458, 1460,'
ms.date: 04/01/2021
ms.author: edupont
---
# Udvidelsen Envestnet Yodlee Bank Feeds

Med tjenesten Envestnet Yodlee Bank Feeds kan du knytte systembankkontoen til din onlinebankkonto for hurtigt at afstemme indbetalinger til bankkonti. Det betyder, at det seneste bankkontoudtog automatisk eller manuelt indlæses i udligningskladden, hvilket sikrer, at du altid behandler de seneste betalinger med minimal risiko for fejl.

Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i USA og Canada.

> [!NOTE]
> Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i onlineversionen af Business Central. Hvis du vil bruge denne funktionalitet lokalt, skal du have en cobrand-konto hos Envestnet Yodlee.<br /><br />
> Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i USA og Canada.
> Kun banker, der er hjemmehørende i disse lande/områder, understøttes, selvom bankerne fra andre lande/områder kan blive vist i Envestnet Yodlee Bank Feeds-vinduet til bankvalg i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]
> På grund af det nye betalingstjenestedirektiv i Europa (PSD2) kan du efter den 14. september 2019 ikke længere automatisk importere bankkontoudtog fra banker i Storbritannien til [!INCLUDE[prod_short](includes/prod_short.md)]. Vi overvejer evt. at tilbyde denne funktion igen i fremtiden.

Envestnet Yodlee Bank Feeds-tjenesten giver følgende fordele:

* Fjerner behovet for manuel indtastning.
* Forbedrer effektivitet og nøjagtighed, når du udfører en udligning af en betaling.
* Understøtter et stort antal banker.
* Tillader opdaterede oplysninger om banktransaktioner fra [!INCLUDE[prod_short](includes/prod_short.md)].
* Understøtter manuelle samt automatiske bankfeeds.
* Gør det muligt at outsource betalingsudligning til en bogholder ved at give adgang til bankkontoudtog.

## Tilgængelige bankfeeds

Du kan kontrollere, om en bank understøttes ved at konfigurere og oprette forbindelse til tjenesten Envestnet Yodlee Bank Feeds. Banken vises på listen, hvis den understøttes af Envestnet Yodlee.

Du kan finde flere oplysninger i [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

## Se også

[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
