---
title: Angive layoutet for en check | Microsoft Docs
description: Du kan designe og udskrive checks i forskellige formater i overensstemmelse med standarderne.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: eace865bc70f56206d478f8e8d38fd217133925e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "935254"
---
# <a name="define-check-layouts"></a><span data-ttu-id="504e8-103">Definere checklayout</span><span class="sxs-lookup"><span data-stu-id="504e8-103">Define Check Layouts</span></span>
<span data-ttu-id="504e8-104">Du kan udforme dine checks i overensstemmelse med de lokale myndigheders standarder.</span><span class="sxs-lookup"><span data-stu-id="504e8-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="504e8-105">Checkbilleder kan udskrives på engelsk, fransk eller spansk.</span><span class="sxs-lookup"><span data-stu-id="504e8-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="504e8-106">Checks er designet til udskrivning i amerikanske og canadiske checkbilledformater i et checkfølgebrevformat eller et følgebrev-følgebrevcheckformat.</span><span class="sxs-lookup"><span data-stu-id="504e8-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="504e8-107">Sådan defineres checklayout</span><span class="sxs-lookup"><span data-stu-id="504e8-107">To define check layouts</span></span>
1. <span data-ttu-id="504e8-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rapportvalg - Bankkonto**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="504e8-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="504e8-109">På siden **Rapportvalg - bankkonto** skal du vælge feltet **Check** i feltet **Forbrug**.</span><span class="sxs-lookup"><span data-stu-id="504e8-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="504e8-110">Vælg et af følgende rapport-id'er.</span><span class="sxs-lookup"><span data-stu-id="504e8-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="504e8-111">Rapport-id</span><span class="sxs-lookup"><span data-stu-id="504e8-111">Report ID</span></span> | <span data-ttu-id="504e8-112">Rapportnavn</span><span class="sxs-lookup"><span data-stu-id="504e8-112">Report Name</span></span> | <span data-ttu-id="504e8-113">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="504e8-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="504e8-114">1401</span><span class="sxs-lookup"><span data-stu-id="504e8-114">1401</span></span> |<span data-ttu-id="504e8-115">Check</span><span class="sxs-lookup"><span data-stu-id="504e8-115">Check</span></span> |<span data-ttu-id="504e8-116">Dette er standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="504e8-116">This is the default report.</span></span> |
| <span data-ttu-id="504e8-117">10401</span><span class="sxs-lookup"><span data-stu-id="504e8-117">10401</span></span> |<span data-ttu-id="504e8-118">Check (følgebrev/følgebrev/check)</span><span class="sxs-lookup"><span data-stu-id="504e8-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="504e8-119">Denne rapport er designet til at udskrive check i et følgebrev/følgebrev/check-format.</span><span class="sxs-lookup"><span data-stu-id="504e8-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="504e8-120">10411</span><span class="sxs-lookup"><span data-stu-id="504e8-120">10411</span></span> |<span data-ttu-id="504e8-121">Check (følgebrev/check/følgebrev)</span><span class="sxs-lookup"><span data-stu-id="504e8-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="504e8-122">Denne rapport er designet til at udskrive check i et check/følgebrev/check-format.</span><span class="sxs-lookup"><span data-stu-id="504e8-122">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="504e8-123">Når du har oprettet checklayout, kan du udskrive check på siden **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="504e8-123">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="504e8-124">Du kan finde flere oplysninger i [Arbejde med checks](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="504e8-124">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="504e8-125">Se også</span><span class="sxs-lookup"><span data-stu-id="504e8-125">See Also</span></span>
[<span data-ttu-id="504e8-126">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="504e8-126">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="504e8-127">[Håndtere bankkonti](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="504e8-127">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="504e8-128">Fuldførelse af periodeafslutningsprocesser</span><span class="sxs-lookup"><span data-stu-id="504e8-128">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="504e8-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="504e8-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="504e8-130">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="504e8-130">General Business Functionality</span></span>](ui-across-business-areas.md)
