---
title: Designdetaljer – Bogføringens grænsefladestruktur | Microsoft Docs
description: Dette emne indeholder en oversigt over de globale procedurer i bogføringens grænsefladestruktur.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5905a16341dc487aaf624810d691ac4628ac2e30
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239517"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="6e8e5-103">Designoplysninger: Bogføring af grænsefladestruktur</span><span class="sxs-lookup"><span data-stu-id="6e8e5-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="6e8e5-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)]-bogføringens grænsefladestruktur er der flere globale procedurer, der bruger den samme struktur:</span><span class="sxs-lookup"><span data-stu-id="6e8e5-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="6e8e5-105">RunWithCheck- og RunWithoutCheck-kaldeprocedurekode – generisk bogføringsgrænseflade for finanskladdelinje.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen. Jnl Line.</span></span>  
* <span data-ttu-id="6e8e5-106">CustPostApplyCustLedgEntry – bogfør debitorudligning, kaldes fra codeunit 226 CustEntry-Udlign bogførte poster.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-106">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="6e8e5-107">VendPostApplyVendLedgEntry – bogfør kreditorudligning, der er kaldt fra codeunit 227 VendEntry-Udlign bogførte poster.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-107">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="6e8e5-108">UnapplyCustLedgEntry – bogfør annullering af debitorudligning, der er kaldt fra codeunit 226 CustEntry-Udlign bogførte poster</span><span class="sxs-lookup"><span data-stu-id="6e8e5-108">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="6e8e5-109">UnapplyVendLedgEntry – bogfør annullering af kreditorudligning, der er kaldt fra codeunit 227 VendEntry-Udlign bogførte poster</span><span class="sxs-lookup"><span data-stu-id="6e8e5-109">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e8e5-110">Se også</span><span class="sxs-lookup"><span data-stu-id="6e8e5-110">See Also</span></span>  
[<span data-ttu-id="6e8e5-111">Designoplysninger: Bogføringsprogramstruktur</span><span class="sxs-lookup"><span data-stu-id="6e8e5-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)