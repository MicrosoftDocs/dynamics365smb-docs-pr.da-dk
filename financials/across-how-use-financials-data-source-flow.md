---
title: Forbinde dataene med Flow | Microsoft Docs
description: "Du kan gøre dine Financials-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette et automatiseret workflow."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: dde99e50c6984a7ec162b4047e8640e6affb3f25
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="38795-103">Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i et automatisk workflow</span><span class="sxs-lookup"><span data-stu-id="38795-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="38795-104">Du kan bruge dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del af en arbejdsproces i Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="38795-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="38795-105">Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Flow.</span><span class="sxs-lookup"><span data-stu-id="38795-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="38795-106">Sådan tilføjes [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow</span><span class="sxs-lookup"><span data-stu-id="38795-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="38795-107">Gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/) i din webbrowser, og log på.</span><span class="sxs-lookup"><span data-stu-id="38795-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="38795-108">Vælg **Mine Flows** på båndet øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="38795-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="38795-109">I vinduet **Mine Flows** skal du vælge indstillingen **Opret fra tom**.</span><span class="sxs-lookup"><span data-stu-id="38795-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="38795-110">På listen over tilgængelige udløsere, skal du vælge en af de [!INCLUDE[d365fin](includes/d365fin_md.md)]-udløsere, der er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="38795-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="38795-111">*Når der anmodes om godkendelse af en debitor*,</span><span class="sxs-lookup"><span data-stu-id="38795-111">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="38795-112">*Når der anmodes om godkendelse af en finanskladdekørsel*,</span><span class="sxs-lookup"><span data-stu-id="38795-112">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="38795-113">*Når der anmodes om godkendelse af en finanskladdelinje*,</span><span class="sxs-lookup"><span data-stu-id="38795-113">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="38795-114">*Når der anmodes om godkendelse af en vare*,</span><span class="sxs-lookup"><span data-stu-id="38795-114">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="38795-115">*Når der anmodes om godkendelse af et købsdokument*,</span><span class="sxs-lookup"><span data-stu-id="38795-115">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="38795-116">*Når der anmodes om godkendelse af et salgsdokument* eller</span><span class="sxs-lookup"><span data-stu-id="38795-116">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="38795-117">*Når der anmodes om godkendelse af en kreditor*.</span><span class="sxs-lookup"><span data-stu-id="38795-117">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="38795-118">Flow beder dig om at vælge et firma i din [!INCLUDE[d365fin](includes/d365fin_md.md)]-lejer.</span><span class="sxs-lookup"><span data-stu-id="38795-118">Flow will prompt you to select a company within your [!INCLUDE[d365fin](includes/d365fin_md.md)] tenant.</span></span> <span data-ttu-id="38795-119">Da hvert trin i Flow er uafhængigt af det næste, kan du blive nødt til at definere virksomheden flere gange, når du bruger en [!INCLUDE[d365fin](includes/d365fin_md.md)]-skabelon.</span><span class="sxs-lookup"><span data-stu-id="38795-119">Because each step in the Flow is independent of the next, you may be required to define the company multiple times when using a [!INCLUDE[d365fin](includes/d365fin_md.md)] template.</span></span>

<span data-ttu-id="38795-120">Nu har du oprettet forbindelse til dine data i Finance and Operations, Business edition og er klar til at opbygge dit flow.</span><span class="sxs-lookup"><span data-stu-id="38795-120">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="38795-121">Du kan finde flere oplysninger i [Flow-dokumentationen](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="38795-121">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="38795-122">For fejlfinding af Microsoft Flow skal du se [Fejlfinding af integration med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="38795-122">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="38795-123">Se også</span><span class="sxs-lookup"><span data-stu-id="38795-123">See Also</span></span>
<span data-ttu-id="38795-124">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="38795-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="38795-125">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="38795-125">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="38795-126">[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="38795-126">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="38795-127">[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="38795-127">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="38795-128">Finans</span><span class="sxs-lookup"><span data-stu-id="38795-128">Finance</span></span>](finance.md)  

