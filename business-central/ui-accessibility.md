---
title: Hjælpefunktioner
description: Tastaturgenveje og andre hjælpefunktioner.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: cb898a459bdf5d0b4ced3baadd2a245cd23b8f38
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311448"
---
# <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="0fed3-103">Tilgængelighedsfunktioner og tastaturgenveje</span><span class="sxs-lookup"><span data-stu-id="0fed3-103">Accessibility and Keyboard Shortcuts</span></span>
<span data-ttu-id="0fed3-104">Dette emne indeholder oplysninger om de funktioner, der gør [!INCLUDE[d365fin](includes/d365fin_md.md)] direkte tilgængelig for personer med handicap.</span><span class="sxs-lookup"><span data-stu-id="0fed3-104">This topic provides information about the features that make [!INCLUDE[d365fin](includes/d365fin_md.md)] readily available to people with disabilities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="0fed3-105">understøtter følgende funktioner i Hjælp til handicappede:</span><span class="sxs-lookup"><span data-stu-id="0fed3-105">supports the following accessibility features:</span></span>  

-   <span data-ttu-id="0fed3-106">Tastaturgenveje</span><span class="sxs-lookup"><span data-stu-id="0fed3-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="0fed3-107">Du kan finde flere oplysninger i [Tastaturgenveje](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="0fed3-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

-   <span data-ttu-id="0fed3-108">Navigation</span><span class="sxs-lookup"><span data-stu-id="0fed3-108">Navigation</span></span>  

-   <span data-ttu-id="0fed3-109">Overskrifter</span><span class="sxs-lookup"><span data-stu-id="0fed3-109">Headings</span></span>  

-   <span data-ttu-id="0fed3-110">Alternativ tekst til billeder og hyperlinks</span><span class="sxs-lookup"><span data-stu-id="0fed3-110">Alternative text for images and links</span></span>  

-   <span data-ttu-id="0fed3-111">Understøttelse af almindelige hjælpeteknologier</span><span class="sxs-lookup"><span data-stu-id="0fed3-111">Support for common assistive technologies</span></span>  

<!-- moved to separate article
##  <a name="Keyboard"></a> Keyboard Shortcuts in the browser
 [!INCLUDE[d365fin](includes/d365fin_md.md)] supports the keyboard shortcuts that are supported by most web browsers. The keyboard shortcuts described here refer to the U.S. keyboard layout. The layout of the keys on other keyboards may not correspond exactly to the keys on a U.S. keyboard.  

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

##  <a name="Navigation"></a> <span data-ttu-id="0fed3-112">Navigation</span><span class="sxs-lookup"><span data-stu-id="0fed3-112">Navigation</span></span>  
 <span data-ttu-id="0fed3-113">Du kan navigere mellem fanerne og handlingerne på båndet, elementerne i navigationslinjen og andre kontrolelementer på [!INCLUDE[d365fin](includes/d365fin_md.md)]-sider og -rapporter vha. tastaturet.</span><span class="sxs-lookup"><span data-stu-id="0fed3-113">You can navigate between the tabs and actions in the ribbon, elements in the navigation bar, and other controls on [!INCLUDE[d365fin](includes/d365fin_md.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="0fed3-114">Flytte fokus fra én fane, handling eller kontrolelement til en anden, skal du trykke på Tab for at flytte fremad.</span><span class="sxs-lookup"><span data-stu-id="0fed3-114">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="0fed3-115">Tryk på Skift+Tab for at gå tilbage.</span><span class="sxs-lookup"><span data-stu-id="0fed3-115">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="0fed3-116">Ved hjælp af fanerækkefølgen kan du også skifte mellem hovedbrowsersiden og dialogbokse, der anmoder om bekræftelse, for eksempel logonsiden.</span><span class="sxs-lookup"><span data-stu-id="0fed3-116">By using the tab order, you can also switch between the main browser page and dialog boxes that request confirmation, for example, or the login page.</span></span>  

##  <a name="Headings"></a> <span data-ttu-id="0fed3-117">Overskrifter</span><span class="sxs-lookup"><span data-stu-id="0fed3-117">Headings</span></span>  
 <span data-ttu-id="0fed3-118">HTML-kilden til [!INCLUDE[d365fin](includes/d365fin_md.md)]-indhold bruger koder til at hjælpe brugerne af hjælpeteknologien med at forstå strukturen og indholdet af siden.</span><span class="sxs-lookup"><span data-stu-id="0fed3-118">The HTML source for [!INCLUDE[d365fin](includes/d365fin_md.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="0fed3-119">På oversigtssider defineres kolonnerne f.eks. i TH-koder, og kolonneoverskrifterne oprettes med TITEL-attributten i koden.</span><span class="sxs-lookup"><span data-stu-id="0fed3-119">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="0fed3-120">Tekster til elementer som oversigtspaneler, faktabokse og felter er inkluderet i overskriftskoder (H1 H2, H3 og H4).</span><span class="sxs-lookup"><span data-stu-id="0fed3-120">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

##  <a name="Images"></a> <span data-ttu-id="0fed3-121">Billede og links</span><span class="sxs-lookup"><span data-stu-id="0fed3-121">Image and Links</span></span>  
 <span data-ttu-id="0fed3-122">En beskrivende tekst til billeder er angivet med attributten ALT i koden IMG.</span><span class="sxs-lookup"><span data-stu-id="0fed3-122">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="0fed3-123">En beskrivende tekst til hyperlinkser angivet med attributten titel i koden A.</span><span class="sxs-lookup"><span data-stu-id="0fed3-123">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

##  <a name="AssistiveTech"></a> <span data-ttu-id="0fed3-124">Hjælpeteknologier</span><span class="sxs-lookup"><span data-stu-id="0fed3-124">Assistive Technologies</span></span>  
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="0fed3-125">understøtter forskellige hjælpeteknologier, f.eks. stor kontrast, skærmlæsere og talegenkendelsessoftware.</span><span class="sxs-lookup"><span data-stu-id="0fed3-125">supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="0fed3-126">Nogle hjælpeteknologier fungerer ikke sammen med bestemte elementer på [!INCLUDE[d365fin](includes/d365fin_md.md)]-sider.</span><span class="sxs-lookup"><span data-stu-id="0fed3-126">Some assistive technologies may not work well with certain elements in [!INCLUDE[d365fin](includes/d365fin_md.md)] pages.</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="0fed3-127">Flere oplysninger om tilgængelighedsfunktioner</span><span class="sxs-lookup"><span data-stu-id="0fed3-127">For more accessibility information</span></span>  
<span data-ttu-id="0fed3-128">Du kan finde flere oplysninger om tilgængelighedsfunktioner i Microsoft-produkter og hjælpeteknologier på webstedet [Microsoft Hjælp til handicappede](https://go.microsoft.com/fwlink/?LinkId=262160).</span><span class="sxs-lookup"><span data-stu-id="0fed3-128">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="0fed3-129">Se også</span><span class="sxs-lookup"><span data-stu-id="0fed3-129">See Also</span></span>
[<span data-ttu-id="0fed3-130">Introduktion</span><span class="sxs-lookup"><span data-stu-id="0fed3-130">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="0fed3-131">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0fed3-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="0fed3-132">Ofte stillede spørgsmål</span><span class="sxs-lookup"><span data-stu-id="0fed3-132">Frequently Asked Questions</span></span>](across-faq.md)  
