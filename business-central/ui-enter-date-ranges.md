---
title: Angive datoer og klokkeslæt i Business Central | Microsoft Docs
description: Få at vide, hvordan du angiver datoer og tidspunkter med forskellige produktivitetstip som oversigter, udtryk og områder. Filtrer lister eller rapporter ned til en bestemt dato eller tidsperioder.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: c7e80edfd796056176d37ad12a56c76e64bb44e6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "932974"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="9506e-104">Arbejde med kalenderdatoer og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="9506e-104">Working with Calendar Dates and Times</span></span>

<span data-ttu-id="9506e-105">I [!INCLUDE[d365fin](includes/d365fin_long_md.md)] er der flere måder til at angive datoer og klokkeslæt, herunder effektive funktioner, der fremskynder indtastning af data og hjælper dig med at skrive komplekse kalenderudtryk.</span><span class="sxs-lookup"><span data-stu-id="9506e-105">[!INCLUDE[d365fin](includes/d365fin_long_md.md)] offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="9506e-106">Der er forskellige steder i programmet, hvor du kan angive datoer og klokkeslæt i felterne.</span><span class="sxs-lookup"><span data-stu-id="9506e-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="9506e-107">På en salgsordre kan du f.eks. angive afsendelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="9506e-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="9506e-108">Når du filtrerer lister eller rapportdata, kan du angive datoer og klokkeslæt for kun at finde de data, du er interesseret i.</span><span class="sxs-lookup"><span data-stu-id="9506e-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="9506e-109">Kontrollere internationale og sproglige indstillinger</span><span class="sxs-lookup"><span data-stu-id="9506e-109">Check your region and language settings</span></span>

