---
title: Planlægge sager til at køre automatisk
description: 'Få mere at vide om, hvordan du bruger Opgavekøposter til at køre rapporter og kodeenheder.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 07/16/2024
ms.custom: bap-template
ms.search.form: '672, 673, 674, 671'
ms.service: dynamics-365-business-central
---
# <a name="use-job-queues-to-schedule-tasks"></a>Bruge sagskøer til at planlægge opgaver

Brug siden **Opgavekøposter** til at planlægge og køre specifikke rapporter og kodeenheder. Du kan angive opgaver, der skal køres én gang eller gentagne gange. Du kan f.eks. køre rapporten **Sælger * salgsstatistik** hver uge for at spore salget pr. sælger, eller du kan køre codeunit **Uddeleger godkendelsesanmodninger** dagligt for at forhindre, at dokumenter hober sig op.

Siden **Opgavekøposter** viser alle eksisterende sager. Hvis du tilføjer en ny opgavekøpost, der kører i en plan, skal du angive nogle oplysninger. Eksempler:

* Den type objekt, der skal køres, f. eks. en rapport eller codeunit. Du skal have tilladelse til at køre rapporten eller codeunit.
* Navn og objekt-id for objektet.
* Parametre for at angive funktionsmåden for opgavekøposten. Du kan f.eks. tilføje en parameter til kun at sende bogførte salgsordrer.
* Planen for, hvornår og hvor ofte opgavekøposten kører.

> [!IMPORTANT]  
> Hvis du er tildelt tilladelsessættet SUPER, der følger med [!INCLUDE[prod_short](includes/prod_short.md)], har du tilladelse til at køre alle objekter inden for licensen. Hvis du har rollen Stedfortræderadministrator, kan du oprette og planlægge opgavekøposter, men kun administratorer og licenserede brugere kan køre dem.

Når en opgave er afsluttet korrekt, fjernes [!INCLUDE [prod_short](includes/prod_short.md)] fra listen over opgavekøposter, medmindre det er en tilbagevendende opgave. Hvis det er tilbagevendende opgaver, justeres feltet **Tidligste starttidspunkt** og vises, næste gang opgaven forventes at køre.

## <a name="important-for-scheduling-recurring-jobs"></a>Vigtigt for at planlægge gentagne opgaver

> [!IMPORTANT]  
> Tilbagevendende opgavekøer kan påvirke ydeevnen, så du bør ikke køre dem for ofte. Når du angiver, hvor ofte en gentaget opgave skal udføres, skal du prøve at angive det størst mulige tidsinterval. For eksempel, hvis du er ved at indstille en gentagelse på fem minutter, skal du overveje, om det kan være 15 minutter eller endda en gang i timen i stedet. Når du planlægger gentagne opgavekøer, skal du overveje, hvilke områder af programmet jobbet vil påvirke. Er det et område, hvor mange brugere arbejder og vil blive påvirket af kraftig aktivitet? Overvej længden af en enkelt jobkørsel og de forretningsmæssige motivationer for at køre job med en given kadence.

## <a name="the-earliest-start-date"></a>Den tidligste startdato

Værdien i feltet **Tidligste startdato/-tidspunkt** på siden **Kort til opgavekøpost** vises, næste gang opgaven køres. Der er flere faktorer, der kan påvirke, om en opgavekøpost rent faktisk kører på det pågældende tidspunkt.

De mest almindelige faktorer er antallet af opgavekøposter i et miljø og det samlede antal planlagte opgaver. For at beskytte ydeevneniveauer er der operationelle grænser. Hvis der er mange poster i køen, og f.eks. en af dem mislykkes, eller tager længere tid end forventet, starter den næste opgave muligvis ikke på det forventede tidspunkt. Hvis du har kodeenheder, der genererer 100.000 eller flere planlagte opgaver, bør du undersøge, om du rent faktisk har brug for alle disse opgaver. Du kan få adgang til listen over alle planlagte opgaver på siden **Planlagte opgaver**.

