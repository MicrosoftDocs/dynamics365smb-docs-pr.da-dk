---
title: Definere granulerede tilladelser
description: Dette emne beskriver, hvordan du definerer granulerede tilladelser, så bestemte brugere får adgang til objekter og tildeler dem tilladelsessæt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 1, 119, 8930, 9807, 9808, 9830, 9831
ms.date: 03/24/2022
ms.author: edupont
ms.openlocfilehash: ca0373fc55fb14d43dae9ce5bc51c0063c88a2af
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522508"
---
# <a name="assign-permissions-to-users-and-groups"></a>Tildele rettigheder til brugere og grupper

Administratorer bruger [!INCLUDE[prod_short](includes/prod_short.md)]-sikkerhedssystemet til at styre, hvilke objekter en bruger kan få adgang til inden for hver database eller hvert miljø, sammen med de licenser, der er tildelt. Du kan angive for hver bruger, om de kan læse, ændre eller indtaste data i de valgte databaseobjekter. Du kan finde flere oplysninger ved at se [Datasikkerhed](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) i indholdet til udviklere og it-eksperter for [!INCLUDE[prod_short](includes/prod_short.md)]

Før du tildeler rettigheder til brugere og brugergrupper, skal du definere, hvem der kan logge på, ved at oprette brugere ifølge licensen, som det er defineret i Microsoft 365 Administration. Du kan finde flere oplysninger i [Oprette brugere i henhold til licenser](ui-how-users-permissions.md).

I [!INCLUDE[prod_short](includes/prod_short.md)]er der to niveauer af rettigheder til databaseobjekter:

