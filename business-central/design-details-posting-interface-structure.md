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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4815e2d4b69095ff61e92d750963879f93dda875
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390770"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="02b5d-103">Designoplysninger: Bogføring af grænsefladestruktur</span><span class="sxs-lookup"><span data-stu-id="02b5d-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="02b5d-104">I [!INCLUDE[prod_short](includes/prod_short.md)]-bogføringens grænsefladestruktur er der flere globale procedurer, der bruger den samme struktur:</span><span class="sxs-lookup"><span data-stu-id="02b5d-104">In the [!INCLUDE[prod_short](includes/prod_short.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="02b5d-105">RunWithCheck- og RunWithoutCheck-kaldeprocedurekode – generisk bogføringsgrænseflade for</span><span class="sxs-lookup"><span data-stu-id="02b5d-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="02b5d-106">finanskladdelinje.</span><span class="sxs-lookup"><span data-stu-id="02b5d-106">Jnl Line.</span></span>  
* <span data-ttu-id="02b5d-107">CustPostApplyCustLedgEntry – bogfør debitorudligning, kaldes fra codeunit 226 CustEntry-Udlign bogførte poster.</span><span class="sxs-lookup"><span data-stu-id="02b5d-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="02b5d-108">VendPostApplyVendLedgEntry – bogfør kreditorudligning, der er kaldt fra codeunit 227 VendEntry-Udlign bogførte poster.</span><span class="sxs-lookup"><span data-stu-id="02b5d-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="02b5d-109">UnapplyCustLedgEntry – bogfør annullering af debitorudligning, der er kaldt fra codeunit 226 CustEntry-Udlign bogførte poster</span><span class="sxs-lookup"><span data-stu-id="02b5d-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="02b5d-110">UnapplyVendLedgEntry – bogfør annullering af kreditorudligning, der er kaldt fra codeunit 227 VendEntry-Udlign bogførte poster</span><span class="sxs-lookup"><span data-stu-id="02b5d-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="02b5d-111">Se også</span><span class="sxs-lookup"><span data-stu-id="02b5d-111">See Also</span></span>  
[<span data-ttu-id="02b5d-112">Designoplysninger: Bogføringsprogramstruktur</span><span class="sxs-lookup"><span data-stu-id="02b5d-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]