---
title: "Foretage indbetalinger med tjenesten til konvertering af bankdata eller SEPA Kreditoverførsel | Microsoft Docs"
description: Du kan behandle betalinger til dine kreditorer ved at eksportere en fil sammen med betalingsoplysningerne fra kladdelinjerne.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1e0c88184d2b453e9eb3d31a2b140fbe9002d849
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="24ed6-103">Foretage indbetalinger med tjenesten til konvertering af bankdata eller SEPA Kreditoverførsel</span><span class="sxs-lookup"><span data-stu-id="24ed6-103">Making Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="24ed6-104">I vinduet **Udbetalingskladde** kan du behandle betalinger til dine kreditorer ved at eksportere en fil sammen med betalingsoplysningerne fra kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="24ed6-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="24ed6-105">Derefter kan du uploade filen til din elektroniske bank, hvor de relaterede pengeoverførsler behandles.</span><span class="sxs-lookup"><span data-stu-id="24ed6-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="24ed6-106">understøtter SEPA-kreditoverførselsformatet, men i dit land/område anvendes der muligvis andre formater til elektroniske betalinger.</span><span class="sxs-lookup"><span data-stu-id="24ed6-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="24ed6-107">Hvis du vil aktivere SEPA-kreditoverførsler, skal du først angive en bankkonto, en kreditor og finanskladdenavnet, som betalingskladden er baseret på.</span><span class="sxs-lookup"><span data-stu-id="24ed6-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="24ed6-108">Derefter forbereder du betalinger til kreditorer ved automatisk at udfylde vinduet **Udbetalingskladde** med forfaldne betalinger med angivne bogføringsdatoer.</span><span class="sxs-lookup"><span data-stu-id="24ed6-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="24ed6-109">Når du har kontrolleret, at betalingerne er behandlet af banken, kan du fortsætte med at bogføre udbetalingskladdens linjer.</span><span class="sxs-lookup"><span data-stu-id="24ed6-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="24ed6-110">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="24ed6-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="24ed6-111">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="24ed6-111">**To**</span></span>|<span data-ttu-id="24ed6-112">**Se**</span><span class="sxs-lookup"><span data-stu-id="24ed6-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="24ed6-113">Aktiver funktionen Tjeneste til konvertering af bankdata for at konvertere en fil med bankkontoudtog til et format, som du kan importere, eller for at få dine eksporterede betalingsfiler konverteret tilbage til det format, som din bank kræver.</span><span class="sxs-lookup"><span data-stu-id="24ed6-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="24ed6-114">Konfigurere tjenesten til konvertering af bankdata</span><span class="sxs-lookup"><span data-stu-id="24ed6-114">Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="24ed6-115">Oprette en bankkonto, en kreditor og en betalingskladde til SEPA-kreditoverførslen.</span><span class="sxs-lookup"><span data-stu-id="24ed6-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="24ed6-116">Opsætte SEPA-kreditoverførsel</span><span class="sxs-lookup"><span data-stu-id="24ed6-116">Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="24ed6-117">Udfyld betalingskladdelinjerne for forfaldne betalinger til kreditorer med mulighed for at indsætte bogføringsdatoer, der er baseret på forfaldsdatoen for de relaterede købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="24ed6-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="24ed6-118">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="24ed6-118">Managing Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="24ed6-119">Eksportér betalingskladdelinjer til en fil i SEPA-kreditoverførselsformat.</span><span class="sxs-lookup"><span data-stu-id="24ed6-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="24ed6-120">Eksportere betalinger til en bankfil</span><span class="sxs-lookup"><span data-stu-id="24ed6-120">Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="24ed6-121">Når elektronisk betaling er behandlet af banken, kan du bogføre betalingerne.</span><span class="sxs-lookup"><span data-stu-id="24ed6-121">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="24ed6-122">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="24ed6-122">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="24ed6-123">Se også</span><span class="sxs-lookup"><span data-stu-id="24ed6-123">See Also</span></span>  
[<span data-ttu-id="24ed6-124">Konfigurere tjenesten til konvertering af bankdata</span><span class="sxs-lookup"><span data-stu-id="24ed6-124">Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="24ed6-125">Opsætte SEPA-kreditoverførsel</span><span class="sxs-lookup"><span data-stu-id="24ed6-125">Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="24ed6-126">[Administrere skyldige beløb](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="24ed6-126">[Managing Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="24ed6-127">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="24ed6-127">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="24ed6-128">Indhente betalinger med SEPA Direct Debit</span><span class="sxs-lookup"><span data-stu-id="24ed6-128">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

