---
title: Bruge udvidelsen Salgs- og lagerprognose til at styre lagerbeholdningen | Microsoft Docs
description: "Udvidelsen hjælper dig med at forudse salg, få et klart billede af forventede lagermangler og oprette genbestillingsanmodninger til kreditorer."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a0cac0236611c90d3d1fdf1bae9deaaeb235b540
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="sales-and-inventory-forecast-for-dynamics-365-for-financials"></a><span data-ttu-id="106de-103">Salgs- og lagerprognose for Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="106de-103">Sales and Inventory Forecast for Dynamics 365 for Financials</span></span>
<span data-ttu-id="106de-104">Lagerstyring håndterer balancen mellem kundeservice og styring af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="106de-104">Inventory management is a trade-off between customer service and managing your cost.</span></span> <span data-ttu-id="106de-105">På én side kræver et lille lager mindre driftskapital, men på den anden side kan manglende lager medføre tabt salg.</span><span class="sxs-lookup"><span data-stu-id="106de-105">On one hand, a low inventory requires less working capital, but, on the other hand, stock-outs potentially lead to missed sales.</span></span> <span data-ttu-id="106de-106">Udvidelsen Salgs- og lagerprognose forudsiger muligt salg ved hjælp af historiske data og giver et klart overblik over forbruget af lageret.</span><span class="sxs-lookup"><span data-stu-id="106de-106">The Sales and Inventory Forecast extension predicts potential sales using historical data and gives a clear overview of expected stock-outs.</span></span> <span data-ttu-id="106de-107">Baseret på prognosen hjælper udvidelsen med at oprette genbestillingsanmodninger til dine leverandører og sparer tid.</span><span class="sxs-lookup"><span data-stu-id="106de-107">Based on the forecast, the extension helps create replenishment requests to your vendors and saves you time.</span></span>  

## <a name="setting-up-forecasting"></a><span data-ttu-id="106de-108">Konfigurere prognose</span><span class="sxs-lookup"><span data-stu-id="106de-108">Setting up forecasting</span></span>
<span data-ttu-id="106de-109">I [!INCLUDE[d365fin](includes/d365fin_md.md)] er forbindelsen til [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) allerede konfigureret for dig.</span><span class="sxs-lookup"><span data-stu-id="106de-109">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the connection to [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) is already set up for you.</span></span> <span data-ttu-id="106de-110">Du kan dog konfigurere en prognose, hvis du vil bruge en anden type periode i rapporten, f.eks hvis du vil skifte fra prognose pr. måned til prognose pr. kvartal.</span><span class="sxs-lookup"><span data-stu-id="106de-110">But you can configure the forecast to use a different type of period to report by, such as changing from forecasting by month to forecasting by quarter.</span></span> <span data-ttu-id="106de-111">Du kan også vælge, hvor mange perioder prognosen skal beregnes for, afhængigt af hvor detaljeret prognosen skal være.</span><span class="sxs-lookup"><span data-stu-id="106de-111">You can also choose the number of periods to calculate the forecast by, depending on how granular you want the forecast to be.</span></span> <span data-ttu-id="106de-112">Vi anbefaler prognose pr. måned og en horisont på 12 måneder for prognosen.</span><span class="sxs-lookup"><span data-stu-id="106de-112">We suggest that you forecast by month and with a 12 month horizon for the forecast.</span></span>  

## <a name="using-the-forecasts"></a><span data-ttu-id="106de-113">Brug af prognoser</span><span class="sxs-lookup"><span data-stu-id="106de-113">Using the forecasts</span></span>
<span data-ttu-id="106de-114">Udvidelsen bruger Cortana Intelligence til at forudse fremtidigt salg ud fra din salgsoversigt, så du bedre kan undgå manglende lager.</span><span class="sxs-lookup"><span data-stu-id="106de-114">The extension uses Cortana Intelligence to predict future sales based on your sales history to help you avoid inventory shortage.</span></span> <span data-ttu-id="106de-115">Når du f.eks. vælger en vare i vinduet **Varer** , og diagrammet i ruden **Vareprognose** viser det anslåede salg af varen i den kommende periode.</span><span class="sxs-lookup"><span data-stu-id="106de-115">For example, when you choose an item in the **Items** window, the chart in the **Item Forecast** pane shows the estimated sales of this item in the coming period.</span></span> <span data-ttu-id="106de-116">På denne måde kan du se, om du sandsynligvis vil løbe tør for lager inden længe.</span><span class="sxs-lookup"><span data-stu-id="106de-116">This way you can see if you are likely to run out of stock of the item soon.</span></span>  

<span data-ttu-id="106de-117">Du kan også bruge udvidelsen til at foreslå, hvornår lageret skal øges.</span><span class="sxs-lookup"><span data-stu-id="106de-117">You can also use the extension to suggest when to stock up on inventory.</span></span> <span data-ttu-id="106de-118">Hvis du f.eks. opretter en købsordre for Fabrikam, fordi du vil købe deres nye skrivebordsstol, vil udvidelsen Salgs- og lagerprognose foreslå, at du også øger lageret af LONDON-drejestolen, som du normalt køber hos denne leverandør.</span><span class="sxs-lookup"><span data-stu-id="106de-118">For example, if you crate a purchase order for Fabrikam because you want to buy their new desk chair, the Sales and Inventory Forecast extension will suggest that you also restock on the LONDON swivel chair that you usually buy from this vendor.</span></span> <span data-ttu-id="106de-119">Det skyldes, at udvidelsen forudser, at lageret af LONDON-drejestolen vil løbe tørt i de kommende to måneder, så du med fordel kan bestille flere stole allerede nu.</span><span class="sxs-lookup"><span data-stu-id="106de-119">This is because the extension forecasts that you will run out of stock of the LONDON swivel chair in the coming two months, so you might want to order more chairs already now.</span></span>  

## <a name="see-also"></a><span data-ttu-id="106de-120">Se også</span><span class="sxs-lookup"><span data-stu-id="106de-120">See Also</span></span>
[<span data-ttu-id="106de-121">Salg</span><span class="sxs-lookup"><span data-stu-id="106de-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="106de-122">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="106de-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="106de-123">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="106de-123">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  

