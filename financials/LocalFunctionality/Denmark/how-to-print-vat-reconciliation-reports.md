---
title: "Sådan udskrives en rapport til afstemning af moms | Microsoft Docs"
description: "I Dynamics 365 kan du bruge rapporten **Momsafstemning** til at få vist en oversigt over finanskonti med deres grundlæggende beløb og momsbeløb. Disse beløb er grupperet efter moms-type for at hjælpe med afstemningen for afregning af moms."
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
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 027d521263ee0da95341abc92505d71aee7bb074
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-print-vat-reconciliation-reports"></a><span data-ttu-id="e1abe-104">Fremgangsmåde: Udskrive en rapport til afstemning af moms</span><span class="sxs-lookup"><span data-stu-id="e1abe-104">How to: Print VAT Reconciliation Reports</span></span>
<span data-ttu-id="e1abe-105">I [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kan du bruge rapporten **Momsafstemning** til at få vist en oversigt over finanskonti med deres grundlæggende beløb og momsbeløb.</span><span class="sxs-lookup"><span data-stu-id="e1abe-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can use the **VAT Reconciliation** report to view a list of general ledger accounts with their base amounts and VAT amounts.</span></span> <span data-ttu-id="e1abe-106">Disse beløb er grupperet efter moms-type for at hjælpe med afstemningen for afregning af moms.</span><span class="sxs-lookup"><span data-stu-id="e1abe-106">These amounts are grouped by VAT type to help with VAT settlement reconciliation.</span></span>  

### <a name="to-print-a-vat-reconciliation-report"></a><span data-ttu-id="e1abe-107">Sådan udskrives en momsafstemningsrapport</span><span class="sxs-lookup"><span data-stu-id="e1abe-107">To print a VAT reconciliation report</span></span>  

1.  <span data-ttu-id="e1abe-108">Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Momsafstemning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e1abe-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **VAT Reconciliation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e1abe-109">I oversigtspanelet **Indstillinger** skal du udfylde felterne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="e1abe-109">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="e1abe-110">Felt</span><span class="sxs-lookup"><span data-stu-id="e1abe-110">Field</span></span>|<span data-ttu-id="e1abe-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e1abe-111">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="e1abe-112">**Vis detaljer**</span><span class="sxs-lookup"><span data-stu-id="e1abe-112">**Show Details**</span></span>|<span data-ttu-id="e1abe-113">Vælg for at udskrive alle transaktionsbeløb i rapporten.</span><span class="sxs-lookup"><span data-stu-id="e1abe-113">Select to print all transaction amounts in the report.</span></span><br /><br /> <span data-ttu-id="e1abe-114">Hvis du ikke markerer feltet, udskrives en enkelt akkumuleret linje for hver finanskonto.</span><span class="sxs-lookup"><span data-stu-id="e1abe-114">If you do not select this field, a single cumulative line is printed for each general ledger account.</span></span>|  
    |<span data-ttu-id="e1abe-115">**Vis transaktioner uden moms**</span><span class="sxs-lookup"><span data-stu-id="e1abe-115">**Show Transactions without VAT**</span></span>|<span data-ttu-id="e1abe-116">Vælg for at udskrive en linje for hver finanskonto, som transaktioner bogføres på.</span><span class="sxs-lookup"><span data-stu-id="e1abe-116">Select to print a line for each general ledger account that transactions are posted to.</span></span> <span data-ttu-id="e1abe-117">Du kan bruge denne indstilling for både enkelte konti og flere konti.</span><span class="sxs-lookup"><span data-stu-id="e1abe-117">You can use this option for both single accounts and multiple accounts.</span></span><br /><br /> <span data-ttu-id="e1abe-118">Standardværdien er **Nej**.</span><span class="sxs-lookup"><span data-stu-id="e1abe-118">The default is **No**.</span></span> <span data-ttu-id="e1abe-119">Rapporten indeholder kun de transaktioner, der omfatter momsposter.</span><span class="sxs-lookup"><span data-stu-id="e1abe-119">The report includes only those transactions that include VAT entries.</span></span> <span data-ttu-id="e1abe-120">Hvis du markerer dette felt, medtager rapporten alle posteringer.</span><span class="sxs-lookup"><span data-stu-id="e1abe-120">If you select this field, the report includes all transactions.</span></span>|  

3.  <span data-ttu-id="e1abe-121">I oversigtspanelet **Finanspost** skal du vælge de relevante filtre.</span><span class="sxs-lookup"><span data-stu-id="e1abe-121">On the **G/L Entry** FastTab, select the appropriate filters.</span></span>  
4.  <span data-ttu-id="e1abe-122">Vælg **Udskriv** for at udskrive rapporten, eller vælg **Vis udskrift** for at se den på skærmen.</span><span class="sxs-lookup"><span data-stu-id="e1abe-122">Choose the **Print** button to print the report or choose the **Preview** button to view it on the screen.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e1abe-123">Se også</span><span class="sxs-lookup"><span data-stu-id="e1abe-123">See Also</span></span>  
 [<span data-ttu-id="e1abe-124">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="e1abe-124">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  

