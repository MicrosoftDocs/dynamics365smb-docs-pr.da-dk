---
title: Betalingsudligning med Envestnet Yodlee Bank Feeds-udvidelsen | Microsoft Docs
description: Beskriver udvidelsen Envestnet Yodlee Bank Feeds, der sammenkæder med bankkonti, så du hurtigt kan afstemme betalinger.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d79ef7c076ec3a529aeb0c679b8b61658ef65af5
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315344"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a>Udvidelsen Envestnet Yodlee Bank Feeds
Med tjenesten Envestnet Yodlee Bank Feeds kan du knytte systembankkontoen til din onlinebankkonto for hurtigt at afstemme indbetalinger til bankkonti. Det betyder, at det seneste bankkontoudtog automatisk eller manuelt indlæses i udligningskladden, hvilket sikrer, at du altid behandler de seneste betalinger med minimal risiko for fejl.

Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i USA og Canada.

> [!NOTE]
> Denne funktionalitet understøttes kun i onlineversionen af Business Central. Hvis du vil bruge denne funktionalitet lokalt, skal du have en cobrand-konto hos Envestnet Yodlee.<br /><br />

> [!IMPORTANT]
> På grund af det nye betalingstjenestedirektiv i Europa (PSD2) kan du efter den 14. september 2019 ikke længere automatisk importere bankkontoudtog fra banker i Storbritannien til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vi overvejer evt. at tilbyde denne funktion igen i fremtiden.

Envestnet Yodlee Bank Feeds-tjenesten giver følgende fordele:

* Fjerner behovet for manuel indtastning.
* Forbedrer effektivitet og nøjagtighed, når du udfører en udligning af en betaling.
* Understøtter et stort antal banker.
* Tillader opdaterede oplysninger om banktransaktioner fra [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Understøtter manuelle samt automatiske bankfeeds.
* Gør det muligt at outsource betalingsudligning til en bogholder ved at give adgang til bankkontoudtog.

Du kan finde flere oplysninger i [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)    
[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
