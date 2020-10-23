---
title: Planlægge sager til at køre automatisk | Microsoft Docs
description: Planlagte sager styres af opgavekøen. Disse sager kører rapporter og kodeenheder. Du kan angive opgaver, der skal køres én gang eller gentagne gange.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5e8c611ed5d542436f470781c92d17095ecd1f5d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924574"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Du kan bruge opgavekøer til at planlægge opgaver

Opgavekøer i [!INCLUDE[d365fin](includes/d365fin_md.md)] giver brugerne mulighed for at planlægge og køre specifikke rapporter og kodeenheder. Du kan angive opgaver, der skal køres én gang eller gentagne gange. Du kan f.eks. køre rapporten **Sælger * Salgsstatistik** hver uge for at spore salget pr. sælger, eller du kan køre codeunit **Uddeleger godkendelsesanmodninger** dagligt for at forhindre, at dokumenter hober sig op eller på anden måde blokerer for arbejdsprocessen.

Siden **Opgavekøposter** viser alle eksisterende sager. Hvis du tilføjer en ny opgavekøpost, du vil planlægge, skal du angive oplysninger om typen af det objekt, du vil køre, f.eks. en rapport eller kodeenhed, og navnet og objekt-id'et for det objekt, du vil køre. Du kan også tilføje parametre for at angive funktionsmåden for opgavekøposten. Du kan f.eks. tilføje en parameter til kun at sende bogførte salgsordrer. Du skal have tilladelse til at køre den pågældende rapport eller kodeenhed, ellers genereres der en fejl, når opgavekøen køres.  

En opgavekø kan have mange poster, som er de opgaver, der administreres og køres i køen. Oplysninger i posten angiver, hvilken codeunit eller rapport der køres, når og hvor ofte posten køres, i hvilken kategori opgaven kører, og hvordan den køres.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Sådan konfigureres baggrundsbogføring med opgavekøer

Opgavekøer er et effektivt værktøj til planlægning af kørsel af forretningsprocesser i baggrunden, f.eks. når mange brugere prøver at bogføre salgsordrer, men kun én ordre kan behandles ad gangen.  

Nedenstående fremgangsmåde beskriver, hvordan du konfigurerer baggrundsbogføring af salgsordrer. Trinnene er lignende for indkøb.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsopsætning**, og vælg derefter det relaterede link.
2. På siden **Salgsopsætning** skal du markere afkrydsningsfeltet **Bogfør med opgavekøen**.
3. Vælg feltet **Opgavekøkategorikode**, og angiv derefter koden **SALGSBOGF**.

    > [!NOTE]
    > Nogle job ændrer de samme data og bør ikke køres på samme tid, fordi det kan forårsage konflikter. Baggrundsopgaver for salgsdokumenter vil f.eks. forsøge at ændre de samme data på samme tid. Jobkøkategorier er med til at forhindre denne type konflikter ved at sikre, at et andet job, der tilhører den samme opgavekø, ikke køres, før den afsluttes. Et job, der tilhører en salgsjobkøkategori, vil f.eks. vente på, at alle andre salgsrelaterede job er udført. Du angiver en jobkøstrategi i oversigtspanelet **Baggrundsbogføring** på siden **Salgsopsætning**.
    >
    > [!INCLUDE[d365fin](includes/d365fin_md.md)] viser jobkøkategorier for salg, køb og bogføring i Finans. Det anbefales, at du altid angiver en af disse eller en af dem, du opretter. Hvis der opstår fejl pga. konflikter, skal du overveje at oprette en kategori for alle de forskellige salgs-, købs- og finanskladder.

    Hvis også salgsdokumenter skal udskrives, når de er bogført, skal du markere afkrydsningsfeltet **Bogfør og udskriv med opgavekøen** på siden **Salgsopsætning**.  

    > [!IMPORTANT]  
    > Hvis du konfigurerer et opgave, der bogfører og udskriver dokumenter, og printeren viser en dialogboks, f.eks. en anmodning om legitimationsoplysninger eller en advarsel om næsten tom blækpatron, bogføres dit dokument, men det udskrives ikke. Den tilsvarende opgavekøpost får på et tidspunkt timeout og feltet **Status** indstilles til **Fejl**. Derfor anbefaler vi, at du ikke bruger en printeropsæting, der kræver interaktion med visningen af printerdialogbokse i forbindelse med baggrundsbogføring.

    Næste gang du bogfører salgsdokumenter, opretter [!INCLUDE [prodshort](includes/prodshort.md)] automatisk en opgavekøpost for hvert dokument, og der køres job i baggrunden, ét efter ét.

