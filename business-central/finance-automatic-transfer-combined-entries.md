---
title: "Automatisk overførsel og kombinerede poster | Microsoft Docs"
description: "I omkostningsregnskab kan du overføre finansposter til en pristype ved hjælp af kombineret bogføring. Du kan angive, om en pristype modtager samlede poster i feltet **Saml poster** i pristypedefinitionen. Den følgende tabel beskriver de forskellige indstillinger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d33fa549f48731c49734e7ecaf65b461c375ec90
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="98ace-105">Automatisk overførsel og kombinerede poster</span><span class="sxs-lookup"><span data-stu-id="98ace-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="98ace-106">I omkostningsregnskab kan du overføre finansposter til en pristype ved hjælp af kombineret bogføring.</span><span class="sxs-lookup"><span data-stu-id="98ace-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="98ace-107">Du kan angive, om en pristype modtager samlede poster i feltet **Saml poster** i pristypedefinitionen.</span><span class="sxs-lookup"><span data-stu-id="98ace-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="98ace-108">Den følgende tabel beskriver de forskellige indstillinger.</span><span class="sxs-lookup"><span data-stu-id="98ace-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="98ace-109">Saml poster</span><span class="sxs-lookup"><span data-stu-id="98ace-109">Combine entries</span></span>|<span data-ttu-id="98ace-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="98ace-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="98ace-111">Ingen</span><span class="sxs-lookup"><span data-stu-id="98ace-111">None</span></span>|<span data-ttu-id="98ace-112">Alle finansposter overføres individuelt til den tilsvarende pristype.</span><span class="sxs-lookup"><span data-stu-id="98ace-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="98ace-113">DAG</span><span class="sxs-lookup"><span data-stu-id="98ace-113">Day</span></span>|<span data-ttu-id="98ace-114">Finansposter med den samme bogføringsdato overføres som én post til den tilsvarende pristype.</span><span class="sxs-lookup"><span data-stu-id="98ace-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="98ace-115">Måned</span><span class="sxs-lookup"><span data-stu-id="98ace-115">Month</span></span>|<span data-ttu-id="98ace-116">Alle finansposter i den samme kalendermåned overføres som én post til den tilsvarende pristype.</span><span class="sxs-lookup"><span data-stu-id="98ace-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="98ace-117">Hvis du har markeret afkrydsningsfeltet **Automatisk overførsel fra finans** i vinduet **Konfiguration af omkostningsregnskab**, opdaterer [!INCLUDE[d365fin](includes/d365fin_md.md)] omkostningsregnskabet efter hver bogføring i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="98ace-117">If you have selected the **Auto Transfer from G/L** check box in the **Cost Accounting Setup** window, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="98ace-118">Kombinerede poster er ikke mulige.</span><span class="sxs-lookup"><span data-stu-id="98ace-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="98ace-119">Se også</span><span class="sxs-lookup"><span data-stu-id="98ace-119">See Also</span></span>  
 <span data-ttu-id="98ace-120">[Overføre finansposter til omkostningsposter](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="98ace-120">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="98ace-121">[Kriterier for overførsel af finansposter til omkostningsposter.](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="98ace-121">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="98ace-122">[Resultater af overførslen](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="98ace-122">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 [<span data-ttu-id="98ace-123">Overførsel og bogføring af omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="98ace-123">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  
 <span data-ttu-id="98ace-124">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="98ace-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

