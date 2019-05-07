---
title: Tilpasse sider | Microsoft Docs
description: Få at vide, hvordan du kan tilpasse brugergrænsefladen, så den passer til din måde at arbejde på i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 16f334548d9831507970a1b74ba5fa1716611380
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "922084"
---
# <a name="personalizing-your-workspace"></a>Tilpasse dit arbejdsområde

Du kan *tilpasse*, dit arbejdsområde, så det passer til dit arbejde og dine præferencer ved at ændre sidernes layout, så de kun viser de oplysninger, du har brug for, hvor du har brug for det. De tilpasningsændringer, du foretager, påvirker kun det, du ser, ikke hvad andre brugere ser.

Afhængigt af sidens type og det siden indeholder, kan du gøre forskellige ting som at flytte eller skjule felter, kolonner og handlinger, flytte og skjule hele dele og meget mere.
<!--
-   Add, move, and remove fields.
-   Add, move, and remove columns in a list.
-   Change the freeze pane of columns in a list. The freeze pane locks one or more columns to the left side of a list so that are always present, even when you scroll horizontally.
-   Adjust the width of columns in a list.
-   Move and remove Cues (tiles).
-   Move and remove parts. Parts are subdivisions or areas on a page that contain things like multiple fields, another page, a chart, or tiles.

-->
> [!NOTE]
> Ud over hvad brugere kan tilpasse, kan administratorer og superbrugere tilsidesætte brugernes tilpasning og definere, hvilke funktioner der skal være tilgængelige i alle eller bestemte regnskaber. Du kan finde flere oplysninger under [Tilpasse Business Central](ui-customizing-overview.md).

## <a name="to-personalize-a-page"></a>Sådan tilpasses en side

1. I øverste højre hjørne skal du vælge ikonet ![Indstillinger](media/ui-experience/settings_icon_small.png "ikonet Indstillinger til rollecenter") og derefter vælge **Tilpas**.

    Banneret **Tilpasning** vises øverst for at angive, at du kan begynde at foretage ændringer.

    ![Tilpasningstilstand](media/ui_personalize_mode_small.png "Tilpasningstilstand")

2. Gå til en side, du vil tilpasse.

    Hvis du får vist ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst") eller ![Tilpasning spærret](media/personalization-blocked-icon.png "Tilpasning spærret") på banneret, kan du ikke tilpasse siden. Du kan finde flere oplysninger i [Hvorfor kan jeg ikke tilpasse en side](ui-personalization-locked.md).

