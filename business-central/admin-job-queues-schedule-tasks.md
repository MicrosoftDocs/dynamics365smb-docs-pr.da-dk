---
title: Planlægge sager til at køre automatisk
description: Planlagte sager styres af opgavekøen. Disse sager kører rapporter og kodeenheder. Du kan angive opgaver, der skal køres én gang eller gentagne gange.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 672, 673, 674, 671
ms.date: 10/01/2021
ms.author: edupont
ms.openlocfilehash: 9ed56b0724b19d971b8dc98ea79807423403fd83
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129761"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Du kan bruge opgavekøer til at planlægge opgaver

Jobkøer giver brugerne mulighed for at planlægge og køre specifikke rapporter og kodeenheder. Du kan angive opgaver, der skal køres én gang eller gentagne gange. Du kan f.eks. køre rapporten **Sælger * salgsstatistik** hver uge for at spore salget pr. sælger, eller du kan køre codeunit **Uddeleger godkendelsesanmodninger** dagligt for at forhindre, at dokumenter hober sig op.

Siden **Opgavekøposter** viser alle eksisterende sager. Hvis du tilføjer en ny opgavekøpost, som du vil planlægge, skal du angive nogle oplysninger. Eksempler:
* Den type objekt, du vil køre, f. eks. en rapport eller codeunit. Du skal have tilladelse til at køre den bestemte rapport eller codeunit.
* Navn og objekt-id for objektet. 
* Parametre for at angive funktionsmåden for opgavekøposten. Du kan f.eks. tilføje en parameter til kun at sende bogførte salgsordrer. 
* Når og hvor ofte, vil opgavekøposten køre.

> [!IMPORTANT]  
> Hvis du bruger tilladelsessættet SUPER, der følger med [!INCLUDE[prod_short](includes/prod_short.md)], har du og dine brugere tilladelse til at køre alle objekter inden for licensen. Dette er stadig ikke tilstrækkeligt til delegeret administrator eller brugere med enhedslicens, som ikke kan oprette en opgavekø.

Når opgavekøer er konfigureret og kører, kan status ændres på følgende måde i hver gentagede periode:

* **Afvent**  
* **Klar**  
* **Igangsat**  
* **Fejl**  
* **Færdig**  

Når en opgave er afsluttet korrekt, fjernes den fra listen over opgavekøposter, medmindre det er en tilbagevendende opgave. Hvis det er tilbagevendende opgaver, justeres feltet **Tidligste starttidspunkt** og vises, næste gang opgaven forventes at køre.  

## <a name="monitor-status-or-errors-in-the-job-queue"></a>Overvåge status eller fejl i opgavekøen

Data, som jobkøen genererer gemmes i databasen, så du kan foretage fejlfinding i opgavekøen.  

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

### <a name="to-view-status-for-any-job"></a>Sådan får du vist status for en opgave

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Poster for jobkøer**, og vælg derefter det relaterede link.
2. På siden **Opgavekøposter** skal du vælge en opgavekøpost og derefter vælge **Logposter**-handlingen.  

> [!TIP]
> Du kan også få vist status for opgavekøposter ved hjælp af Application Insights i Microsoft Azure til mere dybdegående analyse baseret på telemetri. Du kan finde flere oplysninger i [Overvågning og analyse af telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [Analyse af sporingstelemetri for opgavekøs levetid](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) i [!INCLUDE [prod_short](includes/prod_short.md)] indholdet til udviklere og administration.

## <a name="view-scheduled-tasks"></a>Vis planlagte opgaver

Siden **Planlagte opgaver** i [!INCLUDE [prod_short](includes/prod_short.md)] viser, hvilke opgaver der er klar til kørsel i opgavekøen. Siden indeholder også oplysninger om den virksomhed, som hver opgave er konfigureret til at køre i. Det er dog kun de opgaver, der er markeret som tilhørende det aktuelle miljø, der kan køres.  

F.eks. stoppes alle planlagte opgaver, hvis virksomheden er i et miljø, som er en kopi af et andet miljø. Brug siden **Planlagte opgaver** til at indstille, hvilke opgaver der er klar til kørsel i opgavekøen.  

> [!NOTE]
> Interne administratorer og brugere kan planlægge kørsel af opgaver. Uddelegerede administratorer kan ikke.

## <a name="the-my-job-queue-part"></a>Delen Min opgavekø

**Min opgavekø**-delen i dit rollecenter viser de poster i opgavekøen, som du har startet, men som ikke er færdige endnu. Som standard vises delen ikke, men du kan føje den til dit rollecenter. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).  

Delen viser følgende oplysninger:

* Hvilke dokumenter med dit id i feltet **Tildelt bruger-id**, der behandles, eller som er i kø, herunder dokumenter, der udføres i baggrunden. 
* Om der opstod fejl under bogføringen af et dokument eller i opgavekøposten. 

Min opgavekø-del giver dig også mulighed for at annullere bogføringen af et dokument.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Se en fejl fra Min opgavekø

1. I en post med status **Fejl** skal du vælge **Vis fejl**-handlingen.
2. Gennemgå fejlmeddelelsen, og løs problemet.

## <a name="examples-of-what-can-be-scheduled-using-job-queue"></a>Eksempler på, hvad der kan planlægges med jobkø

### <a name="schedule-reports"></a>Planlæg rapporter

Du kan planlægge kørsel af en rapport eller et batchjob på en bestemt dato og et bestemt klokkeslæt. Planlagte rapporter og kørsler indsættes i jobkøen og behandles på det planlagte tidspunkt, ligesom andre job. Du vælger indstillingen **Skema**, når du har valgt knappen **Send til**, og derefter angiver du oplysninger som f.eks. printer og klokkeslæt og dato, gentagelse.  

Du kan få flere oplysninger [Planlægge en rapport til kørsel](ui-work-report.md#ScheduleReport).

### <a name="schedule-synchronization-between-prod_short-and-prod_short"></a>Planlæg synkronisering mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]

Hvis du har integreret [!INCLUDE[prod_short](includes/prod_short.md)] i [!INCLUDE[prod_short](includes/cds_long_md.md)], kan du bruge opgavekøen til at planlægge, hvornår du skal synkronisere data. Afhængigt af den eller de regler, du har defineret, kan posten i opgavekøposten oprette poster i én app, så de svarer til poster i den anden app. Du kan f. eks. registrere en kontakt i [!INCLUDE[crm_md](includes/crm_md.md)], men posten i opgavekøposten kan angive den kontaktperson, du har angivet i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Planlægning af synkronisering mellem Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-the-posting-of-sales-and-purchase-orders"></a>Planlægge bogføring af salgs-og købsordrer

Du kan bruge opgavekøposter til at planlægge forretningsprocesser, der skal køres i baggrunden. For eksempel er baggrundsopgaver nyttige, når flere bruger bogfører salgsordrer op samme tid, men hvor kun én ordre kan behandles ad gangen. Du kan finde flere oplysninger i [Sådan konfigureres baggrundsbogføring med opgavekøer](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## <a name="monitor-the-job-queue-with-telemetry"></a>Overvåge opgavekøen med telemetri

Som administrator kan du bruge [Application Insights](/azure/azure-monitor/app/app-insights-overview) til at indsamle og analysere telemetri, som du kan bruge til at identificere problemer. Du kan finde flere oplysninger i [Overvågning og analyse af telemtri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) i indholdet til udviklere og administration.  

## <a name="see-also"></a>Se også

[Opsætning](admin-setup-and-administration.md)  
[Konfigurere Business Central](setup.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Analysere Job Queue Lifecycle Trace Telemetry](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]