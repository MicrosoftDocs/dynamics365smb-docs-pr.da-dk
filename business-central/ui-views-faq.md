---
title: Ofte stillede spørgsmål om listevisninger
description: Detaljerede oplysninger om lagring af filtre som listevisninger.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 10/01/2020
ms.author: mikebc
ms.openlocfilehash: f39e20a9b4dae7e84c491d6d28308133f4691c05
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024510"
---
# <a name="list-views-faq"></a>Ofte stillede spørgsmål om listevisninger
I dette emne besvares spørgsmål, som vores erfarne brugere ofte stiller om, hvordan de kan arbejde med listevisninger og gemme filtre.  

### <a name="how-do-views-handle-expressions"></a>Hvordan håndteres udtryk i visninger?

Når du gemmer en visning, der omfatter filtre med udtryk, f.eks. datointervaller, operatorer, nøgleord eller filtertokens, gemmes udtrykket og ikke de resulterende værdier. Hvis du f.eks. gemmer en visning, hvor der filtreres på feltet **Oprettelsesdato** med udtrykket `-1W..today`, vil der altid blive fundet poster i forhold til den aktuelle dato, også hvis visningen åbnes næste måned.

### <a name="where-are-list-views-saved"></a>Hvor gemmes listevisninger?

På samme måde som når du skjuler et felt eller ændrer på rækkefølgen i din navigationsmenu, er listevisninger en del af brugertilpasningen og gemmes i databasen. Når du rydder alle tilpasninger på en liste, fjernes dine personlige visninger og yderligere tilpasninger, f.eks. ændret rækkefølge i visninger, også permanent. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).

### <a name="why-dont-i-have-a-save-icon"></a><a name="save"></a>Hvorfor har jeg ikke ikonet Gem?

Der er en par årsager til, at du ikke kan se menuen Gem ikon og indstillinger ved siden af visninger i filterruden.

En årsag kan være, at tilpasning ikke er aktiveret for din brugerrolle. I dette tilfælde har du stadig Access-systemvisninger, som er standarddele af siderne. Du kan ændre disse visninger, f. eks. ændre eller tilføje filtre. Du kan ikke gemme ændringerne. En anden årsag kan være, at den side, du ser på, er en side med en *projektmappe*-typeside&mdash;ikke en liste.

### <a name="on-which-page-types-can-i-use-list-views"></a>På hvilke sidetyper kan jeg bruge listevisninger?

Visninger er kun tilgængelige på liste- og regnearkssider.

### <a name="how-do-i-know-whether-im-on-list-type-page"></a>Hvordan ved jeg, om jeg er på listetypesiden?

Brug sideinspektion Tryk på Ctrl + Alt + F1 for at åbne side inspektion. Derefter i feltet **Side** skal man se efter ordet **Liste** i parentesen til sidst.

### <a name="are-views-also-available-on-other-form-factors"></a>Er visninger også tilgængelige på andre formfaktorer?

Ja. Alle de visninger, du gemmer i browseren eller skrivebordsappen, vil også være tilgængelige på din tablet eller smartphone. Du kan ikke ændre eller tilpasse visninger på mobilenheder.

### <a name="are-my-personal-views-always-accessible"></a>Er mine personlige visninger altid tilgængelige?

De samme visninger er tilgængelige på en listeside, hvis du åbner den fra navigationsmenuen, via vinduet **Fortæl mig** eller via et link med URL-adressen på listesiden. Visninger er ikke tilgængelige i listedele, opslag, eller når en listeside vises som en dialogboks.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>Hvordan vender jeg tilbage til de oprindelige filtre efter at have redigeret dem?

I bunden af filterruden skal du vælge handlingen **Nulstil filtre** for at fjerne filterændringer, du har foretaget i visningen, og vende tilbage til de oprindeligt filtrerede felter og filterkriterier.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>Hvad er forskellen på at skjule og fjerne visninger?

Hvis du fjerner en visning, slettes den permanent. Når du skjuler en visning, kan du midlertidigt skjule den i filterruden, men du kan vise den igen ved at vælge handlingen **Vis**.

### <a name="how-can-i-share-my-views-with-others"></a>Hvordan kan jeg dele mine visninger med andre?

[!INCLUDE[prod_short](includes/prod_short.md)] gør det ikke muligt at dele den nøjagtige listevisning. Men du kan dele dine aktuelle filtre, så andre brugere kan se en tilsvarende liste over poster. Du skal blot kopiere URL-adressen og dele den med dine kolleger i desktop-browseren. Ved deling af filtre kan det ikke garanteres, at modtageren får et sæt filtre, der er identisk med dem, du kan se i browseren.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>Kan jeg søge efter visninger i vinduet Fortæl mig?

Nej. I vinduet **Fortæl mig** vises kun søgeresultater for siden, men du kan nemt se din foretrukne visning ved at gå til siden.

### <a name="what-is-shared-layout"></a>Hvad er delt layout?

Alle visninger på en listeside har samme kolonneformat. Layoutet viser, hvilke kolonner der vises, deres rækkefølge, bredde, Frys rude og indstillinger for hurtig post. Tilpasningen af kolonnelayoutet påvirker også andre visninger, som deler det samme layout på listesiden.

