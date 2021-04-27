---
title: Tildeling og administration af opgaver
description: Få mere at vide om, hvordan du tildeler opgaver til brugere, herunder bogholderen, i Business Central, og hvordan du afhenter og afslutter opgaver.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 71e9c93eede8b39561dc78ff61732273003ce8de
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786978"
---
# <a name="define-user-tasks"></a><span data-ttu-id="83e49-103">Definere brugeropgaver</span><span class="sxs-lookup"><span data-stu-id="83e49-103">Define User Tasks</span></span>

<span data-ttu-id="83e49-104">I [!INCLUDE[prod_short](includes/prod_short.md)] kan du oprette opgaver for at minde dig om arbejde, der skal udføres.</span><span class="sxs-lookup"><span data-stu-id="83e49-104">In [!INCLUDE[prod_short](includes/prod_short.md)], you can create tasks to remind you of work to be done.</span></span> <span data-ttu-id="83e49-105">Du kan oprette opgaver til dig selv, men du kan også tildele opgaver til andre eller få tildelt en opgave af en anden i organisationen.</span><span class="sxs-lookup"><span data-stu-id="83e49-105">You can create tasks for yourself, but you can also assign tasks to others or be assigned a task by someone else in your organization.</span></span>  

## <a name="managing-user-tasks"></a><span data-ttu-id="83e49-106">Administrere brugeropgaver</span><span class="sxs-lookup"><span data-stu-id="83e49-106">Managing User Tasks</span></span>

<span data-ttu-id="83e49-107">Siden **Brugeropgaver** viser alle opgaver, og du kan nemt oprette og tildele nye opgaver.</span><span class="sxs-lookup"><span data-stu-id="83e49-107">The **User Tasks** page shows all tasks, and you can easily create and assign new tasks.</span></span> <span data-ttu-id="83e49-108">Når du opretter en opgave, kan du angive start- og forfaldsdato, og du kan føje et link til siden eller rapporten i [!INCLUDE[prod_short](includes/prod_short.md)], hvor brugeren skal udføre arbejdet.</span><span class="sxs-lookup"><span data-stu-id="83e49-108">When you create a task, you can specify the start date and due date, and you can add a link to the page or report in [!INCLUDE[prod_short](includes/prod_short.md)] where the user must do the work.</span></span>  

<span data-ttu-id="83e49-109">Du kan f.eks. oprette en opgave til dig selv eller en kollega for at få vist alle bogførte salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="83e49-109">For example, you can create a task for yourself or a coworker to view all posted sales invoices.</span></span> <span data-ttu-id="83e49-110">I så fald skal knytte du opgaven til side 143, **Bogf. salgsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="83e49-110">In that case, you link the task to page 143, **Posted Sales Invoices**.</span></span> <span data-ttu-id="83e49-111">På følgende skærmbillede oprettes der en opgave for MeganB for at gennemgå de bogførte salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="83e49-111">In the following screenshot, someone is creating a task for MeganB to review the posted sales invoices.</span></span>  

:::image type="content" source="media/across-user-tasks/sample-user-task.png" alt-text="Eksempel på en brugeropgave":::

> [!TIP]  
> <span data-ttu-id="83e49-113">Brug opslaget i feltet **Side**, og brug derefter feltet **Søg** til at finde den ønskede side.</span><span class="sxs-lookup"><span data-stu-id="83e49-113">Use the look-up in the **Page** field and then use the **Search** field to find the page that you want.</span></span>  
>
> <span data-ttu-id="83e49-114">Du kan oprette et link til enhver side, men du kan ikke oprette en link til enkelte poster, så du skal bruge beskrivelsen så eksplicit som muligt, f.eks. skrive "Kig nærmere på Kundenr."</span><span class="sxs-lookup"><span data-stu-id="83e49-114">You can link to any page, but you cannot link to individual entries, so make the description as explicit as possible, such as writing "Please take a look at customer no.</span></span> <span data-ttu-id="83e49-115">10000, og sørg for, at der ikke er forfaldne betalinger".</span><span class="sxs-lookup"><span data-stu-id="83e49-115">10000 and make sure they don't have overdue payments.".</span></span>

### <a name="picking-up-user-tasks"></a><span data-ttu-id="83e49-116">Hente brugeropgaver</span><span class="sxs-lookup"><span data-stu-id="83e49-116">Picking Up User Tasks</span></span>

<span data-ttu-id="83e49-117">I rollecentrene Virksomhedsleder, Bogholder og Regnskabsmedarbejder viser et felt ventende opgaver, der er knyttet til den pågældende bruger.</span><span class="sxs-lookup"><span data-stu-id="83e49-117">In the Business Manager, Bookkeeper, and Accountant Role Centers, a tile shows pending tasks that are assigned to that user.</span></span> <span data-ttu-id="83e49-118">For at hente en opgave skal du blot vælge den på listen over ventende brugeropgaver.</span><span class="sxs-lookup"><span data-stu-id="83e49-118">To pick up a task, simply choose it from the list of pending user tasks.</span></span> <span data-ttu-id="83e49-119">På båndet åbner linket **Gå til opgaveelementet** den side, hvor du kan udføre arbejdet.</span><span class="sxs-lookup"><span data-stu-id="83e49-119">In the ribbon, the link **Go to Task Item** opens the page where you can do the work.</span></span>  

<span data-ttu-id="83e49-120">Når du har udført en opgave, skal du blot markeres som fuldført.</span><span class="sxs-lookup"><span data-stu-id="83e49-120">When you have completed a task, simply mark it as completed.</span></span>  

### <a name="deleting-user-tasks"></a><span data-ttu-id="83e49-121">Slette brugeropgaver</span><span class="sxs-lookup"><span data-stu-id="83e49-121">Deleting User Tasks</span></span>

<span data-ttu-id="83e49-122">Hvis du vil masseslette alle eller nogle brugeropgaver, kan du bruge rapporten **Slet brugeropgaver**.</span><span class="sxs-lookup"><span data-stu-id="83e49-122">If you want to bulk delete all or some user tasks, you can use the **Delete User Tasks** report.</span></span> <span data-ttu-id="83e49-123">På anmodningssiden kan du angive filtre, der bestemmer, hvilke opgaver der skal slettes.</span><span class="sxs-lookup"><span data-stu-id="83e49-123">In the request page, you can set filters to determine which tasks must be deleted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="83e49-124">Se også</span><span class="sxs-lookup"><span data-stu-id="83e49-124">See Also</span></span>

[<span data-ttu-id="83e49-125">Søge efter en side eller rapport</span><span class="sxs-lookup"><span data-stu-id="83e49-125">Searching for a Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="83e49-126">[Revisoroplevelser i [!INCLUDE[prod_short](includes/prod_short.md)]](finance-accounting.md)</span><span class="sxs-lookup"><span data-stu-id="83e49-126">[Accountant Experiences in [!INCLUDE[prod_short](includes/prod_short.md)]](finance-accounting.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]