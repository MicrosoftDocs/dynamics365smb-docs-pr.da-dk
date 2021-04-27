---
title: Hjælpefunktioner
description: Tastaturgenveje og andre hjælpefunktioner.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c303c39850e22d3df375838d42703133428b4c7d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772350"
---
# <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="2eb77-103">Tilgængelighedsfunktioner og tastaturgenveje</span><span class="sxs-lookup"><span data-stu-id="2eb77-103">Accessibility and Keyboard Shortcuts</span></span>

<span data-ttu-id="2eb77-104">Dette emne indeholder oplysninger om de funktioner, der gør [!INCLUDE[prod_short](includes/prod_short.md)] direkte tilgængelig for personer med handicap.</span><span class="sxs-lookup"><span data-stu-id="2eb77-104">This topic provides information about the features that make [!INCLUDE[prod_short](includes/prod_short.md)] readily available to people with disabilities.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="2eb77-105">understøtter følgende funktioner i Hjælp til handicappede:</span><span class="sxs-lookup"><span data-stu-id="2eb77-105">supports the following accessibility features:</span></span>  

- <span data-ttu-id="2eb77-106">Tastaturgenveje</span><span class="sxs-lookup"><span data-stu-id="2eb77-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="2eb77-107">Du kan finde flere oplysninger i [Tastaturgenveje](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="2eb77-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

- <span data-ttu-id="2eb77-108">Navigation</span><span class="sxs-lookup"><span data-stu-id="2eb77-108">Navigation</span></span>  

- <span data-ttu-id="2eb77-109">Overskrifter</span><span class="sxs-lookup"><span data-stu-id="2eb77-109">Headings</span></span>  

- <span data-ttu-id="2eb77-110">Alternativ tekst til billeder og hyperlinks</span><span class="sxs-lookup"><span data-stu-id="2eb77-110">Alternative text for images and links</span></span>  

- <span data-ttu-id="2eb77-111">Understøttelse af almindelige hjælpeteknologier</span><span class="sxs-lookup"><span data-stu-id="2eb77-111">Support for common assistive technologies</span></span>  

- <span data-ttu-id="2eb77-112">Brug af genvejstaster til at zoome ind eller ud på en side</span><span class="sxs-lookup"><span data-stu-id="2eb77-112">Use keyboard shortcuts to zoom in or out on any page</span></span>

<!-- moved to separate article
##  <a name="Keyboard"></a> Keyboard Shortcuts in the browser
 [!INCLUDE[prod_short](includes/prod_short.md)] supports the keyboard shortcuts that are supported by most web browsers. The keyboard shortcuts described here refer to the U.S. keyboard layout. The layout of the keys on other keyboards may not correspond exactly to the keys on a U.S. keyboard.  

|To do this|Press|  
|----------------|-----------|  
|To move focus to the next or previous control or element on a page, such as buttons, fields, or items in a list.|Tab, Shift+Tab|  
|To enable or access the element or control that is in focus.|Enter|  
|To scroll items up and down in a list.|Up Arrow, Down Arrow|  
|To scroll columns of an item left and right in a list.|Left Arrow, Right Arrow|  
|To open a drop-down list or look up a value for a field.|Alt+Down Arrow|  
|To move focus to the next element outside the list.|Ctrl + Enter|  
|To see the transactions that resulted in a calculated value in a field.|Alt+Right Arrow|  

-->

