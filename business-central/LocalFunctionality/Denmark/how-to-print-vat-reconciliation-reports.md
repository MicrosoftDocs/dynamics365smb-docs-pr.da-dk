---
title: Sådan udskrives en rapport til afstemning af moms | Microsoft Docs
description: I Business Central kan du bruge rapporten Momsafstemning til at få vist en oversigt over finanskonti med deres grundlæggende beløb og momsbeløb. Disse beløb er grupperet efter moms-type for at hjælpe med afstemningen for afregning af moms.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c3b5e4a93c3df32cebc497250b91fa3dd05d83b5
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782241"
---
# <a name="print-vat-reconciliation-reports"></a><span data-ttu-id="0c51f-104">Udskrive rapporter til afstemning af moms</span><span class="sxs-lookup"><span data-stu-id="0c51f-104">Print VAT Reconciliation Reports</span></span>
<span data-ttu-id="0c51f-105">I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan du bruge rapporten **Momsafstemning** til at få vist en oversigt over finanskonti med deres grundlæggende beløb og momsbeløb.</span><span class="sxs-lookup"><span data-stu-id="0c51f-105">In [!INCLUDE[prod_short](../../includes/prod_short.md)], you can use the **VAT Reconciliation** report to view a list of general ledger accounts with their base amounts and VAT amounts.</span></span> <span data-ttu-id="0c51f-106">Disse beløb er grupperet efter moms-type for at hjælpe med afstemningen for afregning af moms.</span><span class="sxs-lookup"><span data-stu-id="0c51f-106">These amounts are grouped by VAT type to help with VAT settlement reconciliation.</span></span>  

### <a name="to-print-a-vat-reconciliation-report"></a><span data-ttu-id="0c51f-107">Sådan udskrives en momsafstemningsrapport</span><span class="sxs-lookup"><span data-stu-id="0c51f-107">To print a VAT reconciliation report</span></span>  

1.  <span data-ttu-id="0c51f-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), åbn **Momsafstemning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0c51f-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Reconciliation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0c51f-109">I oversigtspanelet **Indstillinger** skal du udfylde felterne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="0c51f-109">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="0c51f-110">Felt</span><span class="sxs-lookup"><span data-stu-id="0c51f-110">Field</span></span>|<span data-ttu-id="0c51f-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0c51f-111">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="0c51f-112">**Vis detaljer**</span><span class="sxs-lookup"><span data-stu-id="0c51f-112">**Show Details**</span></span>|<span data-ttu-id="0c51f-113">Vælg for at udskrive alle transaktionsbeløb i rapporten.</span><span class="sxs-lookup"><span data-stu-id="0c51f-113">Select to print all transaction amounts in the report.</span></span><br /><br /> <span data-ttu-id="0c51f-114">Hvis du ikke markerer feltet, udskrives en enkelt akkumuleret linje for hver finanskonto.</span><span class="sxs-lookup"><span data-stu-id="0c51f-114">If you do not select this field, a single cumulative line is printed for each general ledger account.</span></span>|  
    |<span data-ttu-id="0c51f-115">**Vis transaktioner uden moms**</span><span class="sxs-lookup"><span data-stu-id="0c51f-115">**Show Transactions without VAT**</span></span>|<span data-ttu-id="0c51f-116">Vælg for at udskrive en linje for hver finanskonto, som transaktioner bogføres på.</span><span class="sxs-lookup"><span data-stu-id="0c51f-116">Select to print a line for each general ledger account that transactions are posted to.</span></span> <span data-ttu-id="0c51f-117">Du kan bruge denne indstilling for både enkelte konti og flere konti.</span><span class="sxs-lookup"><span data-stu-id="0c51f-117">You can use this option for both single accounts and multiple accounts.</span></span><br /><br /> <span data-ttu-id="0c51f-118">Standardværdien er **Nej**.</span><span class="sxs-lookup"><span data-stu-id="0c51f-118">The default is **No**.</span></span> <span data-ttu-id="0c51f-119">Rapporten indeholder kun de transaktioner, der omfatter momsposter.</span><span class="sxs-lookup"><span data-stu-id="0c51f-119">The report includes only those transactions that include VAT entries.</span></span> <span data-ttu-id="0c51f-120">Hvis du markerer dette felt, medtager rapporten alle posteringer.</span><span class="sxs-lookup"><span data-stu-id="0c51f-120">If you select this field, the report includes all transactions.</span></span>|  

3.  <span data-ttu-id="0c51f-121">I oversigtspanelet **Finanspost** skal du vælge de relevante filtre.</span><span class="sxs-lookup"><span data-stu-id="0c51f-121">On the **G/L Entry** FastTab, select the appropriate filters.</span></span>  
4.  <span data-ttu-id="0c51f-122">Vælg **Udskriv** for at udskrive rapporten, eller vælg **Vis udskrift** for at se den på skærmen.</span><span class="sxs-lookup"><span data-stu-id="0c51f-122">Choose the **Print** button to print the report or choose the **Preview** button to view it on the screen.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0c51f-123">Se også</span><span class="sxs-lookup"><span data-stu-id="0c51f-123">See Also</span></span>  
 [<span data-ttu-id="0c51f-124">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="0c51f-124">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]