---
title: Sortering af, søgning i og filtrering af lister | Microsoft Docs
description: Arbejde effektivt på lister ved at søge på tværs af dine data, sorterer kolonner og præcisere resultater ved at bruge effektive filtersymboler og tastaturgenveje.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 06/03/2019
ms.author: sgroespe
ms.openlocfilehash: fc9cefd33f6ca11ee4f2936671a84071e142a1bd
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621179"
---
# <a name="sorting-searching-and-filtering-lists"></a>Sortering af, søgning i og filtrering af lister
Der er et par ting, du kan gøre som en hjælp til at scanne, finde og begrænse poster på en liste. Disse omfatter sortering, søgning og filtrering. Du kan anvende nogle eller alle af disse samtidigt til hurtigt at finde eller analysere dataene.

> [!TIP]
> Når du får vist dataene som felter, kan du søge og bruge grundlæggende filtrering. Når du vil bruge et komplet sæt af effektive funktioner til sortering, søgning eller filtrering, skal du vælge ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Pil til venstre Vis som liste") for at få vist en liste.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Sortering
Sortering gør det nemt og hurtigt for dig at overskue dine oplysninger. Hvis du har mange kunder, f.eks. kan du vælge at sortere dem efter **Kundenr.**, **Debitorbogføringsgruppe**, **Valutakode**, **Lande-/områdekode** eller **Momsregistreringsnr.** for at få det nødvendige overblik.

Hvis du vil sortere en liste, kan du enten vælge en kolonneoverskriftstekst, hvor du kan skifte mellem stigende og faldende rækkefølge, eller du kan vælge den lille nedadgående pil i kolonneoverskriften og derefter vælge **Stigende** eller **Faldende**.  

> [!NOTE]  
>   Sortering understøttes ikke af billeder, BLOB-felter, FlowFilters og felter, der ikke tilhører en tabel.  

## <a name="searching"></a>Søgning
<!--## Searching by using the Quick Filter -->
Øverst på hver oversigtsside finder du en ![Søgeoversigt](media/ui-search/search-list.png "Ikonet Søgeoversigt") **Søg**, der er en hurtig og nem måde at reducere posterne på en liste på og kun viser de poster, der indeholder data, som du er interesseret i at få vist.

Du søger ved at vælge søgeikonet og derefter skrive den tekst, du leder efter, i feltet. Du kan skrive bogstaver, tal og andre symboler.

### <a name="fine-tuning-the-search"></a>Finjustering af søgningen
Generelt forsøger søgningen at matche teksten på tværs af alle felter. Den skelner ikke mellem store og små bogstaver og sammenligner tekst, hvor som helst i feltet (ved begyndelsen, slutningen eller i midten).

Dog kan du foretage en mere nøjagtig søgning ved hjælp af følgende specialtegn:

- Sæt søgeteksten i enkelte anførselstegn `''` (f.eks. `'man'`) for kun at finde feltværdier, der er identiske med hele teksten, og hvor små og store bogstaver er identiske.

- Sæt `*` efter søgeteksten (f.eks. `man*`) for at finde feltværdier, der begynder med en bestemt tekst, og hvor små og store bogstaver er identiske.

- Sæt `*` før søgeteksten (f.eks. `*man`) for at finde feltværdier, der slutter med en bestemt tekst, og hvor små og store bogstaver er identiske.

- Når du bruger `''` eller `*`, skelnes der mellem små og store bogstaver i søgningen. Hvis du vil have, at der skelnes mellem små og store bogstaver i søgningen, skal du indsætte `@` foran søgeteksten (for eksempel `@man*`).

Følgende tabel indeholder nogle eksempler, der forklarer, hvordan du kan bruge søgningen.

|Søgekriterier|Finder...|
|---------------|----------|
|`man`<br />eller <br />`Man`|Alle poster med felter, der indeholder teksten **man**, uanset store eller små bogstaver. F.eks. **Manchester**, **manual** eller **Sportsman**. |
|`'Man'`|Alle poster med felter, der kun indeholder **Man**. Samme brug af store og små bogstaver.|
|`Man*`|Alle poster med felter, der begynder med teksten <b>Man</b>. Samme brug af store og små bogstaver. F.eks. **Manchester**, men ikke **manual** eller **Sportsman**.|
|`@Man*`|Alle poster med felter, der begynder med teksten **man**, uanset om der bruges store eller små bogstaver. F.eks. **Manchester** og **manual**, men ikke **Sportsman**.|
|`@*man`|Alle poster der slutter med teksten **man**, uanset om der er brugt store eller små bogstaver. F.eks. **Sportsman**, men ikke **Manchester** eller **manual**.|

