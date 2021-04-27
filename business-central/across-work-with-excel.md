---
title: Visning og redigering i Excel fra Business Central
description: Få mere at vide om, hvordan du kan åbne siderne i Microsoft Excel fra Business Central for at få en bedre dataanalyse.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7e3abf36444c4701229ffaac7ceade11bb1879cc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786928"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="eaa28-103">Visning og redigering i Excel fra Business Central</span><span class="sxs-lookup"><span data-stu-id="eaa28-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="eaa28-104">Med sider, der viser en liste over poster i rækker og kolonner, f.eks. en liste over debitorer, salgsordrer eller fakturaer, kan du også få vist posterne ved hjælp af Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="eaa28-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="eaa28-105">Du har to muligheder for at gøre dette.</span><span class="sxs-lookup"><span data-stu-id="eaa28-105">To do this, you have two options.</span></span> <span data-ttu-id="eaa28-106">Du kan vælge enten handlingen **Åbn i Excel** eller handlingen **Rediger i Excel** på siden.</span><span class="sxs-lookup"><span data-stu-id="eaa28-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="eaa28-107">Forskellen på de to handlinger er følgende:</span><span class="sxs-lookup"><span data-stu-id="eaa28-107">The differences between the two actions are as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="eaa28-108">Åbn i Excel</span><span class="sxs-lookup"><span data-stu-id="eaa28-108">Open in Excel</span></span>

- <span data-ttu-id="eaa28-109">Med denne handling respekterer Excel eventuelle filtre på siden, som begrænser, hvilke poster der vises.</span><span class="sxs-lookup"><span data-stu-id="eaa28-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="eaa28-110">Excel-projektmappen indeholder de samme rækker og kolonner, der vises på siden i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="eaa28-110">The Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="eaa28-111">Du kan foretage ændringer af posterne i Excel, men du kan ikke publicere ændringerne tilbage til [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="eaa28-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="eaa28-112">Du kan kun gemme ændringerne til en Excel-fil på computeren.</span><span class="sxs-lookup"><span data-stu-id="eaa28-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="eaa28-113">Denne handling fungerer både på Windows og macOS.</span><span class="sxs-lookup"><span data-stu-id="eaa28-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="eaa28-114">For [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø er handlingen **Åbn i Excel** tilgængelig som standard.</span><span class="sxs-lookup"><span data-stu-id="eaa28-114">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="eaa28-115">Men hvis du konfigurerer [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø til redigering af data i Excel, erstattes handlingen **Åbn i Excel** med handlingen **Rediger i Excel**.</span><span class="sxs-lookup"><span data-stu-id="eaa28-115">However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="eaa28-116">Rediger i Excel</span><span class="sxs-lookup"><span data-stu-id="eaa28-116">Edit in Excel</span></span>

- <span data-ttu-id="eaa28-117">Med denne handling respekterer Excel de fleste filtre på siden, der begrænser de viste poster, så Excel-projektmappen indeholder næsten de samme poster og kolonner.</span><span class="sxs-lookup"><span data-stu-id="eaa28-117">With this action, Excel respects most filters on the page that limit the records shown, so the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="eaa28-118">Fordelen ved handlingen **Rediger i Excel** er, at du kan ændre poster i Excel og derefter publicere ændringerne tilbage til [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="eaa28-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="eaa28-119">Det fungerer kun i Windows, ikke i macOS.</span><span class="sxs-lookup"><span data-stu-id="eaa28-119">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="eaa28-120">Du kan skifte den virksomhed, du arbejder med.</span><span class="sxs-lookup"><span data-stu-id="eaa28-120">You can switch the company that you are working with.</span></span> <span data-ttu-id="eaa28-121">Skift virksomhed ved at vælge ikonet **Valgmuligheder** ![Valgmuligheder for Excel-tilføjelsesprogram](media/cogwheel.png "Valgmuligheder for Excel-tilføjelsesprogrammet") i ruden Excel-tilføjelsesprogram og derefter vælge virksomheden i feltet **Virksomhed**.</span><span class="sxs-lookup"><span data-stu-id="eaa28-121">To switch company, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="eaa28-122">Når du skifter virksomhed, skal du sikre, at feltet **Miljø** ikke er tomt.</span><span class="sxs-lookup"><span data-stu-id="eaa28-122">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="eaa28-123">Hvis det er, skal du angive det som en af de tilgængelige indstillinger. Ellers fungerer tilføjelsesprogrammet ikke korrekt.</span><span class="sxs-lookup"><span data-stu-id="eaa28-123">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="eaa28-124">Hvis du foretager ændringer af tilføjelsesprogrammet, skal du genindlæse det for at opdatere forbindelsen.</span><span class="sxs-lookup"><span data-stu-id="eaa28-124">If you make changes to the add-in, you must reload it to update the connection.</span></span> <span data-ttu-id="eaa28-125">Hvis du vil genindlæse, skal du bruge ![menuen Excel-tilføjelsesprogram](media/excel-addin-menu.png "Menuen Excel-tilføjelsesprogram") i øverste højre hjørne af tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="eaa28-125">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span> <span data-ttu-id="eaa28-126">Hvis du ikke kan indlæse tilføjelsesprogrammet, skal du tale med administratoren.</span><span class="sxs-lookup"><span data-stu-id="eaa28-126">If you cannot load the add-in, talk to your administrator.</span></span> <span data-ttu-id="eaa28-127">Hvis du er administrator, skal du se [Konfigurere Excel-tilføjelsesprogrammet til redigering af Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="eaa28-127">If you are the administrator, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="eaa28-128">For [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø er handlingen **Rediger i Excel** kun tilgængelig, hvis Excel-tilføjelsesprogrammet er konfigureret af administratoren, og kun tilgængelig til webklienten.</span><span class="sxs-lookup"><span data-stu-id="eaa28-128">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="eaa28-129">Til administratorer, hvis du vil vide, hvordan du installerer Excel-tilføjelsesprogrammet, skal du se [Konfigurere Excel-tilføjelsesprogrammet til redigering af Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="eaa28-129">For administrators, if you want to learn how to install the Excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="eaa28-130">Se forskellene mellem indstillingerne</span><span class="sxs-lookup"><span data-stu-id="eaa28-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="eaa28-131">Se relateret træning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="eaa28-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="eaa28-132">Se også</span><span class="sxs-lookup"><span data-stu-id="eaa28-132">See Also</span></span>

[<span data-ttu-id="eaa28-133">Analysere regnskaber i Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="eaa28-133">Analyzing Financial Statements in Microsoft Excel</span></span>](finance-analyze-excel.md)  
[<span data-ttu-id="eaa28-134">Arbejde med Business Central</span><span class="sxs-lookup"><span data-stu-id="eaa28-134">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="eaa28-135">Forbedringer af Excel-integration i frigivelsesbølge 2 i 2019</span><span class="sxs-lookup"><span data-stu-id="eaa28-135">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]