---
title: Aktivere debitorbetalinger via betalingstjenester | Microsoft Docs
description: "Gør det lettere for kunderne at betale deres fakturaer ved at aktivere betalingstjenester."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0154f7fc231023542cc5f389ea6c8a3e99c7fffc
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="enable-customer-payments-through-payment-services"></a>Aktivere debitorbetalinger via betalingstjenester
Som et alternativ til opkrævning af betalinger via bankoverførsel eller kreditkort kan dine kunder betale dig via deres konto hos betalingstjenester som Microsoft Pay, PayPal eller WorldPay.  

Når du har aktiveret en betalingstjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)], vises der et link til tjenesten på de salgsdokumenter, som du sender med mail til dine kunder. Kunder kan bruge linket til at gå til betalingstjenesten og betale fakturaen direkte fra salgsdokumentet. Hvis du ikke vil indsætte linket, f.eks. hvis en debitor betaler kontant, kan du fjerne betalingstjenesten fra fakturaen inden bogføringen.  

Microsoft Pay-, PayPal Payments Standard- og WorldPay Payments Standard-udvidelserne installeres i [!INCLUDE[d365fin](includes/d365fin_md.md)] og er klar til aktivering.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Sådan aktiverer du en betalingstjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingstjenester**, og vælg derefter det relaterede link.  
2. I vinduet **Betalingstjenester** skal du vælge handlingen **Ny**.  
3. Vælg betalingstjenesten, og luk derefter vinduet.  
4. I vinduet **Betalingstjenester** skal du vælge handlingen **Konfigurer**.  
5. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Luk vinduet.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Sådan vælger du en betalingstjeneste på en salgsfaktura
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2. Åbn den faktura, du vil betale med betalingstjenesten.  
3. Vælg betalingstjenesten i feltet **Betalingstjeneste**.  

    > [!NOTE]  
    >   Feltet **Betalingstjeneste** er kun tilgængeligt, hvis du har aktiveret betalingstjenesten.  

## <a name="see-also"></a>Se også  
[Konfigurere salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

