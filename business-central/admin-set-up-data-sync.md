---
title: Konfigurere regnskaber til synkronisering af stamdata
description: 'Få mere at vide om, hvordan du opretter et eller flere regnskaber for at synkronisere stamdata.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---

# Gør dig klar til at synkronisere stamdata

Når du har to eller flere virksomheder, der bruger mindst nogle af de samme stamdata, kan du spare tid ved at synkronisere dem i regnskaberne. Synkronisering af data er især nyttig, når du skal oprette nye datterselskaber.

Stamdata omfatter indstillinger og ikke-transaktionsoplysninger om forretningsenheder, f. eks. debitorer, kreditorer, varer og medarbejdere. Dataene indeholder kontekst for forretningstransaktioner. Her følger nogle få eksempler på stamdata for en kunde:

* Name
* Identifikationsnummer
* Adresse
* Betalingsbetingelser
* Kreditgrænse

Du vælger indstillinger til synkronisering i datterselskaber. Hvis du bruger en pull-model, trækker datterselskaber dataene fra det kilderegnskab, de skal bruge for at gøre forretninger med dem. Når du har konfigureret synkroniseringen og synkroniserer data første gang, er du klargjort. Posterne i tabellerne er koblet fra, og opgavekøposter starter med at opdatere data i datterselskaber, når nogen foretager ændringer i kilde regnskabet.

## Kun etvejs-synkronisering af debitorer

Du kan kun synkronisere data fra kilderegnskabet med datterselskaberne på en pull-måde. Datterselskaber kan ikke skubbe data til kilderegnskabet.

> [!NOTE]
> Selvom det er muligt, anbefaler vi ikke, at du opretter tovejssynkronisering. Det vil sige, at synkronisering af data fra kilderegnskabet til datterselskaberne og fra datterselskaberne til kilderegnskabet. Synkronisering af data i begge retninger kan medføre konflikter eller uønskede overskrivninger.

## Før du starter

Dette er kravene til oprettelse af synkronisering.

* Alle regnskaber skal være den samme miljø.
* Den bruger, der har oprettet datterselskabet, skal have rettighedssættet **Stamdataadministration**. Tilladelsessættet er tilgængeligt i Premium og essentielle licenser. Licensen Team-medlem giver en person adgang, men ikke til at ændre poster, så den kan ikke bruges til at konfigurere synkroniseringen.

## Angive kilderegnskabet

De første trin er at angive, hvilket regnskab der skal være datakilden og aktivere synkronisering. Datterselskaber trækker data fra kilderegnskabet.

1. I datterselskabet skal du vælge ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Administration af opsætning af stamdata**, og vælg derefter det relaterede link.
1. Angiv det regnskab, du vil trække ændringer fra, i feltet **kilderegnskab**.
1. Vælg Til med skifteknappen **Aktivér synkronisering**.
1. Vælg **OK** i bekræftelsesdialogboksen. [!INCLUDE [prod_short](includes/prod_short.md)] finder de tabeller og felter, der er tilgængelige fra kilderegnskabet.

I det næste trin skal du aktivere tabeller og felter til synkronisering.

## Aktivere eller deaktivere tabeller og felter

Hvis du vil spare tid, angiver [!INCLUDE [prod_short](includes/prod_short.md)] en liste over tabeller, som virksomheder ofte synkroniserer. Disse tabeller er som standard aktiveret til synkronisering, men du kan ændre, deaktivere eller slette dem efter behov. Nogle af felterne i tabellerne er allerede deaktiverede som en ekstra tidsbesparelse, fordi de sandsynligvis ikke er relevante for datterselskabet.

