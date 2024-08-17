---
title: Tilpasse sider
description: 'Få at vide, hvordan du kan tilpasse brugergrænsefladen og tilpasser dit arbejdsområde, så det passer til din måde at arbejde på i Business Central.'
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 07/26/2024
ms.author: jswymer
---
# <a name="personalize-your-workspace"></a>Tilpas arbejdsområdet

Du kan tilpasse dit arbejdsområde, så det passer til dit arbejde og dine præferencer. Ændr sider, så der kun vises de oplysninger, du skal bruge, hvis du har brug for det. Tilpasning påvirker kun dit arbejdsområde. Den ændrer ikke, hvordan andre arbejder. Du kan tilpasse alle typer sider, herunder siden [Rollecenter](ui-change-basic-settings.md#role-center).

> [!NOTE]
> På grund af begrænsninger på designmuligheder i webklienten er det i øjeblikket ikke muligt at tilpasse eller tilpasse kontrollerne i `grid` og `fixed`-syntaksen.
Det gælder for alle designtilstande, ikke kun personalisering.

<!--[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]-->

Du kan udføre forskellige ændringer som at flytte eller skjule felter, kolonner, handlinger, hele dele og tilføje nye felter. De fleste tilpasninger skal foretages ved først at aktivere det **personlige** banner. Du kan foretage simple justeringer, f. eks. kolonnebredden, med det samme på en vilkårlig liste.

> [!NOTE]
> Administratorer kan foretage de samme layoutændringer som brugere ved at tilpasse en profil (rolle), som kan tildeles flere brugere. Hvis du vil vide mere om roller, skal du gå til [Tilpasse sider til roller](ui-personalization-manage.md)<br /><br />
Administratorer kan også tilsidesætte eller deaktivere brugernes tilpasninger, og de kan også definere, hvilke funktioner brugerne skal kunne se i alle eller bestemte regnskaber. Du kan finde flere oplysninger i [Tilpasse Business Central](ui-customizing-overview.md).

## <a name="video-and-training"></a>Video og træning

I følgende video vises nogle metoder til at tilpasse dit rollecenter.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

Hvis du vil have onlineundervisning, skal du gå til [Tilpasse Microsoft-brugergrænsefladen Dynamics 365 Business Central](/training/modules/personalize-ui-dynamics-365-business-central/).

## <a name="change-the-width-of-a-column"></a>Ændre kolonnebredden

Du kan nemt ændre kolonnestørrelsen på en vilkårlig liste. Træk blot i kanten mellem to kolonner mod venstre eller højre.  

1. Markér og træk i kanten mellem to kolonner i oversigtshovedet.
2. Du kan også dobbeltklikke på kanten mellem to kolonner for automatisk at tilpasse kolonnebredden. Bredden justeres til den optimale læsestørrelse.

Som ved andre tilpasninger gemmes de ændringer, du foretager af kolonnebredden, på din konto og vises, uanset hvilken enhed du logger på.

## <a name="start-personalizing-by-using-the-personalization-mode"></a>Starte brugertilpasning ved hjælp af tilpasningstilstand

1. Åbn en side, du vil tilpasse.
1. I øverste højre hjørne vælges ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") ikon, og derefter handlingen **Tilpas**.

    Banneret **Tilpasning** vises øverst for at angive, at du kan begynde at foretage ændringer.

    > [!NOTE]
    > Hvis du vil navigere under tilpasningen, skal du bruge <kbd>Ctrl</kbd>+<kbd>Klik</kbd> på en handling, hvis den er fremhævet af pilespidsen.

    Hvis du får vist ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst") eller ![Tilpasning spærret](media/personalization-blocked-icon.png "Tilpasning blokeret") på banneret, kan du ikke tilpasse siden. Du kan finde flere oplysninger i [Hvorfor er en side låst mod tilpasning](ui-personalization-locked.md).

1. Hvis du vil ændre et brugergrænsefladeelement, skal du pege på elementet, f.eks. en handling, et felt eller en del. Elementet fremhæves straks med en pilespids eller kant. Vælg elementet, og vælg derefter enten **Flyt**, **Fjern**, **Skjul**, **Vis**, **Vis under "Vis flere"**, **Vis, når skjult**, **Vis altid**, **Angiv/Ryd låst rude** eller **Medtag/Udeluk fra genvej**, afhængigt af typen og tilstanden for brugergrænsefladeelementet.
1. Hvis du vil tilføje et felt, skal du vælge handlingen **+ Felt**. Træk og slip et felt på den ønskede placering på siden i sideruden **Føj felt til side**.
1. Når du er færdig med at ændre layoutet for en eller flere sider, skal du vælge knappen **Udført** på banneret **Tilpas**.

Du kan finde flere oplysninger i [Hvad kan du tilpasse](#What).

## <a name="what-you-can-personalize"></a><a name="What"></a>Hvad kan du tilpasse

|Hvad vil du foretage dig?|Hvordan du gør det|Kommentarer|
|----|------------|-------|
|Flytte noget, f.eks. et felt, en kolonne i listen, et felt, en handling eller en del af et andet sted på siden|Peg et vilkårligt sted i det, du vil flytte, og træk det til den nye placering. Placeringen angives med enten en fed vandret eller lodret linje.<br /><br />![Kan ikke flytte her-ikon](media/personalization-cannot-move-here.png "Tilpasningstilstand – kan ikke flytte her-ikon") angiver, at du ikke kan flytte elementet til den valgte placering.|Dele er underinddelinger eller områder på en side, der indeholder elementer, f.eks. flere felter, en anden side, et diagram eller felter.<br /><br />[Få flere oplysninger om tilpasning af handlinger](#Actions)<br>[Få flere oplysninger om tilpasning af dele](#Parts)|
|Skjul et element, der aktuelt vises, f.eks. et felt, en kolonne på listen, et felt, en handling eller en del.|Markér elementet, marker pilespidsen, og vælg derefter <b>Skjul</b>.|I tilpasningstilstand er skjulte handlinger nedtonet med kursiv tekst, og skjulte dele er nedtonet af diagonale linjer. Skjulte felter og kolonner vises ikke direkte på siden, men du kan finde dem ved hjælp af ruden <b>Føj felt til side</b> ([få mere at vide om arbejdsfelter](#fields)).<br><br>Når du afslutter tilpasningstilstand, forsvinder alle elementer fra visningen. Hvis det felt, du skjuler, også vises i overskriften til oversigtspanelet, når oversigtspanelet er skjult, vises feltet ikke længere der.|
|Vise en handling eller del, der aktuelt er skjult|For et nedtonet (skjult) element skal du vælge pilespidsen og derefter vælge <b>Vis</b>.|Det skjulte element er synligt igen.|
|Tilføj et felt, der aktuelt er skjult|Vælg handlingen <b>+ Felt</b> i banneret <b>Tilpas</b>.<br /></br>Ruden <b>Tilføj felt til side</b> vises til højre på siden. Hvis du markerer et felt i ruden, vises dets skjulte placering på siden.<br /><br />Hvis du vil tilføje et felt, skal du trække det fra ruden eller den skjulte placering til den ønskede placering. Placeringen angives med enten en fed vandret eller lodret linje.<br><br> En anden måde er at vælge pilespidsen på feltets skjulte placering og vælge **Vis**. |Hver side indeholder et foruddefineret sæt felter, du kan vælge at vise.<br /><br />[Få mere at vide mere om at arbejde med felter](#fields) |
|Vise et felt i overskriften til et oversigtspanel, når det er skjult.|Vælg pilespidsen, og vælg derefter <b>Vis, når skjult</b>. <br /> <br />Hvis du ikke kan se denne indstilling, er den allerede angivet. Hvis det er tilfældet, og feltet ikke skal vises i overskriften til oversigtspanelet, skal du vælge <b>Vis altid</b>.|*Oversigtspanel* er det udtryk, der bruges om en gruppe felter, der vises under en fælles overskrift. Brug indstillingen <b>Vis, når skjult</b> for at få vist de vigtigste felter. Hvis du vælger et felt i overskriften, åbnes oversigtspanelet, og der fokuseres på det valgte felt.<br /><br />Denne indstilling kan kun anvendes, hvis en side har mere end et oversigtspanel. Hvis der kun er ét oversigtspanel, kan det ikke skjules, så indstillingen <b>Vis, når skjult</b> er ikke tilgængelig.|
|Angiv, at et felt kun skal vises, når du vælger **Vis mere**.|Vælg pilespidsen, og vælg derefter <b>Vis under "Vis flere"</b>.|Hvis du ikke kan se indstillingen <b>Vis under "Vis flere"</b>, er feltet allerede angivet. I så fald skal du vælge <b>Vis altid</b> for at få vist et felt hele tiden, og ikke kun når du vælger **Vis mere**.|
|Ændre, om et felt kan redigeres.|Markér feltet, vælg pilehovedet på feltet, og vælg derefter <b>Lås redigering</b> for at forhindre ændring af feltets værdi eller <b>Lås redigering op</b> for at tillade ændring af feltets værdi.|Du kan kun låse op for felter, som du tidligere selv har låst. Nogle felter er låst som standard, enten af design eller af en profiladministrator, der har [tilpasset siden](ui-personalization-manage.md). Disse felter kan ikke låses op.|
|Flytte den fastlåste rude i en liste til en anden kolonne. |Vælg pilespidsen for den kolonne, som du vil bruge som den sidste kolonne i den fastlåste rude, og vælg derefter <b>Angiv låst rude</b>.<br /><br/>Hvis du vil flytte den fastlåste rude tilbage til den oprindelige tiltænkte placering, skal du vælge pilespidsen for den aktuelle kolonne i den låste rude og vælge <b>Ryd låst rude</b>. Bemærk: Du kan ikke fjerne denne låste rude.|Den fastlåste rude angiver de kolonner, der altid vises i venstre side på listen, selv når du ruller vandret.|  
|Spring et felt over, når du trykker på Enter.|Vælg pilespidsen ved siden af feltet eller kolonneoverskriften på en liste, og vælg **Udeluk fra genvej**.  | Hvis du ikke kan se **Udelad fra genvej**, er feltet allerede sprunget over. I det tilfælde skal du stoppe med at springe feltet over og vælge **Medtag i genvej**.<br><br>[Få mere at vide om Genvej](ui-enter-data.md#QuickEntry)|
|Omarrangere og fjerne visninger, der repræsenterer filtrerede lister.|Vælg pilespidsen ud for en visning, og vælg derefter **Flyt**, **Fjern** eller **Skjul**.|[Få mere at vide om lagring og tilpasning af listevisninger](ui-views.md)|  
|Føje en ny handling til en side eller en rapport i dit rollecenter.|Vælg bogmærkeikonet på rapportanmodningssiden eller i vinduet Fortæl mig på målsiden.|[Få flere oplysninger om bogmærker til sider og rapporter](ui-bookmarks.md)|
|Starte altid en liste som udvidet eller skjult|Vælg **Udvid alle** eller **Skjul alle** i øverste venstre hjørne. Du kan også vælge funktionen **Udvid alle** eller **Skjul alle** i menuen til den første kolonne. |Gælder for hierarkilister, der kan skjules|

## <a name="personalize-action-bar-and-menus"></a><a name="Actions"></a>Tilpasse handlingslinje og menuer

Tilpasning gør det muligt at bestemme, hvilke handlinger der skal vises på navigations- handlingslinjerne samt i rollecentre, og hvor de skal vises. Du kan vise, skjule eller flytte individuelle handlinger eller handlingsgrupper.

Følgende video viser, hvordan du kan tilpasse handlinger på sider og rollecentre.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

Tilpasning af navigations- og handlingslinjerne foretages stort set på samme måde som med andre elementer i brugergrænsefladen. Men hvad du kan gøre med en handling eller en gruppe, afhænger af hvor handlingen eller gruppen er placeret. Den bedste måde at finde ud af det på, er ved at vælge tilpasningstilstand og derefter følge pilespidserne.

Der er et par ord, du skal kende for at få en bedre forståelse af handlingstilpasning: *handlingsgruppe* og *fremhævet kategori*.  

En *handlingsgruppe* er et element, som kan vise andre handlinger eller grupper, når det udvides. For eksempel på siden **Salgsordrer** vises handlingsgruppen **Funktioner**-handlingen, når du vælger **Handlinger**.

En *fremhævet kategori* er en handlingsgruppe, der vises foran den lodrette linje `|` på handlingslinjen. Kategorierne omfatter typisk de mest almindeligt anvendte handlinger, så du hurtigt kan finde dem. For eksempel er handlingerne **Ordre**, **Frigivelse** og **Bogføring** på siden **Salgsordrer** fremhævede kategorier.

> [!NOTE]  
> Hvis du vil rydde tilpasningen, skal du markere pilespidsen omkring delens design menu og derefter vælge **Ryd tilpasning**.

### <a name="remove-hide-and-show-actions-and-action-groups"></a>Fjerne, skjule og vise handlinger og handlingsgrupper

Når du vil vise eller skjule en handling, definerer indstillingerne under pilespidsen, hvad du kan gøre, afhængigt af handlingstilstanden. 

1. Vælge pilespidsen for en handling eller en handlingsgruppe.
2. Vælg en af følgende indstillinger:

|Indstilling|Det gør den|
|------|------------|
|**Fjern**|Denne indstilling vises, hvis den valgte handling også er vist et andet sted på navigations- eller handlingslinjen. Hvis du vælger denne indstilling, slettes handlingen fra den valgte placering, så den ikke længere vises. Handlingen eller handlingsgruppen forbliver på de andre placeringer. |
|**Skjul**|Denne indstilling vises, hvis handlingen eller handlingsgruppen ikke er placeret andre steder på navigations- eller handlingslinjen. Som det er tilfældet med **Fjern**, forsvinder handlingen eller handlingsgruppen fra navigations- eller handlingslinjen, hvis du vælger denne indstilling. Men i tilpasningstilstand vises handlingen eller handlingsgruppen stadig på den aktuelle placering, bortset fra at den er nedtonet.|
|**Vis**|Denne indstilling vises, hvis handlingen eller handlingsgruppen er skjult (nedtonet). Vælges denne indstilling, vises handlingen eller handlingsgruppen på navigations- eller handlingslinjen.|

### <a name="move-actions-and-action-groups"></a>Flytte handlinger og handlingsgrupper

Hvor du kan slippe handlinger eller handlingsgrupper, er angivet af en vandret linje mellem to handlinger eller en kant omkring en handlingsgruppe. Der findes følgende begrænsninger:

- Du kan flytte enkelte handlinger til de fremhævede kategorier, men du kan ikke ændre rækkefølgen af handlinger i kategorien.
- Du kan ikke flytte en handlingsgruppe til en fremhævet kategori.

1. Hvis du vil flytte en handling eller handlingsgruppe, skal du trække og slippe den på den ønskede placering på samme måde som med feltet og kolonner.
2. Hvis du vil flytte en handling eller handlingsgruppe til en anden handlingsgruppe, der er tom, skal du trække handlingen eller handlingsgruppen og slippe den i feltet **Slip en handling her**.

### <a name="about-the-automate-menu"></a>Om menuen Automatiser

- Du kan ikke skjule eller flytte menuen **Automatiser** eller **Power Automate**-undermenuen og dens handlinger.
- Du kan flytte flows, der er medtaget under elementet **Automatiser**, men du kan ikke skjule dem ved hjælp af personlig tilpasning. Når flowet flyttes, kopieres flowet til destinationen, men den fjernes ikke fra elementet **Automatiser**.

> [!TIP]
> Som administrator kan du skjule elementet **Automatisering** fra brugere. Flere oplysninger i [Konfigurere Power Automate-integration](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="personalize-parts"></a><a name="Parts"></a>Tilpasning af dele

Peg på eller vælg <kbd>Alt</kbd>+<kbd>Pil op</kbd> - Dele er områder på en side, der typisk består af flere felter, diagrammer eller andet indhold. En del vises med en farvet ramme, når du fokuserer på delen. Et rollecenters startskærm har f.eks. flere dele. På grund af den veldefinerede grænse kan du tilpasse hele delen og dens indhold.

- Træk og slip en del til den ønskede placering for at flytte den. En farvet linje angiver gyldige placeringer på skærmen. Faktabokse kan f.eks. kun flyttes til siden af andre faktabokse i faktaboksruden.
- Du kan skjule en del ved at vælge indstillingen **Skjul** under pilespidsen.
- Når du begynder at tilpasse eller navigere til en ny side, vil alle dele, der aktuelt er skjult, blive vist på siden med karakteristiske detaljer, der angiver, at de er skjulte. Du kan vise denne del igen ved at vælge indstillingen **Vis** under pilespidsen.

Du kan fjerne alle de tilpasningsændringer, du har foretaget i en enkelt del, ved at vælge indstillingen **Fjern tilpasning** under delens pilespids. Hvis du fjerner markering af en del, påvirker det kun, om en del er ændret, ikke placeringen eller synligheden af delen på siden.  

## <a name="work-with-fields-and-columns"></a><a name="fields"></a>Arbejde med felter og kolonner

Når du tilpasser en side, bruger du ruden **Føj felt til side** for at inkludere felter eller kolonner på den side, der aktuelt er skjult fra visning. Du kan åbne denne rude ved at vælge handlingen **+ Felt** nær toppen af siden. I modsætning til andre skjulte elementer er skjulte felter ikke angivet på selve siden i tilpasningstilstand. Du kan dog identificere skjulte felter ved hjælp af ruden **Føj felt til side**.

Her vises nogle generelle retningslinjer, du skal følge, når du bruger ruden **Føj felt til side**:

- Ruden indeholder som standard alle skjulte felter. Skjulte felter er markeret med ikonet ![Viser ikonet for skjult felt](media/hidden-icon.png "Viser ikonet for det skjulte felt").
- Du kan filtrere listen til at vise andre felter, som f.eks. dem, der aktuelt vises på siden, ved at vælge knappen **Anbefalede felter** over listen og vælge en filterindstilling. Navnet på knappen ændres baseret på den filterindstilling, du vælger.
  
   :::image type="content" source="media/personlaization-filter.svg" alt-text="Viser filterknappen i ruden Tilføj et felt i tilpasningstilstand.":::
- Når du vælger et felt på listen, fremhæves dets placering på siden. Hvis feltet aktuelt er skjult, vises dets designede placering i en skyggelagt tilstand. 
- Du kan få flere oplysninger om et felt på listen ved at pege på det eller vælge <kbd>Alt</kbd>+<kbd>Pil op</kbd> for at få vist et værktøjstip.
- De felter, der er tilgængelige i ruden **Føj felt til side**, bestemmes af udvikleren af siden og dens kildetabel eller af en profiladministrator, der har [tilpasset siden](ui-personalization-manage.md). Du kan ikke oprette nye felter og kolonner.
- Nogle sider har flere sidefelter, der er knyttet til den samme kildetabel. Ruden viser begge/alle disse sidefelter uafhængigt af hinanden. At vise/skjule/flytte disse felter er også uafhængigt, uden at det ene påvirker det andet.

### <a name="add-a-field-so-its-visible-on-the-page"></a>Tilføj et felt, så det er synligt på siden

Fra ruden **Føj felt til side** kan du medtage et felt, der aktuelt er skjult på siden, på to måder:

- Træk feltet til den ønskede placering. Målplaceringen angives med en fed vandret eller lodret linje.
- Vælg feltet på listen, gå derefter til det skyggelagte felt på siden, og vælg indstillingen **Vis**.

> [!NOTE]
> Nogle af de felter, du tilføjer, kan ikke redigeres på siden, når du er færdig med tilpasningen. Disse felter er enten oprindeligt designet på denne måde, eller en administrator har [tilpasset](ui-personalization-manage.md) siden for at forhindre dig i at redigere dem.

## <a name="clear-personalization"></a>Fjern tilpasning

På et tidspunkt ønsker du måske at fjerne nogle eller alle de tilpasningsændringer, du har foretaget på en side i tidens løb.

1. Vælg handlingen **Fjern tilpasning** på banneret **Tilpas**.
2. Vælg en af følgende indstillinger.  

> [!CAUTION]
> Fjernelse af tilpasning ikke kan fortrydes.

|Indstilling|Det gør den|
|------|------------|
|**Kun menuen Navigation**|Fjerner alle tilpasningsændringer, du har foretaget i navigationsmenuen, som er delt på tværs af rollecenteret og andre sider. Sådanne ændringer omfatter alle nye handlinger, der er tilføjet som bogmærker, og eventuelle ændringer af links og grupper i menuen.|  
|**Kun handlinger**|Fjerner alle de tilpasningsændringer, du nogensinde har foretaget på navigations- eller handlingslinjerne på siden.|
|**Kun Felter og Kolonner**|Fjerner alle de tilpasningsændringer, du nogensinde har foretaget for siden undtagen ændringer på navigations- eller handlingslinjen. Sådanne ændringer omfatter ændringer af felter, kolonner, dele og fliser. |
|**Alle**|Fjerner alle de tilpasningsændringer, du har foretaget på siden, så siden får sit oprindelige udseende. Sådanne ændringer omfatter ændringer af navigations- og handlingslinjer, felter, kolonner, dele og fliser.|

## <a name="tips-and-other-points-of-interest"></a>Tips og andre punkter af interesse

Her er nogle forslag, der kan hjælpe dig med at opnå en bedre forståelse.

- Når du ændrer en kortside, som du åbner fra en liste, træder ændringerne træde i kraft på alle poster, der åbnes fra denne liste. Lad os antage, at du åbner en bestemt kunde fra listen Debitorer og derefter tilpasser siden ved at tilføje et felt. Når du åbner andre debitorer på listen, vises det felt, du har tilføjet, også.
- Ændringer, du foretager, træder i kraft på alle dine rollecentre. Hvis du f.eks. foretager en ændring på listen Debitorer, når rollecenteret er angivet til virksomhedsleder, vises også ændringen i også på siden **Debitorer**, når Rollecenter er indstillet til Salgsordrebehandler.
- Ændringer af en side i en rude træder i kraft på siden, overalt hvor den vises.  
- Du kan ikke tilpasse en side, der er i [analysetilstand](analysis-mode.md). Kontakten **Analysér** er deaktiveret. Hvis du skifter til tilpasningstilstand, mens siden er i analysetilstand, deaktiveres analysetilstand automatisk. 
- Nogle sider har flere sidefelter, der er knyttet til den samme kildetabel. Ruden viser begge/alle disse sidefelter uafhængigt af hinanden. At vise/skjule/flytte disse felter er også uafhængigt, uden at det ene påvirker det andet.
- Hvis en del eller gruppe er skjult, vises spøgelsesfelter stadig inde i den, men du kan ikke trække og slippe eller tilføje/vise dette felt, før du gør gruppen/delen synlig.

## <a name="see-also"></a>Se også

[Tilpasse sider til profiler](ui-personalization-manage.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
