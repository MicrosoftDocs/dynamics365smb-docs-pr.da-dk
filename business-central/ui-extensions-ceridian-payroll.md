---
title: Indlæse løn eller løndata ved hjælp af udvidelsen Ceridian løn | Microsoft Docs
description: Brug denne udvidelse til at importere løntransaktioner fra tjenesterne Ceridian HR/Payroll (US) og Ceridian PowerPay (Canada).
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: ed3ba9f10ce24c97760dce972aa96134f1bc1119
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "791992"
---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="a8e2c-103">Udvidelsen Ceridian-lønudvidelse</span><span class="sxs-lookup"><span data-stu-id="a8e2c-103">The Ceridian Payroll Extension</span></span>
<span data-ttu-id="a8e2c-104">For at tage højde for lønbetalinger og relaterede transaktioner, skal du importere og bogføre finansielle transaktioner, der er foretaget af din lønningssystemudbyder i finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="a8e2c-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="a8e2c-105">For at gøre dette skal du først importere en fil, som du modtager fra lønningsystemudbyderen, på siden **Finanskladde**.</span><span class="sxs-lookup"><span data-stu-id="a8e2c-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="a8e2c-106">Derefter knytter du de eksterne konti i lønningslistefilen til de relevante finanskonti.</span><span class="sxs-lookup"><span data-stu-id="a8e2c-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="a8e2c-107">Til sidst skal du bogføre lønningstransaktionerne i overensstemmelse med kontotilknytningen.</span><span class="sxs-lookup"><span data-stu-id="a8e2c-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="a8e2c-108">Du kan finde flere oplysninger under [Importere løntransaktioner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="a8e2c-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="a8e2c-109">Udvidelsen Ceridian løn giver dig mulighed at importere løntransaktioner fra tjenesterne Ceridian HR/Payroll (US) og Ceridian PowerPay (Canada).</span><span class="sxs-lookup"><span data-stu-id="a8e2c-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8e2c-110">Se også</span><span class="sxs-lookup"><span data-stu-id="a8e2c-110">See Also</span></span>
<span data-ttu-id="a8e2c-111">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="a8e2c-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="a8e2c-112">[Finans](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="a8e2c-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="a8e2c-113">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a8e2c-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
