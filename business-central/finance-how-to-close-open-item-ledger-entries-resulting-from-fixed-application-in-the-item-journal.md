---
title: Lukke vareposter, der stammer fra brug af fast udligning.
description: Se, hvordan du kan oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion i varekladden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/14/2020
ms.author: edupont
ms.openlocfilehash: 9aa24653d4ae957ff741e85a99c13e0c9a8f7173
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381952"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="a31a4-103">Lukke åbne vareposter, der fremkommer ved fast udligning i varekladden</span><span class="sxs-lookup"><span data-stu-id="a31a4-103">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>

<span data-ttu-id="a31a4-104">Du kan bruge feltet **Udlign fra-post** på siden **Varekladde** for at oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion.</span><span class="sxs-lookup"><span data-stu-id="a31a4-104">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="a31a4-105">For eksempel for at rette den udgående transaktion eller behandle dens returvare.</span><span class="sxs-lookup"><span data-stu-id="a31a4-105">For example, to correct the outbound transaction or to process its return.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="a31a4-106">Faste udligninger, der er foretaget på denne måde, gælder kun omkostningen, ikke mængden.</span><span class="sxs-lookup"><span data-stu-id="a31a4-106">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="a31a4-107">Derfor lukker den bogførte positive varepost ikke den udlignede udgående post og vil selv forblive åben.</span><span class="sxs-lookup"><span data-stu-id="a31a4-107">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="a31a4-108">Dette gælder også, når du bogfører en fast udligning for en positiv post til en negativ post, der ikke er lukket ved en almindelig positiv post, derefter forbliver både den negative og den positive post åben.</span><span class="sxs-lookup"><span data-stu-id="a31a4-108">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>
> <span data-ttu-id="a31a4-109">Det betyder også, at du ikke kan lukke en lagerperiode, hvis der findes en sådan post.</span><span class="sxs-lookup"><span data-stu-id="a31a4-109">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="a31a4-110">Du kan ændre og genanvende udligningsposter under visse betingelser ved hjælp af siden **Applikationskladde**.</span><span class="sxs-lookup"><span data-stu-id="a31a4-110">You can change and reapply application entries under certain conditions by using the **Application Worksheet** page.</span></span>  

<span data-ttu-id="a31a4-111">Følgende procedure viser, hvordan du kan lukke disse poster ved at udføre to korrigerende bogføringer i varekladden.</span><span class="sxs-lookup"><span data-stu-id="a31a4-111">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="a31a4-112">Sådan lukkes åbne vareposter, der fremkommer ved fast udligning i varekladden</span><span class="sxs-lookup"><span data-stu-id="a31a4-112">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1. <span data-ttu-id="a31a4-113">Brug feltet **Udlign fra-post** for at bogføre en positiv regulering med den tilsvarende mængde.</span><span class="sxs-lookup"><span data-stu-id="a31a4-113">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="a31a4-114">Den oprindelige negative post med fast udligning lukkes.</span><span class="sxs-lookup"><span data-stu-id="a31a4-114">This closes the original negative entry with a fixed application.</span></span>  

    <span data-ttu-id="a31a4-115">Feltet **Udlign fra post** angiver antallet af udgående vareposter, hvis omkostninger videresendes til den indgående varepost, når du bogfører en indgående transaktion af typen **Opregulering** eller **Køb** med varekladden.</span><span class="sxs-lookup"><span data-stu-id="a31a4-115">The **Applies-from Entry** field specifies the number of the outbound item ledger entry whose cost is forwarded to the inbound item ledger entry when you post an inbound transaction of type **Positive Adjmt.** or **Purchase** with the item journal.</span></span>  
2. <span data-ttu-id="a31a4-116">Brug feltet **Udlign.postløbenr.** for at bogføre en negativ regulering.</span><span class="sxs-lookup"><span data-stu-id="a31a4-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="a31a4-117">Den oprindelige positive rettelsespost med fast udligning lukkes.</span><span class="sxs-lookup"><span data-stu-id="a31a4-117">This closes the original corrective positive entry with a fixed application.</span></span>  

    <span data-ttu-id="a31a4-118">Feltet **Udligningspostløbenr.** angiver, om antallet på varekladdelinjen skal udlignes med et bilag, der allerede er bogført.</span><span class="sxs-lookup"><span data-stu-id="a31a4-118">The **Applies-to Entry** field specifies if the quantity in the item journal line should be applied to an already-posted document.</span></span> <span data-ttu-id="a31a4-119">Hvis det er tilfældet, skal du angiver det løbenummer på vareposten, som varekladdelinjen skal udlignes med.</span><span class="sxs-lookup"><span data-stu-id="a31a4-119">If this is the case, enter the entry number of the item ledger entry to which the item journal line should be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a31a4-120">Se også</span><span class="sxs-lookup"><span data-stu-id="a31a4-120">See Also</span></span>

[<span data-ttu-id="a31a4-121">Fjerne og genanvende vareposter</span><span class="sxs-lookup"><span data-stu-id="a31a4-121">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
[<span data-ttu-id="a31a4-122">Behandle salgsreturvarer og annulleringer</span><span class="sxs-lookup"><span data-stu-id="a31a4-122">Process Sales Returns and Cancellations</span></span>](sales-how-process-sales-returns-cancellations.md)  
[<span data-ttu-id="a31a4-123">Opsætte lagerværdi og kostprisberegning</span><span class="sxs-lookup"><span data-stu-id="a31a4-123">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="a31a4-124">Administrere lageromkostninger</span><span class="sxs-lookup"><span data-stu-id="a31a4-124">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="a31a4-125">Designoplysninger: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="a31a4-125">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]