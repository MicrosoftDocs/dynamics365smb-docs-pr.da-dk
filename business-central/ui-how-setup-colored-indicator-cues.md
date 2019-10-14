---
title: Tilpasse visuelle signaler om en køindikators aktivitet | Microsoft Docs
description: Du kan oprette et farvet symbol i et Køindikator-felt for at levere et tilpasset visuelt signal om køindikatorens aktivitet.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 10/01/2019
ms.author: solsen
redirect_url: admin-how-set-up-colored-indicator-on-cues
ms.openlocfilehash: 69defdcec64cfaa710af7d3f5b9b35e072c7c3d6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315176"
---
# <a name="set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="cc4f2-103">Oprette en farvet indikator på køindikatorer</span><span class="sxs-lookup"><span data-stu-id="cc4f2-103">Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="cc4f2-104">Du kan oprette køindikatorer, der vises i rollecenteret, for at medtage en indikator, der skifter farve ud fra dataværdierne i køerne.</span><span class="sxs-lookup"><span data-stu-id="cc4f2-104">You can set up Cues that appear on the Role Center to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="cc4f2-105">Indikatoren vises som en farvet streg langs den øverste kant af feltet Køindikator.</span><span class="sxs-lookup"><span data-stu-id="cc4f2-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="cc4f2-106">Det indeholder et visuelt signal af status for køindikatorens aktivitet, som kan indikere favorable eller ikke-favorable betingelser for at bede brugeren om at handle.</span><span class="sxs-lookup"><span data-stu-id="cc4f2-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="cc4f2-107">Hvis en køindikator f.eks. viser løbende salgsfakturaer, kan du oprette indikatoren som grøn (favorabel), når det samlede antal løbende salgsfakturaer er under 10, og rød (ikke-favorabel), når det samlede antal er større end 20.</span><span class="sxs-lookup"><span data-stu-id="cc4f2-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="cc4f2-108">Fra siden **Opsætning af køindikator** kan du konfigurere indikatorer for alle køindikatorer, der findes i regnskabsdatabasen.</span><span class="sxs-lookup"><span data-stu-id="cc4f2-108">From the **Cue Setup** page, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="cc4f2-109">Hvis du vil konfigurere indikatoren, kan du angive op til to tærskelværdier, der definerer tre områder af dataværdier (lav, mellem og høj), hvor du kan anvende en anden farve (eller type).</span><span class="sxs-lookup"><span data-stu-id="cc4f2-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="cc4f2-110">Sådan opretter farveindikatorer på køindikatorer</span><span class="sxs-lookup"><span data-stu-id="cc4f2-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="cc4f2-111">Under **Aktiviteter** i dit Rollecenter skal du vælge **Konfigurer køindikatorer**.</span><span class="sxs-lookup"><span data-stu-id="cc4f2-111">Under **Activities** on your Role Center, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="cc4f2-112">Siden **Opsætning af køindikator** vises.</span><span class="sxs-lookup"><span data-stu-id="cc4f2-112">The **Cue Setup** page appears.</span></span> <span data-ttu-id="cc4f2-113">Siden viser de indikatorer, der aktuelt er konfigureret på køindikatorer.</span><span class="sxs-lookup"><span data-stu-id="cc4f2-113">The page lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="cc4f2-114">Hvis du vil ændre en indikator skal du redigere felterne og ændre f.eks. værdierne for de forskellige intervalgrænser.</span><span class="sxs-lookup"><span data-stu-id="cc4f2-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="cc4f2-115">Følgende tabel viser de farver, der svarer til indstillingerne for felterne **Typen Lavt interval**, **Typen Mellem interval** og **Typen Højt interval**.</span><span class="sxs-lookup"><span data-stu-id="cc4f2-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="cc4f2-116">Indstilling</span><span class="sxs-lookup"><span data-stu-id="cc4f2-116">Option</span></span> | <span data-ttu-id="cc4f2-117">Farve</span><span class="sxs-lookup"><span data-stu-id="cc4f2-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="cc4f2-118">**Ingen**</span><span class="sxs-lookup"><span data-stu-id="cc4f2-118">**None**</span></span> |<span data-ttu-id="cc4f2-119">Ingen farve (samme farve som feltet Køindikator)</span><span class="sxs-lookup"><span data-stu-id="cc4f2-119">No color (same color as the Cue tile)</span></span>|
| <span data-ttu-id="cc4f2-120">**Favorabel**</span><span class="sxs-lookup"><span data-stu-id="cc4f2-120">**Favorable**</span></span> |<span data-ttu-id="cc4f2-121">Grøn</span><span class="sxs-lookup"><span data-stu-id="cc4f2-121">Green</span></span> |
| <span data-ttu-id="cc4f2-122">**Ikke-favorabel**</span><span class="sxs-lookup"><span data-stu-id="cc4f2-122">**Unfavorable**</span></span> |<span data-ttu-id="cc4f2-123">Rød</span><span class="sxs-lookup"><span data-stu-id="cc4f2-123">Red</span></span> |
| <span data-ttu-id="cc4f2-124">**Tvetydig**</span><span class="sxs-lookup"><span data-stu-id="cc4f2-124">**Ambiguous**</span></span> |<span data-ttu-id="cc4f2-125">Gul</span><span class="sxs-lookup"><span data-stu-id="cc4f2-125">Yellow</span></span> |
| <span data-ttu-id="cc4f2-126">**Underordnet**</span><span class="sxs-lookup"><span data-stu-id="cc4f2-126">**Subordinate**</span></span> |<span data-ttu-id="cc4f2-127">Grå</span><span class="sxs-lookup"><span data-stu-id="cc4f2-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="cc4f2-128">Se også</span><span class="sxs-lookup"><span data-stu-id="cc4f2-128">See Also</span></span>
<span data-ttu-id="cc4f2-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cc4f2-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