- Overordnede rettigheder ifølge licensen, også kaldet berettigelser.

  Licenserne omfatter standardtilladelsessæt. Fra og med 2022 udgivelsesbølge 1 kan administratorer tilpasse disse standardtilladelser til de relevante licenstyper. Du kan finde flere oplysninger i [konfigurere tilladelser på baggrund af licenser](ui-how-users-permissions.md#licensespermissions).  
- Mere detaljerede rettigheder, der er tildelt i [!INCLUDE[prod_short](includes/prod_short.md)].

  Denne artikel beskriver, hvordan du kan definere, bruge og anvende tilladelser i [!INCLUDE [prod_short](includes/prod_short.md)] til at ændre standardkonfigurationen.  

[!INCLUDE [prod_short](includes/prod_short.md)] online indeholder standardbrugergrupper, der automatisk tildeles til brugere baseret på deres licens. Du kan ændre standardkonfigurationen ved at ændre eller tilføje brugergrupper, tilladelsessæt og tilladelser. I følgende tabel beskrives nøgle scenarier, der bruges til at ændre standardtilladelserne.  

|Hvis du vil  |Skal du se  |
|---------|---------|
|Hvis du vil gøre det nemmere at administrere rettigheder for flere brugere, kan du organisere dem i brugergrupper og dermed tildele eller ændre et rettighedssæt for mange brugere i én handling.| [Sådan administreres rettigheder via brugergrupper](#to-manage-permissions-through-user-groups) |
|Sådan administreres tilladelsessæt for bestemte brugere | [Sådan tildeles rettighedssæt til brugere](#to-assign-permission-sets-to-users) |
|Sådan defineres et tilladelsessæt|[Sådan oprettes eller redigeres et rettighedssæt](#to-create-or-modify-a-permission-set)|
|Sådan administreres specifikke tilladelser|[Sådan oprettes eller redigeres rettigheder manuelt](#to-create-or-modify-permissions-manually)|
|Sådan får du vist eller fejlfinder en brugers rettigheder|[Sådan får du vist en oversigt over en brugers rettigheder](#to-get-an-overview-of-a-users-permissions)|
|Sådan kan du se mere om sikkerhed på postniveau|[Sikkerhedsfiltre begrænser en brugers adgang til bestemte poster i en tabel](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> En ekstra metode til at definere, hvilke funktioner en bruger har adgang til, er ved at indstille feltet **Oplevelse** på siden **Virksomhedsoplysninger**. Du kan finde flere oplysninger i [Ændre, hvilke funktioner der vises](ui-experiences.md).
>
> Du kan også definere, hvad brugere ser i brugergrænsefladen, og hvordan de interagerer med de tilladte funktioner via sider. Du kan gøre dette via profiler, som du tildeler til forskellige typer brugere, i henhold til deres jobrolle eller afdeling. Du kan finde flere oplysninger i [Administrere profiler](admin-users-profiles-roles.md) og [Tilpasning af [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## <a name="to-manage-permissions-through-user-groups"></a>Sådan administreres rettigheder via brugergrupper

Brugergrupper hjælper dig med at administrere tilladelsessæt på tværs af virksomheden. [!INCLUDE [prod_short](includes/prod_short.md)] online indeholder standardbrugergrupper, der automatisk tildeles til brugere baseret på deres licens. Du kan føje brugere til en brugergruppe manuelt, og du kan oprette nye brugergrupper som kopier af eksisterende.  

Du starter med at oprette en brugergruppe. Derefter kan du tildele et rettighedssæt til gruppen for at definere, hvilket objekt brugere af gruppen har adgang til. Når du føjer en bruger til gruppen, gælder de rettighedssæt, der er defineret for gruppen, for brugeren.

Rettighedssæt, der er tildelt til en bruger via en brugergruppe, forbliver synkroniserede, så en ændring af brugergruppens rettigheder overføres automatisk til brugeren. Hvis du fjerner en bruger fra en brugergruppe, tilbagekaldes de involverede rettigheder automatisk.

### <a name="to-add-users-to-a-user-group"></a>Sådan føjes brugere til en brugergruppe

Følgende procedure beskriver, hvordan du opretter brugergrupper manuelt. Hvis du vil oprette brugergrupper automatisk, skal du se [Sådan kopieres en brugergruppe og alle dens rettighedssæt](#to-copy-a-user-group-and-all-its-permission-sets).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugergrupper**, og vælg derefter det relaterede link.

    1. Du kan også vælge handlingen **Brugergrupper** på siden **Brugere**.
2. Du kan også vælge handlingen **Medlemmer af brugergruppe** på siden **Brugergruppe**.
3. Du kan også vælge handlingen **Medlemmer af brugergruppe** på siden **Tilføj brugere**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Sådan kopierer du en brugergruppe og alle dens rettighedssæt

Hvis du hurtigt vil definere en ny brugergruppe, kan du kopiere alle rettighedssæt fra en eksisterende brugergruppe til den nye brugergruppe.

> [!NOTE]
> Brugergruppemedlemmerne kopieres ikke til den nye brugergruppe. Du skal tilføje dem bagefter. Yderligere oplysninger finder du i afsnittet [Sådan tilføjes brugere til en brugergrupper](#to-add-users-to-a-user-group).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugergrupper**, og vælg derefter det relaterede link.
2. Vælg de brugergrupper, som du vil kopiere, og vælg derefter handlingen **Kopiér brugergruppe**.
3. I feltet **Ny brugergruppekode** skal du angive et navn til gruppen og derefter vælge knappen **OK**.

Den nye gruppe tilføjes på siden **Brugergrupper**. Fortsæt for at tilføje brugere. Yderligere oplysninger finder du i afsnittet [Sådan tilføjes brugere til en brugergrupper](#to-add-users-to-a-user-group).  

### <a name="to-assign-permission-sets-to-user-groups"></a>Sådan tildeles rettighedssæt til brugergrupper

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugergrupper**, og vælg derefter det relaterede link.
2. Vælg den brugergruppe, du vil tildele rettigheden til.  

    Ethvert rettighedssæt, der allerede er tildelt brugeren, vises i faktaboksen **Rettighedssæt**.
3. Vælg handlingen **Brugerrettighedssæt** for at åbne siden **Brugerrettighedssæt**.
4. Udfyld felterne efter behov på en ny linje på siden **Brugerrettighedssæt**.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Sådan tildeles et rettighedssæt på siden **Rettighedssæt efter brugergruppe**

Følgende procedure beskriver, hvordan du tildeler rettighedssæt til en brugergruppe på siden **Rettighedssæt efter brugergruppe**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugere**, og vælg derefter det relaterede link.
2. På siden **Brugere** skal du vælge den relevante bruger og derefter vælge handlingen **Rettighedssæt efter brugergruppe**.
3. På siden **Rettighedssæt efter brugergruppe** skal du markere afkrydsningsfeltet **[brugergruppenavn]** på en linje for det relevante rettighedssæt for at tildele sættet til brugergruppen.
4. Marker afkrydsningsfeltet **Alle brugergrupper** for at tildele rettighedssættet til alle brugergrupper.

Du kan også tildele rettighedssæt direkte til brugere.

## <a name="to-assign-permission-sets-to-users"></a>Sådan tildeles rettighedssæt til brugere

Et rettighedssæt er en samling rettigheder til bestemte databaseobjekter. Alle brugere skal være tildelt et eller flere rettighedssæt, før de kan få adgang til [!INCLUDE[prod_short](includes/prod_short.md)]. 

En [!INCLUDE[prod_short](includes/prod_short.md)]-løsning indeholder typisk et antal foruddefinerede rettighedssæt, der er tilføjet af Microsoft eller din løsningsudbyder. Du kan også tilføje nye rettighedssæt, der er skræddersyet til at opfylde din organisations behov. Du kan finde flere oplysninger i afsnittet [Sådan oprettes eller redigeres et rettighedssæt](#to-create-or-modify-a-permission-set).

> [!NOTE]
> Hvis du ikke vil begrænse en brugers adgang mere, end det allerede er defineret af licensen, kan du tildele et særligt rettighedssæt, der kaldes SUPER, til brugeren. Dette rettighedssæt sikrer, at brugeren kan få adgang til alle de objekter, der er angivet i licensen.
>
> En bruger med den grundlæggende licens og SUPER-rettighedssættet har adgang til flere funktioner end brugere med licensen Teammedlem og SUPER-rettighedssættet.

Du kan tildele rettighedssæt til brugere på to måder:

- Fra siden **Brugerkort** ved at vælge de rettighedssæt, der skal tildeles brugeren.
- Fra siden **Rettighedssæt efter bruger** ved at vælge de brugere, der er tildelt et rettighedssæt.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Sådan tildeles et rettighedssæt på et brugerkort

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugere**, og vælg derefter det relaterede link.
2. Vælg den bruger, du vil tildele rettigheden til.
Ethvert rettighedssæt, der allerede er tildelt brugeren, vises i faktaboksen **Rettighedssæt**.
3. Vælg handlingen **Rediger** for at åbne siden **Brugerkort**.
4. I oversigtspanelet **Brugerrettighedssæt** skal du udfylde felterne efter behov på en ny linje. Du kan finde flere oplysninger i [Sådan oprettes eller redigeres et rettighedssæt](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Sådan tildeles et rettighedssæt på siden Rettighedssæt efter bruger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugere**, og vælg derefter det relaterede link.
2. Du kan også vælge handlingen **Rettighedssæt efter bruger** på siden **Brugere**.
3. På siden **Rettighedssæt efter bruger** skal du markere afkrydsningsfeltet **[brugernavn]** på en linje for det relevante rettighedssæt for at tildele sættet til brugeren.

    Marker afkrydsningsfeltet **Alle brugere** for at tildele rettighedssættet til alle brugere.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Sådan får du vist en oversigt over en brugers rettigheder

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugere**, og vælg derefter det relaterede link.
2. Åbn den relevante brugers kort.
3. Vælg handlingen **Gældende rettigheder**.

    Delen **Rettigheder** viser alle elementer i databasen, som brugeren har adgang til. Du kan ikke redigere denne sektion.

    Delen **Efter rettighedssæt** viser de tildelte rettighedssæt, som rettighederne tildeles via til brugeren, kilden og type af rettighedssæt, og i hvilket omfang de forskellige adgangstyper har rettigheder.

    For hver række, du vælger i sektionen **Rettigheder**, viser sektionen **Efter rettighedssæt**, hvilket rettighedssæt eller sæt rettigheden tildeles gennem. I denne sektion kan du redigere værdien i hvert af felterne for de fem adgangstyper **Læserettighed**, **Indsætterettighed**, **Redigeringsrettighed**, **Sletterettighed** og **Udførelsesrettighed**.

    > [!NOTE]  
    > Kun rettighedssæt af typen **Brugerdefineret** kan redigeres.
    >
    > Rækker med kildeberettigelse stammer fra abonnementslicensen. Rettighedsværdierne for rettigheden tilsidesætter værdier i andre rettighedssæt, hvis de ligger på et højere placeringsniveau. En værdi i et ikke-rettighedssæt, der har et højere placeringsniveau end den relaterede værdi i rettighedsfeltet, sættes i parentes for at angive, at det ikke er gældende, fordi det er tilsidesat af rettigheden.
    >
    > Du kan finde en forklaring på placeringsniveauer i [Sådan oprettes eller redigeres rettigheder manuelt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

4. For at redigere et rettighedssæt skal du i delen **Efter rettighedssæt** på linjen for en relevant rettighed angive typen **Brugerdefineret**, vælge et af de fem adgangstypefelter og vælge en anden værdi.

5. For at redigere individuelle rettigheder i rettighedssættet skal du vælge værdien i feltet **Rettighedssæt** for at åbne siden **Rettigheder**. Følg de trin, der er beskrevet i [Sådan oprettes eller redigeres rettighedssæt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Når du redigerer et rettighedssæt, gælder ændringerne også for andre brugere, som rettighedssættet er tildelt til.

### <a name="security-filters-limit-a-users-access-to-specific-records-in-a-table"></a>Sikkerhedsfiltre begrænser en brugers adgang til bestemte poster i en tabel

Når det drejer sig om postbaseret sikkerhed i [!INCLUDE[prod_short](includes/prod_short.md)], kan du bruge filtrene til at begrænse en brugers adgang til data i en tabel. Du kan oprette sikkerhedsfiltre for tabeldata. Et sikkerhedsfilter beskriver et sæt af poster i en tabel, som en bruger har adgang til. For eksempel kan du angive, at en bruger kun skal kunne læse poster, der indeholder oplysninger om en bestemt kunde. Det betyder, at brugeren ikke kan få adgang til de poster, der indeholder oplysninger om andre kunder. Du kan finde flere oplysninger i [Bruge sikkerhedsfiltre](/dynamics365/business-central/dev-itpro/security/security-filters) i administrationsindholdet.


## <a name="to-create-or-modify-a-permission-set"></a>Sådan oprettes eller redigeres et rettighedssæt

Rettighedssæt fungerer som objektbeholdere for rettigheder, så du let kan håndtere flere rettigheder i én post.

> [!NOTE]  
> En [!INCLUDE[prod_short](includes/prod_short.md)]-løsning indeholder typisk et antal foruddefinerede rettighedssæt, der er tilføjet af Microsoft eller din softwareleverandør. Disse rettighedssæt er af typen **System** eller **Udvidelse**. Du kan ikke oprette eller redigere disse typer rettighedssæt eller rettighederne i dem. Du kan dog kopiere dem for at definere dine egne rettighedssæt og rettigheder.
>
> Rettighedssæt, som brugerne opretter fra grunden eller som kopier, er af typen **Brugerdefineret** og kan redigeres.

### <a name="to-create-new-permission-set-from-scratch"></a>Sådan oprettes et nyt rettighedssæt fra bunden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rettighedssæt**, og vælg derefter det relaterede link.
2. For at oprette et nyt rettighedssæt skal du vælge handlingen **Ny**.
3. Udfyld felterne på den nye linje efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Når du har oprettet et rettighedssæt, skal du tilføje de faktiske rettigheder. Du kan finde flere oplysninger i [Sådan oprettes eller redigeres rettigheder manuelt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-copy-a-permission-set"></a>Sådan kopieres et rettighedssæt

Du kan også bruge en kopieringsfunktion til hurtigt at overføre alle rettigheder fra et andet rettighedssæt til et nyt rettighedssæt.

> [!NOTE]  
> Hvis et System-rettighedssættet, som du har kopieret, ændres, får du besked (afhængigt af dit valg), så du kan overveje, om ændringerne skal kopieres eller skrives til dit brugerdefinerede rettighedssæt.

1. På siden **Rettighedssæt** skal du vælge linjen for et bestemt rettighedssæt, som du vil kopiere, og vælg derefter handlingen **Kopiér rettighedssæt**.
2. På siden **Kopiér rettighedssæt** skal du angive navnet på det nye rettighedssæt og derefter vælge knappen **OK**.
3. Marker afkrydsningsfeltet **Informer i tilfælde af ændret rettighedssæt**, hvis du vil bevare en forbindelse mellem de oprindelige og de kopierede rettighedssæt. Forbindelsen bruges derefter til at give dig besked, hvis navnet eller indholdet af det oprindelige rettighedssæt ændres i en fremtidig version, som løsningen opgraderes til senere.

Det nye rettighedssæt, der indeholder alle rettigheder for det kopierede rettighedssæt, tilføjes som en ny linje på siden **Rettighedssæt**. Du kan nu ændre rettigheden i det nye rettighedssæt. Bemærk, at linjerne sorteres alfabetisk inden for hver type.

### <a name="to-export-and-import-a-permission-set"></a>Sådan eksporteres og importeres et tilladelsessæt

Hvis du hurtigt vil oprette tilladelser, kan du importere tilladelsessæt, som du har eksporteret fra en anden [!INCLUDE[prod_short](includes/prod_short.md)]-lejer.

I miljøer med flere lejere indlæses et tilladelsessæt i en bestemt lejer, dvs. omfanget af importen er "lejer".

1. I lejer 1 på siden **Rettighedssæt** skal du vælge linjen eller de linjer til rettighedssættene, der skal eksporteres, og derefter vælge handlingen **Eksportér rettighedssæt**.

    En XML-fil oprettes i mappen Overførsler på din computer. Som standard hedder filen "Export Permission Sets.xml"

2. I lejer 2 på siden **Rettighedssæt** skal du vælge handlingen **Importer rettighedssæt**.
3. På dialogsiden **Importer rettighedssæt** skal du overveje, om du vil flette eksisterende rettighedssæt med nye rettighedssæt i XML-filen.

    Hvis du markerer afkrydsningsfeltet **Opdater eksisterende tilladelser**, flettes de eksisterende rettighedssæt med samme navn som dem i XML-filen med de importerede rettighedssæt.

    Hvis du ikke markerer afkrydsningsfeltet **Opdater eksisterende tilladelser**, springes rettighedssæt med samme navn som dem i XML-filen over, når der importeres. Hvis det er tilfældet, vil du få besked om, hvilke rettighedssæt der springes over.

4. På dialogsiden **Import** skal du finde og vælge den .xml-fil, der skal importeres, og derefter vælge handlingen **Åbn**.

Rettighedssættene importeres.

## <a name="to-create-or-modify-permissions-manually"></a>Sådan oprettes eller redigeres rettigheder manuelt

Denne fremgangsmåde beskriver, hvordan du kan tilføje eller redigere rettigheder manuelt. Du kan også få en rettighed oprettet automatisk på grundlag af dine handlinger i brugergrænsefladen. Du kan finde flere oplysninger i [Sådan opretter eller redigerer du rettigheder ved at registrere dine handlinger](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions).

> [!NOTE]
> Når du redigerer en rettighed og dermed relaterede rettighedssæt, gælder ændringerne også for andre brugere, som rettighedssættet er tildelt til.

1. På siden **Rettighedssæt** skal du vælge linjen for et bestemt rettighedssæt og derefter vælge handlingen **Rettigheder**.
2. På siden **Rettigheder** kan du oprette en ny linje eller redigere felterne på en eksisterende linje.

I hvert af felterne for de fem adgangstyper **Læserettighed**, **Indsætterettighed**, **Redigeringsrettighed**, **Sletterettighed** og **Udførelsesrettighed** kan du vælge en af følgende tre rettighedsindstillinger:

|Indstilling|Beskrivelse|Placeringsniveau|
|------|-----------|-------|
|**Ja**|Brugeren kan udføre handlingen på det pågældende objekt.|Højeste|
|**Indirekte**|Brugeren kan udføre handlingen på det pågældende objekt, men kun via et relateret objekt, som brugeren har fuld adgang til. Du kan finde flere oplysninger om indirekte rettigheder [Rettighedsegenskab](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property) i hjælpen til udviklere og it-eksperter|Næsthøjeste|
|**Tomt**|Brugeren kan ikke udføre handlingen på det pågældende objekt.|Laveste|

> [!IMPORTANT]
> Vær forsigtig, når du tilknytter **Indsæt tilladelse** eller **Ret tilladelse** til tabellen **9001-brugergruppemedlem** eller **9003-brugergruppetilladelsessæt**. Alle brugere, der har fået tildelt et tilladelsessæt, kan tildele sig selv til andre brugergrupper, som igen kan give dem uønskede rettigheder.

### <a name="example---indirect-permission"></a>Eksempel - indirekte rettighed

Du kan tildele en indirekte rettighed for kun at bruge et objekt gennem et andet objekt.
En bruger kan f.eks. have tilladelse til at køre codeunit 80, salg-post Codeunit Salgs-post udfører mange opgaver, herunder ændring af tabel 37, Salgslinje. Når brugeren bogfører et salgsdokument, codeunit Salgs-post, kontrollerer [!INCLUDE[prod_short](includes/prod_short.md)], om brugeren har rettighed til at ændre tabellen Salgslinje. Hvis ikke, kan codeunit'en ikke udføre sine opgaver, og brugeren får en fejlmeddelelse. I så fald kører codeunit'en korrekt.

Men brugeren behøver ikke at have fuld adgang til tabellen Salgslinje for at køre codeunit'en. Hvis brugeren har indirekte rettighed til tabellen Salgslinje, kører codeunit'en Salgs-post korrekt. Når en bruger har indirekte rettighed, kan brugeren kun redigere tabellen Salgslinje ved at køre codeunit'en salgs-post eller et andet objekt, der har rettighed til at ændre tabellen Salgslinje. Brugeren kan kun redigere tabellen Salgslinje, når det sker fra understøttede funktionalitetsområder. Brugeren kan ikke køre funktionen ved et uheld eller skadeligt ved andre metoder.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Sådan opretter eller redigerer du rettigheder ved at registrere dine handlinger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rettighedssæt**, og vælg derefter det relaterede link.

    Du kan også vælge handlingen **Rettighedssæt** på siden **Brugere**.
2. Vælg handlingen **Ny** på siden **Rettighedssæt**.
3. Udfyld felterne på en ny linje efter behov.
4. Vælg handlingen **Rettigheder**.
5. På siden **Rettigheder** skal du vælge handlingen **Registrer rettigheder** og derefter vælge handlingen **Start**.

    Der startes en registreringsproces, som registrerer alle dine handlinger i brugergrænsefladen.
6. Gå til de forskellige sider og aktiviteter i [!INCLUDE[prod_short](includes/prod_short.md)], som du vil give brugerne med dette rettighedssæt adgang til. Du skal udføre de opgaver, som du vil registrere rettigheder for.
7. Når du vil afslutte registreringen, skal du vende tilbage til siden **Rettigheder** og derefter vælge handlingen **Stop**.
8. Vælg knappen **Ja** for at føje de registrerede rettigheder til det nye rettighedssæt.
9. Angiv, om brugerne skal kunne indsætte, redigere eller slette poster i de registrerede tabeller for hvert objekt på listen over registrerede elementer.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Sådan fjernes forældede rettigheder fra alle rettighedssæt

1. På siden **Rettighedssæt** skal du vælge handlingen **Fjern forældede rettigheder**.

## <a name="to-set-up-user-time-constraints"></a>Sådan opsættes tidsbegrænsninger for brugere

Administratorer kan definere perioder, hvor angivne brugere kan bogføre, og de kan også angive, om systemet skal registrere, hvor lang tid brugerne er logget på. Administratorer kan også knytte ansvarscentre til brugere. Du kan finde flere oplysninger i [Arbejde med ansvarscentre](inventory-responsibility-centers.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugeropsætning**, og vælg derefter det relaterede link.
2. Når siden **Brugeropsætning** åbnes, skal du vælge handlingen **Ny**.
3. I feltet **Bruger-ID** skal du angive ID'et for en bruger, eller vælge feltet for at få vist alle aktuelle Windows-brugere i systemet.
4. Udfyld felterne efter behov.

## <a name="viewing-permission-changes-telemetry"></a>Få vist ændringer af telemetri 

Du kan oprette [!INCLUDE[prod_short](includes/prod_short.md)] for at sende ændringer, der er udført for at få tilladelse til en Application Insights-ressource i Microsoft Azure. Derefter kan du bruge Azure Monitor til at oprette rapporter og konfigurere påmindelser i de indsamlede data. Du kan finde flere oplysninger i følgende artikler i [!INCLUDE[prod_short](includes/prod_short.md)] hjælp til udviklere og it-eksperter:

- [Overvåge og analysere telemetri - aktivere Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analysere feltovervågningstelemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="see-also"></a>Se også

[Oprette brugere i henhold til licenser](ui-how-users-permissions.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Tilpasning [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Blive klar til at handle](ui-get-ready-business.md)  
[Opsætning](admin-setup-and-administration.md)  
[Føje brugere til Microsoft 365 til virksomheder](/microsoft-365/admin/add-users/add-users)  
[Sikkerhed og beskyttelse i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) i hjælp til udviklere og it-eksperter  
[Tildele brugere en telemetri-id](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]