---
title: "Resultaterne af overførslen | Microsoft Docs"
description: "Dette emne beskriver, hvad der sker, når du har overført finansposter til omkostningsposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d479727b8d0cbb4b4ec9f127136f4e0578b8afb7
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="4fa67-103">Resultater af overførsel af finansposter til omkostningsposter.</span><span class="sxs-lookup"><span data-stu-id="4fa67-103">Results of Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="4fa67-104">Under overførslen af regnskabsposter til omkostningsposter opretter [!INCLUDE[d365fin](includes/d365fin_md.md)] forbindelser i posterne i tabellen **Finanspost**, tabellen **Omkostningspost** og tabellen **Omkostningsregister** for at gøre det muligt at spore forbindelserne mellem omkostningsposter og regnskabsposter.</span><span class="sxs-lookup"><span data-stu-id="4fa67-104">During the transfer of general ledger entries to cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates connections in the entries in the **G/L Entry** table, the **Cost Entry** table, and the **Cost Register** table to make it possible to trace the connections between cost entries and general ledger entries.</span></span>  

## <a name="general-ledger-entries"></a><span data-ttu-id="4fa67-105">Finansposter</span><span class="sxs-lookup"><span data-stu-id="4fa67-105">General Ledger Entries</span></span>  
<span data-ttu-id="4fa67-106">For hver regnskabspost, der overføres til omkostningsregnskab, udfylder [!INCLUDE[d365fin](includes/d365fin_md.md)] omkostningsfeltet **Løbenr.**.</span><span class="sxs-lookup"><span data-stu-id="4fa67-106">For each general ledger entry that is transferred to cost accounting, [!INCLUDE[d365fin](includes/d365fin_md.md)] fills the cost **Entry No.** field.</span></span>  

## <a name="cost-entries"></a><span data-ttu-id="4fa67-107">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="4fa67-107">Cost Entries</span></span>  
<span data-ttu-id="4fa67-108">For hver omkostningspost gemmer [!INCLUDE[d365fin](includes/d365fin_md.md)] løbenummeret på den tilsvarende regnskabspost i feltet **Finansløbenr.** i tabellen **Omkostningspost**.</span><span class="sxs-lookup"><span data-stu-id="4fa67-108">For each cost entry, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the corresponding general ledger entry in the **G/L Entry No.** field in the **Cost Entry** table.</span></span>  

<span data-ttu-id="4fa67-109">For samlede omkostningsposter gemmer [!INCLUDE[d365fin](includes/d365fin_md.md)] løbenummer på den sidste regnskabspost, som er posten med det højeste løbenummer.</span><span class="sxs-lookup"><span data-stu-id="4fa67-109">For combined cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the last general ledger entry, which is the entry with the highest entry number.</span></span>  

<span data-ttu-id="4fa67-110">Feltet **Finanskonto** i tabellen **Omkostningspost** indeholder nummeret på den finanskonto, som omkostningsposten stammer fra.</span><span class="sxs-lookup"><span data-stu-id="4fa67-110">The **G/L Account** field in the **Cost Entry** table contains the number of the general ledger account that the cost entry came from.</span></span>  

<span data-ttu-id="4fa67-111">For enkelte omkostningsposter overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] bogføringsteksten fra regnskabsposten til tekstfeltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="4fa67-111">For single cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfers the posting text from the general ledger entry to the **Description** text field.</span></span> <span data-ttu-id="4fa67-112">For kombinerede poster viser tekstfeltet, at disse poster er overfører som kombinerede poster.</span><span class="sxs-lookup"><span data-stu-id="4fa67-112">For combined entries, the text field shows these entries are transferred as combined entries.</span></span> <span data-ttu-id="4fa67-113">For eksempel kan teksten for en kombineret post for oktober 2013 være **Kombinerede poster, oktober 2013**.</span><span class="sxs-lookup"><span data-stu-id="4fa67-113">For example, for a combined entry for the month of October in 2013, the text can be **Combined Entries, October 2013**.</span></span>  

## <a name="cost-register"></a><span data-ttu-id="4fa67-114">Omkostningsregister</span><span class="sxs-lookup"><span data-stu-id="4fa67-114">Cost Register</span></span>  
<span data-ttu-id="4fa67-115">I tabellen **Omkostningsregister** opretter [!INCLUDE[d365fin](includes/d365fin_md.md)] en post med kildeoverførsel fra regnskabet.</span><span class="sxs-lookup"><span data-stu-id="4fa67-115">In the **Cost Register** table, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates an entry with the source transfer from general ledger.</span></span> <span data-ttu-id="4fa67-116">Posten registrerer det første og sidste løbenummer for de finansposter, der overføres, foruden første og sidste postnummer på de omkostningsposter, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="4fa67-116">The entry records the first and last entry numbers of the general ledger entries that are transferred, in addition to the first and last entry numbers of the cost entries that are created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4fa67-117">Se også</span><span class="sxs-lookup"><span data-stu-id="4fa67-117">See Also</span></span>  
<span data-ttu-id="4fa67-118">[Overføre finansposter til omkostningsposter](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="4fa67-118">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
<span data-ttu-id="4fa67-119">[Kriterier for overførsel af finansposter til omkostningsposter](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="4fa67-119">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
<span data-ttu-id="4fa67-120">[Automatisk overførsel og kombinerede poster](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="4fa67-120">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
[<span data-ttu-id="4fa67-121">Overførsel og bogføring af omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="4fa67-121">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  

