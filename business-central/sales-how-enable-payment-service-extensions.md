---
title: Aktivere debitorbetalinger med betalingstjenester
description: Gør det lettere for kunderne at betale deres fakturaer ved at aktivere kundebetaling via betalingstjenester.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: online payment
ms.search.forms: '1060, 1061, 1062'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Aktivere debitorbetalinger via betalingstjenester

Som et alternativ til opkrævning af betalinger via bankoverførsel eller kreditkort kan dine kunder betale dig via deres konto hos betalingstjenester som PayPal eller WorldPay.  

Når du har aktiveret en betalingstjeneste i [!INCLUDE[prod_short](includes/prod_short.md)], vises der et link til tjenesten på de salgsdokumenter, som du sender med mail til dine kunder. Kunder kan bruge linket til at gå til betalingstjenesten og betale fakturaen direkte fra salgsdokumentet. Hvis du ikke vil indsætte linket, f.eks. hvis en debitor betaler kontant, kan du fjerne betalingstjenesten fra fakturaen inden bogføringen.  

PayPal Payments Standard- og WorldPay Payments Standard-udvidelserne installeres i [!INCLUDE[prod_short](includes/prod_short.md)] og er klar til aktivering.  

> [!CAUTION]
> Udvidelsen WorldPay Payments Standard udfases. Koden er marked som forældet startende med 2023 udgivelsesbølge 2. Appen er aktiv for de næste tre vigtige udgivelser, og derefter fjernes den.   

## Sådan aktiverer du en betalingstjeneste i [!INCLUDE[prod_short](includes/prod_short.md)]

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingstjenester**, og vælg derefter det relaterede link.  
2. På siden **Betalingstjenester** skal du vælge handlingen **Ny**.  
3. Vælg betalingstjenesten, og luk derefter siden.  
4. På siden **Betalingstjenester** skal du vælge handlingen **Konfiguration**.  
5. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Luk siden.  

## Sådan vælger du en betalingstjeneste på en salgsfaktura

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2. Åbn den faktura, du vil betale med betalingstjenesten.  
3. Vælg betalingstjenesten i feltet **Betalingstjeneste**.  

    > [!NOTE]  
    > Feltet **Betalingstjeneste** er kun tilgængeligt, hvis du har aktiveret betalingstjenesten.  

## Se også

[Konfigurere salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
