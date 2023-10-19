---
title: Definere granulerede tilladelser
description: 'Denne artikel beskriver, hvordan du definerer granularitet-tilladelser og tildeler hver enkelt bruger de tilladelsessæt, som de skal bruge for at udføre deres arbejde.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# <a name="assign-permissions-to-users-and-groups"></a>Tildele rettigheder til brugere og grupper

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

[!INCLUDE[prod_short](includes/prod_short.md)]-sikkerhedssystemet kontrollerer, hvilke objekter en bruger kan få adgang til inden for hver database eller hvert miljø, sammen med brugerens licens. Du kan angive for hver bruger, om de kan læse, ændre eller indtaste data i de databaseobjekter. Du kan finde flere oplysninger ved at se [Datasikkerhed](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) i indholdet til udviklere og it-eksperter for [!INCLUDE[prod_short](includes/prod_short.md)]

Før du tildeler rettigheder til brugere og brugergrupper, skal du definere, hvem der kan logge på, ved at oprette brugere ifølge deres licens. Du kan finde flere oplysninger i [Oprette brugere i henhold til licenser](ui-how-users-permissions.md).

I [!INCLUDE[prod_short](includes/prod_short.md)]er der to niveauer af rettigheder til databaseobjekter:

- Overordnede rettigheder ifølge licensen, også kaldet berettigelser.

  Licenserne omfatter standardtilladelsessæt. Fra og med 2022 udgivelsesbølge 1 kan administratorer tilpasse disse standardtilladelser til de relevante licenstyper. Du kan finde flere oplysninger i [konfigurere tilladelser på baggrund af licenser](ui-how-users-permissions.md#licensespermissions).  

- Detaljerede tilladelser, som du tildeler i [!INCLUDE[prod_short](includes/prod_short.md)].

Denne artikel beskriver, hvordan du kan definere, bruge og anvende tilladelser i [!INCLUDE [prod_short](includes/prod_short.md)] til at ændre standardkonfigurationen.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Du kan finde flere oplysninger i [Delegeret administratoradgang til Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)] online indeholder standardbrugergrupper, der automatisk tildeles til brugere baseret på deres licens. Du kan ændre standardkonfigurationen ved at ændre eller tilføje sikkerhedsgrupper, tilladelsessæt og tilladelser. I følgende tabel beskrives nøgle scenarier, der bruges til at ændre standardtilladelserne.  

