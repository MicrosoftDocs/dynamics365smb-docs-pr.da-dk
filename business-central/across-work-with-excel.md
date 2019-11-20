---
title: Visning og redigering i Excel fra Business Central | Microsoft Docs
description: Få mere at vide om, hvordan du kan åbne siderne i Microsoft Excel fra Business Central for at få en bedre dataanalyse.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/24/2019
ms.author: jswymer
ms.openlocfilehash: 71b4e5b7124f929255f1374b38cfbe28c9f12d2b
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692796"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="147a6-103">Visning og redigering i Excel fra Business Central</span><span class="sxs-lookup"><span data-stu-id="147a6-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="147a6-104">Med sider, der viser en liste over poster i rækker og kolonner, f.eks. en liste over debitorer, salgsordrer eller fakturaer, kan du også få vist posterne ved hjælp af Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="147a6-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="147a6-105">Du har to muligheder for at gøre dette.</span><span class="sxs-lookup"><span data-stu-id="147a6-105">To do this, you have two options.</span></span> <span data-ttu-id="147a6-106">Du kan vælge enten handlingen **Åbn i Excel** eller handlingen **Rediger i Excel** på siden.</span><span class="sxs-lookup"><span data-stu-id="147a6-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="147a6-107">Forskellen på de to handlinger er følgende:</span><span class="sxs-lookup"><span data-stu-id="147a6-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="147a6-108">Åbn i Excel</span><span class="sxs-lookup"><span data-stu-id="147a6-108">Open in Excel</span></span>

- <span data-ttu-id="147a6-109">Med denne handling respekterer Excel eventuelle filtre på siden, som begrænser, hvilke poster der vises.</span><span class="sxs-lookup"><span data-stu-id="147a6-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="147a6-110">Det betyder, at Excel-projektmappen indeholder de samme rækker og kolonner, der vises på siden i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="147a6-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="147a6-111">Du kan foretage ændringer af posterne i Excel, men du kan ikke publicere ændringerne tilbage til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="147a6-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="147a6-112">Du kan kun gemme ændringerne til en Excel-fil på computeren.</span><span class="sxs-lookup"><span data-stu-id="147a6-112">You can only save the changes to Excel file on your computer.</span></span> 

- <span data-ttu-id="147a6-113">Denne handling fungerer både på Windows og macOS.</span><span class="sxs-lookup"><span data-stu-id="147a6-113">This action works on both on Windows and macOS.</span></span> 

> [!NOTE]
> <span data-ttu-id="147a6-114">For [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø er handlingen **Åbn i Excel** tilgængelig som standard.</span><span class="sxs-lookup"><span data-stu-id="147a6-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="147a6-115">Men hvis du konfigurerer [!INCLUDE [prodshort](includes/prodshort.md)] i det lokale miljø til redigering af data i Excel, erstattes handlingen **Åbn i Excel** med handlingen **Rediger i Excel**.</span><span class="sxs-lookup"><span data-stu-id="147a6-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="147a6-116">Rediger i Excel</span><span class="sxs-lookup"><span data-stu-id="147a6-116">Edit in Excel</span></span>

- <span data-ttu-id="147a6-117">Med denne handling respekterer Excel de fleste filtre på siden, som begrænser, hvilke poster der vises.</span><span class="sxs-lookup"><span data-stu-id="147a6-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="147a6-118">Det betyder, at Excel-projektmappen indeholder næsten de samme poster og kolonner.</span><span class="sxs-lookup"><span data-stu-id="147a6-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="147a6-119">Fordelen ved handlingen **Rediger i Excel** er, at du kan ændre poster i Excel og derefter publicere ændringerne tilbage til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="147a6-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="147a6-120">Det fungerer kun i Windows, ikke i macOS.</span><span class="sxs-lookup"><span data-stu-id="147a6-120">It only works on Windows; not macOS.</span></span>

<span data-ttu-id="147a6-121">Dette blev udvidet i frigivelsesbølge 2 i 2019.</span><span class="sxs-lookup"><span data-stu-id="147a6-121">This was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="147a6-122">Du kan finde flere oplysninger [Forbedringer af Excel-integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)af Excel.</span><span class="sxs-lookup"><span data-stu-id="147a6-122">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="147a6-123">For [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø, er handlingen **Rediger i Excel** kun tilgængelig, hvis Excel-tilføjelsesprogrammet er konfigureret af administratoren.</span><span class="sxs-lookup"><span data-stu-id="147a6-123">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator.</span></span> <span data-ttu-id="147a6-124">Til administratorer, hvis du vil vide, hvordan du installerer Excel-tilføjelsesprogrammet, skal du se [Konfigurere Excel-tilføjelsesprogrammet til redigering af Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="147a6-124">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="147a6-125">For [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø er denne funktion er kun tilgængelig for webklienten.</span><span class="sxs-lookup"><span data-stu-id="147a6-125">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, this feature is only available for the Web client.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="147a6-126">Se forskellene mellem indstillingerne</span><span class="sxs-lookup"><span data-stu-id="147a6-126">See the differences between the options</span></span> 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="147a6-127">Se også</span><span class="sxs-lookup"><span data-stu-id="147a6-127">See Also</span></span>
[<span data-ttu-id="147a6-128">Arbejde med Business Central</span><span class="sxs-lookup"><span data-stu-id="147a6-128">Working with Business Central</span></span>](ui-work-product.md)  
