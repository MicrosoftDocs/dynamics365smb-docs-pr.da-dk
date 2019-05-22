---
title: Angive layoutet for en check | Microsoft Docs
description: Du kan designe og udskrive checks i forskellige formater i overensstemmelse med standarderne.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/24/2019
ms.author: edupont
ms.openlocfilehash: f2b7fa01cff36e3aab335f7d5921954343c69b74
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243591"
---
# <a name="define-check-layouts"></a><span data-ttu-id="7443a-103">Definere checklayout</span><span class="sxs-lookup"><span data-stu-id="7443a-103">Define Check Layouts</span></span>
<span data-ttu-id="7443a-104">Du kan udforme dine checks i overensstemmelse med de lokale myndigheders standarder.</span><span class="sxs-lookup"><span data-stu-id="7443a-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="7443a-105">Checkbilleder kan udskrives på engelsk, fransk eller spansk.</span><span class="sxs-lookup"><span data-stu-id="7443a-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="7443a-106">Checks er designet til udskrivning i amerikanske og canadiske checkbilledformater i et checkfølgebrevformat eller et følgebrev-følgebrevcheckformat.</span><span class="sxs-lookup"><span data-stu-id="7443a-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="7443a-107">Sådan defineres checklayout</span><span class="sxs-lookup"><span data-stu-id="7443a-107">To define check layouts</span></span>
1. <span data-ttu-id="7443a-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rapportvalg - Bankkonto**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="7443a-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="7443a-109">På siden **Rapportvalg - bankkonto** skal du vælge feltet **Check** i feltet **Forbrug**.</span><span class="sxs-lookup"><span data-stu-id="7443a-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="7443a-110">Vælg et af følgende rapport-id'er.</span><span class="sxs-lookup"><span data-stu-id="7443a-110">Select one of the following report IDs.</span></span>

  | <span data-ttu-id="7443a-111">Rapport-id</span><span class="sxs-lookup"><span data-stu-id="7443a-111">Report ID</span></span> | <span data-ttu-id="7443a-112">Rapportnavn</span><span class="sxs-lookup"><span data-stu-id="7443a-112">Report Name</span></span> | <span data-ttu-id="7443a-113">Description</span><span class="sxs-lookup"><span data-stu-id="7443a-113">Description</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="7443a-114">1401</span><span class="sxs-lookup"><span data-stu-id="7443a-114">1401</span></span> |<span data-ttu-id="7443a-115">Check</span><span class="sxs-lookup"><span data-stu-id="7443a-115">Check</span></span> |<span data-ttu-id="7443a-116">Dette er standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="7443a-116">This is the default report.</span></span> |
  | <span data-ttu-id="7443a-117">10411</span><span class="sxs-lookup"><span data-stu-id="7443a-117">10411</span></span> |<span data-ttu-id="7443a-118">Check (følgebrev/følgebrev/check)</span><span class="sxs-lookup"><span data-stu-id="7443a-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="7443a-119">Denne rapport er designet til at udskrive check i et følgebrev/følgebrev/check-format.</span><span class="sxs-lookup"><span data-stu-id="7443a-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
  | <span data-ttu-id="7443a-120">10412</span><span class="sxs-lookup"><span data-stu-id="7443a-120">10412</span></span> |<span data-ttu-id="7443a-121">Check (følgebrev/check/følgebrev)</span><span class="sxs-lookup"><span data-stu-id="7443a-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="7443a-122">Denne rapport er designet til at udskrive check i et følgebrev/check/følgebrev-format.</span><span class="sxs-lookup"><span data-stu-id="7443a-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
  | <span data-ttu-id="7443a-123">10413</span><span class="sxs-lookup"><span data-stu-id="7443a-123">10413</span></span> |<span data-ttu-id="7443a-124">Tre checks pr. side</span><span class="sxs-lookup"><span data-stu-id="7443a-124">Three Checks per Page</span></span> |<span data-ttu-id="7443a-125">Denne rapport er udviklet til at udskrive tre checks på hver side.</span><span class="sxs-lookup"><span data-stu-id="7443a-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="7443a-126">Når du har oprettet checklayout, kan du udskrive check på siden **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="7443a-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="7443a-127">Du kan finde flere oplysninger i [Arbejde med checks](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="7443a-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7443a-128">Se også</span><span class="sxs-lookup"><span data-stu-id="7443a-128">See Also</span></span>
[<span data-ttu-id="7443a-129">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="7443a-129">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="7443a-130">[Håndtere bankkonti](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="7443a-130">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="7443a-131">Fuldførelse af periodeafslutningsprocesser</span><span class="sxs-lookup"><span data-stu-id="7443a-131">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="7443a-132">[Arbejde med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7443a-132">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="7443a-133">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="7443a-133">General Business Functionality</span></span>](ui-across-business-areas.md)
