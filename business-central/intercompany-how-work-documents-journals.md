---
title: Bogføre koncerninterne dokumenter og kladder
description: Flere oplysninger om brug af koncerninterne dokumenter eller kladder til at bogføre transaktioner med koncerninterne partnere.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary, bank-to-bank'
ms.search.form: '600, 610'
ms.service: dynamics-365-business-central
---
# Arbejde med koncerninterne dokumenter og kladder

Bruge IC-dokumenter eller -kladder til at bogføre transaktioner med koncerninterne partnere. Du kan bogføre transaktioner på finanskonti, og hvis du har oprettet IC-bankkonti, kan du også bogføre bank-til-bank-transaktioner. Hvis du vil vide mere om oprettelse af IC-bankkonti, skal du vælge at [Angive de bankkonti, der skal bruges til IC-partnere](intercompany-how-setup.md#specify-the-bank-accounts-to-use-for-intercompany-partners).  

Når du bogfører et koncerninternt dokument eller koncernintern kladde i regnskabet, oprettes der et tilsvarende dokument eller en tilsvarende kladde i din koncerninterne udbakke. Du kan overføre linjen fra din udbakke til partneren. Din partner kan derefter bogføre den tilsvarende transaktion direkte i sit eget regnskab uden at skulle indtaste oplysningerne igen.

For salgs- og købsdokumenter sikrer den koncerninterne partnerkode på den involverede debitor eller kreditor, at alle ordrer og fakturaer, der oprettes på baggrund af transaktioner med disse virksomheder, vil resultere i tilsvarende dokumenter i partnervirksomheder. Regnskabets balance korrekt.

Det samme gælder for IC-finanskladdelinjer. Du behøver ikke at angive konti, men du skal blot vælge partnervirksomheden. De tilsvarende IC-finanskladdelinjer oprettes derefter i partnervirksomheden.

## Udfylde og indsende en IC-salgsordre

Du kan sende salgs- og købsordrer og returordrer, før du bogfører dem. Fakturaer og kreditnotaer kan ikke sendes, før de er blevet bogført.

Den følgende procedure beskriver, hvordan du udfylder og sender en IC-salgsordre. Samme fremgangsmåde anvendes på koncerninterne købsordrer og returordrer og bogførte IC-fakturaer og kreditnotaer.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Vælg **Ny** for at oprette en ny salgsordre. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Sørg for, at debitoren er en koncernintern partner.
5. Hvis du vil sende salgsordren, før du bogfører den, skal du vælge handlingen **Send IC-salgsordre**.

> [!NOTE]
> Hvis du udfører trin 5, flyttes salgsordren derefter til din koncerninterne udbakke, hvor kan du sende den senere. Du kan få mere at vide om IC-indbakken og -udbakken ved at gå til [Administrere IC-indbakke og -Udbakke](intercompany-how-manage-intercompany-inbox.md).

## Udfylde og bogføre en IC-kladde

Når du bogfører en koncernintern finanskladdelinje i regnskabet, oprettes der en tilsvarende finanskladdelinje i din koncerninterne udbakke, som du kan overføre til partneren. Med 2022 udgivelsesbølge 1 kan du også angive, at regnskabet automatisk skal oprette IC-transaktioner, der er modtaget fra IC-partnere, og som bogføres via IC-finanskladden. Din partner kan derefter bogføre den tilsvarende transaktion direkte i sit eget regnskab uden at skulle indtaste oplysningerne igen.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncerninterne finanskladder**, og vælg derefter det relaterede link.  
2. Åbne sagskladden. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).
3. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](../archive/invoicing/includes/tooltip-inline-tip_md.md)]
4. I feltet **IC-partner finanskontonr.** skal du angive den koncerninterne finanskonto , som beløbet skal bogføres til i partnerens virksomhed.

    > [!NOTE]
    > Feltet kan kun udfyldes på en linje med en bankkonto eller finanskonto i feltet **Kontonr.** eller **Modkonto**.  
5. Vælg handlingen **Bogfør**.

De involverede poster bogføres i regnskabet, og der oprettes en kladde med de tilsvarende poster i din koncerninterne udbakke, som du kan sende til din partnervirksomhed.

## Se også

[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]