---
title: Sortering af, søgning i og filtrering af lister | Microsoft Docs
description: Arbejd effektivt på lister ved at søge på tværs af dine data, sorterer kolonner og præcisere resultater ved at bruge effektive filtersymboler og tastaturgenveje.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a3d42fccebafdfa80346f04b43a0e3dd29f467d8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770634"
---
# <a name="sorting-searching-and-filtering"></a>Sortering, søgning og filtrering

Der er et par ting, du kan gøre som en hjælp til at scanne, finde og begrænse poster på en liste eller i en rapport eller XMLport. Disse omfatter sortering, søgning og filtrering. Du kan anvende nogle eller alle af disse samtidigt til hurtigt at finde eller analysere dataene.

I forbindelse med rapporter og XMLporte kan du angive filtre for at afgrænse, hvilke data der skal medtages i rapporten eller XMLport, men du kan ikke sortere og søge.

> [!TIP]
> Når du får vist dataene som felter, kan du søge og bruge grundlæggende filtrering. Når du vil bruge et komplet sæt af effektive funktioner til sortering, søgning eller filtrering, skal du vælge ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Vis som liste pil til venstre") for at få vist posterne som en liste.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Sortering

Sortering gør det nemt og hurtigt for dig at overskue dine oplysninger. Hvis du har mange kunder, f.eks. kan du vælge at sortere dem efter **Kundenr.**, **vvalutakode** eller **Lande-/områdekode** for at få det nødvendige overblik.

Hvis du vil sortere en liste, kan du enten:

- Vælg en kolonneoverskriftstekst til skift mellem stigende og faldende rækkefølge, eller
- Vælg rullepilen i kolonneoverskriften, og vælg derefter **stigende** eller **faldende**.  

> [!NOTE]  
> Sortering understøttes ikke af billeder, BLOB-felter, FlowFilters og felter, der ikke tilhører en tabel.  

## <a name="searching"></a>Søgning

<!--## Searching by using the Quick Filter -->
Øverst på hver oversigtsside finder du handlingen ![Søgeoversigt](media/ui-search/search-list.png "Ikonet Søgeoversigt") **Søg**, der er en hurtig og nem måde at reducere posterne på en liste på og kun viser de poster, der indeholder data, som du er interesseret i at få vist.

Du søger ved at vælge handlingen **Søg** og derefter skrive den tekst, du leder efter, i feltet. Du kan skrive bogstaver, tal og andre symboler.

Normalt vil søgningen forsøge at matche teksten på tværs af alle felter. Den skelner ikke mellem store og små bogstaver og sammenligner tekst, hvor som helst i feltet, ved begyndelsen, slutningen eller i midten.

