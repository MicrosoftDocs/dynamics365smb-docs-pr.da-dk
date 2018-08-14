---
title: "Sådan angiver du data i felter | Microsoft Docs"
description: "Der er mange generelle funktioner, der hjælper dig med at indtaste data på en hurtig og nem måde. De generelle funktioner til indtastning af data er beskrevet i dette emne."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 4354e28522d359cf9fa6178c4a1919831dcc52db
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---

# <a name="entering-data"></a><span data-ttu-id="f0591-104">Angivelse af data</span><span class="sxs-lookup"><span data-stu-id="f0591-104">Entering Data</span></span>
<span data-ttu-id="f0591-105">Der er mange generelle funktioner, der hjælper dig med at indtaste data på en hurtig og nem måde.</span><span class="sxs-lookup"><span data-stu-id="f0591-105">There are many general functions that help you enter data  in a quick and easy way.</span></span> <span data-ttu-id="f0591-106">De generelle funktioner til indtastning af data er beskrevet i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="f0591-106">The general functions for entering data are described in this article.</span></span>  

<span data-ttu-id="f0591-107">Eksemplerne i denne artikel bruger demodata.</span><span class="sxs-lookup"><span data-stu-id="f0591-107">The examples in this article use the demonstration data.</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="f0591-108">Obligatoriske felter</span><span class="sxs-lookup"><span data-stu-id="f0591-108">Mandatory Fields</span></span>
<span data-ttu-id="f0591-109">Når du indtaster data på sider, er visse felter markeret med en rød stjerne.</span><span class="sxs-lookup"><span data-stu-id="f0591-109">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="f0591-110">Den røde stjerne betyder, at feltet skal udfyldes for at fuldføre en bestemt proces, der bruger feltet, f.eks. bogføring af en transaktion, der bruger værdien i feltet.</span><span class="sxs-lookup"><span data-stu-id="f0591-110">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="f0591-111">Selv om feltet indeholder en rød stjerne, er du ikke tvunget til at udfylde feltet, før du fortsætter til andre felter eller lukker siden.</span><span class="sxs-lookup"><span data-stu-id="f0591-111">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="f0591-112">Den røde stjerne tjener kun som en påmindelse om, at du vil blive blokeret fra at udføre en bestemt proces.</span><span class="sxs-lookup"><span data-stu-id="f0591-112">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  


## <a name="finding-data-as-you-type"></a><span data-ttu-id="f0591-113">Søge efter data mens du skriver</span><span class="sxs-lookup"><span data-stu-id="f0591-113">Finding Data As You Type</span></span>  
 <span data-ttu-id="f0591-114">Når du begynder at indtaste tegn i et felt, vises en rulleliste med mulige feltværdier.</span><span class="sxs-lookup"><span data-stu-id="f0591-114">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="f0591-115">Listen ændres, når du skriver flere tegn, og du kan vælge den korrekte værdi, når den vises.</span><span class="sxs-lookup"><span data-stu-id="f0591-115">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="f0591-116">Mange felter har en knap med en nedadgående pil, som du kan vælge.</span><span class="sxs-lookup"><span data-stu-id="f0591-116">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="f0591-117">Når du vælger pilen, vises en liste med data, som du kan vælge at indtaste i feltet.</span><span class="sxs-lookup"><span data-stu-id="f0591-117">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="f0591-118">Knappen har to funktioner afhængigt af felttypen:</span><span class="sxs-lookup"><span data-stu-id="f0591-118">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="f0591-119">Valg – viser oplysninger fra en anden tabel, som du kan indtaste i feltet.</span><span class="sxs-lookup"><span data-stu-id="f0591-119">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="f0591-120">Du kan vælge én enkelt dataangivelse ad gangen.</span><span class="sxs-lookup"><span data-stu-id="f0591-120">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="f0591-121">Rullemenu – viser det sæt indstillinger, der findes til feltet.</span><span class="sxs-lookup"><span data-stu-id="f0591-121">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="f0591-122">Du kan kun vælge én af indstillingerne.</span><span class="sxs-lookup"><span data-stu-id="f0591-122">You can select only one of the options.</span></span>  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards in the **Items** window, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="f0591-123">Angive mængder ved beregning</span><span class="sxs-lookup"><span data-stu-id="f0591-123">Entering Quantities by Calculation</span></span>  
 <span data-ttu-id="f0591-124">Når du angiver tal i mængdefelter, f.eks. i feltet **Antal** på en varekladdelinje, kan du angive formlen i stedet for summen af mængden.</span><span class="sxs-lookup"><span data-stu-id="f0591-124">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

