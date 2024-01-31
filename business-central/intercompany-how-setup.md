---
title: Konfigurere bogføring af koncernintern transaktion
description: 'Lære, hvordan du opretter et internt partnerskab.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 09/27/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621'
ms.service: dynamics-365-business-central
---
# Konfigurere koncerninterne transaktioner

Intercompany-partnerskaber gør det nemmere at håndtere regnskabs processer, når to eller flere datterselskaber ofte gør forretninger med hinanden. Partnere kan udveksle transaktioner, f. eks. salg og køb, og håndtere dem enten manuelt eller automatisk. Når en partner f. eks. sender en salgskladdelinje til en anden partner, oprettes der en købskladdelinje for den modtagende partner.

Intercompany-kontoplanen kan f.eks. være en udgave af synkroniserede partners kontoplan. Hver partner knytter deres konti til IC-kontoplanen. Hver partner knytter også dimensionerne og dimensionsværdierne til IC-dimensionerne.

> [!NOTE]
> I 2023 udgivelsesbølge 1 vi har introduceret en forbedret side **Koncernintern konfiguration**. Den nye side gør det nemmere at oprette et internt partnerskab ved at konsolidere alle opsætningsopgaverne på en enkelt side. Hvis du er ny i [!INCLUDE [prod_short](includes/prod_short.md)], bruger du den nye oplevelse. Hvis du allerede er kunde, kan administratoren slå funktionen til **Automatisk accept af IC-finanskladdetransaktioner** på siden **funktionsstyring**.
>
> Opgaverne i denne artikel forudsætter, at funktionsparameteren er aktiveret. Hvis du allerede har oprettet et internt partnerskab, kan du fortsætte med at bruge det.

## Før du starter

Før du begynder at oprette et internt partnerskab, er der nogle få beslutninger, du skal foretage.

