---
title: Konfigurere kontoplanen | Microsoft Docs
description: "Du kan ændre standardkontiene i kontoplanen, og du kan tilføje nye konti."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 1d0130dde256706460e58e5efc445bc5f4d5c595
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="1a475-103">Konfigurere eller ændre kontoplanen</span><span class="sxs-lookup"><span data-stu-id="1a475-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="1a475-104">Kontoplanen viser de finanskonti, hvor dine finansielle data er gemt.</span><span class="sxs-lookup"><span data-stu-id="1a475-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="1a475-105"> indeholder en standardkontoplan, der er klar til at understøtte din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="1a475-105"> includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="1a475-106">Men du kan ændre standardkontiene, og du kan tilføje nye konti.</span><span class="sxs-lookup"><span data-stu-id="1a475-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="1a475-107">Tilføjelse eller ændring af konti</span><span class="sxs-lookup"><span data-stu-id="1a475-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="1a475-108">Fra kontoplanen kan du åbne hver finanskonto og tilføje eller ændre indstillinger for hver konto.</span><span class="sxs-lookup"><span data-stu-id="1a475-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="1a475-109">Du kan slette en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="1a475-109">You can delete a general ledger account.</span></span> <span data-ttu-id="1a475-110">Men før du sletter den, skal følgende være opfyldt:</span><span class="sxs-lookup"><span data-stu-id="1a475-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="1a475-111">Saldoen på kontoen skal være nul.</span><span class="sxs-lookup"><span data-stu-id="1a475-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="1a475-112">Feltet **Tillad sletning af finanskonti før** skal være indstillet i vinduet **Opsætning af Finans**, og der må ikke bogføres poster på kontoen på eller efter den pågældende dato.</span><span class="sxs-lookup"><span data-stu-id="1a475-112">The **Allow G/L Acc. Deletion Before** field must be set in the **General Ledger Setup** window, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="1a475-113">Hvis feltet **Kontroller brug af finanskonto** i vinduet **Opsætning af Finans** er markeret, må kontoen ikke bruges i nogen bogføringsgrupper eller bogføringsopsætning.</span><span class="sxs-lookup"><span data-stu-id="1a475-113">If the **Check G/L Account Usage** field in the **General Ledger Setup** window is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="1a475-114"> forhindrer, at du kan slette en finanskonto, der indeholder data, der skal bruges i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="1a475-114"> will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1a475-115">Se også</span><span class="sxs-lookup"><span data-stu-id="1a475-115">See Also</span></span>
[<span data-ttu-id="1a475-116">Finans- og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="1a475-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="1a475-117">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="1a475-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="1a475-118">Arbejde med dimensioner</span><span class="sxs-lookup"><span data-stu-id="1a475-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="1a475-119">Importere fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="1a475-119">Importing from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="1a475-120">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1a475-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

