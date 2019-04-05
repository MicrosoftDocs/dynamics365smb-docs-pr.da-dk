---
title: Sådan lukker du åbne vareposter, der fremkommer ved fast udligning i varekladden | Microsoft Docs
description: Du kan bruge feltet **Udlign fra-post** på siden **Varekladde** for at oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion. For eksempel for at rette den udgående transaktion eller behandle dens returvare.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: e3f210b86168d34ec775f85b416b6d0e365cce88
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792488"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="19a3d-104">Lukke åbne vareposter, der fremkommer ved fast udligning i varekladden</span><span class="sxs-lookup"><span data-stu-id="19a3d-104">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="19a3d-105">Du kan bruge feltet **Udlign fra-post** på siden **Varekladde** for at oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion.</span><span class="sxs-lookup"><span data-stu-id="19a3d-105">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="19a3d-106">For eksempel for at rette den udgående transaktion eller behandle dens returvare.</span><span class="sxs-lookup"><span data-stu-id="19a3d-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="19a3d-107">Du kan finde flere oplysninger i Udlign fra-post.</span><span class="sxs-lookup"><span data-stu-id="19a3d-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="19a3d-108">Faste udligninger, der er foretaget på denne måde, gælder kun omkostningen, ikke mængden.</span><span class="sxs-lookup"><span data-stu-id="19a3d-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="19a3d-109">Derfor lukker den bogførte positive varepost ikke den udlignede udgående post og vil selv forblive åben.</span><span class="sxs-lookup"><span data-stu-id="19a3d-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="19a3d-110">Dette gælder også, når du bogfører en fast udligning for en positiv post til en negativ post, der ikke er lukket ved en almindelig positiv post, derefter forbliver både den negative og den positive post åben.</span><span class="sxs-lookup"><span data-stu-id="19a3d-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="19a3d-111">Det betyder også, at du ikke kan lukke en lagerperiode, hvis der findes en sådan post.</span><span class="sxs-lookup"><span data-stu-id="19a3d-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="19a3d-112">Følgende procedure viser, hvordan du kan lukke disse poster ved at udføre to korrigerende bogføringer i varekladden.</span><span class="sxs-lookup"><span data-stu-id="19a3d-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="19a3d-113">Sådan lukkes åbne vareposter, der fremkommer ved fast udligning i varekladden</span><span class="sxs-lookup"><span data-stu-id="19a3d-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="19a3d-114">Brug feltet **Udlign fra-post** for at bogføre en positiv regulering med den tilsvarende mængde.</span><span class="sxs-lookup"><span data-stu-id="19a3d-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="19a3d-115">Den oprindelige negative post med fast udligning lukkes.</span><span class="sxs-lookup"><span data-stu-id="19a3d-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="19a3d-116">Brug feltet **Udlign.postløbenr.** for at bogføre en negativ regulering.</span><span class="sxs-lookup"><span data-stu-id="19a3d-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="19a3d-117">Den oprindelige positive rettelsespost med fast udligning lukkes.</span><span class="sxs-lookup"><span data-stu-id="19a3d-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="19a3d-118">Se også</span><span class="sxs-lookup"><span data-stu-id="19a3d-118">See Also</span></span>  
[<span data-ttu-id="19a3d-119">Fjerne og genanvende vareposter</span><span class="sxs-lookup"><span data-stu-id="19a3d-119"> Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="19a3d-120">[Behandle salgsreturvarer og annulleringer](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="19a3d-120">[Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="19a3d-121">[Opsætte lagerværdi og kostprisberegning](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="19a3d-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="19a3d-122">[Administrere lageromkostninger](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="19a3d-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="19a3d-123">Designoplysninger: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="19a3d-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
