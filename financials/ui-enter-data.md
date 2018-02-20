---
title: "Sådan angiver du data i felter | Microsoft Docs"
description: "Der er mange generelle funktioner, der hjælper dig med at indtaste data på en hurtig og nem måde. De generelle funktioner til indtastning af data er beskrevet i dette emne."
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 5f95efb5cad24db9848752035172bc7bb76db716
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="entering-data"></a>Angivelse af data
Der er mange generelle funktioner, der hjælper dig med at indtaste data på en hurtig og nem måde. De generelle funktioner til indtastning af data er beskrevet i denne artikel.  

Eksemplerne i denne artikel bruger demodata.

## <a name="mandatory-fields"></a>Obligatoriske felter
Når du indtaster data på sider, er visse felter markeret med en rød stjerne. Den røde stjerne betyder, at feltet skal udfyldes for at fuldføre en bestemt proces, der bruger feltet, f.eks. bogføring af en transaktion, der bruger værdien i feltet.  

Selv om feltet indeholder en rød stjerne, er du ikke tvunget til at udfylde feltet, før du fortsætter til andre felter eller lukker siden. Den røde stjerne tjener kun som en påmindelse om, at du vil blive blokeret fra at udføre en bestemt proces.  


## <a name="finding-data-as-you-type"></a>Søge efter data mens du skriver  
 Når du begynder at indtaste tegn i et felt, vises en rulleliste med mulige feltværdier. Listen ændres, når du skriver flere tegn, og du kan vælge den korrekte værdi, når den vises.  

 Mange felter har en knap med en nedadgående pil, som du kan vælge. Når du vælger pilen, vises en liste med data, som du kan vælge at indtaste i feltet. Knappen har to funktioner afhængigt af felttypen:  

-   Valg – viser oplysninger fra en anden tabel, som du kan indtaste i feltet. Du kan vælge én enkelt dataangivelse ad gangen.  

-   Rullemenu – viser det sæt indstillinger, der findes til feltet. Du kan kun vælge én af indstillingerne.  

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

## <a name="entering-quantities-by-calculation"></a>Angive mængder ved beregning  
 Når du angiver tal i mængdefelter, f.eks. i feltet **Antal** på en varekladdelinje, kan du angive formlen i stedet for summen af mængden.  

## <a name="examples"></a>Eksempler  

-   Hvis du skriver 19+19, beregnes feltet til 38.  

-   Hvis du skriver 41-9, beregnes feltet til 32.  

-   Hvis du skriver 12*4, beregnes feltet til 48.  

-   Hvis du skriver 12/4, beregnes feltet til 3.  

# <a name="entering-negative-numbers"></a>Angivelse af negative tal
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
 I et datofelt kan du indtaste to, fire, seks eller otte cifre:  

-   Hvis du kun indtaster to tal, fortolkes dette som dagen og måneden og året indsættes ud fra arbejdsdatoen.  

-   Hvis du indtaster fire tal, fortolkes dette som dagen og måneden, og året indsættes ud fra arbejdsdatoen.  

-   Hvis datoen falder inden for 01-01-1930 og 31-12-2029, kan du nøjes med to tal for året, ellers skal året angives med fire cifre.  

 Du kan også indtaste datoen som en ugedag efterfulgt af ugenummeret og evt. året (f.eks. betyder Man25 eller man25 mandag i uge 25).  

 I stedet for en bestemt dato kan du indtaste én af to koder.  

|Kode|Resultat|  
|--------------|----------------|  
|d|Dette er dags dato (computerens systemdato).|  
|a|Dette er den arbejdsdato, der er angivet i programmet. Hvis du vil ændre arbejdsdatoen, kan du se i [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md). Det er en fordel at anvende en arbejdsdato, hvis du har mange transaktioner at udføre på en dato, der ikke er dags dato.|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

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
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a>Bruge datoformler  
 En datoformel er en kort, forkortet kombination af bogstaver og tal, der angiver, hvordan datoer skal beregnes. Du kan indtaste datoformler i forskellige datoberegningsfelter og i gentagelsesintervalfelter i gentagelseskladder.  

> [!NOTE]  
>  I alle formlens datafelter indgår en dag automatisk til at dække i dag som den dag, hvor perioden starter. Tilsvarende, hvis du f.eks. indtaster 1U, så er perioden faktisk otte dage, fordi i dag er inkluderet. Du skal indtaste 6D eller 1U-1D for at angive en periode på syv dage (en rigtig uge), der medtager periodens startdato.  

 Her følger et par eksempler på brugen af datoformler:  

-   Datoformlen i gentagelsesintervalfeltet i en gentagelseskladde afgør, hvor tit posten på kladdelinjen skal bogføres.  

-   Datoformlen i feltet Respitperiode for et bestemt rykkerniveau afgør det tidsrum, der skal gå fra forfaldsdatoen (eller fra datoen for den forrige rykker), før der oprettes en rykker.  

-   Datoformlen i feltet Forfaldsdatoformel afgør, hvordan forfaldsdatoen på rykkeren beregnes.  

 Datoformlen kan indeholde op til 20 tegn (både tal og bogstaver). Du kan bruge følgende bogstaver som forkortelser for tidsangivelser.  

|||  
|-|-|  
|L|Løbende|  
|D|Dag(e)|  
|U|Uge(r)|  
|M|Måned(er)|  
|K|Kvartal(er)|  
|Å|År|  

 Datoformlen kan opbygges på tre måder.  

 Følgende eksempel viser aktuelle plus en tidsenhed.  

|||  
|-|-|  
|LU|Løbende uge|  
|LM|Løbende måned|  

 Følgende eksempel viser et tal og en tidsenhed. Tallet må ikke være større end 9999.  

|||  
|-|-|  
|10D|10 dage fra i dag|  
|2U|2 uger fra i dag|  

 Følgende eksempel viser en tidsenhed og et tal.  

|||  
|-|-|  
|D10|Den næste 10. dage i en måned|  
|UD4|Den næste 4. dag i en uge (torsdag)|  

 Følgende eksempel viser, hvordan du kan kombinere de tre formler efter behov.  

|||  
|-|-|  
|LM+10D|Løbende måned plus 10 dage|  

 Følgende eksempel viser, hvordan du kan bruge et minustegn til at angive en dato i fortiden.  

|||  
|-|-|  
|-1Å|1 år siden fra i dag|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a>Se også  
 [Søgning i, filtrering og sortering af data](ui-enter-criteria-filters.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

