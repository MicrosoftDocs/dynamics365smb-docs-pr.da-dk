---
title: Konfigurere betalingsvilkår
description: Forfaldsdato og betalinger styres ved hjælp af betalingsbetingelser.
author: brentholtorf
ms.topic: conceptual
ms.search.form: '4,'
ms.date: 09/05/2023
ms.author: bholtorf
---
# Konfiguration af betalingsbetingelser

Betalingsbetingelser bestemmer, hvordan du administrerer forfaldsdatoer og kontantrabatter. Du kan oprette koder og bruge datoformler til at definere betalingsbetingelserne. Når du tilmelder dig første gang til [!INCLUDE [prod_short](includes/prod_short.md)], giver demonstrationsvirksomheden nogle få betalingsmetoder, som virksomheder ofte bruger. Du kan dog tilføje lige så mange, du vil.  

Hvis du vil knytte betalingsbetingelse til debitorer og kreditorer, anvendes den samme betingelse altid på de salgs- og købsdokumenter, du opretter til dem. Bilagsdatoerne på salgs- og købsdokumenterne, ikke bogføringsdatoerne, bruges til at beregne forfaldsdatoer for betalinger. Hvis det er nødvendigt, kan du ændre betingelserne på salgs-eller købsdokumentet, f.eks. Hvis du ønsker, at en bestemt kunde skal betale inden for syv dage i stedet for standard 14 dage. Når du ændrer betingelserne i dokumentet, ændres den standardbetalingsbetingelse, der er tildelt debitoren, ikke. De samme betalingsbetingelser bruges til salgs- og købsdokumenter.

Når du bogfører en faktura, beregnes [!INCLUDE [prod_short](includes/prod_short.md)] kontantrabatten ud fra betalingsbetingelserne. Kontantrabatdatoen er den sidste dato, hvor debitoren kan opnå rabat. Datoen beregnes også, når du bogfører en faktura.  

Når du bogfører en kreditnota, beregner [!INCLUDE [prod_short](includes/prod_short.md)] kontantrabatter på grundlag af betalingsbetingelserne. Rabatten på kreditnotaer beregnes efter samme princip som i forbindelse med kontantrabatter på fakturaer. Når du anvender en kreditnota på en faktura, reducerer [!INCLUDE [prod_short](includes/prod_short.md)] rabatbeløbet for fakturaen med kreditnotaens rabatbeløb.  

Hvis du vil sende rykkere til kunder om forfaldne betalinger, skal du oprette rykkerniveauer og-betingelser. Hvis du vil vide mere om rykkere, skal du gå til [Konfigurere rykkerbetingelser og -niveauer](finance-setup-reminders.md).  

## Sådan defineres betalingsbetingelser

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingsbetingelser**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Efter du har angivet betalingsbetingelserne, kan du tildele dem til debitorer og kreditorer. Du kan også tildele betalingsbetingelser til betalingsmåder.  

> [!TIP]
> I basisversionen af [!INCLUDE [prod_short](includes/prod_short.md)] skal betalingsbetingelser med delbetalinger ikke understøttes. Du skal i stedet bruge funktionen til forudbetalinger. Du kan få mere at vide om forudbetalinger ved at gå til [Konfigurere forudbetalinger](finance-set-up-prepayments.md).
>
> I nogle lande/områder kan du *angive* betalingsbetingelser med delbetalinger. Hvis du vil vide, om denne dit land/område understøtter denne funktion, skal du gå til **Lokal funktionalitet** i indholdsfortegnelsen i venstre side af [Microsoft Learn](about-localization.md)-artiklen.

## Se også

[Konfigurere betalingsformer](finance-payment-methods.md)  
[Oprette forudbetalinger](finance-set-up-prepayments.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Registrere nye debitorer](sales-how-register-new-customers.md)  
[Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]