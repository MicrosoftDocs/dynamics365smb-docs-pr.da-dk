---
title: "Angive datoer og klokkeslæt i Business Central | Microsoft Docs"
description: "Få at vide, hvordan du angiver datoer og tidspunkter med forskellige produktivitetstip som oversigter, udtryk og områder. Filtrer lister eller rapporter ned til en bestemt dato eller tidsperioder."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8717d60a8449ca300eaf9c1a5c4b137ea1a1a247
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---

# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="5ec44-104">Arbejde med kalenderdatoer og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="5ec44-104">Working with Calendar Dates and Times</span></span>
<span data-ttu-id="5ec44-105">I [!INCLUDE[d365fin](includes/d365fin_long_md.md)] er der flere måder til at angive datoer og klokkeslæt, herunder effektive funktioner, der fremskynder indtastning af data og hjælper dig med at skrive komplekse kalenderudtryk.</span><span class="sxs-lookup"><span data-stu-id="5ec44-105">[!INCLUDE[d365fin](includes/d365fin_long_md.md)] offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="5ec44-106">Der er forskellige steder i programmet, hvor du kan angive datoer og klokkeslæt i felterne.</span><span class="sxs-lookup"><span data-stu-id="5ec44-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="5ec44-107">På en salgsordre kan du f.eks. angive afsendelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="5ec44-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="5ec44-108">Når du filtrerer lister eller rapportdata, kan du angive datoer og klokkeslæt for kun at finde de data, du er interesseret i.</span><span class="sxs-lookup"><span data-stu-id="5ec44-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="5ec44-109">Kontrollere internationale og sproglige indstillinger</span><span class="sxs-lookup"><span data-stu-id="5ec44-109">Check your region and language settings</span></span>
<span data-ttu-id="5ec44-110">Siden [**Mine indstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med dine brugerindstillinger i Business Central") angiver det **Land/område** og **Sprog**, du bruger i systemet.</span><span class="sxs-lookup"><span data-stu-id="5ec44-110">The [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="5ec44-111">Disse indstillinger påvirker måden, du angiver datoer og klokkeslæt på.</span><span class="sxs-lookup"><span data-stu-id="5ec44-111">These settings influence how you enter dates and times.</span></span> 

-   <span data-ttu-id="5ec44-112">Indstillingen **Område** bestemmer, hvordan datoer, klokkeslæt, tal og valutaer vises og formateres.</span><span class="sxs-lookup"><span data-stu-id="5ec44-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="5ec44-113">Når datomønstre omfatter ord, skal sproget for de ord, du bruger, svare til indstillingen **Sprog**.</span><span class="sxs-lookup"><span data-stu-id="5ec44-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="5ec44-114">anvender den gregorianske kalender.</span><span class="sxs-lookup"><span data-stu-id="5ec44-114">uses the Gregorian calendar system.</span></span>

<!-- 
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->
## <a name="entering-dates"></a><span data-ttu-id="5ec44-115">Angive datoer</span><span class="sxs-lookup"><span data-stu-id="5ec44-115">Entering Dates</span></span>
<span data-ttu-id="5ec44-116">I et datofelt kan du angive en dato i standardformatet for din land/områdeindstilling.</span><span class="sxs-lookup"><span data-stu-id="5ec44-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="5ec44-117">Forskellige områder kan bruge forskellige separatorer mellem dage, måneder og år.</span><span class="sxs-lookup"><span data-stu-id="5ec44-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="5ec44-118">For eksempel bruger nogle lande/områder bindestreger (mm-dd-åååå), mens andre bruger skråstreger (mm/dd/åååå).</span><span class="sxs-lookup"><span data-stu-id="5ec44-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="5ec44-119">Du kan dog bruge alle separatorer, selv mellemrum, og datoen ændres automatisk til brug af de separatorer, der gælder for dit land/område.</span><span class="sxs-lookup"><span data-stu-id="5ec44-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="5ec44-120">Bemærk, at det format, som datoer vises i på udskrevne rapporter eller dokumenter sendt med e-mails, ikke påvirkes af dit personlige valg af land/område.</span><span class="sxs-lookup"><span data-stu-id="5ec44-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="5ec44-121">For at arbejde mere produktivt med datoer og klokkeslæt kan du bruge de metoder og formater, der er beskrevet i følgende afsnit.</span><span class="sxs-lookup"><span data-stu-id="5ec44-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span> 

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="5ec44-122">Vælge datoer i kalenderen</span><span class="sxs-lookup"><span data-stu-id="5ec44-122">Picking dates from the calendar</span></span>
<span data-ttu-id="5ec44-123">De felter, der viser et kalenderikon, kan angives ved hjælp af kalenderdatovælgeren.</span><span class="sxs-lookup"><span data-stu-id="5ec44-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="5ec44-124">Aktiver kalenderikonet for at få vist kalenderdatovælgeren, eller tryk på Ctrl + Home-tastaturgenvejen i feltet.</span><span class="sxs-lookup"><span data-stu-id="5ec44-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="5ec44-125">![Datofelter](media/ui-date-field.png "Eksempel på et datofelt")</span><span class="sxs-lookup"><span data-stu-id="5ec44-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="5ec44-126">Se også [Tastaturgenveje i kalenderdatovælgeren](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="5ec44-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts)</span></span>

