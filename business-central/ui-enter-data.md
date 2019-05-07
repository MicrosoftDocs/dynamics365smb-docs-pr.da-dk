---
title: Sådan angiver du data i felter | Microsoft Docs
description: Få mere at vide om generelle funktioner, der hjælper dig med at indtaste data i felter.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 00143454cf0b0da9b111f92bcdb7879c7e6743d2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "929069"
---
# <a name="entering-data"></a>Angivelse af data

Der er mange generelle funktioner, der hjælper dig med at indtaste data data lettere, hurtigere og mere nøjagtigt. De generelle funktioner til indtastning af data er beskrevet i denne artikel.  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a>Tastaturgenveje

Der er adskillige tastaturgenveje, du kan bruge, når du vil arbejde uden mus, og som gør dataindtastning hurtigere, især i forbindelse med store poster og gentagne indtastningsopgaver.

Du kan finde flere oplysninger om genveje i [Tastaturgenveje](keyboard-shortcuts.md). Nogle af genvejene er beskrevet i denne artikel.

## <a name="QuickEntry"></a>Fremskynde dataindtastning ved hjælp af genveje

Genvej er en funktion, der er designet til dataindtastning med brug af tastatur. Genvej fungerer på felter (f.eks. på kortider) og i lister (rækker og kolonner). Det er nyttige, når du udfører gentagne indtastningsopgaver, der kræver oprettelse af flere poster i rækkefølge, f.eks. en kørsel med salgsordrer eller registrering af nye varer.

Du er muligvis allerede fortrolig med brugen af tabulatortasten til at navigere fra ét felt på en side til næste redigerbare felt. En ulempe ved at bruge tabulatortasten er, at den altid går til næste felt i rækkefølge. <!-- even if the field is non-editable or seldom filled it in.-->Genvej gør det muligt at ændre denne fremgangsmåde. Med genvej kan du bruge Enter-tasten til udelukkende at navigere blandt de felter, du er interesseret i, og overspringe ikke-redigerbare felter og felter, som du normalt ikke udfylder. Du har muligvis allerede bemærket denne funktionsmåde på nogle sider. Det skyldes, at programmet allerede angiver, hvilke felter der skal medtages, når du trykker på Enter, og hvilke der skal springes over. Du kan tilpasse genvej ved at tilpasse dit arbejdsområde og optimere den måde, du indtaster data på hver side.

### <a name="how-quick-entry-works"></a>Sådan fungerer genvej

Hvert felt kan markeres som enten *medtaget i genvej* eller *udelukket fra genvej*. Felter, der indgår i genvej, medtages i stien, når du trykker på Enter. Felter, der er udelukket fra genvej, medtages ikke.

