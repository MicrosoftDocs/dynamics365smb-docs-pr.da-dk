---
title: Oprette Intrastat-rapportering
description: 'Få at vide, hvordan du opsætter Intrastat-rapporteringsfunktioner og rapporterer handel med virksomheder i andre EU-lande.'
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# Oprette Intrastat-rapportering

Alle virksomheder i EU skal rapportere deres handel med andre EU-lande/områder. Virksomheder skal rapportere bevægelsen af varer til statistikmyndighederne i deres land/område for hver måned, og rapporten skal indleveres til skattemyndighederne. Intrastat er det system, der bruges til indsamling af handelsstatistik for varer inden for disse lande/områder. Du kan bruge **Intrastat-rapporten** til at udfærdige regelmæssig Intrastat-rapportering (typisk månedligt), indsamling, registrering og rapportering af handel med varer i henhold til den lokale lovgivning.

Intrastat-rapportering er baseret på de grundlæggende EU-forordninger, der gælder for alle lande/områder. I praksis er der imidlertid visse forskelle i de enkelte lande. Hvert land har regler for, hvad der nøjagtigt skal rapporteres og hvordan.

> [!NOTE]
> Intrastat-oplysninger gælder ikke for flytning af tjenester mellem lande, men kun handelsvarer (varer og anlægsaktiver). Hvis den lokale regering kræver registrering af tjenesteydelser mellem lande, kan det gøres ved hjælp af funktionen **Serviceerklæring**.
>
> Denne funktion forventes at være tilgængelig fra november 2022 som en app på [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646), så hvis du vil bruge den, skal du først installere den på siden **Udvidelsesstyring**.

> [!IMPORTANT]
> Denne artikel dækker den nye Intrastat-oplevelse, der er tilgængelig fra [!INCLUDE[prod_short](includes/prod_short.md)] version 21. Kontakt administratoren for at få mere at vide om, hvilken version din virksomhed bruger, og for at aktivere den nye funktionalitet.
>
> Læs den forrige versions artikel om Intrastat-opsætning og brugsoplysninger ved i [Konfigurere og rapportere Intrastat](finance-how-setup-report-intrastat-v20.md).

## Aktivere den nye Intrastat-oplevelse

