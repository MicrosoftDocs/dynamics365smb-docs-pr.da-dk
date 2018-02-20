---
title: "Søgning efter data og angivelse af filtreringskriterier | Microsoft Docs"
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
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11d7ef56e980ba263dba6328b2f2f08b86410242
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="searching-filtering-and-sorting-data"></a><span data-ttu-id="a868c-103">Søgning i, filtrering og sortering af data</span><span class="sxs-lookup"><span data-stu-id="a868c-103">Searching, Filtering, and Sorting Data</span></span>
<span data-ttu-id="a868c-104">Der er et par ting, du kan gøre som en hjælp til at finde, identificere og scanne poster på en liste.</span><span class="sxs-lookup"><span data-stu-id="a868c-104">There are a few things that you can do that will help you find, pinpoint, and scan records in a list.</span></span> <span data-ttu-id="a868c-105">Disse omfatter sortering, søgning og filtrering.</span><span class="sxs-lookup"><span data-stu-id="a868c-105">These include sorting, searching and filtering.</span></span>

<span data-ttu-id="a868c-106">Når du vil søge efter data, f.eks debitornavne, adresser eller produktgrupper i grupper, skal du angive kriterier.</span><span class="sxs-lookup"><span data-stu-id="a868c-106">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="a868c-107">I søgekriterier kan du bruge alle de tal og bogstaver, som du plejer at bruge i det specifikke felt.</span><span class="sxs-lookup"><span data-stu-id="a868c-107">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="a868c-108">Derudover kan du bruge nogle specialtegn til at filtrere resultaterne yderligere.</span><span class="sxs-lookup"><span data-stu-id="a868c-108">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="a868c-109">Der kan søges på to måder: Ved hjælp af Quick Filter eller med kolonnefiltre.</span><span class="sxs-lookup"><span data-stu-id="a868c-109">There are two ways to search: using the Quick Filter or column filters.</span></span>

