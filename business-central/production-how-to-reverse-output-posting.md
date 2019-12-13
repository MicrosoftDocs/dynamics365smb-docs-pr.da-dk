---
title: Sådan fortryder du bogføring af afgang | Microsoft Docs
description: Det kan ske, at bogført afgang skal tilbageføres. Det kan f.eks. ske, hvis en oplysning registreres forkert, så et forkert afgangsantal bogføres på en produktionsordre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2cdda8a01d6391f97bfae5600ce35d2ab989ae54
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877835"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="51654-104">Tilbageføre bogføring af afgang</span><span class="sxs-lookup"><span data-stu-id="51654-104">Reverse Output Posting</span></span>
<span data-ttu-id="51654-105">Det kan ske, at bogført afgang skal tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="51654-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="51654-106">Det kan f.eks. ske, hvis en oplysning registreres forkert, så et forkert afgangsantal bogføres på en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="51654-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="51654-107">Tilbageføre en afgangsbogføring</span><span class="sxs-lookup"><span data-stu-id="51654-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="51654-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Afgangskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="51654-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="51654-109">Vælg en kørsel.</span><span class="sxs-lookup"><span data-stu-id="51654-109">Select your batch.</span></span>  
2. <span data-ttu-id="51654-110">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="51654-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="51654-111">Du kan finde flere oplysninger i [Massebogføre afgang og operationstider](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="51654-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="51654-112">Vælg den tilknyttede varepost i feltet **Udlign.postløbenr.**.</span><span class="sxs-lookup"><span data-stu-id="51654-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="51654-113">Det tilbagefører kapacitets- og vareposterne.</span><span class="sxs-lookup"><span data-stu-id="51654-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="51654-114">Bogfør tilbageførslen ved at bogføre kladden.</span><span class="sxs-lookup"><span data-stu-id="51654-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="51654-115">Posterne i afgangskladden bogføres til vareposten som en positiv regulering.</span><span class="sxs-lookup"><span data-stu-id="51654-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="51654-116">Se også</span><span class="sxs-lookup"><span data-stu-id="51654-116">See Also</span></span>  
 <span data-ttu-id="51654-117">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="51654-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="51654-118">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="51654-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="51654-119">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="51654-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="51654-120">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="51654-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="51654-121">Køb</span><span class="sxs-lookup"><span data-stu-id="51654-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="51654-122">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="51654-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
