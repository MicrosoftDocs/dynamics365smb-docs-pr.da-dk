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
ms.date: 01/09/2019
ms.author: bholtorf
ms.openlocfilehash: ac68f8a4d67224ad55b1c34ff9b2e4ffa2c372aa
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792440"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="3acaf-103">Udvidelsen Import af QuickBooks-lønfiler</span><span class="sxs-lookup"><span data-stu-id="3acaf-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="3acaf-104">Brug udvidelsen Import af QuickBooks-lønfiler til at importere lønningstransaktioner fra QuickBooks til finanskonti i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3acaf-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3acaf-105">Dette er f.eks. nyttigt, når du går over fra QuickBooks til [!INCLUDE[d365fin](includes/d365fin_md.md)], eller hvis du outsourcer din løn, men også ønsker at holde styr på den i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3acaf-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="3acaf-106">Trin til import af løndata</span><span class="sxs-lookup"><span data-stu-id="3acaf-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="3acaf-107">Første trin for dig eller måske din bogholder er at bruge eksportfunktionen i QuickBooks til at eksportere løndata til en .IIF- fil.</span><span class="sxs-lookup"><span data-stu-id="3acaf-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="3acaf-108">Det andet trin er at åbne siden **Finanskladder** i [!INCLUDE[d365fin](includes/d365fin_md.md)] og bruge handlingen **Importér løntransaktioner** til at importere filen.</span><span class="sxs-lookup"><span data-stu-id="3acaf-108">The second step is to open the **General Journals** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="3acaf-109">Under importprocessen knytter du finanskontiene fra QuickBooks til de tilsvarende konti i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3acaf-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3acaf-110">Det sidste trin er at bogføre lønningstransaktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] i overensstemmelse med kontotilknytningen.</span><span class="sxs-lookup"><span data-stu-id="3acaf-110">The final step is to post the payroll transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] according to the account mapping.</span></span> 

<span data-ttu-id="3acaf-111">Du kan finde flere oplysninger under [Importere løntransaktioner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="3acaf-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3acaf-112">Se også</span><span class="sxs-lookup"><span data-stu-id="3acaf-112">See Also</span></span>
<span data-ttu-id="3acaf-113">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="3acaf-113">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="3acaf-114">[Finans](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="3acaf-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="3acaf-115">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3acaf-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
