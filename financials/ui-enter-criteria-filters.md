---
title: "Definere søgekriterier i filtre | Microsoft Docs"
description: "Beskriver, hvordan du arbejder med filtre, f.eks. Quick Filter, for at finjustere resultatet, når du søger efter data."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="entering-criteria-in-filters"></a><span data-ttu-id="39449-103">Indtaste kriterier i filtre</span><span class="sxs-lookup"><span data-stu-id="39449-103">Entering Criteria in Filters</span></span>
<span data-ttu-id="39449-104">Når du vil søge efter data, f.eks debitornavne, adresser eller produktgrupper i grupper, skal du angive kriterier.</span><span class="sxs-lookup"><span data-stu-id="39449-104">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="39449-105">I søgekriterier kan du bruge alle de tal og bogstaver, som du plejer at bruge i det specifikke felt.</span><span class="sxs-lookup"><span data-stu-id="39449-105">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="39449-106">Derudover kan du bruge nogle specialtegn til at filtrere resultaterne yderligere.</span><span class="sxs-lookup"><span data-stu-id="39449-106">In addition, you can use special symbols to further filter the results.</span></span>

## <a name="searching-using-the-quick-filter"></a><span data-ttu-id="39449-107">Søge ved hjælp af Quick Filter</span><span class="sxs-lookup"><span data-stu-id="39449-107">Searching using the Quick Filter</span></span>
<span data-ttu-id="39449-108">Du kan føje filtre til alle sider ved hjælp af Quick Filter.</span><span class="sxs-lookup"><span data-stu-id="39449-108">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="39449-109">Quick Filter aktiveres ved at klikke på ikonet Forstørrelsesglas i øverste højre hjørne af en side.</span><span class="sxs-lookup"><span data-stu-id="39449-109">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="39449-110">Denne filtreringstype bruges til en hurtig indtastning af kriterier.</span><span class="sxs-lookup"><span data-stu-id="39449-110">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="39449-111">Quick Filter giver en nem adgang til at filtrere data ved at angive almindelig tekst, men giver også mange søgekriterieindstillinger.</span><span class="sxs-lookup"><span data-stu-id="39449-111">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="39449-112">Afhængigt af, om du indtaster ren tekst eller tekst, der inkluderer symboler, fungerer Quick Filter forskelligt.</span><span class="sxs-lookup"><span data-stu-id="39449-112">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="39449-113">Hvis du angiver almindelig tekst i søgekriterierne, fortolkes søgekriterierne som en søgning uden skelnen mellem store og små bogstaver, der indeholder bestemt tekst.</span><span class="sxs-lookup"><span data-stu-id="39449-113">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="39449-114">Hvis du indtaster tekst, herunder symboler i søgekriterierne, fortolkes søgekriterierne nøjagtigt, som du har angivet, og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="39449-114">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="39449-115">Quick Filter-kriterier</span><span class="sxs-lookup"><span data-stu-id="39449-115">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="39449-116">Søgekriterier</span><span class="sxs-lookup"><span data-stu-id="39449-116">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="39449-117">Fortolkes som...</span><span class="sxs-lookup"><span data-stu-id="39449-117">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="39449-118">Returnerer...</span><span class="sxs-lookup"><span data-stu-id="39449-118">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="39449-119">man</span><span class="sxs-lookup"><span data-stu-id="39449-119">man</span></span></TD>
    <TD><span data-ttu-id="39449-120">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="39449-120">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="39449-121">Alle poster, der indeholder teksten <b>man</b>, og som ikke skelner mellem små og store bogstaver.</span><span class="sxs-lookup"><span data-stu-id="39449-121">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="39449-122">se</span><span class="sxs-lookup"><span data-stu-id="39449-122">se</span></span></TD>
    <TD><span data-ttu-id="39449-123">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="39449-123">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="39449-124">Alle poster, der indeholder teksten <b>se</b>, og som ikke skelner mellem små og store bogstaver.</span><span class="sxs-lookup"><span data-stu-id="39449-124">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="39449-125">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="39449-125">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="39449-126">Starter med <b>Man</b> og skelner mellem små og store bogstaver.</span><span class="sxs-lookup"><span data-stu-id="39449-126">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="39449-127">Alle poster, der starter med teksten <b>Man</b></span><span class="sxs-lookup"><span data-stu-id="39449-127">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="39449-128">'man'</span><span class="sxs-lookup"><span data-stu-id="39449-128">'man'</span></span></TD>
    <TD><span data-ttu-id="39449-129">En nøjagtig tekst, hvor der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="39449-129">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="39449-130">Alle poster, der nøjagtigt svarer til <b>man</b></span><span class="sxs-lookup"><span data-stu-id="39449-130">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="39449-131">@man*</span><span class="sxs-lookup"><span data-stu-id="39449-131">@man*</span></span> </TD>
    <TD><span data-ttu-id="39449-132">Starter med og uden skelnen mellem små og store bogstaver.</span><span class="sxs-lookup"><span data-stu-id="39449-132">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="39449-133">Alle poster, der starter med <b>man</b></span><span class="sxs-lookup"><span data-stu-id="39449-133">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="39449-134">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="39449-134">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="39449-135">Slutter med og uden skelnen mellem små og store bogstaver.</span><span class="sxs-lookup"><span data-stu-id="39449-135">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="39449-136">Alle poster, der slutter med <b>man</b></span><span class="sxs-lookup"><span data-stu-id="39449-136">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="39449-137">Du kan ikke bruge et jokertegn, når du filtrerer i optællingsfelter, f.eks. feltet **Status** på salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="39449-137">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="39449-138">Hvis du vil angive et filter for denne type felt, kan du angive den numeriske værdi som en filterparameter.</span><span class="sxs-lookup"><span data-stu-id="39449-138">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="39449-139">I feltet **Status** på en salgsordre med værdierne **Åben**, **Frigivet**, **Afventer godkendelse** og **Afventer forudbetaling** kan du f.eks. bruge værdierne, **0**, **1**, **2** og **3** til at filtrere efter disse indstillinger.</span><span class="sxs-lookup"><span data-stu-id="39449-139">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span>  

## <a name="see-also"></a><span data-ttu-id="39449-140">Se også</span><span class="sxs-lookup"><span data-stu-id="39449-140">See Also</span></span>
<span data-ttu-id="39449-141">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="39449-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

