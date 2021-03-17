---
title: Sådan slettes omkostningsbudgetposter | Microsoft Docs
description: Du kan bruge kørslen Slet omkostningsbudgetposter til at annullere omkostningsbudgetposter fra omkostningsbudgetregistret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b4c81aa62f3548819db3451130c49fd11984b33a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387370"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="dfe90-103">Slet omkostningsbudgetposter</span><span class="sxs-lookup"><span data-stu-id="dfe90-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="dfe90-104">Du kan bruge kørslen **Slet omkostningsbudgetposter** til at annullere omkostningsbudgetposter fra omkostningsbudgetregistret.</span><span class="sxs-lookup"><span data-stu-id="dfe90-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="dfe90-105">Du kan ikke slette en enkelt post eller flere poster i midten af listen over journalposter i, for at undgå eventuelle mellemrum i omkostningsbudgetposter og omkostningsregisterposter.</span><span class="sxs-lookup"><span data-stu-id="dfe90-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="dfe90-106">Sådan slettes en omkostningsbudgetpost</span><span class="sxs-lookup"><span data-stu-id="dfe90-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="dfe90-107">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet omkostningsbudgetposter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="dfe90-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="dfe90-108">Feltet **Til-journalnr.**</span><span class="sxs-lookup"><span data-stu-id="dfe90-108">The **To Register No.**</span></span> <span data-ttu-id="dfe90-109">indeholder nummeret på den sidste journalpost og kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="dfe90-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="dfe90-110">Du kan bruge feltet **Fra-journalnr.**</span><span class="sxs-lookup"><span data-stu-id="dfe90-110">You can use the **From Register No.**</span></span> <span data-ttu-id="dfe90-111">til at vælge et journalpostnummer, hvorfra sletningen skal begynde.</span><span class="sxs-lookup"><span data-stu-id="dfe90-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="dfe90-112">Tryk på knappen **OK** for at slette de valgte omkostningsbudgetposter.</span><span class="sxs-lookup"><span data-stu-id="dfe90-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="dfe90-113">Du kan lukke registrerposter for at undgå en utilsigtet sletning af omkostningsbudgetposter ved at markere linjerne som **Lukket** i feltet **Lukket** på siden **Omkostningsbudgetregistre**.</span><span class="sxs-lookup"><span data-stu-id="dfe90-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dfe90-114">Se også</span><span class="sxs-lookup"><span data-stu-id="dfe90-114">See Also</span></span>  
<span data-ttu-id="dfe90-115">[Regnskab for omkostninger](finance-manage-cost-accounting.md)
[Oprette omkostningsbudgetter](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="dfe90-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="dfe90-116">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dfe90-116">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]