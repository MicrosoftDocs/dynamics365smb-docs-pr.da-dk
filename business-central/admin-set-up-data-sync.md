---
title: Konfigurere regnskaber til synkronisering af stamdata
description: 'Få mere at vide om, hvordan du opretter et eller flere regnskaber for at synkronisere stamdata.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 05/07/2024
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---

# Gør dig klar til at synkronisere stamdata

Hvis to eller flere regnskaber bruger nogle af de samme stamdata, kan du synkronisere dataene i stedet for at tilføje dem manuelt i hver virksomhed. F.eks. er synkronisering af data især nyttig, når du skal oprette nye datterselskaber.

Stamdata omfatter indstillinger og ikke-transaktionsoplysninger om forretningsenheder. F.eks. kunder, leverandører, varer og medarbejdere. Dataene indeholder kontekst for forretningstransaktioner. Her følger nogle få eksempler på stamdata for en kunde:

* Name
* Identifikationsnummer
* Adresse
* Betalingsbetingelser
* Kreditgrænse

Du vælger indstillinger til synkronisering i datterselskaber. Hvis du bruger en pull-model, trækker datterselskaber dataene fra det kilderegnskab, de skal bruge for at gøre forretninger med dem. Når du har konfigureret synkroniseringen og synkroniserer data første gang, er du klargjort. Opgavekøposter opdaterer sammenkædede poster i datterselskaber, når nogen foretager ændringer af data i kilderegnskabet.

## Kun etvejs-synkronisering af debitorer

Du kan kun synkronisere data fra kilderegnskabet med datterselskaberne på en pull-måde. Datterselskaber kan ikke skubbe data til kilderegnskabet.

> [!NOTE]
> Selvom det er muligt, anbefaler vi ikke, at du opretter tovejssynkronisering. Det vil sige, at synkronisering af data fra kilderegnskabet til datterselskaberne og fra datterselskaberne til kilderegnskabet. Synkronisering af data i begge retninger kan medføre konflikter eller uønskede overskrivninger.

## Før du starter

Følgende er kravene til oprettelse af synkronisering.

* Alle regnskaber skal være den samme miljø.
* Den bruger, der opsætter datterselskabet, skal have den licensen **Essential**, **Premium** eller **Basis-ISV**.

> [!NOTE]
> Licenserne Team-medlem og International administrator giver dig adgang, men ikke til at ændre poster, så de kan ikke bruges til at konfigurere synkroniseringen. Du kan ikke planlægge baggrundsopgaver med den delegerede administratorlicens, så du kan ikke fuldføre installationen.

## Angive kilderegnskabet

De første trin er at angive, hvilket regnskab der skal være datakilden og aktivere synkronisering. Datterselskaber trækker data fra kilderegnskabet.

> [!NOTE]
> Når du aktiverer synkronisering, opretter og planlægger [!INCLUDE [prod_short](includes/prod_short.md)] de opgavekøposter, som synkroniserer dataene. Det kan se ud som om, de indlæste data synkroniseres med det samme, men det er ikke tilfældet. De oprettede opgavekøposter synkroniserer kun sammenkoblede poster, og du har ikke indstillet det endnu. Synkroniseringen starter, når du [aktiverer eller deaktiverer tabeller og felter](#enable-or-disable-tables-and-fields) og [synkronisere for første gang](#synchronize-for-the-first-time).

1. I datterselskabet skal du vælge ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Administration af opsætning af stamdata**, og vælg derefter det relaterede link.
1. Angiv det regnskab, du vil trække ændringer fra, i feltet **kilderegnskab**.
1. Vælg Til med skifteknappen **Aktivér synkronisering**.
1. Vælg **OK** i bekræftelsesdialogboksen. [!INCLUDE [prod_short](includes/prod_short.md)] finder de tabeller og felter, der er tilgængelige fra kilderegnskabet.

I det næste trin skal du aktivere tabeller og felter til synkronisering.

## Aktivere eller deaktivere tabeller og felter

Hvis du vil spare tid, angiver [!INCLUDE [prod_short](includes/prod_short.md)] en liste over tabeller, som virksomheder ofte synkroniserer. Disse tabeller er som standard aktiveret til synkronisering. Du kan ændre, deaktivere eller slette dem efter behov. Nogle af felterne i tabellerne er allerede deaktiverede som en ekstra tidsbesparelse, fordi de sandsynligvis ikke er relevante for datterselskabet.

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

* Hvis du allerede har poster i både kilde-og datterselskaberne, og du vil matche eksisterende poster, skal du vælge handlingen **Brug matchbaseret kobling**. [!INCLUDE [prod_short](includes/prod_short.md)] passer til poster i datterselskab med poster i kilderegnskabet. Overensstemmelserne er baseret på matchkriterier, som du definerer. I forbindelse med flere standardtabeller har [!INCLUDE [prod_short](includes/prod_short.md)] allerede matchede eksisterende poster ved hjælp af deres primære nøgle, men du kan ændre dem efter behov. Du kan også bruge synkroniseringen til at oprette nye poster i datterselskabet for poster i det kilderegnskab, som datterselskabet ikke har. Hvis du vil vide mere om matchning, skal du gå til [Brug match-baseret kobling](#use-match-based-coupling).
* Hvis du vælger **Kør fuld synkronisering**, opretter synkroniseringen nye poster for alle poster i kilderegnskabet, der endnu ikke er sammenkædet. Denne indstilling er f.eks. nyttig i følgende scenarier:

    * Datterselskabet har ikke data i tabellen.
    * Du vil føje poster fra kildevirksomheden uden match.  

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

Hvis du opretter flere datterselskaber, som bruger de samme eller lignende synkroniseringsindstillinger, er der en tidsbesparelse. Opret et datterselskab, og eksporter derefter dets opsætning til en .xml-fil. Filen indeholder hele opsætningen, herunder tabel- og felttilknytninger og filterkriterier. Du kan derefter importere filen til næste datterselskab. Hvis du vil importere eller eksportere en opsætning, skal du bruge **import** eller **eksport** på siden **Opsætning af stamdatastyring**.

## Se også

[Administrere synkronisering af stamdata](admin-sync-master-data.md)