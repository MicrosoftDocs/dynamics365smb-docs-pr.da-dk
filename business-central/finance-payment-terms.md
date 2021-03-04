---
title: Definere betalingsbetingelser
description: Brug betalingsbetingelser til at håndtere forfaldsdatoer og kontantrabatter i basisversionen af Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 01/21/2021
ms.author: edupont
ms.openlocfilehash: c58db7ddd1047d9228a39e7825a5f5ef04fc925a
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035527"
---
# <a name="set-up-payment-terms"></a>Konfiguration af betalingsbetingelser

Betalingsbetingelser bestemmer, hvordan du administrerer forfaldsdatoer og kontantrabatter. Du kan oprette koder og bruge datoformler til at definere betalingsbetingelserne. Når du tilmelder dig første gang til [!INCLUDE [prod_short](includes/prod_short.md)], giver demonstrationsvirksomheden nogle få betalingsmetoder, som virksomheder ofte bruger. Du kan dog tilføje lige så mange, du vil.  

Du kan knytte en betalingsbetingelse til debitorer og kreditorer, så den samme betingelse altid bruges på de salgs- og købsdokumenter, du opretter til dem. Hvis det er nødvendigt, kan du ændre betingelserne på salgs-eller købsdokumentet, f. eks. Hvis du ønsker, at en bestemt kunde skal betale inden for syv dage i stedet for standard 14 dage. Dette ændrer ikke den betalingsbetingelse, der som standard er knyttet til kreditoren. De samme betalingsbetingelser bruges til salgs- og købsdokumenter.

Når du derefter bogfører en faktura [!INCLUDE [prod_short](includes/prod_short.md)], beregnes kontantrabatten ud fra betalingsbetingelserne. Kontantrabatdatoen, dvs. den seneste dato hvor debitoren kan betale og modtage kontantrabatten, beregnes også på dette tidspunkt.  

Når du bogfører en kreditnota [!INCLUDE [prod_short](includes/prod_short.md)], beregner beregningen mulige kontantrabatter på grundlag af betalingsbetingelserne. Rabatten på kreditnotaer beregnes efter samme princip som i forbindelse med kontantrabatter på fakturaer. Når der oprettes en kreditnota i forbindelse med en faktura, vil det mulige kontantrabatbeløb for fakturaen blive reduceret med kontantrabatbeløbet for kreditnotaen.  

Hvis du vil sende rykkere til kunder om forfaldne betalinger, skal du oprette rykkerniveauer og-betingelser. Du kan finde flere oplysninger i [Konfiguration af rykkerbetingelser og -niveauer](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Sådan defineres betalingsbetingelser

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), åbn **Betalingsbetingelser**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Efter du har angivet betalingsbetingelserne, kan du tildele dem til debitorer og kreditorer. Du kan også tildele betalingsbetingelser til betalingsmåder.  

> [!TIP]
> I basisversionen af [!INCLUDE [prod_short](includes/prod_short.md)] skal betalingsbetingelser med delbetalinger ikke understøttes. Du skal i stedet bruge funktionen til forudbetalinger. Du kan finde flere oplysninger i [Oprette forudbetalinger](finance-set-up-prepayments.md).
>
> I nogle lande kan du *angive* betalingsbetingelser med delbetalinger. Hvis du vil vide, om denne funktion understøttes i dit land, skal du se afsnittet **Lokal funktionalitet** i navigationsruden i venstre side på [Docs.microsoft.com ](about-localization.md)-webstedet.

## <a name="see-also"></a>Se også

[Konfigurere betalingsmetoder](finance-payment-methods.md)  
[Oprette forudbetalinger](finance-set-up-prepayments.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Registrere nye debitorer](sales-how-register-new-customers.md)  
[Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]