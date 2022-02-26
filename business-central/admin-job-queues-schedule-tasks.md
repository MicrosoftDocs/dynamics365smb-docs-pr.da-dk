---
title: Planlægge sager til at køre automatisk
description: Planlagte sager styres af opgavekøen. Disse sager kører rapporter og kodeenheder. Du kan angive opgaver, der skal køres én gang eller gentagne gange.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 672, 673, 674, 671
ms.date: 10/01/2021
ms.author: edupont
ms.openlocfilehash: 46759304a312e0376e8b309b29d5e0491b34a69f
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012231"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Du kan bruge opgavekøer til at planlægge opgaver

Opgavekøer i [!INCLUDE[prod_short](includes/prod_short.md)] giver brugerne mulighed for at planlægge og køre specifikke rapporter og kodeenheder. Du kan angive opgaver, der skal køres én gang eller gentagne gange. Du kan f.eks. køre rapporten **Sælger - salgsstatistik** hver uge for at spore salget pr. sælger, eller du kan køre codeunit **Uddeleger godkendelsesanmodninger** dagligt for at forhindre, at dokumenter hober sig op eller på anden måde blokerer for arbejdsprocessen.

Siden **Opgavekøposter** viser alle eksisterende sager. Hvis du tilføjer en ny opgavekøpost, du vil planlægge, skal du angive oplysninger om typen af det objekt, du vil køre, f.eks. en rapport eller kodeenhed, og navnet og objekt-id'et for det objekt, du vil køre. Du kan også tilføje parametre for at angive funktionsmåden for opgavekøposten. Du kan f.eks. tilføje en parameter til kun at sende bogførte salgsordrer. Du skal have tilladelse til at køre den pågældende rapport eller kodeenhed, ellers genereres der en fejl, når opgavekøen køres.  
> [!IMPORTANT]  
> Hvis du bruger tilladelsessættet SUPER, der følger med [!INCLUDE[prod_short](includes/prod_short.md)], har du og dine brugere tilladelse til at køre alle objekter inden for licensen. Dette er stadig ikke tilstrækkeligt til delegeret administrator eller brugere med enhedslicens, som ikke kan oprette en opgavekø.

En opgavekø kan have mange poster, som er de opgaver, der administreres og køres i køen. Oplysninger i posten angiver, hvilken codeunit eller rapport der køres, når og hvor ofte posten køres, i hvilken kategori opgaven kører, og hvordan den køres.  

Når opgavekøer er konfigureret og kører, kan status ændres på følgende måde i hver gentagede periode:

* **Afvent**  
* **Klar**  
* **Igangsat**  
* **Fejl**  
* **Færdig**  

Når en opgave er afsluttet korrekt, fjernes den fra listen over opgavekøposter, medmindre det er en tilbagevendende opgave. Hvis det er en tilbagevendende opgave, justeres feltet **Tidligste starttidspunkt** og viser, næste gang opgaven forventes at køre.  

## <a name="monitor-status-or-errors-in-the-job-queue"></a>Overvåge status eller fejl i opgavekøen

Data, der genereres, når der køres en opgavekø, gemmes i databasen, så du kan foretage fejlfinding i opgavekøen.  

Du kan få vist og ændre status for hver opgavekøpost. Når du opretter en opgavekøpost, er dens status angivet til **Afvent**. Du kan angive status til f.eks. **Klar** og tilbage til **Afvent**. Ellers opdateres oplysninger om status i dette felt automatisk.

I følgende tabel beskrives værdierne i feltet **Status**.

| Status | Description |
|--|--|
| Klar | Angiver, at opgavekøposten er klar til at blive kørt. |
| I arbejde | Angiver, at opgavekøposten er i gang. Feltet opdateres, mens opgavekøen kører. |
| Afvent | Standard. Angiver status for opgavekøposten, da den blev oprettet. Vælg **Angiv Status som Klar** for at ændre status til **Klar**. Vælg **Indstil som Afvent** eller **Afbryd** for at ændre status tilbage til **Afvent**. |
| Fejl | Angiver, at der er en fejl. Vælg **Vis fejl** for at se fejlmeddelelsen. |
| Udført | Angiver, at opgavekøposten er fuldført. |

### <a name="to-view-status-for-any-job"></a>Sådan får du vist status for en opgave

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Poster for jobkøer**, og vælg derefter det relaterede link.
2. På siden **Opgavekøposter** skal du vælge en opgavekøpost og derefter vælge **Logposter**-handlingen.  

