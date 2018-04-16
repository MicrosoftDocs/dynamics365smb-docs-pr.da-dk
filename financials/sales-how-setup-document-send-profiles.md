---
title: Oprette foretrukne metoder til at sende salgsdokumenter | Microsoft Docs
description: Bruges til at oprette hver debitors foretrukne metode til at sende salgsdokumenter, f.eks. e-mail, PDF-fil, elektronisk dokument osv.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: f61203ba83b804257ba2cefad786534b83bb44f0
ms.contentlocale: da-dk
ms.lasthandoff: 04/16/2018

---
# <a name="set-up-document-sending-profiles"></a><span data-ttu-id="2389e-103">Konfigurere dokumentafsendelsesprofiler</span><span class="sxs-lookup"><span data-stu-id="2389e-103">Set Up Document Sending Profiles</span></span>
<span data-ttu-id="2389e-104">Du kan oprette hver debitor med en foretrukken metode til afsendelse af salgsdokumenter, så du ikke behøver at vælge en afsendelsesindstilling, hver gang du vælger handlingen **Bogfør og send**.</span><span class="sxs-lookup"><span data-stu-id="2389e-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="2389e-105">I vinduet **Profiler for afsendelse af dokumenter** skal du oprette forskellige afsendelsesprofiler, som du kan vælge i feltet **Dokumentafsendelsesprofil** på et debitorkort.</span><span class="sxs-lookup"><span data-stu-id="2389e-105">In the **Document Sending Profiles** window, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="2389e-106">Du kan markere afkrydsningsfeltet **Standard** for at angive, at dokumentafsendelsesprofilen er standardprofilen for alle debitorer, bortset fra debitorer, hvor feltet **Dokumentafsendelsesprofil** er udfyldt med en anden afsendelsesprofil.</span><span class="sxs-lookup"><span data-stu-id="2389e-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="2389e-107">Når du vælger handlingen **Bogfør og send** i et salgsdokument, viser dialogboksen **Bekræftelse af bogfør og send** den afsendelsesprofil, der bruges, enten den, der er konfigureret for kunden, eller standard for alle debitorer.</span><span class="sxs-lookup"><span data-stu-id="2389e-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="2389e-108">Du kan ændre afsendelsesprofil for salgsdokumentet i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="2389e-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="2389e-109">Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="2389e-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="2389e-110">Sådan konfigurerer du dokumentafsendelsesprofil</span><span class="sxs-lookup"><span data-stu-id="2389e-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="2389e-111">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Dokumentafsendelsesprofiler**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2389e-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="2389e-112">I vinduet **Dokumentafsendelsesprofil** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2389e-112">In the **Document Sending Profiles** window, choose the **New** action.</span></span>
3. <span data-ttu-id="2389e-113">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="2389e-113">Fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="2389e-114">Angive en afsendelsesprofil på et debitorkort</span><span class="sxs-lookup"><span data-stu-id="2389e-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="2389e-115">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2389e-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="2389e-116">Åbn kortet for den debitor, som du vil angive en afsendelsesprofil for.</span><span class="sxs-lookup"><span data-stu-id="2389e-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="2389e-117">I feltet **Dokumentafsendelsesprofil** skal du vælge en profil, du har konfigureret som beskrevet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="2389e-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="2389e-118">Se også</span><span class="sxs-lookup"><span data-stu-id="2389e-118">See Also</span></span>
[<span data-ttu-id="2389e-119">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="2389e-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="2389e-120">Salg</span><span class="sxs-lookup"><span data-stu-id="2389e-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="2389e-121">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2389e-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

