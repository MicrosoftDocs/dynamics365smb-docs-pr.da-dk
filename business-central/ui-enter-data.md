---
title: Sådan angives data i Business Central | Microsoft Docs
description: Få mere at vide om generelle funktioner, der hjælper dig med at indtaste data i felter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/27/2020
ms.author: sgroespe
ms.openlocfilehash: 6a57af4a29e2b355dfe3f261a5d83fade992551d
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992074"
---
# <a name="entering-data"></a>Angivelse af data

Der er mange generelle funktioner, der hjælper dig med at indtaste data data lettere, hurtigere og mere nøjagtigt. De generelle funktioner til indtastning af data er beskrevet i denne artikel.  

Eksemplerne i denne artikel bruger demodata.

## <a name="keyboard-shortcuts"></a>Tastaturgenveje

Der er adskillige tastaturgenveje, du kan bruge, når du vil arbejde uden mus, og som gør dataindtastning hurtigere, især i forbindelse med store poster og gentagne indtastningsopgaver.

Du kan finde flere oplysninger om genveje i [Tastaturgenveje](keyboard-shortcuts.md). Nogle af genvejene er beskrevet i denne artikel.

## <a name="QuickEntry"></a>Fremskynde dataindtastning ved hjælp af genveje

Genvej er en funktion, der er designet til dataindtastning med brug af tastatur. Genvej fungerer på felter (f.eks. på kortider) og i lister (rækker og kolonner). Det er nyttige, når du udfører gentagne indtastningsopgaver, der kræver oprettelse af flere poster i rækkefølge, f.eks. en kørsel med salgsordrer eller registrering af nye varer.

Du er muligvis allerede fortrolig med brugen af tabulatortasten til at navigere fra ét felt på en side til næste redigerbare felt. En ulempe ved at bruge tabulatortasten er, at den altid går til næste felt i rækkefølge. <!-- even if the field is non-editable or seldom filled it in.-->Genvej gør det muligt at ændre denne fremgangsmåde. Med genvej kan du bruge Enter-tasten til udelukkende at navigere blandt de felter, du er interesseret i, og overspringe ikke-redigerbare felter og felter, som du normalt ikke udfylder. Du har muligvis allerede bemærket denne funktionsmåde på nogle sider. Det skyldes, at programmet allerede angiver, hvilke felter der skal medtages, når du trykker på Enter, og hvilke der skal springes over. Du kan tilpasse genvej ved at tilpasse dit arbejdsområde og optimere den måde, du indtaster data på hver side.

### <a name="how-quick-entry-works"></a>Sådan fungerer genvej

Hvert felt kan markeres som enten *medtaget i genvej* eller *udelukket fra genvej*. Felter, der indgår i genvej, medtages i stien, når du trykker på Enter. Felter, der er udelukket fra genvej, medtages ikke.

