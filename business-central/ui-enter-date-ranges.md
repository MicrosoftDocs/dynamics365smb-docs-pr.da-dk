---
title: Angive datoer og klokkeslæt i Business Central | Microsoft Docs
description: Få at vide, hvordan du angiver datoer og tidspunkter med forskellige produktivitetstip som oversigter, udtryk og områder. Filtrer lister eller rapporter ned til en bestemt dato eller tidsperioder.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 404c39cba663cebc4d9ab30126de97bd20cf7e8e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773526"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="bc484-104">Arbejde med kalenderdatoer og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="bc484-104">Working with Calendar Dates and Times</span></span>

<span data-ttu-id="bc484-105">I [!INCLUDE[prod_short](includes/prod_long.md)] er der flere måder til at angive datoer og klokkeslæt, herunder effektive funktioner, der fremskynder indtastning af data og hjælper dig med at skrive komplekse kalenderudtryk.</span><span class="sxs-lookup"><span data-stu-id="bc484-105">[!INCLUDE[prod_short](includes/prod_long.md)] offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="bc484-106">Der er forskellige steder i programmet, hvor du kan angive datoer og klokkeslæt i felterne.</span><span class="sxs-lookup"><span data-stu-id="bc484-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="bc484-107">På en salgsordre kan du f.eks. angive afsendelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="bc484-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="bc484-108">Når du filtrerer lister eller rapportdata, kan du angive datoer og klokkeslæt for kun at finde de data, du er interesseret i.</span><span class="sxs-lookup"><span data-stu-id="bc484-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="bc484-109">Kontrollere internationale og sproglige indstillinger</span><span class="sxs-lookup"><span data-stu-id="bc484-109">Check your region and language settings</span></span>
<span data-ttu-id="bc484-110">Siden **Mine indstillinger** angiver det **Område** og **Sprog**, du bruger i programmet.</span><span class="sxs-lookup"><span data-stu-id="bc484-110">The **My Settings** page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="bc484-111">Disse indstillinger påvirker måden, du angiver datoer og klokkeslæt på.</span><span class="sxs-lookup"><span data-stu-id="bc484-111">These settings influence how you enter dates and times.</span></span>

-   <span data-ttu-id="bc484-112">Indstillingen **Område** bestemmer, hvordan datoer, klokkeslæt, tal og valutaer vises og formateres.</span><span class="sxs-lookup"><span data-stu-id="bc484-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="bc484-113">Når datomønstre omfatter ord, skal sproget for de ord, du bruger, svare til indstillingen **Sprog**.</span><span class="sxs-lookup"><span data-stu-id="bc484-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] <span data-ttu-id="bc484-114">anvender den gregorianske kalender.</span><span class="sxs-lookup"><span data-stu-id="bc484-114">uses the Gregorian calendar system.</span></span>

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="bc484-115">Angive datoer</span><span class="sxs-lookup"><span data-stu-id="bc484-115">Entering Dates</span></span>

<span data-ttu-id="bc484-116">I et datofelt kan du angive en dato i standardformatet for din land/områdeindstilling.</span><span class="sxs-lookup"><span data-stu-id="bc484-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="bc484-117">Forskellige områder kan bruge forskellige separatorer mellem dage, måneder og år.</span><span class="sxs-lookup"><span data-stu-id="bc484-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="bc484-118">For eksempel bruger nogle lande/områder bindestreger (mm-dd-åååå), mens andre bruger skråstreger (mm/dd/åååå).</span><span class="sxs-lookup"><span data-stu-id="bc484-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="bc484-119">Du kan dog bruge alle separatorer, selv mellemrum, og datoen ændres automatisk til brug af de separatorer, der gælder for dit land/område.</span><span class="sxs-lookup"><span data-stu-id="bc484-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="bc484-120">Bemærk, at det format, som datoer vises i på udskrevne rapporter eller dokumenter sendt med e-mails, ikke påvirkes af dit personlige valg af land/område.</span><span class="sxs-lookup"><span data-stu-id="bc484-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="bc484-121">For at arbejde mere produktivt med datoer og klokkeslæt kan du bruge de metoder og formater, der er beskrevet i følgende afsnit.</span><span class="sxs-lookup"><span data-stu-id="bc484-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span>

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="bc484-122">Vælge datoer i kalenderen</span><span class="sxs-lookup"><span data-stu-id="bc484-122">Picking dates from the calendar</span></span>

