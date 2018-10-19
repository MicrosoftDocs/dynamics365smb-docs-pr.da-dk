---
title: "Importere løntransaktioner | Microsoft Docs"
description: "For at administrere løn skal du importere og bogføre finanstransaktioner fra din lønningslisteudbyder i finansregnskabet ved hjælp af lønudvidelsen, f.eks. Ceridian eller Quickbooks."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: fbe6a61cb48a4c26ff3fc15eb0dd61c002a59092
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="import-payroll-transactions"></a><span data-ttu-id="b0ac7-103">Importér løntransaktioner</span><span class="sxs-lookup"><span data-stu-id="b0ac7-103">Import Payroll Transactions</span></span>
<span data-ttu-id="b0ac7-104">For at tage højde for lønbetalinger og relaterede transaktioner, skal du importere og bogføre finansielle transaktioner, der er foretaget af din lønningssystemudbyder i finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="b0ac7-105">For at gøre dette skal du først importere en fil, som du modtager fra lønningsystemudbyderen, i vinduet **Finanskladde**.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="b0ac7-106">Derefter knytter du de eksterne konti i lønningslistefilen til de relevante finanskonti.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="b0ac7-107">Til sidst skal du bogføre lønningstransaktionerne i overensstemmelse med kontotilknytningen.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b0ac7-108">Hvis du vil bruge denne funktion, skal en udvidelse til import af løn være installeret og aktiveret.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="b0ac7-109">Importudvidelserne Ceridian løn og Quickbooks-lønfil er forudinstalleret i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b0ac7-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="b0ac7-110">Du kan finde flere oplysninger i [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="b0ac7-110">For more information, see [Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="b0ac7-111">Sådan importereres en lønningslistefil</span><span class="sxs-lookup"><span data-stu-id="b0ac7-111">To import a payroll file</span></span>
1. <span data-ttu-id="b0ac7-112">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="b0ac7-113">I den relevante finanskladdekørsel skal du vælge handlingen **Importér løntransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="b0ac7-114">En assisteret opsætningsvejledning åbnes.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="b0ac7-115">Udfør trinnene i vinduet **Importér løntransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-115">Follow the steps in the **Import Payroll Transactions** window.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="b0ac7-116">I trinnet for tilknytning af de eksterne lønposter til dine finanskonti vil de tilknytninger, du foretager, blive husket, næste gang de samme poster importeres.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="b0ac7-117">Derved sparer du tid, da du ikke behøver at udfylde feltet **Kontonr.** manuelt i finanskladden, hver gang du har indlæst gentagne løntransaktioner.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-117">This will save you time as you do not have to manually fill in the **Account No.** field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="b0ac7-118">Når du vælger knappen **OK** i den assisterede opsætningsvejledning, udfyldes vinduet **Finanskladde** med linjer, der repræsenterer de transaktioner, som lønningslistefilen indeholder, og de relevante konti udfyldt på forhånd i **Finanskonto**-felterne i overensstemmelse med de tilknytninger, du har foretaget i vejledningen.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-118">When you choose the **OK** button in the assisted setup guide, the **General Journal** window is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="b0ac7-119">Rediger eller bogfør kladdelinjerne som for alle andre finanstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="b0ac7-119">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="b0ac7-120">Du kan finde flere oplysninger i [Bogføre transaktioner direkte i finansregnskabet](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="b0ac7-120">For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="b0ac7-121">Se også</span><span class="sxs-lookup"><span data-stu-id="b0ac7-121">See Also</span></span>
[<span data-ttu-id="b0ac7-122">Finans</span><span class="sxs-lookup"><span data-stu-id="b0ac7-122">Finance</span></span>](finance.md)  
<span data-ttu-id="b0ac7-123">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="b0ac7-123">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="b0ac7-124">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="b0ac7-124">Working with General Journals</span></span>](ui-work-general-journals.md)  

