---
title: Inspektion af sider i Business Central
description: Brug sideinspektionsfunktionen til at zoome ind på oplysninger om sideopsætningen og datakilden. Sideinspektion er velegnet til fejlfinding af problemer med dine data.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
author: jswymer
ms.date: 04/01/2019
ms.openlocfilehash: eb9d4ec76c0dbbd59763f7622ca51137c9563a91
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2019
ms.locfileid: "969874"
---
# <a name="inspecting-pages-in-business-central"></a><span data-ttu-id="ea831-104">Inspektion af sider i Business Central</span><span class="sxs-lookup"><span data-stu-id="ea831-104">Inspecting Pages in Business Central</span></span>

<span data-ttu-id="ea831-105">Sideinspektionsfunktionen giver mulighed at få oplysninger om en side, giver dig indsigt i sideopsætningen, de forskellige elementer, der udgør siden, og kilden bag de data, der vises.</span><span class="sxs-lookup"><span data-stu-id="ea831-105">The page inspection feature enables you to get details about a page, providing insight into the page design, the different elements that comprise the page, and the source behind the data it displays.</span></span> <span data-ttu-id="ea831-106">Sideinspektion er specielt beregnet til administratorer, superbrugere, supportmedarbejdere og udviklere.</span><span class="sxs-lookup"><span data-stu-id="ea831-106">Page inspection is especially designed for administrators, power users, support personnel, and developers.</span></span> <span data-ttu-id="ea831-107">Den er velegnet til læring af datamodellen bag en side og fejlfinding.</span><span class="sxs-lookup"><span data-stu-id="ea831-107">It is ideal for learning the data model behind a page and troubleshooting.</span></span> <span data-ttu-id="ea831-108">Hvis der f.eks. opstår et problem med en side, kan du bruge sideinspektion til at hente oplysninger,der skal videregives til systemadministratoren eller supportmedarbejderne.</span><span class="sxs-lookup"><span data-stu-id="ea831-108">For example, if you are experiencing a problem with a page, you could use page inspection to get information to pass on to your system administrator or support personnel.</span></span>

## <a name="working-with-page-inspection"></a><span data-ttu-id="ea831-109">Arbejde med sideinspektion</span><span class="sxs-lookup"><span data-stu-id="ea831-109">Working with Page Inspection</span></span>

<span data-ttu-id="ea831-110">Hvis du vil inspicere en side, skal du vælge ![ikonet Indstillinger](media/ui-experience/settings_icon_small.png) i øverste højre hjørne vælge og derefter klikke på **Inspicer**.</span><span class="sxs-lookup"><span data-stu-id="ea831-110">To inspect a page, in the top right corner, choose ![Settings icon](media/ui-experience/settings_icon_small.png), then choose **Inspect**.</span></span> <span data-ttu-id="ea831-111">Du kan også bruge tastaturgenvejen **Ctrl+Alt+F1**.</span><span class="sxs-lookup"><span data-stu-id="ea831-111">Or, you can use the keyboard shortcut **Ctrl+Alt+F1**.</span></span>

<span data-ttu-id="ea831-112">Ruden **Sideinspektion** åbnes på siden.</span><span class="sxs-lookup"><span data-stu-id="ea831-112">The **Page inspection** pane opens on the side.</span></span> <span data-ttu-id="ea831-113">Følgende figur illustrerer ruden **Sideinspektion** på siden **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="ea831-113">The following figure illustrates the **Page Inspection** pane on the **Sales Order** page.</span></span>

![Sideinspektion](media/page-inspection-example.png)

<span data-ttu-id="ea831-115">Når ruden **Sideinspektion** åbnes første gang, indeholder den oplysninger, der vedrører hovedsidens objekt.</span><span class="sxs-lookup"><span data-stu-id="ea831-115">When the **Page Inspection** pane first opens, it shows information that pertains to the main page object.</span></span>

