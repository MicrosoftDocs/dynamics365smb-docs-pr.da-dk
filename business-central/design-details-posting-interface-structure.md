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
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b852d6e5d7f96cfba64de219ca414de60cea3a31
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777596"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="0fac3-103">Designoplysninger: Bogføring af grænsefladestruktur</span><span class="sxs-lookup"><span data-stu-id="0fac3-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="0fac3-104">I [!INCLUDE[prod_short](includes/prod_short.md)]-bogføringens grænsefladestruktur er der flere globale procedurer, der bruger den samme struktur:</span><span class="sxs-lookup"><span data-stu-id="0fac3-104">In the [!INCLUDE[prod_short](includes/prod_short.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="0fac3-105">RunWithCheck- og RunWithoutCheck-kaldeprocedurekode – generisk bogføringsgrænseflade for</span><span class="sxs-lookup"><span data-stu-id="0fac3-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="0fac3-106">finanskladdelinje.</span><span class="sxs-lookup"><span data-stu-id="0fac3-106">Jnl Line.</span></span>  
* <span data-ttu-id="0fac3-107">CustPostApplyCustLedgEntry – bogfør debitorudligning, kaldes fra codeunit 226 CustEntry-Udlign bogførte poster.</span><span class="sxs-lookup"><span data-stu-id="0fac3-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="0fac3-108">VendPostApplyVendLedgEntry – bogfør kreditorudligning, der er kaldt fra codeunit 227 VendEntry-Udlign bogførte poster.</span><span class="sxs-lookup"><span data-stu-id="0fac3-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="0fac3-109">UnapplyCustLedgEntry – bogfør annullering af debitorudligning, der er kaldt fra codeunit 226 CustEntry-Udlign bogførte poster</span><span class="sxs-lookup"><span data-stu-id="0fac3-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="0fac3-110">UnapplyVendLedgEntry – bogfør annullering af kreditorudligning, der er kaldt fra codeunit 227 VendEntry-Udlign bogførte poster</span><span class="sxs-lookup"><span data-stu-id="0fac3-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fac3-111">Se også</span><span class="sxs-lookup"><span data-stu-id="0fac3-111">See Also</span></span>  
[<span data-ttu-id="0fac3-112">Designoplysninger: Bogføringsprogramstruktur</span><span class="sxs-lookup"><span data-stu-id="0fac3-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]