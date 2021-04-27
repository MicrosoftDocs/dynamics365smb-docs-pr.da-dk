---
title: Udvidelsen QuickBooks-overførsel | Microsoft Docs
description: Beskriver, hvordan du bruger udvidelsen til at importere debitorer, kreditorer, varer og konti fra QuickBooks Desktop til Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d6b44ccfc11438930450dd86cab53736f00995c5
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785031"
---
# <a name="the-quickbooks-data-migration-extension"></a><span data-ttu-id="3a921-103">Udvidelsen Overførsel af QuickBooks-data</span><span class="sxs-lookup"><span data-stu-id="3a921-103">The QuickBooks Data Migration Extension</span></span>

<span data-ttu-id="3a921-104">Denne udvidelse gør det nemt at overflytte debitorer, kreditorer, varer og konti fra QuickBooks til [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3a921-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="3a921-105">Hvis din virksomhed bruger QuickBooks i dag, kan du eksportere de relevante oplysninger og derefter åbne en assisteret opsætningsvejledning for at overføre dataene til [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3a921-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  
<span data-ttu-id="3a921-106">Du kan finde flere oplysninger i [Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="3a921-106">For more information, see [Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md).</span></span>

## <a name="data-from-quickbooks-desktop"></a><span data-ttu-id="3a921-107">Data fra QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="3a921-107">Data from QuickBooks Desktop</span></span>

<span data-ttu-id="3a921-108">Du kan importere følgende data fra QuickBooks Online til Business Central:</span><span class="sxs-lookup"><span data-stu-id="3a921-108">You can import the following data from QuickBooks Online to Business Central:</span></span>

- <span data-ttu-id="3a921-109">Kunder (Debitorer)</span><span class="sxs-lookup"><span data-stu-id="3a921-109">Customers</span></span>  
- <span data-ttu-id="3a921-110">Leverandører (Kreditorer)</span><span class="sxs-lookup"><span data-stu-id="3a921-110">Vendors</span></span>  
- <span data-ttu-id="3a921-111">Varer</span><span class="sxs-lookup"><span data-stu-id="3a921-111">Items</span></span>  
- <span data-ttu-id="3a921-112">Kontoplan</span><span class="sxs-lookup"><span data-stu-id="3a921-112">Chart of Accounts</span></span>  
- <span data-ttu-id="3a921-113">Primosaldopostering i regnskabet</span><span class="sxs-lookup"><span data-stu-id="3a921-113">Beginning Balance transactions in General Ledger</span></span>  
- <span data-ttu-id="3a921-114">Disponible antal for lagervarer</span><span class="sxs-lookup"><span data-stu-id="3a921-114">On-hand Quantities for Inventory Items</span></span>  
- <span data-ttu-id="3a921-115">Åbne dokumenter for debitorer og kreditorer, f.eks. fakturaer, kreditnotaer og betalinger</span><span class="sxs-lookup"><span data-stu-id="3a921-115">Open documents for customers and vendors, such as invoices, credit memos and payments</span></span>  

<span data-ttu-id="3a921-116">Vi overfører kun fulde beløb på salgs- og købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="3a921-116">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="3a921-117">Delvist betalte beløb opdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="3a921-117">We do not update partially paid amounts.</span></span> <span data-ttu-id="3a921-118">F.eks. hvis en debitor har indbetalt 300 af i alt 500 dollar på en salgsfaktura, overfører vi hele 500.</span><span class="sxs-lookup"><span data-stu-id="3a921-118">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="3a921-119">Hvis du har modtaget delbetalinger, skal du opdatere dem manuelt, før eller efter at du overfører data.</span><span class="sxs-lookup"><span data-stu-id="3a921-119">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="3a921-120">Det anbefales, at du anvender udestående transaktioner, inden du overfører, for at gøre tingene nemmere bagefter.</span><span class="sxs-lookup"><span data-stu-id="3a921-120">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]
> <span data-ttu-id="3a921-121">Vi overfører ikke indkøbsordrer eller salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="3a921-121">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="3a921-122">Før du starter</span><span class="sxs-lookup"><span data-stu-id="3a921-122">Before You Start</span></span>

<span data-ttu-id="3a921-123">Det er en vigtig del af overførslen at angive de konti, transaktioner skal overføres til.</span><span class="sxs-lookup"><span data-stu-id="3a921-123">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="3a921-124">Det er en god ide at planlægge denne tilknytning, før du overfører data.</span><span class="sxs-lookup"><span data-stu-id="3a921-124">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="3a921-125">F.eks. de konti, hvor du bogfører poster for:</span><span class="sxs-lookup"><span data-stu-id="3a921-125">For example, the accounts where you post transactions for:</span></span>

- <span data-ttu-id="3a921-126">Salget af varer eller servicer til debitorer</span><span class="sxs-lookup"><span data-stu-id="3a921-126">The sale of items or services to customers</span></span>  
- <span data-ttu-id="3a921-127">Køb af varer eller servicer fra kreditorer</span><span class="sxs-lookup"><span data-stu-id="3a921-127">The purchase of items or services from vendors</span></span>  
- <span data-ttu-id="3a921-128">Ændringer i finansbogholderiet</span><span class="sxs-lookup"><span data-stu-id="3a921-128">Adjustments in the general ledger</span></span>  

<span data-ttu-id="3a921-129">Business Central kræver, at finanskonti har kontonumre tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="3a921-129">Business Central requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="3a921-130">Sørg for, at kontonumre er tildelt til kontiene i QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="3a921-130">Make sure that account numbers are assigned to your accounts in QuickBooks.</span></span>
<span data-ttu-id="3a921-131">Hvis der er transaktioner i QuickBooks, der har momsbeløb, du skal oprette en momskonto for dine skatteregioner i Business Central, før du kan bogføre transaktioner.</span><span class="sxs-lookup"><span data-stu-id="3a921-131">If transactions in QuickBooks have tax amounts, you must set up a tax account for your tax jurisdictions in Business Central before you can post transactions.</span></span>

<span data-ttu-id="3a921-132">For at få data ud af programmet QuickBooks Desktop skal du hente værktøjet Microsoft-dataeksportværktøjet.</span><span class="sxs-lookup"><span data-stu-id="3a921-132">In order to get your data out of the QuickBooks desktop application you will need to download the Microsoft Data Exporter Tool.</span></span>  <span data-ttu-id="3a921-133">Instruktioner til værktøjet findes i dataoverførselsguiden i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3a921-133">The instructions for the tool are in the Data Migration Wizard in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="3a921-134">Værktøjet opretter forbindelse til programmet QuickBooks og eksportere de relevante oplysninger til en .zip-fil.</span><span class="sxs-lookup"><span data-stu-id="3a921-134">The tool will connect to your QuickBooks application and export the applicable data to a .zip file.</span></span>  

> [!NOTE]
> <span data-ttu-id="3a921-135">I øjeblikket fungerer dataeksportværktøjet kun sammen med QuickBooks 2017 og 2018.</span><span class="sxs-lookup"><span data-stu-id="3a921-135">Currently the data exporter tool only works with QuickBooks 2017 and 2018.</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="3a921-136">Sådan finder du udvidelsen Overførsel af QuickBooks-data</span><span class="sxs-lookup"><span data-stu-id="3a921-136">Finding the QuickBooks Data Migration Extension</span></span>

<span data-ttu-id="3a921-137">Udvidelsen Overførsel af QuickBooks-data er installeret og klar til brug som en integreret del af den assisterende opsætningsvejledning til dataoverførsel.</span><span class="sxs-lookup"><span data-stu-id="3a921-137">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="3a921-138">Hvis du er klar til at komme i gang nu og har eksporteret dine data fra QuickBooks, skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Assisteret opsætning** og derefter vælge det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="3a921-138">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="3a921-139">Vælg **Overflyt forretningsdata**, og følg derefter trinnene i vejledningen.</span><span class="sxs-lookup"><span data-stu-id="3a921-139">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="3a921-140">Hvad gør jeg, når jeg har overført data?</span><span class="sxs-lookup"><span data-stu-id="3a921-140">What do I do after I migrate Data?</span></span>

<span data-ttu-id="3a921-141">Når du har overført data, har transaktioner status Ikke-bogførte, så du kan gennemgå dem og foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="3a921-141">After you migrate data, transactions have the status Unposted, so you can review them and make adjustments.</span></span> <span data-ttu-id="3a921-142">For at få vist transaktionerne skal du gå til siden, hvor du vil finde dem normalt.</span><span class="sxs-lookup"><span data-stu-id="3a921-142">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="3a921-143">F.eks. for at få vist ikke-bogførte salgsfakturaer, skal du gå til siden Salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="3a921-143">For example, to review unposted sales invoices, go to the Sales Invoices page.</span></span> <span data-ttu-id="3a921-144">For at få vist udbetalingskladder skal du gå til siden Udbetalingskladder.</span><span class="sxs-lookup"><span data-stu-id="3a921-144">To review payment journals, go to the Payment Journals page.</span></span>
<span data-ttu-id="3a921-145">Der er især nogle ting, du skal gøre: Hvis transaktionerne i QuickBooks havde avance- eller rabatbeløb, skal du manuelt føje beløbene til de relaterede transaktioner i Business Central, før du bogfører dem.</span><span class="sxs-lookup"><span data-stu-id="3a921-145">There are a few things in particular that you should do: If the transactions in QuickBooks had markup or discount amounts, you must manually add the amounts to the related transactions in Business Central before you post them.</span></span>
<span data-ttu-id="3a921-146">Hvis du bruger moms, skal du evt. tilføje en virksomhedsbogføringsgruppe og en produktbogføringsgruppe i bogføringsopsætningen, så du kan bogføre momsbeløb.</span><span class="sxs-lookup"><span data-stu-id="3a921-146">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
<span data-ttu-id="3a921-147">Kontroller primosaldi for konti i finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="3a921-147">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="3a921-148">QuickBooks gemmer ikke den aktuelle saldo for alle konti, så det kan være nødvendigt at rette primosaldi.</span><span class="sxs-lookup"><span data-stu-id="3a921-148">QuickBooks does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a921-149">Se også</span><span class="sxs-lookup"><span data-stu-id="3a921-149">See Also</span></span>

[<span data-ttu-id="3a921-150">Importer virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="3a921-150">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="3a921-151">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="3a921-151">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]