### <a name="today"></a><span data-ttu-id="5ec44-127">I dag</span><span class="sxs-lookup"><span data-stu-id="5ec44-127">Today</span></span>
<span data-ttu-id="5ec44-128">Angiv ordet for `today` på det valgte sprog i indstillingen **Sprog**. Dette indstiller datoen til dags dato.</span><span class="sxs-lookup"><span data-stu-id="5ec44-128">Enter the word for `today`, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="5ec44-129">I stedet for at angive hele ordet kan du angive en del af det fra begyndelsen, f.eks. `t` eller `tod`, så længe det ikke også er begyndelsen på et andet ord.</span><span class="sxs-lookup"><span data-stu-id="5ec44-129">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as `t` or `tod`, as long as it is not also the start of another word.</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="5ec44-130">Mønsteret dag\-uge\-år</span><span class="sxs-lookup"><span data-stu-id="5ec44-130">Day\-week\-year pattern</span></span>
<span data-ttu-id="5ec44-131">Du kan angive en dato som en ugedag efterfulgt af et ugenummer og eventuelt et år.</span><span class="sxs-lookup"><span data-stu-id="5ec44-131">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="5ec44-132">F.eks. betyder `Mon25` eller `mon25` Monday i uge 25.</span><span class="sxs-lookup"><span data-stu-id="5ec44-132">For example, `Mon25` or `mon25` means Monday in week 25.</span></span> <span data-ttu-id="5ec44-133">Hvis du ikke angiver et år, bruges året fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5ec44-133">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="5ec44-134">I stedet for at skrive hele ordet for den pågældende dag i ugen kan du skrive en del af ordet fra begyndelsen.</span><span class="sxs-lookup"><span data-stu-id="5ec44-134">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="5ec44-135">Hvis der opstår konflikter (f.eks. med `s`, som kan være Saturday eller Sunday), vurderes dagene i overensstemmelse med lande/områdeindstillingen.</span><span class="sxs-lookup"><span data-stu-id="5ec44-135">In case of conflicts (such as with `s` which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="5ec44-136">Input vurderes først mod `workdate` og `today`, så husk dette, når du laver forkortelser.</span><span class="sxs-lookup"><span data-stu-id="5ec44-136">The input is first evaluated against `workdate` and `today` as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="5ec44-137">F.eks. betyder `t` allerede today så det ikke kan betyde Tuesday eller Thursday.</span><span class="sxs-lookup"><span data-stu-id="5ec44-137">For example, `t` already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="5ec44-138">Ugenummereringen er altid ISO 8601, hvor er uge 1 uge er den uge, som 4. januar indgår i, eller ugen med den første torsdag i året.</span><span class="sxs-lookup"><span data-stu-id="5ec44-138">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="5ec44-139">Talmønstre</span><span class="sxs-lookup"><span data-stu-id="5ec44-139">Digit patterns</span></span>
<span data-ttu-id="5ec44-140">I et datofelt kan du indtaste to, fire, seks eller otte cifre:</span><span class="sxs-lookup"><span data-stu-id="5ec44-140">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="5ec44-141">Hvis du kun indtaster to tal, fortolkes dette som dagen og måneden og året indsættes ud fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5ec44-141">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="5ec44-142">Hvis du indtaster fire tal, fortolkes dette som dagen og måneden, og året indsættes ud fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5ec44-142">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="5ec44-143">Rækkefølgen af dagen og måneden bestemmes af dine områdeindstillinger.</span><span class="sxs-lookup"><span data-stu-id="5ec44-143">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="5ec44-144">Selvom områdeindstillingerne har året før dagen og måneden, fortolkes fire tal som dagen og måneden.</span><span class="sxs-lookup"><span data-stu-id="5ec44-144">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="5ec44-145">Hvis datoen falder inden for 01-01-1930 og 31-12-2029, kan du nøjes med to tal for året, ellers skal året angives med fire cifre.</span><span class="sxs-lookup"><span data-stu-id="5ec44-145">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="current-work-date"></a><span data-ttu-id="5ec44-146">Aktuel arbejdsdato</span><span class="sxs-lookup"><span data-stu-id="5ec44-146">Current work date</span></span>
<span data-ttu-id="5ec44-147">Med arbejdsdatofunktionen kan du registrere transaktioner ved hjælp af en anden dato end dags dato.</span><span class="sxs-lookup"><span data-stu-id="5ec44-147">The work date feature allows you to record transations using a date that is different from the current date.</span></span>

