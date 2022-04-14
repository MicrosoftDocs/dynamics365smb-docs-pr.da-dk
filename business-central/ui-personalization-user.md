---
title: Personlige sider (indeholder video)
description: Få at vide, hvordan du kan tilpasse brugergrænsefladen og tilpasser dit arbejdsområde, så det passer til din måde at arbejde på i Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: a862cb514145d50d1a86816bbd3758055b41a872
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512728"
---
# <a name="personalize-your-workspace"></a>Tilpasse dit arbejdsområde
Du kan tilpasse dit arbejdsområde, så det passer til dit arbejde og dine præferencer ved at ændre sidernes layout, så de kun viser de oplysninger, du har brug for, hvor du har brug for det. De tilpasningsændringer, du foretager, påvirker kun det, du ser, ikke hvad andre brugere ser.

Du kan tilpasse alle typer sider, herunder siden Rollecenter. Du kan finde flere oplysninger om rollecentre i [Rollecenter](ui-change-basic-settings.md#role-center).

Afhængigt af sidens type og det siden indeholder, kan du udføre forskellige ændringer som at flytte eller skjule felter, kolonner, handlinger, hele dele og tilføje nye felter. De fleste tilpasninger skal foretages ved først at aktivere banneret **Tilpas**, men meget enkle justeringer, f.eks. af kolonnebredden, kan udføres med det samme på enhver liste.

> [!NOTE]
> Administratorer kan udføre samme layoutændringer, efterhånden som brugerne kan tilpasse arbejdsområdet til en profil, som tildeles til flere brugere. Du kan finde flere oplysninger i [Tilpasse sider til roller](ui-personalization-manage.md).<br /><br />
Administratorer kan også tilsidesætte eller deaktivere brugernes tilpasninger, og de kan også definere, hvilke funktioner brugerne skal kunne se i alle eller bestemte regnskaber. Du kan finde flere oplysninger i [Tilpasse Business Central](ui-customizing-overview.md).

## <a name="video-overview"></a>Videooversigt
I følgende video vises nogle metoder til at tilpasse dit rollecenter.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## <a name="to-change-the-width-of-a-column"></a>Sådan ændres kolonnebredden
Du kan nemt ændre kolonnestørrelsen i en liste ved at trække i kanten mellem to kolonner mod venstre eller højre.
1. Markér og træk i kanten mellem to kolonner i oversigtshovedet.
2. Du kan også dobbeltklikke på kanten mellem to kolonner for automatisk at tilpasse kolonnebredden. Dette indstiller bredden til den optimale læsestørrelse.

Som ved andre tilpasninger gemmes de ændringer, du foretager af kolonnebredden, på din konto og vises, uanset hvilken enhed du logger på.

## <a name="to-start-personalizing-a-page-through-the-personalizing-banner"></a>Du kan begynde at tilpasse en side via banneret **Tilpasning**
1. Åbn en side, du vil tilpasse.
2. I øverste højre hjørne vælges ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") ikon, og derefter handlingen **Tilpas**.

    Banneret **Tilpasning** vises øverst for at angive, at du kan begynde at foretage ændringer.

    > [!NOTE]
    > Hvis du vil navigere under tilpasningen, skal du bruge Ctrl + klikke på en handling, hvis den er fremhævet af pilespidsen.

    Hvis du får vist ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst") eller ![Tilpasning spærret](media/personalization-blocked-icon.png "Tilpasning blokeret") på banneret, kan du ikke tilpasse siden. Du kan finde flere detaljer i [Hvorfor er en side låst mod tilpasning](ui-personalization-locked.md).

3. Hvis du vil tilføje et felt, skal du vælge handlingen **+ Felt**.
4. Træk og slip et felt på den ønskede placering på siden i sideruden **Føj felt til side**.
5. Hvis du vil ændre et brugergrænsefladeelement, skal du pege på elementet, f.eks. en handling, et felt eller en del. Elementet fremhæves straks med en pilespids eller kant.
6. Vælg elementet, og vælg derefter enten **Flyt**, **Fjern**, **Skjul**, **Vis**, **Vis under "Vis flere"**, **Vis, når skjult**, **Vis altid**, **Angiv/Ryd låst rude** eller **Medtag/Udeluk fra genvej**, afhængigt af typen og tilstanden for brugergrænsefladeelementet. Du kan finde flere oplysninger i [Hvad kan du tilpasse](#What).
7. Når du er færdig med at ændre layoutet for en eller flere sider, skal du vælge knappen **Udført** på banneret **Tilpas**.

## <a name="what-you-can-personalize"></a><a name="What"></a>Hvad kan du tilpasse

|Hvad vil du foretage dig?|Hvordan du gør det|Kommentarer|
|----|------------|-------|
|Flytte noget, f.eks. et felt, en kolonne i listen, et felt, en handling eller en del|Peg et vilkårligt sted i det, du vil flytte, og træk det til den nye placering. Placeringen angives med enten en fed vandret eller lodret linje.<br /><br />![Kan ikke flytte her-ikon](media/personalization-cannot-move-here.png "Tilpasningstilstand – kan ikke flytte her-ikon") angiver, at du ikke kan flytte elementet til den valgte placering.|Dele er underinddelinger eller områder på en side, der indeholder elementer, f.eks. flere felter, en anden side, et diagram eller felter.<br /><br />Du kan finde flere oplysninger om tilpasning af handlinger i [Tilpasning af handlinger](ui-personalization-user.md#Actions). |
|Skjule noget, f.eks. et felt, en kolonne i listen, et felt, en handling eller en del.|Vælg pilespidsen, vælg <b>Skjul</b>.|Elementet vises nedtonet, når du er i tilpasningstilstand. Hvis det felt, du skjuler, også vises i overskriften til oversigtspanelet, når oversigtspanelet er skjult, vises feltet ikke længere der.|
|Vise skjulte handlinger og dele.|For et nedtonet (skjult) element skal du vælge pilespidsen og derefter vælge <b>Vis</b>.|Det skjulte element er synligt igen.|
|Tilføje et felt eller en kolonne.|Vælg handlingen <b>+ Felt</b> i banneret <b>Tilpas</b>.<br /></br>Ruden <b>Tilføj felt til side</b> vises til højre. Den viser de felter, du kan føje til siden.<br /><br />Hvis du vil tilføje et felt, skal du trække det fra ruden til den ønskede placering. Placeringen angives med enten en fed vandret eller lodret linje.|Hver side indeholder et foruddefineret sæt felter, der kan vises. Brug denne fremgangsmåde til at tilføje felter eller kolonner, der ikke tidligere er vist, eller til at vise felter, du har skjult.|
|Vise et felt i overskriften til et oversigtspanel, når det er skjult.|Vælg pilespidsen, og vælg derefter <b>Vis, når skjult</b>. <br /> <br />Hvis du ikke kan se denne indstilling, er den allerede angivet. Hvis det er tilfældet, og feltet ikke skal vises i overskriften til oversigtspanelet, skal du vælge <b>Vis altid</b>.|*Oversigtspanel* er det udtryk, der bruges om en gruppe felter, der vises under en fælles overskrift. Brug indstillingen <b>Vis, når skjult</b> for at få vist de vigtigste felter. Hvis du vælger et felt i overskriften, åbnes oversigtspanelet og fokuserer på det valgte felt.<br /><br />Denne indstilling kan kun anvendes, hvis en side har mere end et oversigtspanel. Hvis der kun er ét oversigtspanel, kan det ikke skjules, så indstiillingen <b>Vis, når skjult</b> er ikke tilgængelig.|
|Angiv, at et felt kun skal vises, når du vælger **Vis mere**.|Vælg pilespidsen, og vælg derefter <b>Vis under "Vis flere"</b>. <br /> <br />Hvis du ikke kan se indstillingen <b>Vis under "Vis flere"</b>, er den allerede angivet. I så fald skal du vælge <b>Vis altid</b> for at få vist et felt hele tiden, og ikke kun når du vælger **Vis mere**.||
|Flytte den fastlåste rude i en liste til en anden kolonne. |Vælg pilespidsen for den kolonne, som du vil bruge som den sidste kolonne i den fastlåste rude, og vælg derefter <b>Angiv låst rude</b>.<br /><br/>Hvis du vil flytte den fastlåste rude tilbage til den oprindelige tiltænkte placering, skal du vælge pilespidsen for den aktuelle kolonne i den låste rude og vælge <b>Ryd låst rude</b>. Bemærk: Du kan ikke fjerne denne låste rude.|Den fastlåste rude angiver de kolonner, der altid vises i venstre side, selv når du ruller vandret.|  
|Spring et felt over, når du trykker på Enter.|Vælg pilespidsen ved siden af feltet eller kolonneoverskriften på en liste, og vælg **Udeluk fra genvej**. <br /><br /> Hvis du ikke kan se denne indstilling, er det allerede angivet, at feltet skal springes over. I det tilfælde skal du stoppe med at springe feltet over og vælge **Medtag i genvej**. |Se [Fremskynde dataindtastning ved hjælp af genveje](ui-enter-data.md#QuickEntry)|
|Omarrangere og fjerne visninger, der repræsenterer filtrerede lister.|Vælg pilespidsen ud for en visning, og vælg derefter **Flyt**, **Fjern** eller **Skjul**.|Se [Gemme og tilpasse listevisninger](ui-views.md)|  
|Føje en ny handling til en side eller en rapport i dit rollecenter.|Vælg bogmærkeikonet på rapportanmodningssiden eller i vinduet Fortæl mig på målsiden.|Se [Bogmærke en side eller en rapport i rollecenteret](ui-bookmarks.md)|
|Starte altid en liste som udvidet eller skjult|Vælg knappen Udvid alle eller Skjul alle øverst til venstre på listen, eller vælg funktionen Udvid alle eller Skjul alle i menuen til den første kolonne. |Gælder for hierarkilister, der kan skjules|

## <a name="personalizing-actions"></a><a name="Actions"></a>Tilpasning af handlinger

Tilpasning gør det muligt at bestemme, hvilke handlinger der skal vises på navigations- handlingslinjerne samt i rollecentre, og hvor de skal vises. Du kan vise, skjule eller flytte individuelle handlinger eller handlingsgrupper. Tilpasning af navigations- og handlingslinjerne foretages stort set på samme måde som med andre elementer i brugergrænsefladen. Men hvad du kan gøre med en handling eller en gruppe, afhænger af hvor handlingen eller gruppen er placeret. Den bedste måde at finde ud af det på, er ved at vælge tilpasningstilstand og derefter følge pilespidserne.

Der er et par ord, du skal kende for at få en bedre forståelse af handlingstilpasning: *handlingsgruppe* og *fremhævet kategori*.  

En *handlingsgruppe* er et element, som kan vise andre handlinger eller grupper, når det udvides. For eksempel på siden **Salgsordrer** er den **Funktioner**-handling, der vises, når du vælger handlingen **Handlinger** en handlingsgruppe.

En *fremhævet kategori* er en handlingsgruppe, der vises foran den lodrette linje `|` på handlingslinjen. Kategorierne omfatter typisk de mest almindeligt anvendte handlinger, så du hurtigt kan finde dem. For eksempel er handlingerne **Ordre**, **Frigivelse** og **Bogføring** på siden **Salgsordrer** fremhævede kategorier.

> [!NOTE]
> Du kan ikke tilpasse handlingslinjen, der vises i dele på siden (f.eks. salgslinjedelen på siden **Salgsordre**).

### <a name="to-remove-hide-and-show-actions-and-action-groups"></a>Sådan fjernes, skjules og vises handlinger og handlingsgrupper
Når du vil vise eller skjule en handling, definerer indstillingerne under pilespidsen, hvad du kan gøre, afhængigt af handlingstilstanden.
1. Vælge pilespidsen for en handling eller en handlingsgruppe.
2. Vælg en af følgende indstillinger:

|Indstilling|Det gør den|
|------|------------
|**Fjern**|Denne indstilling vises, hvis den valgte handling også er vist et andet sted på navigations- eller handlingslinjen. Hvis du vælger denne indstilling, slettes handlingen fra den valgte placering, så den ikke længere vises. Handlingen eller handlingsgruppen forbliver på de andre placeringer. |
|**Skjul**|Denne indstilling vises, hvis handlingen eller handlingsgruppen ikke er placeret andre steder på navigations- eller handlingslinjen. Som det er tilfældet med **Fjern**, forsvinder handlingen eller handlingsgruppen fra navigations- eller handlingslinjen, hvis du vælger denne indstilling. Men i tilpasningstilstand vises handlingen eller handlingsgruppen stadig på den aktuelle placering, bortset fra at den er nedtonet.|
|**Vis**|Denne indstilling vises, hvis handlingen eller handlingsgruppen tidligere har været skjult (nedtonet). Vælges denne indstilling, vises handlingen eller handlingsgruppen på navigations- eller handlingslinjen.|

### <a name="to-move-actions-and-action-groups"></a>Sådan flyttes handlinger og handlingsgrupper
Hvor du kan slippe handlinger eller handlingsgrupper, er angivet af en vandret linje mellem to handlinger eller en kant omkring en handlingsgruppe. Der findes følgende begrænsninger:

- Du kan flytte enkelte handlinger til de fremhævede kategorier, men du kan ikke ændre rækkefølgen af handlinger i kategorien.
- Du kan ikke flytte en handlingsgruppe til en fremhævet kategori.

1. Hvis du vil flytte en handling eller handlingsgruppe, skal du trække og slippe den på den ønskede placering på samme måde som med feltet og kolonner.
2. Hvis du vil flytte en handling eller handlingsgruppe til en anden handlingsgruppe, der er tom, skal du trække handlingen eller handlingsgruppen og slippe den i feltet **Slip en handling her**.


## <a name="personalizing-parts"></a><a name="Parts"></a>Tilpasning af dele

Dele er områder på en side, der typisk består af flere felter, diagrammer eller andet indhold, og som kan identificeres med en farvet ramme, når der sættes fokus på delen. Et rollecenters startskærm har f.eks. flere dele. På grund af den veldefinerede grænse kan du tilpasse hele delen og dens indhold.

- Træk og slip en del til den ønskede placering for at flytte den. En farvet linje angiver gyldige placeringer på skærmen. Faktabokse kan f.eks. kun flyttes til siden af andre faktabokse i faktaboksruden.
- Du kan skjule en del ved at vælge indstillingen **Skjul** under pilespidsen.
- Når du begynder at tilpasse eller navigere til en ny side, vil alle dele, der aktuelt er skjult, blive vist på siden med karakteristiske detaljer, der angiver, at de er skjulte. Du kan vise denne del igen ved at vælge indstillingen **Vis** under pilespidsen.

Du kan fjerne alle de tilpasningsændringer, du har foretaget i en enkelt del, ved at vælge indstillingen **Fjern tilpasning** under delens pilespids. Hvis du fjerner markering af en del, påvirker det kun, om en del er ændret, ikke placeringen eller synligheden af delen på siden.  


## <a name="to-clear-personalization"></a>Sådan fjernes tilpasning
På et tidspunkt ønsker du måske at fjerne nogle eller alle de tilpasningsændringer, du har foretaget på en side i tidens løb.

1. Vælg handlingen **Fjern tilpasning** på banneret **Tilpas**.
2. Vælg en af følgende indstillinger. Vær opmærksom på, at fjernelse af tilpasning ikke kan fortrydes.

|Indstilling|Det gør den|
|------|------------
|**Kun menuen Navigation**|Fjerner alle tilpasningsændringer, du har foretaget i navigationsmenuen, som er delt på tværs af rollecenteret og andre sider. Dette omfatter alle nye handlinger, der er tilføjet som bogmærker, og eventuelle ændringer af links og grupper i menuen.|  
|**Kun handlinger**|Fjerner alle de tilpasningsændringer, du nogensinde har foretaget på navigations- eller handlingslinjerne på siden.|
|**Kun felter, kolonner og dele**|Fjerner alle de tilpasningsændringer, du nogensinde har foretaget for siden undtagen dem på navigations- eller handlingslinjen. Dette omfatter ændringer af felter, kolonner, dele og fliser. |
|**Alle**|Fjerner alle de tilpasningsændringer, du har foretaget på siden, så siden får sit oprindelige udseende. Dette omfatter ændringer af navigations- og handlingslinjer, felter, kolonner, dele og fliser.|

## <a name="additional-points-of-interest"></a>Flere punkter af særlig interesse
Her er nogle forslag, der kan hjælpe dig med at opnå en bedre forståelse.

- Når du ændrer en kortside, som du åbner fra en liste, træder ændringerne træde i kraft på alle poster, der åbnes fra denne liste. Lad os antage, at du åbner en bestemt kunde fra listen Debitorer og derefter tilpasser siden ved at tilføje et felt. Når du åbner andre debitorer på listen, vises det felt, du har tilføjet, også.
- Ændringer, du foretager, træder i kraft på alle dine rollecentre. Hvis du f.eks. foretager en ændring på listen Debitorer, når rollecenteret er angivet til virksomhedsleder, vises også ændringen i også på siden **Debitorer**, når Rollecenter er indstillet til Salgsordrebehandler.
- Ændringer af en side i en rude træder i kraft på siden, overalt hvor den vises.  
- Du kan kun tilføje felter og kolonner fra en foruddefineret liste, der er baseret på siden. Du kan ikke oprette nye felter og kolonner.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Tilpasse sider til profiler](ui-personalization-manage.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
