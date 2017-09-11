---
title: Oprette bankkonti | Microsoft Docs
description: Du kan afstemme bankkonti i Financials med kontoudtog fra banken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f46e95e24ef39a93bc93cfda1b9c575b07273566
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-set-up-bank-accounts"></a><span data-ttu-id="4b06f-103">Fremgangsmåde: Oprette bankkonti</span><span class="sxs-lookup"><span data-stu-id="4b06f-103">How to: Set Up Bank Accounts</span></span>
<span data-ttu-id="4b06f-104">Brug bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] til at holde styr på dine banktransaktioner.</span><span class="sxs-lookup"><span data-stu-id="4b06f-104">You use bank accounts in the [!INCLUDE[d365fin](includes/d365fin_md.md)] to keep track of your banking transactions.</span></span> <span data-ttu-id="4b06f-105">Konti kan være i den lokale valuta eller i fremmed valuta.</span><span class="sxs-lookup"><span data-stu-id="4b06f-105">Accounts can be denominated in your local currency or in a foreign currency.</span></span> <span data-ttu-id="4b06f-106">Når du har oprettet bankkonti, kan du også bruge funktionen til kontrol af udskrevne check.</span><span class="sxs-lookup"><span data-stu-id="4b06f-106">After you have set up bank accounts, you can also use the check printing option.</span></span>

## <a name="to-set-up-bank-accounts"></a><span data-ttu-id="4b06f-107">Sådan oprettes bankkonti</span><span class="sxs-lookup"><span data-stu-id="4b06f-107">To set up bank accounts</span></span>
1. <span data-ttu-id="4b06f-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="4b06f-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="4b06f-109">I vinduet **Bankkonti** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4b06f-109">In the **Bank Accounts** window, choose the **New** action.</span></span>
3. <span data-ttu-id="4b06f-110">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="4b06f-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a><span data-ttu-id="4b06f-111">Sådan oprettes bankkontoen for import eller eksport af bankfiler</span><span class="sxs-lookup"><span data-stu-id="4b06f-111">To set up your bank account for import or export of bank files</span></span>
<span data-ttu-id="4b06f-112">Felter i oversigtspanelet **Overførsel** i vinduet **Bankkontokort** er relateret til indlæsning og udlæsning af bankfeeds og -filer.</span><span class="sxs-lookup"><span data-stu-id="4b06f-112">Fields on the **Transfer** FastTab in the **Bank Account Card** window are related to import and export of bank feeds and files.</span></span> <span data-ttu-id="4b06f-113">Du kan finde flere oplysninger i [Fremgangsmåde: Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-data-conversion-service.md) og [Fremgangsmåde: Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="4b06f-113">For more information, see [How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [How to: Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

1. <span data-ttu-id="4b06f-114">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="4b06f-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="4b06f-115">Åbn kortet for en bankkonto, du vil eksportere eller importere bankfiler for.</span><span class="sxs-lookup"><span data-stu-id="4b06f-115">Open the card for a bank account that you will export or import bank files for.</span></span>
3. <span data-ttu-id="4b06f-116">Udfyld felterne efter behov i oversigtspanelet **Overførsel**.</span><span class="sxs-lookup"><span data-stu-id="4b06f-116">On the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="4b06f-117">Andre fileksporttjenester og deres formater kræver andre konfigurationsværdier i vinduet **Bankkontokort**.</span><span class="sxs-lookup"><span data-stu-id="4b06f-117">Different file export services and their formats require different setup values in the **Bank Account Card** window.</span></span> <span data-ttu-id="4b06f-118">Du får information om forkerte eller manglende konfigurationsværdier, når du prøver at eksportere filen.</span><span class="sxs-lookup"><span data-stu-id="4b06f-118">You will be informed about wrong or missing setup values as you try to export the file.</span></span> <span data-ttu-id="4b06f-119">Så læs omhyggeligt korte beskrivelser af felterne, eller se de relaterede emner med fremgangsmåder.</span><span class="sxs-lookup"><span data-stu-id="4b06f-119">So read the short descriptions of the fields carefully or refer to the related procedure topics.</span></span> <span data-ttu-id="4b06f-120">Eksport af en betalingsfil med nordamerikansk elektronisk pengeoverførsel (EFT) kræver, at både feltet **Sidste remitteringsadvisnr.**</span><span class="sxs-lookup"><span data-stu-id="4b06f-120">For example, exporting a payment file for North American electronic funds transfer (EFT) requires that both the **Last Remittance Advice No.**</span></span> <span data-ttu-id="4b06f-121">og feltet **Transitnr.**</span><span class="sxs-lookup"><span data-stu-id="4b06f-121">field and the **Transit No.**</span></span> <span data-ttu-id="4b06f-122">er udfyldt.</span><span class="sxs-lookup"><span data-stu-id="4b06f-122">field are filled in.</span></span> <span data-ttu-id="4b06f-123">Du kan finde flere oplysninger i [Fremgangsmåde: Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="4b06f-123">For more information, see [How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a><span data-ttu-id="4b06f-124">Sådan konfigureres kreditorbankkonti til eksport af bankfiler</span><span class="sxs-lookup"><span data-stu-id="4b06f-124">To set up vendor bank accounts for export of bank files</span></span>
<span data-ttu-id="4b06f-125">Felter i oversigtspanelet **Overførsel** i vinduet **Kreditors bankkontokort** er relateret til udlæsning af bankfeeds og -filer.</span><span class="sxs-lookup"><span data-stu-id="4b06f-125">Fields on the **Transfer** FastTab in the **Vendor Bank Account Card** window are related to export of bank feeds and files.</span></span> <span data-ttu-id="4b06f-126">Du kan finde flere oplysninger i [Fremgangsmåde: Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-data-conversion-service.md) og [Fremgangsmåde: Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="4b06f-126">For more information, see [How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

1. <span data-ttu-id="4b06f-127">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="4b06f-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="4b06f-128">Åbn kortet for en kreditor, hvis bankkonto du vil eksportere betalingsbankfiler til.</span><span class="sxs-lookup"><span data-stu-id="4b06f-128">Open the card for a vendor whose bank account you will export payment bank files to.</span></span>
3. <span data-ttu-id="4b06f-129">Vælg handlingen **Bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="4b06f-129">Choose the **Bank Accounts** action.</span></span>
3. <span data-ttu-id="4b06f-130">Udfyld felterne efter behov i vinduet **Kreditors bankkontokort** i oversigtspanelet **Overførsel**.</span><span class="sxs-lookup"><span data-stu-id="4b06f-130">In the **Vendor Bank Account Card** window, on the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="4b06f-131">Se også</span><span class="sxs-lookup"><span data-stu-id="4b06f-131">See Also</span></span>
[<span data-ttu-id="4b06f-132">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="4b06f-132">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="4b06f-133">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="4b06f-133">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
<span data-ttu-id="4b06f-134">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4b06f-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

