---
title: 'Fremgangsmåde: Indtaste data Business Central'
description: Der er mange generelle funktioner, der hjælper dig med at indtaste data lettere, hurtigere og mere nøjagtigt. De grundlæggende principper og avancerede funktioner beskrives her.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: decimal separator, data entry, focus
ms.date: 10/01/2021
ms.author: jswymer
ms.openlocfilehash: 1e6dbdd5880902c7b649464ad967f01cc599f37f
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588953"
---
# <a name="entering-data"></a>Angivelse af data

Der er mange generelle funktioner, der hjælper dig med at indtaste data lettere, hurtigere og mere nøjagtigt. De grundlæggende principper og avancerede funktioner til indtastning af data er beskrevet i denne artikel.  

Eksemplerne i denne artikel bruger demodata.

## <a name="working-with-editable-fields"></a>Arbejde med redigerbare felter
Felter i [!INCLUDE[prod_short](includes/prod_short.md)] kan indeholde forskellige redigerbare data, f.eks. tekst eller valutabeløb. Redigerbare felter viser typisk et indtastningsfelt, hvor du kan indtaste eller vælge en værdi. Ikke-redigerbare felter vises typisk med grå baggrund.   

Visse redigerbare felter indeholder en vælger, der kan hjælpe dig med at angive en værdi.  

<!-- TODO: Add illustrations or images of each picker -->
|**Vælger**        |**Sådan hjælper det dig med at angive en værdi**|
|------------------|------------------------------------|
|Datovælger       |Denne vælger viser en kalender, der er baseret på de aktuelle regionale indstillinger. Den gør det lettere at vælge en enkelt dato.|
|Rullemenu          |Rullemenuer giver dig mulighed for at vælge faste værdier eller referenceposter fra en anden tabel|
|Skifteknap eller afkrydsningsfelt|Nogle felter giver mulighed for at vælge mellem *Ja-* eller *Nej*-værdier. Parameteren bruges til at angive denne værdi og vises altid som et afkrydsningsfelt i lister|
|Assisteret redigering       |Nogle felter indeholder brugerdefinerede vælgere, der er gode til at søge efter og vælge den bedste værdi til feltet, f.eks. et pop op-vindue|

### <a name="modifying-a-field-value"></a>Ændring af en feltværdi

Hvis du vil ændre værdien i et felt, skal du først fremhæve feltet. Du kan fremhæve det ved at benytte følgende fremgangsmåde:

- Tryk på **Tab**. Handlingen vælger hele værdien.
- Venstreklik med musen eller den tilsvarende inputenhed. Denne handling markerer kun hele feltværdien, hvis feltet er på en liste.  

Når du interagerer med felter i brugergrænsefladen, prioriterer [!INCLUDE[prod_short](includes/prod_short.md)] typisk markering af hele feltværdien for at gøre det lettere for dig at erstatte denne værdi.

Når hele feltværdien vælges:
- Erstat værdien ved blot at skrive for at angive en ny værdi. Hvis feltet indeholder en vælger, kan du aktivere det med tastaturgenvejen **Alt+pil ned**.
- Brug **Delete** eller **Backspace** til at rydde værdien.

Tryk på **F2** for at skifte mellem at markere hele feltværdien eller placere markøren efter feltets værdi. Når du placerer markøren i slutningen af værdien, bliver det nemmere at vedhæfte til den eksisterende værdi.

Når markøren vises i slutningen af feltværdien:
- Tilføj i værdien ved blot at skrive.
- Brug **Home**, **End**, **venstre pil** og **højrepil** til at flytte markøren inden for værdien. Hvis du redigerer et felt på en liste, fremhæves det forrige felt, når du trykker på **venstre pil** igen, når markøren er i begyndelsen af værdien. Hvis du trykker på **højre pil** igen, når markøren er i slutningen af værdien, fremhæves det næste felt.

> [!NOTE]
> Når du har angivet en værdi, vil Business Central kun kontrollere, at den er gyldig, når du har klikket uden for feltet eller fokuseret på et andet element, f.eks. det næste felt.  

## <a name="keyboard-shortcuts"></a>Tastaturgenveje

Der er flere tastaturgenveje, som du kan bruge til at arbejde uden mus og taste hurtigere. Disse tastaturgenveje er især nyttige, når du skal indtaste meget på én gang og gentagne skriveopgaver.

Du kan finde flere oplysninger om genveje i [Tastaturgenveje](keyboard-shortcuts.md). Nogle af tastaturgenvejene er beskrevet i denne artikel.

## <a name="accelerating-data-entry-using-quick-entry"></a><a name="QuickEntry"></a>Fremskynde dataindtastning ved hjælp af genveje