I 2022 udgivelsesbølge 2 indeholder [!INCLUDE[prod_short](includes/prod_short.md)] en nydesignet Intrastat-oplevelse med udvidede funktioner. Hvis den nye Intrastat-funktionalitet ikke er aktiveret i dit miljø, kan den manuelt aktiveres af en administrator på siden **Funktionsstyring**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Funktionsstyring**, og vælg derefter det relaterede link.
2. På siden **Funktionsstyring** skal du vælge linjen **Funktionsopdatering: Erstat den eksisterende Intrastat-funktionalitet med den nye Intrastat-udvidelse**. Få flere oplysninger om funktionsstyring i [Aktivering af kommende funktioner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management) i administrationsindholdet.
3. Vælg **Alle brugere** i kolonnen **Aktivér for**.
4. Læs forklaringen til, hvordan systemet opgraderes, og vælg **Ja**, hvis du accepterer.
5. Vælg **Næste**, så du får vist en grundlæggende opsætning til Intrastat. Du kan finde flere oplysninger om Intrastat-opsætningen i [Intrastat-konfiguration](#intrastat-configuration).
6. Når du har afsluttet installationen, skal du vælge **Udfør** for at begynde at bruge den nye Intrastat-oplevelse.

> [!IMPORTANT]
> Husk på, at du ikke kan bruge den gamle og nye oplevelse parallelt. Før du aktiverer udvidelsen i et produktionsmiljø, anbefales det, at du først aktiverer og tester denne funktion i et sandkassemiljø med en kopi af produktionsdata, før du gør det i et produktionsmiljø. Når du har aktiveret den nye brugeroplevelse i produktionsmiljøet, kan du ikke vende tilbage til den gamle Intrastat-funktionalitet.

> [!NOTE]
> Afhængigt af virksomhedens placering vil aktivering af den funktion, der er beskrevet ovenfor, være tilstrækkelig. I de lande/områder, der har bestemte funktioner til Intrastat-rapportering, skal du aktivere den landespecifikke Intrastat-app ud over den centrale udvidelse.

## Intrastat-konfiguration

Før du kan bruge Intrastat-rapporter, er der flere konfigurationer, der skal oprettes.

### Oprette Intrastat-rapportering

Siden **Intrastat-rapportopsætning** bruges til at aktivere Intrastat-rapportering og angive standarder for den. Du kan angive, om du vil rapportere Intrastat fra leverancer (afsendelser), tilgange (modtagelser) eller begge afhængigt af de tærskelværdier, der er angivet af lokale regler. Du kan også angive standardtransaktionstyper for almindelige og returnerede dokumenter, der bruges til arten af transaktionsrapporteringen.

Sådan konfigurerer du Intrastat-rapportering:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af Intrastat-rapport**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] I nedenstående tabel beskrives nogle af nøglefelterne:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Rapportér modtagelser** | Angiver, at du skal inkludere tilgang af modtagede varer i Intrastatrapporter. |
   | **Rapportér afsendelser** | Angiver, at du skal inkludere leverancer af afsendte varer i Intrastatrapporter. |
   | **Afsendelser baseret på**  | Angiver, ud fra hvilke landekoder Intrastat-rapportlinjer skal tages. Du kan vælge mellem følgende indstillinger: **Sælg-til-land/område**, **Fakturer-til-land/område** eller **Lever-til-land/område**. |
   | **Momskode baseret på** | Angiver, ud fra hvilken debitor/kreditorkode momsnummeret tages til Intrastat-rapporten. Du kan vælge mellem følgende indstillinger: **Sælg-til-moms** eller **Fakturer-til-moms**. |
   | **Virksomhedens registrerede momsnr.** | Angiver, hvordan virksomhedens momsregistreringsnummer udlæses til Intrastat-filen. Du kan vælge en af mulighederne: Momsreg.nr., tilføje EU-landekoden som et præfiks og fjerne EU-landekoden fra Momsreg.nr. |
   | **Kreditors registrerede momsreg.nr.** | Angiver, hvordan en kreditors momsregistreringsnummer udlæses til Intrastat-filen. Du kan vælge en af mulighederne: Momsreg.nr., tilføje EU-landekoden som et præfiks og fjerne EU-landekoden fra Momsreg.nr. |
   | **Debitors registrerede moms-nr.** | Angiver, hvordan en debitors momsregistreringsnummer udlæses til Intrastat-filen. Du kan vælge en af mulighederne: Momsreg.nr., tilføje EU-landekoden som et præfiks og fjerne EU-landekoden fra Momsreg.nr. |
   | **Hent partnermoms** | Angiver den linjetype for **Intrastat-rapport**, som partnerens momsregistreringsnummer opdateres fra. Afhængigt af dine lokale krav kan du vælge kun til modtagelse, kun til afsendelse eller for begge linjetyper. |
3. Udfyld felterne efter behov i oversigtspanelet **Standardtransaktioner**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] I nedenstående tabel beskrives nogle af nøglefelterne:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Standardtransaktionstype** | Angiver standardtransaktionstypen for almindelige salgsleverancer, serviceleverancer og købsmodtagelser. |
   | **Standardtransaktionstype – returneringer** | Angiver standardtransaktionstypen for salgsreturneringer, servicereturneringer og købsreturneringer. |
   | **Standardmomsnr. for privat person** | Angiver standardmomsnr. for private personer i tilfælde, hvor den private person skal have et bestemt momsnummer i Intrastat-rapporten. |
   | **Standardmomsnr. for tredjeparts handel** | Angiver standardmomsnr. for tredjepartshandel, hvis du ikke har momsnummeret. |
   | **Standardmoms for ukendt tilstand** | Angiver standardmomsnummeret for en ukendt tilstand. |
   | **Kode for standardland/område** | Angiver standardkoden for modtagerland/område. |