## <a name="sorting"></a><span data-ttu-id="a868c-110">Sortering</span><span class="sxs-lookup"><span data-stu-id="a868c-110">Sorting</span></span>
<span data-ttu-id="a868c-111">Sortering gør det nemt og hurtigt for dig at overskue dine oplysninger.</span><span class="sxs-lookup"><span data-stu-id="a868c-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="a868c-112">Hvis du har mange kunder, f.eks. kan du vælge at sortere dem efter **Kundenr.**, **Debitorbogføringsgruppe**, **Valutakode**, **Lande-/områdekode** eller **Momsregistreringsnr.** for at få det nødvendige overblik.</span><span class="sxs-lookup"><span data-stu-id="a868c-112">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="a868c-113">Hvis du vil sortere en liste, kan du enten vælge en kolonneoverskriftstekst, hvor du kan skifte mellem stigende og faldende rækkefølge, eller du kan vælge den lille nedadgående pil i kolonneoverskriften og derefter vælge **Stigende** eller **Faldende**.</span><span class="sxs-lookup"><span data-stu-id="a868c-113">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small downs arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="a868c-114">Sortering understøttes ikke af billeder, BLOB-felter, FlowFilters og felter, der ikke tilhører en tabel.</span><span class="sxs-lookup"><span data-stu-id="a868c-114">Sorting is not supported images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching-by-using-the-quick-filter"></a><span data-ttu-id="a868c-115">Søge ved hjælp af Quick Filter</span><span class="sxs-lookup"><span data-stu-id="a868c-115">Searching by using the Quick Filter</span></span>
<span data-ttu-id="a868c-116">Du kan føje filtre til alle sider ved hjælp af Quick Filter.</span><span class="sxs-lookup"><span data-stu-id="a868c-116">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="a868c-117">Quick Filter aktiveres ved at klikke på ikonet Forstørrelsesglas i øverste højre hjørne af en side.</span><span class="sxs-lookup"><span data-stu-id="a868c-117">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="a868c-118">Denne filtreringstype bruges til en hurtig indtastning af kriterier.</span><span class="sxs-lookup"><span data-stu-id="a868c-118">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="a868c-119">Quick Filter giver en nem adgang til at filtrere data ved at angive almindelig tekst, men giver også mange søgekriterieindstillinger.</span><span class="sxs-lookup"><span data-stu-id="a868c-119">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="a868c-120">Afhængigt af, om du indtaster ren tekst eller tekst, der inkluderer symboler, fungerer Quick Filter forskelligt.</span><span class="sxs-lookup"><span data-stu-id="a868c-120">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="a868c-121">Hvis du angiver almindelig tekst i søgekriterierne, fortolkes søgekriterierne som en søgning uden skelnen mellem store og små bogstaver, der indeholder bestemt tekst.</span><span class="sxs-lookup"><span data-stu-id="a868c-121">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="a868c-122">Hvis du indtaster tekst, herunder symboler i søgekriterierne, fortolkes søgekriterierne nøjagtigt, som du har angivet, og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="a868c-122">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="a868c-123">Quick Filter-kriterier</span><span class="sxs-lookup"><span data-stu-id="a868c-123">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="a868c-124">Søgekriterier</span><span class="sxs-lookup"><span data-stu-id="a868c-124">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="a868c-125">Fortolkes som...</span><span class="sxs-lookup"><span data-stu-id="a868c-125">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="a868c-126">Returnerer...</span><span class="sxs-lookup"><span data-stu-id="a868c-126">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="a868c-127">man</span><span class="sxs-lookup"><span data-stu-id="a868c-127">man</span></span></TD>
    <TD><span data-ttu-id="a868c-128">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="a868c-128">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="a868c-129">Alle poster, der indeholder teksten <b>man</b>, og som ikke skelner mellem små og store bogstaver.</span><span class="sxs-lookup"><span data-stu-id="a868c-129">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="a868c-130">se</span><span class="sxs-lookup"><span data-stu-id="a868c-130">se</span></span></TD>
    <TD><span data-ttu-id="a868c-131">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="a868c-131">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="a868c-132">Alle poster, der indeholder teksten <b>se</b>, og som ikke skelner mellem små og store bogstaver.</span><span class="sxs-lookup"><span data-stu-id="a868c-132">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="a868c-133">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="a868c-133">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="a868c-134">Starter med <b>Man</b> og skelner mellem små og store bogstaver.</span><span class="sxs-lookup"><span data-stu-id="a868c-134">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="a868c-135">Alle poster, der starter med teksten <b>Man</b></span><span class="sxs-lookup"><span data-stu-id="a868c-135">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="a868c-136">'man'</span><span class="sxs-lookup"><span data-stu-id="a868c-136">'man'</span></span></TD>
    <TD><span data-ttu-id="a868c-137">En nøjagtig tekst, hvor der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="a868c-137">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="a868c-138">Alle poster, der nøjagtigt svarer til <b>man</b></span><span class="sxs-lookup"><span data-stu-id="a868c-138">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="a868c-139">@man\*</span><span class="sxs-lookup"><span data-stu-id="a868c-139">@man\*</span></span> </TD>
    <TD><span data-ttu-id="a868c-140">Starter med og uden skelnen mellem små og store bogstaver.</span><span class="sxs-lookup"><span data-stu-id="a868c-140">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="a868c-141">Alle poster, der starter med <b>man</b></span><span class="sxs-lookup"><span data-stu-id="a868c-141">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="a868c-142">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="a868c-142">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="a868c-143">Slutter med og uden skelnen mellem små og store bogstaver.</span><span class="sxs-lookup"><span data-stu-id="a868c-143">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="a868c-144">Alle poster, der slutter med <b>man</b></span><span class="sxs-lookup"><span data-stu-id="a868c-144">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="a868c-145">Du kan ikke bruge et jokertegn, når du filtrerer i optællingsfelter, f.eks. feltet **Status** på salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="a868c-145">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="a868c-146">Hvis du vil angive et filter for denne type felt, kan du angive den numeriske værdi som en filterparameter.</span><span class="sxs-lookup"><span data-stu-id="a868c-146">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="a868c-147">I feltet **Status** på en salgsordre med værdierne **Åben**, **Frigivet**, **Afventer godkendelse** og **Afventer forudbetaling** kan du f.eks. bruge værdierne, **0**, **1**, **2** og **3** til at filtrere efter disse indstillinger.</span><span class="sxs-lookup"><span data-stu-id="a868c-147">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span> 