Genvej er en funktion, der er designet til dataindtastning med brug af tastatur. Genvej fungerer på felter (f.eks. på kortider) og i lister (rækker og kolonner). Dette er nyttigt, når du udfører gentagne indtastningsopgaver, som kræver, at der oprettes flere poster i rækkefølge. Det kan f.eks. være en gruppe af salgsordrer eller registrering af nye varer.

Du er kan bruge Tab til at navigere fra ét felt på en side til det næste redigerbare felt. En ulempe ved at bruge tabulatortasten er, at den altid går til næste felt i rækkefølge. <!-- even if the field is non-editable or seldom filled it in.-->Genvej gør det muligt at ændre denne fremgangsmåde. Genveje giver dig mulighed for at bruge Enter-tasten til kun at navigere gennem de felter, du har brug for. Genveje springer ikke-redigerbare felter over og felter, som du normalt ikke udfylder. Du har muligvis allerede bemærket denne funktionsmåde på nogle sider. Denne adfærd skyldes, at de felter, der skal medtages, når du trykker på Enter, og hvilke der skal springes over, er defineret på forhånd. Du kan tilpasse genvej ved at tilpasse dit arbejdsområde og optimere den måde, du indtaster data på hver side.

### <a name="how-quick-entry-works"></a>Sådan fungerer genvej

Hvert felt kan markeres som enten *medtaget i genvej* eller *Udelukket fra genvej*. Felter, der skal medtages i genveje, vil blive medtaget i stien, når du trykker på ENTER. Felter, der er udeladt fra genveje, medtages ikke.

