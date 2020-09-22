---
title: Designdetaljer – Bogføringens grænsefladestruktur | Microsoft Docs
description: Dette emne indeholder en oversigt over de globale procedurer i bogføringens grænsefladestruktur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1e80b905d96fc2204b61b03c0970257755b9e105
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787342"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="8b11c-103">Designoplysninger: Bogføring af grænsefladestruktur</span><span class="sxs-lookup"><span data-stu-id="8b11c-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="8b11c-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)]-bogføringens grænsefladestruktur er der flere globale procedurer, der bruger den samme struktur:</span><span class="sxs-lookup"><span data-stu-id="8b11c-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="8b11c-105">RunWithCheck- og RunWithoutCheck-kaldeprocedurekode – generisk bogføringsgrænseflade for</span><span class="sxs-lookup"><span data-stu-id="8b11c-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="8b11c-106">finanskladdelinje.</span><span class="sxs-lookup"><span data-stu-id="8b11c-106">Jnl Line.</span></span>  
* <span data-ttu-id="8b11c-107">CustPostApplyCustLedgEntry – bogfør debitorudligning, kaldes fra codeunit 226 CustEntry-Udlign bogførte poster.</span><span class="sxs-lookup"><span data-stu-id="8b11c-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="8b11c-108">VendPostApplyVendLedgEntry – bogfør kreditorudligning, der er kaldt fra codeunit 227 VendEntry-Udlign bogførte poster.</span><span class="sxs-lookup"><span data-stu-id="8b11c-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="8b11c-109">UnapplyCustLedgEntry – bogfør annullering af debitorudligning, der er kaldt fra codeunit 226 CustEntry-Udlign bogførte poster</span><span class="sxs-lookup"><span data-stu-id="8b11c-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="8b11c-110">UnapplyVendLedgEntry – bogfør annullering af kreditorudligning, der er kaldt fra codeunit 227 VendEntry-Udlign bogførte poster</span><span class="sxs-lookup"><span data-stu-id="8b11c-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b11c-111">Se også</span><span class="sxs-lookup"><span data-stu-id="8b11c-111">See Also</span></span>  
[<span data-ttu-id="8b11c-112">Designoplysninger: Bogføringsprogramstruktur</span><span class="sxs-lookup"><span data-stu-id="8b11c-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)