---
title: Planlægge sager til at køre automatisk
description: 'Få mere at vide om, hvordan du bruger Opgavekøposter til at køre rapporter og kodeenheder.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 08/24/2023
ms.custom: bap-template
ms.search.form: '672, 673, 674, 671'
---
# Du kan bruge opgavekøer til at planlægge opgaver

Brug siden **Opgavekøposter** til at planlægge og køre specifikke rapporter og kodeenheder. Du kan angive opgaver, der skal køres én gang eller gentagne gange. Du kan f.eks. køre rapporten **Sælger * salgsstatistik** hver uge for at spore salget pr. sælger, eller du kan køre codeunit **Uddeleger godkendelsesanmodninger** dagligt for at forhindre, at dokumenter hober sig op.

Siden Opgavekøposter viser alle eksisterende sager. Hvis du tilføjer en ny opgavekøpost, der skal køres i en plan, skal du angive nogle oplysninger. Eksempler:

* Den type objekt, der skal køres, f. eks. en rapport eller codeunit. Du skal have tilladelse til at køre den bestemte rapport eller codeunit.
* Navn og objekt-id for objektet.
* Parametre for at angive funktionsmåden for opgavekøposten. Du kan f.eks. tilføje en parameter til kun at sende bogførte salgsordrer.
* Når og hvor ofte, vil opgavekøposten køre.

> [!IMPORTANT]  
> Hvis du er tildelt tilladelsessættet SUPER, der følger med [!INCLUDE[prod_short](includes/prod_short.md)], har du tilladelse til at køre alle objekter inden for licensen. Hvis du har rollen Stedfortræderadministrator, kan du oprette og planlægge opgavekøposter, men kun administratorer og licenserede brugere kan køre dem.

Når opgavekøer er konfigureret og kører, kan status ændres på følgende måde i hver gentagede periode:

* **I venteposition**  
* **Klar**  
* **Igangsat**  
* **Fejl**  
* **Færdig**  
* **Afvent pga. inaktivitet**