<span data-ttu-id="bc484-123">De felter, der viser et kalenderikon, kan angives ved hjælp af kalenderdatovælgeren.</span><span class="sxs-lookup"><span data-stu-id="bc484-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="bc484-124">Aktiver kalenderikonet for at få vist kalenderdatovælgeren, eller tryk på Ctrl + Home-tastaturgenvejen i feltet.</span><span class="sxs-lookup"><span data-stu-id="bc484-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="bc484-125">![Datofelter1](media/ui-date-field.png "Eksempel på et datofelt")</span><span class="sxs-lookup"><span data-stu-id="bc484-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="bc484-126">Se også [Tastaturgenveje i kalenderdatovælgeren](keyboard-shortcuts.md#calendarshortcuts).</span><span class="sxs-lookup"><span data-stu-id="bc484-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts).</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="bc484-127">Mønsteret dag\-uge\-år</span><span class="sxs-lookup"><span data-stu-id="bc484-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="bc484-128">Du kan angive en dato som en ugedag efterfulgt af et ugenummer og eventuelt et år.</span><span class="sxs-lookup"><span data-stu-id="bc484-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="bc484-129">F.eks. betyder Man25 eller man25 mandag i uge 25.</span><span class="sxs-lookup"><span data-stu-id="bc484-129">For example, Mon25 or mon25 means Monday in week 25.</span></span> <span data-ttu-id="bc484-130">Hvis du ikke angiver et år, bruges året fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="bc484-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="bc484-131">I stedet for at skrive hele ordet for den pågældende dag i ugen kan du skrive en del af ordet fra begyndelsen.</span><span class="sxs-lookup"><span data-stu-id="bc484-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="bc484-132">Hvis der opstår konflikter (f.eks. med t, som kan være tirsdag eller torsdag), vurderes dagene i overensstemmelse med indstillingen for land/område.</span><span class="sxs-lookup"><span data-stu-id="bc484-132">In case of conflicts (such as with s which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="bc484-133">Input vurderes først mod arbejdsdag samt dags dato, så husk dette, når du laver forkortelser.</span><span class="sxs-lookup"><span data-stu-id="bc484-133">The input is first evaluated against workdate and today as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="bc484-134">F.eks. betyder d allerede dags dato, så det ikke kan betyde tirsdag eller torsdag.</span><span class="sxs-lookup"><span data-stu-id="bc484-134">For example, t already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="bc484-135">Ugenummereringen er altid ISO 8601, hvor er uge 1 uge er den uge, som 4. januar indgår i, eller ugen med den første torsdag i året.</span><span class="sxs-lookup"><span data-stu-id="bc484-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="bc484-136">Talmønstre</span><span class="sxs-lookup"><span data-stu-id="bc484-136">Digit patterns</span></span>

<span data-ttu-id="bc484-137">I et datofelt kan du indtaste to, fire, seks eller otte cifre:</span><span class="sxs-lookup"><span data-stu-id="bc484-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="bc484-138">Hvis du kun indtaster to tal, fortolkes dette som dagen og måneden og året indsættes ud fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="bc484-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="bc484-139">Hvis du indtaster fire tal, fortolkes dette som dagen og måneden, og året indsættes ud fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="bc484-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="bc484-140">Rækkefølgen af dagen og måneden bestemmes af dine områdeindstillinger.</span><span class="sxs-lookup"><span data-stu-id="bc484-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="bc484-141">Selvom områdeindstillingerne har året før dagen og måneden, fortolkes fire tal som dagen og måneden.</span><span class="sxs-lookup"><span data-stu-id="bc484-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="bc484-142">Hvis datoen falder inden for 01-01-1930 og 31-12-2029, kan du nøjes med to tal for året, ellers skal året angives med fire cifre.</span><span class="sxs-lookup"><span data-stu-id="bc484-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="bc484-143">I dag</span><span class="sxs-lookup"><span data-stu-id="bc484-143">Today</span></span>

<span data-ttu-id="bc484-144">Angiv ordet for i dag på det valgte sprog i indstillingen **Sprog**. Dette indstiller datoen til dags dato.</span><span class="sxs-lookup"><span data-stu-id="bc484-144">Enter the word for today, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="bc484-145">I stedet for at angive hele ordet kan du angive en del af det fra begyndelsen, f.eks. d eller dags , så længe det ikke også er begyndelsen på et andet ord.</span><span class="sxs-lookup"><span data-stu-id="bc484-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as t or tod, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="bc484-146">Periode</span><span class="sxs-lookup"><span data-stu-id="bc484-146">Period</span></span>

<span data-ttu-id="bc484-147">For at filtrere på en bestemt regnskabsperiode skal du i et datofelt skrive bogstavet p eller ordet periode efterfulgt af et tal, der identificerer regnskabsperioden, f.eks. p2 eller periode4.</span><span class="sxs-lookup"><span data-stu-id="bc484-147">To filter on a specific accounting period, in a date field enter the letter p, or the word period, followed by a number that identifies the accounting period, like p2 or period4.</span></span> <span data-ttu-id="bc484-148">Regnskabsperioden passer til regnskabsåret for den aktuelle arbejdsdato, der er angivet i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="bc484-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="bc484-149">Hvis arbejdsdatoen f.eks. er **21-03-22**, så filtrerer p1, eller blot p, på den første regnskabsperiode i regnskabsåret 2022 (f.eks. 01-01-22..31-01-22).</span><span class="sxs-lookup"><span data-stu-id="bc484-149">For example, if the work date is **03/21/22**, then p1, or just p, filters on the first accounting period of the fiscal year 2022 (such as 01/01/22..01/31/22).</span></span> <span data-ttu-id="bc484-150">p15 filtrerer på den 15. regnskabsperiode fra starten af regnskabsåret 2022 (f.eks. 01-03-23 til 31-03-23).</span><span class="sxs-lookup"><span data-stu-id="bc484-150">p15 filters on the fifteenth accounting period from the start of fiscal year 2022 (such as 03/01/23..03/31/23).</span></span>

<span data-ttu-id="bc484-151">Regnskabsperioden defineres på siden **Regnskabsperioder**.</span><span class="sxs-lookup"><span data-stu-id="bc484-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="bc484-152">Hvis du vil se eller ændre regnskabsperioderne, skal du åbne siden [her](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="bc484-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="bc484-153">Aktuel arbejdsdato</span><span class="sxs-lookup"><span data-stu-id="bc484-153">Current work date</span></span>

<span data-ttu-id="bc484-154">Med arbejdsdatofunktionen kan du registrere transaktioner ved hjælp af en anden dato end dags dato.</span><span class="sxs-lookup"><span data-stu-id="bc484-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="bc484-155">Ordet for 'workdate' (arbejdsdato) på det sprog, der er angivet i indstillingen **Sprog**, indstiller datoen til den aktuelt angivne arbejdsdato, der er angivet på siden **Mine indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="bc484-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the **My Settings** page.</span></span> <span data-ttu-id="bc484-156">I stedet for at skrive hele ordet kan du skrive en del af ordet fra begyndelsen, f.eks. 'a' eller 'arbejds'.</span><span class="sxs-lookup"><span data-stu-id="bc484-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="bc484-157">Hvis du ikke har angivet en arbejdsdato, bliver dags dato brugt som arbejdsdato.</span><span class="sxs-lookup"><span data-stu-id="bc484-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="bc484-158">Det er en fordel at anvende en arbejdsdato, hvis du har mange transaktioner at udføre på en dato, der ikke er dags dato.</span><span class="sxs-lookup"><span data-stu-id="bc484-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="bc484-159">Se også [Ændre grundlæggende indstillinger, f.eks. arbejdsdatoen](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="bc484-159">See also [Change Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="bc484-160">Ultimodato</span><span class="sxs-lookup"><span data-stu-id="bc484-160">Closing Date</span></span>

<span data-ttu-id="bc484-161">Ved afslutning af et regnskabsår kan du bruge ultimodatoer til at angive, at posten er en ultimopost.</span><span class="sxs-lookup"><span data-stu-id="bc484-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="bc484-162">I teknisk forstand er en ultimodato en hvilken som helst dato mellem to datoer, f.eks. 31. december og 1. januar.</span><span class="sxs-lookup"><span data-stu-id="bc484-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="bc484-163">Hvis en dato skal være en ultimodato, skal du indsætte et U lige foran datoen, f.eks. U120131.</span><span class="sxs-lookup"><span data-stu-id="bc484-163">To specify that a date is a closing date, put C just before the date, such as C123101.</span></span> <span data-ttu-id="bc484-164">Dette kan bruges sammen med alle datomønstre.</span><span class="sxs-lookup"><span data-stu-id="bc484-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="bc484-165">Eksempler</span><span class="sxs-lookup"><span data-stu-id="bc484-165">Examples</span></span>

<span data-ttu-id="bc484-166">Følgende tabel indeholder eksempler på datoer i alle formater.</span><span class="sxs-lookup"><span data-stu-id="bc484-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="bc484-167">Det forudsætter indstillinger for land/område, der formaterer datoer i henhold til: **år.måned.dag.**, en uge, der begynder om mandagen, og hvor sproget er engelsk.</span><span class="sxs-lookup"><span data-stu-id="bc484-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="bc484-168">**Post**</span><span class="sxs-lookup"><span data-stu-id="bc484-168">**Entry**</span></span>      |<span data-ttu-id="bc484-169">**Fortolkning**</span><span class="sxs-lookup"><span data-stu-id="bc484-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="bc484-170">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="bc484-170">2022.12.31.</span></span>|<span data-ttu-id="bc484-171">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="bc484-171">2022.12.31.</span></span>|
|<span data-ttu-id="bc484-172">221231</span><span class="sxs-lookup"><span data-stu-id="bc484-172">221231</span></span>|<span data-ttu-id="bc484-173">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="bc484-173">2022.12.31.</span></span>|
|<span data-ttu-id="bc484-174">22.12.31.</span><span class="sxs-lookup"><span data-stu-id="bc484-174">22.12.31.</span></span>|<span data-ttu-id="bc484-175">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="bc484-175">2022.12.31.</span></span>|
|<span data-ttu-id="bc484-176">22.12.31.</span><span class="sxs-lookup"><span data-stu-id="bc484-176">22.12.31.</span></span>|<span data-ttu-id="bc484-177">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="bc484-177">2022.12.31.</span></span>|
|<span data-ttu-id="bc484-178">20221231</span><span class="sxs-lookup"><span data-stu-id="bc484-178">20221231</span></span>|<span data-ttu-id="bc484-179">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="bc484-179">2022.12.31.</span></span>|
|<span data-ttu-id="bc484-180">22/12,31</span><span class="sxs-lookup"><span data-stu-id="bc484-180">22/12,31</span></span>|<span data-ttu-id="bc484-181">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="bc484-181">2022.12.31.</span></span>|
|<span data-ttu-id="bc484-182">11</span><span class="sxs-lookup"><span data-stu-id="bc484-182">11</span></span>|<span data-ttu-id="bc484-183">arbejdsdatoår.abejdsdatomåned.11.</span><span class="sxs-lookup"><span data-stu-id="bc484-183">work date year.work date month.11.</span></span>|
|<span data-ttu-id="bc484-184">1112</span><span class="sxs-lookup"><span data-stu-id="bc484-184">1112</span></span>|<span data-ttu-id="bc484-185">arbejdsdatoår.11.12.</span><span class="sxs-lookup"><span data-stu-id="bc484-185">work date year.11.12.</span></span>|
|<span data-ttu-id="bc484-186">d eller dags dato</span><span class="sxs-lookup"><span data-stu-id="bc484-186">t or today</span></span>|<span data-ttu-id="bc484-187">dags dato</span><span class="sxs-lookup"><span data-stu-id="bc484-187">today's date</span></span>|
|<span data-ttu-id="bc484-188">p4</span><span class="sxs-lookup"><span data-stu-id="bc484-188">p4</span></span>|<span data-ttu-id="bc484-189">datointerval, der indeholder den fjerde regnskabsperiode, f.eks. 01-04-20..30-04-20</span><span class="sxs-lookup"><span data-stu-id="bc484-189">date range that includes the fourth accounting period, such as 04/01/20..04/30/20</span></span>|
|<span data-ttu-id="bc484-190">a eller arbejdsdato</span><span class="sxs-lookup"><span data-stu-id="bc484-190">w or workdate</span></span>|<span data-ttu-id="bc484-191">arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="bc484-191">the working date</span></span>|
|<span data-ttu-id="bc484-192">m eller mandag</span><span class="sxs-lookup"><span data-stu-id="bc484-192">m or Monday</span></span>|<span data-ttu-id="bc484-193">Mandag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="bc484-193">Monday of the work date week</span></span>|
|<span data-ttu-id="bc484-194">ti eller tirsdag</span><span class="sxs-lookup"><span data-stu-id="bc484-194">tu or Tuesday</span></span>|<span data-ttu-id="bc484-195">Tirsdag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="bc484-195">Tuesday of the work date week</span></span>|
|<span data-ttu-id="bc484-196">lø eller lørdag</span><span class="sxs-lookup"><span data-stu-id="bc484-196">sa or Saturday</span></span>|<span data-ttu-id="bc484-197">Lørdag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="bc484-197">Saturday of the work date week</span></span>|
|<span data-ttu-id="bc484-198">s eller søndag</span><span class="sxs-lookup"><span data-stu-id="bc484-198">s or Sunday</span></span>|<span data-ttu-id="bc484-199">Søndag i ugen for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="bc484-199">Sunday of the work date week</span></span>|
|<span data-ttu-id="bc484-200">ti23</span><span class="sxs-lookup"><span data-stu-id="bc484-200">t23</span></span>|<span data-ttu-id="bc484-201">Tirsdag i uge 23 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="bc484-201">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="bc484-202">ti 23</span><span class="sxs-lookup"><span data-stu-id="bc484-202">t 23</span></span>|<span data-ttu-id="bc484-203">Tirsdag i uge 23 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="bc484-203">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="bc484-204">ti-1</span><span class="sxs-lookup"><span data-stu-id="bc484-204">t-1</span></span>|<span data-ttu-id="bc484-205">Tirsdag i uge 1 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="bc484-205">Tuesday of week 1 of the work date year</span></span>|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="bc484-206">Angive intervaller</span><span class="sxs-lookup"><span data-stu-id="bc484-206">Setting Ranges</span></span>

<span data-ttu-id="bc484-207">På lister, i totaler og rapporter kan angive filtre for datoer, klokkeslæt og dato/klokkeslæt, der indeholder en startværdi og eventuelt en slutværdi for kun at få vist dataene i det pågældende interval.</span><span class="sxs-lookup"><span data-stu-id="bc484-207">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="bc484-208">Standardreglerne gælder for den måde, du angiver datointervaller på.</span><span class="sxs-lookup"><span data-stu-id="bc484-208">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="bc484-209">**Betydning**</span><span class="sxs-lookup"><span data-stu-id="bc484-209">**Meaning**</span></span>|<span data-ttu-id="bc484-210">**Eksempeludtryk (dato)**</span><span class="sxs-lookup"><span data-stu-id="bc484-210">**Sample expression (Date)**</span></span>|<span data-ttu-id="bc484-211">**Data, der indgår i filteret**</span><span class="sxs-lookup"><span data-stu-id="bc484-211">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="bc484-212">Interval</span><span class="sxs-lookup"><span data-stu-id="bc484-212">Interval</span></span>|<span data-ttu-id="bc484-213">15-12-00..15-01-01</span><span class="sxs-lookup"><span data-stu-id="bc484-213">12 15 00..01 15 01</span></span><br /><br /><span data-ttu-id="bc484-214">..15-12-00</span><span class="sxs-lookup"><span data-stu-id="bc484-214">..12 15 00</span></span><br /><br /><span data-ttu-id="bc484-215">p1..p4</span><span class="sxs-lookup"><span data-stu-id="bc484-215">p1..p4</span></span>|<span data-ttu-id="bc484-216">Records med datoer fra og med 15-12-00 til og med 15-01-01.</span><span class="sxs-lookup"><span data-stu-id="bc484-216">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="bc484-217">Records med datoen 15 12 00 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="bc484-217">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="bc484-218">Datointerval, der indeholder den anden, tredje og fjerde regnskabsperiode, f.eks. 01-01-20--30-04-20.</span><span class="sxs-lookup"><span data-stu-id="bc484-218">Date range that includes the second, third, and fourth accounting periods, such as 01/01/20..04/30/20.</span></span>|
|<span data-ttu-id="bc484-219">Enten/ eller</span><span class="sxs-lookup"><span data-stu-id="bc484-219">Either/or</span></span>|<span data-ttu-id="bc484-220">15 12 00\|16 12 00</span><span class="sxs-lookup"><span data-stu-id="bc484-220">12 15 00\|12 16 00</span></span>|<span data-ttu-id="bc484-221">Records med datoen 15 12 00 eller 16 12 00.</span><span class="sxs-lookup"><span data-stu-id="bc484-221">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="bc484-222">Hvis der er records med datoer på begge dage, vises de alle.</span><span class="sxs-lookup"><span data-stu-id="bc484-222">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="bc484-223">Kombination</span><span class="sxs-lookup"><span data-stu-id="bc484-223">Combination</span></span>|<span data-ttu-id="bc484-224">15 12 00\|01 12 00..10 12 00</span><span class="sxs-lookup"><span data-stu-id="bc484-224">12 15 00\|12 01 00..12 10 00</span></span>  <br /><br /><span data-ttu-id="bc484-225">..14 12 00\|30 12 00..</span><span class="sxs-lookup"><span data-stu-id="bc484-225">..12 14 00\|12 30 00..</span></span>|<span data-ttu-id="bc484-226">Records med datoerne 15-12-00 eller poster fra og med 01-12-00 til og med 10-12-00.</span><span class="sxs-lookup"><span data-stu-id="bc484-226">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <br /><br /><span data-ttu-id="bc484-227">Records med datoer den 14-12-00 eller tidligere eller den 30-12-00 eller senere, dvs. alle records, undtagen dokumenter med datoer fra og med 15-12-00 til og med 29-12-00.</span><span class="sxs-lookup"><span data-stu-id="bc484-227">Records with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="bc484-228">Du kan bruge de gyldige formater i datointervalfiltre.</span><span class="sxs-lookup"><span data-stu-id="bc484-228">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="bc484-229">F.eks. resulterer man14 03..d 16, der anvendes på et dato og klokkeslætsfelt, i et filter fra kl. 3 mandag i uge 14 for den igangværende arbejdsdatos år, begge inklusive, indtil i dag kl. 16 inklusive.</span><span class="sxs-lookup"><span data-stu-id="bc484-229">For example, mon14 3..t 4p applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="bc484-230">Bruge datoformler</span><span class="sxs-lookup"><span data-stu-id="bc484-230">Using Date Formulas</span></span>
<span data-ttu-id="bc484-231">En datoformel er en kort, forkortet kombination af bogstaver og tal, der angiver, hvordan datoer skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="bc484-231">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="bc484-232">Du kan angive datoformler i forskellige datoberegningsfelter eller filtre.</span><span class="sxs-lookup"><span data-stu-id="bc484-232">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="bc484-233">I alle formlens datafelter indgår en dag automatisk til at dække i dag som den dag, hvor perioden starter.</span><span class="sxs-lookup"><span data-stu-id="bc484-233">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="bc484-234">Tilsvarende, hvis du f.eks. indtaster 1U, så er perioden faktisk otte dage, fordi i dag er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="bc484-234">Accordingly, for example, if you enter 1W, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="bc484-235">Du skal indtaste 6D eller 1U-1D for at angive en periode på syv dage \(en rigtig uge\), der medtager periodens startdato.</span><span class="sxs-lookup"><span data-stu-id="bc484-235">To specify a period of seven days \(one true week\) including the period starting date, then you must enter 6D or 1W-1D.</span></span>

<span data-ttu-id="bc484-236">Her følger et par eksempler på brugen af datoformler:</span><span class="sxs-lookup"><span data-stu-id="bc484-236">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="bc484-237">Datoformlen i gentagelsesintervalfeltet i en gentagelseskladde afgør, hvor tit posten på kladdelinjen skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="bc484-237">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="bc484-238">Datoformlen i feltet **Respitperiode** for et bestemt rykkerniveau afgør det tidsrum, der skal gå fra forfaldsdatoen \(eller fra datoen for den forrige rykker\), før der oprettes en rykker.</span><span class="sxs-lookup"><span data-stu-id="bc484-238">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="bc484-239">Datoformlen i feltet **Forfaldsdatoformel** afgør, hvordan forfaldsdatoen på rykkeren beregnes.</span><span class="sxs-lookup"><span data-stu-id="bc484-239">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="bc484-240">Datoformlen kan indeholde op til 20 tegn (både tal og bogstaver).</span><span class="sxs-lookup"><span data-stu-id="bc484-240">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="bc484-241">Du kan bruge følgende bogstaver som forkortelser for kalenderenheder.</span><span class="sxs-lookup"><span data-stu-id="bc484-241">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="bc484-242">Bogstav</span><span class="sxs-lookup"><span data-stu-id="bc484-242">Letter</span></span>  |  <span data-ttu-id="bc484-243">Betyder</span><span class="sxs-lookup"><span data-stu-id="bc484-243">Meaning</span></span>  |
|----------|----------------------|
|<span data-ttu-id="bc484-244">L</span><span class="sxs-lookup"><span data-stu-id="bc484-244">C</span></span>|<span data-ttu-id="bc484-245">Løbende</span><span class="sxs-lookup"><span data-stu-id="bc484-245">Current</span></span>|
|<span data-ttu-id="bc484-246">D</span><span class="sxs-lookup"><span data-stu-id="bc484-246">D</span></span>|<span data-ttu-id="bc484-247">Dag\(e\)</span><span class="sxs-lookup"><span data-stu-id="bc484-247">Day\(s\)</span></span>|
|<span data-ttu-id="bc484-248">U</span><span class="sxs-lookup"><span data-stu-id="bc484-248">W</span></span>|<span data-ttu-id="bc484-249">Uge\(r\)</span><span class="sxs-lookup"><span data-stu-id="bc484-249">Week\(s\)</span></span>|
|<span data-ttu-id="bc484-250">M</span><span class="sxs-lookup"><span data-stu-id="bc484-250">M</span></span>|<span data-ttu-id="bc484-251">Måned\(er\)</span><span class="sxs-lookup"><span data-stu-id="bc484-251">Month\(s\)</span></span>|
|<span data-ttu-id="bc484-252">K</span><span class="sxs-lookup"><span data-stu-id="bc484-252">Q</span></span>|<span data-ttu-id="bc484-253">Kvartal\(er\)</span><span class="sxs-lookup"><span data-stu-id="bc484-253">Quarter\(s\)</span></span>|
|<span data-ttu-id="bc484-254">Å</span><span class="sxs-lookup"><span data-stu-id="bc484-254">Y</span></span>|<span data-ttu-id="bc484-255">År\(\)</span><span class="sxs-lookup"><span data-stu-id="bc484-255">Year\(s\)</span></span>|

<span data-ttu-id="bc484-256">Datoformlen kan opbygges på tre måder.</span><span class="sxs-lookup"><span data-stu-id="bc484-256">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="bc484-257">Følgende eksempel viser, hvordan du skal bruge A for aktuel og en tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="bc484-257">The following example shows how to use C, for current, and a time unit.</span></span>

|  <span data-ttu-id="bc484-258">Udtryk</span><span class="sxs-lookup"><span data-stu-id="bc484-258">Expression</span></span>  |  <span data-ttu-id="bc484-259">Betyder</span><span class="sxs-lookup"><span data-stu-id="bc484-259">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="bc484-260">LU</span><span class="sxs-lookup"><span data-stu-id="bc484-260">CW</span></span>|<span data-ttu-id="bc484-261">Løbende uge</span><span class="sxs-lookup"><span data-stu-id="bc484-261">Current week</span></span>|
|<span data-ttu-id="bc484-262">LM</span><span class="sxs-lookup"><span data-stu-id="bc484-262">CM</span></span>|<span data-ttu-id="bc484-263">Løbende måned</span><span class="sxs-lookup"><span data-stu-id="bc484-263">Current month</span></span>|

<span data-ttu-id="bc484-264">Følgende eksempel viser, hvordan du skal bruge et tal og en tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="bc484-264">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="bc484-265">Tallet må ikke være større end 9999.</span><span class="sxs-lookup"><span data-stu-id="bc484-265">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="bc484-266">Udtryk</span><span class="sxs-lookup"><span data-stu-id="bc484-266">Expression</span></span>  |  <span data-ttu-id="bc484-267">Betyder</span><span class="sxs-lookup"><span data-stu-id="bc484-267">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="bc484-268">10D</span><span class="sxs-lookup"><span data-stu-id="bc484-268">10D</span></span>|<span data-ttu-id="bc484-269">10 dage fra i dag</span><span class="sxs-lookup"><span data-stu-id="bc484-269">10 days from today</span></span>|
|<span data-ttu-id="bc484-270">2U</span><span class="sxs-lookup"><span data-stu-id="bc484-270">2W</span></span>|<span data-ttu-id="bc484-271">2 uger fra i dag</span><span class="sxs-lookup"><span data-stu-id="bc484-271">2 weeks from today</span></span>|

<span data-ttu-id="bc484-272">Følgende eksempel viser, hvordan du skal bruge en tidsenhed og et tal.</span><span class="sxs-lookup"><span data-stu-id="bc484-272">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="bc484-273">Udtryk</span><span class="sxs-lookup"><span data-stu-id="bc484-273">Expression</span></span>  |  <span data-ttu-id="bc484-274">Betyder</span><span class="sxs-lookup"><span data-stu-id="bc484-274">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="bc484-275">D10</span><span class="sxs-lookup"><span data-stu-id="bc484-275">D10</span></span>|<span data-ttu-id="bc484-276">Den næste 10. dage i en måned</span><span class="sxs-lookup"><span data-stu-id="bc484-276">The next 10th day of a month</span></span>|
|<span data-ttu-id="bc484-277">UD4</span><span class="sxs-lookup"><span data-stu-id="bc484-277">WD4</span></span>|<span data-ttu-id="bc484-278">Den næste 4. dag i en uge \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="bc484-278">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="bc484-279">Følgende eksempel viser, hvordan du kan kombinere de tre formler efter behov.</span><span class="sxs-lookup"><span data-stu-id="bc484-279">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="bc484-280">Udtryk</span><span class="sxs-lookup"><span data-stu-id="bc484-280">Expression</span></span>  |  <span data-ttu-id="bc484-281">Betyder</span><span class="sxs-lookup"><span data-stu-id="bc484-281">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="bc484-282">LM+10D</span><span class="sxs-lookup"><span data-stu-id="bc484-282">CM+10D</span></span>|<span data-ttu-id="bc484-283">Løbende måned \+ 10 dage</span><span class="sxs-lookup"><span data-stu-id="bc484-283">Current month \+ 10 days</span></span>|

<span data-ttu-id="bc484-284">Følgende eksempel viser, hvordan du kan bruge et minustegn til at angive en dato i fortiden.</span><span class="sxs-lookup"><span data-stu-id="bc484-284">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="bc484-285">Udtryk</span><span class="sxs-lookup"><span data-stu-id="bc484-285">Expression</span></span>  |  <span data-ttu-id="bc484-286">Betyder</span><span class="sxs-lookup"><span data-stu-id="bc484-286">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="bc484-287">-1Å</span><span class="sxs-lookup"><span data-stu-id="bc484-287">-1Y</span></span>|<span data-ttu-id="bc484-288">1 år siden fra i dag</span><span class="sxs-lookup"><span data-stu-id="bc484-288">1 year ago from today</span></span>|

> [!IMPORTANT]
> <span data-ttu-id="bc484-289">Hvis lokationen bruger en basiskalender, fortolkes den datoformel, du f.eks. indtaster i feltet **Transporttid**, i overensstemmelse med kalenderens arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="bc484-289">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="bc484-290">For eksempel betyder 1U syv arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="bc484-290">For example, 1W  means seven working days.</span></span>
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

Note that we have used the US date format MMDDYY here. As [!INCLUDE[prod_short](includes/prod_short.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

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

## <a name="entering-times"></a><span data-ttu-id="bc484-291">Angive klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="bc484-291">Entering Times</span></span>
<span data-ttu-id="bc484-292">Når du angiver klokkeslæt, kan du indsætte separatorer uden mellemrum, som du vil have mellem enhederne, men hvis du bruger to cifre for hver enhed op til millisekunder, er det ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="bc484-292">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="bc484-293">Du behøver kun at skrive de største enheder, du vil behøver, de øvrige indstilles til nul.</span><span class="sxs-lookup"><span data-stu-id="bc484-293">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="bc484-294">Du kan også udelade AM/PM-symboler.</span><span class="sxs-lookup"><span data-stu-id="bc484-294">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="bc484-295">I den følgende tabel kan du se, hvordan du kan indtaste klokkeslæt, og hvordan de fortolkes.</span><span class="sxs-lookup"><span data-stu-id="bc484-295">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="bc484-296">Det forudsætter indstillinger for land/område, der formaterer tidspunkter i overensstemmelse med: **Timer:Minutter:Sekunder.Millisekunder.**</span><span class="sxs-lookup"><span data-stu-id="bc484-296">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="bc484-297">og bruger AM og PM-symbolerne 'AM' og 'PM hhv.</span><span class="sxs-lookup"><span data-stu-id="bc484-297">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="bc484-298">**Post**</span><span class="sxs-lookup"><span data-stu-id="bc484-298">**Entry**</span></span>      |<span data-ttu-id="bc484-299">**Fortolkning**</span><span class="sxs-lookup"><span data-stu-id="bc484-299">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="bc484-300">05:23:17</span><span class="sxs-lookup"><span data-stu-id="bc484-300">05:23:17</span></span>|<span data-ttu-id="bc484-301">05:23:17</span><span class="sxs-lookup"><span data-stu-id="bc484-301">05:23:17</span></span>|
|<span data-ttu-id="bc484-302">5</span><span class="sxs-lookup"><span data-stu-id="bc484-302">5</span></span>|<span data-ttu-id="bc484-303">05:00:00</span><span class="sxs-lookup"><span data-stu-id="bc484-303">05:00:00</span></span>|
|<span data-ttu-id="bc484-304">5AM</span><span class="sxs-lookup"><span data-stu-id="bc484-304">5AM</span></span>|<span data-ttu-id="bc484-305">05:00:00</span><span class="sxs-lookup"><span data-stu-id="bc484-305">05:00:00</span></span>|
|<span data-ttu-id="bc484-306">5P</span><span class="sxs-lookup"><span data-stu-id="bc484-306">5P</span></span>|<span data-ttu-id="bc484-307">17:00:00</span><span class="sxs-lookup"><span data-stu-id="bc484-307">17:00:00</span></span>|
|<span data-ttu-id="bc484-308">12</span><span class="sxs-lookup"><span data-stu-id="bc484-308">12</span></span>|<span data-ttu-id="bc484-309">12:00:00</span><span class="sxs-lookup"><span data-stu-id="bc484-309">12:00:00</span></span>|
|<span data-ttu-id="bc484-310">12A</span><span class="sxs-lookup"><span data-stu-id="bc484-310">12A</span></span>|<span data-ttu-id="bc484-311">00:00:00</span><span class="sxs-lookup"><span data-stu-id="bc484-311">00:00:00</span></span>|
|<span data-ttu-id="bc484-312">12P</span><span class="sxs-lookup"><span data-stu-id="bc484-312">12P</span></span>|<span data-ttu-id="bc484-313">12:00:00</span><span class="sxs-lookup"><span data-stu-id="bc484-313">12:00:00</span></span>|
|<span data-ttu-id="bc484-314">17</span><span class="sxs-lookup"><span data-stu-id="bc484-314">17</span></span>|<span data-ttu-id="bc484-315">17:00:00</span><span class="sxs-lookup"><span data-stu-id="bc484-315">17:00:00</span></span>|
|<span data-ttu-id="bc484-316">5:30</span><span class="sxs-lookup"><span data-stu-id="bc484-316">5:30</span></span>|<span data-ttu-id="bc484-317">05:30:00</span><span class="sxs-lookup"><span data-stu-id="bc484-317">05:30:00</span></span>|
|<span data-ttu-id="bc484-318">0530</span><span class="sxs-lookup"><span data-stu-id="bc484-318">0530</span></span>|<span data-ttu-id="bc484-319">05:30:00</span><span class="sxs-lookup"><span data-stu-id="bc484-319">05:30:00</span></span>|
|<span data-ttu-id="bc484-320">5:30:5</span><span class="sxs-lookup"><span data-stu-id="bc484-320">5:30:5</span></span>|<span data-ttu-id="bc484-321">05:30:05</span><span class="sxs-lookup"><span data-stu-id="bc484-321">05:30:05</span></span>|
|<span data-ttu-id="bc484-322">053005</span><span class="sxs-lookup"><span data-stu-id="bc484-322">053005</span></span>|<span data-ttu-id="bc484-323">05:30:05</span><span class="sxs-lookup"><span data-stu-id="bc484-323">05:30:05</span></span>|
|<span data-ttu-id="bc484-324">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="bc484-324">5:30:5,50</span></span>|<span data-ttu-id="bc484-325">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="bc484-325">05:30:05.5</span></span>|
|<span data-ttu-id="bc484-326">053005050</span><span class="sxs-lookup"><span data-stu-id="bc484-326">053005050</span></span>|<span data-ttu-id="bc484-327">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="bc484-327">05:30:05.05</span></span>|

<span data-ttu-id="bc484-328">Du skal være opmærksom på, at millisekunder fortolkes som decimalformat.</span><span class="sxs-lookup"><span data-stu-id="bc484-328">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="bc484-329">Altså betyder f.eks. 3, 30 og 300 alle 300 millisekunder, mens 03 betyder 30 og 003 betyder 3 millisekunder.</span><span class="sxs-lookup"><span data-stu-id="bc484-329">So, for example, 3, 30, and 300 all mean 300 milliseconds, while 03 means 30 and 003 means 3 milliseconds.</span></span>

<span data-ttu-id="bc484-330">Du kan ikke bruge 24:00 til at angive midnat eller bruge værdier større end 24:00.</span><span class="sxs-lookup"><span data-stu-id="bc484-330">You cannot use 24:00 to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="bc484-331">Ordet for 'time" på det sprog, som [!INCLUDE[prod_short](includes/prod_long.md)] bruger, vurderes til det aktuelle tidspunkt på din computer eller en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="bc484-331">The word for 'time' in the language used by [!INCLUDE[prod_short](includes/prod_long.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="bc484-332">Du kan angive en del af ordet fra begyndelsen, f.eks. t eller TIM.</span><span class="sxs-lookup"><span data-stu-id="bc484-332">You can enter any part of the word, starting from the beginning, such as t or TIM.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="bc484-333">Indtastning af kombineret dato/klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="bc484-333">Entering Combined Dates and Times</span></span>

[!INCLUDE [datetimes](includes/datetimes.md)]

## <a name="entering-duration"></a><span data-ttu-id="bc484-334">Angivelse af varighed</span><span class="sxs-lookup"><span data-stu-id="bc484-334">Entering Duration</span></span>
<span data-ttu-id="bc484-335">Nogle felter i programmet repræsenterer en varighed eller et forløbet tidsrum i stedet for en bestemt dato eller klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="bc484-335">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="bc484-336">Du angiver varighed ved at skrive et tal efterfulgt af en måleenhed.</span><span class="sxs-lookup"><span data-stu-id="bc484-336">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="bc484-337">Her er nogle eksempler.</span><span class="sxs-lookup"><span data-stu-id="bc484-337">Here are some examples.</span></span>

|<span data-ttu-id="bc484-338">**Varighed**</span><span class="sxs-lookup"><span data-stu-id="bc484-338">**Duration**</span></span>|<span data-ttu-id="bc484-339">**Enhed**</span><span class="sxs-lookup"><span data-stu-id="bc484-339">**Unit of measure**</span></span>|
|------------|-------------------|
|<span data-ttu-id="bc484-340">2t</span><span class="sxs-lookup"><span data-stu-id="bc484-340">2h</span></span>|<span data-ttu-id="bc484-341">2 timer</span><span class="sxs-lookup"><span data-stu-id="bc484-341">2 hrs</span></span>|
|<span data-ttu-id="bc484-342">6t 30 m</span><span class="sxs-lookup"><span data-stu-id="bc484-342">6h 30 m</span></span>|<span data-ttu-id="bc484-343">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="bc484-343">6 hrs 30 mins</span></span>|
|<span data-ttu-id="bc484-344">6,5t</span><span class="sxs-lookup"><span data-stu-id="bc484-344">6.5h</span></span>|<span data-ttu-id="bc484-345">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="bc484-345">6 hrs 30 mins</span></span>|
|<span data-ttu-id="bc484-346">90m</span><span class="sxs-lookup"><span data-stu-id="bc484-346">90m</span></span>|<span data-ttu-id="bc484-347">1 time 30 min</span><span class="sxs-lookup"><span data-stu-id="bc484-347">1 hr 30 mins</span></span>|
|<span data-ttu-id="bc484-348">2d 6t 30m</span><span class="sxs-lookup"><span data-stu-id="bc484-348">2d 6h 30m</span></span>|<span data-ttu-id="bc484-349">2 dage 6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="bc484-349">2 days 6 hrs 30 mins</span></span>|
|<span data-ttu-id="bc484-350">2d 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="bc484-350">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="bc484-351">2 dage 6 timer 30 min 56 sek 600 msek</span><span class="sxs-lookup"><span data-stu-id="bc484-351">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="bc484-352">Du kan også skrive et tal, der automatisk konverteres til en varighed.</span><span class="sxs-lookup"><span data-stu-id="bc484-352">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="bc484-353">Det tal, du skriver, konverteres i overensstemmelse med den standardmåleenhed, der er angivet i feltet Varighed.</span><span class="sxs-lookup"><span data-stu-id="bc484-353">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="bc484-354">Du kan se, hvilken måleenhed, der anvendes i feltet Varighed, ved at skrive et tal og se, hvilken måleenhed tallet konverteres til.</span><span class="sxs-lookup"><span data-stu-id="bc484-354">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="bc484-355">Hvis måleenheden f.eks. er timer, konverteres tallet 5 til 5 timer.</span><span class="sxs-lookup"><span data-stu-id="bc484-355">For example, if the unit of measure is hours, the number 5 is converted to 5 hrs.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc484-356">Se også</span><span class="sxs-lookup"><span data-stu-id="bc484-356">See Also</span></span>
<span data-ttu-id="bc484-357">[Arbejde med [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bc484-357">[Working with [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="bc484-358">Beregning af forfaldsdato for køb</span><span class="sxs-lookup"><span data-stu-id="bc484-358">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="bc484-359">Indtaste kriterier i filtre</span><span class="sxs-lookup"><span data-stu-id="bc484-359">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]