## <a name="examples"></a><span data-ttu-id="f0591-125">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f0591-125">Examples</span></span>  

-   <span data-ttu-id="f0591-126">Hvis du skriver 19+19, beregnes feltet til 38.</span><span class="sxs-lookup"><span data-stu-id="f0591-126">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="f0591-127">Hvis du skriver 41-9, beregnes feltet til 32.</span><span class="sxs-lookup"><span data-stu-id="f0591-127">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="f0591-128">Hvis du skriver 12\*4, beregnes feltet til 48.</span><span class="sxs-lookup"><span data-stu-id="f0591-128">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="f0591-129">Hvis du skriver 12/4, beregnes feltet til 3.</span><span class="sxs-lookup"><span data-stu-id="f0591-129">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="f0591-130">Angivelse af negative tal</span><span class="sxs-lookup"><span data-stu-id="f0591-130">Entering Negative Numbers</span></span>
<span data-ttu-id="f0591-131">Du kan angive negative tal på to måder.</span><span class="sxs-lookup"><span data-stu-id="f0591-131">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="f0591-132">Tallet -20,5 kan angives som:</span><span class="sxs-lookup"><span data-stu-id="f0591-132">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="f0591-133">-20,5</span><span class="sxs-lookup"><span data-stu-id="f0591-133">-20.5</span></span>  

    <span data-ttu-id="f0591-134">eller</span><span class="sxs-lookup"><span data-stu-id="f0591-134">or</span></span>
-   <span data-ttu-id="f0591-135">20,5-</span><span class="sxs-lookup"><span data-stu-id="f0591-135">20.5-</span></span>  

 <span data-ttu-id="f0591-136">I begge tilfælde registreres beløbet som -20,5.</span><span class="sxs-lookup"><span data-stu-id="f0591-136">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="f0591-137">Hvis det sidste tegn i udtrykket er et **+** eller et **-**, registreres hele udtrykket med det tegn.</span><span class="sxs-lookup"><span data-stu-id="f0591-137">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="f0591-138">Eksempel, **10-20+** medfører 10 og ikke -10.</span><span class="sxs-lookup"><span data-stu-id="f0591-138">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="f0591-139">Indtaste datoer og tidspunkter</span><span class="sxs-lookup"><span data-stu-id="f0591-139">Entering Dates and Times</span></span>
