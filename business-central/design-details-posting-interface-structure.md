---
title: Designoplysninger - Bogføring af grænsefladestruktur
description: Dette emne indeholder en oversigt over de globale procedurer og designdetaljer i bogføringens grænsefladestruktur.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'posting, interface, design'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-posting-interface-structure"></a>Designoplysninger: Bogføring af grænsefladestruktur
I [!INCLUDE[prod_short](includes/prod_short.md)]-bogføringens grænsefladestruktur er der flere globale procedurer, der bruger den samme struktur:  
  
* RunWithCheck- og RunWithoutCheck-kaldeprocedurekode – generisk bogføringsgrænseflade for finanskladdelinje.  
* CustPostApplyCustLedgEntry – bogfør debitorudligning, kaldes fra codeunit 226 CustEntry-Udlign bogførte poster.  
* VendPostApplyVendLedgEntry – bogfør kreditorudligning, der er kaldt fra codeunit 227 VendEntry-Udlign bogførte poster.  
* UnapplyCustLedgEntry – bogfør annullering af debitorudligning, der er kaldt fra codeunit 226 CustEntry-Udlign bogførte poster  
* UnapplyVendLedgEntry – bogfør annullering af kreditorudligning, der er kaldt fra codeunit 227 VendEntry-Udlign bogførte poster  
  
## <a name="see-also"></a>Se også
[Designoplysninger: Bogføringsprogramstruktur](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