> [!TIP]
> Du kan også få vist status for opgavekøposter ved hjælp af Application Insights i Microsoft Azure til mere dybdegående analyse baseret på telemetri. Du kan finde flere oplysninger i [Overvågning og analyse af telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [Analyse af sporingstelemetri for opgavekøs levetid](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) i [!INCLUDE [prod_short](includes/prod_short.md)] indholdet til udviklere og administration.

## <a name="view-scheduled-tasks"></a>Vis planlagte opgaver

Siden **Planlagte opgaver** i [!INCLUDE [prod_short](includes/prod_short.md)] viser, hvilke opgaver der er klar til kørsel i opgavekøen. Siden indeholder også oplysninger om den virksomhed, som hver opgave er konfigureret til at køre i. Det er dog kun de opgaver, der er markeret som tilhørende det aktuelle miljø, der kan køres.  

Hvis det aktuelle regnskab f. eks. er i et miljø, som er en kopi af et andet miljø, stoppes alle planlagte opgaver automatisk. Brug siden **Planlagte opgaver** til at indstille, hvilke opgaver der er klar til kørsel i opgavekøen.  

> [!NOTE]
> Interne administratorer og brugere kan planlægge kørsel af opgaver. Uddelegerede administratorer kan ikke.

## <a name="the-my-job-queue-part"></a>Delen Min opgavekø

Delen **Min opgavekø** i dit rollecenter viser de poster i opgavekøen, som du har startet, men som ikke er færdige endnu. Som standard er delen ikke synlig, så du skal føje den til dit rollecenter. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).  

I denne del kan du se, hvilke dokumenter med dit id i feltet **Tildelt bruger-id**, der behandles, eller som er i kø, herunder dem, der er relateret til baggrundsbogføring. Denne del kan give dig et overblik over, om der er opstået en fejl i bogføringen af et dokument, eller om der er fejl i en opgavekøpost. Delen giver dig også mulighed for at annullere bogføringen af et dokument, hvis det ikke kører.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Se en fejl fra Min opgavekø

1. I en post med status **Fejl** skal du vælge **Vis fejl**-handlingen.
2. Gennemgå fejlmeddelelsen, og løs problemet.

## <a name="examples-of-what-can-be-scheduled-using-job-queue"></a>Eksempler på, hvad der kan planlægges med jobkø

### <a name="schedule-reports"></a>Planlæg rapporter

Du kan planlægge kørsel af en rapport eller et batchjob på en bestemt dato og et bestemt klokkeslæt. Planlagte rapporter og kørsler indsættes i jobkøen og behandles på det planlagte tidspunkt, ligesom andre job. Du vælger indstillingen **Skema**, når du har valgt knappen **Send til**, og derefter angiver du oplysninger som f.eks. printer og klokkeslæt og dato, gentagelse.  

Du kan få flere oplysninger [Planlægge en rapport til kørsel](ui-work-report.md#ScheduleReport).

### <a name="schedule-synchronization-between-prod_short-and-prod_short"></a>Planlæg synkronisering mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]

Hvis du har integreret [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)], kan du bruge opgavekøen til at planlægge, hvornår du vil synkronisere data for de poster, du har kombineret i de to forretningsapps. Afhængigt af den retning og de regler, du har defineret for integrationen, kan synkroniseringsopgaverne også oprette nye poster i destinationsappen, så de svarer til dem i kilden. Hvis en sælger f.eks. opretter en ny kontakt i [!INCLUDE[crm_md](includes/crm_md.md)], kan synkroniseringsopgaven oprette kontakten for den sammenkoblede sælger i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Planlægning af synkronisering mellem Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-the-posting-of-sales-and-purchase-orders"></a>Planlægge bogføring af salgs-og købsordrer

Opgavekøer er et effektivt værktøj til planlægning af kørsel af forretningsprocesser i baggrunden, f.eks. når mange brugere prøver at bogføre salgsordrer, men kun én ordre kan behandles ad gangen.  

Du kan finde flere oplysninger i [Sådan konfigureres baggrundsbogføring med opgavekøer](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## <a name="monitor-the-job-queue-with-telemetry"></a>Overvåge opgavekøen med telemetri

Som administrator kan du bruge [Application Insights](/azure/azure-monitor/app/app-insights-overview) til at indsamle og analysere telemetri, som du kan bruge til at identificere problemer. Du kan finde flere oplysninger i [Overvågning og analyse af telemtri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) i indholdet til udviklere og administration.  

## <a name="see-also"></a>Se også

[Opsætning](admin-setup-and-administration.md)  
[Konfigurere Business Central](setup.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Analysere Job Queue Lifecycle Trace Telemetry](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]