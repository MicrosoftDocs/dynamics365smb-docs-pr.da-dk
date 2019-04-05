---
title: Sådan konfigureres et diagram over omkostningstyper | Microsoft Docs
description: Diagrammet over omkostningstyper ligner kontoplanen i regnskabet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 2846967648f5c0e0b6015c7990a941642fc27323
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "793261"
---
# <a name="set-up-cost-types"></a><span data-ttu-id="da557-103">Oprette omkostningstyper</span><span class="sxs-lookup"><span data-stu-id="da557-103">Set Up Cost Types</span></span>
<span data-ttu-id="da557-104">Diagrammet over omkostningstyper ligner kontoplanen i finansregnskabet.</span><span class="sxs-lookup"><span data-stu-id="da557-104">The chart of cost types is similar to the chart of accounts in the general ledger.</span></span> <span data-ttu-id="da557-105">Du kan angive diagrammet over omkostningstyper på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="da557-105">You can set up the chart of cost types in the following ways:</span></span>  

-   <span data-ttu-id="da557-106">Strukturen af diagrammet over omkostningstyper ligner resultatopgørelseskontiene i finanskontoplanen.</span><span class="sxs-lookup"><span data-stu-id="da557-106">Structure the chart of cost types similar to the income statement accounts in the general ledger chart of accounts.</span></span> <span data-ttu-id="da557-107">Herefter kan du overføre finanskontoplanen til diagrammet over omkostningstyper.</span><span class="sxs-lookup"><span data-stu-id="da557-107">Then, you can transfer the general ledger chart of accounts to the chart of cost types.</span></span> <span data-ttu-id="da557-108">Du kan foretage de nødvendige justeringer efter overførslen.</span><span class="sxs-lookup"><span data-stu-id="da557-108">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="da557-109">Opret et nyt diagram over omkostningstyper, eller tilføj nye omkostningstyper til det eksisterende diagram over omkostningstyper.</span><span class="sxs-lookup"><span data-stu-id="da557-109">Create new chart of cost types or add new cost types to existing chart of cost types.</span></span> <span data-ttu-id="da557-110">Du skal oprette hver ny omkostningstype individuelt.</span><span class="sxs-lookup"><span data-stu-id="da557-110">You must create each new cost type individually.</span></span>  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a><span data-ttu-id="da557-111">Sådan overføres finanskontoplanen til diagrammet over omkostningstyper</span><span class="sxs-lookup"><span data-stu-id="da557-111">To transfer the general ledger chart of accounts to the chart of cost types</span></span>  
1.  <span data-ttu-id="da557-112">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningstyper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="da557-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="da557-113">Vælg handlingen **Hent omkostningstyper fra kontoplan**.</span><span class="sxs-lookup"><span data-stu-id="da557-113">Choose the **Get Cost Types from Chart of Accounts** action.</span></span> <span data-ttu-id="da557-114">I dialogboksen skal du trykke på knappen **Ja** for at bekræfte overførslen.</span><span class="sxs-lookup"><span data-stu-id="da557-114">In the dialog box, choose the **Yes** button to confirm the transfer.</span></span> <span data-ttu-id="da557-115">Funktionen bruger kontoplanen til at oprette et diagram over omkostningstyper</span><span class="sxs-lookup"><span data-stu-id="da557-115">The function uses the chart of accounts to create a chart of cost types.</span></span>  

    <span data-ttu-id="da557-116">Diagrammet over omkostningstyper indeholder nu alle resultatopgørelseskonti i regnskabet og omfatter overskrifter og subtotaler.</span><span class="sxs-lookup"><span data-stu-id="da557-116">The chart of cost types now contain all income statement accounts in the general ledger and include headings and subtotals.</span></span> <span data-ttu-id="da557-117">Du kan ændre diagrammet over omkostningstyper, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="da557-117">You can change the chart of cost types, as necessary.</span></span> <span data-ttu-id="da557-118">For eksempel kan du slette dobbelte omkostningstyper.</span><span class="sxs-lookup"><span data-stu-id="da557-118">For example, you can delete duplicate existing cost types.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="da557-119">Funktionen **Registrer omkostningstyper i kontoplanen** opdaterer forholdet mellem kontoplanen og diagrammet over omkostningstyper.</span><span class="sxs-lookup"><span data-stu-id="da557-119">The **Register Cost Types in Chart of Accounts** function updates the relationship between the chart of accounts and the chart of cost types.</span></span> <span data-ttu-id="da557-120">Feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="da557-120">The **No.**</span></span> <span data-ttu-id="da557-121">feltet udfyldes og bekræftes for at sikre, at hver finanskonto kun er relateret til én kostpristype.</span><span class="sxs-lookup"><span data-stu-id="da557-121">field is filled and verified to make sure that each general ledger account is related to only one cost type.</span></span> <span data-ttu-id="da557-122">Funktionen kører automatisk, før den overfører finansposter til omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="da557-122">The function runs automatically before transferring general ledger entries to cost accounting.</span></span>  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a><span data-ttu-id="da557-123">Sådan oprettes nye omkostningstyper på siden Omkostningstyper</span><span class="sxs-lookup"><span data-stu-id="da557-123">To set up new cost types in the Chart of Cost Types page</span></span>  
