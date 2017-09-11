---
title: Opdatere valutakurser | Microsoft Docs
description: Hvis du vil bruge flere forskellige valutaer i virksomheden, skal du angive en kode for hver valuta og bruge en ekstern valutakurstjeneste, som Yahoo.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-update-currency-exchange-rates"></a><span data-ttu-id="37c41-103">Fremgangsmåde: Opdatere valutakurser</span><span class="sxs-lookup"><span data-stu-id="37c41-103">How to: Update Currency Exchange Rates</span></span>
<span data-ttu-id="37c41-104">Du skal oprette koder for hver valuta, du bruger, hvis du foretager køb og salg i andre valutaer end din lokale valuta, eller hvis du registrerer finanstransaktioner i forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="37c41-104">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="37c41-105">Denne funktion kræver, at oplevelsen er indstillet til **Pakke**.</span><span class="sxs-lookup"><span data-stu-id="37c41-105">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="37c41-106">Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="37c41-106">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

<span data-ttu-id="37c41-107">Du kan bruge en ekstern tjeneste til at holde dine valutakurser opdaterede.</span><span class="sxs-lookup"><span data-stu-id="37c41-107">You can use an external service to keep your currency exchange rates up to date.</span></span> <span data-ttu-id="37c41-108">Tjenesten Yahoo Currency Exchange Rates er forudinstalleret og klar til at blive aktiveret.</span><span class="sxs-lookup"><span data-stu-id="37c41-108">The Yahoo Currency Exchange Rates service is preinstalled and ready to enable.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="37c41-109">Sådan konfigureres en valutakurstjeneste</span><span class="sxs-lookup"><span data-stu-id="37c41-109">To set up a currency exchange rate service</span></span>
1. <span data-ttu-id="37c41-110">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Valutakurstjenester**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="37c41-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="37c41-111">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="37c41-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="37c41-112">I vinduet **Valutakurstjenester** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="37c41-112">In the **Currency Exchange Rate Service** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="37c41-113">Marker afkrydsningsfeltet **Aktiveret** for at aktivere tjenesten.</span><span class="sxs-lookup"><span data-stu-id="37c41-113">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="37c41-114">Sådan opdateres valutakurser fra en tjeneste</span><span class="sxs-lookup"><span data-stu-id="37c41-114">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="37c41-115">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Valutaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="37c41-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="37c41-116">Vælg handlingen **Opdater valutakurser**.</span><span class="sxs-lookup"><span data-stu-id="37c41-116">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="37c41-117">Værdien i feltet **Valutakurs** i vinduet **Valutaer** opdateres med den seneste valutakurs.</span><span class="sxs-lookup"><span data-stu-id="37c41-117">The value in the **Exchange Rate** field in the **Currencies** window is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="37c41-118">Se også</span><span class="sxs-lookup"><span data-stu-id="37c41-118">See Also</span></span>
[<span data-ttu-id="37c41-119">Afslutning af år og perioder</span><span class="sxs-lookup"><span data-stu-id="37c41-119">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="37c41-120">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="37c41-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