4. Udfyld felterne efter behov i oversigtspanelet **Rapportering**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] I nedenstående tabel beskrives nogle af nøglefelterne:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Definitionskode for dataudveksling** | Angiver den kode for dataudvekslingsdefinition, som Intrastat-filen skal genereres med. Feltet fungerer kun, hvis feltet **Opdel modtagelser/afsendelsesfiler** er angivet som **Nej**. |
   | **Opdel modtagelser/afsendelsesfiler** | Angiver, om modtagelser og afsendelser skal rapporteres i to separate filer. |
   | **Zip-fil(er)** | Angiver, om der skal føjes rapportfiler til .zip-filen. |
   | **Dataudvekslingsdefinitionskode ⁠– Modtagelse** | Angiver dataudvekslingsdefinitionskoden til at genere Intrastat-filen for modtagne varer. Feltet fungerer kun, hvis feltet **Opdel modtagelser/afsendelsesfiler** er angivet som **Ja**. |
   | **Dataudvekslingsdefinitionskode ⁠– Leverance** | Angiver dataudvekslingsdefinitionskoden til at genere Intrastat-filen for leverede varer. Feltet fungerer kun, hvis feltet **Opdel modtagelser/afsendelsesfiler** er angivet som **Ja**. |
5. Åbn oversigtspanelet **Nummerering** for at oprette **Intrastat-numre**.

### Konfigurere en rapporteringsfil

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Dataudvekslingsdefinitioner**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Brug oversigtspanelet **Generelt** til at beskrive dataudvekslingsdefinitionen, datafiltypen, kolonneseparator, relaterede codeunits, XMLport og andre felter ved at udfylde felterne.
4. I oversigtspanelet **Linjedefinitioner** kan du beskrive formateringen af linjer i datafilen ved at udfylde felterne på grundlag af feltet **Linjetype**, og hvor du vil angive antallet af kolonner for denne linje.
5. Udfyld linjen for hver planlagt kolonne i oversigtspanelet **Kolonnedefinitioner**. Du kan definere kolonnenavne, datatyper (*Tekst*, *Dato* eller *Decimal*), længden på linjen med fast bredde, der indeholder kolonnen, hvis filen er af typen Fasttekst, og nogle andre parametre.
6. Vælg handlingen **Felttilknytning** i oversigtspanelet **Linjedefinitioner** for at åbne siden **Felttilknytning**.
7. Opret den nye post, og i oversigtspanelet **Generelt** skal du vælge det relevante **Tabel-id** (for **Intrastat-rapportlinje** skal du vælge 4812) og derefter udfylde flere felter:
   1. Angiv nøgleindekset, der sorterer kildeposterne inden eksport, i feltet **Nøgleindeks**.
   2. Vælg den korrekte **Koblings-codeunit**.
8. Tilføj de kolonner, du tidligere har konfigureret i oversigtspanelet **Kolonnedefinitioner**, i oversigtspanelet **Felttilknytning**, og tilføj derefter følgende:
   1. Angiv **Felt-id** for hver kolonne.
   2. Angiv **Transformationsregel** for hver enkelt kolonne, du har brug for. Den angiver den regel, der omdanner importeret tekst til en understøttet værdi, før den kan knyttes til et angivet felt i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du vælger en værdi i dette felt, angives den nøjagtige værdi i feltet **Transformationsregel** i feltet tabellen **Koblingsbuffer for feltet Dataudveksling** og omvendt.
