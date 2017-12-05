---
title: "Bruge udvidelsen Import af Quickbooks-lønfil | Microsoft Docs"
description: "Beskriver, hvordan du kan bruge udvidelsen til at indlæse løn og løntransaktioner fra tjenesten Quickbooks-løn."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 03/29/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: c826ab2f82b2fb0d53339690a2da4978d79ab643
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="the-quickbooks-payroll-file-import-extension-to-dynamics-365-business-edition"></a><span data-ttu-id="6b2e6-103">Udvidelsen Import af Quickbooks-lønfil til Dynamics 365 Business edition</span><span class="sxs-lookup"><span data-stu-id="6b2e6-103">The Quickbooks Payroll File Import Extension to Dynamics 365 Business edition</span></span> 
<span data-ttu-id="6b2e6-104">For at tage højde for lønbetalinger og relaterede transaktioner, skal du importere og bogføre finansielle transaktioner, der er foretaget af din lønningssystemudbyder i finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="6b2e6-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="6b2e6-105">For at gøre dette skal du først importere en fil, som du modtager fra lønningsystemudbyderen, i vinduet **Finanskladde**.</span><span class="sxs-lookup"><span data-stu-id="6b2e6-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="6b2e6-106">Derefter knytter du de eksterne konti i lønningslistefilen til de relevante finanskonti.</span><span class="sxs-lookup"><span data-stu-id="6b2e6-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="6b2e6-107">Til sidst skal du bogføre lønningstransaktionerne i overensstemmelse med kontotilknytningen.</span><span class="sxs-lookup"><span data-stu-id="6b2e6-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="6b2e6-108">Du kan finde flere oplysninger under [Fremgangsmåde: Importere løntransaktioner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="6b2e6-108">For more information, see [How to: Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="6b2e6-109">Udvidelsen for import af Quickbooks-lønfiler giver dig mulighed for at importere løntransaktioner fra Quickbooks-løntjenesten.</span><span class="sxs-lookup"><span data-stu-id="6b2e6-109">The Quickbooks Payroll File Import extension allows you to import payroll transaction from the Quickbooks Payroll service.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b2e6-110">Se også</span><span class="sxs-lookup"><span data-stu-id="6b2e6-110">See Also</span></span>
<span data-ttu-id="6b2e6-111">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="6b2e6-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="6b2e6-112">[Finans](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="6b2e6-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="6b2e6-113">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6b2e6-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

