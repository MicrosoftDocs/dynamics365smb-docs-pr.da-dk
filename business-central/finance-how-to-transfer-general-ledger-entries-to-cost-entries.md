---
title: "Sådan overføres finansposter til omkostningsposter | Microsoft Docs"
description: "Du kan overføre finansposter til omkostningsposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 273a8c4341f621710819fd5fbc5cb8ce579c86f5
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="1a8de-103">Overføre finansposter til omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="1a8de-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="1a8de-104">Du kan overføre finansposter til omkostningsposter.</span><span class="sxs-lookup"><span data-stu-id="1a8de-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="1a8de-105">Inden du kører processen til overførsel af finansposter til omkostningsposter, skal du forberede overførslen for at undgå manuel korrektionsbogføring.</span><span class="sxs-lookup"><span data-stu-id="1a8de-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="1a8de-106">Sådan forberedes overførslen</span><span class="sxs-lookup"><span data-stu-id="1a8de-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="1a8de-107">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfiguration af omkostningsregnskab**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1a8de-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1a8de-108">På siden **Konfiguration af omkostningsregnskab** skal du kontrollere, at feltet **Startdato for finansoverførsel** er angivet til den korrekte værdi.</span><span class="sxs-lookup"><span data-stu-id="1a8de-108">On the **Cost Accounting Setup** page, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="1a8de-109">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningstyper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1a8de-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="1a8de-110">På siden **Omkostningstypekort** skal du kontrollere, at feltet **Finanskontointerval** er sammenkædet korrekt for hver pristype for at tage poster fra regnskabet.</span><span class="sxs-lookup"><span data-stu-id="1a8de-110">On the **Cost Type Card** page, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="1a8de-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoplan**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1a8de-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="1a8de-112">For hver relevant finanskonto skal du på siden **Finanskontokort** kontrollere, at feltet **Omkostningstypenr.**</span><span class="sxs-lookup"><span data-stu-id="1a8de-112">For each relevant general ledger account, on the **G/L Account Card** page, verify that the **Cost Type No.**</span></span> <span data-ttu-id="1a8de-113">er korrekt knyttet til en omkostningstype.</span><span class="sxs-lookup"><span data-stu-id="1a8de-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="1a8de-114">Du kan finde flere oplysninger under [Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="1a8de-114">For more information, see [Setting Up Cost Accounting](finance-set-up-cost-accounting.md).</span></span>  
7.  <span data-ttu-id="1a8de-115">Kontroller, at alle relevante finansposter har dimensionsværdier, der svarer til et omkostningssted og et omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="1a8de-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="1a8de-116">Sådan overføres finansposter til omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="1a8de-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="1a8de-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Overfør finansposter til omkostningsregnskab**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1a8de-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1a8de-118">Vælg knappen **Ja** for at starte overførslen.</span><span class="sxs-lookup"><span data-stu-id="1a8de-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="1a8de-119">Processen overfører alle finansposter, der ikke allerede er overført.</span><span class="sxs-lookup"><span data-stu-id="1a8de-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="1a8de-120">Under overførslen opretter processen forbindelser i posterne i tabellen **Omkostningspost** og tabellen **Omkostningsregister**.</span><span class="sxs-lookup"><span data-stu-id="1a8de-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="1a8de-121">Dette gør det muligt at spore kilden til omkostningsposter.</span><span class="sxs-lookup"><span data-stu-id="1a8de-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1a8de-122">Se også</span><span class="sxs-lookup"><span data-stu-id="1a8de-122">See Also</span></span>  
<span data-ttu-id="1a8de-123">[Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="1a8de-123">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
[<span data-ttu-id="1a8de-124">Konfigurere omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="1a8de-124">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)   

