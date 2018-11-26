---
title: "Ofte stillede spørgsmål om Fortæl mig | Microsoft Docs"
description: "Denne artikel indeholder svar på spørgsmål, som vores partnere og kunder ofte stiller om Fortæl mig."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 70ab7fb07cda5ce9d86b3f39dd14321829e85a52
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="tell-me-faq"></a><span data-ttu-id="51e1f-103">Ofte stillede spørgsmål om Fortæl mig</span><span class="sxs-lookup"><span data-stu-id="51e1f-103">Tell Me FAQ</span></span>
<span data-ttu-id="51e1f-104">Dette emne indeholder svar på spørgsmål, som vores avancerede brugere ofte stiller om den nye Fortæl mig-funktion, som erstatter den tidligere sidesøgefunktion, der også kaldes **Søg efter side eller rapport**.</span><span class="sxs-lookup"><span data-stu-id="51e1f-104">This topic answers questions that our advanced users often ask about the new Tell Me feature, which has replaced the previous Page Search feature known as **Find Pages and Reports**.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="51e1f-105">Kan alle handlinger fra min aktuelle side registreres i Fortæl mig?</span><span class="sxs-lookup"><span data-stu-id="51e1f-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="51e1f-106">Nej.</span><span class="sxs-lookup"><span data-stu-id="51e1f-106">No.</span></span> <span data-ttu-id="51e1f-107">Handlinger i dele, f.eks. en salgslinjedelen eller faktabokse, vises ikke i Fortæl mig.</span><span class="sxs-lookup"><span data-stu-id="51e1f-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="51e1f-108">Filtreres resultaterne i Fortæl mig efter rettigheder?</span><span class="sxs-lookup"><span data-stu-id="51e1f-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="51e1f-109">Hvis brugeren ikke har AccessByPermissions, vises handlinger ikke.</span><span class="sxs-lookup"><span data-stu-id="51e1f-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="51e1f-110">Sider og rapporter vises i dog resultaterne, men kræver, at brugeren har rettigheder til at få adgang til dem.</span><span class="sxs-lookup"><span data-stu-id="51e1f-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="51e1f-111">Der vises en meddelelse, hvis brugeren ikke har rettigheder til at få vist objektet.</span><span class="sxs-lookup"><span data-stu-id="51e1f-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="51e1f-112">Viser Fortæl mig indhold fra mine tilpasninger eller installerede udvidelser fra tredjepart?</span><span class="sxs-lookup"><span data-stu-id="51e1f-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="51e1f-113">Handlinger, sider og rapporter, der stammer fra udvidelser, hentes af Fortæl mig, men det gælder ikke brugerdefineret dokumentation med hjælp.</span><span class="sxs-lookup"><span data-stu-id="51e1f-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="51e1f-114">Du kan finde tekniske oplysninger om, hvordan du kan gøre brugerdefinerede sider og rapporter registrerbare, i [Tilføjelse af sider og rapporter til søgning](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="51e1f-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="51e1f-115">Hvordan adskiller denne funktion sig fra det, der tidligere blev kaldt sidesøgning?</span><span class="sxs-lookup"><span data-stu-id="51e1f-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="51e1f-116">Sidesøgning er blevet udviklet til Fortæl mig for at hjælpe dig med at få arbejdet gjort hurtigt.</span><span class="sxs-lookup"><span data-stu-id="51e1f-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="51e1f-117">Sidesøgning kan kun hjælpe dig med at navigere til sider eller rapporter.</span><span class="sxs-lookup"><span data-stu-id="51e1f-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="51e1f-118">På et teknisk plan er Fortæl mig ikke længere baseret på det ældre MenuSuite-princip.</span><span class="sxs-lookup"><span data-stu-id="51e1f-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-included365finincludesd365finmdmd-does-that-include-tell-me"></a><span data-ttu-id="51e1f-119">Jeg bruger [!INCLUDE[d365fin](includes/d365fin_md.md)] til det lokale miljø.</span><span class="sxs-lookup"><span data-stu-id="51e1f-119">I use on-premises [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="51e1f-120">Omfatter det Fortæl mig?</span><span class="sxs-lookup"><span data-stu-id="51e1f-120">Does that include Tell Me?</span></span>
<span data-ttu-id="51e1f-121">Du kan bruge Fortæl mig i den lokale webklient til at finde handlinger, sider og rapporter, men ikke dokumentation.</span><span class="sxs-lookup"><span data-stu-id="51e1f-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation.</span></span> <span data-ttu-id="51e1f-122">Brugere, der opretter forbindelse til [!INCLUDE[d365fin](includes/d365fin_md.md)] fra Dynamics NAV-klienten fortsætter med at bruge sidesøgning.</span><span class="sxs-lookup"><span data-stu-id="51e1f-122">Users connecting to [!INCLUDE[d365fin](includes/d365fin_md.md)] from the Dynamics NAV client continue to use Page Search.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="51e1f-123">Er Fortæl mig tilgængelig for alle formfaktorer?</span><span class="sxs-lookup"><span data-stu-id="51e1f-123">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="51e1f-124">Fortæl mig er kun tilgængelig i webklienten eller Windows-skrivebordsappen.</span><span class="sxs-lookup"><span data-stu-id="51e1f-124">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="51e1f-125">Findes dokumentationsresultaterne på alle sprog?</span><span class="sxs-lookup"><span data-stu-id="51e1f-125">Are the documentation results available in any language?</span></span>
<span data-ttu-id="51e1f-126">Hjælpeartikler vises på det sprog, du har angivet i **Mine indstillinger**, hvis Hjælp er tilgængelig på det pågældende sprog.</span><span class="sxs-lookup"><span data-stu-id="51e1f-126">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

## <a name="see-also"></a><span data-ttu-id="51e1f-127">Se også</span><span class="sxs-lookup"><span data-stu-id="51e1f-127">See Also</span></span>  
[<span data-ttu-id="51e1f-128">Finde funktioner og oplysninger</span><span class="sxs-lookup"><span data-stu-id="51e1f-128">Finding Features and Information</span></span>](ui-search.md)