<span data-ttu-id="f0591-140">Du kan angive datoer og klokkeslæt i alle de felter, der er angivet specielt til datoer (datofelter).</span><span class="sxs-lookup"><span data-stu-id="f0591-140">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="f0591-141">Du kan angive datoer med eller uden separatorer.</span><span class="sxs-lookup"><span data-stu-id="f0591-141">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="f0591-142">Måden, du angiver datoer og klokkeslæt på, afhænger af dine indstillinger i **Område**.</span><span class="sxs-lookup"><span data-stu-id="f0591-142">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="f0591-143">Du kan finde flere oplysninger under [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f0591-143">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="f0591-144">Angive datoer</span><span class="sxs-lookup"><span data-stu-id="f0591-144">Entering Dates</span></span>  
 <span data-ttu-id="f0591-145">I et datofelt kan du indtaste to, fire, seks eller otte cifre:</span><span class="sxs-lookup"><span data-stu-id="f0591-145">In a date field you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="f0591-146">Hvis du kun indtaster to tal, fortolkes dette som dagen og måneden og året indsættes ud fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="f0591-146">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="f0591-147">Hvis du indtaster fire tal, fortolkes dette som dagen og måneden, og året indsættes ud fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="f0591-147">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="f0591-148">Hvis datoen falder inden for 01-01-1930 og 31-12-2029, kan du nøjes med to tal for året, ellers skal året angives med fire cifre.</span><span class="sxs-lookup"><span data-stu-id="f0591-148">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

 <span data-ttu-id="f0591-149">Du kan også indtaste datoen som en ugedag efterfulgt af ugenummeret og evt. året (f.eks. betyder Man25 eller man25 mandag i uge 25).</span><span class="sxs-lookup"><span data-stu-id="f0591-149">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

 <span data-ttu-id="f0591-150">I stedet for en bestemt dato kan du indtaste én af to koder.</span><span class="sxs-lookup"><span data-stu-id="f0591-150">Instead of entering a specific date, you can enter one of two codes.</span></span>  

|<span data-ttu-id="f0591-151">Kode</span><span class="sxs-lookup"><span data-stu-id="f0591-151">Code</span></span>|<span data-ttu-id="f0591-152">Resultat</span><span class="sxs-lookup"><span data-stu-id="f0591-152">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="f0591-153">d</span><span class="sxs-lookup"><span data-stu-id="f0591-153">t</span></span>|<span data-ttu-id="f0591-154">Dette er dags dato (computerens systemdato).</span><span class="sxs-lookup"><span data-stu-id="f0591-154">This is today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="f0591-155">a</span><span class="sxs-lookup"><span data-stu-id="f0591-155">w</span></span>|<span data-ttu-id="f0591-156">Dette er den arbejdsdato, der er angivet i programmet.</span><span class="sxs-lookup"><span data-stu-id="f0591-156">This is the work date that is setup in the application.</span></span> <span data-ttu-id="f0591-157">Hvis du vil ændre arbejdsdatoen, kan du se i [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f0591-157">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="f0591-158">Det er en fordel at anvende en arbejdsdato, hvis du har mange transaktioner at udføre på en dato, der ikke er dags dato.</span><span class="sxs-lookup"><span data-stu-id="f0591-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a><span data-ttu-id="f0591-159">Angive klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="f0591-159">Entering Times</span></span>  
 <span data-ttu-id="f0591-160">Når du angiver klokkeslæt, kan du indsætte en vilkårlig separator mellem tidsenhederne, men det er ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="f0591-160">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="f0591-161">Det er ikke nødvendigt at skrive minutter, sekunder eller AM/PM.</span><span class="sxs-lookup"><span data-stu-id="f0591-161">You do not have to write minutes, seconds, or AM/PM.</span></span>  

 <span data-ttu-id="f0591-162">I den følgende tabel kan du se, hvordan du kan indtaste klokkeslæt, og hvordan de fortolkes.</span><span class="sxs-lookup"><span data-stu-id="f0591-162">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="f0591-163">Post</span><span class="sxs-lookup"><span data-stu-id="f0591-163">Entry</span></span>|<span data-ttu-id="f0591-164">Fortolkning</span><span class="sxs-lookup"><span data-stu-id="f0591-164">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="f0591-165">5</span><span class="sxs-lookup"><span data-stu-id="f0591-165">5</span></span>|<span data-ttu-id="f0591-166">05:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-166">05:00:00</span></span>|  
|<span data-ttu-id="f0591-167">5:30</span><span class="sxs-lookup"><span data-stu-id="f0591-167">5:30</span></span>|<span data-ttu-id="f0591-168">05:30:00</span><span class="sxs-lookup"><span data-stu-id="f0591-168">05:30:00</span></span>|  
|<span data-ttu-id="f0591-169">0530</span><span class="sxs-lookup"><span data-stu-id="f0591-169">0530</span></span>|<span data-ttu-id="f0591-170">05:30:00</span><span class="sxs-lookup"><span data-stu-id="f0591-170">05:30:00</span></span>|  
|<span data-ttu-id="f0591-171">5:30:5</span><span class="sxs-lookup"><span data-stu-id="f0591-171">5:30:5</span></span>|<span data-ttu-id="f0591-172">05:30:05</span><span class="sxs-lookup"><span data-stu-id="f0591-172">05:30:05</span></span>|  
|<span data-ttu-id="f0591-173">053005</span><span class="sxs-lookup"><span data-stu-id="f0591-173">053005</span></span>|<span data-ttu-id="f0591-174">05:30:05</span><span class="sxs-lookup"><span data-stu-id="f0591-174">05:30:05</span></span>|  
|<span data-ttu-id="f0591-175">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="f0591-175">5:30:5,50</span></span>|<span data-ttu-id="f0591-176">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="f0591-176">05:30:05.5</span></span>|  
|<span data-ttu-id="f0591-177">053005050</span><span class="sxs-lookup"><span data-stu-id="f0591-177">053005050</span></span>|<span data-ttu-id="f0591-178">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="f0591-178">05:30:05.05</span></span>|  

 <span data-ttu-id="f0591-179">Du skal skrive to tal for hver tidsenhed, hvis du ikke angiver en separator.</span><span class="sxs-lookup"><span data-stu-id="f0591-179">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="f0591-180">Angive dato/klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="f0591-180">Entering Datetimes</span></span>  
 <span data-ttu-id="f0591-181">Når du angiver dato/klokkeslæt skal du angive et mellemrum mellem datoen og klokkeslættet.</span><span class="sxs-lookup"><span data-stu-id="f0591-181">When you enter datetimes you must enter a space between the date and the time.</span></span>  

 <span data-ttu-id="f0591-182">I den følgende tabel kan du se, hvordan du kan skrive dato og klokkeslæt, og hvordan de fortolkes.</span><span class="sxs-lookup"><span data-stu-id="f0591-182">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="f0591-183">Post</span><span class="sxs-lookup"><span data-stu-id="f0591-183">Entry</span></span>|<span data-ttu-id="f0591-184">Fortolkning</span><span class="sxs-lookup"><span data-stu-id="f0591-184">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="f0591-185">131202 132455</span><span class="sxs-lookup"><span data-stu-id="f0591-185">131202 132455</span></span>|<span data-ttu-id="f0591-186">13-12-02 13:24:55</span><span class="sxs-lookup"><span data-stu-id="f0591-186">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="f0591-187">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="f0591-187">1-12-02 10</span></span>|<span data-ttu-id="f0591-188">01-12-02 10:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-188">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="f0591-189">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="f0591-189">1.12.02 5</span></span>|<span data-ttu-id="f0591-190">01-12-02 05:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-190">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="f0591-191">1.12.02</span><span class="sxs-lookup"><span data-stu-id="f0591-191">1.12.02</span></span>|<span data-ttu-id="f0591-192">01-12-02 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-192">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="f0591-193">11 12</span><span class="sxs-lookup"><span data-stu-id="f0591-193">11 12</span></span>|<span data-ttu-id="f0591-194">11-løbende måned-løbende år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-194">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="f0591-195">1112 12</span><span class="sxs-lookup"><span data-stu-id="f0591-195">1112 12</span></span>|<span data-ttu-id="f0591-196">11-12-aktuelt år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-196">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="f0591-197">d eller dags dato</span><span class="sxs-lookup"><span data-stu-id="f0591-197">t or today</span></span>|<span data-ttu-id="f0591-198">dags dato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-198">today's date 00:00:00</span></span>|  
|<span data-ttu-id="f0591-199">d klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="f0591-199">t time</span></span>|<span data-ttu-id="f0591-200">dags dato aktuelt klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="f0591-200">today's date actual time</span></span>|  
|<span data-ttu-id="f0591-201">d 10:30</span><span class="sxs-lookup"><span data-stu-id="f0591-201">t 10:30</span></span>|<span data-ttu-id="f0591-202">dags dato 10:30:00</span><span class="sxs-lookup"><span data-stu-id="f0591-202">today's date 10:30:00</span></span>|  
|<span data-ttu-id="f0591-203">d 3:3:3</span><span class="sxs-lookup"><span data-stu-id="f0591-203">t 3:3:3</span></span>|<span data-ttu-id="f0591-204">dags dato 03:03:03</span><span class="sxs-lookup"><span data-stu-id="f0591-204">today's date 03:03:03</span></span>|  
|<span data-ttu-id="f0591-205">a eller arbejdsdato</span><span class="sxs-lookup"><span data-stu-id="f0591-205">w or workdate</span></span>|<span data-ttu-id="f0591-206">arbejdsdato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-206">the working date 00:00:00</span></span>|  
|<span data-ttu-id="f0591-207">m eller mandag</span><span class="sxs-lookup"><span data-stu-id="f0591-207">m or Monday</span></span>|<span data-ttu-id="f0591-208">Mandag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-208">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f0591-209">ti eller tirsdag</span><span class="sxs-lookup"><span data-stu-id="f0591-209">tu or Tuesday</span></span>|<span data-ttu-id="f0591-210">Tirsdag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-210">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f0591-211">on eller onsdag</span><span class="sxs-lookup"><span data-stu-id="f0591-211">we or Wednesday</span></span>|<span data-ttu-id="f0591-212">Onsdag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-212">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f0591-213">to eller torsdag</span><span class="sxs-lookup"><span data-stu-id="f0591-213">th or Thursday</span></span>|<span data-ttu-id="f0591-214">Torsdag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-214">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f0591-215">f eller fredag</span><span class="sxs-lookup"><span data-stu-id="f0591-215">f or Friday</span></span>|<span data-ttu-id="f0591-216">Fredag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-216">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f0591-217">l eller lørdag</span><span class="sxs-lookup"><span data-stu-id="f0591-217">s or Saturday</span></span>|<span data-ttu-id="f0591-218">Lørdag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-218">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f0591-219">s eller søndag</span><span class="sxs-lookup"><span data-stu-id="f0591-219">su or Sunday</span></span>|<span data-ttu-id="f0591-220">Søndag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f0591-220">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f0591-221">ti 10:30</span><span class="sxs-lookup"><span data-stu-id="f0591-221">tu 10:30</span></span>|<span data-ttu-id="f0591-222">Tirsdag i den aktuelle uge 10:30:00</span><span class="sxs-lookup"><span data-stu-id="f0591-222">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="f0591-223">ti 3:3:3</span><span class="sxs-lookup"><span data-stu-id="f0591-223">tu 3:3:3</span></span>|<span data-ttu-id="f0591-224">Tirsdag i den aktuelle uge 03:03:03</span><span class="sxs-lookup"><span data-stu-id="f0591-224">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="f0591-225">Angivelse af varighed</span><span class="sxs-lookup"><span data-stu-id="f0591-225">Entering Duration</span></span>  
 <span data-ttu-id="f0591-226">Du angiver varighed ved at skrive et tal efterfulgt af en måleenhed.</span><span class="sxs-lookup"><span data-stu-id="f0591-226">You enter a duration as a number followed by its unit of measure.</span></span>  

 <span data-ttu-id="f0591-227">Her er nogle eksempler.</span><span class="sxs-lookup"><span data-stu-id="f0591-227">Here are some examples.</span></span>  

|<span data-ttu-id="f0591-228">Varighed</span><span class="sxs-lookup"><span data-stu-id="f0591-228">Duration</span></span>|<span data-ttu-id="f0591-229">Enhed**</span><span class="sxs-lookup"><span data-stu-id="f0591-229">Unit of measure**</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="f0591-230">2t</span><span class="sxs-lookup"><span data-stu-id="f0591-230">2h</span></span>|<span data-ttu-id="f0591-231">2 timer</span><span class="sxs-lookup"><span data-stu-id="f0591-231">2 hrs</span></span>|  
|<span data-ttu-id="f0591-232">6t 30 m</span><span class="sxs-lookup"><span data-stu-id="f0591-232">6h 30 m</span></span>|<span data-ttu-id="f0591-233">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="f0591-233">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="f0591-234">6,5t</span><span class="sxs-lookup"><span data-stu-id="f0591-234">6.5h</span></span>|<span data-ttu-id="f0591-235">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="f0591-235">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="f0591-236">90m</span><span class="sxs-lookup"><span data-stu-id="f0591-236">90m</span></span>|<span data-ttu-id="f0591-237">1 time 30 min</span><span class="sxs-lookup"><span data-stu-id="f0591-237">1 hr 30 mins</span></span>|  
|<span data-ttu-id="f0591-238">2d 6t 30m</span><span class="sxs-lookup"><span data-stu-id="f0591-238">2d 6h 30m</span></span>|<span data-ttu-id="f0591-239">2 dage 6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="f0591-239">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="f0591-240">2d 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="f0591-240">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="f0591-241">2 dage 6 timer 30 min 56 sek 600 msek</span><span class="sxs-lookup"><span data-stu-id="f0591-241">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="f0591-242">Du kan også skrive et tal, der så automatisk konverteres til en varighed.</span><span class="sxs-lookup"><span data-stu-id="f0591-242">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="f0591-243">Det tal, du skriver, konverteres i overensstemmelse med den standardmåleenhed, der er angivet i feltet Varighed.</span><span class="sxs-lookup"><span data-stu-id="f0591-243">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="f0591-244">Du kan se, hvilken måleenhed, der anvendes i feltet Varighed, ved at skrive et tal og se, hvilken måleenhed tallet konverteres til.</span><span class="sxs-lookup"><span data-stu-id="f0591-244">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="f0591-245">Tallet 5 konverteres til 5 timer, hvis måleenheden er timer.</span><span class="sxs-lookup"><span data-stu-id="f0591-245">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a><span data-ttu-id="f0591-246">Bruge datoformler</span><span class="sxs-lookup"><span data-stu-id="f0591-246">Using Date Formulas</span></span>  
 <span data-ttu-id="f0591-247">En datoformel er en kort, forkortet kombination af bogstaver og tal, der angiver, hvordan datoer skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="f0591-247">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="f0591-248">Du kan indtaste datoformler i forskellige datoberegningsfelter og i gentagelsesintervalfelter i gentagelseskladder.</span><span class="sxs-lookup"><span data-stu-id="f0591-248">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f0591-249">I alle formlens datafelter indgår en dag automatisk til at dække i dag som den dag, hvor perioden starter.</span><span class="sxs-lookup"><span data-stu-id="f0591-249">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="f0591-250">Tilsvarende, hvis du f.eks. indtaster 1U, så er perioden faktisk otte dage, fordi i dag er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="f0591-250">Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="f0591-251">Du skal indtaste 6D eller 1U-1D for at angive en periode på syv dage (en rigtig uge), der medtager periodens startdato.</span><span class="sxs-lookup"><span data-stu-id="f0591-251">To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.</span></span>  

 <span data-ttu-id="f0591-252">Her følger et par eksempler på brugen af datoformler:</span><span class="sxs-lookup"><span data-stu-id="f0591-252">Here are some examples of how date formulas can be used:</span></span>  

-   <span data-ttu-id="f0591-253">Datoformlen i gentagelsesintervalfeltet i en gentagelseskladde afgør, hvor tit posten på kladdelinjen skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="f0591-253">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>  

-   <span data-ttu-id="f0591-254">Datoformlen i feltet Respitperiode for et bestemt rykkerniveau afgør det tidsrum, der skal gå fra forfaldsdatoen (eller fra datoen for den forrige rykker), før der oprettes en rykker.</span><span class="sxs-lookup"><span data-stu-id="f0591-254">The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.</span></span>  

-   <span data-ttu-id="f0591-255">Datoformlen i feltet Forfaldsdatoformel afgør, hvordan forfaldsdatoen på rykkeren beregnes.</span><span class="sxs-lookup"><span data-stu-id="f0591-255">The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.</span></span>  

 <span data-ttu-id="f0591-256">Datoformlen kan indeholde op til 20 tegn (både tal og bogstaver).</span><span class="sxs-lookup"><span data-stu-id="f0591-256">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="f0591-257">Du kan bruge følgende bogstaver som forkortelser for tidsangivelser.</span><span class="sxs-lookup"><span data-stu-id="f0591-257">You can use the following letters, which are abbreviations for time specifications.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="f0591-258">L</span><span class="sxs-lookup"><span data-stu-id="f0591-258">C</span></span>|<span data-ttu-id="f0591-259">Løbende</span><span class="sxs-lookup"><span data-stu-id="f0591-259">Current</span></span>|  
|<span data-ttu-id="f0591-260">D</span><span class="sxs-lookup"><span data-stu-id="f0591-260">D</span></span>|<span data-ttu-id="f0591-261">Dag(e)</span><span class="sxs-lookup"><span data-stu-id="f0591-261">Day(s)</span></span>|  
|<span data-ttu-id="f0591-262">U</span><span class="sxs-lookup"><span data-stu-id="f0591-262">W</span></span>|<span data-ttu-id="f0591-263">Uge(r)</span><span class="sxs-lookup"><span data-stu-id="f0591-263">Week(s)</span></span>|  
|<span data-ttu-id="f0591-264">M</span><span class="sxs-lookup"><span data-stu-id="f0591-264">M</span></span>|<span data-ttu-id="f0591-265">Måned(er)</span><span class="sxs-lookup"><span data-stu-id="f0591-265">Month(s)</span></span>|  
|<span data-ttu-id="f0591-266">K</span><span class="sxs-lookup"><span data-stu-id="f0591-266">Q</span></span>|<span data-ttu-id="f0591-267">Kvartal(er)</span><span class="sxs-lookup"><span data-stu-id="f0591-267">Quarter(s)</span></span>|  
|<span data-ttu-id="f0591-268">Å</span><span class="sxs-lookup"><span data-stu-id="f0591-268">Y</span></span>|<span data-ttu-id="f0591-269">År</span><span class="sxs-lookup"><span data-stu-id="f0591-269">Year(s)</span></span>|  

 <span data-ttu-id="f0591-270">Datoformlen kan opbygges på tre måder.</span><span class="sxs-lookup"><span data-stu-id="f0591-270">You can construct a date formula in three ways.</span></span>  

 <span data-ttu-id="f0591-271">Følgende eksempel viser aktuelle plus en tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="f0591-271">The following example shows how current plus a time unit.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="f0591-272">LU</span><span class="sxs-lookup"><span data-stu-id="f0591-272">CW</span></span>|<span data-ttu-id="f0591-273">Løbende uge</span><span class="sxs-lookup"><span data-stu-id="f0591-273">Current week</span></span>|  
|<span data-ttu-id="f0591-274">LM</span><span class="sxs-lookup"><span data-stu-id="f0591-274">CM</span></span>|<span data-ttu-id="f0591-275">Løbende måned</span><span class="sxs-lookup"><span data-stu-id="f0591-275">Current month</span></span>|  

 <span data-ttu-id="f0591-276">Følgende eksempel viser et tal og en tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="f0591-276">The following example shows how a number and a time unit.</span></span> <span data-ttu-id="f0591-277">Tallet må ikke være større end 9999.</span><span class="sxs-lookup"><span data-stu-id="f0591-277">A number cannot be larger than 9999.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="f0591-278">10D</span><span class="sxs-lookup"><span data-stu-id="f0591-278">10D</span></span>|<span data-ttu-id="f0591-279">10 dage fra i dag</span><span class="sxs-lookup"><span data-stu-id="f0591-279">10 days from today</span></span>|  
|<span data-ttu-id="f0591-280">2U</span><span class="sxs-lookup"><span data-stu-id="f0591-280">2W</span></span>|<span data-ttu-id="f0591-281">2 uger fra i dag</span><span class="sxs-lookup"><span data-stu-id="f0591-281">2 weeks from today</span></span>|  

 <span data-ttu-id="f0591-282">Følgende eksempel viser en tidsenhed og et tal.</span><span class="sxs-lookup"><span data-stu-id="f0591-282">The following example shows how a time unit and a number.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="f0591-283">D10</span><span class="sxs-lookup"><span data-stu-id="f0591-283">D10</span></span>|<span data-ttu-id="f0591-284">Den næste 10. dage i en måned</span><span class="sxs-lookup"><span data-stu-id="f0591-284">The next 10th day of a month</span></span>|  
|<span data-ttu-id="f0591-285">UD4</span><span class="sxs-lookup"><span data-stu-id="f0591-285">WD4</span></span>|<span data-ttu-id="f0591-286">Den næste 4. dag i en uge (torsdag)</span><span class="sxs-lookup"><span data-stu-id="f0591-286">The next 4th day of a week (Thursday)</span></span>|  

 <span data-ttu-id="f0591-287">Følgende eksempel viser, hvordan du kan kombinere de tre formler efter behov.</span><span class="sxs-lookup"><span data-stu-id="f0591-287">The following example shows how you can combine these three forms as needed.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="f0591-288">LM+10D</span><span class="sxs-lookup"><span data-stu-id="f0591-288">CM+10D</span></span>|<span data-ttu-id="f0591-289">Løbende måned plus 10 dage</span><span class="sxs-lookup"><span data-stu-id="f0591-289">Current month + 10 days</span></span>|  

 <span data-ttu-id="f0591-290">Følgende eksempel viser, hvordan du kan bruge et minustegn til at angive en dato i fortiden.</span><span class="sxs-lookup"><span data-stu-id="f0591-290">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="f0591-291">-1Å</span><span class="sxs-lookup"><span data-stu-id="f0591-291">-1Y</span></span>|<span data-ttu-id="f0591-292">1 år siden fra i dag</span><span class="sxs-lookup"><span data-stu-id="f0591-292">1 year ago from today</span></span>|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a><span data-ttu-id="f0591-293">Se også</span><span class="sxs-lookup"><span data-stu-id="f0591-293">See Also</span></span>  
 [<span data-ttu-id="f0591-294">Søgning i, filtrering og sortering af data</span><span class="sxs-lookup"><span data-stu-id="f0591-294">Searching, Filtering, and Sorting Data</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="f0591-295">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f0591-295">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