Når du er færdig med at angive data i et felt, du blot trykke på Enter for at bekræfte ændringerne og gå til næste felt. Hvis du vil vende retningen og gå til det forrige felt, skal du trykke på Shift+Enter. Du kan finde flere oplysninger om genveje i [Tastaturgenveje i genvej](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Tip
Følgende indeholder nyttige oplysninger om brugen af genvej.

- Den findes i alle redigerbare felter.
- Den kan også bruges på tværs af kolonner og rækker.
- Den forhindrer ikke adgang til andre elementer på en side, f.eks. handlinger. De er stadig tilgængelige ved hjælp af tabulatortasten og Shift+Tab.  
- Oversigtspanelerne behøver ikke at blive udvidet for at få genvej til at fungere. Hvis næste genvejsfelt er placeret i et skjult oversigtspanel, udvides det pågældende oversigtspanel automatisk og fokuserer på det angivne felt.
- Genvej fungerer, uanset om felter skal udfyldes. Det er derfor en god ide at sikre, at obligatoriske felter er medtaget i genvej.
- Som standard medtages de fleste felter automatisk i genvej. Så til at starte med skal du derfor sandsynligvis udelukke felter fra genvej.

### <a name="how-to-change-quick-entry-fields"></a>Sådan ændres genvejsfelter

Hvis du vil ændre, hvilke felter der medtages i eller udelukkes fra genvej på en side, kan du bruge tilpasning.

1. Start tilpasning ved at vælge ikonet ![Indstillinger](media/ui-experience/settings_icon_small.png "ikonet Indstillinger til rollecenter") og derefter **Tilpas**.
2. Markér et felt, du vil ændre, eller markér på lister den tilsvarende kolonneoverskrift, og vælg derefter enten **Medtag i genvej** eller **Udeluk fra genvej**.

Du kan finde flere oplysninger om tilpasning under [Tilpasse dit arbejdsområde](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Obligatoriske felter

Når du indtaster data på sider, er visse felter markeret med en rød stjerne. Den røde stjerne betyder, at feltet skal udfyldes for at fuldføre en bestemt proces, der bruger feltet, f.eks. bogføring af en transaktion, der bruger værdien i feltet.  

Selv om feltet indeholder en rød stjerne, er du ikke tvunget til at udfylde feltet, før du fortsætter til andre felter eller lukker siden. Den røde stjerne tjener kun som en påmindelse om, at du vil blive blokeret fra at udføre en bestemt proces.  

## <a name="finding-data-as-you-type"></a>Søge efter data mens du skriver

 Når du begynder at indtaste tegn i et felt, vises en rulleliste med mulige feltværdier. Listen ændres, når du skriver flere tegn, og du kan vælge den korrekte værdi, når den vises.  

 Mange felter har en knap med en nedadgående pil, som du kan vælge. Når du vælger pilen, vises en liste med data, som du kan vælge at indtaste i feltet. Knappen har to funktioner afhængigt af felttypen:  

-   Valg – viser oplysninger fra en anden tabel, som du kan indtaste i feltet. Du kan vælge én enkelt dataangivelse ad gangen.  

-   Rullemenu – viser det sæt indstillinger, der findes til feltet. Du kan kun vælge én af indstillingerne.  

## <a name="copying-and-pasting-fields-and-lines"></a>Kopiere og indsætte felter og linjer

Du kan kopiere en eller flere rækker fra en liste eller et enkelt felt på en side og derefter indsætte det, du har kopieret på den samme side, en anden side eller et eksternt dokument (som Microsoft Excel og e-mails i Outlook). Kort sagt, når du vil kopiere, skal du trykke på CTRL + C (cmd + C i macOS) på tastaturet. Når du vil indsætte, skal du trykke på CTRL + V (cmd + V i macOS).

Hvis du på en liste vil kopiere feltet i den samme kolonne i rækken ovenfor og indsætte det i den aktuelle række, skal du bare trykke på F8.

Du kan finde flere oplysninger i [Kopiere og indsætte i Business Central](ui-copy-paste.md).

## <a name="Focus"></a>Fokusere på linjevarer

Når du arbejder med dokumenter, som indeholder en del med linjevarer, f.eks. en salgsordre eller fakturaside, kan du skifte visningen til udelukkende at fokusere på linjevarer, hvilket reelt udvider delen med linjevarer, så den optager ret meget af hele arbejdsområdet – og skjuler andre dele af siden undtagen handlingsområdet øverst. Det giver dig et bedre overblik over linjevarerne og giver mere plads til at arbejde med dem. Dette er især nyttige, når du arbejder med store lister med linjevarer, og der ønskes hurtig dataindtastning.

En anden fordel er, at det også indeholder avancerede filterfunktioner, som på andre lister, så det bliver endnu nemmere at gennemse og søge gennem linjevarer.

### <a name="switch-the-focus-on-and-off"></a>Slå fokus til og fra

Når du vil fokusere på linjevarer, skal du markeret et vilkårligt sted i delen med linjevarer og derefter vælge ![Ikonet Fokustilstand](media/focus-mode.png "Ikonet Fokustilstand") i øverste højre hjørne eller trykke på Ctrl+Shift+F12.

For at vende tilbage til normal visning skal du vælge ![Ikonet Fokustilstand](media/focus-mode.png "Ikonet Fokustilstand") eller trykke på Ctrl+Shift+F12 igen.

### <a name="filtering-the-line-items"></a>Filtrere linjevarerne

Du starter filtrering ved at vælge ![Ikonet Filterrude](media/open-filter-pane-icon.png "Ikonet Filterrude") øverst på listen eller ved at trykke på **Shift+F3** for at åbne filterruden. Du arbejder med filterruden, på samme måde som du arbejder med andre lister. Du kan finde flere oplysninger i [Filtrering](ui-enter-criteria-filters.md#Filtering).

Filtrering er især nyttig, når du får vist og analyserer længere dokumenter. Antag f.eks., at du åbner en bogført salgsfaktura og filtrerer linjevarerne for at få vist alle linjevarer med en individuel rabat over 5 % eller filtrerer for udelukkende at få vist cykeltilbehør med 'pro' i navnet.

## <a name="entering-quantities-by-calculation"></a>Angive mængder ved beregning

Når du angiver tal i mængdefelter, f.eks. i feltet **Antal** på en varekladdelinje, kan du angive formlen i stedet for summen af mængden.  

### <a name="examples"></a>Eksempler  

-   Hvis du skriver 19+19, beregnes feltet til 38.  

-   Hvis du skriver 41-9, beregnes feltet til 32.  

-   Hvis du skriver 12*4, beregnes feltet til 48.  

-   Hvis du skriver 12/4, beregnes feltet til 3.  

## <a name="entering-negative-numbers"></a>Angivelse af negative tal

Du kan angive negative tal på to måder. Tallet -20,5 kan angives som:  

-   -20,5  

    eller
-   20,5-  

 I begge tilfælde registreres beløbet som -20,5.  

 Hvis det sidste tegn i udtrykket er et **+** eller et **-**, registreres hele udtrykket med det tegn. Eksempel, **10-20+** medfører 10 og ikke -10.  

## <a name="entering-dates-and-times"></a>Indtaste datoer og tidspunkter

Du kan angive datoer og klokkeslæt i alle de felter, der er angivet specielt til datoer (datofelter). Du kan angive datoer med eller uden separatorer.

> [!NOTE]  
> Måden, du angiver datoer og klokkeslæt på, afhænger af dine indstillinger i **Område**. Du kan finde flere oplysninger under [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Angive datoer

For datofelter kan du enten bruge datavælgeren, som gør det muligt at vælge en dato i en kalender, eller du kan angive datoer manuelt. Denne sektion indeholder en kort oversigt over, hvordan du angiver datoer. Du kan finde flere oplysninger i [Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md).

Hvis du vil indtaste datoen manuelt, kan du indtaste to, fire, seks eller otte cifre:  

-   Hvis du kun indtaster to tal, fortolkes dette som dagen og måneden og året indsættes ud fra arbejdsdatoen.  

-   Hvis du indtaster fire tal, fortolkes dette som dagen og måneden, og året indsættes ud fra arbejdsdatoen.  

-   Hvis datoen falder inden for 01-01-1930 og 31-12-2029, kan du nøjes med to tal for året, ellers skal året angives med fire cifre.  

Du kan også indtaste datoen som en ugedag efterfulgt af ugenummeret og evt. året (f.eks. betyder Man25 eller man25 mandag i uge 25).  

I stedet for en bestemt dato kan du indtaste én af disse koder.  

|Kode|Resultat|  
|--------------|----------------|  
|d|Dette angiver dags dato (computerens systemdato).|  
|p|Dette angiver en regnskabsperiode, hvor `p`betyder den første regnskabsperiode, `p2` betyder den anden regnskabsperiode osv. |
|a|Dette angiver den arbejdsdato, der er angivet i programmet. Hvis du vil ændre arbejdsdatoen, kan du se i [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md). Det er en fordel at anvende en arbejdsdato, hvis du har mange transaktioner at udføre på en dato, der ikke er dags dato.|
|c|Dette angiver, at datoen efter `c`er en ultimodato, f.eks. `C123101`.|  

## <a name="entering-times"></a>Angive klokkeslæt

Når du angiver klokkeslæt, kan du indsætte en vilkårlig separator mellem tidsenhederne, men det er ikke påkrævet. Det er ikke nødvendigt at skrive minutter, sekunder eller AM/PM.  

I den følgende tabel kan du se, hvordan du kan indtaste klokkeslæt, og hvordan de fortolkes.  

|Post|Fortolkning|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5.50|05:30:05,5|  
|053005050|05:30:05.05|  

 Du skal skrive to tal for hver tidsenhed, hvis du ikke angiver en separator.  

## <a name="entering-datetimes"></a>Angive dato/klokkeslæt

Når du angiver dato/klokkeslæt skal du angive et mellemrum mellem datoen og klokkeslættet.  

I den følgende tabel kan du se, hvordan du kan skrive dato og klokkeslæt, og hvordan de fortolkes.  

|Post|Fortolkning|  
|---------------|------------------------|  
|131202 132455|13-12-02 13:24:55|  
|1-12-02 10|01-12-02 10:00:00|  
|1.12.02 5|01-12-02 05:00:00|  
|1.12.02|01-12-02 00:00:00|  
|11 12|11-løbende måned-løbende år 12:00:00|  
|1112 12|11-12-aktuelt år 12:00:00|  
|d eller dags dato|dags dato 00:00:00|  
|t tid|dags dato aktuelt klokkeslæt|  
|d 10:30|dags dato 10:30:00|  
|d 3:3:3|dags dato 03:03:03|  
|a eller arbejdsdato|arbejdsdato 00:00:00|  
|m eller mandag|Mandag i den aktuelle uge 00:00:00|  
|ti eller tirsdag|Tirsdag i den aktuelle uge 00:00:00|  
|on eller onsdag|Onsdag i den aktuelle uge 00:00:00|  
|to eller torsdag|Torsdag i den aktuelle uge 00:00:00|  
|f eller fredag|Fredag i den aktuelle uge 00:00:00|  
|l eller lørdag|Lørdag i den aktuelle uge 00:00:00|  
|s eller søndag|Søndag i den aktuelle uge 00:00:00|  
|ti 10:30|Tirsdag i den aktuelle uge 10:30:00|  
|ti 3:3:3|Tirsdag i den aktuelle uge 03:03:03|  

## <a name="entering-duration"></a>Angivelse af varighed

Du angiver varighed ved at skrive et tal efterfulgt af en måleenhed.  

Her er nogle eksempler.  

|Varighed|Enhed**|  
|------------------|-------------------------|  
|2t|2 timer|  
|6t 30 m|6 timer 30 min|  
|6,5t|6 timer 30 min|  
|90m|1 time 30 min|  
|2d 6t 30m|2 dage 6 timer 30 min|  
|2d 6t 30m 56s 600ms|2 dage 6 timer 30 min 56 sek 600 msek|  

 Du kan også skrive et tal, der så automatisk konverteres til en varighed. Det tal, du skriver, konverteres i overensstemmelse med den standardmåleenhed, der er angivet i feltet Varighed.  

 Du kan se, hvilken måleenhed, der anvendes i feltet Varighed, ved at skrive et tal og se, hvilken måleenhed tallet konverteres til.  

 Tallet 5 konverteres til 5 timer, hvis måleenheden er timer.  

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
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a>Se også  
 [Sortering af, søgning i og filtrering af lister](ui-enter-criteria-filters.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
