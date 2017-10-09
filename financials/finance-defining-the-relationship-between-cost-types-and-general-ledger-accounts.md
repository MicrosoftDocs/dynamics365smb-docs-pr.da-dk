---
title: Definere forholdet mellem omkostningstyper og finanskonti | Microsoft Docs
description: "Få at vide, hvordan du definerer forholdet mellem omkostningstypen og finanskontoen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f30b8b56ae4afcff230a7934a6bcac4d205db
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a><span data-ttu-id="2d074-103">Definition af forholdet mellem omkostningstyper og finanskonti.</span><span class="sxs-lookup"><span data-stu-id="2d074-103">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>
<span data-ttu-id="2d074-104">Forholdet mellem pristype og finanskontoen oprettes i pristypen og finanskontoen.</span><span class="sxs-lookup"><span data-stu-id="2d074-104">The relationship between the cost type and the general ledger account is created in the cost type and in the general ledger account.</span></span>  

* <span data-ttu-id="2d074-105">Feltet **Finanskontointerval** i tabellen **Omkostningstype** fastlægger, hvilke finanskonti der hører til en pristype.</span><span class="sxs-lookup"><span data-stu-id="2d074-105">The **G/L Account Range** field in the **Cost Type** table establishes which general ledger accounts belong to a cost type.</span></span>  
* <span data-ttu-id="2d074-106">Feltet **Omkostningstypenr.**</span><span class="sxs-lookup"><span data-stu-id="2d074-106">The **Cost Type No.**</span></span> <span data-ttu-id="2d074-107">i kontoplanen fastlægger, hvilken pristype en finanskonto tilhører.</span><span class="sxs-lookup"><span data-stu-id="2d074-107">field in the chart of accounts establishes which cost type a general ledger account belongs to.</span></span>  

<span data-ttu-id="2d074-108">Disse to felter udfyldes automatisk, når du bruger funktionen **Få omkostningstyper fra kontoplanen**.</span><span class="sxs-lookup"><span data-stu-id="2d074-108">These two fields are filled automatically when you use the **Get Cost Types from Chart of Accounts** function.</span></span>  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a><span data-ttu-id="2d074-109">Forholdet mellem finanskonti og pristyper</span><span class="sxs-lookup"><span data-stu-id="2d074-109">Relationship Between General Ledger Accounts and Cost Types</span></span>  
<span data-ttu-id="2d074-110">Der er et n:1 forhold mellem finanskonti og pristyper.</span><span class="sxs-lookup"><span data-stu-id="2d074-110">There is an n:1 relationship between general ledger accounts and cost types.</span></span> <span data-ttu-id="2d074-111">Flere finanskonti kan tilhøre én pristype, men hver finanskonto tilhører kun én pristype.</span><span class="sxs-lookup"><span data-stu-id="2d074-111">Several general ledger accounts can belong to one cost type, but each general ledger account belongs to only one cost type.</span></span> <span data-ttu-id="2d074-112">Følgende tabel beskriver detaljerne om relationen.</span><span class="sxs-lookup"><span data-stu-id="2d074-112">The following table describes the details in the relationship.</span></span>  

|<span data-ttu-id="2d074-113">Relationer</span><span class="sxs-lookup"><span data-stu-id="2d074-113">Relationship</span></span>|<span data-ttu-id="2d074-114">**Finanskontointerval**</span><span class="sxs-lookup"><span data-stu-id="2d074-114">**G/L Account Range**</span></span>|<span data-ttu-id="2d074-115">**Omkostningstypenr.**</span><span class="sxs-lookup"><span data-stu-id="2d074-115">**Cost Type No.**</span></span>|  
|------------------|------------------------------------------------|-------------------------------------------|  
|<span data-ttu-id="2d074-116">En finanskonto for hver pristype</span><span class="sxs-lookup"><span data-stu-id="2d074-116">One general ledger account for each cost type</span></span>|<span data-ttu-id="2d074-117">Én finanskonto</span><span class="sxs-lookup"><span data-stu-id="2d074-117">One general ledger account</span></span>|<span data-ttu-id="2d074-118">En pristype</span><span class="sxs-lookup"><span data-stu-id="2d074-118">One cost type</span></span>|  
|<span data-ttu-id="2d074-119">Flere finanskonti for en pristype</span><span class="sxs-lookup"><span data-stu-id="2d074-119">Several general ledger accounts for one cost type</span></span>|<span data-ttu-id="2d074-120">Finanskontointerval, f.eks. 7110..7193, for finanskonto</span><span class="sxs-lookup"><span data-stu-id="2d074-120">General ledger account range, for example, 7110..7193 for each general ledger account</span></span>|<span data-ttu-id="2d074-121">For hver finanskonto i området er det kun én pristype</span><span class="sxs-lookup"><span data-stu-id="2d074-121">For each general ledger account in the range, there is only one cost type</span></span>|  
|<span data-ttu-id="2d074-122">Pristyper uden tilsvarende finanskonti</span><span class="sxs-lookup"><span data-stu-id="2d074-122">Cost types without corresponding general ledger accounts</span></span>|<Empty>||  
|<span data-ttu-id="2d074-123">Finanskonti, hvis poster ikke bliver overført</span><span class="sxs-lookup"><span data-stu-id="2d074-123">General ledger accounts whose entries will not be transferred</span></span>||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a><span data-ttu-id="2d074-124">Pristyper uden relation til finanskontoen</span><span class="sxs-lookup"><span data-stu-id="2d074-124">Cost Types Without a Relationship to the General Ledger</span></span>  
<span data-ttu-id="2d074-125">En pristype kan ikke have en relation til finanskonti, hvis en af følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="2d074-125">A cost type may not have a relationship to general ledger accounts if one of the following conditions is true:</span></span>  

* <span data-ttu-id="2d074-126">Konti til operationelt regnskab, f.eks, Beregn Renter og afskrivning, henter kun omkostninger fra operationelt regnskab.</span><span class="sxs-lookup"><span data-stu-id="2d074-126">Accounts for operational accounting, such as Calc. Interest and Depreciation, only take costs from the operational accounting.</span></span>  
* <span data-ttu-id="2d074-127">Hjælpeomkostningstyper, f.eks. 9901, 9902 og 9903 i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen, bruges som kredit- og debetkonti for tildelinger.</span><span class="sxs-lookup"><span data-stu-id="2d074-127">Helping cost types, such as cost types 9901, 9902, and 9903 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, are used as credit and debit accounts for allocations.</span></span>  
* <span data-ttu-id="2d074-128">Hjælpekontoen, 9920 i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen, indeholder faktiske periodiseringer, der viser forskellen mellem omkostningerne og udgifterne fra finansregnskabet.</span><span class="sxs-lookup"><span data-stu-id="2d074-128">The helping account, 9920 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, contains actual accruals that show the difference between costs and the expense from the general ledger.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2d074-129">Se også</span><span class="sxs-lookup"><span data-stu-id="2d074-129">See Also</span></span>  
[<span data-ttu-id="2d074-130">Regnskab for omkostninger</span><span class="sxs-lookup"><span data-stu-id="2d074-130">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="2d074-131">[Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="2d074-131">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
[<span data-ttu-id="2d074-132">Om omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="2d074-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="2d074-133">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2d074-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

