---
title: GIFI-koder i Canada | Microsoft Docs
Description: "I Canada kan du oprette GIFI-koder (General Index of Financial Information) og knytte dem til bogføringskonti"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-gifi-codes-in-canada"></a><span data-ttu-id="0d2cc-103">Fremgangsmåde: Arbejde med GIFI-koder i Canada</span><span class="sxs-lookup"><span data-stu-id="0d2cc-103">How to: Work With GIFI Codes in Canada</span></span>
<span data-ttu-id="0d2cc-104">Finansielle oplysninger kan omfatte finanskonti, rapporter, resultatopgørelsen, balancen og opgørelse af overført resultat.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-104">Fiscal information can include general ledger accounts, reports, income statements, balance sheets, and statements of retained earnings.</span></span> <span data-ttu-id="0d2cc-105">Finansielle oplysninger klassificeres ved hjælp af koder.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-105">Fiscal information is classified using codes.</span></span> <span data-ttu-id="0d2cc-106">Brug af koder hjælper myndighederne med at behandle oplysninger, forberede elektronisk arkivering og validere skatteoplysningerne elektronisk.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-106">The use of codes helps the government to process information, prepare for electronic filing, and validate tax information electronically.</span></span> <span data-ttu-id="0d2cc-107">Brug af koder kan også hjælpe statistiske organisationer til at arbejde mere effektivt, fordi finansielle oplysninger er mere tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-107">The use of codes also helps statistical organizations to work more efficiently, as financial information is more readily available.</span></span> <span data-ttu-id="0d2cc-108">Du kan finde flere oplysninger under [Webstedet Canada Revenue Agency](http://www.cra-arc.gc.ca/).</span><span class="sxs-lookup"><span data-stu-id="0d2cc-108">For more information, see the [Canada Revenue Agency website](http://www.cra-arc.gc.ca/).</span></span>

<span data-ttu-id="0d2cc-109">Canada Revenue Agency bruger GIFI-koder (General Index of Financial Information) til at indsamle, validere og behandle finansielle data og momsoplysninger elektronisk.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-109">The Canada Revenue Agency uses General Index of Financial Information (GIFI) codes to collect, validate, and process financial and tax information electronically.</span></span> <span data-ttu-id="0d2cc-110">Det er bedst kun at tildele GIFI-koder til bogføringskonti, så alle sammentællinger udføres af dit skattebehandlingsprogram.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-110">It is a best practice to assign GIFI codes only to posting accounts, so that all totaling is done by your tax preparation software.</span></span>

<span data-ttu-id="0d2cc-111">Hvis en konto er knyttet til en GIFI-kode, rapporteres det til skattemyndighederne under denne kode.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-111">When an account is associated with a GIFI code, it is reported to the revenue agency under that code.</span></span> <span data-ttu-id="0d2cc-112">Flere konti kan have den samme GIFI-kode, men hver konto kan kun have én GIFI-kode.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-112">Multiple accounts can all have the same GIFI code, but each account can have only one GIFI code.</span></span>

<span data-ttu-id="0d2cc-113">Du kan eksportere saldooplysninger ved hjælp af GIFI-kode og gemme den eksporterede fil i Excel, som med fordel kan bruges til at overføre oplysninger til dit skattebehandlingsprogram.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-113">You can export balance information by GIFI code and save the exported file in Excel, which is useful for transferring information to your tax preparation software.</span></span>

## <a name="to-set-up-gifi-codes"></a><span data-ttu-id="0d2cc-114">Sådan defineres GIFI-koder</span><span class="sxs-lookup"><span data-stu-id="0d2cc-114">To set up GIFI codes</span></span>
<span data-ttu-id="0d2cc-115">I Dynamics NAV skal du angive GIFI-koder for finanskonti, rapporter, balancer, indtægtsopgørelser og opgørelser over overførte resultater.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-115">In Dynamics NAV, you must set up GIFI codes for general ledger accounts, reports, balance sheets, income sheets, and statements of retained earnings.</span></span>

1. <span data-ttu-id="0d2cc-116">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **GIFI-koder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **GIFI Codes**, and then choose the related link.</span></span>
2. <span data-ttu-id="0d2cc-117">I vinduet **GIFI-koder** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-117">In the **GIFI Codes** window, choose the **New** action.</span></span>
3. <span data-ttu-id="0d2cc-118">Opret GIFI-koder ved at udfylde felterne.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-118">Set up GIFI codes by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a><span data-ttu-id="0d2cc-119">Sådan knyttes GIFI-koder til finanskonti</span><span class="sxs-lookup"><span data-stu-id="0d2cc-119">To associate GIFI codes with G/L accounts</span></span>
<span data-ttu-id="0d2cc-120">Hvis du vil rapportere finansielle oplysninger via GIFI-kode, skal hver GIFI-kode være knyttet til de relevante konti i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-120">To report financial information by GIFI code, each GIFI code must be associated with the appropriate accounts in the chart of accounts.</span></span>

1. <span data-ttu-id="0d2cc-121">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="0d2cc-122">Vælg en relevant finanskonto, og vælg derefter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-122">Select a relevant general ledger account, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="0d2cc-123">I oversigtspanelet **Omkostningsregnskab** skal du i feltet **GIFI-kode** vælge den relevante GIFI-kode.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-123">On the **Cost Accounting** FastTab, in the **GIFI Code** field, select an appropriate GIFI code.</span></span>

## <a name="to-view-account-balances-using-the-gifi-code-report"></a><span data-ttu-id="0d2cc-124">Sådan vises kontosaldi ved hjælp af GIFI-koderapporten</span><span class="sxs-lookup"><span data-stu-id="0d2cc-124">To view account balances using the GIFI code report</span></span>
<span data-ttu-id="0d2cc-125">Du kan gennemse dine kontosaldi via GIFI-kode ved hjælp af rapporten **Kontosaldi efter GIFI-kode**.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-125">You can review your account balances by GIFI code by using the **Account Balances by GIFI Code** report.</span></span>

1. <span data-ttu-id="0d2cc-126">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **GIFI-koder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Balances by GIFI Code**, and then choose the related link.</span></span>
2. <span data-ttu-id="0d2cc-127">Angiv, hvad der skal medtages i rapporten, ved at udfylde felterne.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-127">Specify what to include in the report by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="0d2cc-128">Vælg **Udskriv** eller **Vis udskrift**.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-128">Choose the **Print** or the **Preview** button.</span></span>

## <a name="to-export-balance-information-using-gifi-codes"></a><span data-ttu-id="0d2cc-129">Sådan udlæses saldooplysninger med GIFI-koder</span><span class="sxs-lookup"><span data-stu-id="0d2cc-129">To export balance information using GIFI codes</span></span>
<span data-ttu-id="0d2cc-130">Du kan eksportere saldooplysninger ved hjælp af GIFI-koder og gemme den eksporterede fil i Excel.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-130">You can export balance information using GIFI codes and save the exported file in Excel.</span></span> <span data-ttu-id="0d2cc-131">Du kan ændre, gemme eller slette filen.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-131">You can modify, save, or delete the file.</span></span> <span data-ttu-id="0d2cc-132">Filen kan bruge filen til at overføre oplysninger til dit skattebehandlingsprogram.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-132">You can use the file to transfer information to your tax preparation software.</span></span>

1. <span data-ttu-id="0d2cc-133">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **GIFI-koder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Export GIFI Info. to Excel**, and then choose the related link.</span></span>
2. <span data-ttu-id="0d2cc-134">Angiv, hvad der skal udlæses til Excel, ved at udfylde felterne.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-134">Specify what to export to Excel by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="0d2cc-135">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-135">Choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0d2cc-136">Excel-filen har følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="0d2cc-136">The Excel file has the following characteristics:</span></span>

* <span data-ttu-id="0d2cc-137">Saldoen afrundes til nærmeste procent, men celleværdien vedligeholder samme procentsats som i finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-137">The balance is rounded to the nearest percentage, but the cell value maintains the same percentage as it does in the general ledger.</span></span>
* <span data-ttu-id="0d2cc-138">Negative tal vises som positive tal i parentes.</span><span class="sxs-lookup"><span data-stu-id="0d2cc-138">Negative numbers are represented as positive number in brackets.</span></span> <span data-ttu-id="0d2cc-139">Derfor repræsenteres -123 som (123).</span><span class="sxs-lookup"><span data-stu-id="0d2cc-139">Accordingly, -123 is represented as (123).</span></span>

## <a name="see-also"></a><span data-ttu-id="0d2cc-140">Se også</span><span class="sxs-lookup"><span data-stu-id="0d2cc-140">See Also</span></span>
<span data-ttu-id="0d2cc-141">[Finans](finance.md) </span><span class="sxs-lookup"><span data-stu-id="0d2cc-141">[Finance](finance.md) </span></span>  
[<span data-ttu-id="0d2cc-142">Konfigurere Finans</span><span class="sxs-lookup"><span data-stu-id="0d2cc-142">Setting Up Finance</span></span>](finance-setup-finance.md)

