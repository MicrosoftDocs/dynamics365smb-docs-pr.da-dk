---
title: 'Fremgangsmåde: Begrænse og tillade brug af en post | Microsoft Docs'
description: Hvis du vil begrænse brugen af en record, f.eks. i bestemte aktiviteter, kan du integrere to arbejdsgangssvar i en arbejdsgang, der styrer forbruget af posten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbb22a00e878e8c4d75cb5fcdbcc27a28d9d22a4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783971"
---
# <a name="restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="5414a-103">Begrænse og tillade brugen af en record</span><span class="sxs-lookup"><span data-stu-id="5414a-103">Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="5414a-104">Hvis du vil begrænse brugen af en record, f.eks. i bestemte aktiviteter, kan du integrere to arbejdsgangssvar i en arbejdsgang, der styrer forbruget af posten.</span><span class="sxs-lookup"><span data-stu-id="5414a-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="5414a-105">Et arbejdsgangsvar begrænser brugen af posten, som defineret i arbejdsganghændelsen og -betingelserne.</span><span class="sxs-lookup"><span data-stu-id="5414a-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="5414a-106">Et andet arbejdsgangsvar tillader brug af posten, som defineret i arbejdsganghændelsen og -betingelserne.</span><span class="sxs-lookup"><span data-stu-id="5414a-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="5414a-107">Der findes to svar i den generelle version af [!INCLUDE[prod_short](includes/prod_short.md)] til dette formål: **Begræns brugen af en record.**</span><span class="sxs-lookup"><span data-stu-id="5414a-107">Two responses exist in the generic version of [!INCLUDE[prod_short](includes/prod_short.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="5414a-108">og **Tillad brugen af en record**.</span><span class="sxs-lookup"><span data-stu-id="5414a-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="5414a-109">Den generelle version af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter begrænsning af bogføring af en post, eksport af en post som en betaling og udskrivning af en post som en check.</span><span class="sxs-lookup"><span data-stu-id="5414a-109">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="5414a-110">For at understøtte andre begrænsninger skal en Microsoft-partner tilpasse programkoden.</span><span class="sxs-lookup"><span data-stu-id="5414a-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="5414a-111">Arbejdsgangfunktionen, som begrænser og tillader brug af poster, er ikke relateret til funktioner, der blokerer bogføring af vare-, debitor- og kreditorposter.</span><span class="sxs-lookup"><span data-stu-id="5414a-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="5414a-112">Følgende fremgangsmåde beskriver, hvordan du kan begrænse bogføring af købsordrer, indtil de er godkendt.</span><span class="sxs-lookup"><span data-stu-id="5414a-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="5414a-113">Den nye arbejdsgang baseres på den eksisterende arbejdsgangskabelon Arbejdsgang for godkendelse af købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="5414a-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="5414a-114">Sådan opretter du et trin i en arbejdsgang, som begrænser bogføring af ikke-godkendte købsordrer</span><span class="sxs-lookup"><span data-stu-id="5414a-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="5414a-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Arbejdsgange**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5414a-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5414a-116">På siden **Workflows** skal du oprette et nyt workflow med navnet Godkendelsesworkflow for købsordre.</span><span class="sxs-lookup"><span data-stu-id="5414a-116">On the **Workflows** page, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="5414a-117">Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="5414a-117">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="5414a-118">Vælg handlingen **Kopiér fra arbejdsgangsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="5414a-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="5414a-119">Vælg feltet **Kildearbejdsgangskode**, og vælg derefter på siden **Workflowskabeloner** workflowskabelonen Godkendelsesworkflow for købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="5414a-119">Choose the **Source Workflow Code** field, and then, on the **Workflow Templates** page, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="5414a-120">Bemærk, at de to første trin i arbejdsgangen drejer sig om at begrænse og derefter tillade brug af købsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="5414a-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="5414a-121">Fortsæt for at ændre hændelsesbetingelsen i det første trin af den nye arbejdsgang for at angive, at den gælder for købsordrer.</span><span class="sxs-lookup"><span data-stu-id="5414a-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="5414a-122">I oversigtspanelet **Workflowtrin** skal du vælge feltet **Hændelsesbetingelser** og derefter vælge **Ordre** for filteret **Dokumenttype**.</span><span class="sxs-lookup"><span data-stu-id="5414a-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="5414a-123">Fortsæt med at redigere, slette eller tilføje andre trin i arbejdsgangen for at tilpasse til en forretningsproces, der begynder med at begrænse bogføring af ikke-godkendte købsordrer.</span><span class="sxs-lookup"><span data-stu-id="5414a-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5414a-124">Se også</span><span class="sxs-lookup"><span data-stu-id="5414a-124">See Also</span></span>  
<span data-ttu-id="5414a-125">[Oprette arbejdsgange](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="5414a-125">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="5414a-126">Workflow</span><span class="sxs-lookup"><span data-stu-id="5414a-126">Workflow</span></span>](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]