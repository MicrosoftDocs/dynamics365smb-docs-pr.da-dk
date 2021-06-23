---
title: Designdetaljer – Bogføringens grænsefladestruktur | Microsoft Docs
description: Dette emne indeholder en oversigt over de globale procedurer i bogføringens grænsefladestruktur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 529a0e42d814f0754e62fcc4b93b793d44b8daa7
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215824"
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