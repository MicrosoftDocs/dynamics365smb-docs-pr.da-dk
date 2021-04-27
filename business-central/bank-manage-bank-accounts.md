---
title: Håndtere bankkonti | Microsoft Docs
description: Du skal afstemme bankposter regelmæssigt med de relaterede banktransaktioner i dine bankkonti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: db4afccdd67e400f2effd34b2db3c449db10432a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779703"
---
# <a name="reconciling-bank-accounts"></a><span data-ttu-id="4e821-103">Bankkontoafstemning</span><span class="sxs-lookup"><span data-stu-id="4e821-103">Reconciling Bank Accounts</span></span>

<span data-ttu-id="4e821-104">En bankafstemning skal udføres med jævne mellemrum for alle dine bankkonti for at sikre, at firmaets kontantposter er korrekte.</span><span class="sxs-lookup"><span data-stu-id="4e821-104">A bank reconciliation should be completed at regular intervals for all your bank accounts to ensure that the company's cash records are correct.</span></span> <span data-ttu-id="4e821-105">Det gør du ved at sammenligne og afstemme poster på dine interne bankkonti med banktransaktioner i din bank og derefter bogføre saldi på dine interne bankkonti for at gøre totaler tilgængelige for økonomichefer.</span><span class="sxs-lookup"><span data-stu-id="4e821-105">You do this by comparing and matching entries in your internal bank accounts with bank transactions at your bank, and then posting the balances to your internal bank accounts to make totals available to finance managers.</span></span> <span data-ttu-id="4e821-106">Bankafstemning er også en praktisk måde at opdage og løse manglende betalinger og bogføringsfejl på.</span><span class="sxs-lookup"><span data-stu-id="4e821-106">Bank reconciliation is also a practical way to discover and resolve missing payments and bookkeeping errors.</span></span>

<span data-ttu-id="4e821-107">Du kan udføre opgaven adskilt på siden **Bankkontoafstemning**, hvor du sammenholder (afstemmer) bankkontoudtogslinjer i venstre rude med dine interne bankkontoposter i højre rude.</span><span class="sxs-lookup"><span data-stu-id="4e821-107">You can perform the task on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="4e821-108">Du kan også udføre denne opgave på siden **Betalingsudligningskladde** som en del af behandling af betalinger, der er repræsenteret på et bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="4e821-108">Alternatively, you can perform this task on the **Payment Reconciliation Journal** page as part of processing the payments that are represented on a bank statement.</span></span> <span data-ttu-id="4e821-109">På begge sider kan du angive oplysninger for bankkontoudtog ved at importere en fil eller et feed, og du kan bruge automatiske sammenholdningsforslag.</span><span class="sxs-lookup"><span data-stu-id="4e821-109">On both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="4e821-110">I nordamerikanske versioner kan du også udføre bankafstemning på siden **Bankafstemningskladde**, der er mere velegnet til checks og indskud, men ikke kan bruges til import af bankkontoudtogsfiler.</span><span class="sxs-lookup"><span data-stu-id="4e821-110">In the North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="4e821-111">Hvis du vil bruge denne side i stedet for siden **Bankkontoafstemning**, skal du fjerne markeringen i feltet **Bankafstemning med automatisk match** på siden **Regnskabsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="4e821-111">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="4e821-112">Du kan finde flere oplysninger i afsnittet [Afstemme bankkonti](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under Lokal funktionalitet for USA.</span><span class="sxs-lookup"><span data-stu-id="4e821-112">For more information, see [Reconcile Bank Accounts](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under United States Local Functionality.</span></span>

<span data-ttu-id="4e821-113">Før du kan administrere dine bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)], skal du konfigurere hver bankkonto som et bankkontokort.</span><span class="sxs-lookup"><span data-stu-id="4e821-113">Before you can manage your bank accounts within [!INCLUDE[prod_short](includes/prod_short.md)], you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="4e821-114">Desuden skal du oprette elektroniske tjenester, som du kan bruge til import af bankens kontoudtog og eksport af betalingsfilen.</span><span class="sxs-lookup"><span data-stu-id="4e821-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="4e821-115">Der er flere oplysninger i [Konfigurere banktransaktioner](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="4e821-115">For more information, see [Setting Up Banking](bank-setup-banking.md).</span></span>

<span data-ttu-id="4e821-116">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="4e821-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="4e821-117">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="4e821-117">To</span></span> | <span data-ttu-id="4e821-118">Skal du se</span><span class="sxs-lookup"><span data-stu-id="4e821-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="4e821-119">Afstemme bankkonti som en separat opgave på siden **Bankkontoafstemning**.</span><span class="sxs-lookup"><span data-stu-id="4e821-119">Reconcile bank accounts as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="4e821-120">Afstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="4e821-120">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="4e821-121">Afstem bankkonti i forbindelse med betalingsbehandling på siden **Betalingudligningskladde**.</span><span class="sxs-lookup"><span data-stu-id="4e821-121">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="4e821-122">Udligne betalinger automatisk og afstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="4e821-122">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> <span data-ttu-id="4e821-123">Brug bankafstemning til at kontrollere, at dine bøger er opdaterede og ikke bogfører afstemningen, før du er tilfreds med afstemningen.</span><span class="sxs-lookup"><span data-stu-id="4e821-123">Use bank reconciliation to help verify that your books are up-to-date, and do not post the reconciliation until you are satisfied with the reconciliation.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="4e821-124">Se relateret oplæring på [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="4e821-124">See Related Training at [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="4e821-125">Se også</span><span class="sxs-lookup"><span data-stu-id="4e821-125">See Also</span></span>

[<span data-ttu-id="4e821-126">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="4e821-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="4e821-127">Afstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="4e821-127">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md)  
[<span data-ttu-id="4e821-128">Udligne betalinger automatisk og afstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="4e821-128">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[<span data-ttu-id="4e821-129">Overføre bankbeløb</span><span class="sxs-lookup"><span data-stu-id="4e821-129">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md)  
[<span data-ttu-id="4e821-130">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="4e821-130">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="4e821-131">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="4e821-131">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="4e821-132">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4e821-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4e821-133">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="4e821-133">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]