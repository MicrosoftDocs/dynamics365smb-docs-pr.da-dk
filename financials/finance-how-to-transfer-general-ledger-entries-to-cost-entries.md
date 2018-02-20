---
title: "Sådan overføres finansposter til omkostningsposter | Microsoft Docs"
description: "Du kan overføre finansposter til omkostningsposter."
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
ms.openlocfilehash: 592f42f53593735526ccbd3ddaa69bb0778de0ac
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="bc001-103">Overføre finansposter til omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="bc001-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="bc001-104">Du kan overføre finansposter til omkostningsposter.</span><span class="sxs-lookup"><span data-stu-id="bc001-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="bc001-105">Inden du kører processen til overførsel af finansposter til omkostningsposter, skal du forberede overførslen for at undgå manuel korrektionsbogføring.</span><span class="sxs-lookup"><span data-stu-id="bc001-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="bc001-106">Sådan forberedes overførslen</span><span class="sxs-lookup"><span data-stu-id="bc001-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="bc001-107">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Konfiguration af omkostningsregnskab**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="bc001-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="bc001-108">I vinduet **Konfiguration af omkostningsregnskab** skal du kontrollere, at feltet **Startdato for finansoverførsel** er angivet til den korrekte værdi.</span><span class="sxs-lookup"><span data-stu-id="bc001-108">In the **Cost Accounting Setup** window, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="bc001-109">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Diagram over omkostningstyper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="bc001-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="bc001-110">I vinduet **Omkostningstypekort** skal du kontrollere, at feltet **Finanskontointerval** er sammenkædet korrekt for hver pristype for at tage poster fra regnskabet.</span><span class="sxs-lookup"><span data-stu-id="bc001-110">In the **Cost Type Card** window, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="bc001-111">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="bc001-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="bc001-112">For hver relevant finanskonto skal du i vinduet **Finanskontokort** kontrollere, at feltet **Omkostningstypenr.**</span><span class="sxs-lookup"><span data-stu-id="bc001-112">For each relevant general ledger account, in the **G/L Account Card** window, verify that the **Cost Type No.**</span></span> <span data-ttu-id="bc001-113">er korrekt knyttet til en omkostningstype.</span><span class="sxs-lookup"><span data-stu-id="bc001-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="bc001-114">Du kan finde flere oplysninger i [Definition af forholdet mellem omkostningstyper og finanskonti](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="bc001-114">For more information, see [Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span></span>  
7.  <span data-ttu-id="bc001-115">Kontroller, at alle relevante finansposter har dimensionsværdier, der svarer til et omkostningssted og et omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="bc001-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="bc001-116">Sådan overføres finansposter til omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="bc001-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="bc001-117">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Overfør finansposter til CA**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="bc001-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="bc001-118">Vælg knappen **Ja** for at starte overførslen.</span><span class="sxs-lookup"><span data-stu-id="bc001-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="bc001-119">Processen overfører alle finansposter, der ikke allerede er overført.</span><span class="sxs-lookup"><span data-stu-id="bc001-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="bc001-120">Under overførslen opretter processen forbindelser i posterne i tabellen **Omkostningspost** og tabellen **Omkostningsregister**.</span><span class="sxs-lookup"><span data-stu-id="bc001-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="bc001-121">Dette gør det muligt at spore kilden til omkostningsposter.</span><span class="sxs-lookup"><span data-stu-id="bc001-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bc001-122">Se også</span><span class="sxs-lookup"><span data-stu-id="bc001-122">See Also</span></span>  
 <span data-ttu-id="bc001-123">[Kriterier for overførsel af finansposter til omkostningsposter.](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="bc001-123">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="bc001-124">[Automatisk overførsel og kombinerede poster](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="bc001-124">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
 <span data-ttu-id="bc001-125">[Resultater af overførslen](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="bc001-125">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 <span data-ttu-id="bc001-126">[Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="bc001-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="bc001-127">Definition af forholdet mellem omkostningstyper og finanskonti.</span><span class="sxs-lookup"><span data-stu-id="bc001-127">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

