---
title: Opdatere valutakurser | Microsoft Docs
description: Hvis du vil bruge flere forskellige valutaer i virksomheden, skal du angive en kode for hver valuta og bruge en ekstern valutakurstjeneste.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: da-dk
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a><span data-ttu-id="39176-103">Opdatere valutakurser</span><span class="sxs-lookup"><span data-stu-id="39176-103">Update Currency Exchange Rates</span></span>
<span data-ttu-id="39176-104">Da virksomheder handler i alt flere lande, bliver det mere vigtigt, at de kan handle eller rapportere finansielle oplysninger i mere end én valuta.</span><span class="sxs-lookup"><span data-stu-id="39176-104">As companies operate in increasingly more countries/regions, it becomes more important that they be able to trade and report financials in more than one currency.</span></span> <span data-ttu-id="39176-105">Du skal oprette koder for hver valuta, du bruger, hvis du foretager køb og salg i andre valutaer end din lokale valuta, eller hvis du registrerer finanstransaktioner i forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="39176-105">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>

<span data-ttu-id="39176-106">Finansprogrammet er konfigureret til at bruge den lokale valuta (RV), men du kan også konfigurere det til at bruge en anden valuta med en aktuel valutakurs tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="39176-106">Your general ledger is set up to use your local currency (LCY), but you can set it up to also use another currency with a current exchange rate assigned.</span></span> <span data-ttu-id="39176-107">Ved at angive en anden valuta som en såkaldt ekstra rapporteringsvaluta vil [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk registrere beløb i både RV og i den ekstra rapporteringsvaluta i hver enkelt finanspost og i andre poster, f.eks. momsposter.</span><span class="sxs-lookup"><span data-stu-id="39176-107">By designating a second currency as a so-called additional reporting currency, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically record amounts in both LCY and this additional reporting currency on each G/L entry and other entries, such as VAT entries.</span></span> <span data-ttu-id="39176-108">Du kan finde flere oplysninger i [Oprette en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md).</span><span class="sxs-lookup"><span data-stu-id="39176-108">For more information, see [Set Up an Additional Reporting Currency](finance-how-setup-additional-currencies.md).</span></span>

## <a name="adjusting-exchange-rates"></a><span data-ttu-id="39176-109">Regulering af valutakurser</span><span class="sxs-lookup"><span data-stu-id="39176-109">Adjusting Exchange Rates</span></span>
<span data-ttu-id="39176-110">Fordi valutakurser svinger hele tiden, skal ekstra valutaer i systemet reguleres med jævne mellemrum.</span><span class="sxs-lookup"><span data-stu-id="39176-110">Because exchange rates fluctuate constantly, additional currency equivalents in your system must be adjusted periodically.</span></span> <span data-ttu-id="39176-111">Hvis der ikke foretages reguleringer, kan de beløb, der er konverterede fra udenlandske (eller ekstra) valutaer, og som er bogførte i regnskabet i RV være vildledende.</span><span class="sxs-lookup"><span data-stu-id="39176-111">If these adjustments are not done, amounts that have been converted from foreign (or additional) currencies and posted to the general ledger in LCY may be misleading.</span></span> <span data-ttu-id="39176-112">Derudover skal daglige poster, der er bogført før, en daglig valutakurs angives i programmet, opdateres, efter at de daglige oplysninger om valutakurser angives.</span><span class="sxs-lookup"><span data-stu-id="39176-112">In addition, daily entries posted before a daily exchange rate is entered into the program must be updated after the daily exchange rate information is entered.</span></span> <span data-ttu-id="39176-113">Kørslen Juster valutakurser bruges til at regulere valutakursen for bogførte kunde-, leverandør- og bankkontoposter.</span><span class="sxs-lookup"><span data-stu-id="39176-113">The Adjust Exchange Rates batch job is used to adjust the exchange rates of posted customer, vendor and bank account entries.</span></span> <span data-ttu-id="39176-114">Det kan også opdatere ekstra rapporteringsvalutabeløb i finansposter.</span><span class="sxs-lookup"><span data-stu-id="39176-114">It can also update additional reporting currency amounts on G/L entries.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="39176-115">Sådan konfigureres en valutakurstjeneste</span><span class="sxs-lookup"><span data-stu-id="39176-115">To set up a currency exchange rate service</span></span>
<span data-ttu-id="39176-116">Du kan bruge en ekstern tjeneste til at holde dine valutakurser opdateret, f.eks. FloatRates.</span><span class="sxs-lookup"><span data-stu-id="39176-116">You can use an external service to keep your currency exchange rates up to date, such as FloatRates.</span></span>

1. <span data-ttu-id="39176-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Valutakurstjenester**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="39176-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="39176-118">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="39176-118">Choose the **New** action.</span></span>
3. <span data-ttu-id="39176-119">På siden **Valutakurstjenester** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="39176-119">On the **Currency Exchange Rate Service** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="39176-120">Marker afkrydsningsfeltet **Aktiveret** for at aktivere tjenesten.</span><span class="sxs-lookup"><span data-stu-id="39176-120">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="39176-121">Sådan opdateres valutakurser fra en tjeneste</span><span class="sxs-lookup"><span data-stu-id="39176-121">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="39176-122">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Valutaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="39176-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="39176-123">Vælg handlingen **Opdater valutakurser**.</span><span class="sxs-lookup"><span data-stu-id="39176-123">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="39176-124">Værdien i feltet **Valutakurs** på siden **Valutaer** opdateres med den seneste valutakurs.</span><span class="sxs-lookup"><span data-stu-id="39176-124">The value in the **Exchange Rate** field on the **Currencies** page is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="39176-125">Se også</span><span class="sxs-lookup"><span data-stu-id="39176-125">See Also</span></span>
[<span data-ttu-id="39176-126">Oprette en ekstra rapporteringsvaluta</span><span class="sxs-lookup"><span data-stu-id="39176-126">Set Up an Additional Reporting Currency</span></span>](finance-how-setup-additional-currencies.md)  
[<span data-ttu-id="39176-127">Afslutning af år og perioder</span><span class="sxs-lookup"><span data-stu-id="39176-127">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="39176-128">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="39176-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