## <a name="navigation"></a><a name="Navigation"></a> <span data-ttu-id="2eb77-113">Navigation</span><span class="sxs-lookup"><span data-stu-id="2eb77-113">Navigation</span></span>  
 <span data-ttu-id="2eb77-114">Du kan navigere mellem fanerne og handlingerne på båndet, elementerne i navigationslinjen og andre kontrolelementer på [!INCLUDE[prod_short](includes/prod_short.md)]-sider og -rapporter vha. tastaturet.</span><span class="sxs-lookup"><span data-stu-id="2eb77-114">You can navigate between the tabs and actions in the ribbon, elements in the navigation bar, and other controls on [!INCLUDE[prod_short](includes/prod_short.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="2eb77-115">Flytte fokus fra én fane, handling eller kontrolelement til en anden, skal du trykke på Tab for at flytte fremad.</span><span class="sxs-lookup"><span data-stu-id="2eb77-115">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="2eb77-116">Tryk på Skift+Tab for at gå tilbage.</span><span class="sxs-lookup"><span data-stu-id="2eb77-116">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="2eb77-117">Ved hjælp af fanerækkefølgen kan du også skifte mellem hovedbrowsersiden og dialogbokse, der anmoder om bekræftelse, for eksempel logonsiden.</span><span class="sxs-lookup"><span data-stu-id="2eb77-117">By using the tab order, you can also switch between the main browser page and dialog boxes that request confirmation, for example, or the login page.</span></span>  

## <a name="headings-in-content"></a><a name="Headings"></a> <span data-ttu-id="2eb77-118">Overskrifter i indhold</span><span class="sxs-lookup"><span data-stu-id="2eb77-118">Headings in Content</span></span>
 
 <span data-ttu-id="2eb77-119">HTML-kilden til [!INCLUDE[prod_short](includes/prod_short.md)]-indhold bruger koder til at hjælpe brugerne af hjælpeteknologien med at forstå strukturen og indholdet af siden.</span><span class="sxs-lookup"><span data-stu-id="2eb77-119">The HTML source for [!INCLUDE[prod_short](includes/prod_short.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="2eb77-120">På oversigtssider defineres kolonnerne f.eks. i TH-koder, og kolonneoverskrifterne oprettes med TITEL-attributten i koden.</span><span class="sxs-lookup"><span data-stu-id="2eb77-120">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="2eb77-121">Tekster til elementer som oversigtspaneler, faktabokse og felter er inkluderet i overskriftskoder (H1 H2, H3 og H4).</span><span class="sxs-lookup"><span data-stu-id="2eb77-121">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

## <a name="image-and-links"></a><a name="Images"></a> <span data-ttu-id="2eb77-122">Billede og links</span><span class="sxs-lookup"><span data-stu-id="2eb77-122">Image and Links</span></span>

 <span data-ttu-id="2eb77-123">En beskrivende tekst til billeder er angivet med attributten ALT i koden IMG.</span><span class="sxs-lookup"><span data-stu-id="2eb77-123">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="2eb77-124">En beskrivende tekst til hyperlinkser angivet med attributten titel i koden A.</span><span class="sxs-lookup"><span data-stu-id="2eb77-124">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a> <span data-ttu-id="2eb77-125">Hjælpeteknologier</span><span class="sxs-lookup"><span data-stu-id="2eb77-125">Assistive Technologies</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="2eb77-126">understøtter forskellige hjælpeteknologier, f.eks. stor kontrast, skærmlæsere og talegenkendelsessoftware.</span><span class="sxs-lookup"><span data-stu-id="2eb77-126">supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="2eb77-127">Nogle hjælpeteknologier fungerer ikke sammen med bestemte elementer på [!INCLUDE[prod_short](includes/prod_short.md)]-sider.</span><span class="sxs-lookup"><span data-stu-id="2eb77-127">Some assistive technologies may not work well with certain elements in [!INCLUDE[prod_short](includes/prod_short.md)] pages.</span></span>  

## <a name="zoom"></a><a name="zoom"></a> <span data-ttu-id="2eb77-128">Zoom</span><span class="sxs-lookup"><span data-stu-id="2eb77-128">Zoom</span></span>

<span data-ttu-id="2eb77-129">De fleste browsere bruger standardtastaturgenveje til at zoome ind og ud på den aktuelle side.</span><span class="sxs-lookup"><span data-stu-id="2eb77-129">Most browsers use standard keyboard shortcuts to zoom in and out on the current page.</span></span> <span data-ttu-id="2eb77-130">Disse tastaturgenveje er ikke specifikke for [!INCLUDE [prod_short](includes/prod_short.md)], men de fungerer, når du bruger [!INCLUDE [prod_short](includes/prod_short.md)] i en browser.</span><span class="sxs-lookup"><span data-stu-id="2eb77-130">These keyboard shortcuts are not specific to [!INCLUDE [prod_short](includes/prod_short.md)], but they work when you use [!INCLUDE [prod_short](includes/prod_short.md)] in a browser.</span></span> <span data-ttu-id="2eb77-131">Du kan få vist en liste over understøttede tastaturgenveje under [Tastaturgenveje til zoom ind og ud](keyboard-shortcuts.md#zoomshortcuts).</span><span class="sxs-lookup"><span data-stu-id="2eb77-131">For a list of supported keyboard shortcuts, see [Keyboard Shortcuts for Zooming In and Out](keyboard-shortcuts.md#zoomshortcuts).</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="2eb77-132">Flere oplysninger om tilgængelighedsfunktioner</span><span class="sxs-lookup"><span data-stu-id="2eb77-132">For more accessibility information</span></span>

<span data-ttu-id="2eb77-133">Du kan finde flere oplysninger om tilgængelighedsfunktioner i Microsoft-produkter og hjælpeteknologier på webstedet [Microsoft Hjælp til handicappede](https://go.microsoft.com/fwlink/?LinkId=262160).</span><span class="sxs-lookup"><span data-stu-id="2eb77-133">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="2eb77-134">Se også</span><span class="sxs-lookup"><span data-stu-id="2eb77-134">See Also</span></span>

[<span data-ttu-id="2eb77-135">Blive køreklar</span><span class="sxs-lookup"><span data-stu-id="2eb77-135">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="2eb77-136">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2eb77-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="2eb77-137">Ofte stillede spørgsmål</span><span class="sxs-lookup"><span data-stu-id="2eb77-137">Frequently Asked Questions</span></span>](across-faq.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]