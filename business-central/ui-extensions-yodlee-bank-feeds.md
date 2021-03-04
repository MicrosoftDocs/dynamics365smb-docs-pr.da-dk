---
title: Betalingsudligning med Envestnet Yodlee Bank Feeds-udvidelsen
description: Beskriver udvidelsen Envestnet Yodlee Bank Feeds, der sammenkæder med bankkonti, så du hurtigt kan afstemme betalinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d8a04218e44c4a40d96f5e84677434c51f6ef5f3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757388"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a>Udvidelsen Envestnet Yodlee Bank Feeds

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

## <a name="available-bank-feeds"></a>Tilgængelige bankfeeds
Du kan kontrollere, om en bank understøttes ved at konfigurere og oprette forbindelse til tjenesten Envestnet Yodlee Bank Feeds. Banken vises på listen, hvis den understøttes af Envestnet Yodlee.

Du kan finde flere oplysninger i [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)    
[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]