|Beslutning  |Beskrivlse  |
|---------|---------|
|Hvilke kontoplaner skal danne grundlag for IC-kontoplanen?     | Alle firmaer i partnerskabet skal bruge samme IC-kontoplan. Du kan basere IC-kontoplanen på kontoplanen fra et af regnskaberne i partnerskabet eller oprette en ny IC-kontoplan. Du kan knytte de konti, der skal bruges, i partnerskabet på begge måder, så hver partner både sender og modtager transaktioner i de korrekte konti. Få mere at vide om oprettelse af IC-kontoplanen på [Konfigurere IC-kontoplaner](#set-up-the-intercompany-charts-of-accounts).         |
|Hvilke dimensioner skal der være grundlaget for IC-dimensionerne?     | Hvis du bruger IC-dimensioner, skal de være ens for alle regnskaber i partnerskabet. Når du har angivet IC-dimensionerne, skal du tilknytte deres dimensionsværdier. Få mere at vide om tilknytning af dimensionsværdier til [Opsætning af IC-dimensioner](#set-up-intercompany-dimensions).        |
|Hvilke partnere er debitorer eller kreditorer?     |  Få mere at vide om oprettelse af debitorer og kreditorer i et IC-partnerskab på [Konfigurere IC-partnere som debitorer og kreditorer](#set-up-intercompany-partners-as-customers-and-vendors).       |
|Vil du angive bankkonti, der skal bruges i partnerskabet?| Du kan gøre det hurtigere at registrere betalingstransaktioner ved at angive den bankkonto, der skal bruges til hver enkelt partnervirksomhed. Få mere at vide på [Angiv de bankkonti, der skal bruges til IC-partnere](#specify-the-bank-accounts-to-use-for-intercompany-partners). |
|Hvordan skal virksomhederne identificeres i partnerskabet?     | Alle parter skal aftale en entydig identifikationskode for intercompany-partner for hvert regnskab. Du skal tildele koden til debitor- og kreditorkort for at kunne identificere relaterede transaktioner. Få mere at vide om id'er ved [Oprette nummerserier](ui-create-number-series.md).        |
|Hvordan vil du håndtere varenumre?     | Hvis koncerninterne linjer indeholder varer, kan du enten bruge egne varenumre, eller du kan angive partnerens varenumre for hver relevant vare. Brug enten feltet **Leverandørs varenr.** eller **Fælles varenr.** på varekortet. Du kan også bruge handlingen **Varereference** til at knytte varenumrene til dine IC-partneres beskrivelser af varerne. Hvis du vil vide mere om varereferencer, skal du gå til [Brug af varereferencer](inventory-how-use-item-cross-refs.md).        |
|Er ressourcer involveret?     | Hvis du skal foretage IC-salgstransaktioner, der omfatter ressourcer, skal du udfylde feltet **Finanskt.nr. for IC-partnerkøb** på ressourcekortet til hver relevant ressource. Feltet indeholder nummeret på den IC-finanskonto, som prisen på denne ressource bogføres på i din partners virksomhed. Du kan få mere at vide om ressourcer ved at gå til [Konfigurere ressourcer](projects-how-setup-resources.md).<br><br>**Bemærk**<br>Koncerninterne købstransaktioner, der omfatter ressourcer, anlægsaktiver og varegebyrer, understøttes ikke fuldstændigt. I den koncerninterne partnervirksomhed er feltet **Linjetype** tomt på købsdokumentlinjer, som indeholder disse enheder. Du skal opdatere feltet manuelt.        |

## Oversigt over de trin til at komme i gang

Brug siden **IC-opsætning** til at oprette følgende komponenter af IC-transaktioner:

* Indstillingerne for den interne virksomhed.
* Det firma, som skal være synkroniseringspartneren.
* Den IC-kontoplan, som alle partnere bruger på at udveksle transaktioner.
* Tilknytningerne mellem konti i kontoplanen og IC-kontoplanen for indgående og udgående transaktioner for hver partner.
* Koncerninterne dimensioner og dimensionsværdier til brug og hvordan de tilknyttes til dimensionerne for hver partner.
* Virksomheder, som er partnerens koncerninterne partnere.
* Virksomheder, der er leverandører eller debitorer, eller begge dele.

## Konfigurere en synkroniseringspartner

Alle partnere skal bruge samme IC-kontoplan og, hvis det er nødvendigt, den samme IC-dimension. Du kan spare tid, når du opretter partnerskabet ved hjælp af kontoplanen og dimensioner for en af partnerne som en oprindelig plan for IC-kontoplanen og-dimensioner. Den virksomhed, som du bruger som basislinje, kaldes *synkroniseringspartneren*. Synkroniseringspartneren er som regel Headquarter-firmaet, men det behøver ikke være.

På siden **IC-opsætning** angiver hver partner synkroniseringspartneren i feltet **Synkroniseringspartner** . Derefter angives IC-kontoplanen og IC-dimensionerne automatisk for dem baseret på konfigurationen af synkroniseringspartneren. Partnerne bruger derefter indstillingerne for **Intercompany-kontoplanen** og **intercompany-dimensioner**-siderne til at knytte deres kontoplan og dimensioner til IC-kontoplanen og -dimensioner og omvendt. 

> [!NOTE]
> Det er vigtigt at knytte konti og dimensioner til begge retninger. Både for IC-kontoplanen og-dimensioner, og fra dem til dine egne konti og dimensioner.

### Opret forbindelse til partnere i en anden lejer eller et andet miljø

Hvis en eller flere partneres [!INCLUDE [prod_short](includes/prod_short.md)] er i en anden lejer eller et andet miljø, er der et par ekstra trin til at oprette forbindelsen. Trinnene gælder for alle partnere i en anden lejer eller et andet miljø.

* Konfigurer [!INCLUDE [prod_short](includes/prod_short.md)] som en registreret app på Azure Portal.
* Tilføj og aktiver appregistreringen i [!INCLUDE [prod_short](includes/prod_short.md)].
* Udveksle oplysninger om deres interne opsætninger. Hver partner kan få disse oplysninger fra den assisterede opsætningsvejledning til **IC-partner på tværs af miljøer**.

   |Kopiér fra partnerens opsætning  |Kopiér til din opsætning  |
   |---------|---------|
   |URL-adresse til aktuel forbindelse     |URL-adresse til IC-partners forbindelse         |
   |Aktuelt virksomheds-id     |IC-partnerens virksomheds-id         |
   |Internt id     |IC-partnerens interne id         |
   |Virksomhedens navn     |IC-partnerens virksomhedsnavn         |

* Udveksl følgende godkendelsesindstillinger, så [!INCLUDE [prod_short](includes/prod_short.md)] kan godkende, når der oprettes forbindelse. Hver partner kan få disse oplysninger fra deres registrerede app. Du kan få mere at vide om, hvordan du opretter en registreret app, ved at gå til [Opret en registreret app på Azure Portal](#create-a-registered-app-in-azure-portal).  

  * Klient-id
  * Klienthemmelighed
  * Tokenslutpunkt
  * Omdiriger URL-adresse

Kør den assisterede opsætningsvejledning til **Konfiguration af IC-partner på tværs af miljøer** i alle firmaer for at angive oplysningerne. Hvis du vil starte guiden, skal du bruge handlingen **Opret forbindelse eksternt** på siden **Intercompany-partner**.

#### Opret en registreret app på Azure Portal

Denne proces er kun nødvendig, hvis du vil oprette forbindelse til en partner, hvis [!INCLUDE [prod_short](includes/prod_short.md)] er i en anden lejer eller et andet miljø.

> [!TIP]
> Det er en god ide at have et tekstredigeringsprogram åbent, f.eks. Notesblok, mens du opretter din registrerede app. Du skal bruge nogle af oplysningerne, når du kører den assisterede opsætningsvejledning til **Konfiguration af IC-partner på tværs af miljøer**, så det er rart at have oplysningerne ved hånden.

1. Gå til [Azure-portal](https://portal.azure.com/#home).
2. Vælg tjenesten **Microsoft Entra ID**.
3. Vælg **App-registreringer** i navigationsruden.
4. På siden **Appregistreringer** skal du vælge **Ny registrering**.
5. Angiv et navn til programmet.
6. Vælg kontotypen **Konti i en hvilken som helst organisationsmappe (vilkårlig Microsoft Entra id-lejer - multilejer)**.
7. For omdirigerings-URI'en skal du i feltet vælge **Web** og derefter angive URI i feltet **Vælg en platform**. F.eks. \**https://businesscentral.dynamics.com/OAuthLanding.htm**.

  Hvis du arbejder med en integreret ISV, skal du muligvis bruge en anden URI.

8. Registrer appen.
9. Vælg **API-tilladelser** i navigationsruden på siden **Intercompany-app**.
10. Vælg handlingen **Tilføj en tilladelse**.
11. Vælg **Dynamics 365 Business Central** på fanen **Microsoft API'er**.
12. Vælg **Programtilladelser** i ruden **Anmod om API-tilladelser**, og vælg derefter **API.ReadWrite.All**-tilladelsen.
13. På siden **Intercompany-app | API-tilladelser** skal du vælge handlingen **Giv administratorsamtykke til Contoso** og derefter give samtykke.
14. Gå til navigationsruden, og vælg **Certifikater og hemmeligheder**.
15. Vælg fanen **Klienthemmeligheder**, og vælg derefter **Ny klienthemmelighed**.
16. Angiv et navn til hemmeligheden i ruden **Tilføj en klienthemmelighed**, og angiv, hvornår den udløber.

  > [!NOTE]
  > Alle partnere, der er i forskellige miljøer, skal forny hemmeligheden, før den udløber.

  > [!IMPORTANT]
  > Kopiér id'et i feltet **Værdi**, før du forlader siden **Intercompany-appen | Certifikater og hemmeligheder**. Du skal bruge den i et senere trin, og den vil ikke være tilgængelig, når du forlader siden. Indsæt f.eks. værdien i et tekstredigeringsprogram.

17. Gå til navigationsruden, og vælg **Oversigt**.
18. Kopiér værdien fra feltet **Program (klient)-id**. Indsæt f.eks. værdien i et tekstredigeringsprogram.
19. Vælg handlingen **Slutpunkter**, og kopiér derefter værdien i feltet **OAuth 2.0-tokenslutpunkt (v2)**. Indsæt f.eks. værdien i et tekstredigeringsprogram.
20. Kopiér værdien fra feltet **Directory (lejer)-id**. Indsæt f.eks. værdien i et tekstredigeringsprogram.
21. I den tokenværdi, du kopierede, skal du erstatte **organisationer** med den værdi, du kopierede fra feltet **Directory (lejer)-id** i forrige trin.

#### Tilføj og aktivér din registrerede app i Business Central

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Microsoft Entra-programkort**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Vælg **Aktiveret** i feltet **Status**. 
4. Vælg handlingen **Giv samtykke**. 
5. I feltet **Tilladelsessæt** skal du vælge **API – Intercompany-tilladelsessæt på tværs af miljøer**.

## Oprette IC-kontoplanen

Alle partnere skal bruge samme IC-kontoplan og knytte kontiene i deres egen kontoplan til den. Hvis kontoplanen i din virksomhed definerer IC-kontoplanen for partnerne, skal du følge fremgangsmåden i dette afsnit.

Hvis du bruger en XML-fil, der indeholder IC-kontoplanen, skal du følge trinnene i [Importere eller eksportere en IC-kontoplan](intercompany-how-setup.md#import-or-export-an-intercompany-chart-of-accounts).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern konfiguration**, og vælg derefter det relaterede link.
2. Vælg handlingen **IC-kontoplan**.
3. På siden **Koncernintern kontoplan** kan du tilføje konti på en linje på siden:
    * Vælg **Ny**, og angiv derefter hver konto på en linje på siden.  
    * Hvis den koncerninterne kontoplan skal være identisk med eller ligge tæt opad din almindelige kontoplan, kan du få udfyldt siden automatisk ved at vælge handlingen **Kopier fra kontoplan**. Du kan redigere nye linjer efter behov.
    * Hvis du har oprettet en intercompany-kontoplan til en synkroniseringspartner, skal du bruge handlingen **Synkroniseringsopsætning** til at kopiere disse konti.

    > [!TIP]
    > Hvis du kopierer IC-kontoplanen fra en synkroniseringspartner, kan du bruge handlingen **Synkroniseringsopsætning** til at opdatere IC-kontiene med de ændringer, som partneren foretager.

Det næste trin er at tilknytte IC-kontoplanen til regnskabets kontoplan. Flere oplysninger i [Tilknytte IC-kontoplanen til regnskabets kontoplan](#map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts).

### Importere eller eksportere den koncerninterne kontoplan

Synkroniseringsfirmaet kan dele sin kontoplan med partnere ved at eksportere det til en fil. Partnere kan indlæse filen for at få kontoplanen.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern konfiguration**, og vælg derefter det relaterede link.
2. Vælg handlingen **IC-kontoplan**.
3. På siden **Koncernintern kontoplan** skal du vælge handlingen **Import/Eksport** og derefter vælge **Import** eller **Eksport**.
4. Vælg den fil, der skal importeres eller eksporteres.  

Siden **IC-kontoplan** udfyldes med nye eller redigerede finanskontolinjer i overensstemmelse med den koncerninterne kontoplan i filen. Alle eksisterende, ikke-relaterede linjer på siden forbliver uændrede.

## Tilknytte IC-kontoplanen til regnskabets kontoplan  

Når du har defineret eller indlæst IC-kontoplanen, skal du knytte hver IC-konto til en af dine konti. På siden **IC-kontoplan** angiver du, hvordan IC-finanskonti på indgående transaktioner skal oversættes til finanskonti i dit regnskabs kontoplan.

Hvis IC-kontiene og kontiene har samme nummer, kan du knytte kontiene automatisk.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern konfiguration**, og vælg derefter det relaterede link.  
2. Vælg handlingen **IC-kontoplan**.

    > [!TIP]
    > Hvis du vil have adgang til handlingerne på siden, skal du muligvis udvide siden til visningen i bredformat.

3. På siden **Koncernintern kontoplan** skal du vælge handlingen **Tilknytning af kontoplan**.
4. Du kan tilknytte konti automatisk eller manuelt.

    * Hvis du vil oprette tilknytningen manuelt, skal du vælge en konto i vinduet **kontoplan** og **finanskontoplan**, og derefter vælge en konto i feltet **Finanskontonr.** og **IC-nr.** .
    * Hvis du automatisk vil tilknytte konti, der har samme nummer, skal du markere de linjer, du vil tilknytte, vælge **Tilknytning til konto. med samme nr.**-handlingen og derefter vælge den kontoplan, der skal opdateres.

    > [!TIP]
    > Hvis du vil tilknytte mange eller alle konti, skal du vælge en linje, vælge :::image type="icon" source="media/show-more-options-icon.png" border="false"::: og derefter vælge **Vælg flere**.

## Konfigurere koncerninterne dimensioner

Hvis partnere vil kunne udveksle transaktioner med tilknyttede dimensioner, skal I aftale, hvilke dimensioner I alle skal bruge. Synkroniseringsselskabet i en koncern kan f.eks. oprette en forenklet version af deres egne dimensionssæt, eksportere dem til en XML-fil, der kan distribueres til hver virksomhed i gruppen. Hver partner kan indlæse XML-filen på siden **IC-dimensioner** og derefter knytte IC-dimensionerne til deres dimensioner. Flere oplysninger i [Sådan knyttes IC-dimensioner til dimensioner i regnskabet](#map-intercompany-dimensions-to-your-companys-dimensions).

> [!NOTE]
> Hvert regnskab skal knytte deres dimensioner til IC-dimensionerne for udgående og indgående dokumenter. Det er vigtigt at tilknytte konti i begge retninger, hvilket er med til at sikre ensartethed på tværs af virksomhederne.

Hvis partnere bruger IC-dimensionerne i synkroniseringspartneren, skal du følge fremgangsmåden i dette afsnit. Hvis du vil dele brug af en XML-fil, der indeholder IC-dimensioner, skal du følge trinnene i [Importere eller eksportere en IC-dimensioner](#import-or-export-intercompany-dimensions).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern konfiguration**, og vælg derefter det relaterede link.  
2. Vælg handlingen **IC-dimensioner**.
3. Tilføj dimensioner ved at gøre følgende på siden **Koncerninterne dimensioner**:
    * Vælg **Ny**, og angiv derefter hver dimension på en linje.  
    * Hvis de koncerninterne dimensioner skal være identisk med eller ligge tæt opad din almindelige dimensioner, kan du få udfyldt siden automatisk ved at vælge handlingen **Kopier fra dimensioner**. Du kan derefter redigere linjerne efter behov.
    * Hvis du har angivet en intercompany-dimensioner til en synkroniseringspartner, skal du bruge handlingen **Synkroniseringsopsætning** til at kopiere disse dimensioner.

    > [!TIP]
    > Hvis du kopierer IC-dimensioner fra en synkroniseringspartner, kan du bruge handlingen **Synkroniseringsopsætning** til at opdatere IC-dimensionerne med de ændringer, som partneren foretager.  

### Importere eller eksportere koncerninterne dimensioner  

Synkroniseringsfirmaet kan dele sine dimensioner med partnere ved at eksportere dem til en fil. Partnere kan indlæse filen for at få dimensionerne.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern konfiguration**, og vælg derefter det relaterede link.
2. Vælg handlingen **IC-dimensioner**.  
3. På siden **Koncernintern dimension** skal du vælge handlingen **Import/Eksport** og derefter vælge **Import** eller **Eksport**.
4. Vælg den fil, der skal importeres eller eksporteres.

Det næste trin er at tilknytte dimensioner til koncerninterne dimensioner. Flere oplysninger i [Sådan knyttes IC-dimensioner til dimensioner i regnskabet](#map-intercompany-dimensions-to-your-companys-dimensions).

### Tilknytte IC-dimensioner til dimensioner i regnskabet

Når du angiver de dimensioner, du skal bruge, tilknyttes hver koncernintern dimension til en af firmaets dimensioner og omvendt. Brug siden **Tilknytning af IC-dimensioner** til at angive tilknytningen. Gentag derefter processen for dimensionsværdierne.

* Angiv, hvordan IC-dimensioner på indgående transaktioner skal knyttes til dimensioner fra dit firmas dimensionsoversigt.
* Angiv, hvordan dine dimensioner skal oversættes til IC-dimensioner på *udgående transaktioner*.

Hvis nogle af IC-dimensionerne har samme kode som de tilsvarende dimensioner i virksomheden i dit eget regnskab, kan du få programmet til automatisk at knytte dimensionerne sammen:  

I følgende trin skal du først knytte IC-dimensionerne til dimensioner for indgående dokumenter på siden **IC-dimensioner**. Derefter knytter du dimensioner til IC-dimensioner for udgående dokumenter på siden **Aktuelle virksomhedsdimensioner**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern konfiguration**, og vælg derefter det relaterede link.
2. Vælg handlingen **IC-dimensioner**.
3. På siden **Koncerninterne dimensioner** skal du vælge handlingen **Dimensionstilknytning**.
4. Du kan tilknytte dimensioner automatisk eller manuelt.

    * Hvis du vil oprette tilknytningen manuelt, skal du vælge en dimension i ruderne **IC-dimensioner** og **Aktuel virksomhedsdimension** og derefter vælge en dimension i felterne **Dim. kode** og **IC-dim. kode**.
    * Hvis du automatisk vil tilknytte dimensioner, der har samme kode, skal du markere de linjer, du vil tilknytte, vælge **Tilknyt dimensioner med samme kode**-handlingen og derefter vælge de dimensioner, der skal opdateres. 

    > [!TIP]
    > Hvis du vil tilknytte mange eller alle dimensioner, skal du vælge en linje, vælge :::image type="icon" source="media/show-more-options-icon.png" border="false"::: og derefter vælge **Vælg flere**.

5. Vælg handlingen **Tilknytning af dimensionsværdier**.
6. De trin, du skal oprette tilknytningen på, svarer til det, du netop har angivet for dimensioner, på siden **Tilknytning af IC-dimensionsværdier**.

## Konfigurere koncerninterne kladdeskabeloner og batches

Du skal oprette en Finanskladdeskabelon og et finanskladdenavn, der som standard skal bruges til IC-transaktioner. Skabelonen og navnet er specielt vigtig, hvis du automatisk accepterer IC-transaktioner fra partnerne. Hvis du vil vide mere om automatisk accept af transaktioner, skal du gå til [Automatisk accept af transaktioner fra IC-partnere](#auto-accept-transactions-from-intercompany-partners).   

* Finanskladder bruges til at bogføre til finanskonti og andre konti, f.eks. bank-, debitor- og kreditorkonti. Når du bogfører via en finanskonto, oprettes der altid poster i finanskonti.  Brug siden **IC-finanskladde** til at angive det finanskladdenavn, der skal bruges. De indstillinger, der er specifikke for IC-transaktioner, er de konti, som du angiver i felterne **IC-kontotype** og **IC-kontonr**.
* De forskellige kladdeskabeloner giver dig mulighed for at arbejde med de kladder, der er beregnet til bestemte formål. Det vil sige, at felterne i hver kladdeskabeloner er netop dem, der skal bruges til en bestemt funktionalitet i programmet. Brug siden **Finanskladdeskabeloner** til at oprette en skabelon, der skal bruges til IC-transaktioner.

Hvis du vil vide mere om Finanskladdetyper og -navne, skal du gå til [Brug kladdetyper og navne](ui-work-general-journals.md#use-journal-templates-and-batches).

## Konfigurere en virksomhed til koncerninterne transaktioner

I følgende trin antages det, at en synkroniseringspartner er sat op med den kontoplan og de dimensioner, som IC-kontoplanen og-dimensionerne skal baseres på. Du kan konfigurere dem selv, men det er typisk hurtigere at komme i gang, og det er nemmere at bruge en synkroniseringspartner. Få mere at vide om synkroniseringspartneren ved at gå til [Opsætte en synkroniseringspartner](#set-up-a-synchronization-partner).

> [!TIP]
> Det er en god ide at udfylde felterne i oversigtspanelet **Generelt** på siden **Koncernintern konfiguration** for hver partner, før du tilføjer deres partnere. Når du tilføjer partnervirksomheder, der befinder sig i samme lejer, hentes [!INCLUDE [prod_short](includes/prod_short.md)] deres IC-kode og virksomhedsnavn fra opsætningen i oversigtspanelet Generelt. Feltet **Firmanavn** kontrollerer, om IC-koden er entydig.

> [!NOTE]
> Hvis du vil bruge en synkroniseringspartner, skal du lade feltet **Synkroniseringspartner** være tomt, når du indstiller det pågældende regnskab op for partnerskabet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern konfiguration**, og vælg derefter det relaterede link.  
2. Udfyld felterne i oversigtspanelet **Generelt** på siden **Koncernintern konfiguration**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> I [!INCLUDE[prod_short](includes/prod_short.md)] online kan du ikke bruge filplaceringer til at overføre transaktioner til partnerne, fordi [!INCLUDE[prod_short](includes/prod_short.md)] ikke har adgang til dit lokale netværk. Hvis du vælger **Filplacering** i feltet **Overførselstype**, er feltet **Mappesti** ikke tilgængeligt. I stedet bliver filen downloadet til mappen **Overførsler** på din computer. Derefter kan du sende filen til en person i partnervirksomheden, f.eks. via mail. Hvis du vil have en mere direkte proces, anbefales du at vælge **e-mail** i stedet.

Det næste trin er at konfigurere partnerfirmaer.

## Konfigurere koncerninterne partnere

Hver partner skal tilføje alle andre virksomheder i partnerskabet som partner.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern konfiguration**, og vælg derefter det relaterede link.
2. Vælg **Tilføj** på oversigtspanelet **IC-partnere**.
3. På siden **Koncernintern partner** skal du udfylde følgende felter. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gentag trin 2 og 3 for alle firmaer i partnerskabet.

> [!NOTE]
> Når du har aktiveret funktionen til **automatisk accept af transaktioner** på siden **Intercompany-bogføring**, vises der en [!INCLUDE[prod_short](includes/prod_short.md)]-meddelelse, der varsler om købsfakturaer, der duplikerer den oprindelige købsordre. Det er derfor vigtigt at have en forretningsproces til håndtering af dubletter. F.eks. ved at slette disse købsordrer, når købsfakturaen modtages fra IC-partneren.

### Konfigurere koncerninterne partnere som debitorer og kreditorer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern konfiguration**, og vælg derefter det relaterede link.
2. I oversigtspanelet **IC-partnere** skal du åbne kortsiden af partneren.
3. Afhængigt af hvad du vil gøre, skal du vælge debitoren eller partneren i feltet **Debitornr.** eller **kreditornr.**-felterne.

    > [!NOTE]
    > Hvis debitoren eller kreditoren ikke er oprettet, kan du vælge **+Ny** i rullemenuen for at oprette dem. Hvis du vil vide mere om, hvordan du opretter debitorer og kreditorer, skal du [Registrere nye debitorer](sales-how-register-new-customers.md) og [Registrere nye kreditorer](purchasing-how-register-new-vendors.md).

    > [!TIP]
    > Du kan også angive en debitor eller kreditor som IC-partnere ved at udfylde feltet **IC-partnerkode** på siderne **Debitorkort** og **Kreditorkort**.

### Konfigurere standardfinanskonti for IC-partnere  

Når du opretter en salgs- eller købslinje, der skal sendes som udgående IC-transaktion, angiver du en konto fra den koncerninterne kontoplan, hvor beløbet som standard bogføres på partnerens regnskab. På siden **Finanskort** kan du for de konti, som du normalt bruger på udgående koncerninterne salgslinjer eller købslinjer, angive en standardfinanskonto for en koncernintern partner. Du kan f.eks. angive de tilsvarende samlekonti fra den koncerninterne kontoplan for samlekontiene i dit eget regnskab. Tilgodehavender og skyldige beløb bruges som off-Setting-konto til IC-partneren, når du bogfører transaktioner i IC-finanskladder.  

Når du derefter angiver en finanskonto i feltet **Modkontonr.** på en koncernintern linje, hvor der står **Koncernintern partner** i feltet **Kontotype**, udfyldes feltet **Finanskonto for koncernintern partner** automatisk.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
2. Åbne finanskontoen, der bruges til koncerninterne transaktioner, og feltet **Standardfinanskonto for koncernintern partner** angives den IC-finanskonto, som partneren bogfører på, når du bogfører til finanskontoen på linjen.
3. Gentag trin 2 for hver konto, som du ofte angiver i feltet **Modkontonr.** på en linje i en IC-kladde eller et IC-dokument.

### Acceptér automatisk transaktioner fra IC-partnere

Du kan gøre det hurtigere at behandle koncerninterne transaktion ved at angive, om der automatisk oprettes kladdelinjer på baggrund af IC-partnernes indlæg fra **IC-finanskladde**-siden. Hvis du vil oprette indgående og udgående transaktioner automatisk, skal du aktivere følgende for hver partner:

* For synkroniseringspartneren skal du aktivere **Auto-send transaktioner** til siden **Koncernintern konfiguration**. Angiv derefter, hvor de modtagne IC-kladdeposteringer skal oprettes, ved at udfylde felterne i **Standardskabelon for koncerninterne finanskladder** og **Koncernintern standardfinanskladde**.

    > [!TIP]
    > Hvis feltet **Standardskabelon for koncerninterne finanskladder** er tomt, skal du oprette en Finanskladdetype, der skal bruges til IC-finanskladder. Hvis du vil vide mere om Finanskladdetyper og -navne, skal du gå til [Konfigurere koncerninterne finanskladeskabeloner og navne](#set-up-intercompany-general-journal-templates-and-batches)    

* Aktiver feltet **Auto-send transaktioner** på siden **Koncernintern konfiguration** .

Kladdelinjerne er oprettet til dig, men de er ikke bogført.

> [!NOTE]
> Hvis din organisation har brugt intercompany-funktioner i [!INCLUDE [prod_short](includes/prod_short.md)] før 2022 udgivelsesbølge 1, skal du aktivere funktionen **Acceptér automatisk IC-finanskladdetransaktioner** for automatisk at acceptere på siden **Funktionsstyring**.

### Angiv de bankkonti, der skal bruges til IC-partnere

Hvis du vil have en hurtig betaling, skal du angive en eller flere bankkonti, der skal bruges i forbindelse med IC-partnere. Når en partner bruger en IC-finanskladde til at foretage en betaling, kan han angive bankkontoen på linjen. Bankkontoen bruges som modkonto i modtagelsesfirmaet, hvilket minimerer behovet for at angive transaktioner manuelt.

* Hvis du vil angive den bankkonto, der skal bruges, skal du vælge handlingen **Bankkonti** på siden **Intercompany-partnere**. Angiv kontooplysningerne på **IC-bankkontokortet**.

## Fejlfinde koncernintern opsætning

På siden **Opsætning af intern handel** indeholder ruden **Koncernintern opsætningsdiagnosticering**, der angiver, om du har opsat alle de komponenter, der er nødvendige for at udveksle IC-transaktioner. Felterne er også tilgængelige i rollecentret forretningsregler. Vælg ruderne for at finde ud af, hvad der mangler. Du kan få vist en oversigt over de påkrævede komponenter ved at gå til [Oversigt over de trin, hvor du skal starte](#overview-of-the-steps-to-get-started).

## Se også

[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]