---
title: Aktivere debitorbetalinger via betalingstjenester | Microsoft Docs
description: Gør det lettere for kunderne at betale deres fakturaer ved at aktivere betalingstjenester.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e5d4d9fd0c6857c22f2b4c929a6e6ed528cadf26
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "931672"
---
# <a name="enable-customer-payments-through-payment-services"></a>Aktivere debitorbetalinger via betalingstjenester
Som et alternativ til opkrævning af betalinger via bankoverførsel eller kreditkort kan dine kunder betale dig via deres konto hos betalingstjenester som Microsoft Pay, PayPal eller WorldPay.  

Når du har aktiveret en betalingstjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)], vises der et link til tjenesten på de salgsdokumenter, som du sender med mail til dine kunder. Kunder kan bruge linket til at gå til betalingstjenesten og betale fakturaen direkte fra salgsdokumentet. Hvis du ikke vil indsætte linket, f.eks. hvis en debitor betaler kontant, kan du fjerne betalingstjenesten fra fakturaen inden bogføringen.  

Microsoft Pay-, PayPal Payments Standard- og WorldPay Payments Standard-udvidelserne installeres i [!INCLUDE[d365fin](includes/d365fin_md.md)] og er klar til aktivering.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Sådan aktiverer du en betalingstjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Betalingstjenester**, og vælg derefter det relaterede link.  
2. På siden **Betalingstjenester** skal du vælge handlingen **Ny**.  
3. Vælg betalingstjenesten, og luk derefter siden.  
4. På siden **Betalingstjenester** skal du vælge handlingen **Konfiguration**.  
5. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Luk siden.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Sådan vælger du en betalingstjeneste på en salgsfaktura
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2. Åbn den faktura, du vil betale med betalingstjenesten.  
3. Vælg betalingstjenesten i feltet **Betalingstjeneste**.  

    > [!NOTE]  
    > Feltet **Betalingstjeneste** er kun tilgængeligt, hvis du har aktiveret betalingstjenesten.  

## <a name="see-also"></a>Se også  
[Konfigurere salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