3. Peg på et område, som du vil tilpasse, f.eks. et felt eller kolonneoverskriften på en liste. Alt, du kan tilpasse, fremhæves straks med en pilespids eller ramme. Se [næste sektion](#What) med oplysninger om, hvad du kan gøre.

4. Du kan fortsætte med at foretage ændringer på samme side eller åbne en anden side. Ændringerne gemmes automatisk, når du foretager dem. Når du er færdig, skal du i banneret **Tilpasning** vælge **Færdig**.

## <a name="What"></a>Hvad kan du tilpasse

|Hvad vil du foretage dig?|Hvordan du gør det|Kommentarer|
|----|------------|-------|
|Flytte noget, f.eks. et felt, en kolonne i listen, et felt, en handling eller en del|Peg et vilkårligt sted i det, du vil flytte, og træk det til den nye placering. Placeringen angives med enten en fed vandret eller lodret linje.<br /><br />![Kan ikke flytte her-ikon](media/personalization-cannot-move-here.png "Tilpasningstilstand – kan ikke flytte her-ikon"), betyder det, at du ikke kan flytte elementet til den valgte placering.|Dele er underinddelinger eller områder på en side, der indeholder elementer, f.eks. flere felter, en anden side, et diagram eller felter.<br /><br />Der er flere oplysninger om handlingstilpasning i [næste sektion](ui-personalization-user.md#Actions). |
|Skjule noget, f.eks. et felt, en kolonne i listen, et felt eller en del.|Vælg pilespidsen, og vælg <b>Skjul</b>.|Hvis det felt, du skjuler, også er vist i overskriften til oversigtspanelet, når oversigtspanelet er skjult, vises feltet ikke længere der.|
|Tilføje et felt eller en kolonne.|I banneret <b>Tilpas</b> skal du vælge <b>Flere</b>, og derefter vælge <b>Felt</b>.<br /></br>Ruden <b>Tilføj felt til side</b> vises til højre. Den viser de felter, du kan føje til siden.<br /><br />Hvis du vil tilføje et felt, skal du trække det fra ruden til den ønskede placering. Placeringen angives med enten en fed vandret eller lodret linje.|Hver side indeholder et foruddefineret sæt felter, der kan vises. Brug denne fremgangsmåde til at tilføje felter eller kolonner, der ikke tidligere er vist, eller til at vise felter, du har skjult.|
|Vise et felt i overskriften til et oversigtspanel, når oversigtspanelet er skjult.|Vælg pilespidsen, og vælg <b>Vis, når skjult</b>. <br /> <br />Hvis du ikke kan se denne indstilling, er den allerede angivet. Hvis det er tilfældet, og feltet ikke skal vises i overskriften til oversigtspanelet, skal du vælge <b>Vis altid</b>.|*Oversigtspanel* er det udtryk, der bruges om en gruppe felter, der vises under en fælles overskrift. Brug indstillingen <b>Vis, når skjult</b> for at få vist de vigtigste felter. Hvis du vælger et felt i overskriften, åbnes oversigtspanelet og fokuserer på det valgte felt.<br /><br />Denne indstilling kan kun anvendes, hvis en side har mere end et oversigtspanel. Hvis der kun er ét oversigtspanel, kan det ikke skjules, så indstiillingen <b>Vis, når skjult</b> er ikke tilgængelig.|
|Angiv, at et felt kun skal vises, når du vælger **Vis mere**.|Vælg pilespidsen, og vælg <b>Vis under "Vis flere"</b>. <br /> <br />Hvis du ikke kan se indstillingen <b>Vis under "Vis flere"</b>, er den allerede angivet. I så fald skal du vælge <b>Vis altid</b> for at få vist et felt hele tiden, og ikke kun når du vælger **Vis mere**.||
|Flytte den fastlåste rude i en liste til en anden kolonne. |Vælg pilespidsen for den kolonne, som du vil bruge som den sidste kolonne i den fastlåste rude, og vælg derefter <b>Angiv låst rude</b>.<br /><br/>Hvis du vil flytte den fastlåste rude tilbage til den oprindelige tiltænkte placering, skal du vælge pilespidsen for den aktuelle kolonne i den låste rude og vælge <b>Ryd låst rude</b>. Bemærk: Du kan ikke fjerne denne låste rude.|Den fastlåste rude angiver de kolonner, der altid vises i venstre side, selv når du ruller vandret.|  
|Ændre kolonnebredden.|Træk i kolonnes højre ramme i rækken med kolonneoverskriften. <br /><br />Dobbeltklik på højre ramme for at maksimere kolonnebredden, så den passer til den længste tekstlinje i kolonnen.||
|Spring et felt over, når du trykker på Enter.|Vælg pilespidsen ved siden af feltet eller kolonneoverskriften på en liste, og vælg **Udeluk fra genvej**. <br /><br /> Hvis du ikke kan se denne indstilling, er det allerede angivet, at feltet skal springes over. I det tilfælde skal du stoppe med at springe feltet over og vælge **Medtag i genvej**. |Se [Fremskynde dataindtastning ved hjælp af genveje](ui-enter-data.md#QuickEntry)|

## <a name="Actions"></a>Tilpasning af handlinger

Du kan tilpasse handlingslinjen, der er placeret øverst på siden som indikeret af det markerede område i nedenstående illustration.

![Tilpasse handlingslinje](media/personalize-action-bar.png "Tilpasse handlingslinje")

Tilpasning gør det muligt at bestemme, hvilke handlinger der skal vises på handlingslinjen, og hvor de skal vises. Du kan vise, skjule eller flytte individuelle handlinger eller handlingsgrupper. Tilpasning af handlingslinjen foretages stort set på samme måde som med andre elementer i arbejdsområdet. Men nøjagtigt hvad du kan gøre med en handling eller en gruppe, afhænger af hvor handlingen eller gruppen er placeret på handlingslinjen. Den bedste måde at finde ud af det på, er blot at afprøve tingene og følge vejledningen på skærmen. I følgende afsnit beskrives nogle af de små forskelle ved tilpasning af handlingslinjen.

### <a name="action-bar-overview"></a>Oversigt over handlingslinje

Der er et par ord, du skal kende for at få en bedre forståelse af handlingstilpasning: *handlingsgruppe* og *fremhævet kategori*.  

En *handlingsgruppe* er varer, som udvides til at vise andre handlinger eller grupper. I følgende illustration er **Bogføring** f.eks. en handlingsgruppe.

En *fremhævet kategori* er en handlingsgruppe, der vises mellem to lodrettte linjer `|` på handlingslinjen. Kategorierne omfatter typisk de mest almindeligt anvendte handlinger, så du hurtigt kan finde dem. I følgende illustration er **Version**, **Bogføring**, **Faktura** og **Naviger** f.eks. fremhævede kategorier.

![Tilpasse handlingslinjegruppe](media/personalize-action-bar-group-clip.png "Tilpasse handlingslinjegruppe ")

### <a name="to-remove-hide-and-show-actions-and-groups"></a>Sådan fjernes, skjules og vises handlinger og grupper

Når du vil vise eller skjule en handling eller handlingsgruppe, skal du markere den og derefter vælge en af følgende indstillinger:

|Indstilling|Det gør den|
|------|------------
|**Fjern**|Denne indstilling vises, hvis den valgte handling også er vist et andet sted på handlingslinjen. Hvis du vælger denne indstilling, slettes handlingen fra den valgte placering, så den ikke længere vises. Handlingen eller handlingsgruppen forbliver på de andre placeringer. |
|**Skjul**|Denne indstilling vises, hvis handlingen eller handlingsgruppen ikke er placeret andre steder på handlingslinjen. Som det er tilfældet med **Fjern**, forsvinder handlingen eller handlingsgruppen fra handlingslinjen, hvis du vælger denne indstilling. Men i tilpasningstilstand vises handlingen eller handlingsgruppen stadig på den aktuelle placering, bortset fra at den er nedtonet.|
|**Vis**|Denne indstilling vises, hvis handlingen eller handlingsgruppen tidligere har været skjult (nedtonet). Vælges denne indstilling, vises handlingen eller handlingsgruppen på handlingslinjen.|

### <a name="to-move-actions-and-action-groups"></a>Sådan flyttes handlinger og handlingsgrupper

Hvis du vil flytte en handling eller handlingsgruppe, skal du trække og slippe den på den ønskede placering på samme måde som med feltet og kolonner.

Hvor du kan slippe handlinger eller handlingsgrupper, er angivet af en vandret linje mellem handlinger eller en ramme omkring en handlingsgruppe.

- Du kan flytte enkelte handlinger til de fremhævede kategorier, men du kan ikke ændre rækkefølgen af handlinger i kategorien.
- Du kan ikke flytte en handlingsgruppe til en fremhævet kategori.
- Hvis du vil flytte en handling eller handlingsgruppe til en anden handlingsgruppe, der er tom, skal du trække handlingen eller handlingsgruppen og slippe den i feltet **Slip en handling her**.

## <a name="additional-points-of-interest"></a>Flere punkter af særlig interesse

Her er nogle forslag, der kan hjælpe dig med at opnå en bedre forståelse.

- Når du ændrer en kortside, som du åbner fra en liste, træder ændringerne træde i kraft på alle poster, der åbnes fra denne liste. Lad os antage, at du åbner en bestemt kunde fra listen Debitorer og derefter tilpasser siden ved at tilføje et felt. Når du åbner andre debitorer på listen, vises det felt, du har tilføjet, også.
- Ændringer, du foretager, træder i kraft på alle dine rollecentre. Hvis du f.eks. foretager en ændring på listen Debitorer, når rollecenteret er angivet til virksomhedsleder, vises også ændringen i også i listen Debitorer, når rollecenter er angivet til salgsordrebehandler.
- Ændringer af en side i en rude træder i kraft på siden, overalt hvor den vises.  
- Du kan kun tilføje felter og kolonner fra en foruddefineret liste, der er baseret på siden. Du kan ikke oprette nye felter og kolonner.

## <a name="to-clear-personalization"></a>Sådan fjernes tilpasning

På et tidspunkt ønsker du måske at fjerne nogle eller alle de tilpasningsændringer, du har foretaget på en side i tidens løb. Hvis du vil gøre dette, skal du i banneret **Tilpasning** vælge **Flere**, **Fjern tilpasning** og derefter vælge en af følgende muligheder. Vær opmærksom på, at fjernelse af tilpasning ikke kan fortrydes.

|Indstilling|Det gør den|
|------|------------
|Kun handlinger|Fjerne alle de tilpasningsændringer, du nogensinde har foretaget for handlingslinjen på siden.|
|Alle undtagen handlinger|Fjerner alle de tilpasningsændringer, du nogensinde har foretaget for siden undtagen dem på handlingslinjen. Dette omfatter ændringer af felter, kolonner, dele og fliser. |
|Alle|Fjerner alle de tilpasningsændringer, du har foretaget på siden, så siden får sit oprindelige udseende. Dette omfatter ændringer af handlingslinje, felter, kolonner, dele og fliser.|

## <a name="see-also"></a>Se også

[Administration af tilpasning](ui-personalization-manage.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
