---
title: Angive datoer og klokkeslæt i Business Central | Microsoft Docs
description: Få at vide, hvordan du angiver datoer og tidspunkter med forskellige produktivitetstip som oversigter, udtryk og områder. Filtrer lister eller rapporter ned til en bestemt dato eller tidsperioder.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 09/17/2019
ms.author: sgroespe
ms.openlocfilehash: 96471b07d48120db7fda5e48a14c9ca0147688fb
ms.sourcegitcommit: 7ce8005806465417c7040c61da1d6cada29cd9c0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/17/2019
ms.locfileid: "2000759"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="ffe0c-104">Arbejde med kalenderdatoer og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="ffe0c-104">Working with Calendar Dates and Times</span></span>

<span data-ttu-id="ffe0c-105">I [!INCLUDE[d365fin](includes/d365fin_long_md.md)] er der flere måder til at angive datoer og klokkeslæt, herunder effektive funktioner, der fremskynder indtastning af data og hjælper dig med at skrive komplekse kalenderudtryk.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-105">[!INCLUDE[d365fin](includes/d365fin_long_md.md)] offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="ffe0c-106">Der er forskellige steder i programmet, hvor du kan angive datoer og klokkeslæt i felterne.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="ffe0c-107">På en salgsordre kan du f.eks. angive afsendelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="ffe0c-108">Når du filtrerer lister eller rapportdata, kan du angive datoer og klokkeslæt for kun at finde de data, du er interesseret i.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="ffe0c-109">Kontrollere internationale og sproglige indstillinger</span><span class="sxs-lookup"><span data-stu-id="ffe0c-109">Check your region and language settings</span></span>