<span data-ttu-id="9506e-110">Siden [**Mine indstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med dine brugerindstillinger i Business Central") angiver det **Land/område** og **Sprog**, du bruger i systemet.</span><span class="sxs-lookup"><span data-stu-id="9506e-110">The [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="9506e-111">Disse indstillinger påvirker måden, du angiver datoer og klokkeslæt på.</span><span class="sxs-lookup"><span data-stu-id="9506e-111">These settings influence how you enter dates and times.</span></span> 

-   <span data-ttu-id="9506e-112">Indstillingen **Område** bestemmer, hvordan datoer, klokkeslæt, tal og valutaer vises og formateres.</span><span class="sxs-lookup"><span data-stu-id="9506e-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="9506e-113">Når datomønstre omfatter ord, skal sproget for de ord, du bruger, svare til indstillingen **Sprog**.</span><span class="sxs-lookup"><span data-stu-id="9506e-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="9506e-114">anvender den gregorianske kalender.</span><span class="sxs-lookup"><span data-stu-id="9506e-114">uses the Gregorian calendar system.</span></span>

<!-- 
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="9506e-115">Angive datoer</span><span class="sxs-lookup"><span data-stu-id="9506e-115">Entering Dates</span></span>

<span data-ttu-id="9506e-116">I et datofelt kan du angive en dato i standardformatet for din land/områdeindstilling.</span><span class="sxs-lookup"><span data-stu-id="9506e-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="9506e-117">Forskellige områder kan bruge forskellige separatorer mellem dage, måneder og år.</span><span class="sxs-lookup"><span data-stu-id="9506e-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="9506e-118">For eksempel bruger nogle lande/områder bindestreger (mm-dd-åååå), mens andre bruger skråstreger (mm/dd/åååå).</span><span class="sxs-lookup"><span data-stu-id="9506e-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="9506e-119">Du kan dog bruge alle separatorer, selv mellemrum, og datoen ændres automatisk til brug af de separatorer, der gælder for dit land/område.</span><span class="sxs-lookup"><span data-stu-id="9506e-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="9506e-120">Bemærk, at det format, som datoer vises i på udskrevne rapporter eller dokumenter sendt med e-mails, ikke påvirkes af dit personlige valg af land/område.</span><span class="sxs-lookup"><span data-stu-id="9506e-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="9506e-121">For at arbejde mere produktivt med datoer og klokkeslæt kan du bruge de metoder og formater, der er beskrevet i følgende afsnit.</span><span class="sxs-lookup"><span data-stu-id="9506e-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span> 

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="9506e-122">Vælge datoer i kalenderen</span><span class="sxs-lookup"><span data-stu-id="9506e-122">Picking dates from the calendar</span></span>

<span data-ttu-id="9506e-123">De felter, der viser et kalenderikon, kan angives ved hjælp af kalenderdatovælgeren.</span><span class="sxs-lookup"><span data-stu-id="9506e-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="9506e-124">Aktiver kalenderikonet for at få vist kalenderdatovælgeren, eller tryk på Ctrl + Home-tastaturgenvejen i feltet.</span><span class="sxs-lookup"><span data-stu-id="9506e-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="9506e-125">![Datofelter](media/ui-date-field.png "Eksempel på et datofelt")</span><span class="sxs-lookup"><span data-stu-id="9506e-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="9506e-126">Se også [Tastaturgenveje i kalenderdatovælgeren](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="9506e-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts)</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="9506e-127">Mønsteret dag\-uge\-år</span><span class="sxs-lookup"><span data-stu-id="9506e-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="9506e-128">Du kan angive en dato som en ugedag efterfulgt af et ugenummer og eventuelt et år.</span><span class="sxs-lookup"><span data-stu-id="9506e-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="9506e-129">F.eks. betyder `Mon25` eller `mon25` Monday i uge 25.</span><span class="sxs-lookup"><span data-stu-id="9506e-129">For example, `Mon25` or `mon25` means Monday in week 25.</span></span> <span data-ttu-id="9506e-130">Hvis du ikke angiver et år, bruges året fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="9506e-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="9506e-131">I stedet for at skrive hele ordet for den pågældende dag i ugen kan du skrive en del af ordet fra begyndelsen.</span><span class="sxs-lookup"><span data-stu-id="9506e-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="9506e-132">Hvis der opstår konflikter (f.eks. med `s`, som kan være Saturday eller Sunday), vurderes dagene i overensstemmelse med lande/områdeindstillingen.</span><span class="sxs-lookup"><span data-stu-id="9506e-132">In case of conflicts (such as with `s` which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="9506e-133">Input vurderes først mod `workdate` og `today`, så husk dette, når du laver forkortelser.</span><span class="sxs-lookup"><span data-stu-id="9506e-133">The input is first evaluated against `workdate` and `today` as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="9506e-134">F.eks. betyder `t` allerede today så det ikke kan betyde Tuesday eller Thursday.</span><span class="sxs-lookup"><span data-stu-id="9506e-134">For example, `t` already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="9506e-135">Ugenummereringen er altid ISO 8601, hvor er uge 1 uge er den uge, som 4. januar indgår i, eller ugen med den første torsdag i året.</span><span class="sxs-lookup"><span data-stu-id="9506e-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="9506e-136">Talmønstre</span><span class="sxs-lookup"><span data-stu-id="9506e-136">Digit patterns</span></span>

<span data-ttu-id="9506e-137">I et datofelt kan du indtaste to, fire, seks eller otte cifre:</span><span class="sxs-lookup"><span data-stu-id="9506e-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="9506e-138">Hvis du kun indtaster to tal, fortolkes dette som dagen og måneden og året indsættes ud fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="9506e-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="9506e-139">Hvis du indtaster fire tal, fortolkes dette som dagen og måneden, og året indsættes ud fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="9506e-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="9506e-140">Rækkefølgen af dagen og måneden bestemmes af dine områdeindstillinger.</span><span class="sxs-lookup"><span data-stu-id="9506e-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="9506e-141">Selvom områdeindstillingerne har året før dagen og måneden, fortolkes fire tal som dagen og måneden.</span><span class="sxs-lookup"><span data-stu-id="9506e-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="9506e-142">Hvis datoen falder inden for 01-01-1930 og 31-12-2029, kan du nøjes med to tal for året, ellers skal året angives med fire cifre.</span><span class="sxs-lookup"><span data-stu-id="9506e-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="9506e-143">I dag</span><span class="sxs-lookup"><span data-stu-id="9506e-143">Today</span></span>

<span data-ttu-id="9506e-144">Angiv ordet for `today` på det valgte sprog i indstillingen **Sprog**. Dette indstiller datoen til dags dato.</span><span class="sxs-lookup"><span data-stu-id="9506e-144">Enter the word for `today`, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="9506e-145">I stedet for at angive hele ordet kan du angive en del af det fra begyndelsen, f.eks. `t` eller `tod`, så længe det ikke også er begyndelsen på et andet ord.</span><span class="sxs-lookup"><span data-stu-id="9506e-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as `t` or `tod`, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="9506e-146">Periode</span><span class="sxs-lookup"><span data-stu-id="9506e-146">Period</span></span>

<span data-ttu-id="9506e-147">For at filtrere på en bestemt regnskabsperiode skal du i et datofelt skrive bogstavet `p` eller ordet `period` efterfulgt af et tal, der identificerer regnskabsperioden, f.eks. `p2` eller `period4`.</span><span class="sxs-lookup"><span data-stu-id="9506e-147">To filter on a specific accounting period, in a date field enter the letter `p`, or the word `period`, followed by a number that identifies the accounting period, like `p2` or `period4`.</span></span> <span data-ttu-id="9506e-148">Regnskabsperioden passer til regnskabsåret for den aktuelle arbejdsdato, der er angivet i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="9506e-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="9506e-149">F.eks., hvis arbejdsdatoen er **21-03-20**, filtrerer `p1`, eller blot `p`, på den første regnskabsperiode i regnskabsåret 2020 (f.eks. `01/01/20..01/31/20`).</span><span class="sxs-lookup"><span data-stu-id="9506e-149">For example, if the work date is **03/21/20**, then `p1`, or just `p`, filters on the first accounting period of the fiscal year 2020 (such as `01/01/20..01/31/20`).</span></span> <span data-ttu-id="9506e-150">`p15` filtrerer på den 15. regnskabsperiode fra starten på regnskabsåret 2020 (f.eks. `03/01/21..03/31/21`).</span><span class="sxs-lookup"><span data-stu-id="9506e-150">`p15` filters on the fifteenth accounting period from the start of fiscal year 2020 (such as `03/01/21..03/31/21`).</span></span> 

<span data-ttu-id="9506e-151">Regnskabsperioden defineres på siden **Regnskabsperioder**.</span><span class="sxs-lookup"><span data-stu-id="9506e-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="9506e-152">Hvis du vil se eller ændre regnskabsperioderne, skal du åbne siden [her](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="9506e-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="9506e-153">Aktuel arbejdsdato</span><span class="sxs-lookup"><span data-stu-id="9506e-153">Current work date</span></span>

<span data-ttu-id="9506e-154">Med arbejdsdatofunktionen kan du registrere transaktioner ved hjælp af en anden dato end dags dato.</span><span class="sxs-lookup"><span data-stu-id="9506e-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="9506e-155">Ordet for 'workdate' (arbejdsdato) på det sprog, der er angivet i indstillingen **Sprog**, indstiller datoen til den aktuelt angivne arbejdsdato, der er angivet på siden [**Mine indstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med dine brugerindstillinger i Business Central").</span><span class="sxs-lookup"><span data-stu-id="9506e-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page.</span></span> <span data-ttu-id="9506e-156">I stedet for at skrive hele ordet kan du skrive en del af ordet fra begyndelsen, f.eks. 'a' eller 'arbejds'.</span><span class="sxs-lookup"><span data-stu-id="9506e-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="9506e-157">Hvis du ikke har angivet en arbejdsdato, bliver dags dato brugt som arbejdsdato.</span><span class="sxs-lookup"><span data-stu-id="9506e-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="9506e-158">Det er en fordel at anvende en arbejdsdato, hvis du har mange transaktioner at udføre på en dato, der ikke er dags dato.</span><span class="sxs-lookup"><span data-stu-id="9506e-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="9506e-159">Se også [Ændring af grundlæggende indstillinger, f.eks. arbejdsdatoen](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="9506e-159">See also [Changing Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="9506e-160">Ultimodato</span><span class="sxs-lookup"><span data-stu-id="9506e-160">Closing Date</span></span>

<span data-ttu-id="9506e-161">Ved afslutning af et regnskabsår kan du bruge ultimodatoer til at angive, at posten er en ultimopost.</span><span class="sxs-lookup"><span data-stu-id="9506e-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="9506e-162">I teknisk forstand er en ultimodato en hvilken som helst dato mellem to datoer, f.eks. 31. december og 1. januar.</span><span class="sxs-lookup"><span data-stu-id="9506e-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="9506e-163">Hvis en dato skal være en ultimodato, skal du indsætte et `C` lige foran datoen, f.eks. `C123101`.</span><span class="sxs-lookup"><span data-stu-id="9506e-163">To specify that a date is a closing date, put `C` just before the date, such as `C123101`.</span></span> <span data-ttu-id="9506e-164">Dette kan bruges sammen med alle datomønstre.</span><span class="sxs-lookup"><span data-stu-id="9506e-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="9506e-165">Eksempler</span><span class="sxs-lookup"><span data-stu-id="9506e-165">Examples</span></span>

<span data-ttu-id="9506e-166">Følgende tabel indeholder eksempler på datoer i alle formater.</span><span class="sxs-lookup"><span data-stu-id="9506e-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="9506e-167">Det forudsætter lande/områdeindstillinger, der formaterer datoer i henhold til: **år.måned.dag.**, en uge, der begynder om mandagen, og hvor sproget er engelsk.</span><span class="sxs-lookup"><span data-stu-id="9506e-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="9506e-168">**Post**</span><span class="sxs-lookup"><span data-stu-id="9506e-168">**Entry**</span></span>      |<span data-ttu-id="9506e-169">**Fortolkning**</span><span class="sxs-lookup"><span data-stu-id="9506e-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|`2018.12.31.`|<span data-ttu-id="9506e-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="9506e-170">2018.12.31.</span></span>|
|`181231`|<span data-ttu-id="9506e-171">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="9506e-171">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="9506e-172">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="9506e-172">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="9506e-173">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="9506e-173">2018.12.31.</span></span>|
|`20181231`|<span data-ttu-id="9506e-174">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="9506e-174">2018.12.31.</span></span>|
|`18/12,31`|<span data-ttu-id="9506e-175">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="9506e-175">2018.12.31.</span></span>|
|`11`|<span data-ttu-id="9506e-176">arbejdsdatoår.abejdsdatomåned.11.</span><span class="sxs-lookup"><span data-stu-id="9506e-176">work date year.work date month.11.</span></span>|
|`1112`|<span data-ttu-id="9506e-177">arbejdsdatoår.11.12.</span><span class="sxs-lookup"><span data-stu-id="9506e-177">work date year.11.12.</span></span>|
|<span data-ttu-id="9506e-178">`t` eller `today`</span><span class="sxs-lookup"><span data-stu-id="9506e-178">`t` or `today`</span></span>|<span data-ttu-id="9506e-179">dags dato</span><span class="sxs-lookup"><span data-stu-id="9506e-179">today's date</span></span>|
|`p4`|<span data-ttu-id="9506e-180">datointerval, der indeholder den fjerde regnskabsperiode, f.eks. `04/01/20..04/30/20`</span><span class="sxs-lookup"><span data-stu-id="9506e-180">date range that includes the fourth accounting period, such as `04/01/20..04/30/20`</span></span>|
|<span data-ttu-id="9506e-181">`w` eller `workdate`</span><span class="sxs-lookup"><span data-stu-id="9506e-181">`w` or `workdate`</span></span>|<span data-ttu-id="9506e-182">arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="9506e-182">the working date</span></span>|
|<span data-ttu-id="9506e-183">`m` eller `Monday`</span><span class="sxs-lookup"><span data-stu-id="9506e-183">`m` or `Monday`</span></span>|<span data-ttu-id="9506e-184">Mandag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="9506e-184">Monday of the work date week</span></span>|
|<span data-ttu-id="9506e-185">`tu` eller `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="9506e-185">`tu` or `Tuesday`</span></span>|<span data-ttu-id="9506e-186">Tirsdag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="9506e-186">Tuesday of the work date week</span></span>|
|<span data-ttu-id="9506e-187">`sa` eller `Saturday`</span><span class="sxs-lookup"><span data-stu-id="9506e-187">`sa` or `Saturday`</span></span>|<span data-ttu-id="9506e-188">Lørdag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="9506e-188">Saturday of the work date week</span></span>|
|<span data-ttu-id="9506e-189">`s` eller `Sunday`</span><span class="sxs-lookup"><span data-stu-id="9506e-189">`s` or `Sunday`</span></span>|<span data-ttu-id="9506e-190">Søndag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="9506e-190">Sunday of the work date week</span></span>|
|`t23`|<span data-ttu-id="9506e-191">Tirsdag i uge 23 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="9506e-191">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="9506e-192">Tirsdag i uge 23 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="9506e-192">Tuesday of week 23 of the work date year</span></span>|
|`t-1`|<span data-ttu-id="9506e-193">Tirsdag i uge 1 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="9506e-193">Tuesday of week 1 of the work date year</span></span>|

##  <a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="9506e-194">Angive intervaller</span><span class="sxs-lookup"><span data-stu-id="9506e-194">Setting Ranges</span></span>

<span data-ttu-id="9506e-195">På lister, i totaler og rapporter kan angive filtre for datoer, klokkeslæt og dato/klokkeslæt, der indeholder en startværdi og eventuelt en slutværdi for kun at få vist dataene i det pågældende interval.</span><span class="sxs-lookup"><span data-stu-id="9506e-195">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="9506e-196">Standardreglerne gælder for den måde, du angiver datointervaller på.</span><span class="sxs-lookup"><span data-stu-id="9506e-196">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="9506e-197">**Betydning**</span><span class="sxs-lookup"><span data-stu-id="9506e-197">**Meaning**</span></span>|<span data-ttu-id="9506e-198">**Eksempeludtryk (dato)**</span><span class="sxs-lookup"><span data-stu-id="9506e-198">**Sample expression (Date)**</span></span>|<span data-ttu-id="9506e-199">**Data, der indgår i filteret**</span><span class="sxs-lookup"><span data-stu-id="9506e-199">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="9506e-200">Interval</span><span class="sxs-lookup"><span data-stu-id="9506e-200">Interval</span></span>|`12 15 00..01 15 01`<br /><br />`..12 15 00`<br /><br />`p1..p4`|<span data-ttu-id="9506e-201">Records med datoer fra og med 15-12-00 til og med 15-01-01.</span><span class="sxs-lookup"><span data-stu-id="9506e-201">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="9506e-202">Records med datoen 15 12 00 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="9506e-202">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="9506e-203">Datointerval, der indeholder den anden, tredje og fjerde regnskabsperiode, f.eks. `01/01/20..04/30/20`.</span><span class="sxs-lookup"><span data-stu-id="9506e-203">Date range that includes the second, third, and fourth accounting periods, such as `01/01/20..04/30/20`.</span></span>|
|<span data-ttu-id="9506e-204">Enten/ eller</span><span class="sxs-lookup"><span data-stu-id="9506e-204">Either/or</span></span>|`12 15 00|12 16 00`|<span data-ttu-id="9506e-205">Records med datoen 15 12 00 eller 16 12 00.</span><span class="sxs-lookup"><span data-stu-id="9506e-205">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="9506e-206">Hvis der er records med datoer på begge dage, vises de alle.</span><span class="sxs-lookup"><span data-stu-id="9506e-206">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="9506e-207">Kombination</span><span class="sxs-lookup"><span data-stu-id="9506e-207">Combination</span></span>|<span data-ttu-id="9506e-208">`12 15 00|12 01 00..12 10 00`  \n`..12 14 00|12 30 00..`</span><span class="sxs-lookup"><span data-stu-id="9506e-208">`12 15 00|12 01 00..12 10 00`  \n`..12 14 00|12 30 00..`</span></span>|<span data-ttu-id="9506e-209">Records med datoerne 15-12-00 eller poster fra og med 01-12-00 til og med 10-12-00.</span><span class="sxs-lookup"><span data-stu-id="9506e-209">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <span data-ttu-id="9506e-210">\nRecords med datoer den 14-12-00 eller tidligere eller den 30-12-00 eller senere, dvs. alle records, undtagen dokumenter med datoer fra og med 15-12-00 til og med 29-12-00.</span><span class="sxs-lookup"><span data-stu-id="9506e-210">\nRecords with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="9506e-211">Du kan bruge de gyldige formater i datointervalfiltre.</span><span class="sxs-lookup"><span data-stu-id="9506e-211">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="9506e-212">F.eks. resulterer `mon14 3..t 4p`, der anvendes på et dato og klokkeslætsfelt, i et filter fra kl. 3 mandag i uge 14 for den igangværende arbejdsdatos år, begge inklusive, indtil i dag kl. 16 inklusive.</span><span class="sxs-lookup"><span data-stu-id="9506e-212">For example, `mon14 3..t 4p` applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="9506e-213">Bruge datoformler</span><span class="sxs-lookup"><span data-stu-id="9506e-213">Using Date Formulas</span></span>
<span data-ttu-id="9506e-214">En datoformel er en kort, forkortet kombination af bogstaver og tal, der angiver, hvordan datoer skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="9506e-214">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="9506e-215">Du kan angive datoformler i forskellige datoberegningsfelter eller filtre.</span><span class="sxs-lookup"><span data-stu-id="9506e-215">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="9506e-216">I alle formlens datafelter indgår en dag automatisk til at dække i dag som den dag, hvor perioden starter.</span><span class="sxs-lookup"><span data-stu-id="9506e-216">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="9506e-217">Tilsvarende, hvis du f.eks. indtaster `1W`, så er perioden faktisk otte dage, fordi i dag er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="9506e-217">Accordingly, for example, if you enter `1W`, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="9506e-218">Du skal indtaste `6D` eller `1W-1D` for at angive en periode på syv dage \(en rigtig uge\), der medtager periodens startdato.</span><span class="sxs-lookup"><span data-stu-id="9506e-218">To specify a period of seven days \(one true week\) including the period starting date, then you must enter `6D` or `1W-1D`.</span></span>

<span data-ttu-id="9506e-219">Her følger et par eksempler på brugen af datoformler:</span><span class="sxs-lookup"><span data-stu-id="9506e-219">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="9506e-220">Datoformlen i gentagelsesintervalfeltet i en gentagelseskladde afgør, hvor tit posten på kladdelinjen skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="9506e-220">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="9506e-221">Datoformlen i feltet **Respitperiode** for et bestemt rykkerniveau afgør det tidsrum, der skal gå fra forfaldsdatoen \(eller fra datoen for den forrige rykker\), før der oprettes en rykker.</span><span class="sxs-lookup"><span data-stu-id="9506e-221">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="9506e-222">Datoformlen i feltet **Forfaldsdatoformel** afgør, hvordan forfaldsdatoen på rykkeren beregnes.</span><span class="sxs-lookup"><span data-stu-id="9506e-222">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="9506e-223">Datoformlen kan indeholde op til 20 tegn (både tal og bogstaver).</span><span class="sxs-lookup"><span data-stu-id="9506e-223">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="9506e-224">Du kan bruge følgende bogstaver som forkortelser for kalenderenheder.</span><span class="sxs-lookup"><span data-stu-id="9506e-224">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="9506e-225">Bogstav</span><span class="sxs-lookup"><span data-stu-id="9506e-225">Letter</span></span>  |  <span data-ttu-id="9506e-226">Betyder</span><span class="sxs-lookup"><span data-stu-id="9506e-226">Meaning</span></span>  |
|----------|----------------------|
|`C`|<span data-ttu-id="9506e-227">Løbende</span><span class="sxs-lookup"><span data-stu-id="9506e-227">Current</span></span>|
|`D`|<span data-ttu-id="9506e-228">Dag\(e\)</span><span class="sxs-lookup"><span data-stu-id="9506e-228">Day\(s\)</span></span>|
|`W`|<span data-ttu-id="9506e-229">Uge\(r\)</span><span class="sxs-lookup"><span data-stu-id="9506e-229">Week\(s\)</span></span>|
|`M`|<span data-ttu-id="9506e-230">Måned\(er\)</span><span class="sxs-lookup"><span data-stu-id="9506e-230">Month\(s\)</span></span>|
|`Q`|<span data-ttu-id="9506e-231">Kvartal\(er\)</span><span class="sxs-lookup"><span data-stu-id="9506e-231">Quarter\(s\)</span></span>|
|`Y`|<span data-ttu-id="9506e-232">År\(\)</span><span class="sxs-lookup"><span data-stu-id="9506e-232">Year\(s\)</span></span>|

<span data-ttu-id="9506e-233">Datoformlen kan opbygges på tre måder.</span><span class="sxs-lookup"><span data-stu-id="9506e-233">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="9506e-234">Følgende eksempel viser, hvordan du skal bruge `C` for aktuel og en tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="9506e-234">The following example shows how to use `C`, for current, and a time unit.</span></span>

|  <span data-ttu-id="9506e-235">Udtryk</span><span class="sxs-lookup"><span data-stu-id="9506e-235">Expression</span></span>  |  <span data-ttu-id="9506e-236">Betyder</span><span class="sxs-lookup"><span data-stu-id="9506e-236">Meaning</span></span>  |
|--------------|-----------|
|`CW`|<span data-ttu-id="9506e-237">Løbende uge</span><span class="sxs-lookup"><span data-stu-id="9506e-237">Current week</span></span>|
|`CM`|<span data-ttu-id="9506e-238">Løbende måned</span><span class="sxs-lookup"><span data-stu-id="9506e-238">Current month</span></span>|

<span data-ttu-id="9506e-239">Følgende eksempel viser, hvordan du skal bruge et tal og en tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="9506e-239">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="9506e-240">Tallet må ikke være større end 9999.</span><span class="sxs-lookup"><span data-stu-id="9506e-240">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="9506e-241">Udtryk</span><span class="sxs-lookup"><span data-stu-id="9506e-241">Expression</span></span>  |  <span data-ttu-id="9506e-242">Betyder</span><span class="sxs-lookup"><span data-stu-id="9506e-242">Meaning</span></span>  |
|--------------|-----------|
|`10D`|<span data-ttu-id="9506e-243">10 dage fra i dag</span><span class="sxs-lookup"><span data-stu-id="9506e-243">10 days from today</span></span>|
|`2W`|<span data-ttu-id="9506e-244">2 uger fra i dag</span><span class="sxs-lookup"><span data-stu-id="9506e-244">2 weeks from today</span></span>|

<span data-ttu-id="9506e-245">Følgende eksempel viser, hvordan du skal bruge en tidsenhed og et tal.</span><span class="sxs-lookup"><span data-stu-id="9506e-245">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="9506e-246">Udtryk</span><span class="sxs-lookup"><span data-stu-id="9506e-246">Expression</span></span>  |  <span data-ttu-id="9506e-247">Betyder</span><span class="sxs-lookup"><span data-stu-id="9506e-247">Meaning</span></span>  |
|--------------|-----------|
|`D10`|<span data-ttu-id="9506e-248">Den næste 10. dage i en måned</span><span class="sxs-lookup"><span data-stu-id="9506e-248">The next 10th day of a month</span></span>|
|`WD4`|<span data-ttu-id="9506e-249">Den næste 4. dag i en uge \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="9506e-249">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="9506e-250">Følgende eksempel viser, hvordan du kan kombinere de tre formler efter behov.</span><span class="sxs-lookup"><span data-stu-id="9506e-250">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="9506e-251">Udtryk</span><span class="sxs-lookup"><span data-stu-id="9506e-251">Expression</span></span>  |  <span data-ttu-id="9506e-252">Betyder</span><span class="sxs-lookup"><span data-stu-id="9506e-252">Meaning</span></span>  |
|--------------|-----------|
|`CM+10D`|<span data-ttu-id="9506e-253">Løbende måned \+ 10 dage</span><span class="sxs-lookup"><span data-stu-id="9506e-253">Current month \+ 10 days</span></span>|

<span data-ttu-id="9506e-254">Følgende eksempel viser, hvordan du kan bruge et minustegn til at angive en dato i fortiden.</span><span class="sxs-lookup"><span data-stu-id="9506e-254">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="9506e-255">Udtryk</span><span class="sxs-lookup"><span data-stu-id="9506e-255">Expression</span></span>  |  <span data-ttu-id="9506e-256">Betyder</span><span class="sxs-lookup"><span data-stu-id="9506e-256">Meaning</span></span>  |
|--------------|-----------|
|`-1Y`|<span data-ttu-id="9506e-257">1 år siden fra i dag</span><span class="sxs-lookup"><span data-stu-id="9506e-257">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="9506e-258">Hvis lokationen bruger en basiskalender, fortolkes den datoformel, du f.eks. indtaster i feltet **Transporttid**, i overensstemmelse med kalenderens arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="9506e-258">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="9506e-259">For eksempel betyder `1W` syv arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="9506e-259">For example, `1W`  means seven working days.</span></span>
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

## <a name="entering-times"></a><span data-ttu-id="9506e-260">Angive klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="9506e-260">Entering Times</span></span>
<span data-ttu-id="9506e-261">Når du angiver klokkeslæt, kan du indsætte separatorer uden mellemrum, som du vil have mellem enhederne, men hvis du bruger to cifre for hver enhed op til millisekunder, er det ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="9506e-261">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="9506e-262">Du behøver kun at skrive de største enheder, du vil behøver, de øvrige indstilles til nul.</span><span class="sxs-lookup"><span data-stu-id="9506e-262">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="9506e-263">Du kan også udelade AM/PM-symboler.</span><span class="sxs-lookup"><span data-stu-id="9506e-263">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="9506e-264">I den følgende tabel kan du se, hvordan du kan indtaste klokkeslæt, og hvordan de fortolkes.</span><span class="sxs-lookup"><span data-stu-id="9506e-264">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="9506e-265">Det forudsætter lande/områdeindstillinger, der formaterer tidspunkter i overensstemmelse med: **Timer:Minutter:Sekunder.Millisekunder.**</span><span class="sxs-lookup"><span data-stu-id="9506e-265">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="9506e-266">og bruger AM og PM-symbolerne 'AM' og 'PM hhv.</span><span class="sxs-lookup"><span data-stu-id="9506e-266">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="9506e-267">**Post**</span><span class="sxs-lookup"><span data-stu-id="9506e-267">**Entry**</span></span>      |<span data-ttu-id="9506e-268">**Fortolkning**</span><span class="sxs-lookup"><span data-stu-id="9506e-268">**Interpretation**</span></span>      |
|---------------|------------------------|
|`05:23:17`|<span data-ttu-id="9506e-269">05:23:17</span><span class="sxs-lookup"><span data-stu-id="9506e-269">05:23:17</span></span>|
|`5`|<span data-ttu-id="9506e-270">05:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-270">05:00:00</span></span>|
|`5AM`|<span data-ttu-id="9506e-271">05:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-271">05:00:00</span></span>|
|`5P`|<span data-ttu-id="9506e-272">17:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-272">17:00:00</span></span>|
|`12`|<span data-ttu-id="9506e-273">12:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-273">12:00:00</span></span>|
|`12A`|<span data-ttu-id="9506e-274">00:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-274">00:00:00</span></span>|
|`12P`|<span data-ttu-id="9506e-275">12:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-275">12:00:00</span></span>|
|`17`|<span data-ttu-id="9506e-276">17:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-276">17:00:00</span></span>|
|`5:30`|<span data-ttu-id="9506e-277">05:30:00</span><span class="sxs-lookup"><span data-stu-id="9506e-277">05:30:00</span></span>|
|`0530`|<span data-ttu-id="9506e-278">05:30:00</span><span class="sxs-lookup"><span data-stu-id="9506e-278">05:30:00</span></span>|
|`5:30:5`|<span data-ttu-id="9506e-279">05:30:05</span><span class="sxs-lookup"><span data-stu-id="9506e-279">05:30:05</span></span>|
|`053005`|<span data-ttu-id="9506e-280">05:30:05</span><span class="sxs-lookup"><span data-stu-id="9506e-280">05:30:05</span></span>|
|`5:30:5,50`|<span data-ttu-id="9506e-281">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="9506e-281">05:30:05.5</span></span>|
|`053005050`|<span data-ttu-id="9506e-282">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="9506e-282">05:30:05.05</span></span>|

<span data-ttu-id="9506e-283">Du skal være opmærksom på, at millisekunder fortolkes som decimalformat.</span><span class="sxs-lookup"><span data-stu-id="9506e-283">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="9506e-284">Altså betyder f.eks. `3`, `30` og `300` alle 300 millisekunder, mens `03` betyder `30` og `003` betyder 3 millisekunder.</span><span class="sxs-lookup"><span data-stu-id="9506e-284">So, for example, `3`, `30`, and `300` all mean 300 milliseconds, while `03` means `30` and `003` means 3 milliseconds.</span></span>

<span data-ttu-id="9506e-285">Du kan ikke bruge `24:00` til at angive midnat eller bruge værdier større end 24:00.</span><span class="sxs-lookup"><span data-stu-id="9506e-285">You cannot use `24:00` to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="9506e-286">Ordet for 'time" på det sprog, som [!INCLUDE[d365fin](includes/d365fin_long_md.md)] bruger, vurderes til det aktuelle tidspunkt på din computer eller en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="9506e-286">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="9506e-287">Du kan angive en del af ordet fra begyndelsen, f.eks. `t` eller `TIM`.</span><span class="sxs-lookup"><span data-stu-id="9506e-287">You can enter any part of the word, starting from the beginning, such as `t` or `TIM`.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="9506e-288">Indtaste kombinerede datoer og tidspunkter</span><span class="sxs-lookup"><span data-stu-id="9506e-288">Entering combined Dates and Times</span></span>
<span data-ttu-id="9506e-289">Når du angiver dato/klokkeslæt, som en dato og klokkeslæt kombineret i ét felt, skal du angive et mellemrum mellem datoen og klokkeslættet.</span><span class="sxs-lookup"><span data-stu-id="9506e-289">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="9506e-290">Datodelen kan kun indeholde mellemrum i form af officielle datoseparatorer af lande/områdeindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="9506e-290">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="9506e-291">Tid, der kan indeholde mellemrum omkring AM/PM-symbolet.</span><span class="sxs-lookup"><span data-stu-id="9506e-291">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="9506e-292">Det er også muligt kun at angive en dato i et dato/klokkeslætsfelt, men det er ikke muligt kun at angive én gang.</span><span class="sxs-lookup"><span data-stu-id="9506e-292">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="9506e-293">Følgende tabel viser eksempler på dato/klokkeslætskombinationer.</span><span class="sxs-lookup"><span data-stu-id="9506e-293">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="9506e-294">Lande/områdeindstillinger i eksemplerne viser datoer på dag\-måned\-år-format ved hjælp af AM/PM-symboler, engelsk sprog og søndag som første ugedag.</span><span class="sxs-lookup"><span data-stu-id="9506e-294">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="9506e-295">**Post**</span><span class="sxs-lookup"><span data-stu-id="9506e-295">**Entry**</span></span>      |<span data-ttu-id="9506e-296">**Fortolkning**</span><span class="sxs-lookup"><span data-stu-id="9506e-296">**Interpretation**</span></span>      |
|---------------|------------------------|
|`08-01-2016 05:48:12 PM`|<span data-ttu-id="9506e-297">08\-01\-2016 17:48:12</span><span class="sxs-lookup"><span data-stu-id="9506e-297">08\-01\-2016 05:48:12 PM</span></span>|
|`131202 132455`|<span data-ttu-id="9506e-298">13\-12\-2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="9506e-298">13\-12\-2002 13:24:55</span></span>|
|`1-12-02 10`|<span data-ttu-id="9506e-299">01\-12\-2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-299">01\-12\-2002 10:00:00</span></span>|
|`1.12.02 5`|<span data-ttu-id="9506e-300">01\-12\-2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-300">01\-12\-2002 05:00:00</span></span>|
|`1.12.02`|<span data-ttu-id="9506e-301">01\-12\-2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-301">01\-12\-2002 00:00:00</span></span>|
|`11 12`|<span data-ttu-id="9506e-302">11\-arbejdsdatomåned\-abejdsdatoår 12:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-302">11\-work date month\-work date year 12:00:00</span></span>|
|`1112 12`|<span data-ttu-id="9506e-303">11\-12\-arbejdsdatoår 12:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-303">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="9506e-304">`t` eller `today`</span><span class="sxs-lookup"><span data-stu-id="9506e-304">`t` or `today`</span></span>|<span data-ttu-id="9506e-305">dags dato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-305">today's date 00:00:00</span></span>|
|`t 10:30`|<span data-ttu-id="9506e-306">dags dato 10:30:00</span><span class="sxs-lookup"><span data-stu-id="9506e-306">today's date 10:30:00</span></span>|
|`t 3:3:3`|<span data-ttu-id="9506e-307">dags dato 03:03:03</span><span class="sxs-lookup"><span data-stu-id="9506e-307">today's date 03:03:03</span></span>|
|<span data-ttu-id="9506e-308">`w` eller `workdate`</span><span class="sxs-lookup"><span data-stu-id="9506e-308">`w` or `workdate`</span></span>|<span data-ttu-id="9506e-309">arbejdsdato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-309">the working date 00:00:00</span></span>|
|<span data-ttu-id="9506e-310">`m` eller `Monday`</span><span class="sxs-lookup"><span data-stu-id="9506e-310">`m` or `Monday`</span></span>|<span data-ttu-id="9506e-311">Mandag i ugen for arbejdsdatoen 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-311">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="9506e-312">`tu` eller `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="9506e-312">`tu` or `Tuesday`</span></span>|<span data-ttu-id="9506e-313">Tirsdag i ugen for arbejdsdatoen 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-313">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="9506e-314">`sa` eller `Saturday`</span><span class="sxs-lookup"><span data-stu-id="9506e-314">`sa` or `Saturday`</span></span>|<span data-ttu-id="9506e-315">Lørdag i ugen for arbejdsdatoen 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-315">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="9506e-316">`s` eller `Sunday`</span><span class="sxs-lookup"><span data-stu-id="9506e-316">`s` or `Sunday`</span></span>|<span data-ttu-id="9506e-317">Søndag i ugen for arbejdsdatoen 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-317">Sunday of the work date week 00:00:00</span></span>|
|`tu 10:30`|<span data-ttu-id="9506e-318">Tirsdag i ugen for arbejdsdatoen 10:30:00</span><span class="sxs-lookup"><span data-stu-id="9506e-318">Tuesday of the work date week 10:30:00</span></span>|
|`tu 3:3:3`|<span data-ttu-id="9506e-319">Tirsdag i ugen for arbejdsdatoen 03:03:03</span><span class="sxs-lookup"><span data-stu-id="9506e-319">Tuesday of the work date week 03:03:03</span></span>|
|`t23 t`|<span data-ttu-id="9506e-320">Tirsdag i uge 23 i året for arbejdsdatoen, det aktuelle tidspunkt på dagen</span><span class="sxs-lookup"><span data-stu-id="9506e-320">Tuesday of week 23 of the work date year, current time of day</span></span>|
|`t23`|<span data-ttu-id="9506e-321">Tirsdag i uge 23 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="9506e-321">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="9506e-322">Dags dato 23:00:00</span><span class="sxs-lookup"><span data-stu-id="9506e-322">Today 23:00:00</span></span>|
|`t-1`|<span data-ttu-id="9506e-323">Tirsdag i uge 1 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="9506e-323">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="9506e-324">Angivelse af varighed</span><span class="sxs-lookup"><span data-stu-id="9506e-324">Entering Duration</span></span>
<span data-ttu-id="9506e-325">Nogle felter i programmet repræsenterer en varighed eller et forløbet tidsrum i stedet for en bestemt dato eller klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="9506e-325">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="9506e-326">Du angiver varighed ved at skrive et tal efterfulgt af en måleenhed.</span><span class="sxs-lookup"><span data-stu-id="9506e-326">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="9506e-327">Her er nogle eksempler.</span><span class="sxs-lookup"><span data-stu-id="9506e-327">Here are some examples.</span></span>

|<span data-ttu-id="9506e-328">**Varighed**</span><span class="sxs-lookup"><span data-stu-id="9506e-328">**Duration**</span></span>|<span data-ttu-id="9506e-329">**Enhed**</span><span class="sxs-lookup"><span data-stu-id="9506e-329">**Unit of measure**</span></span>|
|------------|-------------------|
|`2h`|<span data-ttu-id="9506e-330">2 timer</span><span class="sxs-lookup"><span data-stu-id="9506e-330">2 hrs</span></span>|
|`6h 30 m`|<span data-ttu-id="9506e-331">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="9506e-331">6 hrs 30 mins</span></span>|
|`6.5h`|<span data-ttu-id="9506e-332">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="9506e-332">6 hrs 30 mins</span></span>|
|`90m`|<span data-ttu-id="9506e-333">1 time 30 min</span><span class="sxs-lookup"><span data-stu-id="9506e-333">1 hr 30 mins</span></span>|
|`2d 6h 30m`|<span data-ttu-id="9506e-334">2 dage 6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="9506e-334">2 days 6 hrs 30 mins</span></span>|
|`2d 6h 30m 56s 600ms`|<span data-ttu-id="9506e-335">2 dage 6 timer 30 min 56 sek 600 msek</span><span class="sxs-lookup"><span data-stu-id="9506e-335">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="9506e-336">Du kan også skrive et tal, der automatisk konverteres til en varighed.</span><span class="sxs-lookup"><span data-stu-id="9506e-336">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="9506e-337">Det tal, du skriver, konverteres i overensstemmelse med den standardmåleenhed, der er angivet i feltet Varighed.</span><span class="sxs-lookup"><span data-stu-id="9506e-337">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="9506e-338">Du kan se, hvilken måleenhed, der anvendes i feltet Varighed, ved at skrive et tal og se, hvilken måleenhed tallet konverteres til.</span><span class="sxs-lookup"><span data-stu-id="9506e-338">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="9506e-339">Hvis måleenheden f.eks. er timer, konverteres tallet `5` til 5 timer.</span><span class="sxs-lookup"><span data-stu-id="9506e-339">For example, if the unit of measure is hours, the number `5` is converted to 5 hrs.</span></span>


## <a name="see-also"></a><span data-ttu-id="9506e-340">Se også</span><span class="sxs-lookup"><span data-stu-id="9506e-340">See Also</span></span>
<span data-ttu-id="9506e-341">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9506e-341">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="9506e-342">Beregning af forfaldsdato for køb</span><span class="sxs-lookup"><span data-stu-id="9506e-342">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="9506e-343">Indtaste kriterier i filtre</span><span class="sxs-lookup"><span data-stu-id="9506e-343">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
