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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="2eb35-103">Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i et automatisk workflow</span><span class="sxs-lookup"><span data-stu-id="2eb35-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="2eb35-104">Du kan bruge dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del af en arbejdsproces i Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="2eb35-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="2eb35-105">Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Flow.</span><span class="sxs-lookup"><span data-stu-id="2eb35-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="2eb35-106">Sådan tilføjes [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow</span><span class="sxs-lookup"><span data-stu-id="2eb35-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="2eb35-107">Gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/) i din webbrowser, og log på.</span><span class="sxs-lookup"><span data-stu-id="2eb35-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="2eb35-108">Vælg **Mine Flows** på båndet øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="2eb35-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="2eb35-109">I vinduet **Mine Flows** skal du vælge indstillingen **Opret fra tom**.</span><span class="sxs-lookup"><span data-stu-id="2eb35-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="2eb35-110">På listen over tilgængelige udløsere, skal du vælge en af de [!INCLUDE[d365fin](includes/d365fin_md.md)]-udløsere, der er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="2eb35-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="2eb35-111">*Når en post oprettes*,</span><span class="sxs-lookup"><span data-stu-id="2eb35-111">*When a record is created*,</span></span>  
    <span data-ttu-id="2eb35-112">*Når en post slettes*,</span><span class="sxs-lookup"><span data-stu-id="2eb35-112">*When a record is deleted*,</span></span>  
    <span data-ttu-id="2eb35-113">*Når en post ændres*,</span><span class="sxs-lookup"><span data-stu-id="2eb35-113">*When a record is modified*,</span></span>  
    <span data-ttu-id="2eb35-114">*Når der anmodes om godkendelse af en debitor*,</span><span class="sxs-lookup"><span data-stu-id="2eb35-114">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="2eb35-115">*Når der anmodes om godkendelse af en finanskladdekørsel*,</span><span class="sxs-lookup"><span data-stu-id="2eb35-115">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="2eb35-116">*Når der anmodes om godkendelse af en finanskladdelinje*,</span><span class="sxs-lookup"><span data-stu-id="2eb35-116">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="2eb35-117">*Når der anmodes om godkendelse af en vare*,</span><span class="sxs-lookup"><span data-stu-id="2eb35-117">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="2eb35-118">*Når der anmodes om godkendelse af et købsdokument*,</span><span class="sxs-lookup"><span data-stu-id="2eb35-118">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="2eb35-119">*Når der anmodes om godkendelse af et salgsdokument* eller</span><span class="sxs-lookup"><span data-stu-id="2eb35-119">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="2eb35-120">*Når der anmodes om godkendelse af en kreditor*.</span><span class="sxs-lookup"><span data-stu-id="2eb35-120">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="2eb35-121">Flow beder dig om de oplysninger, der kræves for at oprette forbindelse til dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data.</span><span class="sxs-lookup"><span data-stu-id="2eb35-121">Flow will prompt you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="2eb35-122">Hvis du har valgt en af følgende udløsere: *Når en post oprettes*, *Når en post ændres*, eller *Når en post slettes*, skal du vælge en firmanavn og tabelnavn.</span><span class="sxs-lookup"><span data-stu-id="2eb35-122">If you selected one of the following triggers: *When a record is created*, *When a record is modified*, or *When a record is deleted*, you must select a company name and table name.</span></span> <span data-ttu-id="2eb35-123">Til andre udløsere er kun firmanavnet påkrævet for at oprette forbindelse.</span><span class="sxs-lookup"><span data-stu-id="2eb35-123">With any other trigger, only the company name is required to connect.</span></span>

   <span data-ttu-id="2eb35-124">Flow viser en liste over regnskaber og tabeller, der er tilgængelige fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2eb35-124">Flow will show a list of companies and tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2eb35-125">Disse tabeller, eller slutpunkter, repræsenterer de webtjenester, som du har publiceret fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2eb35-125">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="2eb35-126">Du kan også vælge at oprette en ny URL-adresse for webtjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at bruge handlingen **Opret datasæt** på siden **Webtjenester** ved hjælp af guiden Assisteret opsætning for **Konfigurer rapporteringsdata** eller ved at vælge handlingen **Rediger i Excel** på en af listerne.</span><span class="sxs-lookup"><span data-stu-id="2eb35-126">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>

<span data-ttu-id="2eb35-127">Nu har du oprettet forbindelse til dine data i Finance and Operations, Business edition og er klar til at opbygge dit flow.</span><span class="sxs-lookup"><span data-stu-id="2eb35-127">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="2eb35-128">Du kan finde flere oplysninger i [Flow-dokumentationen](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="2eb35-128">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="2eb35-129">For fejlfinding af Microsoft Flow skal du se [Fejlfinding af integration med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="2eb35-129">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2eb35-130">Se også</span><span class="sxs-lookup"><span data-stu-id="2eb35-130">See Also</span></span>
<span data-ttu-id="2eb35-131">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="2eb35-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="2eb35-132">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="2eb35-132">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="2eb35-133">[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="2eb35-133">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="2eb35-134">[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="2eb35-134">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="2eb35-135">Finans</span><span class="sxs-lookup"><span data-stu-id="2eb35-135">Finance</span></span>](finance.md)  

