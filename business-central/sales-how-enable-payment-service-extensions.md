---
title: Aktivere debitorbetalinger med betalingstjenester
description: Gør det lettere for kunderne at betale deres fakturaer ved at aktivere kundebetaling via betalingstjenester.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.search.forms: 1060, 1061, 1062
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 7dad5bcdc5f3c98364bffc81787639e1f3ff11d2
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9074403"
---
# <a name="enable-customer-payments-through-payment-services"></a>Aktivere debitorbetalinger via betalingstjenester

Som et alternativ til opkrævning af betalinger via bankoverførsel eller kreditkort kan dine kunder betale dig via deres konto hos betalingstjenester som PayPal eller WorldPay.  

Når du har aktiveret en betalingstjeneste i [!INCLUDE[prod_short](includes/prod_short.md)], vises der et link til tjenesten på de salgsdokumenter, som du sender med mail til dine kunder. Kunder kan bruge linket til at gå til betalingstjenesten og betale fakturaen direkte fra salgsdokumentet. Hvis du ikke vil indsætte linket, f.eks. hvis en debitor betaler kontant, kan du fjerne betalingstjenesten fra fakturaen inden bogføringen.  

PayPal Payments Standard- og WorldPay Payments Standard-udvidelserne installeres i [!INCLUDE[prod_short](includes/prod_short.md)] og er klar til aktivering.  

## <a name="to-enable-a-payment-service-in-prod_short"></a>Sådan aktiverer du en betalingstjeneste i [!INCLUDE[prod_short](includes/prod_short.md)]

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingstjenester**, og vælg derefter det relaterede link.  
2. På siden **Betalingstjenester** skal du vælge handlingen **Ny**.  
3. Vælg betalingstjenesten, og luk derefter siden.  
4. På siden **Betalingstjenester** skal du vælge handlingen **Konfiguration**.  
5. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Luk siden.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Sådan vælger du en betalingstjeneste på en salgsfaktura

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2. Åbn den faktura, du vil betale med betalingstjenesten.  
3. Vælg betalingstjenesten i feltet **Betalingstjeneste**.  

    > [!NOTE]  
    > Feltet **Betalingstjeneste** er kun tilgængeligt, hvis du har aktiveret betalingstjenesten.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Konfigurere salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]