---
title: Ofte stillede spørgsmål om Fortæl mig | Microsoft Docs
description: Denne artikel indeholder svar på spørgsmål, som vores partnere og kunder ofte stiller om Fortæl mig.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 02/12/2020
ms.author: bholtorf
ms.openlocfilehash: 67dd65491710206245a2ff83dce3d3eb94484770
ms.sourcegitcommit: c78df3aefb3e2ed8c28e5ac8340d56ab787212e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071906"
---
# <a name="tell-me-faq"></a><span data-ttu-id="93510-103">Ofte stillede spørgsmål om Fortæl mig</span><span class="sxs-lookup"><span data-stu-id="93510-103">Tell Me FAQ</span></span>
<span data-ttu-id="93510-104">I dette emne besvares spørgsmål, som erfarne brugere ofte stiller om funktionen Fortæl mig.</span><span class="sxs-lookup"><span data-stu-id="93510-104">This topic answers questions that our advanced users often ask about the Tell Me feature.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="93510-105">Kan alle handlinger fra min aktuelle side registreres i Fortæl mig?</span><span class="sxs-lookup"><span data-stu-id="93510-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="93510-106">Nej.</span><span class="sxs-lookup"><span data-stu-id="93510-106">No.</span></span> <span data-ttu-id="93510-107">Handlinger i dele, f.eks. en salgslinjedelen eller faktabokse, vises ikke i Fortæl mig.</span><span class="sxs-lookup"><span data-stu-id="93510-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="93510-108">Filtreres resultaterne i Fortæl mig efter rettigheder?</span><span class="sxs-lookup"><span data-stu-id="93510-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="93510-109">Hvis brugeren ikke har AccessByPermissions, vises handlinger ikke.</span><span class="sxs-lookup"><span data-stu-id="93510-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="93510-110">Sider og rapporter vises i dog resultaterne, men kræver, at brugeren har rettigheder til at få adgang til dem.</span><span class="sxs-lookup"><span data-stu-id="93510-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="93510-111">Der vises en meddelelse, hvis brugeren ikke har rettigheder til at få vist objektet.</span><span class="sxs-lookup"><span data-stu-id="93510-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="93510-112">Viser Fortæl mig indhold fra mine tilpasninger eller installerede udvidelser fra tredjepart?</span><span class="sxs-lookup"><span data-stu-id="93510-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="93510-113">Handlinger, sider og rapporter, der stammer fra udvidelser, hentes af Fortæl mig, men det gælder ikke brugerdefineret dokumentation med hjælp.</span><span class="sxs-lookup"><span data-stu-id="93510-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="93510-114">Du kan finde tekniske oplysninger om, hvordan du kan gøre brugerdefinerede sider og rapporter registrerbare, i [Tilføjelse af sider og rapporter til søgning](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="93510-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="93510-115">Hvordan adskiller denne funktion sig fra det, der tidligere blev kaldt sidesøgning?</span><span class="sxs-lookup"><span data-stu-id="93510-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="93510-116">Sidesøgning er blevet udviklet til Fortæl mig for at hjælpe dig med at få arbejdet gjort hurtigt.</span><span class="sxs-lookup"><span data-stu-id="93510-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="93510-117">Sidesøgning kan kun hjælpe dig med at navigere til sider eller rapporter.</span><span class="sxs-lookup"><span data-stu-id="93510-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="93510-118">På et teknisk plan er Fortæl mig ikke længere baseret på det ældre MenuSuite-princip.</span><span class="sxs-lookup"><span data-stu-id="93510-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-d365fin-does-that-include-tell-me"></a><span data-ttu-id="93510-119">Jeg bruger [!INCLUDE[d365fin](includes/d365fin_md.md)] til det lokale miljø.</span><span class="sxs-lookup"><span data-stu-id="93510-119">I use on-premises [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="93510-120">Omfatter det Fortæl mig?</span><span class="sxs-lookup"><span data-stu-id="93510-120">Does that include Tell Me?</span></span>
<span data-ttu-id="93510-121">Du kan bruge Fortæl mig i den lokale webklient til at finde handlinger, sider og rapporter, men ikke dokumentation eller apps og konsulenttjenester i AppSource.</span><span class="sxs-lookup"><span data-stu-id="93510-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation, or apps and consulting services on AppSource.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="93510-122">Er Fortæl mig tilgængelig for alle formfaktorer?</span><span class="sxs-lookup"><span data-stu-id="93510-122">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="93510-123">Fortæl mig er kun tilgængelig i webklienten eller Windows-skrivebordsappen.</span><span class="sxs-lookup"><span data-stu-id="93510-123">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="93510-124">Findes dokumentationsresultaterne på alle sprog?</span><span class="sxs-lookup"><span data-stu-id="93510-124">Are the documentation results available in any language?</span></span>
<span data-ttu-id="93510-125">Hjælpeartikler vises på det sprog, du har angivet i **Mine indstillinger**, hvis Hjælp er tilgængelig på det pågældende sprog.</span><span class="sxs-lookup"><span data-stu-id="93510-125">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a><span data-ttu-id="93510-126">Hvorfor vises der ikke et bogmærkeikon for mine søgeresultater?</span><span class="sxs-lookup"><span data-stu-id="93510-126">Why don't I see a bookmark icon for my search results?</span></span>
<span data-ttu-id="93510-127">Bogmærkeikonet vises ikke i vinduet Fortæl mig, når tilpasning er deaktiveret for en brugerrolle.</span><span class="sxs-lookup"><span data-stu-id="93510-127">The bookmark icon is not displayed in the Tell Me window when personalization is disabled for a user role.</span></span>


## <a name="see-also"></a><span data-ttu-id="93510-128">Se også</span><span class="sxs-lookup"><span data-stu-id="93510-128">See Also</span></span>  
[<span data-ttu-id="93510-129">Gemme og tilpasse listevisninger</span><span class="sxs-lookup"><span data-stu-id="93510-129">Save and Personalize List Views</span></span>](ui-views.md)  
[<span data-ttu-id="93510-130">Søge efter sider og oplysninger med Fortæl mig</span><span class="sxs-lookup"><span data-stu-id="93510-130">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
[<span data-ttu-id="93510-131">Søge efter sider med Rollestifinder</span><span class="sxs-lookup"><span data-stu-id="93510-131">Finding Pages with the Role Explorer</span></span>](ui-role-explorer.md)  
[<span data-ttu-id="93510-132">Bogmærke en side eller en rapport i rollecenteret</span><span class="sxs-lookup"><span data-stu-id="93510-132">Bookmark a Page or Report on Your Role Center</span></span>](ui-bookmarks.md)
