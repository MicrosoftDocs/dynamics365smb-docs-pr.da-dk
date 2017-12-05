---
title: "Sådan lukker du åbne vareposter, der fremkommer ved fast udligning i varekladden | Microsoft Docs"
description: "Du kan bruge feltet **Udlign fra-post** i vinduet **Varekladde** for at oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion. For eksempel for at rette den udgående transaktion eller behandle dens returvare."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d30a1316b48bd1b80ab4658ee99b14f0a0217478
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="e6d0e-104">Sådan gør du: Lukke åbne vareposter, der fremkommer ved fast udligning i varekladden</span><span class="sxs-lookup"><span data-stu-id="e6d0e-104">How to: Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="e6d0e-105">Du kan bruge feltet **Udlign fra-post** i vinduet **Varekladde** for at oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion.</span><span class="sxs-lookup"><span data-stu-id="e6d0e-105">You can use the **Applies-from Entry** field in the **Item Journal** window to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="e6d0e-106">For eksempel for at rette den udgående transaktion eller behandle dens returvare.</span><span class="sxs-lookup"><span data-stu-id="e6d0e-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="e6d0e-107">Du kan finde flere oplysninger i Udlign fra-post.</span><span class="sxs-lookup"><span data-stu-id="e6d0e-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="e6d0e-108">Faste udligninger, der er foretaget på denne måde, gælder kun omkostningen, ikke mængden.</span><span class="sxs-lookup"><span data-stu-id="e6d0e-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="e6d0e-109">Derfor lukker den bogførte positive varepost ikke den udlignede udgående post og vil selv forblive åben.</span><span class="sxs-lookup"><span data-stu-id="e6d0e-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="e6d0e-110">Dette gælder også, når du bogfører en fast udligning for en positiv post til en negativ post, der ikke er lukket ved en almindelig positiv post, derefter forbliver både den negative og den positive post åben.</span><span class="sxs-lookup"><span data-stu-id="e6d0e-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="e6d0e-111">Det betyder også, at du ikke kan lukke en lagerperiode, hvis der findes en sådan post.</span><span class="sxs-lookup"><span data-stu-id="e6d0e-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="e6d0e-112">Følgende procedure viser, hvordan du kan lukke disse poster ved at udføre to korrigerende bogføringer i varekladden.</span><span class="sxs-lookup"><span data-stu-id="e6d0e-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="e6d0e-113">Sådan lukkes åbne vareposter, der fremkommer ved fast udligning i varekladden</span><span class="sxs-lookup"><span data-stu-id="e6d0e-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="e6d0e-114">Brug feltet **Udlign fra-post** for at bogføre en positiv regulering med den tilsvarende mængde.</span><span class="sxs-lookup"><span data-stu-id="e6d0e-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="e6d0e-115">Den oprindelige negative post med fast udligning lukkes.</span><span class="sxs-lookup"><span data-stu-id="e6d0e-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="e6d0e-116">Brug feltet **Udlign.postløbenr.** for at bogføre en negativ regulering.</span><span class="sxs-lookup"><span data-stu-id="e6d0e-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="e6d0e-117">Den oprindelige positive rettelsespost med fast udligning lukkes.</span><span class="sxs-lookup"><span data-stu-id="e6d0e-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e6d0e-118">Se også</span><span class="sxs-lookup"><span data-stu-id="e6d0e-118">See Also</span></span>  
[<span data-ttu-id="e6d0e-119">Fremgangsmåde: Fjerne og genanvende poster</span><span class="sxs-lookup"><span data-stu-id="e6d0e-119"> How to: Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="e6d0e-120">[Fremgangsmåde: Behandle salgsreturvarer og annulleringer](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="e6d0e-120">[How to: Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="e6d0e-121">[Opsætte lagerværdi og kostprisberegning](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="e6d0e-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="e6d0e-122">[Administrere lageromkostninger](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="e6d0e-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="e6d0e-123">Designoplysninger: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="e6d0e-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
