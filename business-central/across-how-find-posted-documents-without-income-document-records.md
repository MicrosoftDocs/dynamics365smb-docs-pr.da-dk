---
title: Søge efter dokumenter uden vedhæftede filer | Microsoft Docs
Description: Du kan søge efter finansposter for bogførte købs- og salgsdokumenter, der ikke har indgående elektroniske dokumenter, f.eks. importerede fakturaer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 79504010d6bb4f2afb0f09f866991dd76f6e35b5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "923690"
---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="1ffb5-103">Finde bogførte dokumenter uden indgående dokumentposter</span><span class="sxs-lookup"><span data-stu-id="1ffb5-103">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="1ffb5-104">Fra på siderne **Kontoplan** og **Finansposter** kan du bruge en søgefunktionen til at finde finansposter for bogførte og købs- og salgsdokumenter, som ikke har indgående dokument poster og derefter knytte centralt til eksisterende poster eller oprette nye med vedhæftede dokument filer.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-104">From the **Chart of Accounts** and **General Ledger Entries** pages, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="1ffb5-105">Sådan findes bogførte dokumenter uden indgående dokumentposter</span><span class="sxs-lookup"><span data-stu-id="1ffb5-105">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="1ffb5-106">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoplan**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="1ffb5-107">Vælg en linje for en finanskonto, for hvis finansposter du vil se bogførte købs- og salgsdokumenter uden indgående dokumentposter, og vælg derefter handlingen **Bogførte dokumenter uden indgående bilag**.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-107">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="1ffb5-108">Alternativt kan du vælge handlingen **Poster**.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-108">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="1ffb5-109">På siden **Finansposter** skal du vælge handlingen **Bogførte dokumenter uden indgående dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-109">On the **General Ledger Entries** page, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="1ffb5-110">Siden **Bogførte dokumenter uden indgående dokument** åbnes og viser bogførte købs- åbnes og salgsdokumenter uden indgående dokumentposter repræsenteret af finansposter på den finanskonto, som du åbnede siden for.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-110">The **Posted Documents without Incoming Document** page opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the page for.</span></span> <span data-ttu-id="1ffb5-111">Siden kan vise højst 1000 linjer.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-111">The page can show a maximum of 1000 lines.</span></span> <span data-ttu-id="1ffb5-112">Som standard indeholder feltet **Datofilter** derfor et filter, der begrænser linjerne til poster med bogføringsdatoer fra begyndelsen af den aktuelle regnskabsperiode til arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-112">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="1ffb5-113">Sådan knyttes fundne dokumenter med eksisterende indgående bilagsposter</span><span class="sxs-lookup"><span data-stu-id="1ffb5-113">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="1ffb5-114">På siden **Bogførte dokumenter uden indgående dokument** skal du vælge linjen for et bogført dokument, du vil knytte til en eksisterende indgående dokumentpost og derefter vælge handlingen **Vælg indgående bilag**.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-114">On the **Posted Documents without Incoming Document** page, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="1ffb5-115">Vælg den indgående dokumentpost, som du vil knytte til det bogførte fundne dokument, på siden **Indgående bilag**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-115">On the **Incoming Documents** page, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="1ffb5-116">På siden **Bogførte dokumenter uden indgående dokument** er den valgte indgående dokumentpost nu tilknyttet det bogførte dokument, som du kan se i faktaboksen **Indgående bilagsfiler**.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-116">On the **Posted Documents without Incoming Document** page, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="1ffb5-117">Hvis der ikke findes en relevant indgående dokument post på siden **Indgående bilag** kan du oprette den.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-117">If a relevant incoming document record does not exist on the **Incoming Documents** page, then you can create it.</span></span> <span data-ttu-id="1ffb5-118">Du kan finde flere oplysninger under [Oprette indgående dokumentposter](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="1ffb5-118">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1ffb5-119">Se også</span><span class="sxs-lookup"><span data-stu-id="1ffb5-119">See Also</span></span>
[<span data-ttu-id="1ffb5-120">Behandle indgående bilag</span><span class="sxs-lookup"><span data-stu-id="1ffb5-120">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="1ffb5-121">Indgående bilag</span><span class="sxs-lookup"><span data-stu-id="1ffb5-121">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="1ffb5-122">Køb</span><span class="sxs-lookup"><span data-stu-id="1ffb5-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="1ffb5-123">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1ffb5-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