<span data-ttu-id="ea831-116">Bruge tastaturgenvejen eller pegeredskabet til at flytte fokus til forskellige elementer på siden.</span><span class="sxs-lookup"><span data-stu-id="ea831-116">Use the keyboard or pointing device to move focus to different elements on the page.</span></span> <span data-ttu-id="ea831-117">Når du vælger en faktaboks eller et element på hovedsiden, er det omgivende område fremhævet med en kant, og ruden **Sideinspektion** viser oplysninger om det valgte element.</span><span class="sxs-lookup"><span data-stu-id="ea831-117">When you select a FactBox or a part on the main page, the bounding area is highlighted by a border, and the **Page Inspection** pane shows information about the selected element.</span></span> <span data-ttu-id="ea831-118">Den foregående figur viser f.eks. oplysninger om oversigtsdelen på siden **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="ea831-118">For example, the previous figure shows information about the list part in the **Sales Order** page.</span></span> <span data-ttu-id="ea831-119">Når du navigerer til andre sider i programmet, opdateres ruden **Sideinspektion** automatisk med sideoplysningerne, mens du bevæger dig videre.</span><span class="sxs-lookup"><span data-stu-id="ea831-119">As you navigate to other pages in the application, the **Page Inspection** pane will automatically update with page information as you move along.</span></span>

<span data-ttu-id="ea831-120">Du kan finde flere oplysninger om, hvad der vises i sideinspektionen, i [Inspektion og fejlfinding af sider](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) i hjælpen til Business Central-udviklere og it-eksperter.</span><span class="sxs-lookup"><span data-stu-id="ea831-120">For more information about what is shown in page inspection, see [Inspecting and Troubleshooting Pages](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) in the Business Central Developer and IT Pro help.</span></span>

<span data-ttu-id="ea831-121">Hvis du ikke kan se de oplysninger, du forventer at se, i ruden **Sideinspektion**, har du sandsynligvis ikke har de nødvendige rettigheder som beskrevet i næste sektion.</span><span class="sxs-lookup"><span data-stu-id="ea831-121">If you do not see the details that you expect to see in the **Page Inspection** pane, you probably do not have the required permissions, as described in th next section.</span></span>

## <a name="controlling-access-to-page-inspection-details"></a><span data-ttu-id="ea831-122">Styring af adgang til oplysninger om sideinspektion</span><span class="sxs-lookup"><span data-stu-id="ea831-122">Controlling Access to Page Inspection Details</span></span>

<span data-ttu-id="ea831-123">Som administrator kan du styre adgang til alle detaljer, der vises i ruden **Sideinspektion**, ved at konfigurere de rettigheder, som brugere har.</span><span class="sxs-lookup"><span data-stu-id="ea831-123">As an administrator, you can control access to the full details that are shown in the **Page Inspection** pane by configuring the permissions that users have.</span></span> <span data-ttu-id="ea831-124">Hvis du vil tildele en bruger rettigheder til alle detaljer, skal du give vedkommende rettigheden **Udfør** til **System** objekt **5330**.</span><span class="sxs-lookup"><span data-stu-id="ea831-124">To grant a user permission to the full details, give users **Execute** permission on the **System** object **5330**.</span></span> <span data-ttu-id="ea831-125">Du kan give denne rettighed ved hjælp af et rettighedssæt (f.eks. **D365-fejlfinding**) eller en brugergruppe (f.eks. **D365-fejlfinding**).</span><span class="sxs-lookup"><span data-stu-id="ea831-125">You can grant this permission by using a permission set (such as **D365 Troubleshoot**) or a user group (such as **D365 Troubleshoot**).</span></span> <span data-ttu-id="ea831-126">Du kan finde flere oplysninger om rettigheder i [Administrere brugere og deres rettigheder](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="ea831-126">For more information about permissions, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>

<span data-ttu-id="ea831-127">Brugere, der ikke tildeles rettigheder i **Systemobjekt 5330**, kan stadig få adgang til ruden **Sideinspektion**, men de får kun vist felterne **Side** og **Tabel**, der viser grundlæggende oplysninger, som de kan videregive til deres supportteam.</span><span class="sxs-lookup"><span data-stu-id="ea831-127">Users who are not granted permissions on **System object 5330** can still access the **Page Inspection** pane, but they will only see the **Page** and **Table** fields, which display basic details that they can pass on to their support team.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea831-128">Se også</span><span class="sxs-lookup"><span data-stu-id="ea831-128">See Also</span></span>

<span data-ttu-id="ea831-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ea831-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
