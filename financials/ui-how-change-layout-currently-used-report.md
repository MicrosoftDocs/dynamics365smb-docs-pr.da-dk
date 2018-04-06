---
title: "Ændre udseendet af en rapport ved at vælge et andet layout | Microsoft Docs"
description: "Du kan bruge forskellige layout til en rapport og skifte mellem layout for at ændre udseendet af en rapport."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0cf867dc453b01b074010ee47c7c4c6560195361
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="change-which-layout-is-currently-used-on-a-report"></a><span data-ttu-id="0b07d-103">Ændre, hvilket layout der aktuelt bruges i en rapport</span><span class="sxs-lookup"><span data-stu-id="0b07d-103">Change Which Layout is Currently Used on a Report</span></span>
<span data-ttu-id="0b07d-104">En rapport kan konfigureres med flere rapportlayout, som du kan skifte mellem efter behov.</span><span class="sxs-lookup"><span data-stu-id="0b07d-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="0b07d-105">Afhængig af de layout, der er tilgængelige for en rapport, kan du vælge at bruge et indbygget RDLC-rapportlayout, et indbygget Word-rapportlayout eller et brugerdefineret layout.</span><span class="sxs-lookup"><span data-stu-id="0b07d-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="0b07d-106">Find flere oplysninger om RDLC- og Word-rapportlayout, indbyggede og brugerdefinerede layout og mere under [Administration af rapportlayout](ui-manage-report-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="0b07d-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

## <a name="to-change-the-layout-that-is-used-on-a-report"></a><span data-ttu-id="0b07d-107">Sådan ændrer du layoutet, der bruges i en rapport</span><span class="sxs-lookup"><span data-stu-id="0b07d-107">To change the layout that is used on a report</span></span>
1. <span data-ttu-id="0b07d-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Valg af rapportlayout**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0b07d-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="0b07d-109">Vinduet **Valg af rapportlayout** viser en liste over alle de rapporter, der er tilgængelige for det firma, der er angivet i feltet Virksomhed øverst i vinduet.</span><span class="sxs-lookup"><span data-stu-id="0b07d-109">The **Report Layout Selection** window lists all the reports that are available for the company that is specified in the Company field at the top of the window.</span></span> <span data-ttu-id="0b07d-110">Feltet Valgt layout angiver det layout, der aktuelt bruges af rapporten.</span><span class="sxs-lookup"><span data-stu-id="0b07d-110">The Selected Layout field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="0b07d-111">Angiv feltet **Virksomhed** øverst i vinduet til det firma, der indeholder rapporten.</span><span class="sxs-lookup"><span data-stu-id="0b07d-111">Set the **Company** field at the top of the window to the company that includes the report.</span></span>
3. <span data-ttu-id="0b07d-112">Hvis du vil ændre layoutet for en rapport, skal du i rækken for rapporten på listen angive feltet **Valgt layout** til en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b07d-112">To change the layout that is used by a report, in the row for the report in the list, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="0b07d-113">RDLC (indbygget), bruger det indbyggede RDLC-rapportlayout i rapporten.</span><span class="sxs-lookup"><span data-stu-id="0b07d-113">RDLC (built-in), uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="0b07d-114">Word (indbygget), bruger det indbyggede Word-rapportlayout i rapporten.</span><span class="sxs-lookup"><span data-stu-id="0b07d-114">Word (built-in), uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="0b07d-115">Brugerdefineret, bruger et brugerdefineret layout i rapporten.</span><span class="sxs-lookup"><span data-stu-id="0b07d-115">Custom, uses a custom layout on the report.</span></span>  
     <span data-ttu-id="0b07d-116">Du kan se, hvilke brugerdefinerede layout der er tilgængelige for rapporten i faktaboksen Rapportlayoutdel.</span><span class="sxs-lookup"><span data-stu-id="0b07d-116">You can see which custom layouts are available for the report in the Report Layouts Part FactBox.</span></span> <span data-ttu-id="0b07d-117">Hvis der ikke er nogen brugerdefinerede layout for rapporten, skal du først oprette ét.</span><span class="sxs-lookup"><span data-stu-id="0b07d-117">If there are no custom layouts for the report, then you will have to create one first.</span></span> <span data-ttu-id="0b07d-118">Hvis du vælger denne indstilling, kan du gå til den næste procedure for at angive et brugerdefineret layout, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="0b07d-118">If you choose this option, go to the next procedure to specify the custom layout that you want to use.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="0b07d-119">Hvis du vælger **RDLC (indbygget)** eller **Word (indbygget)** , og du får en fejlmeddelelse om, at rapporten ikke har et layout med den angivne type, skal du vælge en anden layoutindstilling eller oprette en brugerdefineret rapport af den type, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="0b07d-119">If you choose **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span>

<span data-ttu-id="0b07d-120">Hvis du har valgt et indbygget RDLC- eller Word-rapportlayout, kræves ingen yderligere handling, og layoutet bruges, næste gang rapporten køres.</span><span class="sxs-lookup"><span data-stu-id="0b07d-120">If you selected a built-in RDLC or Word report layout, then no further action is required and the layout will be used the next time the report is run.</span></span>

## <a name="to-specify-a-custom-layout-on-a-report"></a><span data-ttu-id="0b07d-121">Sådan angiver du et brugerdefineret layout i en rapport</span><span class="sxs-lookup"><span data-stu-id="0b07d-121">To specify a custom layout on a report</span></span>
1. <span data-ttu-id="0b07d-122">Du kan angive, hvilket brugerdefinerede layout der skal bruges i rapporten, fra vinduet **Tilpassede rapportlayouts**.</span><span class="sxs-lookup"><span data-stu-id="0b07d-122">You specify which custom layout to use on the report from the **Custom Report Layouts** window.</span></span> <span data-ttu-id="0b07d-123">Hvis vinduet **Tilpassede rapportlayouts** ikke er åbent, skal du i feltet **Beskrivelse af rapportlayout** klikke på opslagsknappen.</span><span class="sxs-lookup"><span data-stu-id="0b07d-123">If the **Custom Report Layouts** window is not open, then in the **Report Layout Description** field, choose the lookup button.</span></span>
2. <span data-ttu-id="0b07d-124">Brug vinduet **Tilpassede rapportlayouts** til at vælge rækken med det brugerdefinerede layout, du vil bruge, og luk derefter vinduet.</span><span class="sxs-lookup"><span data-stu-id="0b07d-124">In the **Custom Report Layouts** window, select the row for custom layout that you want to use, and then close the window.</span></span>

<span data-ttu-id="0b07d-125">Du kommer tilbage til vinduet **Valg af rapportlayout**.</span><span class="sxs-lookup"><span data-stu-id="0b07d-125">You return to the **Report Layout Selection** window.</span></span> <span data-ttu-id="0b07d-126">Navnet på det valgte brugerdefinerede layout vises i feltet **Beskrivelse af brugerdefineret layout**.</span><span class="sxs-lookup"><span data-stu-id="0b07d-126">The name of the selected custom layout displays in the **Custom Layout Description** field.</span></span> <span data-ttu-id="0b07d-127">Det brugerdefinerede layout, der skal bruges, næste gang du kører rapporten.</span><span class="sxs-lookup"><span data-stu-id="0b07d-127">The custom layout will be used the next time that you run the report.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b07d-128">Se også</span><span class="sxs-lookup"><span data-stu-id="0b07d-128">See Also</span></span>
[<span data-ttu-id="0b07d-129">Administration af rapportlayout</span><span class="sxs-lookup"><span data-stu-id="0b07d-129">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="0b07d-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0b07d-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

