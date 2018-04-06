---
title: "Håndtere bankkonti | Microsoft Docs"
description: Normalt skal du afstemme bankposter i Financials med de relaterede banktransaktioner i dine bankkonti.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bfc83194a1010e3ac628484952bd0c6b1046481b
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="bee82-103">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="bee82-103">Managing Bank Accounts</span></span>
<span data-ttu-id="bee82-104">Med faste intervaller skal du afstemme dine bankposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] med de relaterede banktransaktioner i bankkonti i din bank og derefter bogføre saldoen til din bankkonto.</span><span class="sxs-lookup"><span data-stu-id="bee82-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="bee82-105">Du kan udføre denne opgave, enten som en del af behandling af betalinger, der er repræsenteret på bankkontoudtoget i feltet **Betalingsudligningskladde**.</span><span class="sxs-lookup"><span data-stu-id="bee82-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="bee82-106">Eller du kan udføre opgaven adskilt fra betalingsbehandling i vinduet **Bankkontoafstemning**, som understøtter checkposter.</span><span class="sxs-lookup"><span data-stu-id="bee82-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window, which supports check ledger entries.</span></span> <span data-ttu-id="bee82-107">I begge tilfælde skal du udfylde vinduerne ved at importere bankkontoudtoget til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bee82-107">In both cases, you fill in the windows by importing the bank statement into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="bee82-108">Nogle gange skal der overføres beløb mellem bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] for at afspejle overførsler i din bank.</span><span class="sxs-lookup"><span data-stu-id="bee82-108">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="bee82-109">Du udfører denne opgave i vinduet **Finanskladde** på forskellige måder afhængigt af valutaen for beløbene.</span><span class="sxs-lookup"><span data-stu-id="bee82-109">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="bee82-110">Før du kan administrere bankkonti, skal du konfigurere hver bankkonto som et bankkontokort.</span><span class="sxs-lookup"><span data-stu-id="bee82-110">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="bee82-111">Desuden skal du oprette elektroniske tjenester, som du kan bruge til import af bankens kontoudtog og eksport af betalingsfilen.</span><span class="sxs-lookup"><span data-stu-id="bee82-111">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="bee82-112">Du kan finde flere oplysninger i [Oprette bankkonti](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="bee82-112">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="bee82-113">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="bee82-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="bee82-114">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="bee82-114">To</span></span> | <span data-ttu-id="bee82-115">Se</span><span class="sxs-lookup"><span data-stu-id="bee82-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="bee82-116">Afstem bankkonti i forbindelse med betalingsbehandling i vinduet **Betalingudligningskladde** vindue.</span><span class="sxs-lookup"><span data-stu-id="bee82-116">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="bee82-117">Udligne betalinger automatisk og afstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="bee82-117">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="bee82-118">Afstemme bankkonti, herunder checkposter, som en separat opgave i vinduet **Bankkontoafstemning**.</span><span class="sxs-lookup"><span data-stu-id="bee82-118">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="bee82-119">Afstemme bankkonti separat</span><span class="sxs-lookup"><span data-stu-id="bee82-119">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="bee82-120">Bogføre overførsler mellem bankkonti i samme valuta eller i forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="bee82-120">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="bee82-121">Overføre bankbeløb</span><span class="sxs-lookup"><span data-stu-id="bee82-121">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="bee82-122">Se også</span><span class="sxs-lookup"><span data-stu-id="bee82-122">See Also</span></span>
[<span data-ttu-id="bee82-123">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="bee82-123">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="bee82-124">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="bee82-124">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="bee82-125">[Administrere skyldige beløb](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="bee82-125">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="bee82-126">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bee82-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="bee82-127">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="bee82-127">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