> [!TIP]
> Du kan trykke på F3 for at aktivere og deaktivere søgefeltet. Du kan finde flere oplysninger i [Tastaturgenveje](keyboard-shortcuts.md#KeyboardFilter).

## <a name="Filtering"> </a>Filtrering
Filtrering giver en mere avanceret og fleksibel må de at kontrollere, hvilke poster der vises på en liste. Der er to vigtige forskelle mellem søgning eller filtrering, som beskrevet i nedenstående tabel.

|| **Søgning** | **Filtrering** |
|--|----------|------------|
| **Relevante felter** | Søger på tværs af alle de felter, der kan ses på siden. | Filtrerer et eller flere felter hver for sig og vælger fra et felt i tabellen, herunder felter, ikke der kan ses på siden. |
| **Matching** | Viser poster med felter, der stemmer overens med søgeteksten, uanset store eller små bogstaver eller placeringen af teksten. | Viser poster, hvor feltet nøjagtigt svarer til filteret, og der skelnes mellem små og store bogstaver, medmindre der er angivet særlige filtersymboler.

Filtrering giver dig mulighed at få vist poster for bestemte konti eller kunder, datoer, beløb og andre oplysninger ved at angive filterkriterier. Det er kun poster, der svarer til kriterierne, som vises. Hvis du angiver kriterier for flere felter, vises kun poster, der svarer til alle kriterier.

### <a name="working-in-the-filter-pane"></a>Arbejde i filterruden

Du får vist filterruden ved at vælge ![Ikonet Filterrude](media/open-filter-pane-icon.png "Ikonet Filterrude") øverst på listen eller ved at trykke på **Shift+F3**. For lister i rollecenteret kan du også vælge pil ned tæt på sidetitlen på navigationslinjen over listen og derefter vælge **Vis Filterrude** som vist her.

![Vis Filterrude](media/open-filter-pane.png "Vis Filterrude")

Filterruden viser de aktuelle filtre på en liste, og gør det muligt at angive dine egne brugerdefinerede filtre i en eller flere felter. Følgende figur viser et eksempel på filterruden for en liste over salgstilbud.

![Oversigt over Filterrude](media/filter-pane-overview.png "Filterikon")

En filterrude er inddelt i tre afsnit: **Visninger**, **Filtrer listen efter** og **Filtrer totaler efter**:

- **Visninger**

  Nogle lister indeholder sektionen **Visninger**. Visninger er variationer af listen, der er forudkonfigureret med filtre. For at skifte til en anden visning af listen skal du blot vælge et andet link. Du kan midlertidigt ændre filtrene i en visning, men ændringerne gemmes ikke permanent.

- **Filtrer listen efter**

  Sektionen **Filtrer listen efter** er der, hvor du tilføjer filtre i bestemte felter for at reducere antallet af viste poster. Du kan tilføje et filter ved at vælge **+ Filter**, markere det felt, du vil filtrere fra et felt i tabellen, og derefter angive filterkriterierne i feltet.

- **Filtrer totaler efter**

  Nogle lister, der viser beregnede felter, som beløb og antal, indeholder sektionen **Filtrer totaler efter**, hvor du kan justere forskellige dimensioner, der påvirker beregninger. F.eks. kan du hurtigt analysere din kontoplan ved at filtrere beløb til en bestemt periode, eller du kan få vist de samlede beløb for f.eks. salgsordrer fra et bestemt lagersted.

  Du kan tilføje et filter ved at vælge **+ Filter**, vælge en af de foruddefinerede dimensioner og derefter tilføje filterkriterierne i feltet.

  > [!NOTE]
  > Filtre i sektionen **Filtrer totaler efter** styres af FlowFilters i sideopsætningen. Du kan finde tekniske oplysninger i [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).


### <a name="entering-filter-criteria-in-the-filter-pane"></a>Angivelse af filterkriterier i filterruden
Når du vil vælge et felt, du vil filtrere, skal du gøre et af følgende indstillinger:
  - Vælg **+ Felt** i filterruden. Skriv navnet på det felt, du vil filtrere, eller vælg et felt i den menu, der viser alle felter i tabellen.

  - Vælg rullepilen i en kolonneoverskrift, og vælg derefter **Filter...**. Derved åbnes filterruden, og kolonnen føjes til filterruden.

Du kan nu skrive eller vælge filterkriterierne i feltet. Den typen felt, du filtrerer bestemmer, hvilke kriterier du kan angive. For eksempel kan du, når du filtrerer et felt, der har faste værdier, kun vælge mellem disse værdier. Du kan finde yderligere oplysninger om særlige filtersymboler i [Filterkriterier](#FilterCriteria) og [Filtertokens](#FilterTokens).

Kolonner, som allerede indeholder filtre, er angivet med ![Filterikonet](media/ui-search/filter-icon.png "Filterikonet") i kolonneoverskriften. Hvis du vil fjerne et filter, skal du markere kolonneoverskriften og derefter vælge **Ryd filter**.


### <a name="entering-filter-criteria-without-using-the-filter-pane"></a>Angivelse af filterkriterier uden brug af filterruden
Du kan angive simple filtre direkte på listen uden at skulle bruge filterruden.
Med et eller flere felter markere i en række skal du bruge tastaturgenvejen **Alt + F3** til at få vist kun de poster, der har den samme værdi. Du kan derefter vælge et andet felt og bruge den samme genvej igen for at fortsatte med at præcisere filtrene. Hvis det valgte felt allerede er filtreret, kan du bruge **Alt + F3** til at fjerne filteret.

> [!TIP]
> Fremskynd søgning efter og analyse af dine data ved hjælp af kombinationer af genvejstaster. For f.eks. at markere et felt skal du bruge **Skift + Alt + F3** for at føje dette felt til filterruden, angive filterkriterierne, bruge **Ctrl + Enter** for at vende tilbage til rækkerne, vælge et andet felt og bruge **Alt + F3** til at filtrere til værdien.
Du kan finde flere oplysninger i [Tastaturgenveje](keyboard-shortcuts.md#KeyboardFilter).


## <a name="FilterCriteria"> </a>Filterkriterier og -symboler
Når du angiver kriterier, kan du bruge alle de tal og bogstaver, som du plejer at bruger i feltet. Derudover kan du bruge nogle specialtegn til at filtrere resultaterne yderligere. Følgende tabeller viser de tegn, der kan bruges i filtre. Ved datoer og klokkeslæt kan du også se [Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md) for at få flere oplysninger.

> [!IMPORTANT]  
>  Der kan være tilfælde, hvor feltværdierne indeholder disse symboler, og du vil filtrere efter dem. Hvis du vil gøre dette, skal du medtage det filterudtryk, der indeholder symbolet i anførselstegn ("). Hvis du f.eks. vil filtrere efter poster, der starter med teksten *S&R*, er filterudtrykket `'S&R*'`.  

### <a name="-interval"></a>(..) Interval

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`1100..2100`|Tal fra 1100 til og med 2100.|  
|`..2500`|Konti til og med 2500|  
|`..12 31 00`|Datoer til og med 31-12-00.|  
|`P8..`|Oplysninger for regnskabsperiode 8 og frem|  
|`..23`|Fra begyndelsesdatoen til 23-aktuel måned-aktuelt år 23.59.59|  
|`23..`|Fra 23-aktuel måned-aktuelt år 0.00.00 til sluttidspunktet|  
|`22..23`|Fra den 23-aktuel måned-aktuelt år 0.00.00 til 22-aktuel måned-aktuelt år 22.59.59|  

### <a name="124-eitheror"></a>(&#124;) Enten/eller  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`1200|1300`|Tal med 1200 eller 1300.|  

### <a name="-not-equal-to"></a>(<>) Ikke lig med  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`<>0`|Alle tal undtagen 0<br /><br /> I SQL Server Option kan du kombinere dette symbol med et udtryk med jokertegn. <>A* betyder f.eks. ikke lig med tekst, der starter med A.|  

### <a name="-greater-than"></a>(>) Større end  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`>1200`|Tal større end 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Større end eller lig med  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`>=1200`|Tal lig med eller større end 1200|  

### <a name="-less-than"></a>(<) Mindre end  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`<1200`|Tal mindre end 1200|  

### <a name="-less-than-or-equal-to"></a>(<=) Mindre end eller lig med  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`<=1200`|Tal lig med eller mindre end 1200|  

### <a name="-and"></a>(&) Og  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`>200&<1200`|Tal større end 200 og mindre end 1200|  

### <a name="-an-exact-character-match"></a>('') Tegn, der stemmer nøjagtigt overens  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`'man'`|Tekst, der svarer nøjagtigt til man, og der skelnes mellem store og små bogstaver.|  

### <a name="-case-insensitive"></a>(@) Ingen forskel på store og små bogstaver  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`@man*`|Tekst, der starter med man, og der skelnes mellem store og små bogstaver.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Mange ukendte tegn

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`*Co*`|Tekst, der indeholder "A/S", og der skelnes mellem store og små bogstaver.|  
|`*Co`|Tekst, der ender på "A/S", og der skelnes mellem store og små bogstaver.|  
|`Co*`|Tekst, der begynder med "A/S", og der skelnes mellem store og små bogstaver.|  

> [!NOTE]  
>   Du kan ikke bruge en `*`, når du filtrerer i indstillingsfelter (optælling), f.eks. feltet **Status** i salgsordrer. Hvis du vil angive et filter for denne type felt, kan du angive den numeriske værdi som en filterparameter. I feltet **Status** på en salgsordre med værdierne **Åben**, **Frigivet**, **Afventer godkendelse** og **Afventer forudbetaling** kan du f.eks. bruge værdierne `0`, `1`, `2` og `3` til at filtrere efter disse indstillinger.

### <a name="-one-unknown-character"></a>(?) Ét ukendt tegn  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`Hans?n`|Tekst som f.eks. Hansen eller Hanson|  

### <a name="combined-format-expressions"></a>Kombinerede formatudtryk  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Tallet 5999 og tallene fra og med 8100 til og med 8490.|  
|`..1299|1400..`|Medtag poster med et tal mindre end eller lig med 1299, eller tal lig med 1400 eller derover (alle tal undtagen 1300 til og med 1399).|  
|`>50&<100`|Medtag poster med tal større end 50 og mindre end 100 (tal fra 51 til og med 99).|  


## <a name="FilterTokens"> </a>Filtertokens
Når du angiver filterkriterier, kan du også skrive ord, der har en særlig betydning, kaldet filtertokens. Når du har angivet et tokenordet, erstattes ordet af den eller de værdier, det repræsenterer. Det gør filtrering nemmere ved at reducere behovet for at navigere til andre sider for at søge efter værdier, du vil føje til filteret. Tabellerne nedenfor beskriver nogle af de tegn, du kan skrive som filterkriterier.

> [!TIP]
> Din organisation bruger muligvis brugerdefinerede tokens. For at få mere at vide om det komplette sæt tokens, der er tilgængelige for dig, eller tilføje flere brugerdefinerede tokens, skal du kontakte din administrator. Du kan finde tekniske oplysninger i [Tilføje filtertokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).


### <a name="me-or-userid-records-assigned-to-you"></a>(%me eller %userid) Poster, der er tildelt til dig

Brug `%me` eller `%userid` ved filtrering af felter, der indeholder bruger-id'et, f.eks. feltet **Tildelt til bruger-id**, for at få vist alle poster, der er tildelt til dig.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%me`<br />eller<br />`%userid`|Poster, der er knyttet til din brugerkonto. |  

### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Debitorer i Mine debitorer

Brug `%mycustomers` i debitorfeltet **Nej** til at vise alle poster for debitorer, der står på listen **Mine debitorer** i dit rollecenter.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%mycustomers`|Debitorer i **Mine debitorer** i dit rollecenter. |  

### <a name="myitems-items-in-my-items"></a>(%myitems) Varer i Mine varer

Brug `%myitems` i varefeltet **Nej** til at vise alle poster for varer, der står på listen **Mine varer** i dit rollecenter.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%myitems`|Varer i **Mine varer** i dit rollecenter. |  

### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Kreditorer i Mine kreditorer

Brug `%myvendors` i kreditorfeltet **Nej** til at vise alle poster for kreditorer, der står på listen **Mine kreditor** i dit rollecenter.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%myvendors`|Kreditorer i **Mine kreditorer** i dit rollecenter. |  


## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Almindelige spørgsmål om søgning og filtrering](ui-search-filter-faq.md)
