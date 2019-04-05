---
title: Sådan fortryder du bogføring af afgang | Microsoft Docs
description: Det kan ske, at bogført afgang skal tilbageføres. Det kan f.eks. ske, hvis en oplysning registreres forkert, så et forkert afgangsantal bogføres på en produktionsordre.
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
ms.openlocfilehash: fb107d6d165ede233799ab165d735c030c0c8bba
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792306"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="32ac9-104">Tilbageføre bogføring af afgang</span><span class="sxs-lookup"><span data-stu-id="32ac9-104">Reverse Output Posting</span></span>
<span data-ttu-id="32ac9-105">Det kan ske, at bogført afgang skal tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="32ac9-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="32ac9-106">Det kan f.eks. ske, hvis en oplysning registreres forkert, så et forkert afgangsantal bogføres på en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="32ac9-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="32ac9-107">Tilbageføre en afgangsbogføring</span><span class="sxs-lookup"><span data-stu-id="32ac9-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="32ac9-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Afgangskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="32ac9-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="32ac9-109">Vælg en kørsel.</span><span class="sxs-lookup"><span data-stu-id="32ac9-109">Select your batch.</span></span>  
2. <span data-ttu-id="32ac9-110">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="32ac9-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="32ac9-111">Du kan finde flere oplysninger i [Massebogføre afgang og operationstider](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="32ac9-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="32ac9-112">Vælg den tilknyttede varepost i feltet **Udlign.postløbenr.**.</span><span class="sxs-lookup"><span data-stu-id="32ac9-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="32ac9-113">Det tilbagefører kapacitets- og vareposterne.</span><span class="sxs-lookup"><span data-stu-id="32ac9-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="32ac9-114">Bogfør tilbageførslen ved at bogføre kladden.</span><span class="sxs-lookup"><span data-stu-id="32ac9-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="32ac9-115">Posterne i afgangskladden bogføres til vareposten som en positiv regulering.</span><span class="sxs-lookup"><span data-stu-id="32ac9-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="32ac9-116">Se også</span><span class="sxs-lookup"><span data-stu-id="32ac9-116">See Also</span></span>  
 <span data-ttu-id="32ac9-117">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="32ac9-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="32ac9-118">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="32ac9-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="32ac9-119">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="32ac9-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="32ac9-120">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="32ac9-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="32ac9-121">Køb</span><span class="sxs-lookup"><span data-stu-id="32ac9-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="32ac9-122">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="32ac9-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