9. Hvis du har brug for at gruppere poster baseret på nogle kolonner, skal du i oversigtspanelet **Feltgruppering** vælge de felter, du vil bruge til gruppering.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] indeholder den forudkonfigurerede dataudvekslingsdefinition for Intrastat til alle lokaliserede lande/områder. Du kan finde flere oplysninger om oprettelse af en dataudvekslingsdefinition i artiklen [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

### Angive obligatoriske felter med Intrastat-rapportens kontrolliste

I nogle lande kræver myndighederne, at Intrastat-rapporter omfatter f.eks. leveringsformen for køb eller andre værdier, når salgsordren er over en bestemt grænse.

Sådan angives obligatoriske felter og/eller værdier på **Intrastat-rapport**-siden:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af Intrastat-rapport**, og vælg derefter det relaterede link.
2. Vælg handlingen **Tjekliste til Intrastat-rapport**.
3. Tilføj de nødvendige linjer til kontrol af følgende instruktioner:
   1. Indstil feltet **Feltnr.** til et felt, der skal kontrolleres for en ikke-tom værdi.
   2. Udfyld om nødvendigt **Filterudtryk**-feltet ud fra følgende regler:
      1. Når du åbner **Filterside**, skal du vælge det **Filter**, du skal bruge til kontrol.
      2. I det næste trin skal du vælge en værdi, der er relateret til det **Filter**, du har brugt.
      3. Hvis du har flere filtre, skal du udfylde dette felt, og du kan tilføje endnu et filter på samme måde.
      4. Klik på **OK**, når du er færdig med at indtaste filtre til det valgte felt.
   3. Vælg feltet **Tilbageført filterudtryk** for at angive, at kontrollen af felter kun køres på de linjer, der ikke matcher med filterudtrykket. Hvis linjen ikke er filtreret, ignoreres dette felt.

> [!NOTE]
> Når du åbner **Filterside** fra **Filterudtryk**-linjen, kan du bruge alle standardfilterudtryk, der er knyttet til det specifikke felt, du vil filtrere.
>
> Vær forsigtig, når du konfigurerer valideringsregler. De kan være forskellige fra land/område til land/område.

## Bruge tilpassede codeunits i Intrastat-rapporting

Hvis du vil ændre den måde, som Intrastat fungerer på, og standardkonfigurationen ikke er nok, kan du tilpasse systemet ved at udvide standardfunktionerne. Hvis du vil ændre Intrastat-funktionaliteten yderligere, kan du selv udvikle dine egne codeunits. Når du opretter codeunits, skal du imidlertid foretage yderligere ændringer for at bruge dem. Sådan konfigureres systemet til at bruge dine egne objekter:

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfiguration af momsrapporter**, og vælg derefter det relaterede link.
2. På siden **Konfiguration af momsrapporter** skal du tilføje en ny linje.
3. Vælg **Intrastat-rapport** i feltet **Momsrapporttype**.
4. Angiv versionen af rapporten i feltet **Momsrapportversion**.
5. Derefter kan du tilføje dine codeunits for følgende indstillinger: a. I feltet **Codeunit-id for Foreslå linjer** skal du angive den nye codeunit for forslag til linjer på Intrastat-rapportlinjerne.
   b. I feltet **Codeunit-id for indhold** skal du angive den nye codeunit for eksport af data som en fil ved hjælp af en dataudvekslingsdefinition.
   c. I feltet **Codeunit-id for validering** skal du angive de nye codeunits for validering af resultater på Intrastat-rapportlinjerne.

> [!IMPORTANT]
>
> Denne linje skal være tom, hvis du bruger standard-codeunits. Du skal kun oprette en linje og konfigurere den, hvis du har udviklet egne codeunits.

## Andre Intrastat-konfigurationer

> [!IMPORTANT]
> Debitorkort og kreditorkort indeholder et felt, **Intrastat-partnertype**, der har de samme indstillingsværdier som feltet **Partnertype**: "" (tom), *Virksomhed* og *Person*. Feltet **Intrastat-partnertype** har erstattet feltet **Partnertype** i Intrastat-rapportering. Feltet **Partnertype** bruges i SEPA (Single Euro Payments Area) til at definere SEPA Direct debet-skema (Core eller B2B). Feltet **Intrastat-partnertype** bruges kun til Intrastat-rapportering. På den måde kan du angive forskellige værdier til de to felter, hvis det er nødvendigt.
>
> Hvis feltet **Intrastat-Partnertype** er tomt, bruges værdien fra feltet **Partnertype** til Intrastat-rapportering.

Undtagen for **Opsætning af Intrastat-rapport**, **Dataudvekslingsdefinitioner** og **Tjekliste til Intrastat-rapport** skal du også konfigurere andre indstillinger:

| Side | Beskrivelse |
| ---- | ----------- |
| **Lande/områder** | Før du begynder at bruge Intrastat-rapporter, skal du også konfigurere siden **Lande/områder**. På denne side skal du tilføje **EU-lande-/områdekode** og **Intrastat-kode** for at angive en kode for det land/område, du handler med, da den skal bruges i Intrastat-rapportering. |
| **Varekoder** | I mange lande har told- og·skattemyndighederne etableret ottecifrede koder til de forskellige varer. Hvis vareposter skal indeholde de nødvendige oplysninger, når de indlæses i Intrastat-kladdelinjen, skal du have angivet varekoden på siden **Varekoder**: Find varekoderne på de varer, dit firma handler med, og indsæt dem på siden **Varekoder**. |
| **Transportmåder** | Der er syv encifrede koder til Intrastat-transportmåder. **1** for vand, **2** for jernbane, **3** for vej, **4** for fly, **5** for post, **7** for faste installationer og **9** for egen fremdrift (f.eks. transport af en bil ved at køre den). [!INCLUDE[prod_short](includes/prod_short.md)] kræver ikke disse koder, men det anbefales, at beskrivelserne indeholder den samme betydning. |
| **Transaktionsarter** | Lande og områder har forskellige koder for de typer Intrastat-transaktioner, som almindeligt køb og salg, ombytning af returnerede varer og ombytning af ikke-returnerede varer. Opret alle de koder, der gælder for dit land/område. Du kan bruge disse koder i oversigtspanelet **Udenrigshandel** på salgs- og købsdokumenter, og når du behandler returneringer. |
| **Transaktionsspecifikationer** | Definer koder, der supplerer transaktionsartens beskrivelser. |
  > [!NOTE]
  > Fra og med januar 2022 kræver Intrastat forskellige koder for transaktionsarten ved afsendelser til private personer eller ikke-momsregistrerede virksomheder og registrerede virksomheder. For at efterkomme dette krav anbefales det, at du gennemgår og/eller tilføjer nye posteringsartkoder på **Transaktionsarter**-siden i henhold til kravene i dit land. Du kan også tjekke og opdatere feltet **Intrastat-partnertype** for *Person* for privatperson eller ikke-momsregistrerede erhvervskunder på den relevante **Kunde**-side. Hvis du ikke er sikker på den korrekte Intrastat-partnertype eller transaktionstype, anbefales det, at du spørger en ekspert i dit land eller område.

| **Felt** | **Beskrivelse** |
| --------- | --------------- |
| **Nettovægt** | Vægt er en af de grundlæggende konfigurationer, der relaterer til Intrastat-rapportering, da den **Samlede vægt** skal angives til rapportering. Du skal også udfylde feltet **Nettovægt** på varekortet eller anlægskortet for at være klar til dette krav. |
| **Oprindelseskode for land/område** | Brug ISO alpha-koderne på to bogstaver på varekortet eller anlægskortet for det land, hvor varen er anskaffet eller produceret. Hvis det er produceret i mere end ét land, er oprindelseslandet det sidste land, hvor det blev væsentligt behandlet. |
| **Partnerens momsregistreringsnummer i importmedlemsstaten** | Det er partnerens momsregistreringsnummer i importmedlemsstaten. MOMS-ID bruges også til udveksling af EU-eksportdata mellem medlemsstaterne og giver medlemsstaterne mulighed for at allokere de modtagne oplysninger til det importerende selskab i deres eget land. Rapporteringsenheder skal rapportere momsnr. for det selskab, der har angivet, at varer inden for Unionen er blevet erhvervet i importmedlemsstaten. |

Du kan også konfigurere:

* **Varekoder**: Told- og skattemyndigheder har defineret numeriske koder, der klassificerer varer og serviceydelser. Du kan angive disse koder for varer.
* **Områder**: Supplerende oplysninger om lande og områder.
* **Indførsels-/ udførselssteder**: Angiv de lokationer, hvor du sender eller modtager varer til eller fra andre lande. En lufthavn er et eksempel på et indførsels-/udførselssted. Du kan angive indførsels-/udførselssteder i salgs- og købsdokumenter i oversigtspanelet **Udenrigshandel**. Oplysningerne kopieres også fra vareposterne, når du opretter Intrastatkladden.
* **Supplerende enhedskode**: Mængden af varer til Intrastat-rapportering kan være enten nettovægt (i kg) eller en supplerende enhed. Hvis der er behov for supplerende enheder, skal du konfigurere dem til varer og anlægsaktiver.

#### Definere transportmåder

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Transportmåder**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Konfigurere koder for transaktionsarter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Transaktionsarter**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Andre relaterede konfigurationer

Før du bruger funktionen Intrastat-rapportering, skal du konfigurere nogle felter på vare-, anlægsaktiv-, debitor- og kreditorkortene.

#### Varekort

Sådan konfigureres alle nødvendige oplysninger, der vedrører Intrastat, på varekort:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Varer**, og vælg derefter det relaterede link.
2. Vælg den vare, du vil konfigurere.
3. I oversigtspanelet **Omkostninger og bogføring** skal du udfylde felterne **Tarifnr.**, **SSupplerende enhed** og **Oprindelseskode for land/område**.
4. I oversigtspanelet **Lager** skal du angive decimalværdien i feltet **Nettovægt**.

> [!NOTE]
> Du kan bruge forskellige måleenheder som din supplerende enhedskode. Hvis det ikke er det samme som **basisenheden**, skal du konfigurere denne enhed på siden **Vareenheder**.

#### Anlægskort

Sådan konfigureres alle nødvendige oplysninger, der vedrører Intrastat, på anlægskort:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, du vil konfigurere.
3. I oversigtspanelet **Intrastat** skal du udfylde felterne **Tarifnr.**, **Nettovægt**og **Supplerende enhed**.

> [!NOTE]
> Du kan bruge forskellige måleenheder som din supplerende enhedskode. Men uanset hvilken **Enhedskode**, du vælger, vil dens **Antal** altid være 1 i Intrastat-rapporter.

#### Kreditorkort

Før du bruger en kreditor i Intrastat-rapportering, skal du have en dedikeret **Lande-/områdekode** og **Momsregistreringsnr.** for hver af dem i tillæg til yderligere oplysninger på deres **Kreditorkort**-side:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Kreditorer**, og vælg derefter det relaterede link.
2. Vælg den kreditor, du vil konfigurere.
3. I oversigtspanelet **Intrastat** kan du angive standardværdier for felterne **Standardtransaktionstype**, **Standardtransaktionstype – returneringer** og **Standardtransportmåde**.
4. I oversigtspanelet **Betalinger** skal du i feltet **Intrastat-partnertype** angive, om kreditoren er en person eller en virksomhed.

#### Debitorkort

Før du bruger en debitor i Intrastat-rapportering, skal du have en dedikeret **Lande-/områdekode** og **Momsregistreringsnr.** for hver af dem i tillæg til yderligere oplysninger på deres **Debitorkort**-side:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Debitorer**, og vælg derefter det relaterede link.
2. Vælg den debitor, du vil konfigurere.
3. I oversigtspanelet **Intrastat** kan du angive standardværdier for felterne **Standardtransaktionstype**, **Standardtransaktionstype – returneringer** og **Standardtransportmåde**.
4. I oversigtspanelet **Betalinger** skal du i feltet **Intrastat-partnertype** angive, om kreditoren er en person eller en virksomhed.

#### Udelade varer og anlægsaktiver fra Intrastat-rapportering

Hvis der er grund til, at en bestemt vare eller et bestemt anlægsaktiv udelukkes fra Intrastat-rapportering, skal du ændre en indstilling på kortet.

##### Udelade en vare fra Intrastat-rapportering

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Varer**, og vælg derefter det relaterede link.
2. Vælg den vare, du vil konfigurere.
3. I oversigtspanelet **Omkostninger og bogføring** skal du markere feltet **Udeluk fra Intrastat-rapport**.

##### Udelade et anlægsaktiv i Intrastat-rapportering

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, du vil konfigurere.
3. I oversigtspanelet **Intrastat** skal du markere feltet **Udeluk fra Intrastat-rapport**.

## Opsætning af landespecifik Intrastat

Intrastat-kravene er næsten de samme i alle EU-medlemsstater, men der er vigtige undtagelser. I teorien bør reglerne anvendes ensartet i alle medlemsstater. Der er imidlertid forskelle i implementeringen, fordi nogle medlemsstater fastsætter retningslinjer for, hvordan de generelle principper i forordningen skal anvendes i særlige situationer. F. eks. kommercielle prøver, returvarer osv. Disse retningslinjer kan give forskellige resultater for forskellige situationer i EU-medlemslande. Derfor har nogle lande visse ekstra specifikke oplysninger, der er anderledes end i andre lande. De bruger også et andet filformat til rapportering.

### Østrig

Intrastat-rapportering i Østrig kræver to forskellige filer til modtagelser og forsendelser. Følg disse trin for at kontrollere, at opsætningen er korrekt:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af Intrastat-rapport**, og vælg derefter det relaterede link.  
2. I oversigtspanelet **Rapportering** skal du kontrollere, om **Opdel modtagelser/afsendelsesfiler** er valgt. I relation til dette kan du se, at der er konfigureret to separate **Definitionskoder for dataudveksling**. Feltet **Zip-fil(er)** er også markeret for at sikre, at rapportfiler bliver føjet til zip-filen.

Arbejdsprocessen i forbindelse med Intrastat-rapporter er den samme som i den globale funktion.

<!-- ### Belgium-->

### Tjekkiet

Den nye Intrastat-rapport-oplevelse for Tjekkiet vil være tilgængelig fra 2023-udgivelsesbølge 1. I mellemtiden kan du fortsætte med at bruge funktionen **Intrastat-kladde**.

### Finland

I Finland er der et par ekstra trin til opsætning af Intrastat. Intrastat-rapportering i Finland kræver to forskellige filer til modtagelser og forsendelser. I relation til dette kan du se, at der er konfigureret to separate **Definitionskoder for dataudveksling**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af Intrastat-rapport**, og vælg derefter det relaterede link.  
2. På siden **Opsætning af Intrastat-rapport** skal du i oversigtapanelet **Filopsætning** udfylde felterne som beskrevet i følgende tabel:

    |Felt|Beskrivlse|  
    |------------------------------------|---------------------------------------|
    | **Brugerdefineret kode**|Angiver en brugerdefineret kode til oplysningerne om opsætningen af Intrastat-filer. |
    | **Virksomhedsserienr.**|Angiver et virksomhedsserienummer til oplysningerne om opsætningen af Intrastat-filer. |

3. I oversigtspanelet **Rapportering** skal du kontrollere, om **Opdel modtagelser/afsendelsesfiler** er valgt.

Arbejdsprocessen i forbindelse med Intrastat-rapporter er den samme som i den globale funktion.

<!-- ### Germany-->

### Italien

Ny Intrastat-rapport-oplevelse for Italien vil være tilgængelig fra februar 2023. I mellemtiden kan du fortsætte med at bruge funktionen **Intrastat-kladde**.

<!-- ### France-->

### Sverige

Intrastat-rapportering i Sverige kræver to forskellige filer til modtagelser og forsendelser. Følg disse trin for at kontrollere, at opsætningen er korrekt:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af Intrastat-rapport**, og vælg derefter det relaterede link.  
2. I oversigtspanelet **Rapportering** skal du kontrollere, om **Opdel modtagelser/afsendelsesfiler** er valgt. I relation til dette kan du se, at der er konfigureret to separate **Definitionskoder for dataudveksling**.

Arbejdsprocessen i forbindelse med Intrastat-rapporter er den samme som i den globale funktion.

<!-- ### United Kingdom-->

## Se relateret træning på [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## Se også

[Intrastat-rapportering i Business Central](finance-how-report-intrastat.md)  
[Økonomistyring](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
