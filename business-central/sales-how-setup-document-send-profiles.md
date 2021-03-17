---
title: Oprette foretrukne metoder til at sende salgsdokumenter | Microsoft Docs
description: Bruges til at oprette hver debitors foretrukne metode til at sende salgsdokumenter, f.eks. e-mail, PDF-fil, elektronisk dokument osv.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 18f9fdf997608cc75fbf2736cc7a834787a8b414
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387557"
---
# <a name="set-up-document-sending-profiles"></a><span data-ttu-id="c06eb-103">Konfigurere dokumentafsendelsesprofiler</span><span class="sxs-lookup"><span data-stu-id="c06eb-103">Set Up Document Sending Profiles</span></span>
<span data-ttu-id="c06eb-104">Du kan oprette hver debitor med en foretrukken metode til afsendelse af salgsdokumenter, så du ikke behøver at vælge en afsendelsesindstilling, hver gang du vælger handlingen **Bogfør og send**.</span><span class="sxs-lookup"><span data-stu-id="c06eb-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="c06eb-105">På siden **Profiler for afsendelse af dokumenter** skal du oprette forskellige afsendelsesprofiler, som du kan vælge i feltet **Dokumentafsendelsesprofil** på et debitorkort.</span><span class="sxs-lookup"><span data-stu-id="c06eb-105">On the **Document Sending Profiles** page, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="c06eb-106">Du kan markere afkrydsningsfeltet **Standard** for at angive, at dokumentafsendelsesprofilen er standardprofilen for alle debitorer, bortset fra debitorer, hvor feltet **Dokumentafsendelsesprofil** er udfyldt med en anden afsendelsesprofil.</span><span class="sxs-lookup"><span data-stu-id="c06eb-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="c06eb-107">Når du vælger handlingen **Bogfør og send** i et salgsdokument, viser dialogboksen **Bekræftelse af bogfør og send** den afsendelsesprofil, der bruges, enten den, der er konfigureret for kunden, eller standard for alle debitorer.</span><span class="sxs-lookup"><span data-stu-id="c06eb-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="c06eb-108">Du kan ændre afsendelsesprofil for salgsdokumentet i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c06eb-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="c06eb-109">Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="c06eb-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHH?rel=0]

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="c06eb-110">Sådan konfigurerer du dokumentafsendelsesprofil</span><span class="sxs-lookup"><span data-stu-id="c06eb-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="c06eb-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Dokumentafsendelsesprofiler**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c06eb-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="c06eb-112">På siden **Dokumentafsendelsesprofil** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c06eb-112">On the **Document Sending Profiles** page, choose the **New** action.</span></span>
3. <span data-ttu-id="c06eb-113">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="c06eb-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="c06eb-114">Angive en afsendelsesprofil på et debitorkort</span><span class="sxs-lookup"><span data-stu-id="c06eb-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="c06eb-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c06eb-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="c06eb-116">Åbn kortet for den debitor, som du vil angive en afsendelsesprofil for.</span><span class="sxs-lookup"><span data-stu-id="c06eb-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="c06eb-117">I feltet **Dokumentafsendelsesprofil** skal du vælge en profil, du har konfigureret som beskrevet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="c06eb-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="c06eb-118">Se også</span><span class="sxs-lookup"><span data-stu-id="c06eb-118">See Also</span></span>
[<span data-ttu-id="c06eb-119">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="c06eb-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="c06eb-120">Salg</span><span class="sxs-lookup"><span data-stu-id="c06eb-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="c06eb-121">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c06eb-121">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]