4. Du kan kontrollere, at opgavekøen fungerer som forventet ved at bogføre en salgsordre. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).

5. Gennemse på siden **Logposter i opgavekø**, hvis salgsordren blev bogført korrekt. Du kan finde flere oplysninger i [Sådan får du vist status eller fejl i opgavekøen](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Sådan oprettes en opgavekøpost for baggrundsbogføring af salgsordrer

Alternativt kan du udsætte posteringer, når det er belejligt for din organisation. F.eks. giver det måske mening i din virksomhed at køre visse rutiner, når de fleste af dataindtastningerne for den pågældende dag er afsluttede. Du kan opnå dette ved at indstille opgavekøen til at køre forskellige massebogføringsrapporter, f.eks. rapporterne **Massebogfør salgsordrer**, **Massebogfør salgsfakturaer** og lignende rapporter. [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter baggrundsbogføring for alle salg, køb og servicedokumenter.

Følgende procedure viser, hvordan du kan indstille rapporten **Massebogfør salgsordrer** til automatisk bogføring af salgsordrer kl. 16 på hverdage.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opgavekøposter**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. I feltet **Objekttype, der skal aktiveres** skal du vælge **Rapport**.  
4. I feltet **Objekt-id, der skal køres** skal du vælge 296, **Massebogfør salgsordrer**.

   Du kan også bruge følgende rapporter:
  
   * 900 **Massebogfør montageordrer**
   * 497 **Massebogfør købsfakturaer**
   * 496 **Massebogfør købsordrer**
   * 498 **Massebogfør købskreditnotaer**
   * 6665 **Massebogfør købsreturv.ordrer**
   * 298 **Massebogfør salgskreditnotaer**
   * 297 **Massebogfør salgsfakturaer**
   * 296 **Massebogfør salgsordrer**
   * 6655 **Massebogfør salgsreturvareordrer**
   * 6005 **Massebogfør servicekreditnotaer**
   * 6004 **Massebogfør servicefakturaer**
   * 6001 **Kørsel - bogfør serviceordrer**

5. Marker **Siden Rapportanmodning** afkrydsningsfeltet.
6. På siden **Massebogfør salgsordrer** skal du definere, hvad der skal medtages under den automatiske bogføring af salgsordrer, og derefter vælge **OK** knappen.

    > [!IMPORTANT]
    > Husk at angive strenge filtre. Ellers vil [!INCLUDE [prodshort](includes/prodshort.md)] bogføre alle dokumenterne, selvom de ikke er klar. Overvej at angive et filter på feltet **Status** for værdien *Frigivet* og et filter på feltet **Bogføringsdato** for værdien *..i dag*. Du kan finde flere oplysninger under [Sortering, søgning og filtrering](ui-enter-criteria-filters.md).
7. Marker alle afkrydsningsfelter fra **Aktiver hver mandag** til og med **Aktiver hver fredag**.
8. I feltet **Starttidspunkt** skal du angive kl. 16.
9. Vælg handlingen **Angiv status til Klar**.

Salgsordrer, der falder inden for de definerede filtre, bogføres alle hverdage kl. 16.

> [!NOTE]
> Hvis opgavekøen ikke kan bogføre salgsordren, ændres status til **Fejlmeddelelse**, og salgsordren føjes til listen over salgsordrer, som brugeren skal håndtere manuelt. Du kan finde flere oplysninger i [Sådan får du vist status eller fejl i opgavekøen](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Når opgavekøer er konfigureret og kører, kan status ændres på følgende måde i hver gentagede periode:

* **Afvent**  
* **Klar**  
* **Igangsat**  
* **Fejl**  
* **Færdig**  

Når en opgave er afsluttet korrekt, fjernes den fra listen over opgavekøposter, medmindre det er en tilbagevendende opgave. Hvis det er en tilbagevendende opgave, justeres feltet **Tidligste starttidspunkt** og viser, næste gang opgaven forventes at køre.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Sådan får du vist status eller fejl i opgavekøen
Data, der genereres, når der køres en opgavekø, gemmes i databasen, så du kan foretage fejlfinding i opgavekøen.

### <a name="to-view-status-for-any-job"></a>Sådan får du vist status for en opgave
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opgavekøposter**, og vælg derefter det relaterede link.
2. På siden **Opgavekøposter** skal du vælge en opgavekøpost og derefter vælge **Logposter**-handlingen.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Sådan vises status fra et salgs- eller købsdokument
1. I det dokument, du har forsøgt at bogføre med baggrundsbogføring, skal du vælge feltet **Opgavekøstatus**, der indeholder **Fejl**.
2. Gennemgå fejlmeddelelsen, og løs problemet.

## <a name="the-my-job-queue-part"></a>Delen Min opgavekø
Delen **Min opgavekø** i dit rollecenter viser de poster i opgavekøen, som du har startet, men som ikke er færdige endnu. Som standard er delen ikke synlig, så du skal føje den til dit rollecenter. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).  

I denne del kan du se, hvilke dokumenter med dit id i feltet **Tildelt bruger-id**, der behandles, eller som er i kø, herunder dem, der er relateret til baggrundsbogføring. Denne del kan give dig et overblik over, om der er opstået en fejl i bogføringen af et dokument, eller om der er fejl i en opgavekøpost. Delen giver dig også mulighed for at annullere bogføringen af et dokument, hvis det ikke kører.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Se en fejl fra Min opgavekø
1. I en post med status **Fejl** skal du vælge **Vis fejl**-handlingen.
2. Gennemgå fejlmeddelelsen, og løs problemet.

## <a name="security"></a>Sikkerhed  
Opgavekøposter kører på basis af tilladelser. Disse tilladelser skal tillade kørsel af rapporten eller codeunit'en.  

Når en opgavekø aktiveres manuelt, køres den med legitimationsoplysningerne for brugeren. Når en opgavekø aktiveres som en planlagt opgave, køres den med legitimationsoplysningerne for serverforekomsten. Når en opgave kører, køres den med legitimationsoplysningerne for den opgavekø, der aktiverede den. Men den bruger, der oprettede opgavekøposten, skal dog også have tilladelser. Når en opgave er "Kør i brugersession" (f.eks. i baggrundsbogføring), køres den med legitimationsoplysningerne for den bruger, der oprettede jobbet.  

> [!IMPORTANT]  
> Hvis du bruger tilladelsessættet SUPER, der følger med [!INCLUDE[d365fin](includes/d365fin_md.md)], har du og dine brugere tilladelse til at køre alle objekter. I dette tilfælde begrænses adgangen for hver bruger kun af tilladelser til data.  

## <a name="using-job-queues-effectively"></a>Effektiv brug af opgavekøer  
Opgavekøposten har mange felter, hvis formål er at overføre parametre i en codeunit, du har angivet til kørsel sammen med en opgavekø. Det betyder også, at codeunits, der skal køres via opgavekøen, skal angives med opgavekøposten som en parameter i udløseren **OnRun**. Dette giver et ekstra niveau af sikkerhed, da dette forhindrer brugerne i at køre vilkårlige kodeenheder via opgavekøen. Hvis brugeren skal overføre parametre til en rapport, er den eneste måde at gøre dette ved at placere rapportudførelsen i en codeunit, som derefter analyserer inputparametrene og skriver dem i rapporten, før den udføres.  

## <a name="scheduling-synchronization-between-d365fin-and-d365fin"></a>Sådan planlægger du synkronisering mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)]

Hvis du har integreret [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[d365fin](includes/cds_long_md.md)], kan du bruge opgavekøen til at planlægge, hvornår du vil synkronisere data for de poster, du har kombineret i de to forretningsapps. Afhængigt af den retning og de regler, du har defineret for integrationen, kan synkroniseringsopgaverne også oprette nye poster i destinationsappen, så de svarer til dem i kilden. Hvis en sælger f.eks. opretter en ny kontakt i [!INCLUDE[crm_md](includes/crm_md.md)], kan synkroniseringsopgaven oprette kontakten for den sammenkoblede sælger i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger under [Planlægning af synkronisering mellem Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

## <a name="see-also"></a>Se også

[Opsætning](admin-setup-and-administration.md)  
[Konfigurere Business Central](setup.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