Når du er færdig med at angive data i et felt, skal du bare trykke på Enter for at bekræfte ændringerne og gå til næste felt. Hvis du vil vende retningen og gå til det forrige felt, skal du trykke på Skift+Enter. Du kan finde flere oplysninger om genveje i [Genveje for felter](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Tip

Følgende liste indeholder nyttige oplysninger om brugen af genveje.

- Den findes i alle redigerbare felter.
- Den kan også bruges på tværs af kolonner og rækker.
- Den forhindrer ikke adgang til andre elementer på en side, f.eks. handlinger. Disse elementer er stadig tilgængelige ved hjælp af Tab og Shift+Tab.  
- Det er ikke nødvendigt at udvide oversigtspanelet for at få genveje til at fungere. Hvis det næste genvejsfelt er placeret i et skjult oversigtspanel, udvides det pågældende oversigtspanel automatisk og fokuserer på det valgte felt. [!INCLUDE[prod_short](includes/prod_short.md)] husker, at oversigtspanelet skal udvides, næste gang du besøger siden.  
- Genveje fungerer, uanset om felter skal udfyldes eller ej. Det er derfor en god ide at sikre, at obligatoriske felter er medtaget i genvej.
- Som standard medtages de fleste felter automatisk i genvej. Så til at starte med skal du derfor sandsynligvis udelukke felter fra genvej.

### <a name="to-change-quick-entry-fields"></a>Sådan ændres genvejsfelter

Hvis du vil konfigurere genvejsmenuen for felter, skal du bruge tilpasning.

1. Start personlige indstillinger ved at vælge ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") Og derefter funktionen **Tilpas**.
2. Markér et felt, der skal ændres. Markér den tilsvarende kolonneoverskrift på listerne. Vælg derefter enten **Medtag i genvej** eller **Udelad fra genvej**.

Du kan finde flere oplysninger om tilpasning under [Tilpasse dit arbejdsområde](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Obligatoriske felter

Når du indtaster data på sider, er visse felter markeret med en rød stjerne. Den røde stjerne betyder, at feltet skal udfyldes, før en bestemt proces kan afsluttes. Det kan f.eks. være, når du bogfører en transaktion, der bruger værdien i feltet.  

Selv om feltet skal udfyldes, er du ikke tvunget til at udfylde feltet, før du fortsætter til andre felter eller lukker siden. Den røde stjerne er kun en påmindelse om, at du vil blive forhindret i at udføre en bestemt proces.  

## <a name="finding-data-as-you-type"></a>Søge efter data mens du skriver

 Når du begynder at indtaste tegn i et felt, vises en rulleliste med mulige feltværdier. Listen ændres, når du skriver flere tegn, og du kan vælge den korrekte værdi, når den vises.  

 Mange felter har en knap med en nedadgående pil, som du kan vælge. Når du vælger pilen, vises en liste med data, som du kan vælge at indtaste i feltet. Knappen har to funktioner afhængigt af felttypen:  

-   Valg – viser oplysninger fra en anden tabel, som du kan indtaste i feltet. Du kan vælge én enkelt dataangivelse ad gangen.  

-   Rullemenu – viser det sæt indstillinger, der findes til feltet. Du kan kun vælge én af indstillingerne.  

## <a name="copying-and-pasting-faq-fields-and-lines"></a>Ofte stillede spørgsmål om kopiering og indsætning af felter og linjer

Du kan kopiere en eller flere rækker fra en liste eller et enkelt felt på en side. Indsæt derefter det, du har kopieret, på den samme side, på en anden side eller i et eksternt dokument. Du kan f.eks. indsætte i Microsoft Excel eller en mail i Outlook. Kort sagt, når du vil kopiere, skal du trykke på CTRL + C (cmd + C i macOS) på tastaturet. Når du vil indsætte, skal du trykke på CTRL + V eller cmd + V i macOS.

Hvis du på en liste vil kopiere feltet i den samme kolonne i rækken ovenfor og indsætte det i den aktuelle række, skal du bare trykke på F8.

Du kan finde flere oplysninger i [Ofte stillede spørgsmål om kopiering og indsætning](faq-copy-paste.yml).

## <a name="filtering-line-items"></a>Filtrere linjevarer

Du starter filtrering ved at vælge ![Ikonet Filterrude](media/open-filter-pane-icon.png "Ikonet Filterrude") øverst på listen eller ved at trykke på Skift+F3 for at åbne filterruden. Du arbejder med filterruden, på samme måde som du arbejder med andre lister. Du kan finde flere oplysninger i [Filtrering](ui-enter-criteria-filters.md#filtering).

Filtrering er især nyttig, når du ser og analyserer længere dokumenter. Forestil dig, at du åbner en bogført salgsfaktura. Derefter filtrerer du linjeelementerne, så de viser alle linjeposter, der har en individuel rabat på over 5 %. Eller du kan filtrere for kun at se cykeltilbehør med "pro" i navnet.

## <a name="focusing-on-line-items"></a><a name="Focus"></a>Fokusere på linjevarer

Når du arbejder med dokumenter, der indeholder en del af en linjevarepost, kan du ændre visningen, så der kun fokuseres på linjevarerne. Dokumenter kan f.eks. være salgsordrer eller fakturasider. Delen af linjeelementer udvides, så den fylder næsten hele arbejdsområdet. Den skjuler andre dele af siden med undtagelse af området med handlinger øverst. Dette layout giver dig et bedre overblik over linjevarerne og giver mere plads til at arbejde med dem.

Dette er især nyttigt, når du arbejder med store linjeelementlister, og du skal indtaste data hurtigt. Denne funktion giver også mulighed for avanceret filtrering. På samme måde som med andre lister bliver søgning efter og gennemsøgning af linjeelementer endnu lettere.

### <a name="switching-the-focus-on-and-off"></a>Slå fokus til og fra

Hvis du vil fokusere på linjeelementer, skal du vælge et vilkårligt sted i linjeelement delen og derefter vælge ![ikonet Fokustilstand.](media/focus-mode.png "Ikonet Fokustilstand") i øverste højre hjørne, eller tryk på Ctrl + Skift + F12.

Hvis du vil skifte tilbage til normal visning, skal du vælge ![ikonet Fokustilstand.](media/focus-mode.png "Ikonet Fokustilstand") eller tryk på Ctrl + Skift + F12 igen.

## <a name="multitasking-across-multiple-pages"></a>Multitasking på tværs af flere sider

Du kan åbne et kort eller en dokumentside i et nyt vindue. Når du åbner et nyt vindue, kan du:

- Arbejde med flere opgaver samtidig
- Håndtere afbrydelser af den aktuelle opgave, f.eks. et indgående opkald.
- Holde et vindue åbent for en igangværende opgave, mens du starter eller udfører en anden opgave i vinduer.

Hvis du vil åbne det aktuelle kort eller dokument i et nyt vindue, skal du vælge ![Åbn nyt vindue.](media/open-new-window-icon.png "Ikonet Åbn i nyt vindue") i øverste højre hjørne, eller tryk på Alt + Skift + W.

<!--
When working on multiple tasks at a time or when managing interruptions to the current task, such as taking an incoming call, you can open a card or document page in a new window. This allows you to keep a window open for an ongoing task while you start or complete another task in one or more other windows.
-->
Hvis du vil åbne det aktuelle kort eller dokument i et nyt vindue, skal du vælge ![Åbn nyt vindue.](media/open-new-window-icon.png "Ikonet Åbn i nyt vindue") i øverste højre hjørne, eller tryk på Alt + Skift + W.

> [!NOTE]
> Når du åbner andre sider fra et kort eller et dokument, der er åbnet i et nyt vindue, åbnes disse sider i et nyt vindue, selvom du ikke vælger ![Åbn nyt vindue.](media/open-new-window-icon.png "Ikonet Åbn i nyt vindue").

> [!NOTE]
> Hvis du arbejder i Safari-browseren, kan blokering af et pop op-vindue medføre, at det nye vindue ikke åbnes. Hvis det er tilfældet, skal du angive produktets URL-adresse som et tilladt websted. Du kan finde flere oplysninger i [Ændre indstillinger i Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Det samme kan forekomme i andre browsere som f.eks. Firefox. Du kan finde flere oplysninger i [Indstillinger for blokering af pop op-vinduer i Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400).  

En anden måde at multitaske på er at åbne [!INCLUDE[prod_short](includes/prod_short.md)] på to eller flere browserfaner. Når du gør det på denne måde, skal du oprette en ny fane og derefter kopiere/indsætte URL-adressen til den oprindelige fane på den nye fane. Derved oprettes en ny session.   

> [!NOTE]
> Brug ikke funktionen **Dupliker** i browseren til at oprette den nye fane, da det kan medføre, at handlinger på en fane blokerer handlinger på andre faner, fordi de er en del af samme session.

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

Du kan angive datoer og klokkeslæt i alle de felter, der er angivet til datoer (datofelter). Du kan angive datoer med eller uden separatorer.

> [!NOTE]  
> Måden, du angiver datoer og klokkeslæt på, afhænger af dine indstillinger i **Område**. Du kan finde flere oplysninger i [Ændre grundlæggende indstillinger](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Angive datoer

Du kan enten bruge datovælgeren til at vælge en dato i en kalender, eller du kan angive datoer manuelt. Denne sektion indeholder en kort oversigt over, hvordan du angiver datoer. Du kan finde flere oplysninger i [Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md).

Hvis du vil indtaste datoen manuelt, kan du indtaste to, fire, seks eller otte cifre:  

-   To tal fortolkes som dagen. Det vil tilføje måneden og året for arbejdsdatoen.  

-   Fire tal fortolkes som dagen og måneden. Dette vil tilføje året for arbejdsdatoen.  

-   Hvis den ønskede dato ligger i intervallet 01/01/1930 til 12/31/2029, skal du indtaste året med to cifre. Ellers skal du indtaste årstallet med fire cifre.  

Du kan også angive en dato som en ugedag efterfulgt af et ugenummer. Du kan også angive et år. F.eks. betyder Man25 eller man25 mandag i uge 25.  

I stedet for en bestemt dato kan du indtaste én af disse koder.  

|Kode|Resultat|  
|--------------|----------------|  
|d|Angiver dags dato (computerens systemdato).|  
|p|Angiver en regnskabsperiode, hvor p betyder den første regnskabsperiode, p2 betyder den anden regnskabsperiode osv. |
|a|Angiver den arbejdsdato, der er angivet i programmet. Hvis du vil ændre arbejdsdatoen, kan du se i [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md). Det er en fordel at anvende en arbejdsdato, hvis du har mange transaktioner at udføre på en dato, der ikke er dags dato.|
|u|Angiver, at datoen efter U er en ultimodato, f.eks. U123101.|  

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

## <a name="entering-combined-datetimes"></a>Indtaste kombineret dato/klokkeslæt

[!INCLUDE [datetimes](includes/datetimes.md)]

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

## <a name="setting-the-decimal-separator-used-by-numeric-keyboards"></a><a name="decimal"></a>Angive den decimalseparator, der bruges af numeriske tastaturer

Når du bruger decimalseparatortasten for numerisk tastatur til at indtaste data, bestemmes den faktiske decimalseparator, der er angivet i feltet, af områdeindstillingen for Business Central. Du angiver området i Business Central på siden **Mine indstillinger**.

Antag f.eks., at du bruger et numerisk tastatur, der bruger et punkt (.) som decimalseparatortast. Men du indtaster data for et regionalt sprog, der bruger et komma (**,**) til decimalseparatoren, f.eks. dansk (Danmark) eller fransk (Frankrig). Decimaler som "1,23" skal derfor angives som "1,23". I dette tilfælde kan du gå til siden **Mine indstillinger** og indstille **regionen** til det nationale målsprog, f.eks. **Dansk (Danmark)** eller **Fransk (Frankrig)**. Du kan finde flere oplysninger i [Ændre grundlæggende indstillinger](ui-change-basic-settings.md#region).

## <a name="see-also"></a>Se også

[Sortering af, søgning i og filtrering af lister](ui-enter-criteria-filters.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]