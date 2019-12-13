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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: d4818c9dfe96f7e890d84a16c717d4451f56497a
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808573"
---
# <a name="select-a-check-layout"></a><span data-ttu-id="c722d-103">Vælge et checklayout</span><span class="sxs-lookup"><span data-stu-id="c722d-103">Select a Check Layout</span></span>
<span data-ttu-id="c722d-104">Du kan udforme dine checks i overensstemmelse med de lokale myndigheders standarder.</span><span class="sxs-lookup"><span data-stu-id="c722d-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="c722d-105">Checkbilleder kan udskrives på engelsk, fransk eller spansk.</span><span class="sxs-lookup"><span data-stu-id="c722d-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="c722d-106">Checks er designet til udskrivning i amerikanske og canadiske checkbilledformater i et checkfølgebrevformat eller et følgebrev-følgebrevcheckformat.</span><span class="sxs-lookup"><span data-stu-id="c722d-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-select-a-check-layout"></a><span data-ttu-id="c722d-107">Sådan vælges et checklayout</span><span class="sxs-lookup"><span data-stu-id="c722d-107">To select a check layout</span></span>
1. <span data-ttu-id="c722d-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rapportvalg - Bankkonto**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c722d-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="c722d-109">På siden **Rapportvalg - bankkonto** skal du vælge feltet **Check** i feltet **Forbrug**.</span><span class="sxs-lookup"><span data-stu-id="c722d-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="c722d-110">Vælg et af følgende rapport-id'er.</span><span class="sxs-lookup"><span data-stu-id="c722d-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="c722d-111">Rapport-id</span><span class="sxs-lookup"><span data-stu-id="c722d-111">Report ID</span></span> | <span data-ttu-id="c722d-112">Rapportnavn</span><span class="sxs-lookup"><span data-stu-id="c722d-112">Report Name</span></span> | <span data-ttu-id="c722d-113">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c722d-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c722d-114">1401</span><span class="sxs-lookup"><span data-stu-id="c722d-114">1401</span></span> |<span data-ttu-id="c722d-115">Check</span><span class="sxs-lookup"><span data-stu-id="c722d-115">Check</span></span> |<span data-ttu-id="c722d-116">Dette er standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="c722d-116">This is the default report.</span></span> |
| <span data-ttu-id="c722d-117">10411</span><span class="sxs-lookup"><span data-stu-id="c722d-117">10411</span></span> |<span data-ttu-id="c722d-118">Check (følgebrev/følgebrev/check)</span><span class="sxs-lookup"><span data-stu-id="c722d-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="c722d-119">Denne rapport er designet til at udskrive check i et følgebrev/følgebrev/check-format.</span><span class="sxs-lookup"><span data-stu-id="c722d-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="c722d-120">10412</span><span class="sxs-lookup"><span data-stu-id="c722d-120">10412</span></span> |<span data-ttu-id="c722d-121">Check (følgebrev/check/følgebrev)</span><span class="sxs-lookup"><span data-stu-id="c722d-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="c722d-122">Denne rapport er designet til at udskrive check i et følgebrev/check/følgebrev-format.</span><span class="sxs-lookup"><span data-stu-id="c722d-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
| <span data-ttu-id="c722d-123">10413</span><span class="sxs-lookup"><span data-stu-id="c722d-123">10413</span></span> |<span data-ttu-id="c722d-124">Tre checks pr. side</span><span class="sxs-lookup"><span data-stu-id="c722d-124">Three Checks per Page</span></span> |<span data-ttu-id="c722d-125">Denne rapport er udviklet til at udskrive tre checks på hver side.</span><span class="sxs-lookup"><span data-stu-id="c722d-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="c722d-126">Når du har oprettet checklayout, kan du udskrive check på siden **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="c722d-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="c722d-127">Du kan finde flere oplysninger i [Arbejde med checks](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="c722d-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

<span data-ttu-id="c722d-128">Hvis du vil ændre et af disse standardchecklayout, skal du bruge enten Word eller RDLC-integration til at gøre det.</span><span class="sxs-lookup"><span data-stu-id="c722d-128">To change one of these default check layouts, use either the Word or the RDLC integration to do so.</span></span> <span data-ttu-id="c722d-129">Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="c722d-129">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c722d-130">Se også</span><span class="sxs-lookup"><span data-stu-id="c722d-130">See Also</span></span>
[<span data-ttu-id="c722d-131">Sådan opretter og ændrer du Brugerdefinerede rapportlayouts</span><span class="sxs-lookup"><span data-stu-id="c722d-131">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="c722d-132">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="c722d-132">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="c722d-133">[Håndtere bankkonti](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="c722d-133">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="c722d-134">Fuldførelse af periodeafslutningsprocesser</span><span class="sxs-lookup"><span data-stu-id="c722d-134">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="c722d-135">[Arbejde med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c722d-135">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c722d-136">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="c722d-136">General Business Functionality</span></span>](ui-across-business-areas.md)
