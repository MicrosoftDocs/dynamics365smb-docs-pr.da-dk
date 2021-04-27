---
title: Se tabeloplysninger
description: Få mere at vide om, hvordan du kan få vist oplysninger om databasetabeller direkte fra klientgrænsefladen i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7a01143dd7928d5996c1620676a758ea634bdf5d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776887"
---
# <a name="viewing-table-information"></a><span data-ttu-id="c1f11-103">Sådan ser du tabeloplysninger</span><span class="sxs-lookup"><span data-stu-id="c1f11-103">Viewing Table Information</span></span>

<span data-ttu-id="c1f11-104">Siden **8700-tabeloplysninger** indeholder oplysninger om alle system- og forretningstabeller i en Business Central-løsning.</span><span class="sxs-lookup"><span data-stu-id="c1f11-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="c1f11-105">Siden viser især oplysninger om den mængde data, som tabellerne indeholder.</span><span class="sxs-lookup"><span data-stu-id="c1f11-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="c1f11-106">Disse oplysninger kan være nyttige til fejlfinding i forbindelse med ydeevnen, da du kan se fordelingen af datastørrelse på tværs af tabeller.</span><span class="sxs-lookup"><span data-stu-id="c1f11-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="c1f11-107">Sådan ser du tabeloplysninger</span><span class="sxs-lookup"><span data-stu-id="c1f11-107">Viewing table information</span></span>

<span data-ttu-id="c1f11-108">Hvis du vil åbne denne side, skal du klikke på ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Tabeloplysninger** og derefter vælge det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c1f11-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="c1f11-109">Følgende tabel indeholder en beskrivelse af de oplysninger, der er angivet for hver tabel:</span><span class="sxs-lookup"><span data-stu-id="c1f11-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="c1f11-110">Kolonne</span><span class="sxs-lookup"><span data-stu-id="c1f11-110">Column</span></span>|<span data-ttu-id="c1f11-111">Description</span><span class="sxs-lookup"><span data-stu-id="c1f11-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="c1f11-112">Virksomhedsnavn</span><span class="sxs-lookup"><span data-stu-id="c1f11-112">Company Name</span></span>|<span data-ttu-id="c1f11-113">Navnet på den virksomhed, som tabellen tilhører (hvis det er relevant).</span><span class="sxs-lookup"><span data-stu-id="c1f11-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="c1f11-114">Tabelnavn</span><span class="sxs-lookup"><span data-stu-id="c1f11-114">Table Name</span></span>|<span data-ttu-id="c1f11-115">Navnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="c1f11-115">The name of the table.</span></span>|
|<span data-ttu-id="c1f11-116">Tabelnr.</span><span class="sxs-lookup"><span data-stu-id="c1f11-116">Table No.</span></span>|<span data-ttu-id="c1f11-117">Tabellens ID</span><span class="sxs-lookup"><span data-stu-id="c1f11-117">The ID of the table</span></span>|
|<span data-ttu-id="c1f11-118">Nummer</span><span class="sxs-lookup"><span data-stu-id="c1f11-118">No.</span></span> <span data-ttu-id="c1f11-119">Poster</span><span class="sxs-lookup"><span data-stu-id="c1f11-119">of Records</span></span>|<span data-ttu-id="c1f11-120">Det samlede antal poster, der er gemt i tabellen.</span><span class="sxs-lookup"><span data-stu-id="c1f11-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="c1f11-121">Poststørrelse</span><span class="sxs-lookup"><span data-stu-id="c1f11-121">Record Size</span></span>|<span data-ttu-id="c1f11-122">Den gennemsnitlige poststørrelse i KB/post.</span><span class="sxs-lookup"><span data-stu-id="c1f11-122">The average record size in KB/record.</span></span> <span data-ttu-id="c1f11-123">Værdien beregnes ved hjælp af følgende formel: 1024 (størrelse)/(antal</span><span class="sxs-lookup"><span data-stu-id="c1f11-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="c1f11-124">poster).</span><span class="sxs-lookup"><span data-stu-id="c1f11-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c1f11-125">Se også</span><span class="sxs-lookup"><span data-stu-id="c1f11-125">See Also</span></span>

[<span data-ttu-id="c1f11-126">Inspicere sider</span><span class="sxs-lookup"><span data-stu-id="c1f11-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="c1f11-127">Artikler om ydeevne til udviklere</span><span class="sxs-lookup"><span data-stu-id="c1f11-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]