|Hvis du vil  |Skal du se  |
|---------|---------|
|Hvis du vil gøre det nemmere at administrere rettigheder for flere brugere, kan du organisere dem i sikkerhedsgrupper og dermed tildele eller ændre et rettighedssæt for mange brugere i én handling.| [Sådan administreres rettigheder via brugergrupper](#to-manage-permissions-through-user-groups) |
|Sådan administreres tilladelsessæt for bestemte brugere | [Sådan tildeles rettighedssæt til brugere](#to-assign-permission-sets-to-users) |
|Sådan defineres et tilladelsessæt|[Oprette et rettighedssæt](#to-create-a-permission-set)|
|Sådan får du vist eller fejlfinder en brugers rettigheder|[Sådan får du vist en oversigt over en brugers rettigheder](#to-get-an-overview-of-a-users-permissions)|
|Sådan kan du se mere om sikkerhed på postniveau|[Sikkerhedsfiltre begrænser en brugers adgang til bestemte poster i en tabel](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> En bredere metode til at definere, hvilke funktioner en bruger har adgang til, er ved at indstille feltet **Oplevelse** på siden **Virksomhedsoplysninger**. Du kan finde flere oplysninger i [Ændre, hvilke funktioner der vises](ui-experiences.md).
>
> Du kan også definere de funktioner, der er tilgængelige for brugere i brugergrænsefladen, og hvordan de interagerer med de tilladte funktioner via sider. Du kan gøre dette via profiler, som du tildeler til forskellige typer brugere, i henhold til deres jobrolle eller afdeling. Du kan finde flere oplysninger i [Administrere profiler](admin-users-profiles-roles.md) og [Tilpasning af [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## <a name="to-create-a-permission-set"></a>Oprette et rettighedssæt

> [!NOTE]
> I 2022 udgivelsesbølge 2 gjorde vi det nemmere at føje tilladelser til tilladelsessæt. I stedet for at tilføje tilladelser enkeltvis, kan du tilføje hele tilladelsessæt. Hvis det er nødvendigt, kan du udelukke individuelle tilladelser i dem. Du kan finde flere oplysninger i [Tilføje andre rettighedssæt](#to-add-other-permission-sets). For at gøre dette skal vi erstatte siden med tilladelsessættet med en ny. De vigtigste forskelle er de nye ruder for **tilladelsessæt** og **resultater** samt faktaboksen **inkludere tilladelser**. Hvis du vil fortsætte med at bruge siden erstattede tilladelser, skal du vælge handlingen **tilladelser (ældre)** på siden **tilladelsessæt**.

Vedligeholdelse er også nemmere. Når du tilføjer en systemtilladelse, opdateres det brugerdefinerede tilladelsessæt automatisk med de ændringer, som Microsoft foretager af disse tilladelser.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rettighedssæt**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne på den nye linje efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg handlingen **Rettigheder**.
5. På siden **tilladelsessæt** skal du medtage eller udelade tilladelser til objektet i feltet **type**:

  Du kan inkludere tilladelsen ved at vælge **Inkluder**, og vælg derefter adgangsniveau for felterne **Læserettighed**, **Indsætterettighed**, **Redigeringsrettighed**, **Sletterettighed** og **Udførelsesrettighed**. Den følgende tabel beskriver indstillingerne.

  |Indstilling|Beskrivelse|Rangering|
  |------|-----------|-------|
  |**Tomt**|Brugeren kan ikke udføre handlingen på objektet.|Laveste|  
  |**Ja**|Brugeren kan udføre handlingen på objektet.|Højeste|
  |**Indirekte**|Brugeren kan udføre handlingen på objektet, men kun via et relateret objekt, som brugeren har fuld adgang til. Du kan finde flere oplysninger i [Eksempel - Indirekte tilladelse](#example---indirect-permission) i denne artikel og [Tilladelsesejendom](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property#example---indirect-permission) i Hjælp til udviklere og it-fagfolk.|Næsthøjeste|
  
  Hvis du vil udelukke tilladelsen eller et eller flere adgangsniveauer, skal du vælge **Udeluk** og derefter vælge det adgangsniveau, du vil give. Den følgende tabel beskriver indstillingerne.

  |Indstilling|Beskrivelse|
  |------|-----------|-------|
  |**Tomt**|Brug adgangsniveauet baseret på hierarkiet af tilladelser i sættet.  |
  |**Udeluk**|Fjern det specifikke adgangsniveau for objektet.|
  |**Reduktion af indirekte**|Ændre adgangsniveauet til indirekte, hvis et tilladelsessæt giver direkte adgang til objektet. Du kan f. eks. vælge denne indstilling, hvis tilladelsessættet giver direkte adgang til finansposter, men du ikke ønsker, at brugerne har fuld adgang til posterne.|
  
  > [!NOTE]
  > Hvis en rettighed befinder sig i et rettighedssæt, der er medtaget, og som også er angivet i et udeladt rettighedssæt, udelukkes rettigheden.

6. Brug felterne **Objekttype** og **Objekt-id** til at angive det objekt, du giver adgang til.

  > [!TIP]
  > Nye linjer viser standardværdier. Feltet **objekttype** indeholder f.eks. **tabeldata**, og feltet **Objekt-id** indeholder **0**. Standardværdierne er blot pladsholdere og bruges ikke. Du skal vælge en objekttype og et objekt i feltet **Objekt-id**, før du kan oprette en ny linje.

7. Valgfrit: Hvis du definerer tilladelser for en dataobjekttype i en tabel, kan du filtrere de data, som en bruger kan få adgang til i felter i den valgte tabel, i feltet **Sikkerhedsfilter**. For eksempel kan du angive, at en bruger kun skal kunne læse poster, der indeholder oplysninger om en bestemt kunde. Du kan finde flere oplysninger i [Sikkerhedsfiltre begrænser en brugers adgang til bestemte poster i en tabel](#security-filters-limit-a-users-access-to-specific-records-in-a-table) og [Bruge sikkerhedsfiltre](/dynamics365/business-central/dev-itpro/security/security-filters).
8. Valgfrit: Tilføj et eller flere tilladelsessæt i ruden **tilladelsessæt**. Du kan finde flere oplysninger i [Tilføje andre rettighedssæt](#to-add-other-permission-sets).

> [!IMPORTANT]
> Vær forsigtig, når du tilknytter **Indsæt tilladelse** eller **Ret tilladelse** til tabellen **9001-brugergruppemedlem** eller **9003-brugergruppetilladelsessæt**. Alle brugere, der har fået tildelt et tilladelsessæt, kan tildele sig selv til andre brugergrupper, som igen kan give dem uønskede rettigheder.

### <a name="example---indirect-permission"></a>Eksempel - indirekte rettighed

Du kan tildele en indirekte rettighed for kun at bruge et objekt gennem et andet objekt. En bruger kan f.eks. have tilladelse til at køre codeunit 80, salg-post Codeunit Salgs-post udfører mange opgaver, herunder ændring af tabel 37, Salgslinje. Når brugeren bogfører et salgsdokument med Salgs-post-codeunit, kontrollerer [!INCLUDE[prod_short](includes/prod_short.md)], om brugeren har rettighed til at ændre tabellen Salgslinje. Hvis ikke, kan codeunit ikke udføre sine opgaver, og brugeren får en fejlmeddelelse. I så fald kører codeunit'en korrekt.

Men brugeren behøver ikke at have fuld adgang til tabellen Salgslinje for at køre codeunit'en. Hvis brugeren har indirekte rettighed til tabellen Salgslinje, kører codeunit'en Salgs-post korrekt. Når en bruger har indirekte rettighed, kan brugeren kun redigere tabellen Salgslinje ved at køre codeunit'en salgs-post eller et andet objekt, der har rettighed til at ændre tabellen Salgslinje. Brugeren kan kun redigere tabellen Salgslinje, når det sker fra understøttede funktionalitetsområder. Brugeren kan ikke køre funktionen ved et uheld eller skadeligt ved andre metoder.

### <a name="to-add-other-permission-sets"></a>Sådan tilføjes andre tilladelsessæt

Udvid et tilladelsessæt ved at føje andre tilladelsessæt til det. Derefter kan du medtage eller udelade bestemte tilladelser eller hele tilladelsessæt i hvert sæt, du tilføjer. Dette omfatter tilladelser i tilladelsessæt og systemtype-tilladelsessæt, som ellers ikke er tilladt. Udeladelser gælder kun for det tilladelsessæt, du er ved at udvide. Det oprindelige sæt ændres ikke.

Tilføj et tilladelsessæt i ruden **Tilladelsessæt** på siden **Tilladelsessæt**. I ruden **Resultat** vises alle tilføjede tilladelsessæt. Hvis du vil undersøge de tilladelser, der er medtaget i et sæt, du har tilføjet, skal du vælge indstillingen sæt i resultatruden og faktaboksen **Inkluderede tilladelser** vil vise tilladelserne.

I ruden **Resultat** skal du bruge feltet **Medtagelsesstatus** til at identificere de tilladelsessæt, hvor du har udeladt tilladelser eller tilladelsessæt. Hvis noget er udelukket, vil status være **delvis**.

Hvis du vil have en overordnet visning af tilladelserne i tilladelsessættet, skal du vælge handlingen **Vis alle tilladelser**. Siden **Udvidede tilladelser** viser alle de tilladelser, der allerede er tildelt til tilladelsessættet, og tilladelserne i tilføjede tilladelsessæt.

Hvis du helt vil udelukke alle tilladelser fra et tilladelsessæt, skal du markere linjen i ruden **Resultat**, vælge **Vis flere indstillinger** og derefter vælge **Udeluk**. Når du udelukker et tilladelsessæt, oprettes der en linje i ruden **Tilladelsessæt** af typen udeladt. Hvis du har udeladt et tilladelsessæt, men vil medtage det igen, skal du slette linjen i ruden med **Tilladelsessæt**.

Hvis du vil udelukke en bestemt tilladelse helt eller delvist i et sæt, du har tilføjet, skal du oprette en linje for objektet under **Tilladelser**. Felterne adgangsniveau, Indsæt tilladelse, Rediger tilladelse osv. vil alle indeholde **Udelad**. Hvis du vil tillade et bestemt adgangsniveau, skal du vælge den relevante indstilling.

Hvis du udelader et tilladelsessæt, udelukkes alle tilladelserne i sættet. [!INCLUDE [prod_short](includes/prod_short.md)] beregner tilladelserne som følger:

1. Beregne den fuldstændige liste over inkluderede tilladelser
2. Beregne den fuldstændige liste over ekskluderede tilladelser
3. Fjerne udelukkede tilladelser fra listen over inkluderede tilladelser (fjerne en indirekte tilladelse er den samme som reduktion af indirekte)

## <a name="to-copy-a-permission-set"></a>Sådan kopieres et rettighedssæt

Opret et nyt tilladelsessæt ved at kopiere et andet. Det nye sæt vil omfatte alle tilladelser og tilladelsessæt fra det sæt, du har kopieret. Den måde, tilladelserne og tilladelses sættene arrangeres på, afhænger af det, du har valgt i feltet **Kopier operation**. Den følgende tabel beskriver indstillingerne.

|Indstilling  |Beskrivelse  |
|---------|---------|
|**Kopier efter reference**     | Det oprindelige tilladelsessæt og alle tilføjede tilladelsessæt er angivet i **resultat**-ruden.       |
|**Flad rettighedskopi**  | Alle tilladelser fra alle tilladelsessæt er medtaget på en simpel liste i ruden **Tilladelser**. Tilladelserne er ikke organiseret efter tilladelsessæt.        |
|**Klon**     | Opret en nøjagtig kopi af det oprindelige tilladelsessæt.        |

1. På siden **Rettighedssæt** skal du vælge linjen for et bestemt rettighedssæt, som du vil kopiere, og vælg derefter handlingen **Kopiér rettighedssæt**.
2. På siden **Kopiér rettighedssæt** skal du angive navnet på det nye rettighedssæt.
3. I feltet **Kopier handling** skal du angive, hvordan tilladelsessættet skal arrangeres i det nye tilladelsessæt.
4. Valgfrit: Hvis du tilføjer et systemtilladelsessæt, kan det være en god idé at få besked, hvis navnet eller indholdet af det oprindelige tilladelsessæt ændres i en fremtidig version. Her kan du se, om du skal opdatere dit brugerdefinerede tilladelsessæt. Hvis du vil modtage en besked, skal du aktivere funktionen **Giv besked om ændret tilladelsessæt**.

> [!NOTE]
> Meddelelsen kræver, at meddelelsen **Oprindelige systemtilladelsessæt ændret** er aktiveret på siden **Mine beskeder**.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Sådan opretter eller redigerer du rettigheder ved at registrere dine handlinger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rettighedssæt**, og vælg derefter det relaterede link.

    Du kan også vælge handlingen **Rettighedssæt** på siden **Brugere**.
2. Vælg handlingen **Ny** på siden **Rettighedssæt**.
3. Udfyld felterne på en ny linje efter behov.
4. Vælg handlingen **Rettigheder**.
5. På siden **Rettigheder** skal du vælge handlingen **Registrer rettigheder** og derefter vælge handlingen **Start**.  
    Optagelsen skal udføres enten ved hjælp af **Åbn siden i en ny Windows**-funktion (pop-out) for at få **tilladelse** til at optage siden ved siden af eller ved at arbejde på den samme fane.  
    Der startes nu en registreringsproces, som registrerer alle dine handlinger i brugergrænsefladen.
6. Gå til de forskellige sider og aktiviteter i [!INCLUDE[prod_short](includes/prod_short.md)], som du vil give brugerne med dette rettighedssæt adgang til. Du skal udføre de opgaver, som du vil registrere rettigheder for.
7. Når du vil afslutte registreringen, skal du vende tilbage til siden **Rettigheder** og derefter vælge handlingen **Stop**.
8. Vælg knappen **Ja** for at føje de registrerede rettigheder til det nye rettighedssæt.
9. Angiv, om brugerne skal kunne indsætte, redigere eller slette poster i de registrerede tabeller for hvert objekt på listen over registrerede elementer.

### <a name="to-export-and-import-a-permission-set"></a>Sådan eksporteres og importeres et tilladelsessæt

Hvis du hurtigt vil oprette tilladelser, kan du importere tilladelsessæt, som du har eksporteret fra en anden [!INCLUDE[prod_short](includes/prod_short.md)]-lejer.

I miljøer med flere lejere importeres et tilladelsessæt i en bestemt lejer. Det vil sige, at importomfanget er *Leje*.

1. I lejer 1 på siden **Rettighedssæt** skal du vælge linjen eller de linjer til rettighedssættene, der skal eksporteres, og derefter vælge handlingen **Eksportér rettighedssæt**.

    En XML-fil oprettes i mappen Overførsler på din computer. Som standard hedder filen *Export Permission Sets.xml*.

2. I lejer 2 på siden **Rettighedssæt** skal du vælge handlingen **Importer rettighedssæt**.
3. På dialogsiden **Importer rettighedssæt** skal du overveje, om du vil flette eksisterende rettighedssæt med nye rettighedssæt i XML-filen.

    Hvis du markerer afkrydsningsfeltet **Opdater eksisterende tilladelser**, flettes de eksisterende rettighedssæt med samme navn som dem i XML-filen med de importerede rettighedssæt.

    Hvis du ikke markerer afkrydsningsfeltet **Opdater eksisterende tilladelser**, springes rettighedssæt med samme navn som dem i XML-filen over, når der importeres. Hvis det er tilfældet, vil du få besked om, hvilke rettighedssæt der springes over.

4. På dialogsiden **Import** skal du finde og vælge den XML-fil, der skal importeres, og derefter vælge handlingen **Åbn**.

Rettighedssættene importeres.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Sådan fjernes forældede rettigheder fra alle rettighedssæt

På siden **Rettighedssæt** skal du vælge handlingen **Fjern forældede rettigheder**.

## <a name="to-set-up-time-constraints-for-users"></a>Sådan opsættes tidsbegrænsninger for brugere

Administratorer kan angive perioder, hvor angivne brugere kan bogføre. Administratorer kan også angive, om systemet skal logge af, hvor lang tid brugere er logget på. Administratorer kan også knytte ansvarscentre til brugere. Du kan finde flere oplysninger i [Arbejde med ansvarscentre](inventory-responsibility-centers.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugeropsætning**, og vælg derefter det relaterede link.
2. Når siden **Brugeropsætning** åbnes, skal du vælge handlingen **Ny**.
3. I feltet **Bruger-ID** skal du angive ID'et for en bruger, eller vælge feltet for at få vist alle aktuelle Windows-brugere i systemet.
4. Udfyld felterne efter behov.

## <a name="to-manage-permissions-through-user-groups"></a>Sådan administreres rettigheder via brugergrupper

Brugergrupper hjælper dig med at administrere tilladelsessæt på tværs af virksomheden. [!INCLUDE [prod_short](includes/prod_short.md)] online indeholder standardbrugergrupper, der automatisk tildeles til brugere baseret på deres licens. Du kan føje brugere til en brugergruppe manuelt, og du kan oprette nye brugergrupper som kopier af eksisterende.  

Du starter med at oprette en brugergruppe. Derefter kan du tildele et rettighedssæt til gruppen for at definere, hvilket objekt brugere af gruppen har adgang til. Når du føjer en bruger til gruppen, gælder de rettighedssæt, der er defineret for gruppen, for brugeren.

Tilladelsessæt, der er tildelt en bruger via en brugergruppe, forbliver synkroniseret. En ændring af brugergruppens rettigheder overføres automatisk til brugerne. Hvis du fjerner en bruger fra en brugergruppe, tilbagekaldes de involverede rettigheder automatisk.

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

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugergrupper**, og vælg derefter det relaterede link.
2. Vælg de brugergrupper, som du vil kopiere, og vælg derefter handlingen **Kopiér brugergruppe**.
3. I feltet **Ny brugergruppekode** skal du angive et navn til gruppen og derefter vælge knappen **OK**.

Den nye gruppe tilføjes på siden **Brugergrupper**. Fortsæt for at tilføje brugere. Yderligere oplysninger finder du i afsnittet [Sådan tilføjes brugere til en brugergrupper](#to-add-users-to-a-user-group).  

> [!IMPORTANT]
> Du får en valideringsfejl, hvis du forsøger at tildele en brugergruppe til brugeren, som henviser til et tilladelsessæt, som er defineret i en ikke-installeret udvidelse. Det skyldes, at app-id'et for filtypenavnet er valideret, hver gang der refereres til den. Hvis du vil tildele den pågældende brugergruppe til en bruger, kan du enten geninstallere udvidelsen, fjerne referencen til den ikke-installerede udvidelse fra tilladelsessættet eller fjerne tilladelsen fra brugergruppen.

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
3. På siden **Rettighedssæt efter brugergruppe** skal du markere feltet **[brugergruppenavn]** på en linje for det relevante rettighedssæt for at tildele sættet til brugergruppen.
4. Marker afkrydsningsfeltet **Alle brugergrupper** for at tildele rettighedssættet til alle brugergrupper.

Du kan også tildele rettighedssæt direkte til brugere.

## <a name="to-assign-permission-sets-to-users"></a>Sådan tildeles rettighedssæt til brugere

Et rettighedssæt er en samling rettigheder til bestemte databaseobjekter. Alle brugere skal være tildelt et eller flere rettighedssæt, før de kan få adgang til [!INCLUDE[prod_short](includes/prod_short.md)].  

En [!INCLUDE[prod_short](includes/prod_short.md)]-løsning indeholder et antal foruddefinerede rettighedssæt, der er tilføjet af Microsoft eller din løsningsudbyder. Du kan også tilføje nye rettighedssæt, der er skræddersyet til at opfylde din organisations behov. Du kan finde flere oplysninger i afsnittet [Sådan oprettes eller redigeres et rettighedssæt](#to-create-a-permission-set).

> [!NOTE]
> Hvis du ikke vil begrænse en brugers adgang mere, end det allerede er defineret af licensen, kan du tildele et særligt rettighedssæt, der kaldes SUPER, til brugeren. Dette rettighedssæt sikrer, at brugeren kan få adgang til alle de objekter, der er angivet i licensen.
>
> En bruger med den grundlæggende licens og SUPER-rettighedssættet har adgang til flere funktioner end brugere med licensen Teammedlem og SUPER-rettighedssættet.

Du kan tildele rettighedssæt til brugere på to måder:

- Fra siden **Brugerkort** ved at vælge de rettighedssæt, der skal tildeles brugeren.
- Fra siden **Rettighedssæt efter bruger** ved at vælge de brugere, der er tildelt et rettighedssæt.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Sådan tildeles et rettighedssæt på et brugerkort

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugere**, og vælg derefter det relaterede link.
2. Vælg den bruger, du vil tildele rettigheden til.
Ethvert rettighedssæt, der allerede er tildelt brugeren, vises i faktaboksen **Rettighedssæt**.
3. Vælg handlingen **Rediger** for at åbne siden **Brugerkort**.
4. I oversigtspanelet **Brugerrettighedssæt** skal du udfylde felterne efter behov på en ny linje. Du kan finde flere oplysninger i [Sådan oprettes eller redigeres et rettighedssæt](ui-define-granular-permissions.md#to-create-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Sådan tildeles et rettighedssæt på siden Rettighedssæt efter bruger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugere**, og vælg derefter det relaterede link.
2. Du kan også vælge handlingen **Rettighedssæt efter bruger** på siden **Brugere**.
3. På siden **Rettighedssæt efter bruger** skal du markere afkrydsningsfeltet **[brugernavn]** på en linje for det relevante rettighedssæt for at tildele sættet til brugeren.

    Marker afkrydsningsfeltet **Alle brugere** for at tildele rettighedssættet til alle brugere.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Sådan får du vist en oversigt over en brugers rettigheder

Du kan vise andre brugeres gældende rettigheder, hvis du har tilladelserne SUPER eller SIKKERHED. 

Siden **Gældende tilladelser** indeholder yderligere oplysninger om kilden for hver tilladelse. Det kan f.eks. være, om kilden er en sikkerhedsgruppe, eller om en tilladelse er nedarvet. Siden indeholder også en kolonne, hvor administratorer kan gennemse de sikkerhedsfiltre, der anvendes. Du kan finde flere oplysninger i sikkerhedsfiltre i [Sikkerhedsfiltre begrænser en brugers adgang til bestemte poster i en tabel](#security-filters-limit-a-users-access-to-specific-records-in-a-table).

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
    > Du kan finde en forklaring på placeringsniveauer i [Sådan oprettes et tilladelsessæt](ui-define-granular-permissions.md#to-create-a-permission-set).  

4. For at redigere et rettighedssæt skal du i delen **Efter rettighedssæt** på linjen for en relevant rettighed angive typen **Brugerdefineret**, vælge et af de fem adgangstypefelter og vælge en anden værdi.

5. For at redigere individuelle rettigheder i rettighedssættet skal du vælge værdien i feltet **Rettighedssæt** for at åbne siden **Rettigheder**.

> [!NOTE]  
> Når du redigerer et rettighedssæt, gælder ændringerne også for andre brugere, som rettighedssættet er tildelt til.

### <a name="security-filters-limit-a-users-access-to-specific-records-in-a-table"></a>Sikkerhedsfiltre begrænser en brugers adgang til bestemte poster i en tabel

Når det drejer sig om postbaseret sikkerhed i [!INCLUDE[prod_short](includes/prod_short.md)], kan du bruge filtrene til at begrænse en brugers adgang til data i en tabel. Du kan oprette sikkerhedsfiltre for tabeldata. Et sikkerhedsfilter beskriver et sæt af poster i en tabel, som en bruger har adgang til. For eksempel kan du angive, at en bruger kun skal kunne læse poster, der indeholder oplysninger om en bestemt kunde. Det betyder, at brugeren ikke kan få adgang til de poster, der indeholder oplysninger om andre kunder. Du kan finde flere oplysninger i [Bruge sikkerhedsfiltre](/dynamics365/business-central/dev-itpro/security/security-filters) i administrationsindholdet.

## <a name="viewing-permission-changes-telemetry"></a>Få vist ændringer af telemetri

Du kan oprette [!INCLUDE[prod_short](includes/prod_short.md)] for at sende ændringer, der er udført for at få tilladelse til en Application Insights-ressource i Microsoft Azure. Derefter kan du bruge Azure Monitor til at oprette rapporter og konfigurere påmindelser i de indsamlede data. Du kan finde flere oplysninger i følgende artikler i [!INCLUDE[prod_short](includes/prod_short.md)]-hjælp til udviklere og it-eksperter:

- [Overvåge og analysere telemetri - aktivere Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analysere feltovervågningstelemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="delegated-admin-users"></a>Opsætning af administratorbrugere

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

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
