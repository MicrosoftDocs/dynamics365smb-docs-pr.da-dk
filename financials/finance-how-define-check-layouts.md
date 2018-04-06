---
title: Angive layoutet for en check | Microsoft Docs
description: Du kan designe og udskrive checks i forskellige formater i overensstemmelse med standarderne.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: dd745186e4518c2005e34e6b2cbbc8925fd8931e
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="define-check-layouts"></a><span data-ttu-id="084cd-103">Definere checklayout</span><span class="sxs-lookup"><span data-stu-id="084cd-103">Define Check Layouts</span></span>
<span data-ttu-id="084cd-104">Du kan udforme dine checks i overensstemmelse med de lokale myndigheders standarder.</span><span class="sxs-lookup"><span data-stu-id="084cd-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="084cd-105">Checkbilleder kan udskrives på engelsk, fransk eller spansk.</span><span class="sxs-lookup"><span data-stu-id="084cd-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="084cd-106">Checks er designet til udskrivning i amerikanske og canadiske checkbilledformater i et checkfølgebrevformat eller et følgebrev-følgebrevcheckformat.</span><span class="sxs-lookup"><span data-stu-id="084cd-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="084cd-107">Sådan defineres checklayout</span><span class="sxs-lookup"><span data-stu-id="084cd-107">To define check layouts</span></span>
1. <span data-ttu-id="084cd-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Rapportvalg - Bankkonto**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="084cd-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="084cd-109">I vinduet **Rapportvalg - bankkonto** skal du vælge feltet **Check** i feltet **Forbrug**.</span><span class="sxs-lookup"><span data-stu-id="084cd-109">In the **Report Selection - Bank Acc.** window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="084cd-110">Vælg et af følgende rapport-id'er.</span><span class="sxs-lookup"><span data-stu-id="084cd-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="084cd-111">Rapport-id</span><span class="sxs-lookup"><span data-stu-id="084cd-111">Report ID</span></span> | <span data-ttu-id="084cd-112">Rapportnavn</span><span class="sxs-lookup"><span data-stu-id="084cd-112">Report Name</span></span> | <span data-ttu-id="084cd-113">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="084cd-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="084cd-114">1401</span><span class="sxs-lookup"><span data-stu-id="084cd-114">1401</span></span> |<span data-ttu-id="084cd-115">Check</span><span class="sxs-lookup"><span data-stu-id="084cd-115">Check</span></span> |<span data-ttu-id="084cd-116">Dette er standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="084cd-116">This is the default report.</span></span> |
| <span data-ttu-id="084cd-117">10401</span><span class="sxs-lookup"><span data-stu-id="084cd-117">10401</span></span> |<span data-ttu-id="084cd-118">Check (følgebrev/følgebrev/check)</span><span class="sxs-lookup"><span data-stu-id="084cd-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="084cd-119">Denne rapport er designet til at udskrive check i et følgebrev/følgebrev/check-format.</span><span class="sxs-lookup"><span data-stu-id="084cd-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="084cd-120">10411</span><span class="sxs-lookup"><span data-stu-id="084cd-120">10411</span></span> |<span data-ttu-id="084cd-121">Check (følgebrev/check/følgebrev)</span><span class="sxs-lookup"><span data-stu-id="084cd-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="084cd-122">Denne rapport er designet til at udskrive check i et check/følgebrev/check-format.</span><span class="sxs-lookup"><span data-stu-id="084cd-122">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="084cd-123">Når du har oprettet checklayout, kan du udskrive check i vinduet **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="084cd-123">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="084cd-124">Du kan finde flere oplysninger i [Arbejde med checks](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="084cd-124">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="084cd-125">Se også</span><span class="sxs-lookup"><span data-stu-id="084cd-125">See Also</span></span>
[<span data-ttu-id="084cd-126">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="084cd-126">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="084cd-127">[Håndtere bankkonti](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="084cd-127">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="084cd-128">Fuldførelse af periodeafslutningsprocesser</span><span class="sxs-lookup"><span data-stu-id="084cd-128">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="084cd-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="084cd-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="084cd-130">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="084cd-130">General Business Functionality</span></span>](ui-across-business-areas.md)