<span data-ttu-id="5ec44-148">Ordet for 'workdate' (arbejdsdato) på det sprog, der er angivet i indstillingen **Sprog**, indstiller datoen til den aktuelt angivne arbejdsdato, der er angivet på siden [**Mine indstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med dine brugerindstillinger i Business Central").</span><span class="sxs-lookup"><span data-stu-id="5ec44-148">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page.</span></span> <span data-ttu-id="5ec44-149">I stedet for at skrive hele ordet kan du skrive en del af ordet fra begyndelsen, f.eks. 'a' eller 'arbejds'.</span><span class="sxs-lookup"><span data-stu-id="5ec44-149">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="5ec44-150">Hvis du ikke har angivet en arbejdsdato, bliver dags dato brugt som arbejdsdato.</span><span class="sxs-lookup"><span data-stu-id="5ec44-150">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="5ec44-151">Det er en fordel at anvende en arbejdsdato, hvis du har mange transaktioner at udføre på en dato, der ikke er dags dato.</span><span class="sxs-lookup"><span data-stu-id="5ec44-151">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="5ec44-152">Se også [Ændring af grundlæggende indstillinger, f.eks. arbejdsdatoen](ui-change-basic-settings.md#work-date)</span><span class="sxs-lookup"><span data-stu-id="5ec44-152">See also [Changing Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date)</span></span>

### <a name="closing-date"></a><span data-ttu-id="5ec44-153">Ultimodato</span><span class="sxs-lookup"><span data-stu-id="5ec44-153">Closing Date</span></span>
<span data-ttu-id="5ec44-154">Ved afslutning af et regnskabsår kan du bruge ultimodatoer til at angive, at posten er en ultimopost.</span><span class="sxs-lookup"><span data-stu-id="5ec44-154">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="5ec44-155">I teknisk forstand er en ultimodato en hvilken som helst dato mellem to datoer, f.eks. 31. december og 1. januar.</span><span class="sxs-lookup"><span data-stu-id="5ec44-155">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="5ec44-156">Hvis en dato skal være en ultimodato, skal du indsætte et `C` lige foran datoen, f.eks. `C123101`.</span><span class="sxs-lookup"><span data-stu-id="5ec44-156">To specify that a date is a closing date, put `C` just before the date, such as `C123101`.</span></span> <span data-ttu-id="5ec44-157">Dette kan bruges sammen med alle datomønstre.</span><span class="sxs-lookup"><span data-stu-id="5ec44-157">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="5ec44-158">Eksempler</span><span class="sxs-lookup"><span data-stu-id="5ec44-158">Examples</span></span>
<span data-ttu-id="5ec44-159">Følgende tabel indeholder eksempler på datoer i alle formater.</span><span class="sxs-lookup"><span data-stu-id="5ec44-159">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="5ec44-160">Det forudsætter lande/områdeindstillinger, der formaterer datoer i henhold til: **år.måned.dag.**, en uge, der begynder om mandagen, og hvor sproget er engelsk.</span><span class="sxs-lookup"><span data-stu-id="5ec44-160">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="5ec44-161">**Post**</span><span class="sxs-lookup"><span data-stu-id="5ec44-161">**Entry**</span></span>      |<span data-ttu-id="5ec44-162">**Fortolkning**</span><span class="sxs-lookup"><span data-stu-id="5ec44-162">**Interpretation**</span></span>      |
|---------------|------------------------|
|`2018.12.31.`|<span data-ttu-id="5ec44-163">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="5ec44-163">2018.12.31.</span></span>|
|`181231`|<span data-ttu-id="5ec44-164">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="5ec44-164">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="5ec44-165">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="5ec44-165">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="5ec44-166">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="5ec44-166">2018.12.31.</span></span>|
|`20181231`|<span data-ttu-id="5ec44-167">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="5ec44-167">2018.12.31.</span></span>|
|`18/12,31`|<span data-ttu-id="5ec44-168">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="5ec44-168">2018.12.31.</span></span>|
|`11`|<span data-ttu-id="5ec44-169">arbejdsdatoår.abejdsdatomåned.11.</span><span class="sxs-lookup"><span data-stu-id="5ec44-169">work date year.work date month.11.</span></span>|
|`1112`|<span data-ttu-id="5ec44-170">arbejdsdatoår.11.12.</span><span class="sxs-lookup"><span data-stu-id="5ec44-170">work date year.11.12.</span></span>|
|<span data-ttu-id="5ec44-171">`t` eller `today`</span><span class="sxs-lookup"><span data-stu-id="5ec44-171">`t` or `today`</span></span>|<span data-ttu-id="5ec44-172">dags dato</span><span class="sxs-lookup"><span data-stu-id="5ec44-172">today's date</span></span>|
|<span data-ttu-id="5ec44-173">`w` eller `workdate`</span><span class="sxs-lookup"><span data-stu-id="5ec44-173">`w` or `workdate`</span></span>|<span data-ttu-id="5ec44-174">arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="5ec44-174">the working date</span></span>|
|<span data-ttu-id="5ec44-175">`m` eller `Monday`</span><span class="sxs-lookup"><span data-stu-id="5ec44-175">`m` or `Monday`</span></span>|<span data-ttu-id="5ec44-176">Mandag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="5ec44-176">Monday of the work date week</span></span>|
|<span data-ttu-id="5ec44-177">`tu` eller `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="5ec44-177">`tu` or `Tuesday`</span></span>|<span data-ttu-id="5ec44-178">Tirsdag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="5ec44-178">Tuesday of the work date week</span></span>|
|<span data-ttu-id="5ec44-179">`sa` eller `Saturday`</span><span class="sxs-lookup"><span data-stu-id="5ec44-179">`sa` or `Saturday`</span></span>|<span data-ttu-id="5ec44-180">Lørdag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="5ec44-180">Saturday of the work date week</span></span>|
|<span data-ttu-id="5ec44-181">`s` eller `Sunday`</span><span class="sxs-lookup"><span data-stu-id="5ec44-181">`s` or `Sunday`</span></span>|<span data-ttu-id="5ec44-182">Søndag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="5ec44-182">Sunday of the work date week</span></span>|
|`t23`|<span data-ttu-id="5ec44-183">Tirsdag i uge 23 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="5ec44-183">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="5ec44-184">Tirsdag i uge 23 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="5ec44-184">Tuesday of week 23 of the work date year</span></span>|
|`t-1`|<span data-ttu-id="5ec44-185">Tirsdag i uge 1 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="5ec44-185">Tuesday of week 1 of the work date year</span></span>|

##  <a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="5ec44-186">Angive intervaller</span><span class="sxs-lookup"><span data-stu-id="5ec44-186">Setting Ranges</span></span>
<span data-ttu-id="5ec44-187">På lister, i totaler og rapporter kan angive filtre for datoer, klokkeslæt og dato/klokkeslæt, der indeholder en startværdi og eventuelt en slutværdi for kun at få vist dataene i det pågældende interval.</span><span class="sxs-lookup"><span data-stu-id="5ec44-187">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="5ec44-188">Standardreglerne gælder for den måde, du angiver datointervaller på.</span><span class="sxs-lookup"><span data-stu-id="5ec44-188">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="5ec44-189">**Betydning**</span><span class="sxs-lookup"><span data-stu-id="5ec44-189">**Meaning**</span></span>|<span data-ttu-id="5ec44-190">**Eksempeludtryk (dato)**</span><span class="sxs-lookup"><span data-stu-id="5ec44-190">**Sample expression (Date)**</span></span>|<span data-ttu-id="5ec44-191">**Data, der indgår i filteret**</span><span class="sxs-lookup"><span data-stu-id="5ec44-191">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="5ec44-192">Interval</span><span class="sxs-lookup"><span data-stu-id="5ec44-192">Interval</span></span>|<span data-ttu-id="5ec44-193">`12 15 00..01 15 01`  \n`..12 15 00`</span><span class="sxs-lookup"><span data-stu-id="5ec44-193">`12 15 00..01 15 01`  \n`..12 15 00`</span></span>|<span data-ttu-id="5ec44-194">Records med datoer fra og med 15-12-00 til og med 15-01-01.</span><span class="sxs-lookup"><span data-stu-id="5ec44-194">Records with dates between and including 12 15 00 and 01 15 01.</span></span>  <span data-ttu-id="5ec44-195">\nRecords med datoen 15 12 00 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="5ec44-195">\nRecords with dates of 12 15 00 or earlier.</span></span>|
|<span data-ttu-id="5ec44-196">Enten/ eller</span><span class="sxs-lookup"><span data-stu-id="5ec44-196">Either/or</span></span>|<span data-ttu-id="5ec44-197">\`12 15 00</span><span class="sxs-lookup"><span data-stu-id="5ec44-197">\`12 15 00</span></span>|<span data-ttu-id="5ec44-198">12 16 00\`</span><span class="sxs-lookup"><span data-stu-id="5ec44-198">12 16 00\`</span></span>|<span data-ttu-id="5ec44-199">Records med datoen 15 12 00 eller 16 12 00.</span><span class="sxs-lookup"><span data-stu-id="5ec44-199">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="5ec44-200">Hvis der er records med datoer på begge dage, vises de alle.</span><span class="sxs-lookup"><span data-stu-id="5ec44-200">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="5ec44-201">Kombination</span><span class="sxs-lookup"><span data-stu-id="5ec44-201">Combination</span></span>|<span data-ttu-id="5ec44-202">\`12 15 00</span><span class="sxs-lookup"><span data-stu-id="5ec44-202">\`12 15 00</span></span>|<span data-ttu-id="5ec44-203">12 01 00..12 10 00`  \n`..12 14 00</span><span class="sxs-lookup"><span data-stu-id="5ec44-203">12 01 00..12 10 00`  \n`..12 14 00</span></span>|<span data-ttu-id="5ec44-204">12 30 00..\`</span><span class="sxs-lookup"><span data-stu-id="5ec44-204">12 30 00..\`</span></span>|<span data-ttu-id="5ec44-205">Records med datoerne 15-12-00 eller poster fra og med 01-12-00 til og med 10-12-00.</span><span class="sxs-lookup"><span data-stu-id="5ec44-205">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <span data-ttu-id="5ec44-206">\nRecords med datoer den 14-12-00 eller tidligere eller den 30-12-00 eller senere, dvs. alle records, undtagen dokumenter med datoer fra og med 15-12-00 til og med 29-12-00.</span><span class="sxs-lookup"><span data-stu-id="5ec44-206">\nRecords with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="5ec44-207">Du kan bruge de gyldige formater i datointervalfiltre.</span><span class="sxs-lookup"><span data-stu-id="5ec44-207">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="5ec44-208">F.eks. resulterer `mon14 3..t 4p`, der anvendes på et dato og klokkeslætsfelt, i et filter fra kl. 3 mandag i uge 14 for den igangværende arbejdsdatos år, begge inklusive, indtil i dag kl. 16 inklusive.</span><span class="sxs-lookup"><span data-stu-id="5ec44-208">For example, `mon14 3..t 4p` applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>


## <a name="using-date-formulas"></a><span data-ttu-id="5ec44-209">Bruge datoformler</span><span class="sxs-lookup"><span data-stu-id="5ec44-209">Using Date Formulas</span></span>
<span data-ttu-id="5ec44-210">En datoformel er en kort, forkortet kombination af bogstaver og tal, der angiver, hvordan datoer skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="5ec44-210">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="5ec44-211">Du kan angive datoformler i forskellige datoberegningsfelter eller filtre.</span><span class="sxs-lookup"><span data-stu-id="5ec44-211">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="5ec44-212">I alle formlens datafelter indgår en dag automatisk til at dække i dag som den dag, hvor perioden starter.</span><span class="sxs-lookup"><span data-stu-id="5ec44-212">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="5ec44-213">Tilsvarende, hvis du f.eks. indtaster `1W`, så er perioden faktisk otte dage, fordi i dag er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="5ec44-213">Accordingly, for example, if you enter `1W`, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="5ec44-214">Du skal indtaste `6D` eller `1W-1D` for at angive en periode på syv dage \(en rigtig uge\), der medtager periodens startdato.</span><span class="sxs-lookup"><span data-stu-id="5ec44-214">To specify a period of seven days \(one true week\) including the period starting date, then you must enter `6D` or `1W-1D`.</span></span>

<span data-ttu-id="5ec44-215">Her følger et par eksempler på brugen af datoformler:</span><span class="sxs-lookup"><span data-stu-id="5ec44-215">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="5ec44-216">Datoformlen i gentagelsesintervalfeltet i en gentagelseskladde afgør, hvor tit posten på kladdelinjen skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="5ec44-216">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="5ec44-217">Datoformlen i feltet **Respitperiode** for et bestemt rykkerniveau afgør det tidsrum, der skal gå fra forfaldsdatoen \(eller fra datoen for den forrige rykker\), før der oprettes en rykker.</span><span class="sxs-lookup"><span data-stu-id="5ec44-217">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="5ec44-218">Datoformlen i feltet **Forfaldsdatoformel** afgør, hvordan forfaldsdatoen på rykkeren beregnes.</span><span class="sxs-lookup"><span data-stu-id="5ec44-218">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="5ec44-219">Datoformlen kan indeholde op til 20 tegn (både tal og bogstaver).</span><span class="sxs-lookup"><span data-stu-id="5ec44-219">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="5ec44-220">Du kan bruge følgende bogstaver som forkortelser for kalenderenheder.</span><span class="sxs-lookup"><span data-stu-id="5ec44-220">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="5ec44-221">Bogstav</span><span class="sxs-lookup"><span data-stu-id="5ec44-221">Letter</span></span>  |  <span data-ttu-id="5ec44-222">Betyder</span><span class="sxs-lookup"><span data-stu-id="5ec44-222">Meaning</span></span>  |
|----------|----------------------|
|`C`|<span data-ttu-id="5ec44-223">Løbende</span><span class="sxs-lookup"><span data-stu-id="5ec44-223">Current</span></span>|
|`D`|<span data-ttu-id="5ec44-224">Dag\(e\)</span><span class="sxs-lookup"><span data-stu-id="5ec44-224">Day\(s\)</span></span>|
|`W`|<span data-ttu-id="5ec44-225">Uge\(r\)</span><span class="sxs-lookup"><span data-stu-id="5ec44-225">Week\(s\)</span></span>|
|`M`|<span data-ttu-id="5ec44-226">Måned\(er\)</span><span class="sxs-lookup"><span data-stu-id="5ec44-226">Month\(s\)</span></span>|
|`Q`|<span data-ttu-id="5ec44-227">Kvartal\(er\)</span><span class="sxs-lookup"><span data-stu-id="5ec44-227">Quarter\(s\)</span></span>|
|`Y`|<span data-ttu-id="5ec44-228">År\(\)</span><span class="sxs-lookup"><span data-stu-id="5ec44-228">Year\(s\)</span></span>|

<span data-ttu-id="5ec44-229">Datoformlen kan opbygges på tre måder.</span><span class="sxs-lookup"><span data-stu-id="5ec44-229">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="5ec44-230">Følgende eksempel viser, hvordan du skal bruge `C` for aktuel og en tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="5ec44-230">The following example shows how to use `C`, for current, and a time unit.</span></span>

|  <span data-ttu-id="5ec44-231">Udtryk</span><span class="sxs-lookup"><span data-stu-id="5ec44-231">Expression</span></span>  |  <span data-ttu-id="5ec44-232">Betyder</span><span class="sxs-lookup"><span data-stu-id="5ec44-232">Meaning</span></span>  |
|--------------|-----------|
|`CW`|<span data-ttu-id="5ec44-233">Løbende uge</span><span class="sxs-lookup"><span data-stu-id="5ec44-233">Current week</span></span>|
|`CM`|<span data-ttu-id="5ec44-234">Løbende måned</span><span class="sxs-lookup"><span data-stu-id="5ec44-234">Current month</span></span>|

<span data-ttu-id="5ec44-235">Følgende eksempel viser, hvordan du skal bruge et tal og en tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="5ec44-235">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="5ec44-236">Tallet må ikke være større end 9999.</span><span class="sxs-lookup"><span data-stu-id="5ec44-236">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="5ec44-237">Udtryk</span><span class="sxs-lookup"><span data-stu-id="5ec44-237">Expression</span></span>  |  <span data-ttu-id="5ec44-238">Betyder</span><span class="sxs-lookup"><span data-stu-id="5ec44-238">Meaning</span></span>  |
|--------------|-----------|
|`10D`|<span data-ttu-id="5ec44-239">10 dage fra i dag</span><span class="sxs-lookup"><span data-stu-id="5ec44-239">10 days from today</span></span>|
|`2W`|<span data-ttu-id="5ec44-240">2 uger fra i dag</span><span class="sxs-lookup"><span data-stu-id="5ec44-240">2 weeks from today</span></span>|

<span data-ttu-id="5ec44-241">Følgende eksempel viser, hvordan du skal bruge en tidsenhed og et tal.</span><span class="sxs-lookup"><span data-stu-id="5ec44-241">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="5ec44-242">Udtryk</span><span class="sxs-lookup"><span data-stu-id="5ec44-242">Expression</span></span>  |  <span data-ttu-id="5ec44-243">Betyder</span><span class="sxs-lookup"><span data-stu-id="5ec44-243">Meaning</span></span>  |
|--------------|-----------|
|`D10`|<span data-ttu-id="5ec44-244">Den næste 10. dage i en måned</span><span class="sxs-lookup"><span data-stu-id="5ec44-244">The next 10th day of a month</span></span>|
|`WD4`|<span data-ttu-id="5ec44-245">Den næste 4. dag i en uge \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="5ec44-245">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="5ec44-246">Følgende eksempel viser, hvordan du kan kombinere de tre formler efter behov.</span><span class="sxs-lookup"><span data-stu-id="5ec44-246">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="5ec44-247">Udtryk</span><span class="sxs-lookup"><span data-stu-id="5ec44-247">Expression</span></span>  |  <span data-ttu-id="5ec44-248">Betyder</span><span class="sxs-lookup"><span data-stu-id="5ec44-248">Meaning</span></span>  |
|--------------|-----------|
|`CM+10D`|<span data-ttu-id="5ec44-249">Løbende måned \+ 10 dage</span><span class="sxs-lookup"><span data-stu-id="5ec44-249">Current month \+ 10 days</span></span>|

<span data-ttu-id="5ec44-250">Følgende eksempel viser, hvordan du kan bruge et minustegn til at angive en dato i fortiden.</span><span class="sxs-lookup"><span data-stu-id="5ec44-250">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="5ec44-251">Udtryk</span><span class="sxs-lookup"><span data-stu-id="5ec44-251">Expression</span></span>  |  <span data-ttu-id="5ec44-252">Betyder</span><span class="sxs-lookup"><span data-stu-id="5ec44-252">Meaning</span></span>  |
|--------------|-----------|
|`-1Y`|<span data-ttu-id="5ec44-253">1 år siden fra i dag</span><span class="sxs-lookup"><span data-stu-id="5ec44-253">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="5ec44-254">Hvis lokationen bruger en basiskalender, fortolkes den datoformel, du f.eks. indtaster i feltet **Transporttid**, i overensstemmelse med kalenderens arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="5ec44-254">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="5ec44-255">For eksempel betyder `1W` syv arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="5ec44-255">For example, `1W`  means seven working days.</span></span>
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a><span data-ttu-id="5ec44-256">Angive klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="5ec44-256">Entering Times</span></span>
<span data-ttu-id="5ec44-257">Når du angiver klokkeslæt, kan du indsætte separatorer uden mellemrum, som du vil have mellem enhederne, men hvis du bruger to cifre for hver enhed op til millisekunder, er det ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="5ec44-257">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="5ec44-258">Du behøver kun at skrive de største enheder, du vil behøver, de øvrige indstilles til nul.</span><span class="sxs-lookup"><span data-stu-id="5ec44-258">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="5ec44-259">Du kan også udelade AM/PM-symboler.</span><span class="sxs-lookup"><span data-stu-id="5ec44-259">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="5ec44-260">I den følgende tabel kan du se, hvordan du kan indtaste klokkeslæt, og hvordan de fortolkes.</span><span class="sxs-lookup"><span data-stu-id="5ec44-260">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="5ec44-261">Det forudsætter lande/områdeindstillinger, der formaterer tidspunkter i overensstemmelse med: **Timer:Minutter:Sekunder.Millisekunder.**</span><span class="sxs-lookup"><span data-stu-id="5ec44-261">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="5ec44-262">og bruger AM og PM-symbolerne 'AM' og 'PM hhv.</span><span class="sxs-lookup"><span data-stu-id="5ec44-262">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="5ec44-263">**Post**</span><span class="sxs-lookup"><span data-stu-id="5ec44-263">**Entry**</span></span>      |<span data-ttu-id="5ec44-264">**Fortolkning**</span><span class="sxs-lookup"><span data-stu-id="5ec44-264">**Interpretation**</span></span>      |
|---------------|------------------------|
|`05:23:17`|<span data-ttu-id="5ec44-265">05:23:17</span><span class="sxs-lookup"><span data-stu-id="5ec44-265">05:23:17</span></span>|
|`5`|<span data-ttu-id="5ec44-266">05:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-266">05:00:00</span></span>|
|`5AM`|<span data-ttu-id="5ec44-267">05:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-267">05:00:00</span></span>|
|`5P`|<span data-ttu-id="5ec44-268">17:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-268">17:00:00</span></span>|
|`12`|<span data-ttu-id="5ec44-269">12:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-269">12:00:00</span></span>|
|`12A`|<span data-ttu-id="5ec44-270">00:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-270">00:00:00</span></span>|
|`12P`|<span data-ttu-id="5ec44-271">12:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-271">12:00:00</span></span>|
|`17`|<span data-ttu-id="5ec44-272">17:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-272">17:00:00</span></span>|
|`5:30`|<span data-ttu-id="5ec44-273">05:30:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-273">05:30:00</span></span>|
|`0530`|<span data-ttu-id="5ec44-274">05:30:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-274">05:30:00</span></span>|
|`5:30:5`|<span data-ttu-id="5ec44-275">05:30:05</span><span class="sxs-lookup"><span data-stu-id="5ec44-275">05:30:05</span></span>|
|`053005`|<span data-ttu-id="5ec44-276">05:30:05</span><span class="sxs-lookup"><span data-stu-id="5ec44-276">05:30:05</span></span>|
|`5:30:5,50`|<span data-ttu-id="5ec44-277">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="5ec44-277">05:30:05.5</span></span>|
|`053005050`|<span data-ttu-id="5ec44-278">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="5ec44-278">05:30:05.05</span></span>|

<span data-ttu-id="5ec44-279">Du skal være opmærksom på, at millisekunder fortolkes som decimalformat.</span><span class="sxs-lookup"><span data-stu-id="5ec44-279">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="5ec44-280">Altså betyder f.eks. `3`, `30` og `300` alle 300 millisekunder, mens `03` betyder `30` og `003` betyder 3 millisekunder.</span><span class="sxs-lookup"><span data-stu-id="5ec44-280">So, for example, `3`, `30`, and `300` all mean 300 milliseconds, while `03` means `30` and `003` means 3 milliseconds.</span></span>

<span data-ttu-id="5ec44-281">Du kan ikke bruge `24:00` til at angive midnat eller bruge værdier større end 24:00.</span><span class="sxs-lookup"><span data-stu-id="5ec44-281">You cannot use `24:00` to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="5ec44-282">Ordet for 'time" på det sprog, som [!INCLUDE[d365fin](includes/d365fin_long_md.md)] bruger, vurderes til det aktuelle tidspunkt på din computer eller en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="5ec44-282">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="5ec44-283">Du kan angive en del af ordet fra begyndelsen, f.eks. `t` eller `TIM`.</span><span class="sxs-lookup"><span data-stu-id="5ec44-283">You can enter any part of the word, starting from the beginning, such as `t` or `TIM`.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="5ec44-284">Indtaste kombinerede datoer og tidspunkter</span><span class="sxs-lookup"><span data-stu-id="5ec44-284">Entering combined Dates and Times</span></span>
<span data-ttu-id="5ec44-285">Når du angiver dato/klokkeslæt, som en dato og klokkeslæt kombineret i ét felt, skal du angive et mellemrum mellem datoen og klokkeslættet.</span><span class="sxs-lookup"><span data-stu-id="5ec44-285">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="5ec44-286">Datodelen kan kun indeholde mellemrum i form af officielle datoseparatorer af lande/områdeindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="5ec44-286">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="5ec44-287">Tid, der kan indeholde mellemrum omkring AM/PM-symbolet.</span><span class="sxs-lookup"><span data-stu-id="5ec44-287">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="5ec44-288">Det er også muligt kun at angive en dato i et dato/klokkeslætsfelt, men det er ikke muligt kun at angive én gang.</span><span class="sxs-lookup"><span data-stu-id="5ec44-288">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="5ec44-289">Følgende tabel viser eksempler på dato/klokkeslætskombinationer.</span><span class="sxs-lookup"><span data-stu-id="5ec44-289">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="5ec44-290">Lande/områdeindstillinger i eksemplerne viser datoer på dag\-måned\-år-format ved hjælp af AM/PM-symboler, engelsk sprog og søndag som første ugedag.</span><span class="sxs-lookup"><span data-stu-id="5ec44-290">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="5ec44-291">**Post**</span><span class="sxs-lookup"><span data-stu-id="5ec44-291">**Entry**</span></span>      |<span data-ttu-id="5ec44-292">**Fortolkning**</span><span class="sxs-lookup"><span data-stu-id="5ec44-292">**Interpretation**</span></span>      |
|---------------|------------------------|
|`08-01-2016 05:48:12 PM`|<span data-ttu-id="5ec44-293">08\-01\-2016 17:48:12</span><span class="sxs-lookup"><span data-stu-id="5ec44-293">08\-01\-2016 05:48:12 PM</span></span>|
|`131202 132455`|<span data-ttu-id="5ec44-294">13\-12\-2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="5ec44-294">13\-12\-2002 13:24:55</span></span>|
|`1-12-02 10`|<span data-ttu-id="5ec44-295">01\-12\-2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-295">01\-12\-2002 10:00:00</span></span>|
|`1.12.02 5`|<span data-ttu-id="5ec44-296">01\-12\-2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-296">01\-12\-2002 05:00:00</span></span>|
|`1.12.02`|<span data-ttu-id="5ec44-297">01\-12\-2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-297">01\-12\-2002 00:00:00</span></span>|
|`11 12`|<span data-ttu-id="5ec44-298">11\-arbejdsdatomåned\-abejdsdatoår 12:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-298">11\-work date month\-work date year 12:00:00</span></span>|
|`1112 12`|<span data-ttu-id="5ec44-299">11\-12\-arbejdsdatoår 12:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-299">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="5ec44-300">`t` eller `today`</span><span class="sxs-lookup"><span data-stu-id="5ec44-300">`t` or `today`</span></span>|<span data-ttu-id="5ec44-301">dags dato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-301">today's date 00:00:00</span></span>|
|`t 10:30`|<span data-ttu-id="5ec44-302">dags dato 10:30:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-302">today's date 10:30:00</span></span>|
|`t 3:3:3`|<span data-ttu-id="5ec44-303">dags dato 03:03:03</span><span class="sxs-lookup"><span data-stu-id="5ec44-303">today's date 03:03:03</span></span>|
|<span data-ttu-id="5ec44-304">`w` eller `workdate`</span><span class="sxs-lookup"><span data-stu-id="5ec44-304">`w` or `workdate`</span></span>|<span data-ttu-id="5ec44-305">arbejdsdato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-305">the working date 00:00:00</span></span>|
|<span data-ttu-id="5ec44-306">`m` eller `Monday`</span><span class="sxs-lookup"><span data-stu-id="5ec44-306">`m` or `Monday`</span></span>|<span data-ttu-id="5ec44-307">Mandag i ugen for arbejdsdatoen 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-307">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="5ec44-308">`tu` eller `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="5ec44-308">`tu` or `Tuesday`</span></span>|<span data-ttu-id="5ec44-309">Tirsdag i ugen for arbejdsdatoen 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-309">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="5ec44-310">`sa` eller `Saturday`</span><span class="sxs-lookup"><span data-stu-id="5ec44-310">`sa` or `Saturday`</span></span>|<span data-ttu-id="5ec44-311">Lørdag i ugen for arbejdsdatoen 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-311">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="5ec44-312">`s` eller `Sunday`</span><span class="sxs-lookup"><span data-stu-id="5ec44-312">`s` or `Sunday`</span></span>|<span data-ttu-id="5ec44-313">Søndag i ugen for arbejdsdatoen 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-313">Sunday of the work date week 00:00:00</span></span>|
|`tu 10:30`|<span data-ttu-id="5ec44-314">Tirsdag i ugen for arbejdsdatoen 10:30:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-314">Tuesday of the work date week 10:30:00</span></span>|
|`tu 3:3:3`|<span data-ttu-id="5ec44-315">Tirsdag i ugen for arbejdsdatoen 03:03:03</span><span class="sxs-lookup"><span data-stu-id="5ec44-315">Tuesday of the work date week 03:03:03</span></span>|
|`t23 t`|<span data-ttu-id="5ec44-316">Tirsdag i uge 23 i året for arbejdsdatoen, det aktuelle tidspunkt på dagen</span><span class="sxs-lookup"><span data-stu-id="5ec44-316">Tuesday of week 23 of the work date year, current time of day</span></span>|
|`t23`|<span data-ttu-id="5ec44-317">Tirsdag i uge 23 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="5ec44-317">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="5ec44-318">Dags dato 23:00:00</span><span class="sxs-lookup"><span data-stu-id="5ec44-318">Today 23:00:00</span></span>|
|`t-1`|<span data-ttu-id="5ec44-319">Tirsdag i uge 1 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="5ec44-319">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="5ec44-320">Angivelse af varighed</span><span class="sxs-lookup"><span data-stu-id="5ec44-320">Entering Duration</span></span>
<span data-ttu-id="5ec44-321">Nogle felter i programmet repræsenterer en varighed eller et forløbet tidsrum i stedet for en bestemt dato eller klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="5ec44-321">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="5ec44-322">Du angiver varighed ved at skrive et tal efterfulgt af en måleenhed.</span><span class="sxs-lookup"><span data-stu-id="5ec44-322">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="5ec44-323">Her er nogle eksempler.</span><span class="sxs-lookup"><span data-stu-id="5ec44-323">Here are some examples.</span></span>

|<span data-ttu-id="5ec44-324">**Varighed**</span><span class="sxs-lookup"><span data-stu-id="5ec44-324">**Duration**</span></span>|<span data-ttu-id="5ec44-325">**Enhed**</span><span class="sxs-lookup"><span data-stu-id="5ec44-325">**Unit of measure**</span></span>|
|------------|-------------------|
|`2h`|<span data-ttu-id="5ec44-326">2 timer</span><span class="sxs-lookup"><span data-stu-id="5ec44-326">2 hrs</span></span>|
|`6h 30 m`|<span data-ttu-id="5ec44-327">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="5ec44-327">6 hrs 30 mins</span></span>|
|`6.5h`|<span data-ttu-id="5ec44-328">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="5ec44-328">6 hrs 30 mins</span></span>|
|`90m`|<span data-ttu-id="5ec44-329">1 time 30 min</span><span class="sxs-lookup"><span data-stu-id="5ec44-329">1 hr 30 mins</span></span>|
|`2d 6h 30m`|<span data-ttu-id="5ec44-330">2 dage 6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="5ec44-330">2 days 6 hrs 30 mins</span></span>|
|`2d 6h 30m 56s 600ms`|<span data-ttu-id="5ec44-331">2 dage 6 timer 30 min 56 sek 600 msek</span><span class="sxs-lookup"><span data-stu-id="5ec44-331">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="5ec44-332">Du kan også skrive et tal, der automatisk konverteres til en varighed.</span><span class="sxs-lookup"><span data-stu-id="5ec44-332">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="5ec44-333">Det tal, du skriver, konverteres i overensstemmelse med den standardmåleenhed, der er angivet i feltet Varighed.</span><span class="sxs-lookup"><span data-stu-id="5ec44-333">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="5ec44-334">Du kan se, hvilken måleenhed, der anvendes i feltet Varighed, ved at skrive et tal og se, hvilken måleenhed tallet konverteres til.</span><span class="sxs-lookup"><span data-stu-id="5ec44-334">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="5ec44-335">Hvis måleenheden f.eks. er timer, konverteres tallet `5` til 5 timer.</span><span class="sxs-lookup"><span data-stu-id="5ec44-335">For example, if the unit of measure is hours, the number `5` is converted to 5 hrs.</span></span>


## <a name="see-also"></a><span data-ttu-id="5ec44-336">Se også</span><span class="sxs-lookup"><span data-stu-id="5ec44-336">See Also</span></span>
<span data-ttu-id="5ec44-337">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5ec44-337">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5ec44-338">Beregning af forfaldsdato for køb</span><span class="sxs-lookup"><span data-stu-id="5ec44-338">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="5ec44-339">Indtaste kriterier i filtre</span><span class="sxs-lookup"><span data-stu-id="5ec44-339">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