## <a name="searching-by-using-column-filters"></a><span data-ttu-id="a868c-148">Søge ved hjælp af kolonnefiltre</span><span class="sxs-lookup"><span data-stu-id="a868c-148">Searching by using column Filters</span></span>
<span data-ttu-id="a868c-149">Du kan tilføje et filter til en eller flere kolonner på en liste.</span><span class="sxs-lookup"><span data-stu-id="a868c-149">You can add a filter on one or more columns in a list.</span></span> <span data-ttu-id="a868c-150">Filtrering på kolonner er mere fleksibelt og omfattede end Quick Filter.</span><span class="sxs-lookup"><span data-stu-id="a868c-150">Filtering on columns is more flexible and enhanced than the Quick Filter.</span></span> 

### <a name="to-add-a-filter-on-a-column"></a><span data-ttu-id="a868c-151">Sådan tilføjes et filter på en kolonne</span><span class="sxs-lookup"><span data-stu-id="a868c-151">To add a filter on a column</span></span>
1.  <span data-ttu-id="a868c-152">Før du tilføjer et filter, skal du vælge ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Pil til venstre Vis som liste") for at skifte til listevisningen.</span><span class="sxs-lookup"><span data-stu-id="a868c-152">Before you add a filter, choose ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to change to the list view.</span></span>
2. <span data-ttu-id="a868c-153">Vælg den nedadgående pil i kolonneoverskriften, og vælg derefter **Filter**.</span><span class="sxs-lookup"><span data-stu-id="a868c-153">Choose the downwards arrow in the column heading, and then choose **Filter**.</span></span>
3. <span data-ttu-id="a868c-154">Gør ét af følgende:</span><span class="sxs-lookup"><span data-stu-id="a868c-154">Do one of the following:</span></span> 
  -  <span data-ttu-id="a868c-155">Vælg *...* ud for feltet for at vælge en værdi på en liste.</span><span class="sxs-lookup"><span data-stu-id="a868c-155">Choose *...* next to the box to select a value from a list.</span></span>
  -  <span data-ttu-id="a868c-156">Angiv filterkriterier i feltet.</span><span class="sxs-lookup"><span data-stu-id="a868c-156">Enter filter criteria in the box.</span></span> <span data-ttu-id="a868c-157">Se næste afsnit kan få flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="a868c-157">See the next section for details.</span></span>
4. <span data-ttu-id="a868c-158">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="a868c-158">Choose the **OK** button.</span></span>

## <a name="filter-criteria-and-symbols"></a><span data-ttu-id="a868c-159">Filterkriterier og -symboler</span><span class="sxs-lookup"><span data-stu-id="a868c-159">Filter criteria and symbols</span></span>
<span data-ttu-id="a868c-160">Når du angiver kriterier, kan du bruge alle de tal og bogstaver, som du plejer at bruger i feltet.</span><span class="sxs-lookup"><span data-stu-id="a868c-160">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="a868c-161">Derudover kan du bruge nogle specialtegn til at filtrere resultaterne yderligere.</span><span class="sxs-lookup"><span data-stu-id="a868c-161">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="a868c-162">Følgende tabeller viser de tegn, der kan bruges i filtre.</span><span class="sxs-lookup"><span data-stu-id="a868c-162">The following tables show the symbols which can be used in filters.</span></span>  
  
