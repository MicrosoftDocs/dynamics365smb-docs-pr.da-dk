---
title: "Fremgangsmåde: Begrænse og tillade brug af en post | Microsoft Docs"
description: "Hvis du vil begrænse brugen af en record, f.eks. i bestemte aktiviteter, kan du integrere to arbejdsgangssvar i en arbejdsgang, der styrer forbruget af posten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4636cdedc2c99d1aa7cfc2dc361f7135aa3c4199
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="c3274-103">Begrænse og tillade brugen af en record</span><span class="sxs-lookup"><span data-stu-id="c3274-103">Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="c3274-104">Hvis du vil begrænse brugen af en record, f.eks. i bestemte aktiviteter, kan du integrere to arbejdsgangssvar i en arbejdsgang, der styrer forbruget af posten.</span><span class="sxs-lookup"><span data-stu-id="c3274-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="c3274-105">Et arbejdsgangsvar begrænser brugen af posten, som defineret i arbejdsganghændelsen og -betingelserne.</span><span class="sxs-lookup"><span data-stu-id="c3274-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="c3274-106">Et andet arbejdsgangsvar tillader brug af posten, som defineret i arbejdsganghændelsen og -betingelserne.</span><span class="sxs-lookup"><span data-stu-id="c3274-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="c3274-107">Der findes to svar i den generelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] til dette formål: **Begræns brugen af en record.**</span><span class="sxs-lookup"><span data-stu-id="c3274-107">Two responses exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="c3274-108">og **Tillad brugen af en record**.</span><span class="sxs-lookup"><span data-stu-id="c3274-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="c3274-109">Den generelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter begrænsning af bogføring af en post, eksport af en post som en betaling og udskrivning af en post som en check.</span><span class="sxs-lookup"><span data-stu-id="c3274-109">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="c3274-110">For at understøtte andre begrænsninger skal en Microsoft-partner tilpasse programkoden.</span><span class="sxs-lookup"><span data-stu-id="c3274-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c3274-111">Arbejdsgangfunktionen, som begrænser og tillader brug af poster, er ikke relateret til funktioner, der blokerer bogføring af vare-, debitor- og kreditorposter.</span><span class="sxs-lookup"><span data-stu-id="c3274-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="c3274-112">Følgende fremgangsmåde beskriver, hvordan du kan begrænse bogføring af købsordrer, indtil de er godkendt.</span><span class="sxs-lookup"><span data-stu-id="c3274-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="c3274-113">Den nye arbejdsgang baseres på den eksisterende arbejdsgangskabelon Arbejdsgang for godkendelse af købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="c3274-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="c3274-114">Sådan opretter du et trin i en arbejdsgang, som begrænser bogføring af ikke-godkendte købsordrer</span><span class="sxs-lookup"><span data-stu-id="c3274-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="c3274-115">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Workflows**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c3274-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c3274-116">I vinduet **Workflows** skal du oprette et nyt workflow med navnet Godkendelsesworkflow for købsordre.</span><span class="sxs-lookup"><span data-stu-id="c3274-116">In the **Workflows** window, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="c3274-117">Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="c3274-117">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="c3274-118">Vælg handlingen **Kopiér fra arbejdsgangsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="c3274-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="c3274-119">Vælg feltet **Kildearbejdsgangskode**, og vælg derefter i vinduet **Workflowskabeloner** workflowskabelonen Godkendelsesworkflow for købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="c3274-119">Choose the **Source Workflow Code** field, and then, in the **Workflow Templates** window, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="c3274-120">Bemærk, at de to første trin i arbejdsgangen drejer sig om at begrænse og derefter tillade brug af købsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="c3274-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="c3274-121">Fortsæt for at ændre hændelsesbetingelsen i det første trin af den nye arbejdsgang for at angive, at den gælder for købsordrer.</span><span class="sxs-lookup"><span data-stu-id="c3274-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="c3274-122">I oversigtspanelet **Workflowtrin** skal du vælge feltet **Hændelsesbetingelser** og derefter vælge **Ordre** for filteret **Dokumenttype**.</span><span class="sxs-lookup"><span data-stu-id="c3274-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="c3274-123">Fortsæt med at redigere, slette eller tilføje andre trin i arbejdsgangen for at tilpasse til en forretningsproces, der begynder med at begrænse bogføring af ikke-godkendte købsordrer.</span><span class="sxs-lookup"><span data-stu-id="c3274-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c3274-124">Se også</span><span class="sxs-lookup"><span data-stu-id="c3274-124">See Also</span></span>  
<span data-ttu-id="c3274-125">[Oprette arbejdsgange](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c3274-125">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="c3274-126">Workflow</span><span class="sxs-lookup"><span data-stu-id="c3274-126">Workflow</span></span>](across-workflow.md)   