<span data-ttu-id="ffe0c-110">Siden [**Mine indstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med dine brugerindstillinger i Business Central") angiver det **Land/område** og **Sprog**, du bruger i systemet.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-110">The [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="ffe0c-111">Disse indstillinger påvirker måden, du angiver datoer og klokkeslæt på.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-111">These settings influence how you enter dates and times.</span></span>

-   <span data-ttu-id="ffe0c-112">Indstillingen **Område** bestemmer, hvordan datoer, klokkeslæt, tal og valutaer vises og formateres.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="ffe0c-113">Når datomønstre omfatter ord, skal sproget for de ord, du bruger, svare til indstillingen **Sprog**.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="ffe0c-114">anvender den gregorianske kalender.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-114">uses the Gregorian calendar system.</span></span>

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="ffe0c-115">Angive datoer</span><span class="sxs-lookup"><span data-stu-id="ffe0c-115">Entering Dates</span></span>

<span data-ttu-id="ffe0c-116">I et datofelt kan du angive en dato i standardformatet for din land/områdeindstilling.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="ffe0c-117">Forskellige områder kan bruge forskellige separatorer mellem dage, måneder og år.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="ffe0c-118">For eksempel bruger nogle lande/områder bindestreger (mm-dd-åååå), mens andre bruger skråstreger (mm/dd/åååå).</span><span class="sxs-lookup"><span data-stu-id="ffe0c-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="ffe0c-119">Du kan dog bruge alle separatorer, selv mellemrum, og datoen ændres automatisk til brug af de separatorer, der gælder for dit land/område.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="ffe0c-120">Bemærk, at det format, som datoer vises i på udskrevne rapporter eller dokumenter sendt med e-mails, ikke påvirkes af dit personlige valg af land/område.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="ffe0c-121">For at arbejde mere produktivt med datoer og klokkeslæt kan du bruge de metoder og formater, der er beskrevet i følgende afsnit.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span>

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="ffe0c-122">Vælge datoer i kalenderen</span><span class="sxs-lookup"><span data-stu-id="ffe0c-122">Picking dates from the calendar</span></span>

<span data-ttu-id="ffe0c-123">De felter, der viser et kalenderikon, kan angives ved hjælp af kalenderdatovælgeren.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="ffe0c-124">Aktiver kalenderikonet for at få vist kalenderdatovælgeren, eller tryk på Ctrl + Home-tastaturgenvejen i feltet.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="ffe0c-125">![Datofelter](media/ui-date-field.png "Eksempel på et datofelt")</span><span class="sxs-lookup"><span data-stu-id="ffe0c-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="ffe0c-126">Se også [Tastaturgenveje i kalenderdatovælgeren](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="ffe0c-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts)</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="ffe0c-127">Mønsteret dag\-uge\-år</span><span class="sxs-lookup"><span data-stu-id="ffe0c-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="ffe0c-128">Du kan angive en dato som en ugedag efterfulgt af et ugenummer og eventuelt et år.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="ffe0c-129">F.eks. betyder Man25 eller man25 mandag i uge 25.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-129">For example, Mon25 or mon25 means Monday in week 25.</span></span> <span data-ttu-id="ffe0c-130">Hvis du ikke angiver et år, bruges året fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="ffe0c-131">I stedet for at skrive hele ordet for den pågældende dag i ugen kan du skrive en del af ordet fra begyndelsen.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="ffe0c-132">Hvis der opstår konflikter (f.eks. med t, som kan være tirsdag eller torsdag), vurderes dagene i overensstemmelse med lande/områdeindstillingen.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-132">In case of conflicts (such as with s which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="ffe0c-133">Input vurderes først mod arbejdsdag samt dags dato, så husk dette, når du laver forkortelser.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-133">The input is first evaluated against workdate and today as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="ffe0c-134">F.eks. betyder d allerede dags dato, så det ikke kan betyde tirsdag eller torsdag.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-134">For example, t already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="ffe0c-135">Ugenummereringen er altid ISO 8601, hvor er uge 1 uge er den uge, som 4. januar indgår i, eller ugen med den første torsdag i året.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="ffe0c-136">Talmønstre</span><span class="sxs-lookup"><span data-stu-id="ffe0c-136">Digit patterns</span></span>

<span data-ttu-id="ffe0c-137">I et datofelt kan du indtaste to, fire, seks eller otte cifre:</span><span class="sxs-lookup"><span data-stu-id="ffe0c-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="ffe0c-138">Hvis du kun indtaster to tal, fortolkes dette som dagen og måneden og året indsættes ud fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="ffe0c-139">Hvis du indtaster fire tal, fortolkes dette som dagen og måneden, og året indsættes ud fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="ffe0c-140">Rækkefølgen af dagen og måneden bestemmes af dine områdeindstillinger.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="ffe0c-141">Selvom områdeindstillingerne har året før dagen og måneden, fortolkes fire tal som dagen og måneden.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="ffe0c-142">Hvis datoen falder inden for 01-01-1930 og 31-12-2029, kan du nøjes med to tal for året, ellers skal året angives med fire cifre.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="ffe0c-143">I dag</span><span class="sxs-lookup"><span data-stu-id="ffe0c-143">Today</span></span>

<span data-ttu-id="ffe0c-144">Angiv ordet for i dag på det valgte sprog i indstillingen **Sprog**. Dette indstiller datoen til dags dato.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-144">Enter the word for today, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="ffe0c-145">I stedet for at angive hele ordet kan du angive en del af det fra begyndelsen, f.eks. d eller dags , så længe det ikke også er begyndelsen på et andet ord.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as t or tod, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="ffe0c-146">Periode</span><span class="sxs-lookup"><span data-stu-id="ffe0c-146">Period</span></span>

<span data-ttu-id="ffe0c-147">For at filtrere på en bestemt regnskabsperiode skal du i et datofelt skrive bogstavet p eller ordet periode efterfulgt af et tal, der identificerer regnskabsperioden, f.eks. p2 eller periode4.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-147">To filter on a specific accounting period, in a date field enter the letter p, or the word period, followed by a number that identifies the accounting period, like p2 or period4.</span></span> <span data-ttu-id="ffe0c-148">Regnskabsperioden passer til regnskabsåret for den aktuelle arbejdsdato, der er angivet i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="ffe0c-149">Hvis arbejdsdatoen f.eks. er **21-03-20**, så filtrerer p1, eller blot p, på den første regnskabsperiode i regnskabsåret 2020 (f.eks. 01-01-20..31-01-20).</span><span class="sxs-lookup"><span data-stu-id="ffe0c-149">For example, if the work date is **03/21/20**, then p1, or just p, filters on the first accounting period of the fiscal year 2020 (such as 01/01/20..01/31/20).</span></span> <span data-ttu-id="ffe0c-150">p15 filtrerer på den 15. regnskabsperiode fra starten på regnskabsåret 2020 (f.eks. 01-03-21..31-03-21).</span><span class="sxs-lookup"><span data-stu-id="ffe0c-150">p15 filters on the fifteenth accounting period from the start of fiscal year 2020 (such as 03/01/21..03/31/21).</span></span>

<span data-ttu-id="ffe0c-151">Regnskabsperioden defineres på siden **Regnskabsperioder**.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="ffe0c-152">Hvis du vil se eller ændre regnskabsperioderne, skal du åbne siden [her](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="ffe0c-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="ffe0c-153">Aktuel arbejdsdato</span><span class="sxs-lookup"><span data-stu-id="ffe0c-153">Current work date</span></span>

<span data-ttu-id="ffe0c-154">Med arbejdsdatofunktionen kan du registrere transaktioner ved hjælp af en anden dato end dags dato.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="ffe0c-155">Ordet for 'workdate' (arbejdsdato) på det sprog, der er angivet i indstillingen **Sprog**, indstiller datoen til den aktuelt angivne arbejdsdato, der er angivet på siden [**Mine indstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med dine brugerindstillinger i Business Central").</span><span class="sxs-lookup"><span data-stu-id="ffe0c-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page.</span></span> <span data-ttu-id="ffe0c-156">I stedet for at skrive hele ordet kan du skrive en del af ordet fra begyndelsen, f.eks. 'a' eller 'arbejds'.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="ffe0c-157">Hvis du ikke har angivet en arbejdsdato, bliver dags dato brugt som arbejdsdato.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="ffe0c-158">Det er en fordel at anvende en arbejdsdato, hvis du har mange transaktioner at udføre på en dato, der ikke er dags dato.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="ffe0c-159">Se også [Ændring af grundlæggende indstillinger, f.eks. arbejdsdatoen](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="ffe0c-159">See also [Changing Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="ffe0c-160">Ultimodato</span><span class="sxs-lookup"><span data-stu-id="ffe0c-160">Closing Date</span></span>

<span data-ttu-id="ffe0c-161">Ved afslutning af et regnskabsår kan du bruge ultimodatoer til at angive, at posten er en ultimopost.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="ffe0c-162">I teknisk forstand er en ultimodato en hvilken som helst dato mellem to datoer, f.eks. 31. december og 1. januar.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="ffe0c-163">Hvis en dato skal være en ultimodato, skal du indsætte et U lige foran datoen, f.eks. U120131.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-163">To specify that a date is a closing date, put C just before the date, such as C123101.</span></span> <span data-ttu-id="ffe0c-164">Dette kan bruges sammen med alle datomønstre.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="ffe0c-165">Eksempler</span><span class="sxs-lookup"><span data-stu-id="ffe0c-165">Examples</span></span>

<span data-ttu-id="ffe0c-166">Følgende tabel indeholder eksempler på datoer i alle formater.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="ffe0c-167">Det forudsætter lande/områdeindstillinger, der formaterer datoer i henhold til: **år.måned.dag.**, en uge, der begynder om mandagen, og hvor sproget er engelsk.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="ffe0c-168">**Post**</span><span class="sxs-lookup"><span data-stu-id="ffe0c-168">**Entry**</span></span>      |<span data-ttu-id="ffe0c-169">**Fortolkning**</span><span class="sxs-lookup"><span data-stu-id="ffe0c-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="ffe0c-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-170">2018.12.31.</span></span>|<span data-ttu-id="ffe0c-171">31-12-2018.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-171">2018.12.31.</span></span>|
|<span data-ttu-id="ffe0c-172">181231</span><span class="sxs-lookup"><span data-stu-id="ffe0c-172">181231</span></span>|<span data-ttu-id="ffe0c-173">31-12-2018.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-173">2018.12.31.</span></span>|
|<span data-ttu-id="ffe0c-174">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-174">18.12.31.</span></span>|<span data-ttu-id="ffe0c-175">31-12-2018.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-175">2018.12.31.</span></span>|
|<span data-ttu-id="ffe0c-176">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-176">18.12.31.</span></span>|<span data-ttu-id="ffe0c-177">31-12-2018.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-177">2018.12.31.</span></span>|
|<span data-ttu-id="ffe0c-178">20181231</span><span class="sxs-lookup"><span data-stu-id="ffe0c-178">20181231</span></span>|<span data-ttu-id="ffe0c-179">31-12-2018.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-179">2018.12.31.</span></span>|
|<span data-ttu-id="ffe0c-180">18/12,31</span><span class="sxs-lookup"><span data-stu-id="ffe0c-180">18/12,31</span></span>|<span data-ttu-id="ffe0c-181">31-12-2018.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-181">2018.12.31.</span></span>|
|<span data-ttu-id="ffe0c-182">11</span><span class="sxs-lookup"><span data-stu-id="ffe0c-182">11</span></span>|<span data-ttu-id="ffe0c-183">arbejdsdatoår.abejdsdatomåned.11.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-183">work date year.work date month.11.</span></span>|
|<span data-ttu-id="ffe0c-184">1112</span><span class="sxs-lookup"><span data-stu-id="ffe0c-184">1112</span></span>|<span data-ttu-id="ffe0c-185">arbejdsdatoår.11.12.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-185">work date year.11.12.</span></span>|
|<span data-ttu-id="ffe0c-186">d eller dags dato</span><span class="sxs-lookup"><span data-stu-id="ffe0c-186">t or today</span></span>|<span data-ttu-id="ffe0c-187">dags dato</span><span class="sxs-lookup"><span data-stu-id="ffe0c-187">today's date</span></span>|
|<span data-ttu-id="ffe0c-188">p4</span><span class="sxs-lookup"><span data-stu-id="ffe0c-188">p4</span></span>|<span data-ttu-id="ffe0c-189">datointerval, der indeholder den fjerde regnskabsperiode, f.eks. 01-04-20..30-04-20</span><span class="sxs-lookup"><span data-stu-id="ffe0c-189">date range that includes the fourth accounting period, such as 04/01/20..04/30/20</span></span>|
|<span data-ttu-id="ffe0c-190">a eller arbejdsdato</span><span class="sxs-lookup"><span data-stu-id="ffe0c-190">w or workdate</span></span>|<span data-ttu-id="ffe0c-191">arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="ffe0c-191">the working date</span></span>|
|<span data-ttu-id="ffe0c-192">m eller mandag</span><span class="sxs-lookup"><span data-stu-id="ffe0c-192">m or Monday</span></span>|<span data-ttu-id="ffe0c-193">Mandag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="ffe0c-193">Monday of the work date week</span></span>|
|<span data-ttu-id="ffe0c-194">ti eller tirsdag</span><span class="sxs-lookup"><span data-stu-id="ffe0c-194">tu or Tuesday</span></span>|<span data-ttu-id="ffe0c-195">Tirsdag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="ffe0c-195">Tuesday of the work date week</span></span>|
|<span data-ttu-id="ffe0c-196">lø eller lørdag</span><span class="sxs-lookup"><span data-stu-id="ffe0c-196">sa or Saturday</span></span>|<span data-ttu-id="ffe0c-197">Lørdag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="ffe0c-197">Saturday of the work date week</span></span>|
|<span data-ttu-id="ffe0c-198">s eller søndag</span><span class="sxs-lookup"><span data-stu-id="ffe0c-198">s or Sunday</span></span>|<span data-ttu-id="ffe0c-199">Søndag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="ffe0c-199">Sunday of the work date week</span></span>|
|<span data-ttu-id="ffe0c-200">ti23</span><span class="sxs-lookup"><span data-stu-id="ffe0c-200">t23</span></span>|<span data-ttu-id="ffe0c-201">Tirsdag i uge 23 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="ffe0c-201">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="ffe0c-202">ti 23</span><span class="sxs-lookup"><span data-stu-id="ffe0c-202">t 23</span></span>|<span data-ttu-id="ffe0c-203">Tirsdag i uge 23 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="ffe0c-203">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="ffe0c-204">ti-1</span><span class="sxs-lookup"><span data-stu-id="ffe0c-204">t-1</span></span>|<span data-ttu-id="ffe0c-205">Tirsdag i uge 1 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="ffe0c-205">Tuesday of week 1 of the work date year</span></span>|

##  <a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="ffe0c-206">Angive intervaller</span><span class="sxs-lookup"><span data-stu-id="ffe0c-206">Setting Ranges</span></span>

<span data-ttu-id="ffe0c-207">På lister, i totaler og rapporter kan angive filtre for datoer, klokkeslæt og dato/klokkeslæt, der indeholder en startværdi og eventuelt en slutværdi for kun at få vist dataene i det pågældende interval.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-207">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="ffe0c-208">Standardreglerne gælder for den måde, du angiver datointervaller på.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-208">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="ffe0c-209">**Betydning**</span><span class="sxs-lookup"><span data-stu-id="ffe0c-209">**Meaning**</span></span>|<span data-ttu-id="ffe0c-210">**Eksempeludtryk (dato)**</span><span class="sxs-lookup"><span data-stu-id="ffe0c-210">**Sample expression (Date)**</span></span>|<span data-ttu-id="ffe0c-211">**Data, der indgår i filteret**</span><span class="sxs-lookup"><span data-stu-id="ffe0c-211">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="ffe0c-212">Interval</span><span class="sxs-lookup"><span data-stu-id="ffe0c-212">Interval</span></span>|<span data-ttu-id="ffe0c-213">15-12-00..15-01-01</span><span class="sxs-lookup"><span data-stu-id="ffe0c-213">12 15 00..01 15 01</span></span><br /><br /><span data-ttu-id="ffe0c-214">..15-12-00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-214">..12 15 00</span></span><br /><br /><span data-ttu-id="ffe0c-215">p1..p4</span><span class="sxs-lookup"><span data-stu-id="ffe0c-215">p1..p4</span></span>|<span data-ttu-id="ffe0c-216">Records med datoer fra og med 15-12-00 til og med 15-01-01.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-216">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="ffe0c-217">Records med datoen 15 12 00 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-217">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="ffe0c-218">Datointerval, der indeholder den anden, tredje og fjerde regnskabsperiode, f.eks. 01-01-20--30-04-20.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-218">Date range that includes the second, third, and fourth accounting periods, such as 01/01/20..04/30/20.</span></span>|
|<span data-ttu-id="ffe0c-219">Enten/ eller</span><span class="sxs-lookup"><span data-stu-id="ffe0c-219">Either/or</span></span>|<span data-ttu-id="ffe0c-220">15-12-00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-220">12 15 00</span></span>|<span data-ttu-id="ffe0c-221">16-12-00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-221">12 16 00</span></span>|<span data-ttu-id="ffe0c-222">Records med datoen 15 12 00 eller 16 12 00.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-222">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="ffe0c-223">Hvis der er records med datoer på begge dage, vises de alle.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-223">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="ffe0c-224">Kombination</span><span class="sxs-lookup"><span data-stu-id="ffe0c-224">Combination</span></span>|<span data-ttu-id="ffe0c-225">15-12-00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-225">12 15 00</span></span>|<span data-ttu-id="ffe0c-226">01-12-00..10-12-00  \n..14-12-00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-226">12 01 00..12 10 00  \n..12 14 00</span></span>|<span data-ttu-id="ffe0c-227">30-12-00..</span><span class="sxs-lookup"><span data-stu-id="ffe0c-227">12 30 00..</span></span>|<span data-ttu-id="ffe0c-228">Records med datoerne 15-12-00 eller poster fra og med 01-12-00 til og med 10-12-00.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-228">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <span data-ttu-id="ffe0c-229">\Records med datoer den 14-12-00 eller tidligere eller den 30-12-00 eller senere, dvs. alle records, undtagen dem med datoer mellem og inklusive 15-12-00 til og med 29-12-00.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-229">\Records with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="ffe0c-230">Du kan bruge de gyldige formater i datointervalfiltre.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-230">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="ffe0c-231">F.eks. resulterer man14 03..d 16, der anvendes på et dato og klokkeslætsfelt, i et filter fra kl. 3 mandag i uge 14 for den igangværende arbejdsdatos år, begge inklusive, indtil i dag kl. 16 inklusive.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-231">For example, mon14 3..t 4p applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="ffe0c-232">Bruge datoformler</span><span class="sxs-lookup"><span data-stu-id="ffe0c-232">Using Date Formulas</span></span>
<span data-ttu-id="ffe0c-233">En datoformel er en kort, forkortet kombination af bogstaver og tal, der angiver, hvordan datoer skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-233">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="ffe0c-234">Du kan angive datoformler i forskellige datoberegningsfelter eller filtre.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-234">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="ffe0c-235">I alle formlens datafelter indgår en dag automatisk til at dække i dag som den dag, hvor perioden starter.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-235">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="ffe0c-236">Tilsvarende, hvis du f.eks. indtaster 1U, så er perioden faktisk otte dage, fordi i dag er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-236">Accordingly, for example, if you enter 1W, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="ffe0c-237">Du skal indtaste 6D eller 1U-1D for at angive en periode på syv dage \(en rigtig uge\), der medtager periodens startdato.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-237">To specify a period of seven days \(one true week\) including the period starting date, then you must enter 6D or 1W-1D.</span></span>

<span data-ttu-id="ffe0c-238">Her følger et par eksempler på brugen af datoformler:</span><span class="sxs-lookup"><span data-stu-id="ffe0c-238">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="ffe0c-239">Datoformlen i gentagelsesintervalfeltet i en gentagelseskladde afgør, hvor tit posten på kladdelinjen skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-239">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="ffe0c-240">Datoformlen i feltet **Respitperiode** for et bestemt rykkerniveau afgør det tidsrum, der skal gå fra forfaldsdatoen \(eller fra datoen for den forrige rykker\), før der oprettes en rykker.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-240">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="ffe0c-241">Datoformlen i feltet **Forfaldsdatoformel** afgør, hvordan forfaldsdatoen på rykkeren beregnes.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-241">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="ffe0c-242">Datoformlen kan indeholde op til 20 tegn (både tal og bogstaver).</span><span class="sxs-lookup"><span data-stu-id="ffe0c-242">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="ffe0c-243">Du kan bruge følgende bogstaver som forkortelser for kalenderenheder.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-243">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="ffe0c-244">Bogstav</span><span class="sxs-lookup"><span data-stu-id="ffe0c-244">Letter</span></span>  |  <span data-ttu-id="ffe0c-245">Betyder</span><span class="sxs-lookup"><span data-stu-id="ffe0c-245">Meaning</span></span>  |
|----------|----------------------|
|<span data-ttu-id="ffe0c-246">L</span><span class="sxs-lookup"><span data-stu-id="ffe0c-246">C</span></span>|<span data-ttu-id="ffe0c-247">Løbende</span><span class="sxs-lookup"><span data-stu-id="ffe0c-247">Current</span></span>|
|<span data-ttu-id="ffe0c-248">D</span><span class="sxs-lookup"><span data-stu-id="ffe0c-248">D</span></span>|<span data-ttu-id="ffe0c-249">Dag\(e\)</span><span class="sxs-lookup"><span data-stu-id="ffe0c-249">Day\(s\)</span></span>|
|<span data-ttu-id="ffe0c-250">U</span><span class="sxs-lookup"><span data-stu-id="ffe0c-250">W</span></span>|<span data-ttu-id="ffe0c-251">Uge\(r\)</span><span class="sxs-lookup"><span data-stu-id="ffe0c-251">Week\(s\)</span></span>|
|<span data-ttu-id="ffe0c-252">M</span><span class="sxs-lookup"><span data-stu-id="ffe0c-252">M</span></span>|<span data-ttu-id="ffe0c-253">Måned\(er\)</span><span class="sxs-lookup"><span data-stu-id="ffe0c-253">Month\(s\)</span></span>|
|<span data-ttu-id="ffe0c-254">K</span><span class="sxs-lookup"><span data-stu-id="ffe0c-254">Q</span></span>|<span data-ttu-id="ffe0c-255">Kvartal\(er\)</span><span class="sxs-lookup"><span data-stu-id="ffe0c-255">Quarter\(s\)</span></span>|
|<span data-ttu-id="ffe0c-256">Å</span><span class="sxs-lookup"><span data-stu-id="ffe0c-256">Y</span></span>|<span data-ttu-id="ffe0c-257">År\(\)</span><span class="sxs-lookup"><span data-stu-id="ffe0c-257">Year\(s\)</span></span>|

<span data-ttu-id="ffe0c-258">Datoformlen kan opbygges på tre måder.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-258">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="ffe0c-259">Følgende eksempel viser, hvordan du skal bruge A for aktuel og en tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-259">The following example shows how to use C, for current, and a time unit.</span></span>

|  <span data-ttu-id="ffe0c-260">Udtryk</span><span class="sxs-lookup"><span data-stu-id="ffe0c-260">Expression</span></span>  |  <span data-ttu-id="ffe0c-261">Betyder</span><span class="sxs-lookup"><span data-stu-id="ffe0c-261">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ffe0c-262">LU</span><span class="sxs-lookup"><span data-stu-id="ffe0c-262">CW</span></span>|<span data-ttu-id="ffe0c-263">Løbende uge</span><span class="sxs-lookup"><span data-stu-id="ffe0c-263">Current week</span></span>|
|<span data-ttu-id="ffe0c-264">LM</span><span class="sxs-lookup"><span data-stu-id="ffe0c-264">CM</span></span>|<span data-ttu-id="ffe0c-265">Løbende måned</span><span class="sxs-lookup"><span data-stu-id="ffe0c-265">Current month</span></span>|

<span data-ttu-id="ffe0c-266">Følgende eksempel viser, hvordan du skal bruge et tal og en tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-266">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="ffe0c-267">Tallet må ikke være større end 9999.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-267">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="ffe0c-268">Udtryk</span><span class="sxs-lookup"><span data-stu-id="ffe0c-268">Expression</span></span>  |  <span data-ttu-id="ffe0c-269">Betyder</span><span class="sxs-lookup"><span data-stu-id="ffe0c-269">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ffe0c-270">10D</span><span class="sxs-lookup"><span data-stu-id="ffe0c-270">10D</span></span>|<span data-ttu-id="ffe0c-271">10 dage fra i dag</span><span class="sxs-lookup"><span data-stu-id="ffe0c-271">10 days from today</span></span>|
|<span data-ttu-id="ffe0c-272">2U</span><span class="sxs-lookup"><span data-stu-id="ffe0c-272">2W</span></span>|<span data-ttu-id="ffe0c-273">2 uger fra i dag</span><span class="sxs-lookup"><span data-stu-id="ffe0c-273">2 weeks from today</span></span>|

<span data-ttu-id="ffe0c-274">Følgende eksempel viser, hvordan du skal bruge en tidsenhed og et tal.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-274">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="ffe0c-275">Udtryk</span><span class="sxs-lookup"><span data-stu-id="ffe0c-275">Expression</span></span>  |  <span data-ttu-id="ffe0c-276">Betyder</span><span class="sxs-lookup"><span data-stu-id="ffe0c-276">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ffe0c-277">D10</span><span class="sxs-lookup"><span data-stu-id="ffe0c-277">D10</span></span>|<span data-ttu-id="ffe0c-278">Den næste 10. dage i en måned</span><span class="sxs-lookup"><span data-stu-id="ffe0c-278">The next 10th day of a month</span></span>|
|<span data-ttu-id="ffe0c-279">UD4</span><span class="sxs-lookup"><span data-stu-id="ffe0c-279">WD4</span></span>|<span data-ttu-id="ffe0c-280">Den næste 4. dag i en uge \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="ffe0c-280">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="ffe0c-281">Følgende eksempel viser, hvordan du kan kombinere de tre formler efter behov.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-281">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="ffe0c-282">Udtryk</span><span class="sxs-lookup"><span data-stu-id="ffe0c-282">Expression</span></span>  |  <span data-ttu-id="ffe0c-283">Betyder</span><span class="sxs-lookup"><span data-stu-id="ffe0c-283">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ffe0c-284">LM+10D</span><span class="sxs-lookup"><span data-stu-id="ffe0c-284">CM+10D</span></span>|<span data-ttu-id="ffe0c-285">Løbende måned \+ 10 dage</span><span class="sxs-lookup"><span data-stu-id="ffe0c-285">Current month \+ 10 days</span></span>|

<span data-ttu-id="ffe0c-286">Følgende eksempel viser, hvordan du kan bruge et minustegn til at angive en dato i fortiden.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-286">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="ffe0c-287">Udtryk</span><span class="sxs-lookup"><span data-stu-id="ffe0c-287">Expression</span></span>  |  <span data-ttu-id="ffe0c-288">Betyder</span><span class="sxs-lookup"><span data-stu-id="ffe0c-288">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ffe0c-289">-1Å</span><span class="sxs-lookup"><span data-stu-id="ffe0c-289">-1Y</span></span>|<span data-ttu-id="ffe0c-290">1 år siden fra i dag</span><span class="sxs-lookup"><span data-stu-id="ffe0c-290">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="ffe0c-291">Hvis lokationen bruger en basiskalender, fortolkes den datoformel, du f.eks. indtaster i feltet **Transporttid**, i overensstemmelse med kalenderens arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-291">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="ffe0c-292">For eksempel betyder 1U syv arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-292">For example, 1W  means seven working days.</span></span>
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

## <a name="entering-times"></a><span data-ttu-id="ffe0c-293">Angive klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="ffe0c-293">Entering Times</span></span>
<span data-ttu-id="ffe0c-294">Når du angiver klokkeslæt, kan du indsætte separatorer uden mellemrum, som du vil have mellem enhederne, men hvis du bruger to cifre for hver enhed op til millisekunder, er det ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-294">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="ffe0c-295">Du behøver kun at skrive de største enheder, du vil behøver, de øvrige indstilles til nul.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-295">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="ffe0c-296">Du kan også udelade AM/PM-symboler.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-296">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="ffe0c-297">I den følgende tabel kan du se, hvordan du kan indtaste klokkeslæt, og hvordan de fortolkes.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-297">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="ffe0c-298">Det forudsætter lande/områdeindstillinger, der formaterer tidspunkter i overensstemmelse med: **Timer:Minutter:Sekunder.Millisekunder.**</span><span class="sxs-lookup"><span data-stu-id="ffe0c-298">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="ffe0c-299">og bruger AM og PM-symbolerne 'AM' og 'PM hhv.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-299">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="ffe0c-300">**Post**</span><span class="sxs-lookup"><span data-stu-id="ffe0c-300">**Entry**</span></span>      |<span data-ttu-id="ffe0c-301">**Fortolkning**</span><span class="sxs-lookup"><span data-stu-id="ffe0c-301">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="ffe0c-302">05:23:17</span><span class="sxs-lookup"><span data-stu-id="ffe0c-302">05:23:17</span></span>|<span data-ttu-id="ffe0c-303">05:23:17</span><span class="sxs-lookup"><span data-stu-id="ffe0c-303">05:23:17</span></span>|
|<span data-ttu-id="ffe0c-304">5</span><span class="sxs-lookup"><span data-stu-id="ffe0c-304">5</span></span>|<span data-ttu-id="ffe0c-305">05:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-305">05:00:00</span></span>|
|<span data-ttu-id="ffe0c-306">5AM</span><span class="sxs-lookup"><span data-stu-id="ffe0c-306">5AM</span></span>|<span data-ttu-id="ffe0c-307">05:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-307">05:00:00</span></span>|
|<span data-ttu-id="ffe0c-308">5P</span><span class="sxs-lookup"><span data-stu-id="ffe0c-308">5P</span></span>|<span data-ttu-id="ffe0c-309">17:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-309">17:00:00</span></span>|
|<span data-ttu-id="ffe0c-310">12</span><span class="sxs-lookup"><span data-stu-id="ffe0c-310">12</span></span>|<span data-ttu-id="ffe0c-311">12:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-311">12:00:00</span></span>|
|<span data-ttu-id="ffe0c-312">12A</span><span class="sxs-lookup"><span data-stu-id="ffe0c-312">12A</span></span>|<span data-ttu-id="ffe0c-313">00:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-313">00:00:00</span></span>|
|<span data-ttu-id="ffe0c-314">12P</span><span class="sxs-lookup"><span data-stu-id="ffe0c-314">12P</span></span>|<span data-ttu-id="ffe0c-315">12:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-315">12:00:00</span></span>|
|<span data-ttu-id="ffe0c-316">17</span><span class="sxs-lookup"><span data-stu-id="ffe0c-316">17</span></span>|<span data-ttu-id="ffe0c-317">17:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-317">17:00:00</span></span>|
|<span data-ttu-id="ffe0c-318">5:30</span><span class="sxs-lookup"><span data-stu-id="ffe0c-318">5:30</span></span>|<span data-ttu-id="ffe0c-319">05:30:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-319">05:30:00</span></span>|
|<span data-ttu-id="ffe0c-320">0530</span><span class="sxs-lookup"><span data-stu-id="ffe0c-320">0530</span></span>|<span data-ttu-id="ffe0c-321">05:30:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-321">05:30:00</span></span>|
|<span data-ttu-id="ffe0c-322">5:30:5</span><span class="sxs-lookup"><span data-stu-id="ffe0c-322">5:30:5</span></span>|<span data-ttu-id="ffe0c-323">05:30:05</span><span class="sxs-lookup"><span data-stu-id="ffe0c-323">05:30:05</span></span>|
|<span data-ttu-id="ffe0c-324">053005</span><span class="sxs-lookup"><span data-stu-id="ffe0c-324">053005</span></span>|<span data-ttu-id="ffe0c-325">05:30:05</span><span class="sxs-lookup"><span data-stu-id="ffe0c-325">05:30:05</span></span>|
|<span data-ttu-id="ffe0c-326">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="ffe0c-326">5:30:5,50</span></span>|<span data-ttu-id="ffe0c-327">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="ffe0c-327">05:30:05.5</span></span>|
|<span data-ttu-id="ffe0c-328">053005050</span><span class="sxs-lookup"><span data-stu-id="ffe0c-328">053005050</span></span>|<span data-ttu-id="ffe0c-329">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="ffe0c-329">05:30:05.05</span></span>|

<span data-ttu-id="ffe0c-330">Du skal være opmærksom på, at millisekunder fortolkes som decimalformat.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-330">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="ffe0c-331">Altså betyder f.eks. 3, 30 og 300 alle 300 millisekunder, mens 03 betyder 30 og 003 betyder 3 millisekunder.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-331">So, for example, 3, 30, and 300 all mean 300 milliseconds, while 03 means 30 and 003 means 3 milliseconds.</span></span>

<span data-ttu-id="ffe0c-332">Du kan ikke bruge 24:00 til at angive midnat eller bruge værdier større end 24:00.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-332">You cannot use 24:00 to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="ffe0c-333">Ordet for 'time" på det sprog, som [!INCLUDE[d365fin](includes/d365fin_long_md.md)] bruger, vurderes til det aktuelle tidspunkt på din computer eller en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-333">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="ffe0c-334">Du kan angive en del af ordet fra begyndelsen, f.eks. t eller TIM.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-334">You can enter any part of the word, starting from the beginning, such as t or TIM.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="ffe0c-335">Indtaste kombinerede datoer og tidspunkter</span><span class="sxs-lookup"><span data-stu-id="ffe0c-335">Entering combined Dates and Times</span></span>
<span data-ttu-id="ffe0c-336">Når du angiver dato/klokkeslæt, som en dato og klokkeslæt kombineret i ét felt, skal du angive et mellemrum mellem datoen og klokkeslættet.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-336">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="ffe0c-337">Datodelen kan kun indeholde mellemrum i form af officielle datoseparatorer af lande/områdeindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-337">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="ffe0c-338">Tid, der kan indeholde mellemrum omkring AM/PM-symbolet.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-338">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="ffe0c-339">Det er også muligt kun at angive en dato i et dato/klokkeslætsfelt, men det er ikke muligt kun at angive én gang.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-339">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="ffe0c-340">Følgende tabel viser eksempler på dato/klokkeslætskombinationer.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-340">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="ffe0c-341">Lande/områdeindstillinger i eksemplerne viser datoer på dag\-måned\-år-format ved hjælp af AM/PM-symboler, engelsk sprog og søndag som første ugedag.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-341">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="ffe0c-342">**Post**</span><span class="sxs-lookup"><span data-stu-id="ffe0c-342">**Entry**</span></span>      |<span data-ttu-id="ffe0c-343">**Fortolkning**</span><span class="sxs-lookup"><span data-stu-id="ffe0c-343">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="ffe0c-344">08-01-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="ffe0c-344">08-01-2016 05:48:12 PM</span></span>|<span data-ttu-id="ffe0c-345">08\-01\-2016 17:48:12</span><span class="sxs-lookup"><span data-stu-id="ffe0c-345">08\-01\-2016 05:48:12 PM</span></span>|
|<span data-ttu-id="ffe0c-346">131202 132455</span><span class="sxs-lookup"><span data-stu-id="ffe0c-346">131202 132455</span></span>|<span data-ttu-id="ffe0c-347">13\-12\-2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="ffe0c-347">13\-12\-2002 13:24:55</span></span>|
|<span data-ttu-id="ffe0c-348">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="ffe0c-348">1-12-02 10</span></span>|<span data-ttu-id="ffe0c-349">01\-12\-2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-349">01\-12\-2002 10:00:00</span></span>|
|<span data-ttu-id="ffe0c-350">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="ffe0c-350">1.12.02 5</span></span>|<span data-ttu-id="ffe0c-351">01\-12\-2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-351">01\-12\-2002 05:00:00</span></span>|
|<span data-ttu-id="ffe0c-352">1.12.02</span><span class="sxs-lookup"><span data-stu-id="ffe0c-352">1.12.02</span></span>|<span data-ttu-id="ffe0c-353">01\-12\-2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-353">01\-12\-2002 00:00:00</span></span>|
|<span data-ttu-id="ffe0c-354">11 12</span><span class="sxs-lookup"><span data-stu-id="ffe0c-354">11 12</span></span>|<span data-ttu-id="ffe0c-355">11\-arbejdsdatomåned\-abejdsdatoår 12:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-355">11\-work date month\-work date year 12:00:00</span></span>|
|<span data-ttu-id="ffe0c-356">1112 12</span><span class="sxs-lookup"><span data-stu-id="ffe0c-356">1112 12</span></span>|<span data-ttu-id="ffe0c-357">11\-12\-arbejdsdatoår 12:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-357">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="ffe0c-358">d eller dags dato</span><span class="sxs-lookup"><span data-stu-id="ffe0c-358">t or today</span></span>|<span data-ttu-id="ffe0c-359">dags dato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-359">today's date 00:00:00</span></span>|
|<span data-ttu-id="ffe0c-360">d 10:30</span><span class="sxs-lookup"><span data-stu-id="ffe0c-360">t 10:30</span></span>|<span data-ttu-id="ffe0c-361">dags dato 10:30:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-361">today's date 10:30:00</span></span>|
|<span data-ttu-id="ffe0c-362">d 3:3:3</span><span class="sxs-lookup"><span data-stu-id="ffe0c-362">t 3:3:3</span></span>|<span data-ttu-id="ffe0c-363">dags dato 03:03:03</span><span class="sxs-lookup"><span data-stu-id="ffe0c-363">today's date 03:03:03</span></span>|
|<span data-ttu-id="ffe0c-364">a eller arbejdsdato</span><span class="sxs-lookup"><span data-stu-id="ffe0c-364">w or workdate</span></span>|<span data-ttu-id="ffe0c-365">arbejdsdato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-365">the working date 00:00:00</span></span>|
|<span data-ttu-id="ffe0c-366">m eller mandag</span><span class="sxs-lookup"><span data-stu-id="ffe0c-366">m or Monday</span></span>|<span data-ttu-id="ffe0c-367">Mandag i ugen for arbejdsdatoen 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-367">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="ffe0c-368">ti eller tirsdag</span><span class="sxs-lookup"><span data-stu-id="ffe0c-368">tu or Tuesday</span></span>|<span data-ttu-id="ffe0c-369">Tirsdag i ugen for arbejdsdatoen 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-369">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="ffe0c-370">lø eller lørdag</span><span class="sxs-lookup"><span data-stu-id="ffe0c-370">sa or Saturday</span></span>|<span data-ttu-id="ffe0c-371">Lørdag i ugen for arbejdsdatoen 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-371">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="ffe0c-372">s eller søndag</span><span class="sxs-lookup"><span data-stu-id="ffe0c-372">s or Sunday</span></span>|<span data-ttu-id="ffe0c-373">Søndag i ugen for arbejdsdatoen 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-373">Sunday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="ffe0c-374">ti 10:30</span><span class="sxs-lookup"><span data-stu-id="ffe0c-374">tu 10:30</span></span>|<span data-ttu-id="ffe0c-375">Tirsdag i ugen for arbejdsdatoen 10:30:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-375">Tuesday of the work date week 10:30:00</span></span>|
|<span data-ttu-id="ffe0c-376">ti 3:3:3</span><span class="sxs-lookup"><span data-stu-id="ffe0c-376">tu 3:3:3</span></span>|<span data-ttu-id="ffe0c-377">Tirsdag i ugen for arbejdsdatoen 03:03:03</span><span class="sxs-lookup"><span data-stu-id="ffe0c-377">Tuesday of the work date week 03:03:03</span></span>|
|<span data-ttu-id="ffe0c-378">ti23 t</span><span class="sxs-lookup"><span data-stu-id="ffe0c-378">t23 t</span></span>|<span data-ttu-id="ffe0c-379">Tirsdag i uge 23 i året for arbejdsdatoen, det aktuelle tidspunkt på dagen</span><span class="sxs-lookup"><span data-stu-id="ffe0c-379">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="ffe0c-380">ti23</span><span class="sxs-lookup"><span data-stu-id="ffe0c-380">t23</span></span>|<span data-ttu-id="ffe0c-381">Tirsdag i uge 23 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="ffe0c-381">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="ffe0c-382">ti 23</span><span class="sxs-lookup"><span data-stu-id="ffe0c-382">t 23</span></span>|<span data-ttu-id="ffe0c-383">Dags dato 23:00:00</span><span class="sxs-lookup"><span data-stu-id="ffe0c-383">Today 23:00:00</span></span>|
|<span data-ttu-id="ffe0c-384">ti-1</span><span class="sxs-lookup"><span data-stu-id="ffe0c-384">t-1</span></span>|<span data-ttu-id="ffe0c-385">Tirsdag i uge 1 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="ffe0c-385">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="ffe0c-386">Angivelse af varighed</span><span class="sxs-lookup"><span data-stu-id="ffe0c-386">Entering Duration</span></span>
<span data-ttu-id="ffe0c-387">Nogle felter i programmet repræsenterer en varighed eller et forløbet tidsrum i stedet for en bestemt dato eller klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-387">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="ffe0c-388">Du angiver varighed ved at skrive et tal efterfulgt af en måleenhed.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-388">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="ffe0c-389">Her er nogle eksempler.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-389">Here are some examples.</span></span>

|<span data-ttu-id="ffe0c-390">**Varighed**</span><span class="sxs-lookup"><span data-stu-id="ffe0c-390">**Duration**</span></span>|<span data-ttu-id="ffe0c-391">**Enhed**</span><span class="sxs-lookup"><span data-stu-id="ffe0c-391">**Unit of measure**</span></span>|
|------------|-------------------|
|<span data-ttu-id="ffe0c-392">2t</span><span class="sxs-lookup"><span data-stu-id="ffe0c-392">2h</span></span>|<span data-ttu-id="ffe0c-393">2 timer</span><span class="sxs-lookup"><span data-stu-id="ffe0c-393">2 hrs</span></span>|
|<span data-ttu-id="ffe0c-394">6t 30 m</span><span class="sxs-lookup"><span data-stu-id="ffe0c-394">6h 30 m</span></span>|<span data-ttu-id="ffe0c-395">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="ffe0c-395">6 hrs 30 mins</span></span>|
|<span data-ttu-id="ffe0c-396">6,5t</span><span class="sxs-lookup"><span data-stu-id="ffe0c-396">6.5h</span></span>|<span data-ttu-id="ffe0c-397">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="ffe0c-397">6 hrs 30 mins</span></span>|
|<span data-ttu-id="ffe0c-398">90m</span><span class="sxs-lookup"><span data-stu-id="ffe0c-398">90m</span></span>|<span data-ttu-id="ffe0c-399">1 time 30 min</span><span class="sxs-lookup"><span data-stu-id="ffe0c-399">1 hr 30 mins</span></span>|
|<span data-ttu-id="ffe0c-400">2d 6t 30m</span><span class="sxs-lookup"><span data-stu-id="ffe0c-400">2d 6h 30m</span></span>|<span data-ttu-id="ffe0c-401">2 dage 6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="ffe0c-401">2 days 6 hrs 30 mins</span></span>|
|<span data-ttu-id="ffe0c-402">2d 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="ffe0c-402">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="ffe0c-403">2 dage 6 timer 30 min 56 sek 600 msek</span><span class="sxs-lookup"><span data-stu-id="ffe0c-403">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="ffe0c-404">Du kan også skrive et tal, der automatisk konverteres til en varighed.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-404">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="ffe0c-405">Det tal, du skriver, konverteres i overensstemmelse med den standardmåleenhed, der er angivet i feltet Varighed.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-405">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="ffe0c-406">Du kan se, hvilken måleenhed, der anvendes i feltet Varighed, ved at skrive et tal og se, hvilken måleenhed tallet konverteres til.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-406">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="ffe0c-407">Hvis måleenheden f.eks. er timer, konverteres tallet 5 til 5 timer.</span><span class="sxs-lookup"><span data-stu-id="ffe0c-407">For example, if the unit of measure is hours, the number 5 is converted to 5 hrs.</span></span>

## <a name="see-also"></a><span data-ttu-id="ffe0c-408">Se også</span><span class="sxs-lookup"><span data-stu-id="ffe0c-408">See Also</span></span>
<span data-ttu-id="ffe0c-409">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ffe0c-409">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ffe0c-410">Beregning af forfaldsdato for køb</span><span class="sxs-lookup"><span data-stu-id="ffe0c-410">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="ffe0c-411">Indtaste kriterier i filtre</span><span class="sxs-lookup"><span data-stu-id="ffe0c-411">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
