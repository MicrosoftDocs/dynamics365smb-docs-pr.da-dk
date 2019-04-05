---
title: Sådan gennemgås og tilpasses de eksisterende databasedata | Microsoft Docs
description: Efterhånden som du opretter en konfigurationspakke for en løsning, kan du få vist og tilpasse tilgængelige databasedata, så de passer til debitorens behov. Databasetabellen skal have en tilknyttet side.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: admin-how-to-create-custom-company-configuration-packages
ms.openlocfilehash: 1f49d437e03ecf45a234574530f1e65d93584dea
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792375"
---
# <a name="review-and-customize-existing-database-data"></a><span data-ttu-id="b63e3-104">Gennemgå og tilpasse de eksisterende databasedata</span><span class="sxs-lookup"><span data-stu-id="b63e3-104">Review and Customize Existing Database Data</span></span>
<span data-ttu-id="b63e3-105">Efterhånden som du opretter en konfigurationspakke for en løsning, kan du få vist og tilpasse tilgængelige databasedata, så de passer til debitorens behov.</span><span class="sxs-lookup"><span data-stu-id="b63e3-105">As you create a configuration package for a solution, you can view and customize the available database data to suit your customer needs.</span></span> <span data-ttu-id="b63e3-106">Databasetabellen skal have en tilknyttet side.</span><span class="sxs-lookup"><span data-stu-id="b63e3-106">The database table has to have an associated page.</span></span>  

### <a name="to-customize-data-in-the-database"></a><span data-ttu-id="b63e3-107">Tilpasse data i databasen</span><span class="sxs-lookup"><span data-stu-id="b63e3-107">To customize data in the database</span></span>  

1.  <span data-ttu-id="b63e3-108">I konfigurationsregnearket skal du identificere de tabeller, hvis data du ønsker at se eller tilpasse.</span><span class="sxs-lookup"><span data-stu-id="b63e3-108">In the configuration worksheet, identify the tables whose data that you want to view or customize.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="b63e3-109">Sørg for, at hver enkelt tabel har fået tildelt et side-id.</span><span class="sxs-lookup"><span data-stu-id="b63e3-109">Make sure that each table has a page ID assigned to it.</span></span> <span data-ttu-id="b63e3-110">For standardtabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] angives værdien automatisk.</span><span class="sxs-lookup"><span data-stu-id="b63e3-110">For standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables, this value is automatically filled in.</span></span> <span data-ttu-id="b63e3-111">For brugerdefinerede tabeller skal du angive id'et.</span><span class="sxs-lookup"><span data-stu-id="b63e3-111">For custom tables, you have to provide the ID.</span></span>  

2.  <span data-ttu-id="b63e3-112">Under fanen **Handlinger** i gruppen **Vis** skal du vælge **Databasedata**.</span><span class="sxs-lookup"><span data-stu-id="b63e3-112">On the **Actions** tab, in the **Show** group, choose **Database Data**.</span></span>  

     <span data-ttu-id="b63e3-113">Siden [!INCLUDE[d365fin](includes/d365fin_md.md)] for siden åbnes.</span><span class="sxs-lookup"><span data-stu-id="b63e3-113">The [!INCLUDE[d365fin](includes/d365fin_md.md)] page for the page opens.</span></span>  

3.  <span data-ttu-id="b63e3-114">Gennemse de tilgængelige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="b63e3-114">Review the available information.</span></span> <span data-ttu-id="b63e3-115">Rediger dem efter behov ved at slette poster, der ikke er relevante, eller ved tilføje nye.</span><span class="sxs-lookup"><span data-stu-id="b63e3-115">Modify it as necessary by deleting records that are not relevant or by adding new ones.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b63e3-116">Se også</span><span class="sxs-lookup"><span data-stu-id="b63e3-116">See Also</span></span>  
 [<span data-ttu-id="b63e3-117">Administrere virksomhedskonfigurationen i et regneark</span><span class="sxs-lookup"><span data-stu-id="b63e3-117">Manage Company Configuration in a Worksheet</span></span>](admin-how-to-manage-company-configuration-in-a-worksheet.md)
