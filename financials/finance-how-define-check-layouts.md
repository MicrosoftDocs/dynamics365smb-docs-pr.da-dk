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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a2db2860846cd9b8010222faf580f0c9889e39a4
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-define-check-layouts"></a><span data-ttu-id="ae60c-103">Fremgangsmåde: Definere checklayout</span><span class="sxs-lookup"><span data-stu-id="ae60c-103">How to: Define Check Layouts</span></span>
<span data-ttu-id="ae60c-104">Du kan udforme dine checks i overensstemmelse med de lokale myndigheders standarder.</span><span class="sxs-lookup"><span data-stu-id="ae60c-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="ae60c-105">Checkbilleder kan udskrives på engelsk, fransk eller spansk.</span><span class="sxs-lookup"><span data-stu-id="ae60c-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="ae60c-106">Checks er designet til udskrivning i amerikanske og canadiske checkbilledformater i et checkfølgebrevformat eller et følgebrev-følgebrevcheckformat.</span><span class="sxs-lookup"><span data-stu-id="ae60c-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="ae60c-107">Sådan defineres checklayout</span><span class="sxs-lookup"><span data-stu-id="ae60c-107">To define check layouts</span></span>
1. <span data-ttu-id="ae60c-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Rapportvalg - Bankkonto**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ae60c-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae60c-109">I vinduet **Rapportvalg - bankkonto**</span><span class="sxs-lookup"><span data-stu-id="ae60c-109">In the **Report Selection - Bank Acc.**</span></span> <span data-ttu-id="ae60c-110">skal du i feltet **Forbrug** vælge **Check**.</span><span class="sxs-lookup"><span data-stu-id="ae60c-110">window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="ae60c-111">Vælg et af følgende rapport-id'er.</span><span class="sxs-lookup"><span data-stu-id="ae60c-111">Select one of the following report IDs.</span></span>

| <span data-ttu-id="ae60c-112">Rapport-id</span><span class="sxs-lookup"><span data-stu-id="ae60c-112">Report ID</span></span> | <span data-ttu-id="ae60c-113">Rapportnavn</span><span class="sxs-lookup"><span data-stu-id="ae60c-113">Report Name</span></span> | <span data-ttu-id="ae60c-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ae60c-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ae60c-115">1401</span><span class="sxs-lookup"><span data-stu-id="ae60c-115">1401</span></span> |<span data-ttu-id="ae60c-116">Check</span><span class="sxs-lookup"><span data-stu-id="ae60c-116">Check</span></span> |<span data-ttu-id="ae60c-117">Dette er standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="ae60c-117">This is the default report.</span></span> |
| <span data-ttu-id="ae60c-118">10401</span><span class="sxs-lookup"><span data-stu-id="ae60c-118">10401</span></span> |<span data-ttu-id="ae60c-119">Check (følgebrev/følgebrev/check)</span><span class="sxs-lookup"><span data-stu-id="ae60c-119">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="ae60c-120">Denne rapport er designet til at udskrive check i et følgebrev/følgebrev/check-format.</span><span class="sxs-lookup"><span data-stu-id="ae60c-120">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="ae60c-121">10411</span><span class="sxs-lookup"><span data-stu-id="ae60c-121">10411</span></span> |<span data-ttu-id="ae60c-122">Check (følgebrev/check/følgebrev)</span><span class="sxs-lookup"><span data-stu-id="ae60c-122">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="ae60c-123">Denne rapport er designet til at udskrive check i et check/følgebrev/check-format.</span><span class="sxs-lookup"><span data-stu-id="ae60c-123">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="ae60c-124">Når du har oprettet checklayout, kan du udskrive check i vinduet **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="ae60c-124">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="ae60c-125">Du kan finde flere oplysninger i [Fremgangsmåde: Arbejde med checks](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="ae60c-125">For more information, see [How to: Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ae60c-126">Se også</span><span class="sxs-lookup"><span data-stu-id="ae60c-126">See Also</span></span>
[<span data-ttu-id="ae60c-127">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="ae60c-127">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="ae60c-128">[Håndtere bankkonti](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="ae60c-128">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="ae60c-129">Fuldførelse af periodeafslutningsprocesser</span><span class="sxs-lookup"><span data-stu-id="ae60c-129">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="ae60c-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ae60c-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ae60c-131">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="ae60c-131">General Business Functionality</span></span>](ui-across-business-areas.md)