Du kan få mere at vide om overvågning af status for opgavekøposter ved at gå til [Sådan får du vist status for en opgave](#to-view-status-for-any-job). Du kan få mere at vide om driftsgrænser ved at gå til [Asynkrone opgavegrænser](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#Task).

## <a name="monitor-status-or-errors-in-the-job-queue"></a>Overvåge status eller fejl i opgavekøen

Data, som jobkøen genererer gemmes, så du kan foretage fejlfinding.  

Du kan få vist og ændre status for hver opgavekøpost. Når du opretter en opgavekøpost, er dens status angivet til **Afvent**. Du kan angive status til f.eks. **Klar** og tilbage til **Afvent**. Ellers opdateres oplysninger om status i dette felt automatisk.

I følgende tabel beskrives værdierne i feltet **Status**.

| Status | Beskrivelse |
|--|--|
| Klar | Jobkøposten er klar til at blive kørt. |
| Igangsat | Opgavekøposten er i gang. Feltet opdateres, mens opgavekøen kører. |
| I venteposition | Standardstatus for opgavekøposten, da den blev oprettet. Vælg **Angiv Status som Klar** for at ændre status til **Klar**. Vælg handlingen **Indstil som afvent** omdannes status til **Afvent**. Du kan få mere at vide ved at gå til [Om I venteposition](#about-on-hold).|
| Afvent pga. inaktivitet | Brugt primært til opgavekøposter, der planlægger synkronisering mellem [!INCLUDE [prod_short](includes/prod_short.md)] og et andet program, f.eks. [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Hvis du vil vide mere om denne status, skal du gå til [Om inaktivitets timeout](/dynamics365/business-central/admin-scheduled-synchronization-using-the-synchronization-job-queue-entries#about-inactivity-timeouts). |
|Venter | Kun relevant for opgavekøposter, der er tildelt en kategorikode. Angiver, at opgaven er planlagt, men at den underliggende planlagte opgave ikke er aktiv. Når den opgavekøpost, der aktuelt kører, og som er i samme kategori, er afsluttet, bliver status for den næste opgave i kategorien med statussen Venter til Klar. |
| Fejl | Noget gik galt. Vælg **Vis fejl** for at se fejlmeddelelsen. |
| Afsluttet | Opgavekøposten er fuldført. |

 > [!TIP]  
> Opgavekøposten holder op med at køre, når der er en fejl. Dette kan f. eks. være et problem, når en post opretter forbindelse til en ekstern tjeneste, f. eks. en arkføder. Hvis tjenesten midlertidigt ikke er tilgængelig, og opgavekøposten ikke kan oprette forbindelse, viser posten en fejl og stopper med at køre. Du skal genstarte opgavekøposten manuelt. Men **Maks. antal forsøg** og **Forsinkelse før genkørsel (sek.)** kan hjælpe dig med at undgå denne situation. Feltet **Maks. af feltet forsøg** giver dig mulighed for at angive, hvor mange gange opgavekøposten skal mislykkes, før det forsøges at køre. Feltet **Kør forsinkelse igen (sek.)** giver dig mulighed for at angive, hvor lang tid, der skal være mellem forsøg. Kombinationen af disse to felter kan holde opgavekøposten kørende, indtil den eksterne tjeneste bliver tilgængelig.

### <a name="about-on-hold"></a>Om I venteposition

Hvis du angiver en opgavekøpost til **I venteposition**, påvirker det ikke et job, der allerede kører. Når et job starter, fortsætter den, indtil den er færdig, uanset eventuelle efterfølgende ændringer af opgavekøposten, f.eks. hvis den sættes i venteposition.<br><br>Status **I venteposition** bruges typisk til at forhindre, at et job starter automatisk, når det planlagte starttidspunkt nås. Det giver dig mulighed for midlertidigt at sætte et job på pause, før det begynder at blive behandlet. <br><br>Hvis du har brug for at stoppe eller annullere et kørende job, kan du manuelt gribe ind i processen. Du kan f.eks. stoppe den tilsvarende session eller proces.

### <a name="to-view-status-for-any-job"></a>Sådan får du vist status for en opgave

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Poster for jobkøer**, og vælg derefter det relaterede link.
2. På siden **Opgavekøposter** skal du vælge en opgavekøpost og derefter vælge **Logposter**-handlingen.  

> [!TIP]
> Du kan også få vist status for opgavekøposter ved hjælp af Application Insights i Microsoft Azure til mere dybdegående analyse baseret på telemetri. Hvis du vil vide mere om telemetri, skal du gå til [Overvåge og analysere telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [Analysere opgavekøens levetidssporing](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

## <a name="view-scheduled-tasks"></a>Vis planlagte opgaver

Siden **Planlagte opgaver** i [!INCLUDE [prod_short](includes/prod_short.md)] viser, hvilke opgaver der er klar til kørsel i opgavekøen. Siden indeholder også oplysninger om den virksomhed, som hver opgave er konfigureret til at køre i. Det er dog kun de opgaver, der er markeret som tilhørende det aktuelle miljø, der kan køres.  

F.eks. stoppes alle planlagte opgaver, hvis virksomheden er i et miljø, som er en kopi af et andet miljø. Brug siden **Planlagte opgaver** til at indstille, hvilke opgaver der er klar til kørsel i opgavekøen.  

> [!NOTE]
> Interne administratorer og brugere med licens kan planlægge kørsel af opgaver. Stedfortræderadministratorer kan oprette og planlægge opgaver til kørsel, men kun licenserede brugere kan køre dem.

## <a name="the-my-job-queue-part"></a>Min opgavekødel

**Min opgavekø**-delen i dit rollecenter viser de poster i opgavekøen, som du har startet, men som ikke er færdige endnu. Som standard vises delen ikke, men du kan føje den til dit rollecenter. Du kan finde flere oplysninger om tilpasning under [Tilpasse dit arbejdsområde](ui-personalization-user.md).  

Delen viser følgende oplysninger:

* Hvilke dokumenter med dit id i feltet **Tildelt bruger-id**, der behandles, eller som er i kø, herunder dokumenter, der udføres i baggrunden. 
* Om der opstod fejl under bogføringen af et dokument eller i opgavekøposten. 

Min opgavekø-del giver dig også mulighed for at annullere bogføringen af et dokument.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Se en fejl fra Min opgavekø

1. I en post med status **Fejl** skal du vælge **Vis fejl**-handlingen.
2. Gennemgå fejlmeddelelsen, og løs problemet.

## <a name="examples-of-what-you-can-schedule-using-job-queue-entries"></a>Eksempler på, hvad der kan planlægges med jobkøelementer

### <a name="schedule-reports"></a>Planlæg rapporter

Du kan planlægge kørsel af en rapport eller et batchjob på en bestemt dato og et bestemt klokkeslæt. Planlagte rapporter og kørsler indsættes i jobkøen og behandles på det planlagte tidspunkt, ligesom andre job. Du vælger indstillingen **Skema**, når du har valgt knappen **Send til**, og derefter angiver du oplysninger som f.eks. printer og klokkeslæt og dato, gentagelse.  

Hvis du vil vide mere om planlægning, skal du fortsætte med at [Planlægge, at rapporten skal køres](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between--and-includeprod_short"></a>Planlæg synkronisering mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]

Hvis du integrerer [!INCLUDE[prod_short](includes/prod_short.md)] i [!INCLUDE[prod_short](includes/cds_long_md.md)], kan du bruge opgavekøen til at planlægge, hvornår du skal synkronisere data. Afhængigt af retningen og reglerne, du har defineret, kan posten i opgavekøposten oprette poster i én app, så de svarer til poster i den anden app. Du kan f. eks. registrere en kontakt i [!INCLUDE[crm_md](includes/crm_md.md)], men posten i opgavekøposten kan angive den kontaktperson, du har angivet i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger om planlægning i [Planlægning af synkronisering mellem Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-when-to-post-sales-and-purchase-orders"></a>Planlægge bogføring af salgs-og købsordrer

Du kan bruge opgavekøposter til at planlægge forretningsprocesser, der skal køres i baggrunden. For eksempel er baggrundsopgaver nyttige, når flere bruger bogfører salgsordrer op samme tid, men hvor kun én ordre kan behandles ad gangen. Hvis du vil vide mere om bogføring af baggrunden, skal du gå til [Sådan konfigureres baggrundsbogføring med opgavekøer](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## <a name="handle-job-queue-entry-issues"></a>Håndter problemer med opgavekøposter

Hvis en opgavekøpost viser en fejl, er den første mulighed for at løse problemet ved at genstarte opgavekøposten. Du kan angive status for opgavekøposten til **Venter** og derefter **Klar** eller bare genstarte.

Hvis det ikke hjælper at genstarte, kan problemet være i koden. Du kan finde ejeren (også kaldet *Udgiveren*) af koden i sporing af AL stak i logfilen til opgavekøen. Hvis fejlen opstår fra en app/udvidelse, skal du kontakte din Microsoft-partner. Hvis fejlen stammer fra et Microsoft-program, skal du åbne en supportanmodning hos Microsoft.

Hvis du kontakter din Microsoft-partner eller Microsoft for at få support, skal du angive følgende oplysninger:

* Id'et for opgavekøposten kører der, hvor fejlen opstod
* Tidsstemplet for, hvornår fejlen opstod
* Din tidszone

> [!TIP]
> Afhængigt af om din [!INCLUDE [prod_short](includes/prod_short.md)] er tidligere er ældre eller nyere end version 22.1, skal du indsamle oplysningerne på følgende måder:
>
> * Til tidligere versioner skal du angive et skærmbillede af siden **logposter i opgavekø**.
> * Til senere versioner skal du bruge handlingen **Kopier detaljer** på siden logførte logposter i opgavekø til at kopiere oplysningerne (kø-id, tidsstempel og tidszone).

## <a name="monitor-the-job-queue-with-telemetry"></a>Overvåge opgavekøen med telemetri

Administratorer kan bruge [Azure Application Insights](/azure/azure-monitor/app/app-insights-overview) til at indsamle og analysere telemetri, som kan hjælpe med at identificere problemer. Hvis du vil vide mere om telemetri, skal du gå til [Overvåge og analysere telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [Analysere opgavekøens levetidssporing](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

Med telemetri får administratorer mulighed for at konfigurere påmindelser i forbindelse med jobkøer, der sender en SMS-besked, e-mail eller en meddelelse i grupper, hvis noget ikke er korrekt. Du kan få mere at vide om disse beskeder [Besked på telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-alert).

## <a name="see-also"></a>Se også

[Opsætning](admin-setup-and-administration.md)  
[Konfigurere Business Central](setup.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Analysere Job Queue Lifecycle Trace Telemetry](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  
[Besked om telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-alert)

[!INCLUDE[footer-include](includes/footer-banner.md)]
