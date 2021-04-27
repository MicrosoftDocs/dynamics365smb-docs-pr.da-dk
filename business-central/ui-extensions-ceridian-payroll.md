---
title: Indlæse løn eller løndata ved hjælp af udvidelsen Ceridian-løn
description: Brug denne udvidelse til at importere løntransaktioner fra tjenesterne Ceridian HR/Payroll (US) og Ceridian PowerPay (Canada).
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f2129d26cab8de999ae6ae1e80943ee4066ab50f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787423"
---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="afef0-103">Udvidelsen Ceridian-lønudvidelse</span><span class="sxs-lookup"><span data-stu-id="afef0-103">The Ceridian Payroll Extension</span></span>

<span data-ttu-id="afef0-104">For at tage højde for lønbetalinger og relaterede transaktioner, skal du importere og bogføre finansielle transaktioner, der er foretaget af din lønningssystemudbyder i finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="afef0-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="afef0-105">For at gøre dette skal du først importere en fil, som du modtager fra lønningsystemudbyderen, på siden **Finanskladde**.</span><span class="sxs-lookup"><span data-stu-id="afef0-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="afef0-106">Derefter knytter du de eksterne konti i lønningslistefilen til de relevante finanskonti.</span><span class="sxs-lookup"><span data-stu-id="afef0-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="afef0-107">Til sidst skal du bogføre lønningstransaktionerne i overensstemmelse med kontotilknytningen.</span><span class="sxs-lookup"><span data-stu-id="afef0-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="afef0-108">Du kan finde flere oplysninger i [Importere løntransaktioner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="afef0-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="afef0-109">Udvidelsen Ceridian løn giver dig mulighed at importere løntransaktioner fra tjenesterne Ceridian HR/Payroll (US) og Ceridian PowerPay (Canada).</span><span class="sxs-lookup"><span data-stu-id="afef0-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="afef0-110">Se også</span><span class="sxs-lookup"><span data-stu-id="afef0-110">See Also</span></span>

<span data-ttu-id="afef0-111">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="afef0-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="afef0-112">Finans</span><span class="sxs-lookup"><span data-stu-id="afef0-112">Finance</span></span>](finance.md)  
<span data-ttu-id="afef0-113">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="afef0-113">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]