1.  <span data-ttu-id="da557-124">Åbn siden **Omkostningstyper** i redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="da557-124">Open the **Chart of Cost Types** page in edit mode.</span></span>  
2.  <span data-ttu-id="da557-125">Udfyld felterne som beskrevet efter behov.</span><span class="sxs-lookup"><span data-stu-id="da557-125">Fill in the fields as described as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  <span data-ttu-id="da557-126">Du kan oprette og vedligeholde omkostningstyper enten på siden **Omkostningstypekort** eller på siden **Omkostningstyper**.</span><span class="sxs-lookup"><span data-stu-id="da557-126">You can set up and maintain cost types in either the **Cost Type Card** page or on the **Chart of Cost Types** page.</span></span> <span data-ttu-id="da557-127">I denne procedure opretter du omkostningstyper på siden **Omkostningstyper**.</span><span class="sxs-lookup"><span data-stu-id="da557-127">In this procedure, you set up cost types on the **Chart of Cost Types** page.</span></span>

3.  <span data-ttu-id="da557-128">Når du har oprettet alle omkostningstyper, skal du vælge handlingen **Indryk omkostningstyper**.</span><span class="sxs-lookup"><span data-stu-id="da557-128">After you have created all cost types, choose the **Indent Cost Types** action.</span></span> <span data-ttu-id="da557-129">I dialogboksen skal du trykke på knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="da557-129">In the dialog box, choose the **Yes** button.</span></span>  
4.  <span data-ttu-id="da557-130">Sammenkæd den nye pristype til den tilsvarende finanskonto.</span><span class="sxs-lookup"><span data-stu-id="da557-130">Link the new cost type to the corresponding general ledger account.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="da557-131">Hvis du har angivet definitioner i felterne **Sammentælling** for linjetypen **Til-sum**, før du kører funktionen **Indryk omkostningstyper**, skal du angive definitionerne igen, fordi funktionen overskriver værdierne i alle felter af typen **Til-sum**.</span><span class="sxs-lookup"><span data-stu-id="da557-131">If you have entered definitions in the **Totaling** fields for the line type of **End-Total** before you run the **Indent Cost Types** function, then you must enter the definitions again because the function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="to-update-cost-types"></a><span data-ttu-id="da557-132">Sådan opdateres omkostningstyper</span><span class="sxs-lookup"><span data-stu-id="da557-132">To update cost types</span></span>  
1.  <span data-ttu-id="da557-133">På siden **Konfiguration af omkostningsregnskab** skal du vælge, om du ønsker, at omkostningstypeplanen automatisk opdateres, når kontoplanen ændres.</span><span class="sxs-lookup"><span data-stu-id="da557-133">On the **Cost Accounting Setup** page, select if you want the chart of cost types to be automatically updated when the chart of accounts is changed.</span></span>  
2.  <span data-ttu-id="da557-134">Du kan vælge mellem følgende indstillinger i feltet **Opdater finanskonto**.</span><span class="sxs-lookup"><span data-stu-id="da557-134">In the **Align G/L Account** field, you can choose from the following options.</span></span>  

- <span data-ttu-id="da557-135">**Ingen justering** der er ingen tilsvarende ændring i diagrammet over omkostningstyper, når du ændrer kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="da557-135">**No Alignment** - There is no corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="da557-136">**Automatisk** - en tilsvarende ændring foretages i diagrammet over omkostningstyper, når du ændrer kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="da557-136">**Automatic** - A corresponding change is made in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="da557-137">**Spørg** - der vises en meddelelse, hvor du bliver spurgt, om du vil foretage en tilsvarende ændring i diagrammet typer omkostninger, når du ændrer kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="da557-137">**Prompt** - A message is displayed asking if you want to make a corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="da557-138">Se også</span><span class="sxs-lookup"><span data-stu-id="da557-138">See Also</span></span>  
[<span data-ttu-id="da557-139">Regnskab for omkostninger</span><span class="sxs-lookup"><span data-stu-id="da557-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="da557-140">[Definition af omkostningssteder og omkostningsobjekter for kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="da557-140">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="da557-141">[Saldi mellem omkostningstype, omkostningssted og omkostningsobjekt](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="da557-141">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="da557-142">[Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="da557-142">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="da557-143">[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="da557-143">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="da557-144">Om omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="da557-144">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="da557-145">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="da557-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
