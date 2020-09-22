---
title: Sådan slettes omkostningsbudgetposter | Microsoft Docs
description: Du kan bruge kørslen Slet omkostningsbudgetposter til at annullere omkostningsbudgetposter fra omkostningsbudgetregistret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d26bba0cf0bd273d981e7bc83f06a7bd53216637
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784178"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="21cca-103">Slet omkostningsbudgetposter</span><span class="sxs-lookup"><span data-stu-id="21cca-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="21cca-104">Du kan bruge kørslen **Slet omkostningsbudgetposter** til at annullere omkostningsbudgetposter fra omkostningsbudgetregistret.</span><span class="sxs-lookup"><span data-stu-id="21cca-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="21cca-105">Du kan ikke slette en enkelt post eller flere poster i midten af listen over journalposter i, for at undgå eventuelle mellemrum i omkostningsbudgetposter og omkostningsregisterposter.</span><span class="sxs-lookup"><span data-stu-id="21cca-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="21cca-106">Sådan slettes en omkostningsbudgetpost</span><span class="sxs-lookup"><span data-stu-id="21cca-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="21cca-107">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet omkostningsbudgetposter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="21cca-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="21cca-108">Feltet **Til-journalnr.**</span><span class="sxs-lookup"><span data-stu-id="21cca-108">The **To Register No.**</span></span> <span data-ttu-id="21cca-109">indeholder nummeret på den sidste journalpost og kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="21cca-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="21cca-110">Du kan bruge feltet **Fra-journalnr.**</span><span class="sxs-lookup"><span data-stu-id="21cca-110">You can use the **From Register No.**</span></span> <span data-ttu-id="21cca-111">til at vælge et journalpostnummer, hvorfra sletningen skal begynde.</span><span class="sxs-lookup"><span data-stu-id="21cca-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="21cca-112">Tryk på knappen **OK** for at slette de valgte omkostningsbudgetposter.</span><span class="sxs-lookup"><span data-stu-id="21cca-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="21cca-113">Du kan lukke registrerposter for at undgå en utilsigtet sletning af omkostningsbudgetposter ved at markere linjerne som **Lukket** i feltet **Lukket** på siden **Omkostningsbudgetregistre**.</span><span class="sxs-lookup"><span data-stu-id="21cca-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="21cca-114">Se også</span><span class="sxs-lookup"><span data-stu-id="21cca-114">See Also</span></span>  
<span data-ttu-id="21cca-115">[Regnskab for omkostninger](finance-manage-cost-accounting.md)
[Oprette omkostningsbudgetter](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="21cca-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="21cca-116">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="21cca-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
