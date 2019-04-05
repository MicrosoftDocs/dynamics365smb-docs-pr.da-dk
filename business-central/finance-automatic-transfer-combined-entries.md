---
title: Automatisk overførsel og kombinerede poster | Microsoft Docs
description: I omkostningsregnskab kan du overføre finansposter til en pristype ved hjælp af kombineret bogføring. Du kan angive, om en pristype modtager samlede poster i feltet **Saml poster** i pristypedefinitionen. Den følgende tabel beskriver de forskellige indstillinger.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 6f58e569bea6a42a9ee695095ce308e7a69e2a8d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792177"
---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="05b29-105">Automatisk overførsel og kombinerede poster</span><span class="sxs-lookup"><span data-stu-id="05b29-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="05b29-106">I omkostningsregnskab kan du overføre finansposter til en pristype ved hjælp af kombineret bogføring.</span><span class="sxs-lookup"><span data-stu-id="05b29-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="05b29-107">Du kan angive, om en pristype modtager samlede poster i feltet **Saml poster** i pristypedefinitionen.</span><span class="sxs-lookup"><span data-stu-id="05b29-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="05b29-108">Den følgende tabel beskriver de forskellige indstillinger.</span><span class="sxs-lookup"><span data-stu-id="05b29-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="05b29-109">Saml poster</span><span class="sxs-lookup"><span data-stu-id="05b29-109">Combine entries</span></span>|<span data-ttu-id="05b29-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="05b29-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="05b29-111">Ingen</span><span class="sxs-lookup"><span data-stu-id="05b29-111">None</span></span>|<span data-ttu-id="05b29-112">Alle finansposter overføres individuelt til den tilsvarende pristype.</span><span class="sxs-lookup"><span data-stu-id="05b29-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="05b29-113">DAG</span><span class="sxs-lookup"><span data-stu-id="05b29-113">Day</span></span>|<span data-ttu-id="05b29-114">Finansposter med den samme bogføringsdato overføres som én post til den tilsvarende pristype.</span><span class="sxs-lookup"><span data-stu-id="05b29-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="05b29-115">Måned</span><span class="sxs-lookup"><span data-stu-id="05b29-115">Month</span></span>|<span data-ttu-id="05b29-116">Alle finansposter i den samme kalendermåned overføres som én post til den tilsvarende pristype.</span><span class="sxs-lookup"><span data-stu-id="05b29-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="05b29-117">Hvis du har markeret afkrydsningsfeltet **Automatisk overførsel fra finans** på siden **Konfiguration af omkostningsregnskab**, opdaterer [!INCLUDE[d365fin](includes/d365fin_md.md)] omkostningsregnskabet efter hver bogføring i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="05b29-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="05b29-118">Kombinerede poster er ikke mulige.</span><span class="sxs-lookup"><span data-stu-id="05b29-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="05b29-119">Se også</span><span class="sxs-lookup"><span data-stu-id="05b29-119">See Also</span></span>  
 <span data-ttu-id="05b29-120">[Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="05b29-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="05b29-121">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="05b29-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
