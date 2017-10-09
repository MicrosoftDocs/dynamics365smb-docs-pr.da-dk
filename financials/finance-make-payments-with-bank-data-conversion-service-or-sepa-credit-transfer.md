---
title: "Vælg metoden for elektroniske betalinger | Microsoft Docs"
description: Du kan behandle betalinger til dine kreditorer ved at eksportere en fil sammen med betalingsoplysningerne fra kladdelinjerne.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bbb38f7d4a4b7d1b63cfceef2640172d7b69e364
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="9b1b0-103">Foretag indbetalinger med tjenesten til konvertering af bankdata eller SEPA Kreditoverførsel</span><span class="sxs-lookup"><span data-stu-id="9b1b0-103">Make Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="9b1b0-104">I vinduet **Udbetalingskladde** kan du behandle betalinger til dine kreditorer ved at eksportere en fil sammen med betalingsoplysningerne fra kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="9b1b0-105">Derefter kan du uploade filen til din elektroniske bank, hvor de relaterede pengeoverførsler behandles.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9b1b0-106"> understøtter SEPA-kreditoverførselsformatet, men i dit land/område anvendes der muligvis andre formater til elektroniske betalinger.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="9b1b0-107">Hvis du vil aktivere SEPA-kreditoverførsler, skal du først angive en bankkonto, en kreditor og finanskladdenavnet, som betalingskladden er baseret på.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="9b1b0-108">Derefter forbereder du betalinger til kreditorer ved automatisk at udfylde vinduet **Udbetalingskladde** med forfaldne betalinger med angivne bogføringsdatoer.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9b1b0-109">Når du har kontrolleret, at betalingerne er behandlet af banken, kan du fortsætte med at bogføre udbetalingskladdens linjer.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="9b1b0-110">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="9b1b0-111">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="9b1b0-111">**To**</span></span>|<span data-ttu-id="9b1b0-112">**Se**</span><span class="sxs-lookup"><span data-stu-id="9b1b0-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="9b1b0-113">Aktiver funktionen Tjeneste til konvertering af bankdata for at konvertere en fil med bankkontoudtog til et format, som du kan importere, eller for at få dine eksporterede betalingsfiler konverteret tilbage til det format, som din bank kræver.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="9b1b0-114">Fremgangsmåde: Konfigurere tjenesten til konvertering af bankdata</span><span class="sxs-lookup"><span data-stu-id="9b1b0-114">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="9b1b0-115">Opret en bankkonto, en kreditor og en betalingskladde til SEPA-kreditoverførslen.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="9b1b0-116">Fremgangsmåde: Opsætte SEPA-kreditoverførsel</span><span class="sxs-lookup"><span data-stu-id="9b1b0-116">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="9b1b0-117">Udfyld betalingskladdelinjerne for forfaldne betalinger til kreditorer med mulighed for at indsætte bogføringsdatoer, der er baseret på forfaldsdatoen for de relaterede købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="9b1b0-118">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="9b1b0-118">Manage Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="9b1b0-119">Eksportér betalingskladdelinjer til en fil i SEPA-kreditoverførselsformat.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="9b1b0-120">Fremgangsmåde: Eksportere betalinger til en bankfil</span><span class="sxs-lookup"><span data-stu-id="9b1b0-120">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="9b1b0-121">Gennemgå, hvilke betalinger der er eksporteret, og i hvilke filer.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-121">Review which payments have been exported and into which files.</span></span>|<span data-ttu-id="9b1b0-122">Kreditoverførselsjournaler</span><span class="sxs-lookup"><span data-stu-id="9b1b0-122">Credit Transfer Registers</span></span>|  
|<span data-ttu-id="9b1b0-123">Når elektronisk betaling er behandlet af banken, kan du bogføre betalingerne.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-123">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="9b1b0-124">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="9b1b0-124">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="9b1b0-125">Se også</span><span class="sxs-lookup"><span data-stu-id="9b1b0-125">See Also</span></span>  
[<span data-ttu-id="9b1b0-126">Fremgangsmåde: Konfigurere tjenesten til konvertering af bankdata</span><span class="sxs-lookup"><span data-stu-id="9b1b0-126">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="9b1b0-127">Fremgangsmåde: Opsætte SEPA-kreditoverførsel</span><span class="sxs-lookup"><span data-stu-id="9b1b0-127">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="9b1b0-128">[Administrere skyldige beløb](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="9b1b0-128">[Manage Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="9b1b0-129">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="9b1b0-129">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="9b1b0-130">Indhente betalinger med SEPA Direct Debit</span><span class="sxs-lookup"><span data-stu-id="9b1b0-130">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