> [!NOTE]
> Hvis en eller flere udvidelser er installeret i kilderegnskabet, og et datterselskab opsætter synkroniseringen, indeholder siden **Synkroniseringstabeller** tabeller fra udvidelserne, og du kan få adgang til felterne. Men hvis kilderegnskabet tilføjer et filtypenavn, efter at synkroniseringen er oprettet, skal de enkelte datterselskaber manuelt tilføje tabellerne. Hvis du vil vide mere om, hvordan du tilføjer tabeller, skal du gå til [Tilføj eller slet tabeller på synkroniseringslisten](#add-or-delete-tables-from-the-synchronization-tables-list). Hvis du vil vide mere om udvidelse [!INCLUDE [prod_short](includes/prod_short.md)], skal du gå til [Udvikling af udvidelser i Visual Studio Code](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview#developing-extensions-in-visual-studio-code).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Administration af opsætning af stamdata**, og vælg derefter det relaterede link.
1. Vælg handlingen **Synkroniseringstabeller**.
1. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Feltet **tabelfilter** bruges til at kontrollere, hvad der skal synkroniseres i en tabel. Du kan kun konfigurere filtre, der skal synkroniseres, når bestemte betingelser er opfyldt. Du kan f. eks. tilføje filtre, som angiver, at du kun synkroniserer kreditorer i et bestemt område. Debitorer, som bruger en bestemt valuta.
>
> Hvis datterselskabet allerede har data i tabellerne, er det en god måde at angive kriterier for synkroniseringen på, når du opretter matchbaseret kobling. Hvis du vil vide mere om matchning, skal du gå til [Brug match-baseret kobling](#use-match-based-coupling).

1. Hvis du vil aktivere felter for en tabel, skal du vælge tabellen og derefter vælge handlingen **Felter** .
1. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Du kan hurtigt aktivere eller deaktivere flere felter på én gang ved at markere dem på listen og derefter bruge handlingerne **Aktiver** eller **Deaktiver**.

### Brug matchbaseret sammenkædning

Du kan angive de data, der skal synkroniseres for en tabel, ved at sammenligne posterne på basis af kriterier. På side **Administration af stamdataopsætning** skal du vælge handlingen **Matchbaseret sammenkædning** for at åbne siden **Vælg sammenkædningskriterie**. Du kan angive følgende kriterier for sammenligningen:

* Angiv, om du vil synkronisere, når du har koblet posterne.
* Angiv, om der skal oprettes en ny post i datterfirmaet, hvis der findes entydigt, ikke-sammenkoblet match ved hjælp af søgekriterierne. Hvis du vil aktivere denne funktion, skal du aktivere afkrydsningsfeltet **Opret ny, hvis der ikke findes en match**-handling.
* De felter, der skal bruges til at matche poster, og om der er forskel på store og små bogstaver.
* Prioritere den rækkefølge, som poster gennemsøges i, ved at angive en matchprioritet. [!INCLUDE [prod_short](includes/prod_short.md)] søger efter et match i stigende rækkefølge på grundlag af matchprioritet. En tom værdi i feltet er lig med prioritet 0, som er den højeste prioritet. Felter med prioriteten 0 behandles først.

## Synkronisere første gang

Når du er klar, skal du vælge handlingen **Start første synkronisering** på siden **Opsætning af stamdatastyring**. På siden **Første synkronisering af stamdata** skal du vælge den type synkronisering, du vil bruge til hver tabel.

* Hvis du allerede har poster i både kilde-og datterselskaberne, og du vil matche eksisterende poster, skal du vælge handlingen **Brug matchbaseret kobling**. [!INCLUDE [prod_short](includes/prod_short.md)] matcher poster i datterselskabet med poster i kildevirksomheden, baseret på de matchkriterier du definerer. I forbindelse med flere standardtabeller har [!INCLUDE [prod_short](includes/prod_short.md)] allerede matchede eksisterende poster ved hjælp af deres primære nøgle, men du kan ændre dem efter behov. Du kan også bruge synkroniseringen til at oprette nye poster i datterselskabet for poster i det kilderegnskab, som datterselskabet ikke har. Hvis du vil vide mere om matchning, skal du gå til [Brug match-baseret kobling](#use-match-based-coupling).
* Hvis du vælger **Kør fuld synkronisering**, vil synkroniseringen oprette nye poster for alle poster i kilderegnskabet, der endnu ikke er sammenkædet. Denne indstilling er typisk nyttig, hvis der ikke er nogen data i datterselskabet, eller hvis du kun vil tilføje poster fra kilde regnskabet uden at tilsvarende.  

Når du har valgt indstillingen, der skal bruges, skal du vælge **Start alle**-handlingen for at starte synkroniseringen.

Mens synkroniseringen kører, viser **Opgavestatus**-kolonnen på siden **Fuld synkronisering af stamdata** vises status for hver opgavekøpost. Tryk på **F5** på tastaturet for at opdatere status.

> [!TIP]
> Tabeller synkroniseres i en foruddefineret rækkefølge. Hvis synkroniseringen sidder fast i en tabel, skal du markere tabellen og derefter vælge handlingen **Genstart** for at få den til at gå videre.

Du kan få adgang til detaljer, f. eks. det antal poster, der indsættes eller ændres, ved at vælge værdien i kolonnen **jobstatus** for at åbne siden **Vis-integrationssynkroniseringsjob**. I forbindelse med poster, der er indsat, kan du vælge tallet i den **indsatte** kolonne for at få adgang til flere detaljer om de nye poster.

## Tilføje eller slette tabeller på listen over synkroniseringstabeller

### Tilføje en tabel

> [!IMPORTANT]
> Selvom tabeller, der indeholder transaktionsdata, er tilgængelige på listen, f. eks. tabeller, der indeholder poster, skal du ikke vælge dem. Synkronisering fungerer kun for tabeller, der indeholder ikke-transaktionsdata.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Synkroniseringstabeller**, og vælg derefter det relaterede link.
1. Vælg **Ny**, og vælg derefter den tabel, der skal tilføjes.
1. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

### Slet en tabel

> [!NOTE]
> Hvis du sletter en post i kilde regnskabet, slettes den ikke også i datterselskabet. Dette er med til at forhindre uønsket tab af data. Du kan f. eks. vælge at slette tabellen.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Synkroniseringstabeller**, og vælg derefter det relaterede link.
1. Vælg handlingen **Slet**.

## Bruge Eksporter og Importer til at dele en synkroniseringsopsætning

Hvis du opretter flere datterselskaber, som vil bruge de samme eller lignende synkroniseringsindstillinger, kan du spare tid ved at oprette et datterselskab og derefter udlæse opsætningen til en .xml-fil. Filen indeholder hele opsætningen, herunder tabel- og felttilknytninger og filterkriterier. Du kan derefter importere filen til næste datterselskab. Hvis du vil importere eller eksportere en opsætning, skal du bruge **import** eller **eksport** på siden **Opsætning af stamdatastyring**.

## Se også

[Administrere synkronisering af stamdata](admin-sync-master-data.md)