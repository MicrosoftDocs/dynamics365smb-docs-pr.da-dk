---
title: "Sådan fortryder du bogføring af afgang | Microsoft Docs"
description: "Det kan ske, at bogført afgang skal tilbageføres. Det kan f.eks. ske, hvis en oplysning registreres forkert, så et forkert afgangsantal bogføres på en produktionsordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 73d90f585b86785b9bdb1355a52a682612488182
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="reverse-output-posting"></a><span data-ttu-id="d0067-104">Tilbageføre bogføring af afgang</span><span class="sxs-lookup"><span data-stu-id="d0067-104">Reverse Output Posting</span></span>
<span data-ttu-id="d0067-105">Det kan ske, at bogført afgang skal tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="d0067-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="d0067-106">Det kan f.eks. ske, hvis en oplysning registreres forkert, så et forkert afgangsantal bogføres på en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="d0067-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="d0067-107">Tilbageføre en afgangsbogføring</span><span class="sxs-lookup"><span data-stu-id="d0067-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="d0067-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Afgangskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d0067-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="d0067-109">Vælg en kørsel.</span><span class="sxs-lookup"><span data-stu-id="d0067-109">Select your batch.</span></span>  
2. <span data-ttu-id="d0067-110">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="d0067-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="d0067-111">Du kan finde flere oplysninger i [Massebogføre afgang og operationstider](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="d0067-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="d0067-112">Vælg den tilknyttede varepost i feltet **Udlign.postløbenr.**.</span><span class="sxs-lookup"><span data-stu-id="d0067-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="d0067-113">Det tilbagefører kapacitets- og vareposterne.</span><span class="sxs-lookup"><span data-stu-id="d0067-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="d0067-114">Bogfør tilbageførslen ved at bogføre kladden.</span><span class="sxs-lookup"><span data-stu-id="d0067-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="d0067-115">Posterne i afgangskladden bogføres til vareposten som en positiv regulering.</span><span class="sxs-lookup"><span data-stu-id="d0067-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d0067-116">Se også</span><span class="sxs-lookup"><span data-stu-id="d0067-116">See Also</span></span>  
 <span data-ttu-id="d0067-117">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="d0067-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="d0067-118">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="d0067-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="d0067-119">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="d0067-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="d0067-120">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="d0067-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="d0067-121">Køb</span><span class="sxs-lookup"><span data-stu-id="d0067-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="d0067-122">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d0067-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