Når du er færdig med at angive data i et felt, du blot trykke på Enter for at bekræfte ændringerne og gå til næste felt. Hvis du vil vende retningen og gå til det forrige felt, skal du trykke på Skift+Enter. Du kan finde flere oplysninger om genveje i [Genveje for felter](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Tip
Følgende indeholder nyttige oplysninger om brugen af genvej.

- Den findes i alle redigerbare felter.
- Den kan også bruges på tværs af kolonner og rækker.
- Den forhindrer ikke adgang til andre elementer på en side, f.eks. handlinger. De er stadig tilgængelige ved hjælp af tabulatortasten og Skift+Tab.  
- Oversigtspanelerne behøver ikke at blive udvidet for at få genvej til at fungere. Hvis næste genvejsfelt er placeret i et skjult oversigtspanel, udvides det pågældende oversigtspanel automatisk og fokuserer på det angivne felt.
- Genvej fungerer, uanset om felter skal udfyldes. Det er derfor en god ide at sikre, at obligatoriske felter er medtaget i genvej.
- Som standard medtages de fleste felter automatisk i genvej. Så til at starte med skal du derfor sandsynligvis udelukke felter fra genvej.

### <a name="to-change-quick-entry-fields"></a>Sådan ændres genvejsfelter

Hvis du vil ændre, hvilke felter der medtages i eller udelukkes fra genvej på en side, kan du bruge tilpasning.

1. Start tilpasning ved at vælge ikonet ![Indstillinger](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") og derefter handlingen **Tilpas**.
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

## <a name="copying-and-pasting-faq-fields-and-lines"></a>Ofte stillede spørgsmål om kopiering og indsætning af felter og linjer

Du kan kopiere en eller flere rækker fra en liste eller et enkelt felt på en side og derefter indsætte det, du har kopieret på den samme side, en anden side eller et eksternt dokument (som Microsoft Excel og e-mails i Outlook). Kort sagt, når du vil kopiere, skal du trykke på CTRL + C (cmd + C i macOS) på tastaturet. Når du vil indsætte, skal du trykke på CTRL + V (cmd + V i macOS).

Hvis du på en liste vil kopiere feltet i den samme kolonne i rækken ovenfor og indsætte det i den aktuelle række, skal du bare trykke på F8.

Du kan finde flere oplysninger i [Ofte stillede spørgsmål om kopiering og indsætning](ui-copy-paste.md).

## <a name="filtering-line-items"></a>Filtrere linjevarer

Du starter filtrering ved at vælge ![Ikonet Filterrude](media/open-filter-pane-icon.png "Ikonet Filterrude") øverst på listen eller ved at trykke på Skift+F3 for at åbne filterruden. Du arbejder med filterruden, på samme måde som du arbejder med andre lister. Du kan finde flere oplysninger i [Filtrering](ui-enter-criteria-filters.md#Filtering).

Filtrering er især nyttig, når du får vist og analyserer længere dokumenter. Antag f.eks., at du åbner en bogført salgsfaktura og filtrerer linjevarerne for at få vist alle linjevarer med en individuel rabat over 5 % eller filtrerer for udelukkende at få vist cykeltilbehør med 'pro' i navnet.

## <a name="Focus"></a>Fokusere på linjevarer

Når du arbejder med dokumenter, der indeholder en del af en linjevarepost, f.eks. en salgsordre eller fakturaside, kan du ændre visningen, så der kun fokuseres på linjevarerne. Derefter udvides delen med linjevarer, så den fylder næsten hele arbejdsområdet, og så andre dele af siden bortset fra handlingsområdet øverst skjules. Det giver dig et bedre overblik over linjevarerne og giver mere plads til at arbejde med dem.

Dette er især nyttigt, når du arbejder med store lister med linjevarer, og når der ønskes hurtig dataindtastning. En anden fordel er, at det også indeholder avancerede filterfunktioner, som på andre lister, så det bliver endnu nemmere at gennemse og søge gennem linjevarer.

### <a name="switching-the-focus-on-and-off"></a>Slå fokus til og fra

Når du vil fokusere på linjevarer, skal du markeret et vilkårligt sted i delen med linjevarer og derefter vælge ![Ikonet Fokustilstand](media/focus-mode.png "Ikonet Fokustilstand") i øverste højre hjørne eller trykke på Ctrl+Skift+F12.

For at vende tilbage til normal visning skal du vælge ![Ikonet Fokustilstand](media/focus-mode.png "Ikonet Fokustilstand") eller trykke på Ctrl+Skift+F12 igen.

## <a name="multitasking-across-multiple-pages"></a>Multitasking på tværs af flere sider
Når du arbejder på flere opgaver ad gangen eller administrerer afbrydelser af den aktuelle opgave, f.eks. besvarer et indgående opkald, kan du åbne en kort- eller dokumentside i et nyt vindue. Det giver dig mulighed for at holde et vindue åbent for en igangværende opgave, mens du starter eller udfører en anden opgave i et eller flere andre vinduer.

Hvis du vil åbne det aktuelle kort eller dokument i et nyt vindue, skal du vælge ![Åbn nyt vindue](media/open-new-window-icon.png "Ikonet Åbn i nyt vindue") i øverste højre hjørne eller trykke på Alt+Skift+W.

> [!NOTE]
> Når du åbner andre sider fra et kort eller et dokument, der er åbnet i et nyt vindue, åbnes disse sider i et nyt vindue, selvom du ikke vælger ![Åbn nyt vindue](media/open-new-window-icon.png "Ikonet Åbn i nyt vindue").

> [!NOTE]
> Hvis du arbejder i Safari-browseren, kan blokering af et pop op-vindue medføre, at det nye vindue ikke åbnes. Hvis det er tilfældet, skal du angive produktets URL-adresse som et tilladt websted. Du kan finde flere oplysninger under [Ændre indstillinger i Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Det samme kan forekomme i andre browsere, f.eks. Firefox. Du kan finde flere oplysninger under [Indstillinger for blokering af pop op-vinduer i Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400).  

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
> Måden, du angiver datoer og klokkeslæt på, afhænger af dine indstillinger i **Område**. Du kan finde flere oplysninger under [Ændre grundlæggende indstillinger](ui-change-basic-settings.md).  

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
|p|Dette angiver en regnskabsperiode, hvor p betyder den første regnskabsperiode, p2 betyder den anden regnskabsperiode osv. |
|a|Dette angiver den arbejdsdato, der er angivet i programmet. Hvis du vil ændre arbejdsdatoen, kan du se i [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md). Det er en fordel at anvende en arbejdsdato, hvis du har mange transaktioner at udføre på en dato, der ikke er dags dato.|
|u|Dette angiver, at datoen efter U er en ultimodato, f.eks. U120131.|  

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
|`131202` 132455|13-12-02 13:24:55|  
|1-12-02 10|01-12-02 10:00:00|  
|1.12.02 5|01-12-02 05:00:00|  
|1.12.02|01-12-02 00:00:00|  
|11 12|11-løbende måned-løbende år 12:00:00|  
|1112 12|11-12-aktuelt år 12:00:00|  
|d eller dags dato|dags dato 00:00:00|  
|d tid|dags dato aktuelt klokkeslæt|  
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

## <a name="see-also"></a>Se også  
 [Sortering af, søgning i og filtrering af lister](ui-enter-criteria-filters.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
