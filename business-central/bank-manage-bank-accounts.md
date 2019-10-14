---
title: Håndtere bankkonti | Microsoft Docs
description: Du skal afstemme bankposter regelmæssigt med de relaterede banktransaktioner i dine bankkonti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9e5fe99fe822ca94758a3030659bf484f917fcaa
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308376"
---
# <a name="managing-bank-accounts"></a><span data-ttu-id="ece4f-103">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="ece4f-103">Managing Bank Accounts</span></span>
<span data-ttu-id="ece4f-104">Med faste intervaller skal du afstemme dine bankposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] med de relaterede banktransaktioner i bankkonti i din bank og derefter bogføre saldoen til din bankkonto.</span><span class="sxs-lookup"><span data-stu-id="ece4f-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="ece4f-105">Du kan udføre denne opgave, enten som en del af behandling af betalinger, der er repræsenteret på bankkontoudtoget i feltet **Betalingsudligningskladde**.</span><span class="sxs-lookup"><span data-stu-id="ece4f-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="ece4f-106">Alternativt kan du udføre opgaven adskilt fra betalingsbehandlingen på siden **Bankkontoafstemning**, hvor du sammenholder (afstemmer) bankkontoudtogslinjer i venstre rude med dine interne bankkontoposter i højre rude.</span><span class="sxs-lookup"><span data-stu-id="ece4f-106">Alternatively, you can perform the task separately from payment processing, on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="ece4f-107">På begge sider kan du angive oplysninger for bankkontoudtog ved at importere en fil eller et feed, og du kan bruge automatiske sammenholdningsforslag.</span><span class="sxs-lookup"><span data-stu-id="ece4f-107">In both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="ece4f-108">I nordamerikanske versioner kan du også udføre bankafstemning på siden **Bankafstemningskladde**, der er mere velegnet til checks og indskud, men ikke kan bruges til import af bankkontoudtogsfiler.</span><span class="sxs-lookup"><span data-stu-id="ece4f-108">In North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="ece4f-109">Hvis du vil bruge denne side i stedet for siden **Bankkontoafstemning**, skal du fjerne markeringen i feltet **Bankafstemning med automatisk match** på siden **Regnskabsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="ece4f-109">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="ece4f-110">Du kan finde flere oplysninger i afsnittet "Afstemme bankkonti" under Lokal funktionalitet for USA.</span><span class="sxs-lookup"><span data-stu-id="ece4f-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="ece4f-111">Nogle gange skal der overføres beløb mellem bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] for at afspejle overførsler i din bank.</span><span class="sxs-lookup"><span data-stu-id="ece4f-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="ece4f-112">Du udfører denne opgave på siden **Finanskladde** på forskellige måder afhængigt af valutaen for beløbene.</span><span class="sxs-lookup"><span data-stu-id="ece4f-112">You perform this task on the **General Journal** page, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="ece4f-113">Før du kan administrere bankkonti, skal du konfigurere hver bankkonto som et bankkontokort.</span><span class="sxs-lookup"><span data-stu-id="ece4f-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="ece4f-114">Desuden skal du oprette elektroniske tjenester, som du kan bruge til import af bankens kontoudtog og eksport af betalingsfilen.</span><span class="sxs-lookup"><span data-stu-id="ece4f-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="ece4f-115">Du kan finde flere oplysninger i [Oprette bankkonti](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="ece4f-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="ece4f-116">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="ece4f-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="ece4f-117">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="ece4f-117">To</span></span> | <span data-ttu-id="ece4f-118">Se</span><span class="sxs-lookup"><span data-stu-id="ece4f-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="ece4f-119">Afstem bankkonti i forbindelse med betalingsbehandling på siden **Betalingudligningskladde**.</span><span class="sxs-lookup"><span data-stu-id="ece4f-119">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="ece4f-120">Udligne betalinger automatisk og afstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="ece4f-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="ece4f-121">Afstemme bankkonti, herunder checkposter, som en separat opgave på siden **Bankkontoafstemning**.</span><span class="sxs-lookup"><span data-stu-id="ece4f-121">Reconcile bank accounts, including check ledger entries, as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="ece4f-122">Afstemme bankkonti separat</span><span class="sxs-lookup"><span data-stu-id="ece4f-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="ece4f-123">Bogføre overførsler mellem bankkonti i samme valuta eller i forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="ece4f-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="ece4f-124">Overføre bankbeløb</span><span class="sxs-lookup"><span data-stu-id="ece4f-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="ece4f-125">Se også</span><span class="sxs-lookup"><span data-stu-id="ece4f-125">See Also</span></span>
[<span data-ttu-id="ece4f-126">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="ece4f-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="ece4f-127">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="ece4f-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="ece4f-128">[Administrere skyldige beløb](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="ece4f-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="ece4f-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ece4f-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ece4f-130">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="ece4f-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
