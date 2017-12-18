---
title: "Sådan kombineres leverancer på én enkelt faktura | Microsoft Docs"
description: "Hvis du vil fakturere mere end én leverance samtidig, kan du bruge samlefunktionen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e6be50119da5c617ce6dbf603903266f9ced821e
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-combine-shipments-on-a-single-invoice"></a>Sådan kombineres leverancer på én enkelt faktura
Hvis du vil fakturere mere end én leverance samtidig, kan du bruge samlefunktionen.  

 Før du kan oprette en samleleverance, skal der bogføres mere end én salgsleverance i samme valuta til den samme kunde. Du skal med andre ord have udfyldt to eller flere salgsordrer og bogført dem som leveret, men ikke faktureret. For at kombinere leverancer skal afkrydsningsfeltet **Tillad samlefaktura** være markeret i oversigtspanelet **Levering** på **debitor**-kortet.  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Sådan kombinerer du manuelt leverancer på én enkelt faktura  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Du kan finde flere oplysninger under [Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md).
3. I feltet **Kundenr** skal du angive den kunde, der skal modtage fakturaen for de leverede varer.  
4. I oversigtspanelet **Linjer** skal du vælge handlingen **Hent salgsleverancelinjer**.  
5. Vælg de leverancelinjer, der skal indgå i fakturaen:  

    - Hvis alle linjer skal indsættes, skal du markere samtlige linjer og vælge knappen **OK**.  
    - Hvis specifikke linjer skal indsættes, skal du markere linjerne og vælge knappen **OK**. Du kan bruge Ctrl-tasten til at markere flere ikke-fortløbende linjer.  

    Hvis du kommer til at vælge en forkert leveringslinje eller vil begynde forfra, skal du bare slette linjerne på fakturaen og bruge funktionen **Hent salgsleverancelinjer** igen.  
7. Vælg handlingen **Bogfør** for at fakturere kladden.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Sådan kombinerer du automatisk leverancer på én enkelt faktura  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Tillad samlefaktura**, og vælg derefter det relaterede link. Kørselsvinduet åbner.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Markér afkrydsningsfeltet **Bogfør fakturaer**.  
4.  Vælg knappen **OK**.  

> [!NOTE]  
>  Du er nødt til at bogføre fakturaerne manuelt, hvis afkrydsningsfeltet **Bogfør fakturaer** ikke var markeret til kørslen.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Sådan fjernes åbne salgsordrer efter bogføring af kombineret leverance 
Når leverancer samles på en faktura og bogføres, oprettes der en bogført salgsfaktura for de fakturerede linjer. Feltet **Faktureret (antal)** på den oprindelige rammesalgsordre eller salgsordre opdateres på basis af det fakturerede antal.  

Når du fakturerer leverancer på denne måde, findes de ordrer, som leverancerne er bogført fra, stadig, selvom de er leveret og faktureret i fuldt omfang.   

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Slet fakturerede salgsordrer**, og vælg linket.  
2. I feltet **Nummer** skal du angive, hvilke ordrer der skal slettes.  
3. Vælg knappen **OK**.  

Du kan også slette individuelle salgsordrer manuelt.  

Gentag trin 1 til 3 for eventuelle andre berørte dokumenter, f.eks. rammesalgsordrer.

## <a name="see-also"></a>Se også  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

