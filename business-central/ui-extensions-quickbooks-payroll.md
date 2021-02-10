---
title: Bruge udvidelsen Import af QuickBooks-lønfil | Microsoft Docs
description: Dette emne beskriver, hvordan du kan bruge udvidelsen til at importere gage- og løntransaktioner fra tjenesten QuickBooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: eae93ea8cf81a2fad6af2c3810f94d5292eef93f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757088"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="b656a-103">Udvidelsen Import af QuickBooks-lønfiler</span><span class="sxs-lookup"><span data-stu-id="b656a-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="b656a-104">Brug udvidelsen Import af QuickBooks-lønfiler til at importere lønningstransaktioner fra QuickBooks til finanskonti i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b656a-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b656a-105">Dette er f.eks. nyttigt, når du går over fra QuickBooks til [!INCLUDE[prod_short](includes/prod_short.md)], eller hvis du outsourcer din løn, men også ønsker at holde styr på den i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b656a-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="b656a-106">Trin til import af løndata</span><span class="sxs-lookup"><span data-stu-id="b656a-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="b656a-107">Første trin for dig eller måske din bogholder er at bruge eksportfunktionen i QuickBooks til at eksportere løndata til en .IIF- fil.</span><span class="sxs-lookup"><span data-stu-id="b656a-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="b656a-108">Det andet trin er at åbne siden **Finanskladder** i [!INCLUDE[prod_short](includes/prod_short.md)] og bruge handlingen **Importér løntransaktioner** til at importere filen.</span><span class="sxs-lookup"><span data-stu-id="b656a-108">The second step is to open the **General Journals** page in [!INCLUDE[prod_short](includes/prod_short.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="b656a-109">Under importprocessen knytter du finanskontiene fra QuickBooks til de tilsvarende konti i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b656a-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b656a-110">Det sidste trin er at bogføre lønningstransaktionerne i [!INCLUDE[prod_short](includes/prod_short.md)] i overensstemmelse med kontotilknytningen.</span><span class="sxs-lookup"><span data-stu-id="b656a-110">The final step is to post the payroll transactions in [!INCLUDE[prod_short](includes/prod_short.md)] according to the account mapping.</span></span> 

<span data-ttu-id="b656a-111">Du kan finde flere oplysninger under [Importere løntransaktioner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="b656a-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b656a-112">Se også</span><span class="sxs-lookup"><span data-stu-id="b656a-112">See Also</span></span>
<span data-ttu-id="b656a-113">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="b656a-113">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="b656a-114">[Finans](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="b656a-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="b656a-115">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b656a-115">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