> [!TIP]
> Du kan trykke på **F3** for at aktivere og deaktivere søgefeltet. Du kan finde flere oplysninger i [Tastaturgenveje](keyboard-shortcuts.md#KeyboardFilter).

> [!NOTE]  
> Søgning matcher ikke værdier i billeder, BLOB-felter, FlowFilter, FlowField og andre felter, der ikke er en del af en tabel.


### <a name="fine-tuning-the-search-with-filter-criteria"></a>Finjustere søgningen med filterkriterier

Du kan foretage en mere præcis søgning ved hjælp af filteroperatorer, udtryk og filter-tokens. I modsætning til filtrering anvendes alle felter på tværs af alle felter, når de bruges i søgefeltet, så de bliver mindre effektive end filtrering.

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


## <a name="filtering"></a><a name="filtering"></a>Filtrering

Filtrering giver en mere avanceret og fleksibel må de at kontrollere, hvilke poster der skal vises på en liste eller medtages i en rapport eller XMLport. Der er to vigtige forskelle mellem søgning eller filtrering, som beskrevet i nedenstående tabel.

|| **Søgning** | **Filtrering** |
|--|----------|------------|
| **Relevante felter** | Søger på tværs af alle de felter, der kan ses på siden. | Filtrerer et eller flere felter hver for sig og vælger fra et felt i tabellen, herunder felter, ikke der kan ses på siden. |
| **Matching** | Viser poster med felter, der stemmer overens med søgeteksten, uanset store eller små bogstaver eller placeringen af teksten. | Viser poster, hvor feltet nøjagtigt svarer til filteret, og der skelnes mellem små og store bogstaver, medmindre der er angivet særlige filtersymboler.

Filtrering giver dig mulighed at få vist poster for bestemte konti eller kunder, datoer, beløb og andre oplysninger ved at angive filterkriterier. Kun poster, der opfylder de kriterier, som vises på listen, medtages i rapporten, kørslen eller XMLport. Hvis du angiver kriterier for flere felter, vises kun poster, der svarer til alle kriterier.

I forbindelse med lister vises filtrene i en filterrude, der vises til venstre på listen, når du aktiverer den. For rapporter, kørsler og XMLporte kan filtrene ses direkte på anmodningssiden.

### <a name="filtering-with-option-fields"></a>Filtrere med indstillingsfelter

I forbindelse med "almindelige" felter, der indeholder data, opsætningsdata eller virksomhedsdata, kan du indsætte filtre både ved at vælge data og indtaste filterværdier, og du kan bruge symboler til at angive avancerede filterkriterier. Du kan finde flere oplysninger i [Angivelse af filerkriterier](ui-enter-criteria-filters.md#entering-filter-criteria).

Ved felter af typen **Indstilling** kan du imidlertid kun angive et filter ved at vælge en eller flere indstillinger på en rulleliste med tilgængelige indstillinger. Et eksempel på et indstillingsfelt er feltet **Status** på siden **Salgsordrer**.

> [!NOTE]
> Hvis du vælger flere indstillinger som en filterværdi, defineres relationen mellem indstillingerne som *OR*. Hvis du f.eks. både markerer afkrydsningsfeltet **Åbne** og afkrydsningsfeltet **Frigivet** i filterfeltet **Status** på siden **Salgsordrer**, betyder det, at salgsordrer, der enten er åbne eller frigivne, vises.

### <a name="setting-filters-on-lists"></a>Angive filtre på lister

På lister kan du indstille filtre ved hjælp af filterruden. Hvis du vil have vist filterruden for en liste, skal du vælge rullepilen ud for navnet på siden og derefter vælge handlingen **Vis filterrude**. Du kan også trykke på **Skift+F3**.

Hvis du vil have vist filterruden for kolonne på en liste, skal du vælge rullepilen og derefter vælge handlingen **Filter**. Du kan også trykke på **Skift+F3**. Filterruden åbnes med den valgte kolonne vist som filterfelt i sektionen **Filtrer listen efter**.

Filterruden viser de aktuelle filtre på en liste, og gør det muligt at angive dine egne brugerdefinerede filtre i et eller flere felter ved at vælge handlingen **+ Filter**.

 En filterrude er inddelt i tre afsnit: **Visninger**, **Filtrer listen efter** og **Filtrer totaler efter**:

- **Visninger**

  Nogle lister indeholder sektionen **Visninger**. Visninger er variationer af listen, der er forudkonfigureret med filtre. Du kan definere og gemme så mange visninger, du ønsker, pr. liste. Visningerne er tilgængelige for dig på alle de enheder, du logger på. Du kan finde flere oplysninger i [Gemme og tilpasse listevisninger](ui-views.md).

- **Filtrer listen efter**

  Det er i denne sektion, du kan tilføje filtre i bestemte felter for at reducere antallet af viste poster. Hvis du vil tilføje et filter, skal du vælge handlingen **+ Filter**. Når du vil tilføje et filter, skal du skrive navnet på det felt, du vil filtrere listen efter, eller vælge et felt på rullelisten.

- **Filtrer totaler efter**

  Nogle lister, der viser beregnede felter, som beløb og antal, indeholder sektionen **Filtrer totaler efter**, hvor du kan justere forskellige dimensioner, der påvirker beregninger. Hvis du vil tilføje et filter, skal du vælge handlingen **+ Filter**. Når du vil tilføje et filter, skal du skrive navnet på det felt, du vil filtrere listen efter, eller vælge et felt på rullelisten.

  > [!NOTE]
  > Filtre i sektionen **Filtrer totaler efter** styres af FlowFilters i sideopsætningen. Du kan finde tekniske oplysninger i [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).

Du kan angive et enkelt filter direkte på en liste under brug af filterruden, dvs. et filter, hvor der kun vises poster med den samme værdi som i den markerede celle. Vælg en celle på listen, vælg rullepilen, og vælg derefter handlingen **Filtrer til denne værdi**. Du kan også trykke på **Alt+F3**.

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a>Angive filtre i rapporter, kørsler og XMLporte

For rapporter og XMLporte kan filtrene ses direkte på anmodningssiden. På anmodningssiden vises de senest anvendte filtre på grundlag af dit valg i feltet **Brug standardværdier fra**. Du kan finde flere oplysninger i [Bruge gemte indstillinger](ui-work-report.md#SavedSettings).

**Filter**-hovedsektionen viser de standardfilterfelter, som du kan bruge til at afgrænse, hvilke poster der skal medtages i rapporten eller i XMLport. Hvis du vil tilføje et filter, skal du vælge handlingen **+ Filter**. Når du vil tilføje et filter, skal du skrive navnet på det felt, du vil filtrere listen efter, eller vælge et felt på rullelisten.

I sektionen **Filtrer totaler efter** kan du justere forskellige dimensioner, der påvirker beregninger i rapporten eller i XMLport. Hvis du vil tilføje et filter, skal du vælge handlingen **+ Filter**. Når du vil tilføje et filter, skal du skrive navnet på det felt, du vil filtrere listen efter, eller vælge et felt på rullelisten.

## <a name="entering-filter-criteria"></a>Angivelse af filterkriterier

Både i filterruden og på en anmodningsside angiver du filterkriterierne i feltet under filterfeltet.

Filterfeltets type er bestemmende for, hvilke kriterier du kan angive. For eksempel kan du, når du filtrerer et felt, der har faste værdier, kun vælge mellem disse værdier. Du kan finde yderligere oplysninger om særlige filtersymboler i [Filterkriterier](#FilterCriteria) og [Filtertokens](#FilterTokens).

Kolonner, som allerede indeholder filtre, er angivet med ikonet ![Filter](media/ui-search/filter-icon.png "Filter-ikon") i kolonneoverskriften. Hvis du vil fjerne et filter, skal du vælge rullepilen og derefter vælge handlingen **Ryd filter**.

> [!TIP]
> Fremskynd søgning efter og analyse af dine data ved hjælp af kombinationer af genvejstaster. For f.eks. at markere et felt skal du bruge **Skift + Alt + F3** for at føje dette felt til filterruden, angive filterkriterierne, bruge **Ctrl + Enter** for at vende tilbage til rækkerne, vælge et andet felt og bruge **Alt + F3** til at filtrere til værdien. Du kan finde flere oplysninger i [Tastaturgenveje](keyboard-shortcuts.md#KeyboardFilter).

### <a name="filter-criteria-and-operators"></a><a name="FilterCriteria"> </a>Filterkriterier og -operatorer

Når du angiver kriterier, kan du bruge alle de tal og bogstaver, som du plejer at bruger i feltet. Men der er også en række specielle symboler, som du kan bruge som operatorer for at filtrere resultaterne yderligere. I følgende afsnit beskrives disse symboler, og hvordan de bruges som operatorer i filtre.

> [!TIP]
> Du kan finde flere oplysninger om filtrering af dato og klokkeslæt i [Arbejde med kalenderdatoer og-klokkeslæt](ui-enter-date-ranges.md).

> [!IMPORTANT]
> - Der kan være situationer, hvor den værdi, der skal filtreres efter, indeholder et symbol, som er en operator. Du kan finde flere oplysninger om håndtering af disse situationer i [Filtrering på værdier, der indeholder symboler](#symbols) for at få flere oplysninger om håndtering af denne situation.
>
> - Hvis der er mere end 200 operatorer i et enkelt filter, vil systemet automatisk gruppere nogle udtryk i parenteser `()` med henblik på behandling. Det har ingen indflydelse på filteret eller resultaterne.  

#### <a name="-interval"></a>(..) Interval

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`1100..2100`|Tal fra 1100 til og med 2100.|  
|`..2500`|Konti til og med 2500|  
|`..12 31 00`|Datoer til og med 31-12-00.|  
|`P8..`|Oplysninger for regnskabsperiode 8 og frem|  
|`..23`|Fra begyndelsesdatoen til 23-aktuel måned-aktuelt år 23.59.59|  
|`23..`|Fra 23-aktuel måned-aktuelt år 0.00.00 til sluttidspunktet|  
|`22..23`|Fra den 23-aktuel måned-aktuelt år 0.00.00 til 22-aktuel måned-aktuelt år 22.59.59|  

#### <a name="124-eitheror"></a>(&#124;) Enten/eller

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`1200|1300`|Tal med 1200 eller 1300.|  

#### <a name="-not-equal-to"></a>(<>) Ikke lig med  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`<>0`|Alle tal undtagen 0<br /><br /> I SQL Server Option kan du kombinere dette symbol med et udtryk med jokertegn. <>A* betyder f.eks. ikke lig med tekst, der starter med A.|  

#### <a name="-greater-than"></a>(>) Større end  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`>1200`|Tal større end 1200|  

#### <a name="-greater-than-or-equal-to"></a>(>=) Større end eller lig med  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`>=1200`|Tal lig med eller større end 1200|  

#### <a name="-less-than"></a>(<) Mindre end  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`<1200`|Tal mindre end 1200|  

#### <a name="-less-than-or-equal-to"></a>(<=) Mindre end eller lig med  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`<=1200`|Tal lig med eller mindre end 1200|  

#### <a name="-and"></a>(&) Og  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`>200&<1200`|Tal større end 200 og mindre end 1200|  

#### <a name="-an-exact-character-match"></a>('') Tegn, der stemmer nøjagtigt overens  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`'man'`|Tekst, der svarer nøjagtigt til **man**, og der skelnes mellem store og små bogstaver.|  

#### <a name="-case-insensitive"></a>(@) Ingen forskel på store og små bogstaver  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`@man*`|Tekst, der starter med **man**, og der skelnes mellem store og små bogstaver.|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Mange ukendte tegn

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`*Co*`|Tekst, der indeholder **A/S**, og der skelnes mellem store og små bogstaver.|  
|`*Co`|Tekst, der ender på **A/S**, og der skelnes mellem store og små bogstaver.|  
|`Co*`|Tekst, der begynder med **A/S**, og der skelnes mellem store og små bogstaver.|  

#### <a name="-one-unknown-character"></a>(?) Ét ukendt tegn  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`Hans?n`|Tekst som f.eks. **Hansen** eller **Hanson**|  

#### <a name="combined-format-expressions"></a>Kombinerede formatudtryk  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Tallet 5999 og tallene fra og med 8100 til og med 8490.|  
|`..1299|1400..`|Medtag poster med et tal mindre end eller lig med 1299, eller tal lig med 1400 eller derover (alle tal undtagen 1300 til og med 1399).|  
|`>50&<100`|Medtag poster med tal større end 50 og mindre end 100 (tal fra 51 til og med 99).|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a>Filtrere på værdier, der indeholder symboler

Der kan være tilfælde, hvor feltværdier indeholder et af følgende symboler:

- &
- (
- )
- =
- &#124;

Hvis du vil filtrere efter et af disse symboler, skal du placere filterudtrykket i anførselstegn (' '). Hvis du f.eks. vil filtrere efter poster, der starter med teksten *J & V*, er filterudtrykket `'J & V*'`.

Dette krav er ikke nødvendigt for andre symboler.

### <a name="filter-tokens"></a><a name="FilterTokens"> </a>Filtertokens

Når du angiver filterkriterier, kan du også skrive ord, der har en særlig betydning, kaldet filtertokens. Når du har angivet et tokenordet, erstattes ordet af den eller de værdier, det repræsenterer. Med filter-tokens bliver filtrering nemmere ved at reducere behovet for at navigere til andre sider for at søge efter værdier, du vil føje til filteret. Tabellerne nedenfor beskriver nogle af de tegn, du kan skrive som filterkriterier.

> [!TIP]
> Din organisation bruger muligvis brugerdefinerede tokens. For at få mere at vide om det komplette sæt tokens, der er tilgængelige for dig, eller tilføje flere brugerdefinerede tokens, skal du kontakte din administrator. Du kan finde tekniske oplysninger i [Tilføje filtertokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).

#### <a name="me-or-userid-records-assigned-to-you"></a>(%me eller %userid) Poster, der er tildelt til dig

Brug `%me` eller `%userid` ved filtrering af felter, der indeholder bruger-id'et, f.eks. feltet **Tildelt til bruger-id**, for at få vist alle poster, der er tildelt til dig.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%me`<br />eller<br />`%userid`|Poster, der er knyttet til din brugerkonto. |  

#### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Debitorer i Mine debitorer

Brug `%mycustomers` i debitorfeltet **Nej** til at vise alle poster for debitorer, der står på listen **Mine debitorer** i dit rollecenter.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%mycustomers`|Debitorer i **Mine debitorer** i dit rollecenter. |  

#### <a name="myitems-items-in-my-items"></a>(%myitems) Varer i Mine varer

Brug `%myitems` i varefeltet **Nej** til at vise alle poster for varer, der står på listen **Mine varer** i dit rollecenter.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%myitems`|Varer i **Mine varer** i dit rollecenter. |  

#### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Kreditorer i Mine kreditorer

Brug `%myvendors` i kreditorfeltet **Nej** til at vise alle poster for kreditorer, der står på listen **Mine kreditor** i dit rollecenter.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%myvendors`|Kreditorer i **Mine kreditorer** i dit rollecenter. |  

## <a name="see-also"></a>Se også

[Ofte stillede spørgsmål om søgning og filtrering](ui-search-filter-faq.md)  
[Gemme og tilpasse listevisninger](ui-views.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]