> [!NOTE]
> Statussen **Sat på pause pga. inaktivitet** bruges primært til opgavekøposter, der planlægger synkronisering mellem [!INCLUDE [prod_short](includes/prod_short.md)] og et andet program, f.eks. [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Hvis du vil vide mere om denne status, skal du gå til [Om inaktivitets timeout](/dynamics365/business-central/admin-scheduled-synchronization-using-the-synchronization-job-queue-entries#about-inactivity-timeouts).

Når en opgave er afsluttet korrekt, fjernes den fra listen over opgavekøposter, medmindre det er en tilbagevendende opgave. Hvis det er tilbagevendende opgaver, justeres feltet **Tidligste starttidspunkt** og vises, næste gang opgaven forventes at køre.  

## Den tidligste startdato

Værdien i feltet **Tidligste startdato/-tidspunkt** på siden **Kort til opgavekøpost** vises, næste gang opgaven køres. Der er flere faktorer, der kan påvirke, om en opgavekøpost rent faktisk kører på det pågældende tidspunkt.

De mest almindelige faktorer er antallet af opgavekøposter i et miljø og det samlede antal planlagte opgaver. For at beskytte ydeevneniveauer er der operationelle grænser. Hvis der er mange poster i køen, og f.eks. en af dem mislykkes, eller posterne bare tager længere tid end forventet, starter den næste opgave muligvis ikke på det forventede tidspunkt. Hvis du har kodeenheder, der genererer 100.000 eller flere planlagte opgaver, bør du undersøge, om du rent faktisk har brug for alle disse opgaver. Du kan få adgang til listen over alle planlagte opgaver på siden **Planlagte opgaver**.

Du kan få mere at vide om overvågning af status for opgavekøposter ved at gå til [Sådan får du vist status for en opgave](#to-view-status-for-any-job). Du kan få mere at vide om driftsgrænser ved at gå til [Asynkrone opgavegrænser](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#Task).

## Overvåge status eller fejl i opgavekøen

Data, som jobkøen genererer gemmes, så du kan foretage fejlfinding.  

Du kan få vist og ændre status for hver opgavekøpost. Når du opretter en opgavekøpost, er dens status angivet til **Afvent**. Du kan angive status til f.eks. **Klar** og tilbage til **Afvent**. Ellers opdateres oplysninger om status i dette felt automatisk.

I følgende tabel beskrives værdierne i feltet **Status**.

| Status | Beskrivelse |
|--|--|
| Klar | Jobkøposten er klar til at blive kørt. |
| Igangsat | Opgavekøposten er i gang. Feltet opdateres, mens opgavekøen kører. |
| I venteposition | Standardstatus for opgavekøposten, da den blev oprettet. Vælg **Angiv Status som Klar** for at ændre status til **Klar**. Vælg handlingen **Indstil som afvent** omdannes status til **Afvent**. |
| Fejl | Noget gik galt. Vælg **Vis fejl** for at se fejlmeddelelsen. |
| Afsluttet | Opgavekøposten er fuldført. |

> [!Tip]  
> Opgavekøposten holder op med at køre, når der er en fejl. Dette kan f. eks. være et problem, når en post opretter forbindelse til en ekstern tjeneste, f. eks. en arkføder. Hvis tjenesten midlertidigt ikke er tilgængelig, og opgavekøposten ikke kan oprette forbindelse, viser posten en fejl og stopper med at køre. Du skal genstarte opgavekøposten manuelt. Men **Maks. antal forsøg** og **Forsinkelse før genkørsel (sek.)** kan hjælpe dig med at undgå denne situation. Feltet **Maks. af feltet forsøg** giver dig mulighed for at angive, hvor mange gange opgavekøposten skal mislykkes, før det forsøges at køre. Feltet **Kør forsinkelse igen (sek.)** giver dig mulighed for at angive, hvor lang tid, der skal være mellem forsøg. Kombinationen af disse to felter kan holde opgavekøposten kørende, indtil den eksterne tjeneste bliver tilgængelig.

### Sådan får du vist status for en opgave

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Poster for jobkøer**, og vælg derefter det relaterede link.
2. På siden **Opgavekøposter** skal du vælge en opgavekøpost og derefter vælge **Logposter**-handlingen.  

> [!TIP]
> Du kan også få vist status for opgavekøposter ved hjælp af Application Insights i Microsoft Azure til mere dybdegående analyse baseret på telemetri. Hvis du vil vide mere om telemetri, skal du gå til [Overvåge og analysere telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [Analysere opgavekøens levetidssporing](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

## Vis planlagte opgaver

Siden **Planlagte opgaver** i [!INCLUDE [prod_short](includes/prod_short.md)] viser, hvilke opgaver der er klar til kørsel i opgavekøen. Siden indeholder også oplysninger om den virksomhed, som hver opgave er konfigureret til at køre i. Det er dog kun de opgaver, der er markeret som tilhørende det aktuelle miljø, der kan køres.  

F.eks. stoppes alle planlagte opgaver, hvis virksomheden er i et miljø, som er en kopi af et andet miljø. Brug siden **Planlagte opgaver** til at indstille, hvilke opgaver der er klar til kørsel i opgavekøen.  

> [!NOTE]
> Interne administratorer og brugere med licens kan planlægge kørsel af opgaver. Stedfortræderadministratorer kan oprette og planlægge opgaver til kørsel, men kun licenserede brugere kan køre dem.

## Min opgavekødel

**Min opgavekø**-delen i dit rollecenter viser de poster i opgavekøen, som du har startet, men som ikke er færdige endnu. Som standard vises delen ikke, men du kan føje den til dit rollecenter. Du kan finde flere oplysninger om tilpasning under [Tilpasse dit arbejdsområde](ui-personalization-user.md).  

Delen viser følgende oplysninger:

* Hvilke dokumenter med dit id i feltet **Tildelt bruger-id**, der behandles, eller som er i kø, herunder dokumenter, der udføres i baggrunden. 
* Om der opstod fejl under bogføringen af et dokument eller i opgavekøposten. 

Min opgavekø-del giver dig også mulighed for at annullere bogføringen af et dokument.

### Se en fejl fra Min opgavekø

1. I en post med status **Fejl** skal du vælge **Vis fejl**-handlingen.
2. Gennemgå fejlmeddelelsen, og løs problemet.

## Eksempler på, hvad der kan planlægges med jobkøelementer

### Planlæg rapporter

Du kan planlægge kørsel af en rapport eller et batchjob på en bestemt dato og et bestemt klokkeslæt. Planlagte rapporter og kørsler indsættes i jobkøen og behandles på det planlagte tidspunkt, ligesom andre job. Du vælger indstillingen **Skema**, når du har valgt knappen **Send til**, og derefter angiver du oplysninger som f.eks. printer og klokkeslæt og dato, gentagelse.  

Hvis du vil vide mere om planlægning, skal du fortsætte med at [Planlægge, at rapporten skal køres](ui-work-report.md#ScheduleReport)

### Planlæg synkronisering mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]

Hvis du har integreret [!INCLUDE[prod_short](includes/prod_short.md)] i [!INCLUDE[prod_short](includes/cds_long_md.md)], kan du bruge opgavekøen til at planlægge, hvornår du skal synkronisere data. Afhængigt af den eller de regler, du har defineret, kan posten i opgavekøposten oprette poster i én app, så de svarer til poster i den anden app. Du kan f. eks. registrere en kontakt i [!INCLUDE[crm_md](includes/crm_md.md)], men posten i opgavekøposten kan angive den kontaktperson, du har angivet i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger om planlægning i [Planlægning af synkronisering mellem Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### Planlægge bogføring af salgs-og købsordrer

Du kan bruge opgavekøposter til at planlægge forretningsprocesser, der skal køres i baggrunden. For eksempel er baggrundsopgaver nyttige, når flere bruger bogfører salgsordrer op samme tid, men hvor kun én ordre kan behandles ad gangen. Hvis du vil vide mere om bogføring af baggrunden, skal du gå til [Sådan konfigureres baggrundsbogføring med opgavekøer](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## Håndter problemer med opgavekøposter

Hvis en opgavekøpost viser en fejl, er den første mulighed for at løse problemet ved at genstarte opgavekøposten. Du kan angive status for opgavekøposten til **Venter** og derefter **Klar** eller bare genstarte.

Hvis det ikke hjælper at genstarte, kan problemet være i koden. Du kan finde ejeren (også kaldet *Udgiveren*) af koden i sporing af AL stak i logfilen til opgavekøen. Hvis fejlen opstår fra en app/udvidelse, skal du kontakte din Microsoft-partner. Hvis fejlen stammer fra et Microsoft-program, skal du åbne en supportanmodning hos Microsoft.

Hvis du kontakter din Microsoft-partner eller Microsoft for at få support, skal du angive følgende oplysninger:

* Id for det jobkøelement, hvor fejlen er opstået
* Tidsstemplet for, hvornår fejlen opstod
* Din tidszone

> [!TIP]
> Afhængigt af om din [!INCLUDE [prod_short](includes/prod_short.md)] er tidligere er ældre eller nyere end version 22.1, skal du indsamle oplysningerne på følgende måder:
>
> * Til tidligere versioner skal du angive et skærmbillede af siden **logposter i opgavekø**.
> * Til senere versioner skal du bruge handlingen **Kopier detaljer** på siden logførte logposter i opgavekø til at kopiere oplysningerne (kø-id, tidsstempel og tidszone).

## Overvåge opgavekøen med telemetri

Administratorer kan bruge [Azure Application Insights](/azure/azure-monitor/app/app-insights-overview) til at indsamle og analysere telemetri, som kan hjælpe med at identificere problemer. Hvis du vil vide mere om telemetri, skal du gå til [Overvåge og analysere telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [Analysere opgavekøens levetidssporing](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

Med telemetri får administratorer mulighed for at konfigurere påmindelser i forbindelse med jobkøer, der sender en SMS-besked, e-mail eller en meddelelse i grupper, hvis noget ikke er korrekt. Du kan få mere at vide om disse beskeder [Besked på telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-alert).

## Se også

[Opsætning](admin-setup-and-administration.md)  
[Konfigurere Business Central](setup.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Analysere Job Queue Lifecycle Trace Telemetry](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  
[Besked om telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-alert)

[!INCLUDE[footer-include](includes/footer-banner.md)]
