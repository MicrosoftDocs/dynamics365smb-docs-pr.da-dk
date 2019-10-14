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
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: 2474f83fd9fa137b40756a3d07ac025208f3ac6c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308256"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="8069b-103">Visning og redigering i Excel fra Business Central</span><span class="sxs-lookup"><span data-stu-id="8069b-103">Viewing and Editing in Excel From Business Central</span></span> 

<span data-ttu-id="8069b-104">Med sider, der viser en liste over poster i rækker og kolonner, f.eks. en liste over debitorer, salgsordrer eller fakturaer, kan du også få vist posterne ved hjælp af Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="8069b-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="8069b-105">Du har to muligheder for at gøre dette.</span><span class="sxs-lookup"><span data-stu-id="8069b-105">To do this, you have two options.</span></span> <span data-ttu-id="8069b-106">Du kan vælge enten handlingen **Åbn i Excel** eller handlingen **Rediger i Excel** på siden.</span><span class="sxs-lookup"><span data-stu-id="8069b-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="8069b-107">Forskellen på de to handlinger er følgende:</span><span class="sxs-lookup"><span data-stu-id="8069b-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="8069b-108">Åbn i Excel</span><span class="sxs-lookup"><span data-stu-id="8069b-108">Open in Excel</span></span>

-    <span data-ttu-id="8069b-109">Med denne handling respekterer Excel eventuelle filtre på siden, som begrænser, hvilke poster der vises.</span><span class="sxs-lookup"><span data-stu-id="8069b-109">With this action, Excel respects any filters on the page the limit the records shown.</span></span> <span data-ttu-id="8069b-110">Det betyder, at Excel-projektmappen indeholder de samme rækker og kolonner, der vises på den side i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="8069b-110">This means that the Excel workbook will contain the same rows and columns that appear on the the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="8069b-111">Du kan foretage ændringer af posterne i Excel, men du kan ikke publicere ændringerne tilbage til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="8069b-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="8069b-112">Du kan kun gemme ændringerne til en Excel-fil på computeren.</span><span class="sxs-lookup"><span data-stu-id="8069b-112">You can only save the changes to Excel file on your computer.</span></span> 

-    <span data-ttu-id="8069b-113">Denne handling fungerer både på Windows og macOS.</span><span class="sxs-lookup"><span data-stu-id="8069b-113">This action works on both on Windows and macOS.</span></span> 

>[!NOTE]
><span data-ttu-id="8069b-114">For [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø er handlingen **Åbn i Excel** ikke tilgængelig, hvis handlingen **Rediger i Excel** er det.</span><span class="sxs-lookup"><span data-stu-id="8069b-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is not available if the **Edit in Excel** action is.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="8069b-115">Rediger i Excel</span><span class="sxs-lookup"><span data-stu-id="8069b-115">Edit in Excel</span></span>

-    <span data-ttu-id="8069b-116">Med denne handling respekterer Excel-projektmappen ikke eventuelle filtre på siden, som begrænser, hvilke poster der vises.</span><span class="sxs-lookup"><span data-stu-id="8069b-116">With this action, the Excel workbook does not respect filters on the page the limit the records shown.</span></span> <span data-ttu-id="8069b-117">Det betyder, at Excel-projektmappen indeholder alle de tilgængelige poster og kolonner, uanset hvad der vises på siden.</span><span class="sxs-lookup"><span data-stu-id="8069b-117">This means that the Excel workbook will contain all the available records and columns, regardless of what is shown on the page.</span></span> 

-    <span data-ttu-id="8069b-118">Fordelen ved handlingen **Rediger i Excel** er, at du kan ændre poster i Excel og derefter publicere ændringerne tilbage til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="8069b-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="8069b-119">Det fungerer kun i Windows, ikke i macOS.</span><span class="sxs-lookup"><span data-stu-id="8069b-119">It only works on Windows; not macOS.</span></span>

>[!NOTE]
><span data-ttu-id="8069b-120">For [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø, er handlingen **Rediger i Excel** kun tilgængelig, hvis Excel-tilføjelsesprogrammet er installeret af administratoren.</span><span class="sxs-lookup"><span data-stu-id="8069b-120">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been installed by your administrator.</span></span> <span data-ttu-id="8069b-121">Til administratorer, hvis du vil vide, hvordan du installerer Excel-tilføjelsesprogrammet, skal du se [Konfigurere Excel-tilføjelsesprogrammet](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="8069b-121">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="8069b-122">Se forskellene mellem indstillingerne</span><span class="sxs-lookup"><span data-stu-id="8069b-122">See the differences between the options</span></span> 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="8069b-123">Se også</span><span class="sxs-lookup"><span data-stu-id="8069b-123">See Also</span></span>
[<span data-ttu-id="8069b-124">Arbejde med Business Central</span><span class="sxs-lookup"><span data-stu-id="8069b-124">Working with Business Central</span></span>](ui-work-product.md)  