> [!IMPORTANT]  
>  <span data-ttu-id="a868c-163">Der kan være tilfælde, hvor feltværdierne indeholder disse symboler, og du vil filtrere efter dem.</span><span class="sxs-lookup"><span data-stu-id="a868c-163">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="a868c-164">Hvis du vil gøre dette, skal du medtage det filterudtryk, der indeholder symbolet i anførselstegn (").</span><span class="sxs-lookup"><span data-stu-id="a868c-164">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="a868c-165">Hvis du f.eks. vil filtrere efter poster, der starter med teksten *S&R*, er filterudtrykket **S&R\*'**.</span><span class="sxs-lookup"><span data-stu-id="a868c-165">For example, if you want to filter on records that start with the text *S&R*, the filter expression is **'S&R\*'**.</span></span>  
  
### <a name="-interval"></a><span data-ttu-id="a868c-166">(..) Interval</span><span class="sxs-lookup"><span data-stu-id="a868c-166">(..) Interval</span></span>  
  
|<span data-ttu-id="a868c-167">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-167">Sample Expression</span></span>|<span data-ttu-id="a868c-168">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-168">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-169">1100..2100</span><span class="sxs-lookup"><span data-stu-id="a868c-169">1100..2100</span></span>|<span data-ttu-id="a868c-170">Tal fra 1100 til og med 2100.</span><span class="sxs-lookup"><span data-stu-id="a868c-170">Numbers 1100 through 2100</span></span>|  
|<span data-ttu-id="a868c-171">..2500</span><span class="sxs-lookup"><span data-stu-id="a868c-171">..2500</span></span>|<span data-ttu-id="a868c-172">Konti til og med 2500</span><span class="sxs-lookup"><span data-stu-id="a868c-172">Up to and including 2500</span></span>|  
|<span data-ttu-id="a868c-173">..31-12-00</span><span class="sxs-lookup"><span data-stu-id="a868c-173">..12 31 00</span></span>|<span data-ttu-id="a868c-174">Datoer til og med 31-12-00.</span><span class="sxs-lookup"><span data-stu-id="a868c-174">Dates up to and including 12 31 00</span></span>|  
|<span data-ttu-id="a868c-175">P8..</span><span class="sxs-lookup"><span data-stu-id="a868c-175">P8..</span></span>|<span data-ttu-id="a868c-176">Oplysninger for regnskabsperiode 8 og frem</span><span class="sxs-lookup"><span data-stu-id="a868c-176">Information for accounting period 8 and thereafter</span></span>|  
|<span data-ttu-id="a868c-177">..23</span><span class="sxs-lookup"><span data-stu-id="a868c-177">..23</span></span>|<span data-ttu-id="a868c-178">Fra begyndelsesdatoen til 23-aktuel måned-aktuelt år 23.59.59</span><span class="sxs-lookup"><span data-stu-id="a868c-178">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|<span data-ttu-id="a868c-179">23..</span><span class="sxs-lookup"><span data-stu-id="a868c-179">23..</span></span>|<span data-ttu-id="a868c-180">Fra 23-aktuel måned-aktuelt år 0.00.00 til sluttidspunktet</span><span class="sxs-lookup"><span data-stu-id="a868c-180">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|<span data-ttu-id="a868c-181">22..23</span><span class="sxs-lookup"><span data-stu-id="a868c-181">22..23</span></span>|<span data-ttu-id="a868c-182">Fra den 23-aktuel måned-aktuelt år 0.00.00 til 22-aktuel måned-aktuelt år 22.59.59</span><span class="sxs-lookup"><span data-stu-id="a868c-182">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  
  
### <a name="124-eitheror"></a><span data-ttu-id="a868c-183">(&#124;) Enten/eller</span><span class="sxs-lookup"><span data-stu-id="a868c-183">(&#124;) Either/or</span></span>  
  
|<span data-ttu-id="a868c-184">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-184">Sample Expression</span></span>|<span data-ttu-id="a868c-185">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-185">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-186">1200&#124;1300</span><span class="sxs-lookup"><span data-stu-id="a868c-186">1200&#124;1300</span></span>|<span data-ttu-id="a868c-187">Tal med 1200 eller 1300.</span><span class="sxs-lookup"><span data-stu-id="a868c-187">Numbers with 1200 or 1300</span></span>|  
  
### <a name="-not-equal-to"></a><span data-ttu-id="a868c-188">(<>) Ikke lig med</span><span class="sxs-lookup"><span data-stu-id="a868c-188">(<>) Not equal to</span></span>  
  
|<span data-ttu-id="a868c-189">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-189">Sample Expression</span></span>|<span data-ttu-id="a868c-190">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-190">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-191"><>0</span><span class="sxs-lookup"><span data-stu-id="a868c-191"><>0</span></span>|<span data-ttu-id="a868c-192">Alle tal undtagen 0</span><span class="sxs-lookup"><span data-stu-id="a868c-192">All numbers except 0</span></span><br /><br /> <span data-ttu-id="a868c-193">I SQL Server Option kan du kombinere dette symbol med et udtryk med jokertegn.</span><span class="sxs-lookup"><span data-stu-id="a868c-193">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="a868c-194"><>A\* betyder f.eks. ikke lig med tekst, der starter med A.</span><span class="sxs-lookup"><span data-stu-id="a868c-194">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  
  
### <a name="-greater-than"></a><span data-ttu-id="a868c-195">(>) Større end</span><span class="sxs-lookup"><span data-stu-id="a868c-195">(>) Greater than</span></span>  
  
|<span data-ttu-id="a868c-196">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-196">Sample Expression</span></span>|<span data-ttu-id="a868c-197">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-197">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-198">>1200</span><span class="sxs-lookup"><span data-stu-id="a868c-198">>1200</span></span>|<span data-ttu-id="a868c-199">Tal større end 1200</span><span class="sxs-lookup"><span data-stu-id="a868c-199">Numbers greater than 1200</span></span>|  
  
### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="a868c-200">(>=) Større end eller lig med</span><span class="sxs-lookup"><span data-stu-id="a868c-200">(>=) Greater than or equal to</span></span>  
  
|<span data-ttu-id="a868c-201">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-201">Sample Expression</span></span>|<span data-ttu-id="a868c-202">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-202">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-203">>=1200</span><span class="sxs-lookup"><span data-stu-id="a868c-203">>=1200</span></span>|<span data-ttu-id="a868c-204">Tal lig med eller større end 1200</span><span class="sxs-lookup"><span data-stu-id="a868c-204">Numbers greater than or equal to 1200</span></span>|  
  
### <a name="-less-than"></a><span data-ttu-id="a868c-205">(<) Mindre end</span><span class="sxs-lookup"><span data-stu-id="a868c-205">(<) Less than</span></span>  
  
|<span data-ttu-id="a868c-206">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-206">Sample Expression</span></span>|<span data-ttu-id="a868c-207">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-207">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-208"><1200</span><span class="sxs-lookup"><span data-stu-id="a868c-208"><1200</span></span>|<span data-ttu-id="a868c-209">Tal mindre end 1200</span><span class="sxs-lookup"><span data-stu-id="a868c-209">Numbers less than 1200</span></span>|  
  
### <a name="-less-than-or-equal-to"></a><span data-ttu-id="a868c-210">(<=) Mindre end eller lig med</span><span class="sxs-lookup"><span data-stu-id="a868c-210">(<=) Less than or equal to</span></span>  
  
|<span data-ttu-id="a868c-211">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-211">Sample Expression</span></span>|<span data-ttu-id="a868c-212">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-212">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-213"><=1200</span><span class="sxs-lookup"><span data-stu-id="a868c-213"><=1200</span></span>|<span data-ttu-id="a868c-214">Tal lig med eller mindre end 1200</span><span class="sxs-lookup"><span data-stu-id="a868c-214">Numbers less than or equal to 1200</span></span>|  
  
### <a name="-and"></a><span data-ttu-id="a868c-215">(&) Og</span><span class="sxs-lookup"><span data-stu-id="a868c-215">(&) And</span></span>  
  
|<span data-ttu-id="a868c-216">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-216">Sample Expression</span></span>|<span data-ttu-id="a868c-217">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-217">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-218">>200&<1200</span><span class="sxs-lookup"><span data-stu-id="a868c-218">>200&<1200</span></span>|<span data-ttu-id="a868c-219">Tal større end 200 og mindre end 1200</span><span class="sxs-lookup"><span data-stu-id="a868c-219">Numbers greater than 200 and less than 1200</span></span>|  
  
### <a name="-an-exact-character-match"></a><span data-ttu-id="a868c-220">('') Tegn, der stemmer nøjagtigt overens</span><span class="sxs-lookup"><span data-stu-id="a868c-220">('') An exact character match</span></span>  
  
|<span data-ttu-id="a868c-221">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-221">Sample Expression</span></span>|<span data-ttu-id="a868c-222">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-222">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-223">'man'</span><span class="sxs-lookup"><span data-stu-id="a868c-223">'man'</span></span>|<span data-ttu-id="a868c-224">Tekst, der svarer nøjagtigt til man, og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="a868c-224">Text that matches man exactly and is case sensitive.</span></span>|  
  
### <a name="-case-insensitive"></a><span data-ttu-id="a868c-225">(@) Ingen forskel på store og små bogstaver</span><span class="sxs-lookup"><span data-stu-id="a868c-225">(@) Case insensitive</span></span>  
  
|<span data-ttu-id="a868c-226">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-226">Sample Expression</span></span>|<span data-ttu-id="a868c-227">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-227">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-228">@man\*</span><span class="sxs-lookup"><span data-stu-id="a868c-228">@man\*</span></span>|<span data-ttu-id="a868c-229">Tekst, der starter med man, og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="a868c-229">Text that starts with man and is case insensitive.</span></span>|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="a868c-230">(\*) Mange ukendte tegn</span><span class="sxs-lookup"><span data-stu-id="a868c-230">(\*) An indefinite number of unknown characters</span></span>  
  
|<span data-ttu-id="a868c-231">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-231">Sample Expression</span></span>|<span data-ttu-id="a868c-232">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-232">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-233">*A/S*</span><span class="sxs-lookup"><span data-stu-id="a868c-233">*Co*</span></span>|<span data-ttu-id="a868c-234">Tekst, der indeholder "A/S", og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="a868c-234">Text that contains "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="a868c-235">\*A/S</span><span class="sxs-lookup"><span data-stu-id="a868c-235">\*Co</span></span>|<span data-ttu-id="a868c-236">Tekst, der ender på "A/S", og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="a868c-236">Text that ends with "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="a868c-237">A/S\*</span><span class="sxs-lookup"><span data-stu-id="a868c-237">Co\*</span></span>|<span data-ttu-id="a868c-238">Tekst, der begynder med "A/S", og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="a868c-238">Text that begins with "Co" and is case sensitive.</span></span>|  
  
### <a name="-one-unknown-character"></a><span data-ttu-id="a868c-239">(?) Ét ukendt tegn</span><span class="sxs-lookup"><span data-stu-id="a868c-239">(?) One unknown character</span></span>  
  
|<span data-ttu-id="a868c-240">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-240">Sample Expression</span></span>|<span data-ttu-id="a868c-241">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-241">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-242">Hans?n</span><span class="sxs-lookup"><span data-stu-id="a868c-242">Hans?n</span></span>|<span data-ttu-id="a868c-243">Tekst som f.eks. Hansen eller Hanson</span><span class="sxs-lookup"><span data-stu-id="a868c-243">Text such as Hansen or Hanson</span></span>|  
  
### <a name="combined-format-expressions"></a><span data-ttu-id="a868c-244">Kombinerede formatudtryk</span><span class="sxs-lookup"><span data-stu-id="a868c-244">Combined format expressions</span></span>  
  
|<span data-ttu-id="a868c-245">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a868c-245">Sample Expression</span></span>|<span data-ttu-id="a868c-246">Viste poster</span><span class="sxs-lookup"><span data-stu-id="a868c-246">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a868c-247">5999&#124;8100..8490</span><span class="sxs-lookup"><span data-stu-id="a868c-247">5999&#124;8100..8490</span></span>|<span data-ttu-id="a868c-248">Tallet 5999 og tallene fra og med 8100 til og med 8490.</span><span class="sxs-lookup"><span data-stu-id="a868c-248">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|<span data-ttu-id="a868c-249">..1299&#124;1400..</span><span class="sxs-lookup"><span data-stu-id="a868c-249">..1299&#124;1400..</span></span>|<span data-ttu-id="a868c-250">Medtag poster med et tal mindre end eller lig med 1299, eller tal lig med 1400 eller derover (alle tal undtagen 1300 til og med 1399).</span><span class="sxs-lookup"><span data-stu-id="a868c-250">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|<span data-ttu-id="a868c-251">>50&<100</span><span class="sxs-lookup"><span data-stu-id="a868c-251">>50&<100</span></span>|<span data-ttu-id="a868c-252">Medtag poster med tal større end 50 og mindre end 100 (tal fra 51 til og med 99).</span><span class="sxs-lookup"><span data-stu-id="a868c-252">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  
 
## <a name="see-also"></a><span data-ttu-id="a868c-253">Se også</span><span class="sxs-lookup"><span data-stu-id="a868c-253">See Also</span></span>
<span data-ttu-id="a868c-254">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a868c-254">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