Nogle systemvisninger kan have entydige layout af kolonnerne på listen. De kan f.eks. omarrangere kolonnerne, så kun de kolonner, der er mest relevante for den pågældende visning, er synlige. Du kan finde ud af, hvilke visninger der har entydige layout, ved at vælge ikonet ![Vis flere indstillinger](media/show-more-options-icon.png "Vis flere indstillinger") og se efter, at afkrydsningsfeltet **Delt layout** ikke er markeret. Som bruger kan du tilpasse kolonnelayoutet for en visning med unikt layout, uden at det påvirker andre visninger på listesiden. Kun udviklere kan definere et entydigt kolonneformat for en visning, der til at begynde med har et delt layout.

### <a name="what-does-the-show-system-filters-link-do"></a>Hvad gør linket Vis systemfiltre?

På nogle listesider viser filterruden **Vis systemfiltre** nederst i filterruden, når siden indeholder filtre, der er angivet af systemet. Disse Special filtre bruges typisk til at vise poster baseret på den aktuelle kontekst. Et eksempel kan være, når en Ordreoversigt skal filtreres for en bestemt kunde.

Systemfiltre indstilles af udviklere ved hjælp af filtergruppe 0. Tekniske oplysninger om systemfiltre finder du i [Filtergruppetyper](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method).

### <a name="i-see-multiple-views-on-my-page-but-i-didnt-create-them-where-did-they-come-from"></a>Der er flere visninger på min side, men jeg har ikke oprettet dem. Hvor kommer de fra?

De visninger, du kan se på en liste, er en kombination af dine personlige visninger og systemvisninger. Systemvisninger kan stamme fra forretningsprogrammet, fra udvidelser eller kan være rollespecifikke, hvis listen er tilpasset til din rolle.

### <a name="why-do-some-views-provide-fewer-options"></a>Hvorfor har nogle visninger færre indstillinger?

Nogle visninger giver kun mulighed for at gemme en kopi af visningen, mens det i andre tilfælde ikke er muligt at gemme ændringer af visningen. Den måde, visningen er oprettet på, bestemmer de indstillinger, der er tilgængelige for den pågældende visning. Visninger kan oprettes på flere måder:

- Personlige visninger, du har gemt
- Systemvisninger, som er en standarddel af forretningsprogrammet, eller som er tilføjet af udvidelser eller rollespecifikke visninger. I modsætning til personlige visninger kan du ikke gemme ændringer af filtre i den pågældende systemvisning.
- Ældre systemvisninger, som er en standarddel af forretningsprogrammet, men som er oprettet med ældre versioner af [!INCLUDE[prod_short](includes/prod_short.md)]. Disse visninger giver færre valgmuligheder. Du kan kun gemme dem som en ny visning og kan ikke skjule dem eller ændre rækkefølgen for dem. Ældre systemvisninger bliver udeladt i en fremtidig opdatering af [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="how-do-i-convert-legacy-system-views"></a>Hvordan kan jeg konvertere ældre systemvisninger?

Ældre systemvisninger er listevisninger, der er oprettet af udviklere i ældre versioner af [!INCLUDE[prod_short](includes/prod_short.md)] ved at placere dem på rollecentersiden. Disse visninger vises nu direkte på listesiden, men giver en forringet oplevelse og færre muligheder. Du kan konvertere en ældre systemvisning til en personlig visning, som kan tilpasses, ved at gemme den gamle visning som en ny visning. På samme måde kan administratorer vælge at konvertere rollespecifikke ældre systemvisninger ved at tilpasse brugerrollen og gemme den ældre visning som en ny rollespecifik visning.

Ældre systemvisninger bliver udeladt i en fremtidig opdatering af [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>Andre i min organisation skal bruge lignende listevisninger som standard. Hvad kan jeg gøre?

Arbejdet med personlige visninger er hurtigt og effektivt, men [!INCLUDE[prod_short](includes/prod_short.md)] indeholder yderligere værktøjer, der kan bruges til at definere listevisninger, som er nødvendige for bestemte brugerroller eller for alle brugere i organisationen.
 - Udviklere kan tilpasse miljøet og oprette listevisninger i udvidelser for alle brugere i organisationen.
 - Ikke-programmører, f.eks. administratorer eller afdelingsledere, kan oprette rollespecifikke listevisninger, når de tilpasser en rolle fra siden **Profiler (roller)**.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Jeg arbejder med flere sprog: Hvordan kan jeg oversætte navnet på visningen?

Når du gemmer en ny visning eller omdøber en eksisterende visning, skal du give visningen et navn, der giver mening. Navnet gemmes på det aktuelle sprog og vises også, når du eller andre brugere arbejder med [!INCLUDE[prod_short](includes/prod_short.md)] på andre sprog. Skift sprog for at angive oversatte visningsnavne på siden **Mine indstillinger**. Omdøb derefter visningen, som gemmer det oversatte navn på det nye sprog.

### <a name="do-views-with-expressions-work-in-all-languages"></a>Fungerer visninger med udtryk på alle sprog?

Udtryk, der kun bruger symboler som f.eks. `|` eller `..` betragtes som sikre for brugerne at anvende på alle sprog. Alle visninger med udtryk, der omfatter bogstaver, nøgleord eller filtertokens, fungerer kun for det sprog, som de er skrevet på.

### <a name="see-also"></a>Se også

[Gemme og tilpasse listevisninger](ui-views.md)  
[Finde funktioner og oplysninger](ui-search.md)  
[Sortering, søgning og filtrering](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]