---
title: Resultaterne af overførslen | Microsoft Docs
description: Dette emne beskriver, hvad der sker, når du har overført finansposter til omkostningsposter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 590c1501f9da2c7c343b5c2f3617df873fcd3b7a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242487"
---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="7eff3-103">Resultater af overførsel af finansposter til omkostningsposter.</span><span class="sxs-lookup"><span data-stu-id="7eff3-103">Results of Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="7eff3-104">Under overførslen af regnskabsposter til omkostningsposter opretter [!INCLUDE[d365fin](includes/d365fin_md.md)] forbindelser i posterne i tabellen **Finanspost**, tabellen **Omkostningspost** og tabellen **Omkostningsregister** for at gøre det muligt at spore forbindelserne mellem omkostningsposter og regnskabsposter.</span><span class="sxs-lookup"><span data-stu-id="7eff3-104">During the transfer of general ledger entries to cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates connections in the entries in the **G/L Entry** table, the **Cost Entry** table, and the **Cost Register** table to make it possible to trace the connections between cost entries and general ledger entries.</span></span>  

## <a name="general-ledger-entries"></a><span data-ttu-id="7eff3-105">Finansposter</span><span class="sxs-lookup"><span data-stu-id="7eff3-105">General Ledger Entries</span></span>  
<span data-ttu-id="7eff3-106">For hver regnskabspost, der overføres til omkostningsregnskab, udfylder [!INCLUDE[d365fin](includes/d365fin_md.md)] omkostningsfeltet **Løbenr.**.</span><span class="sxs-lookup"><span data-stu-id="7eff3-106">For each general ledger entry that is transferred to cost accounting, [!INCLUDE[d365fin](includes/d365fin_md.md)] fills the cost **Entry No.** field.</span></span>  

## <a name="cost-entries"></a><span data-ttu-id="7eff3-107">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="7eff3-107">Cost Entries</span></span>  
<span data-ttu-id="7eff3-108">For hver omkostningspost gemmer [!INCLUDE[d365fin](includes/d365fin_md.md)] løbenummeret på den tilsvarende regnskabspost i feltet **Finansløbenr.** i tabellen **Omkostningspost**.</span><span class="sxs-lookup"><span data-stu-id="7eff3-108">For each cost entry, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the corresponding general ledger entry in the **G/L Entry No.** field in the **Cost Entry** table.</span></span>  

<span data-ttu-id="7eff3-109">For samlede omkostningsposter gemmer [!INCLUDE[d365fin](includes/d365fin_md.md)] løbenummer på den sidste regnskabspost, som er posten med det højeste løbenummer.</span><span class="sxs-lookup"><span data-stu-id="7eff3-109">For combined cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the last general ledger entry, which is the entry with the highest entry number.</span></span>  

<span data-ttu-id="7eff3-110">Feltet **Finanskonto** i tabellen **Omkostningspost** indeholder nummeret på den finanskonto, som omkostningsposten stammer fra.</span><span class="sxs-lookup"><span data-stu-id="7eff3-110">The **G/L Account** field in the **Cost Entry** table contains the number of the general ledger account that the cost entry came from.</span></span>  

<span data-ttu-id="7eff3-111">For enkelte omkostningsposter overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] bogføringsteksten fra regnskabsposten til tekstfeltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7eff3-111">For single cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfers the posting text from the general ledger entry to the **Description** text field.</span></span> <span data-ttu-id="7eff3-112">For kombinerede poster viser tekstfeltet, at disse poster er overfører som kombinerede poster.</span><span class="sxs-lookup"><span data-stu-id="7eff3-112">For combined entries, the text field shows these entries are transferred as combined entries.</span></span> <span data-ttu-id="7eff3-113">For eksempel kan teksten for en kombineret post for oktober 2013 være **Kombinerede poster, oktober 2013**.</span><span class="sxs-lookup"><span data-stu-id="7eff3-113">For example, for a combined entry for the month of October in 2013, the text can be **Combined Entries, October 2013**.</span></span>  

## <a name="cost-register"></a><span data-ttu-id="7eff3-114">Omkostningsregister</span><span class="sxs-lookup"><span data-stu-id="7eff3-114">Cost Register</span></span>  
<span data-ttu-id="7eff3-115">I tabellen **Omkostningsregister** opretter [!INCLUDE[d365fin](includes/d365fin_md.md)] en post med kildeoverførsel fra regnskabet.</span><span class="sxs-lookup"><span data-stu-id="7eff3-115">In the **Cost Register** table, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates an entry with the source transfer from general ledger.</span></span> <span data-ttu-id="7eff3-116">Posten registrerer det første og sidste løbenummer for de finansposter, der overføres, foruden første og sidste postnummer på de omkostningsposter, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="7eff3-116">The entry records the first and last entry numbers of the general ledger entries that are transferred, in addition to the first and last entry numbers of the cost entries that are created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7eff3-117">Se også</span><span class="sxs-lookup"><span data-stu-id="7eff3-117">See Also</span></span>  
[<span data-ttu-id="7eff3-118">Overførsel og bogføring af omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="7eff3-118">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)   
